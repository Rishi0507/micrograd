# micrograd; Implementing Backpropagation from Scratch

This is a simple autograd engine that I built while following Andrej Karpathy's [micrograd](https://github.com/karpathy/micrograd). The original implementation and all core ideas are his - this repository documents my process of understanding them.

---

## About this

Honestly it's a learning exercise - reading, understanding, and rebuilding a tiny neural network engine line by line.

My goal was to understand how gradients flow actually flow, why topological sort matters, and how a neural network is just a composition of simple mathematical operations chained together.

---

## What I learned

- How a computation graph is built during the forward pass
- Why backpropagation is just the chain rule applied in reverse topological order
- Why `zero_grad` exists and what happens if you forget it
- Weight initialization; swapped random uniform for He initialization, better suited for ReLU activations
- Gradients just flow equivalently when the '+' operation takes place. Might sound funny but didn't actually realise this while I was studying DL with pen and paper :D, and honestly - embarassing

---

## Changes from original

- **He initialization** instead of random uniform for neuron weights
- This resulted in faster convergence. On the toy dataset; 3 steps earlier. Will test on bigger datasets in future to see more differences

---

## Future Scope 

- Try out other weight initilization techniques as well(althought not directly related to the core micrograd idea)

## Credit

All credit to [Andrej Karpathy](https://github.com/karpathy). This repository exists purely as a learning artifact.
