# See the data flowing through your app by André Staltz

### Demo:

He made a 2 inputs view and some text binding the value of this inputs.
with xstream and CycleJS showing the potencial of DevTools Cycle.
That gets the streams that are running on the browser and represent the Stream
Graph.

--

### Problem that appers for create CycleJS
- Architecture for any kind of UI
- Clean, readable and predictable
- How code works

--

Debugger: Shows information about the micro-level of your app.
You'r losing the big picture.

--

### There're some tools to watch out at macro-level your code:
- **Minimaps**... X
- **Algorithm Visualizer**: Shows the algorithm, functions to jump your code is running X
- **UML Diagrams**: Only showing the Class Structure X
- **Component Information Model**: How models talks each other X
- **React Monocle:** Showing the Component Three of your App √
- **Redux DevTools** √
  - Small explainaiton how redux can manage Async and what are some different of solutions,
    that you can control on your mental model. (saga, redux-observable, etc...)

--

##### What is trying to solve?
  Visualize the macro-level logic in slow motion inside a Reactive App.

--

##### Basic explainaiton about Streams:
  Everything is a event.

-: the road
Julia: Observe the road and advise when she see a BLUE car
Raphael: Observe the road and advise when she see a RED car
Mónica: Observe Julie and Raphael
Dominic: Observe Mónica and do some operation

```
Road: ------------------
          |       |
        Julia    Raphael
          |       |
            \    /
             Mónica
               |
             Dominic
```

Every time that Julia see a blue car, gonna show a blue flag
Every time that Rapahel see a blue car, gonna show a red flag
Mónica is going to do some operation of how many flags of each color,
and Dominic will get this number and do some operation.

```
Road: ------------------
          |       |
        Julia    Raphael
          |       |
            \    /
             Mónica
               |
             Dominic
```

This is why Reactive Programing is better than invert the three and have
all the persons of this diagram advise the different Layers,
this is how CycleJS comes alive.

--

[...]

```javascript
import xs from 'xstrem'
import Cycle from '@cycle/xtream-run'
import { makeDOMDriver } '@cycle/dom'

const PASSED_BY = 'click'

function stage (events) {
  const julia = events.DOM
    .select('.blue-car')
    .events(PASSED_BY)
    .mapTo(+1)

  const raphael = events.DOM
    .select('.red-car')
    .events(PASSED_BY)
    .mapTo(-1)

    const monica = xs.merge(julia, raphael)
      .fold((memory, num) => memory + num, 0)
      // like reduce or scan

    const domenic = monica.map(num => {
        button('.decrement', 'Decrement')
        button('.increment', 'Increment')
        h2('Count: ', count)
      })
}

Cycle.run(stage), {
  DOM: makeDOMDriver('#app-container')
})
```

--

What about real world large-apps?

--

Explain why reactive paradigm is better on the "imperative" world.

--

[Slides](https://speakerdeck.com/staltz/see-the-data-flowing-through-your-app)
