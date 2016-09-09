# Reactive Reality by Massimiliano Mantione

He's working on a company that created a 3D Game in the Web
but now they want to move it to VR

##### The 10 - 90 Rule
**10% _Inspiration_**
**90% _Transpiration_**

### We need UI in 3D
- Usually when we are talking about UI, we are talking about touching the DOM,
the first question could be do we have DOM in WebGL.
- CSS 3D transforms are unnatural and doesn't work with WebGL too
- SVG's inside Canvas

None of this is already integrated with WebGL.

--

### Idea
We can render the Ui in a separeted 2D canvas,
and use that as texture in the 3D canvas

texture: means a way of render a flat dimension to a 3D space and represent
a 2D

### Render the UI
They use React
  - Because separates logic from view
  - DOM-independent (It could manipulate DOM or any Canvas)

### Demo
He made a Todo List App with React and Redux "style" for the logic.
and he's able to reuse the logic for the 3D UI, only replacing the output
of the Components in React.

### For do that, we can use
[React-canvas](https://github.com/Flipboard/react-canvas) by Flipboard
Pixi.js
[Konva.js](http://konvajs.github.io) and [react-konva](https://github.com/lavrton/react-konva)

He picked Konva.js for simplicity and used css-layout for styling

He uses some 3D engine render to use the same logic in a 3 different places
in a normal Web UI, another inside a Canvas frame and the other inside a
Canvas in 3D.
