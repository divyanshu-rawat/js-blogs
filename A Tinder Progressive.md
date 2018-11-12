## A Tinder Progressive Web App Performance Case Study.

Tinder recently swiped right on the web. Their new responsive Progressive Web App — [Tinder Online](https://tinder.com/) — is available to 100% of users on desktop and mobile, employing techniques for **JavaScript performance optimization** , **Service Workers for network resilience** and **Push Notifications for chat engagement**. Today we’ll walk through some of their web perf learnings

The MVP for the PWA took 3 months to implement using React as their UI library and Redux for state management. The result of their efforts is a PWA that delivers the core Tinder experience in 10% of the data-investment costs for someone in a data-costly or data-scarce market.

*The PWA loads code for new routes on demand, and the cost of additional code is amortized over the lifetime of the application. Subsequent navigations still don’t cost as much data as the download of the app.*

Early signs show good swiping, messaging and session length compared to the native app. With the PWA:

* Users swipe more on web than their native apps
* Users message more on web than their native apps
* Users purchase on par with native apps
* Users edit profiles more on web than on their native apps
* Session times are longer on web than their native apps

Testing the new experience on WebPageTest and Lighthouse (using the Galaxy S7 on 4G) we can see that they’re able to load and get interactive in under 5 seconds.

**Performance Optimization** : Tinder were able to improve how quickly their pages could load and become interactive through a number of techniques. They implemented route-based code-splitting, introduced performance budgets and long-term asset caching.

#### Route-level code-splitting

Tinder initially had large, monolithic JavaScript bundles that delayed how quickly their experience could get interactive. These bundles contained code that *wasn’t immediately needed to boot-up the core user experience, so it could be broken up using code-splitting.* **It’s generally useful to only ship code users need upfront and lazy-load the rest as needed.**

To accomplish this, Tinder used *React Router* and *React Loadable*. As their application centralized all their route and rendering info a configuration base, they found it straight-forward to implement code splitting at the top level.

* After adding code-splitting, components A and B could be loaded as and when needed. Tinder did this by introducing React Loadable, dynamic import() and webpack’s magic comment syntax (for naming dynamic chunks) to their JS:

* For “vendor” (library) chunking, Tinder used the webpack CommonsChunkPlugin to move commonly used libraries across routes up to a single bundle file that could be cached for longer periods of time:

* Next, Tinder used React Loadable’s preload support to preload potential resources for the next page on control component:

* [SERVICE WORLKERS](https://developers.google.com/web/fundamentals/primers/service-workers/)

* Tinder also used Service Workers to precache all their route level bundles and include routes that users are most likely to visit in the main bundle without code-splitting. They’re of course also using common optimizations like JavaScript minification via UglifyJS.

* [THIRD PARTY LIB](https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/loading-third-party-javascript/)

* [Web Push Notifications: Timely, Relevant, and Precise](https://www.google.co.in/search?q=ff&client=ubuntu&espv=2&biw=1317&bih=654&source=lnms&tbm=nws&sa=X&ved=0ahUKEwiat_2su4rOAhUKK48KHWaDBkYQ_AUICSgE)

#### Preloading late-discovered resources

As a refresher, <link rel=preload> is a declarative instruction to the browser to *load critical, late-discovered resources earlier on.* In single-page applications, these resources can sometimes be JavaScript bundles.

Tinder implemented support for to preload their critical JavaScript/webpack bundles that were important for the core experience. This reduced load time by 1s and first paint from 1000ms to about 500ms.

#### Performance Budget

Tinder adopted performance budgets for helping them hit their performance goals on mobile. As Alex Russell noted in “Can you afford it?: real-world performance budgets”, you have a limited headroom to deliver an experience when considering slow 3G connections being used on median mobile hardware.

* [Can you afford it]?(https://infrequently.org/2017/10/can-you-afford-it-real-world-web-performance-budgets/)
* To get and stay interactive quickly, Tinder enforced a budget of ~155KB for their main and vendor chunks, asynchronous (lazily loaded) chunks are ~55KB and other chunks are ~35KB. CSS has a limit of 20KB. This was crucial to ensuring they were able to avoid regressing on performance.

#### Webpack Bundle Analysis

* [Webpack Bundle Analyzer](https://github.com/webpack-contrib/webpack-bundle-analyzer) allows you to discover what the dependency graph for your JavaScript bundles looks like so you can discover whether there’s low-hanging fruit to optimize.

#### CSS Strategy

Tinder are using [Atomic CSS](https://acss.io/) to create highly reusable CSS styles. All of these atomic CSS styles are inlined in the initial paint and some of the rest of the CSS is loaded in the stylesheet (including animation or base/reset styles). Critical styles have a maximum size of 20KB gzipped, with recent builds coming in at a lean < 11KB

Tinder use CSS stats and Google Analytics for each release to keep track of what has changed. Before Atomic CSS was being used, average page load times were ~6.75s. After they were ~5.75s.

* [CRITICAL CSS](https://www.smashingmagazine.com/2015/08/understanding-critical-css/)

Using bundle analysis led to also also taking advantage of Webpack’s Lodash Module Replacement Plugin. The plugin creates smaller Lodash builds by replacing feature sets of modules with noop, identity or simpler alternatives:

#### Runtime performance

To improve runtime performance, Tinder opted to use requestIdleCallback() to defer non-critical actions into idle time.

* [Using requestIdleCallback](https://developers.google.com/web/updates/2015/08/using-requestidlecallback)

`requestIdleCallback(myNonEssentialWork);`

#### Dependency upgrades

In older versions of webpack, when bundling each module in your bundle would be wrapped in individual function closures. These wrapper functions made it slower for your JavaScript to execute in the browser. Webpack 3 introduced “scope hoisting” — the ability to concatenate the scope of all your modules into one closure and allow for your code to have a faster execution time in the browser. It accomplishes this with the Module Concatenation plugin:

*Webpack 3’s scope hoisting improved Tinder’s initial JavaScript parsing time for vendor chunk by 8%.*

#### React 16

* [reduced file size](https://reactjs.org/blog/2017/09/26/react-v16.0.html#reduced-file-size)

React 16 introduced improvements that decreased React’s bundle size compared to previous versions. This was in part due to better packaging (using Rollup) as well as removing now unused code.

By updating from React 15 to React 16, Tinder reduced the total gzipped size of their vendor chunk by ~7%.

The size of react + react-dom used to be~50KB gzipped and is now just ~35KB. Thanks to Dan Abramov, Dominic Gannaway and Nate Hunzaker who were instrumental in trimming down React 16’s bundle size.

#### Workbox for network resilience and offline asset caching

Tinder also use the [Workbox Webpack plugin](https://developers.google.com/web/tools/workbox/guides/codelabs/webpack) for caching both their Application Shell and their core static assets like their main, vendor, manifest bundles and CSS. This enables network resilience for repeat visits and ensures that the application starts-up more quickly when a user returns for subsequent visits.

#### Oppurtunities

Digging into the Tinder bundles using source-map-explorer (another bundle analysis tool), there are additional opportunities for reducing payload size. Before logging in, components like Facebook Photos, notifications, messaging and captchas are fetched. Moving these away from the critical path could save up to 20% off the main bundle:

