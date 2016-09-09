# CSP in JavaScript by Vincenzo Chianese

### CSP: Communicating Sequential Processes
> All the concepts are abailable on Front or Back

##### Problem: Sharing the memory
  - Non determinism
  - Rece conditions
  - Deadlocks

  So...
    Hard to **reproduce** > Hard to **debug** > Hard to **test*

--

##### Possible solution
  - Mutexes
  - Semaphores
  - Atomic operations

  So...
  - **Complexity** and **overhead**
  - **Leaky**

--

JavaScript is not Parallel, as much of us know is one threaded,
only one line of code is running at the same time.

--

##### Example: High Level Tasks
Showing a logic operation that is async like aP AJAX request, and a render
function that represent the result in the screen, need to run syncronously after
the first AJAX Request finishes.

--

##### Possible solution of running code on Asyncronous way are:
  - Callbacks is the "default" solution
  - Promises creates a piping of operation that solves the Callback Hell Problem,
  and encapsulate this piping in a easy-to-understand way.
  - Generators, breaks the difference between the Sync and Async way of writing code,
  just adding a few keywords your code becomes asyncronous.
  It trate the functions as iterators each time that you `yield` a value, like a
  normal return.
  - Async-await

--

##### High order pattern
We could need a stream of data for handling all the events, the we see on Observables (RxJS) and CSP.

--

##### CSP

For understand CSP you can think like pipes:
- Like bash pipe: `cat file | grep search`
- You can **compose** them
- Are running on **parallel**
- doesn't **leak**

CSP it's an algebra defined by maths.

--

##### Channels
A similar concept than Observables:
Message passing between processes happens via channels. Channels can have many writers and readers, which can do put and get operations on them putting or getting a single value at a time.

--

Code time

--

##### CSP Recap
- Solid **theory** concepts
- **Simple API** than RxJS
- Build in **backpressure**
- Highest order pattern

##### CSP Caveats
- Idea from future
- Different, **opinionated** implementations (You can use aync-await, generators, etc)
- Doesn't integrate yet with more famous libs like React
