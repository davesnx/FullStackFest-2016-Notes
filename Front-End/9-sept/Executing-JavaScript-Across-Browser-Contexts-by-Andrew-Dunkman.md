# Executing JavaScript Across Browser Contexts by Andrew Dunkman

THIS IS NOT ABOUT GRAPHQL

### Standard Browser APIs

Given a bunch of daily dev user, with a lot of Tabs opened, every single Tab is connected to a service.
But you could have some problems like the state is changing meanwhile you are
in another Tab, to solve that or even more use cases, we could use:

- document.cookie
- localStorage, the key-pair db value for save information on the browser, tries to solve the problem of saving this state or even user information on the client.

--

There's more to the web than web pages.
- Browser Contexts
- Domain-Level Objects
- Bunch of new Browser APIs

--

### SharedWorker
are great for sharing proceses between browser contexts, different windows.
The concept could come to some Tab talking to another one and operatin as a P2P or
even a single client-server connection.

ServiceWorker is:

- For **W3C** is a generic entry point for event-driven background processing in the Web Platform.

- The **MDN** definition is: essentially act as proxy servers that sit between web applications, and the browser and network. ServiceWorker is an event-driven worker registered against an origin and a path.

but for him: is a process which is tied to domain evnets rather than to a browsing context.

--

You are able to put the Domain Events into a worker script, like push, sync and fetch.

DEMO: Push
Showing how a server can trigger a Push Notification to you browser using Notification Service

--

Each time that you run a script that have a workser registred, It creates this
connection with the worker, but if eventually you open a new Tab with the same
script it still conects to the first worker, without creating a new connection.

### "push" Event

The push event is capable to put values into the ServiceWorker, in able to subscribe into this event and keep receiving.

<!-- Define what's that with code here -->
<!-- Browser support -->

--

### "sync" Event

Is a event that listen for the events that the Tab could send to this worker
with a certain tags, to keep syncronized between them.

<!-- Define what's that with code here -->
<!-- Browser support -->

--

### "fetch" Event

The worker can pre-fetch the assets of your page.
It gives you programmatic access to Browser Caches, you can be able to get or set
stuff from this Cache, not like old days that the Cache just works magically.
Replaces AppCache
Also custom offline logic
Is completly encapsulated

<!-- Define what's that with code here -->
<!-- Browser support -->

--

[Slides](dunkman.me/talks/fsf)
