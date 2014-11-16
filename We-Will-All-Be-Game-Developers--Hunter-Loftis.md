# We Will All Be Game Developers
*Hunter Loftis*

## I Am Not a Game Developer
*Why should I care?*

- Forcing yourself to make a game will give you awesome skills as a developer
- It is easy to make money from JavaScript games nowadays since it is compatible everywhere
- App interfaces are becoming more game-like

## Move Rendering onto the Hardware

- Software rendering sucks
  - Typical game rendering is done on the GPU
  - WebGL renders on the GPU
- WebGL platforms--1.7 billion devices sold this year
- JS + WebGL architecture
  - Babylon.js--3D engine for JavaScript

## Minimize and Isolate State

- replace state with 'pure' functions)

```javascript
function Player() {
  // position, speed, velocity
  this.x = [0,0,0];
  this.y = [0,0,0];
  this.interval = [1,1,1];
  this.distance = 0;
}
```

- Zero side-effects functions (no storage)
  - Speeding up and slowing down the character doesn't require extra code because velocity is a function

## Separate Rendering and Simulation

- requestAnimationFrame isn't enough
- Use a browser timeline
  - not ```setInterval(frame, 0);```
  - requestAnimationFrame is allowed to drop frames
  - you're simulation will get out of sync
  - use a time accumulator

## Step at a Constant Time Interval

- Especially for physics, momentum, scrolling, etc.

## Simulate at a Higher Frequency Than Rendering

- e.g. 60fps render => 180 Hz
- smaller steps minimize vsync jitter

## My Favorite Bug

> The goal is to make systems that are more deterministic so they can be tested.

## Suggested Tools

- Physics - Matter.js
- 2D Graphics - Pixi.js
- 3D Graphics - ThreeJS, BabylonJS
- Multiplayer - npm install ws + Heroku
- DOM rendering - React.js

## Q&A

### How do you separate the simulation from the rendering?

- Simulation can be a nested/inner loop inside your frame
