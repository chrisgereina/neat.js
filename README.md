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

As of de5da3149a78c7b19bed8e53d376893540d3eb66 the evolution process is hardcoded to use a dataset to evolve, because there are no visible agents, fitness output is being logged to the console for a four input XOR dataset. The network within the blue flappy-bird background does update to reflect changes in the topology of the network.

## How to format input / output data to evaluate fitness

The format for the dataset used internally to evaluate fitness and evolve is the same as [Neataptic](https://github.com/wagenaartje/neataptic) and [Carrot](https://github.com/liquidcarrot/carrot)

The dataset is a series of objects with two keys, `input` and `output` which correspond to the inputs and outputs of the neural network. Currently the inputs are hardcoded at 4 and the output is hardcoded at 1. Below is a 4 input XOR gate for demonstration.

```
    // XOR is true only if exactly one of the inputs is true
    dataset = [
      { input: [0, 0, 0, 0], output: [0] },
      { input: [0, 0, 0, 1], output: [1] },
      { input: [0, 0, 1, 0], output: [1] },
      { input: [0, 0, 1, 1], output: [0] },
      { input: [0, 1, 0, 0], output: [1] },
      { input: [0, 1, 0, 1], output: [0] },
      { input: [0, 1, 1, 0], output: [0] },
      { input: [0, 1, 1, 1], output: [0] },
      { input: [1, 0, 0, 0], output: [1] },
      { input: [1, 0, 0, 1], output: [0] },
      { input: [1, 0, 1, 0], output: [0] },
      { input: [1, 0, 1, 1], output: [0] },
      { input: [1, 1, 0, 0], output: [0] },
      { input: [1, 1, 0, 1], output: [0] },
      { input: [1, 1, 1, 0], output: [0] },
      { input: [1, 1, 1, 1], output: [0] },
    ];
```
