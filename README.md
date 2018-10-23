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
