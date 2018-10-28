# JS-Blogs

* [React’s JSX vs Vue’s templates: a showdown on the front end](https://medium.freecodecamp.org/reacts-jsx-vs-vue-s-templates-a-showdown-on-the-front-end-b00a70470409#.ycvoyji7a)
* [What exactly is Node.js?](https://medium.freecodecamp.org/what-exactly-is-node-js-ae36e97449f5)
* [Angular 2 versus React: There Will Be Blood](https://medium.freecodecamp.org/angular-2-versus-react-there-will-be-blood-66595faafd51)
* [JavaScript essentials for React developers](https://codeburst.io/whats-new-in-es6-or-es2015-480edf104489)
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



