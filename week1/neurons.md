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

   \[
   H = (X_1 \times W_1) + (X_2 \times W_2) + (X_3 \times W_3) + \dots
   \]

2. **Activation Function**: After calculating the weighted sum, the neuron applies an **activation function** to the result. This function is usually a non-linear function like the **sigmoid function**, which helps the model learn more complex patterns.

   The sigmoid function looks like this:

   \[
   f(H) = \frac{1}{1 + e^{-H}}
   \]

   This function squashes the output between 0 and 1, which is useful for making decisions or classifications.

### Example of an Artificial Neuron

Let’s say we have three inputs:

- \( X_1 = 0.5 \)
- \( X_2 = 0.3 \)
- \( X_3 = 0.2 \)

And their respective weights:

- \( W_1 = 0.4 \)
- \( W_2 = 0.7 \)
- \( W_3 = 0.2 \)

First, we calculate the weighted sum \( H \):

\[
H = (0.5 \times 0.4) + (0.3 \times 0.7) + (0.2 \times 0.2) = 0.45
\]

Next, we apply the sigmoid activation function to \( H \):

\[
f(0.45) = \frac{1}{1 + e^{-0.45}} \approx 0.61
\]

So, the output of the neuron in this case is approximately **0.61**.

And that’s the basic idea behind artificial neurons. They take inputs, process them with weights and an activation function, and produce an output.
