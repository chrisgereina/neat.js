# NEAT JS

This is a NEAT implementation originating from Code Bullet's demonstration on YouTube

## Getting Started

Currently the project is a front-end NEAT implementation in JavaScript for demonstration purposes. The project uses the [P5.js](https://p5js.org/reference/) library to draw a flappy-bird game and test the NEAT implemenation.

How to start the evolution process:

1. Navigate to the `src/` folder using your terminal
1. Create a server to host the project with `python -m SimpleHTTPServer`
1. Open a browser and type `http://127.0.0.1:8000`

*SimpleHTTPServer expects there to be an index.html file in the root directory to serve as the initial file*

## Interacting with the implementation

Open your browser's console

As of de5da3149a78c7b19bed8e53d376893540d3eb66 the evolution process is hardcoded to use a dataset to evolve, because there is no visual component the results are currently being sent to the browser console.