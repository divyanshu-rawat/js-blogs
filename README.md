### JS-Blogs

* [React’s JSX vs Vue’s templates: a showdown on the front end](https://medium.freecodecamp.org/reacts-jsx-vs-vue-s-templates-a-showdown-on-the-front-end-b00a70470409#.ycvoyji7a)
* [What exactly is Node.js?](https://medium.freecodecamp.org/what-exactly-is-node-js-ae36e97449f5)
* [Angular 2 versus React: There Will Be Blood](https://medium.freecodecamp.org/angular-2-versus-react-there-will-be-blood-66595faafd51)
* [JavaScript essentials for React developers](https://codeburst.io/whats-new-in-es6-or-es2015-480edf104489)
* [3 JavaScript Performance Mistakes You Should Stop Doing](https://hackernoon.com/3-javascript-performance-mistakes-you-should-stop-doing-ebf84b9de951)
  * Looping Over an Array
     * For Loop, average loop time: ~10 microseconds
     * For-Of, average loop time: ~110 microseconds
     * ForEach, average loop time: ~77 microseconds
     * While, average loop time: ~11 microseconds
     * Reduce, average loop time: ~113 microseconds
     
```  reduce and forEach requires a call back function to be executed which is called recursively and bloats the stack, and additional operation and verification which are made over the executed code. ```

* Mistake 2
   * Duplicating an Array
       * Duplicate using ``` Slice, ``` average: ~367 microseconds
       * Duplicate using ``` Map, ``` average: ~469 microseconds
       * Duplicate using ``` Spread, ``` average: ~512 microseconds
       * Duplicate using ``` Conct, ``` average: ~366 microseconds
       * Duplicate using ``` Array From, ``` average: ~1,436 microseconds
       * Duplicate manually, ``` average, ``` ~412 microseconds
       
* Mistake 3
   * Iterating Objects
       * Object iterate For-In, average: ~240 microseconds
       * Object iterate Keys For Each, average: ~294 microseconds
       * Object iterate Entries For-Of, average: ~535 microseconds

### Testing

* [Using Jest to run tests on a simple Node script dealing with fs module](https://medium.com/@shashankshekhar_40767/using-jest-mocking-to-run-tests-on-a-simple-node-script-dealing-with-fs-module-db8bc01ff583)

### Redux-Blogs

* [Introducing Redux Offline: Offline-First Architecture for Progressive Web Applications and React Native](https://hackernoon.com/introducing-redux-offline-offline-first-architecture-for-progressive-web-applications-and-react-68c5167ecfe0)
  * https://pouchdb.com/
  * https://www.datomic.com/
  * [redux-offline](https://github.com/redux-offline/redux-offline)

* [Redux: Persist Your State](https://medium.com/async-la/redux-persist-your-state-7ad346c4dd07)
  * [redux-persist](https://github.com/rt2zz/redux-persist)

* [How to use Redux Persist when migrating your states](https://medium.freecodecamp.org/how-to-use-redux-persist-when-migrating-your-states-a5dee16b5ead)

* [{Persist}ence is Key: Using Redux-Persist to Store Your State in LocalStorage](https://medium.com/@clrksanford/persist-ence-is-key-using-redux-persist-to-store-your-state-in-localstorage-ac6a000aee63)

Now even if your user clicks away from a page or refreshes, the relevant information which you had saved in state will still be there. Thank you, redux-persist, for this handy service!

### Promises v/s Observables
* [Promises vs Observables](https://medium.com/@mpodlasin/promises-vs-observables-4c123c51fe13)

Promises are eager, Observables are lazy, Single value v/s multiple values, Not cancellable v/s cancellable, Multicast v/s either unicast or multicast, Always asynchronous v/s possibly asynchronous.

``` Function passed to Observable constructor gets called only when someone actually subscribes to an Observable: ``` 


### PWA (Progressive Web Apps)
* [What is a PWA and why should you care?](https://blog.bitsrc.io/what-is-a-pwa-and-why-should-you-care-388afb6c0bad)
   * [FidgetSpin PWA](https://www.fidgetspin.xyz/)
   * [PWA Examples](https://pwa.rocks/)
   * [Lighthouse](https://developers.google.com/web/tools/lighthouse/)
   * [Google Showcase PWA](https://developers.google.com/web/showcase/)
   * [Workbox](https://developers.google.com/web/tools/workbox/)
   
If a company is dedicated and wants to get maximum engaged customers, the experience of a web app has to be close to that of the native app.

```Let’s take the example of Whatsapp on your phone. When there is no network, you can still open the app, check past messages and even reply to someone. When the phone gets the internet connection, the messages are being automatically sent in the background```

A PWA provides features like push notification, home screen icon, full-screen and offline first app to glorify user engagement.

The PWA stores HTML files, CSS files and images in the browser cache and the developers can fully control the network call. All of these are being achieved by Service Workers.


### React 16
* [2 Minutes to Learn React 16's componentDidCatch Lifecycle Method](https://medium.com/@sgroff04/2-minutes-to-learn-react-16s-componentdidcatch-lifecycle-method-d1a69a1f753)

``` “Error boundaries are React components that catch JavaScript errors anywhere in their child component tree, log those errors, and display a fallback UI instead of the component tree that crashed. Error boundaries catch errors during rendering, in lifecycle methods, and in constructors of the whole tree below them.” -Dan Abramov ```

``` In practice, most of the time you’ll want to declare an error boundary component once and use it throughout your application. -Dan Abramov ```

* [Portals](https://reactjs.org/docs/portals.html)

Portals provide a first-class way to render children into a DOM node that exists outside the DOM hierarchy of the parent component.

* [Stateless Component vs Pure Component](https://medium.com/groww-engineering/stateless-component-vs-pure-component-d2af88a1200b)

Pure Components gives a considerable increase in performance because it reduces the number of render operation in the application which is a huge win for complex UI and therefore advised to use if possible.

* [Learn the basics of destructuring props in React](https://medium.freecodecamp.org/the-basics-of-destructuring-props-in-react-a196696f5477)

[SANDBOX](https://codesandbox.io/s/ovp7x99zvz)


### Dart
* [Why Dart is the Language to Learn of 2018](https://medium.com/@mswehli/why-dart-is-the-language-to-learn-of-2018-e5fa12adb6c1)


### Redis
* [Introduction to Redis + Node.js](https://codeburst.io/introduction-to-redis-node-js-demo-f3326dd43c0f)

* [Using Redis with Node JS](https://hackernoon.com/using-redis-with-node-js-8d87a48c5dd7)

Redis is an in-memory data structure store which can be used as a ``` database, a cache and a message broker ```. Simply Redis uses you RAM to store data which is very fast, however if you reboot your server the values are gone, unless you enable Redis persistence.

* [Building an API Cache with Redis and Node](https://medium.com/ibm-watson-data-lab/building-an-api-cache-with-redis-and-node-3fbad5675d5d)

Redis DataTypes : ``` Strings, Lists, Sets (sorted or otherwise), Hashes, Bitmaps, HyperLogLogs. ```


### Code Splitting
* [React-Docs](https://reactjs.org/docs/code-splitting.html)

Most React apps will have their files “bundled” using tools like ``` Webpack ``` or ``` Browserify. ```
Browserify is an open-source JavaScript tool that allows developers to write Node.js-style modules that compile for use in the browser. 

Bundling is the process of following imported files and merging them into a single file: a “bundle”. This bundle can then be included on a webpage to load an entire app at once.

``` If you’re using Create React App, Next.js, Gatsby, or a similar tool, you will have a Webpack setup out of the box to bundle your app. ```

Bundling is great, but as your app grows, your bundle will grow too. Especially if you are including large third-party libraries.

To avoid winding up with a large bundle, it’s good to get ahead of the problem and start “splitting” your bundle.

Code-splitting your app can help you “lazy-load” just the things that are currently needed by the user,``` which can dramatically improve the performance of your app.``` While you haven’t reduced the overall amount of code in your app, you’ve avoided loading code that the user may never need, and reduced the amount of code needed during the initial load.

The best way to introduce code-splitting into your app is through the dynamic import() syntax.

``` The best way to introduce code-splitting into your app is through the dynamic import() syntax. ```

``` js 

import("./math").then(math => {
  console.log(math.add(16, 26));
}); 

```

Create React App, this is already configured for you and you can start using it immediately. 

``` React Loadable ``` wraps dynamic imports in a nice, React-friendly API for introducing code splitting into your app at a given component.

* [Introducing React Loadable](https://jamie.build/react-loadable.html)

A common piece of advice you will see is to break your app into separate routes and load each one asynchronously. This seems to work well enough for most apps, clicking on a link and loading a new page is not a terrible experience.

So what if we optimized around components instead of delegating that responsibility to routes?

``` It turns out quite a lot. There are many more places than just routes where you can pretty easily split apart your app. Modals, tabs, and many more UI components hide content until the user has done something to reveal it. ```

Not to mention all the places where you can defer loading content until higher priority content is finished loading. 

### Next.js

* [Why I chose React + Next.js for my next website instead of Vue or Angular](https://medium.freecodecamp.org/use-react-with-next-js-framework-and-how-it-made-my-life-easier-4280b643451)

Next.js features:

* Server-rendered by default (Yay!).
* Automatic code splitting for faster page loads.
* Simple client-side routing (page based).
* Webpack-based dev environmet which supports Hot Module Replacement (HMR).
* Able to implement with Express or any other Node.js HTTP server.
* Customizable with your own Babel and Webpack configurations.

* [Now – Global Serverless Deployments](https://zeit.co/now#whats-now)

now allows you to take your JavaScript (Node.js) or Docker powered websites, applications and services to the cloud with ease, speed and reliability. In practical terms, any directory that contains a package.json or Dockerfile can be transported to the cloud with one command: now

* [Getting Started](https://nextjs.org/learn/basics/getting-started/setup)


### AWS
* [AWS Lambda + Serverless Framework + Python](https://hackernoon.com/aws-lambda-serverless-framework-python-part-1-a-step-by-step-hello-world-4182202aba4a)

The ``` Serverless ``` Framework helps you develop and deploy your ``` AWS Lambda functions ```, along with the AWS ``` infrastructure resources they require ```, allowing you to focus on building sophisticated, ``` event-driven, serverless architectures, comprised of Functions and Events.```

A Function is an AWS Lambda function. It's an independent ``` unit of deployment, like a microservice. ``` It's merely code, deployed in the cloud, that is most often written to perform a single job such as:

* Saving a user to the database.
* Processing a file in a database.
* Performing a scheduled task.

Anything that triggers an AWS Lambda Function to execute is regarded by the Framework as an ``` Event ```. Events are infrastructure events on AWS such as:

* An AWS API Gateway HTTP endpoint request (e.g., for a REST API)
* An AWS S3 bucket upload (e.g., for an image)
* A CloudWatch timer (e.g., run every 5 minutes)

Resources are AWS ``` infrastructure components ``` which your Functions use such as.

* An AWS ``` DynamoDB Table (e.g., for saving Users/Posts/Comments data) ```
* An AWS ``` S3 Bucket (e.g., for saving images or files)```
* An AWS ``` SNS Topic (e.g., for sending messages asynchronously)```

A Service is the Framework's unit of organization. It's where you define your Functions, the Events that trigger them, and the Resources your Functions use, all in one file entitled ``` serverless.yml (or serverless.json or serverless.js).```

```yml
 
service: users

functions: # Your "Functions"
  usersCreate:
    events: # The "Events" that trigger this function
      - http: post users/create
  usersDelete:
    events:
      - http: delete users/delete

resources: # The "Resources" your "Functions" use.  Raw AWS CloudFormation goes in here.

```

More resource to explore:

* [AWS - Functions](https://serverless.com/framework/docs/providers/aws/guide/functions/) 
* [Create a Simple Lambda Function](https://docs.aws.amazon.com/lambda/latest/dg/get-started-create-function.html)
* [What is the difference between a Serverless Function, and a Lambda Function?](https://stackoverflow.com/questions/49953270/what-is-the-difference-between-a-serverless-function-and-a-lambda-function)

You can use AWS Lambda to run your code in response to events, such as changes to data in an Amazon S3 bucket or an Amazon DynamoDB table; to run your code in response to HTTP requests using Amazon API Gateway; or invoke your code using API calls made using AWS SDKs. With these capabilities, you can use Lambda to easily build data processing triggers for AWS services like Amazon S3 and Amazon DynamoDB, process streaming data stored in Kinesis, or create your own back end that operates at AWS scale, performance, and security.

``` You can also build serverless applications composed of functions that are triggered by events and automatically deploy them using AWS CodePipeline and AWS CodeBuild.  ```

When using AWS Lambda, you are responsible only for your code. AWS Lambda manages the compute fleet that offers a balance of ``` memory, CPU, network, and other resources. ``` This is in exchange for flexibility, which means you cannot log in to compute instances, or customize the operating system or language runtime. These constraints enable AWS Lambda to perform ``` operational and administrative activities on your behalf, including provisioning capacity, monitoring fleet health, applying security patches, deploying your code, and monitoring and logging your Lambda functions.```

* [Serverless Dynamic Real-Time Dashboard with AWS DynamoDB, S3 and Cognito](https://medium.com/@rfreeman/serverless-dynamic-real-time-dashboard-with-aws-dynamodb-a1a7f8d3bc01)

The downside is that you need to maintain your own infrastructure, servers and code base. In addition, if the volumes of data ingested per second is very high then different scalable patterns need to be implemented.
 
Some of these issues can be addressed using Amazon Web Services (AWS) managed services like Amazon ElastiCache for in memory cache (Memcached or Redis are supported), Amazon DynamoDB as an NoSQL database that can reduce the maintenance and support requirements.

AWS managed NoSQL DynamoDB, scalable static website in Amazon Simple Storage Service (S3) and security using Amazon Cognito and AWS Identity and Access Management (IAM) Roles removing the need to run any app server, web server or use a 3rd party service.

* [Reduce latency and increase security using Amazon CloudFront.](https://aws.amazon.com/cloudfront/)

Amazon CloudFront is a fast content delivery network (CDN) service that securely delivers data, videos, applications, and APIs to customers globally with low latency, high transfer speeds, all within a developer-friendly environment. 

* DynamoDB allows us to have a persistent store for the data.
* Cognito and IAM role deals with the authentication and authorisation.
* S3 deals with the hosting the HMTL, JavaScript and node.js code, making it low cost, scalable and secure.


[Monolith Vs Microservice Vs Serverless — The Real Winner?](https://hackernoon.com/monolith-vs-microservice-vs-serverless-the-real-winner-the-developer-8aae6042fb48)

### Serverless — The Advantages:

Imagine the scenario where you have a new requirement handed down to you from upper management.

* Shoe horn your new requirement into one of your existing systems
* Architect a new system that handles this requirement
* leverage the likes of AWS Lambda.

You need not to take care of infrastructure, security, maintenance, scalability etc.
``` AWS lambda does a hell of a lot of heavy lifting for you, including things like resiliency, horizontal scaling and so on. ```

The advantages of a ``` microservice based approach ``` in this scenario is that you can effectively design, develop a microservice that satisfies ‘X’ and can be called from within your monolith through your favourite communication protocol.

This allows you:

* To independently scale ‘X’ to cope with variable demands on the system.
* To reduce the risk of ‘X’ bringing down your system in Production at 3 in the morning.


### uber-eng

[Powering UberEATS with React Native and Uber Engineering](https://eng.uber.com/ubereats-react-native/)

As noted earlier, React Native fuses web and mobile development, allowing us to write features either natively or in JavaScript.
We ultimately architected UberEATS in much the same way as we would a regular React /Redux web app, eschewing iOS patterns and modules wherever possible. Fortunately for our needs and preferences, web concepts and technologies on the whole translate quite nicely to native development.

One example of this easy translation to the web is the app’s routing functionality. On the web, Restaurant Dashboard uses the popular react-router library which enables routes to be defined declaratively, much in the same way as a View. However this system assumes the existence of URLs which tend to be lacking outside of the browser. React Native provides an imperative navigation library, which resembles the interface provided by UINavigationController.

Another key lesson from the porting process was that it is highly advantageous to minimize interaction between iOS and JavaScript and concentrate logic in the JavaScript layer. Doing so has a number of significant benefits, such as:

* Less context switching between JavaScript and Objective-C
* Increased portability (through diminished platform-specific code)
* Reduced scope for bugs

Using Flow to type check allows us to verify that our state maintains its correct shape after this process, and it is a credit to the Flow community that new releases have continued to find possible sources of bugs in our application.

It is often necessary to alter the store in response to asynchronous actions, such as network requests. Redux does not prescribe a way of doing this, but a common approach is to use `Thunks` , a middleware for Redux that allows actions to be functions that return a promise and dispatch additional actions along the way

Our initial approach was to use Thunks, but we quickly ran into problems as our application logic (and side effects) became more complicated. Specifically, we encountered two side effect patterns that did not naturally fit into the Thunk model:

* Periodic updates to application state
* Coordination between side effects

`Sagas` , an alternative side effect model for Redux apps, leverage ES6 (ECMAScript 6) generator functions to provide a less complicated option. Rather than extending the concept of an action, they are modeled as a separate thread which can access the store, listen to Redux actions, and dispatch new ones. In an effort to avoid Thunk-related problems, UberEATS.com recently migrated entirely to Sagas, giving us confidence that they could scale and were mature enough for our needs.

For example, the component could periodically dispatch an action to fetch orders; alternatively, the Thunk could call itself recursively. Aside from the implementation issues, however, neither having a component with timer logic—nor an independent Thunk that keeps triggering itself—fits neatly into the Redux model.

Sagas provide a clean way of solving this problem, as they enable us to create a long-living task that periodically fetches new orders and dispatches an action to update the store.

``` 
This approach of having many small services communicating with each other through message passing will be familiar to many backend engineers, but we generate and consume Redux actions instead of Kafka events. From our view on the developer side, it has been fascinating to watch these patterns applied to client code.

```

## Netflix-eng
[Netflix Web Performance case study](https://medium.com/dev-channel/a-netflix-web-performance-case-study-c0bcde26a9d9?fbclid=IwAR3lhY1dAoJ5Xg3w_oDOKEMStiNfLs4Jz9Daxv9kdnNO455BJTP-pIDMzLc)

``` 
There are no silver bullets to web performance. Simple static pages benefit from being server-rendered with minimal JavaScript. Libraries can provide great value for complex pages when used with care.
```

* Loading and Time-to-Interactive decreased by 50% (for the logged-out desktop homepage at Netflix.com)
* JavaScript bundle size reduced by 200kB by switching from React and other client-side libraries to vanilla JavaScript. React   was still used server-side.
* Prefetching HTML, CSS and JavaScript (React) reduced Time-to-Interactive by 30% for future navigations.


Even though React’s initial footprint was just 45kB, removing React, several libraries and the corresponding app code from the client-side reduced the total amount of JavaScript by over 200kB, causing an over-50% reduction in Netflix’s Time-to-Interactivity for the logged-out homepage.

**Prefetching React for subsequent pages** To further improve performance when navigating their logged-out homepage, Netflix utilized the time spent by users on the landing page to prefetch resources for the next page users were likely to land on.

This was achieved by using two techniques — the built-in <link rel=prefetch> browser API and XHR prefetching.

*By using both the built-in browser API and XHR to prefetch HTML, CSS, and JS, the Time-to-Interactive was reduced by 30%.*

**By prefetching resources and optimizing the client-side code on Netflix’s logged-out homepage. **

Netflix was able to greatly improve their Time-to-Interactive metrics during the sign-up process. By prefetching future pages using the built-in browser API and XHR prefetching, Netflix was able to reduce Time-to-Interactive by 30%. This was for the second-page loading, which contained the bootstrapping code for single-page app sign-up flow.

*The tradeoff Netflix decided to make is to server-render the landing page using React, but also pre-fetching React / the code for the rest of the signup flow while on it.This optimizes first load performance, but also optimizes the time to load for the rest of the signup flow, which has a much larger JS bundle size to download since it’s a single-page app.*



## COST OF JS

[The Cost Of JavaScript In 2018](https://medium.com/@addyosmani/the-cost-of-javascript-in-2018-7d8950fbb5d4)

Building interactive sites can involve sending JavaScript to your users. Often, too much of it. Have you been on a mobile page that looked like it had loaded only to tap on a link or tried to scroll and nothing happens?

Today we’ll cover some strategies you can use to deliver JavaScript efficiently while still giving users a valuable experience.

* To stay fast, only load JavaScript needed for the current page.
  * Prioritize what a user will need and lazy-load the rest with [code-splitting](https://webpack.js.org/guides/code-splitting/). This gives you the best chance at loading and getting interactive fast. Stacks with route-based code-splitting by default are game-changers.

* Embrace performance budgets and learn to live within them.
  * mobile, aim for a JS budget of < 170KB minified/compressed. Uncompressed this is still ~0.7MB of code. Budgets are critical to success, however, they can’t magically fix perf in isolation. Team culture, structure and enforcement matter. Building without a budget invites performance regressions and failure.
  
* Learn how to audit and trim your JavaScript bundles. 
  * There’s a high chance you’re shipping full-libraries when you only need a fraction, [polyfills for browsers that don’t need them, or duplicate code](https://webpack.js.org/guides/code-splitting/)
  
* Every interaction is the start of a new ‘Time-to-Interactive’
  * consider optimizations in this context. Transmission size is critical for low-end mobile networks and JavaScript parse time for CPU-bound devices.
  
* If client-side JavaScript isn’t benefiting the user-experience, ask yourself if it’s really necessary.
  * Maybe server-side-rendered HTML would actually be faster. Consider limiting the use of client-side frameworks to pages that absolutely require them. Server-rendering and client-rendering are a disaster if done poorly.
  
We’re hitting this ceiling across both desktop and mobile web, where sites are sometimes shipping multiple megabytes-worth of code that a browser then needs to process. The question to ask is, [can you afford this much JavaScript](https://infrequently.org/2017/10/can-you-afford-it-real-world-web-performance-budgets/)?
 
 **Note: If you’re sending too much script, consider code-splitting to break up bundles or reducing [JS payloads using tree-shaking.](https://developers.google.com/web/fundamentals/performance/optimizing-javascript/tree-shaking/)**
 
 
* A client-side framework or UI library
* A state management solution (e.g. Redux)
* Polyfills (often for modern browsers that don’t need them)
* Full libraries vs. only what they use (e.g. all of lodash, Moment + locales)
* A suite of UI components (buttons, headers, sidebars etc.)

Loading too much JavaScript into the main thread (via <script>, etc) is the issue. Pulling JS into a [Web Worker](https://developer.mozilla.org/en-US/docs/Web/API/Web_Workers_API/Using_web_workers) or caching via a [Service Worker](https://developers.google.com/web/fundamentals/primers/service-workers/) doesn’t have the same negative Time-to-Interactive impact.
 
Avoid blocking the main thread as much as possible. For more, see [Why web developers need to care about interactivity](https://philipwalton.com/articles/why-web-developers-need-to-care-about-interactivity/)

* [Pinterest](https://medium.com/dev-channel/a-pinterest-progressive-web-app-performance-case-study-3bd6ed2e6154) reduced their JavaScript bundles from 2.5MB to < 200KB and Time-to-Interactive reduced from 23s to 5.6s. Revenue went up 44%, sign-ups are up 753%, weekly active users on mobile web are up 103%.

* [AutoTrader](https://engineering.autotrader.co.uk/2017/07/24/how-we-halved-page-load-times.html) reduced their JavaScript bundle sizes by 56% and reduced Time-to-Interactive for their pages by ~50%.
* [Nikkei](https://www.youtube.com/watch?v=Mv-l3-tJgGk&feature=youtu.be&t=1967) reduced their JavaScript bundle size by 43% and Time-to-Interactive improved by 14s.

The orange represents all the time spent parsing JavaScript that popular sites are sending down. In yellow, is the time spent compiling. Together, these take anywhere up to 30% of the time it takes to process the JavaScript for your page — this is a real cost.

A JPEG image needs to be decoded, rasterized, and painted on the screen. A JavaScript bundle needs to be downloaded and then parsed, compiled, executed —and there are a number of other steps that an engine needs to complete. Just be aware that these costs are not quite equivalent.


“Variability is what kills the User Experience” — Ilya Grigorik. Fast devices can actually sometimes be slow. Fast networks can be slow, variability can end up making absolutely everything slow.

If you want JavaScript to be fast, pay attention to download times for low end networks. The improvements you can make there are: ship less code, minify your source, take advantage of compression (i.e., gzip, [Brotli](https://github.com/google/brotli), and Zopfli).

Take advantage of caching for repeat visits. Parse time is critical for phones with slow CPUs.

Code-splitting is this idea that, instead of shipping down your users a massive monolithic JavaScript bundle — sort of like a massive full pizza — what if you were to just send them one slice at a time? Just enough script needed to make the current page usable.

Code-splitting can be done at the page level, route level, or component level. It’s something that’s well supported by many modern libraries and frameworks through bundlers like webpack and Parcel. Guides to accomplish this are available for React, Vue.js and Angular.

both [Twitter](https://blog.twitter.com/engineering/en_us/topics/open-source/2017/how-we-built-twitter-lite.html) and [Tinder](https://medium.com/@addyosmani/a-tinder-progressive-web-app-performance-case-study-78919d98ece0) saw anywhere up to a 50% improvement in their Time to Interactive when they adopted aggressive code splitting.

Stacks like Gatsby.js (React), Preact CLI, and PWA Starter Kit attempt to enforce good defaults for loading & getting interactive quickly on average mobile hardware.

Tools like Webpack Bundle Analyzer, Source Map Explorer and Bundle Buddy allow you to audit your bundles for opportunities to trim them down.

These tools visualize the content of your JavaScript bundles: they highlight large libraries, duplicate code, and dependencies you may not need.

*Bundle auditing often highlights opportunities to swap heavy dependencies (like Moment.js and its locales) for lighter alternatives (such as date-fns).*

We’ve recently added support for flagging high “JavaScript boot-up time” to Lighthouse. This audit highlights scripts which might be spending a long time parsing/compiling, which delays interactivity. You can look at this audit as opportunities to either split up those scripts, or just be doing less work there.

``` 
Code coverage is a feature in DevTools that allows you to discover unused JavaScript (and CSS) in your pages. Load up a page in DevTools and the coverage tab will display how much code was executed vs. how much was loaded. You can improve the performance of your pages by only shipping the code a user needs.

```
This can be valuable for identifying opportunities to split up scripts and defer the loading of non-critical ones until they’re needed.

If you’re looking for a pattern for serving JavaScript efficiently to your users, check out the [PRPL pattern](https://developers.google.com/web/fundamentals/performance/prpl-pattern/)

PRPL (Push, Render, Precache and Lazy-Load) is a pattern for aggressively splitting code for every single route, then taking advantage of a service worker to pre-cache the JavaScript and logic needed for future routes, and lazy load it as needed.

* The first is Long Tasks — an API enabling you to gather real-world telemetry on tasks (and their attributed scripts) that last longer than 50 milliseconds that could block the main thread. You can record these tasks and log them back to your analytics.

* First Input Delay (FID) is a metric that measures the time from when a user first interacts with your site (i.e. when they tap a button) to the time when the browser is actually able to respond to that interaction. FID is still an early metric, but we have a polyfill available for it today that you can check out.

*It’s well known that third-party JavaScript can have a dire impact on page load performance. While this remains true, it’s important to acknowledge that many of today’s experiences ship a lot of first-party JavaScript of their own, too. If we’re to load fast, we need to chip away at the impact both sides of this problem can have on the user experience.*

[LOADING THIRD PARTY JS](https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/loading-third-party-javascript/)

**Performance is a journey. Many small changes can lead to big gains.**
