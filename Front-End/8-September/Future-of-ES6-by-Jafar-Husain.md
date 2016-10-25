# Future of ES6 by Jafar Husain

### ES stages
- 0: **Starwman**
- 1: **Proposal**
- 2: **Draft**
- 3: **Candidate**
- 4: **Finished**

--

### Example how async functions comes to stage-4

  Syntax:
  ```js
    async function operationAsync () {
      let lola = await anotherAsyncOperation()
      let result = await getLolaResultAsync(lola)
      return result
    }
  ```

  Can become also with try/catch:

  ```js
    async function operationAsync () {
      let lola = await anotherAsyncOperation()
      let result
      try {
        result = await getLolaResultAsync(lola)
      } catch (e) {
        throw e
      }
      return result
    }
  ```

-

### Example how cancelation tokens arrives to stage-2

Is some kind of token for promises to be sure that can be cancellable.

You pass a token and this is triggered if the callback that you provide on the `.then()` is cancelled.

also works with async-functions comented below.

--

### Explain what a Generator function is...

--

The idea behind the TC-39 is to solve the async/sync syntax difference and behaviour, adding async or generators.

Then they can join Node Streams and (?) to be Iterators.

--

The web has no standard **Observable** interface.
But in the `stage-1` there are a proposal called "**Push API's**".

> The same API than xstream by Andre
and works exactly the same as RxJS Observables Pattern.
But seems like under the wood, they implement it with iterables.

```
interface Observer<T>: {
  next(T): void,
  error(Error): void,
  complete(T): void
}

interface Observable<T>: {
  void subscribe(Observer<T>, [CancelToken])
}
```

- Composition of Observables: they try to add the interface that comes from lodash/underscore, but still the same as RxJS.

--

### Questions:
  - Doesn't talk about hot/cold in Observable?
  - Doesn't talk abut Symbols?
  - Nothing about
    - https://github.com/tc39/proposals/blob/master/README.md

[@jhusain](https://twitter.com/jhusain)
