# Clients in control by
### Building demand-driven system with Om Next

# Problems about REST

- only one request/create trivial data
- "joined" resources
- bload enpoint?
- multiple requests?

The problem could be not the huge amount of devices that we have, just the way of we develop them.

There a few technologies that tries to solve this problems:
  - Meteor
  - Firebase
  - Parse

But for his opinion doesn't solve the problem. They lose the oportunity of relational queries.

-

"Demand-driven" Architecture
  Is a concept that you get what the client demand, and they will request
  what the client needs.

  1. Demand with some Requirements
  2. Composition data structures (you could be storage-agnostic)
  3. Interpretation

  GraphQL is a query language based on a contract on demand.

-

**DEMO TIME**: Shows that you are agnostic about the implementation of the backend
and how flexible is.

Few optons to solve this problems:
  - React comes here to solve also the problem, plus Relay with the GraphQL to
  join the Facebook Stack.
  - In the other hand we have Falcor from NetFlix. Explain the NetFlix history.
  - ClojureScript that are Immutable by default.

All them become David Nolan to create **om.next**.
1. clients can request the **exatc total** response they need
2. clients can comunacte novelty atomically


##### Om Next opinions
> (Redux some values too)

- Single source of trouth
- Minimize flushing to DOM
- No (visible)
  - asynchrony
  - event model

-

##### Parser
- reads & mutations
- runs front and backend
- Hydrate queries
  - no reshaping!
- Edge of the system

-

[...]

-

The differente between Om.next and React is that Om.next doesn't try to do
all the diff of the full Tree, just the proper component based on the pure functions.

```
      O
    /   \
  [O]    O
  /\
 O  O
```

Re-render this component (`[O]`), make the diff of the full tree,
meanwhile in Om.next does only trigger the re-render of this Component `[O]`.

-

More Om Next

- Amazing Unit Testing
- Recursive UIs
- Heterogeneous UIs
- HTTP Caching
- Custom storage
- Streaming
- Server-Side Rendering

-

#### Conclusions:

- We can radically simplify UI programming


-

Sources: [om](https://github.com/omcljs/om/wiki)
Tutorial: [om-tutorial](http://awkay.github.io/om-tutorial)
Personal site: [anmonteiro.com](https://anmonteiro.com)
Slides: [anmonteiro/talks](https://github.com/anmonteiro/talks)
