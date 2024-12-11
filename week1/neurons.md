# Understanding and Implementing Artificial Neurons

## Introduction

Now we’re going to break down artificial neurons, how they work, and the math behind them.

## Biological Neurons (Quick Overview)

First, let’s quickly touch on biological neurons. A biological neuron has three main parts:

1. **Dendrites**: These receive signals from other neurons. Think of them like the _inputs_ of the neuron.
2. **Cell Body**: This processes the signals it gets from the dendrites. It’s like the neuron’s _control center_.
3. **Axon**: Once the cell body processes the signals, the axon transmits the output to other neurons through synapses.

The power of a biological neuron comes not just from the neuron itself but from its connections with billions of other neurons. These connections form the foundation of our brain’s incredible computational ability.

## Artificial Neurons

Now, let's talk about artificial neurons. These are modeled loosely on biological neurons, but they’re a lot simpler.

An artificial neuron takes multiple **inputs** (just like the dendrites), each with a **weight** associated with it. The neuron computes a weighted sum of all its inputs, applies an **activation function**, and produces an **output**.

### The Math Behind Artificial Neurons

An artificial neuron works in two main steps:

1. **Weighted Sum**: The neuron first calculates the sum of each input multiplied by its corresponding weight.

   ![equation](http://latex.codecogs.com/gif.latex?H%20=%20(X_1%20\times%20W_1)%20+%20(X_2%20\times%20W_2)%20+%20(X_3%20\times%20W_3)%20+%20\dots)

2. **Activation Function**: After calculating the weighted sum, the neuron applies an **activation function** to the result. This function is usually a non-linear function like the **sigmoid function**, which helps the model learn more complex patterns.

   The sigmoid function looks like this:

   ![equation](http://latex.codecogs.com/gif.latex?f(H)%20=%20\frac{1}{1%20+%20e^{-H}})

   This function squashes the output between 0 and 1, which is useful for making decisions or classifications.

### Example of an Artificial Neuron

Let’s say we have three inputs:

- ![equation](http://latex.codecogs.com/gif.latex?%20X_1%20=%200.5%20)
- ![equation](http://latex.codecogs.com/gif.latex?%20X_2%20=%200.3%20)
- ![equation](http://latex.codecogs.com/gif.latex?%20X_3%20=%200.2%20)

And their respective weights:

- ![equation](http://latex.codecogs.com/gif.latex?%20W_1%20=%200.4%20)
- ![equation](http://latex.codecogs.com/gif.latex?%20W_2%20=%200.7%20)
- ![equation](http://latex.codecogs.com/gif.latex?%20W_3%20=%200.2%20)

First, we calculate the weighted sum ![equation](http://latex.codecogs.com/gif.latex?H):

![equation](http://latex.codecogs.com/gif.latex?H%20=%20(0.5%20\times%200.4)%20+%20(0.3%20\times%200.7)%20+%20(0.2%20\times%200.2)%20=%200.45)

Next, we apply the sigmoid activation function to ![equation](http://latex.codecogs.com/gif.latex?H):

![equation](http://latex.codecogs.com/gif.latex?f(H)%20=%20\frac{1}{1%20+%20e^{-H}})

So, the output of the neuron in this case is approximately **0.61**.

And that’s the basic idea behind artificial neurons. They take inputs, process them with weights and an activation function, and produce an output.
