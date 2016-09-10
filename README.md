## Clone Clash

### Overview

The rules of the game are simple:

1) Collect coins
2) Don't crash

How hard can that be?

It starts getting difficult because once you collect your first coin then ever
second a clone ships start spawning from your original start position and following
the exact path you took to the first coin where it de-spawns. After you collect the
second coin, the ships now follow the entire path you have taken form the start, through the first coin, and to the location of the second where they de-spawn. This continues until you collect the required number of coins or the sheer number of clone ships following your old path overwhelms you and you accidentally hit one, ending the game.  


### Functionality & MVP  

In the game, users will be able to:

- [ ] Start, pause, and reset the game
- [ ] Level selection for easy, medium, and hard
- [ ] fly a ship
- [ ] collect coins
- [ ] clones following exact path to a given coin location
- [ ] win / loose a game

In addition, this project will include:

- [ ] A production Readme

### Wireframes

This app will consist of a single screen with game board, game controls, and nav links to the Github, my LinkedIn, my website.  

Game controls will include:
 - Level selection to start the game
 - Stop (Pause) - bound to the space bar
 - Reset buttons to display while paused
 - arrow keys and WASD key bindings for control of ship.  

#### Start Screen
![wireframes](https://s13.postimg.org/oiidhiokn/home.png)

#### Easy Level
![wireframes](https://s10.postimg.org/nulfb5bk9/easy.png)

#### Medium Level
![wireframes](https://s10.postimg.org/mg0aoctex/medium.png)

#### Hard Level
![wireframes](https://s3.postimg.org/43s4gtvkz/hard.png)

### Architecture and Technologies

This project will be implemented with the following technologies:

- Vanilla JavaScript and `jquery` for overall structure and game logic,
- `Easel.js` with `HTML5 Canvas` for DOM manipulation and rendering,
- Webpack to bundle and serve up the various scripts.

In addition to the webpack entry file, there will be three scripts involved in this project:

`game_view.js`: this script will handle the logic for creating and updating the necessary `Easel.js` elements and rendering them to the DOM.

`game.js`: this script will handle the logic behind the scenes. The game object will hold the information of all the `ship`s that are currently in the game as well as the `coin`s.

`ship.js`: this script will keep the logic for the ship such as moving itself, velocity,  path it has taken to get to where it is.

`clone.js`: extends the ship with a path of where to go and when to de-spawn.

`coin.js`: this will hold the coin logic such as where to render and what to do if caught.

### Implementation Timeline

**Day 1**: Setup all necessary Node modules, including getting webpack up and running and `Easel.js` installed.  Create `webpack.config.js` as well as `package.json`.  Write a basic entry file and the bare bones of all 3 scripts outlined above.  Learn the basics of `Easel.js`.  Goals for the day:

- Get a green bundle with `webpack`
- Learn enough `Easel.js` to render an object to the `Canvas` element

**Day 2**: Dedicate this day to learning the `Easel.js` API.  First, build out the `Ship` object to connect to the `GameView` object.  Then, use `game_view.js` to create and render at least the ship.  Have the ship follow a velocity and change directions with key strokes.  Goals for the day:

- Complete the `ship.js` module (constructor, update functions)
- Render a game_view to the `Canvas` using `Easel.js`
- Render ship and move ship around

**Day 3**: Create the coin and ensure that there is proper recording of the path of the ship to use for the clones. Goals for the day:

- Complete the `coin.js` module (constructor, update functions)
- Have a functioning coin system (including scoring)
- Ensure I have a path system for the clones to follow


**Day 4**: create the `clone`s.  Goals for the day:

- Complete the `clone.js` module that extends the ship module
- Have them follow the path that has been setup and de-spawn correctly
- Allow end of game to occur on contact


### Bonus features


- [ ] Adding a element, like a coin, that when captured allows you to kill clones when you hit them. Similar to packman when you get the circles.
