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


