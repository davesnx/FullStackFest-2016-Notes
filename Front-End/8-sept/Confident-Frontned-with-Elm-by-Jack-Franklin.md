# Confident Front-End with Elm by Jack Franklin
## Basic Introdution to Elm

### Let's begin what we know now and what we have now:

- MVC is death, blablalba.
- Doble **Data Binding** and "dirty checker" is awful.
- Observable.observe() was part of some browsers.
- The problem is **"Changes in data"**
- Mutability doesn't solve the browser issues.
- Single source of Thurth.

--

### Elm
- Functional, Typed and Compiled
- Syntax sucks
- Expressive, clear code
- Piping
- Everything is Immutable
- Pure func
- Types!
- No undefiend and null pain.
    - Really agains the undefiend is not a function,
    or even null
- Maybe: is a sanity check for having or not having the data that you expect.

  ```

    Type a
      Just 3
      | Nothing

  ```

-

**Messages:**
  The way of express the actions in Elm.

  **Msg**: "MsgName" aka (Actions in Redux)

  ```
{
  type: ACTION.name,
  payload: { ... }
}
  ```

-

**Command:**
  Is where you trigger the Side Effects or some Actions that could do
  whatever asyncronous.

-

**Updates:**
  Define how the state can change (usually are called "Updates").
  `f(State) => State'` (Same as Reducers in Redux).

-

### Q&A:
  - Not mature enought
  - Elm not Server Side Rendering
  - When use Elm instead of JS?
    - Lot data changes all the time
    - Side projects could be the best start

-

[@Jack_Franklin](https://twitter.com/Jack_Franklin)
**GitHub code**: [jackfranklin/elm-for-js-developers-talk](https://github.com/jackfranklin/elm-for-js-developers-talk)
**Slides**: [fullstackfest-elm-for-js-developers](https://speakerdeck.com/jackfranklin/fullstackfest-elm-for-js-developers)
