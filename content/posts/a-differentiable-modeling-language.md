---
title: 'A differentiable modeling language'
date: Fri, 22 Feb 2019 19:00:54 +0000
draft: false
tags: [ideas, modeling]
aliases: ["/2019/02/22/a-differentiable-modeling-language/"]
---

Differentiable programming is getting a little exciting nowadays. The core idea is that you can build a language from the ground up that simultaneous supports both (a) computation of direct numerical results and (b) cheap, cheap computation of the derivative.

The most popular implementation of this idea is [TensorFlow](https://www.tensorflow.org/). TensorFlow is by most accounts a tool for constructing neural networks. The principal way you build a neural network is by designing its _architecture_ as a series of interacting "layers" that compute a _forward prediction_ based on input data and then you _train_ that architecture through a process known as _gradient descent_—which essentially requires computing the derivative of the forward prediction over and over and over.

Before tools like TensorFlow you'd construct the equations for the NN architecture and its derivative by hand. This placed a significant constraint on both the accessibility of the technology and the complexity of architectures you'd reasonably want to explore. It's a big, mostly mechanical, pain in the ass to compute these derivatives.

So TensorFlow creates a lot of leverage by just doing that for you automatically.

Where else do we want cheap derivatives?
----------------------------------------

TensorFlow today enjoys a bit of an underground role as being the premiere language for differentiable programming. While it's geared toward construction of NN architectures, there's nothing preventing you from writing other kinds of "tensor" programs and exploiting the same cheap derivative property.

Cheap derivatives are important in many other statistical and modeling applications. They're the key technique for big hammer tools like [convex optimization](https://en.wikipedia.org/wiki/Convex_optimization) and [Laplacian approximation](https://metacademy.org/graphs/concepts/laplace_approximation). Many physical processes are specified as systems of differential equations where the interaction between derivatives and first order terms is key.

Is TensorFlow a good match for other domains that are further afield of neural network machine learning? Is there an opportunity for new kinds of differentiable programming languages?

I can imagine a differentiable modeling language that's explicitly geared for designing models of physical processes. It'd need a good story for modularity as well as unit quantities and would plausibly want to compile to fast code both on the forward path and the (higher order?) derivative paths. Packaged in a tooling system that prints out traces of intermediate quantities and can run various optimization routines over the core model, this feels like it opens new doors for the process of building, refining, and using these sorts of models.