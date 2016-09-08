## Immutable User Interface
### Immutable App Architecture
##### Lee Byron

He's gonna explain how to make a "osom" Applications

-

What's a Architecture?

- Durability -
- Utility - How's gonna be used
- Beauty - Usable and desirable (Developer Experience)

All about is making "Fundamental Structural Choices"
  > Chosing Elements of Abstraction

-

MVC sucks blablal Model/View lose control of the flow.

-

Also need to consider all the variables in Mobile/Latency/Accesibility/etc.

-

Examples, blalba

-

Immutablility
- Isn't new
- Performance (?)

Everything is about Power vs Principles
aka. Pros and Cons

Power maintains inside the low level of languages, meanwhile the Principles [...]

Everything comes from Elm, pure functional programing.

-

Component is a abstraction about a view that we want to controll how to represent some element(HTMLElement, UIView, etc...) some point of time.

Component
(State) => View
f(State): View

Explaining how React works...

-

Colocated Data Dependencies
That's comes from where you store your data(?)

Explain what's GraphQL...

How the GraphQL queries match so well with WebComponents (actually, React).

-

The State of the Application comes from the Server
and goes to the Model, that represent on the Components,
that they made it rendering on the View, the user triggers
a action and this changes the state again.

State       <-         Actions

|         Server          ^
v                         |

Models -> Components -> Views


He points that sounds expensive, and It is (IMHO)
but thanks to the some perf optimizations that are there, like:

- Component Diff: diff(VDOM, DOM)
- Memorize Func: Cache the same ouput from the same input
  - https://github.com/reactjs/reselect
  - https://github.com/sindresorhus/mem
- Immutable Structures (Records, Maps, Lists, etc...)
  - https://facebook.github.io/immutable-js

-

Actions Asyncronous?

Action: (State) => State

But also they can be Async:
`Action: (State) => State, Promise<State>`
`Action: (actualState) => optimisticState, Promise<newState>`

They think the actions as a Queue
Explain what a Optimistic Request is...

So... at the end actions would request stuff to the server and will wait
in the **Action Queue**, will wait until the server respond the Request, meanwhile
the state would be a `optimisticState`

-

Everything is Immutable.
