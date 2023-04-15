# Welcome to Numerical Elixir!

Numerical Elixir is an effort started in 2021 to bring the power of numerical computing to Elixir (and vice-versa).
This organization hosts several projects that empowers Elixir in the areas of data, machine learning, AI, and more.
Our beloved mascot is the [Numbat](https://en.wikipedia.org/wiki/Numbat).

## Key projects

There are 5 key projects in our Numerical Elixir effort. We will briefly summarize them below and draw comparisons
to other ecosystems to help developers familiarize with our work.

<h3><img src="https://github.com/elixir-nx/nx/raw/main/nx/nx.png" alt="Nx" width="120" style="margin-top: 10px"></h3>

<a href="https://github.com/elixir-nx/nx">Nx</a> stands for Numerical Elixir and it is the project that started it all.
Nx is a multi-dimensional tensors library with multi-staged compilation to the CPU/GPU. It plays a similar role to Numpy
in the Elixir community. It is inspired by Google's [`JAX`](https://github.com/google/jax) and ships with its own Tensor
Serving implementation that can run concurrently, distributed over multiple nodes, as well as partitioned across several GPUs.

<h3><img src="https://github.com/livebook-dev/livebook/raw/main/static/images/logo-with-text.png" alt="Livebook" width="250" style="margin: 10px 0 -15px -15px"></h3>

<a href="https://livebook.dev/">Livebook</a> brings the next generation of open-source local-first notebooks to Elixir.
With Livebook you can write interactive and collaborative notebooks, which are truly reproducible, all the way to package
management. If you are not yet familiar with Elixir, Livebook and its smart cells are one of the best ways to get started,
and it features [a growing ecosystem of integrations](https://livebook.dev/integrations).

<h3><img src="https://github.com/elixir-nx/explorer/raw/main/explorer.png" alt="Explorer" width="200" style="margin: 10px 0 -15px -15px"></h3>

<a href="https://github.com/elixir-nx/explorer">Explorer</a> brings series (one-dimensional) and dataframes (two-dimensional)
for fast data exploration to Elixir. It brings the power of Rust [via the Polars library](https://github.com/pola-rs/polars)
and it is inspired by [dplyr (from the R community)](https://dplyr.tidyverse.org/).

<h3><img src="https://github.com/elixir-nx/axon/raw/main/axon.png" alt="Axon" width="200" style="margin: 10px 0 -15px -15px"></h3>

<a href="https://github.com/elixir-nx/axon">Axon</a> is a Nx-powered Neural Network library. It splits out into four components:
a Functional API of numerical functions, a high-level Model Creation API, an Optimization API based on [Optax](https://github.com/deepmind/optax),
and a Training API inspired by [PyTorch Ignite](https://pytorch.org/ignite/index.html).

Also check out the <a href="https://github.com/elixir-nx/bumblebee">Bumblebee</a> project, which provides several pre-trained
Neural Networks with [Hugging Face Models integration](https://huggingface.co/models). Together with Livebook, [it only takes
3 clicks to get your first Neural Network running in Elixir](https://news.livebook.dev/announcing-bumblebee-gpt2-stable-diffusion-and-more-in-elixir-3Op73O).

For integration with other platforms, check out [AxonONNX](https://github.com/elixir-nx/axon_onnx).

<h3><img src="https://github.com/elixir-nx/scholar/raw/main/images/scholar.png" alt="Scholar" width="220" style="margin: 5px 0 -25px -15px"></h3>

<a href="https://github.com/elixir-nx/scholar">Scholar</a> is the most recent addition to the Nx ecosystem and it focus on
traditional machine learning techniques, such as classification, regression, clustering, dimensionality reduction, metrics,
and preprocessing. Because Scholar is fully built on top of Nx, it is fully GPU-ready, vectorizable, distributable, and more.

<br />

## Why Elixir?

The goal of the Nx project is to marry the power of numerical computing with the Erlang VM capabilities for building concurrent,
scalable, and fault-tolerant systems.

Elixir is a functional programming language that runs on the Erlang VM. And, at this point, you might ask: is functional programming
a good fit for numerical computing? One of the main concerns is that immutability can lead to high memory usage when working with
large blobs of memory. And that's true!

However, it turns out that the most efficient way of executing numerical computations is by first building a graph of all computations,
then compiling that graph to run on your CPUs/GPUs just-in-time. At this point, your numerical computing code becomes a function:

    input -> [compiled numerical computing graph] -> output

The `input` is an Elixir data-structure. Inside the function, the algorithm is highly optimized and free to mutate the data in any way
it seems fit. Then we get an output that once again must obey Elixir semantics.

To build those graphs, immutability becomes an indispensable tool both in terms of implementation and reasoning. As an example, the JAX
library for Python, which has been one of the inspirations for Nx, also promotes functional and immutable principles:

> JAX is intended to be used with a functional style of programming
>
> — JAX Docs

> Unlike NumPy arrays, JAX arrays are always immutable
>
> — JAX Docs

At the end of the day, Elixir provides the functional foundation and a powerful macro system that allows us to compile a subset of Elixir to
the CPU/GPU.

With the addition of `Nx.Serving`, we started to marry the benefits of the Erlang VM with numerical computing. With `Nx.Serving`, you can
batch numerical computing requests, as well as load balance requests over a cluster of machines
([see the announcement](https://news.livebook.dev/distributed2-machine-learning-notebooks-with-elixir-and-livebook---launch-week-1---day-2-1aIlaw)).
This makes it easy to embed and scale Nx code within your existing Elixir systems, both horizontally and vertically, and without a need
for third-party services. Our goal is to apply those principles to our whole Numerical Elixir stack.

We also expect numerical computing to complement the Elixir ecosystem in different ways, such as:

  * running Machine Learning models in real-time within your [Phoenix web application](https://phoenixframework.org/)

  * deploying models, signal processing, and data modelling inside embedded systems [via Nerves](https://www.nerves-project.org/)

  * incorporating data analysis and classification algorithms inside concurrent data pipelines powered [by Broadway](https://www.elixir-broadway.org/)

  * adding audio and video processing and AI capabilities to media systems [through Membrane](https://membrane.stream/)

## Resources

Here is a non-exhaustive list of resources put together by Numerical Elixir contributors.

### Videos

  * [(2023) Data wrangling with Livebook and Explorer](https://news.livebook.dev/data-wrangling-in-elixir-with-explorer-the-power-of-rust-the-elegance-of-r---launch-week-1---day-5-1xqwCI) (Livebook, Explorer)

  * [(2023) Build and deploy a Machine Learning powered chat app to Hugging Face in 15 mninutes](https://news.livebook.dev/build-and-deploy-a-whisper-chat-app-to-hugging-face-in-15-minutes---launch-week-1---day-4-wYM0w) (Nx, Livebook, Bumblebee)

  * [(2023) Distributed² Machine Learning notebooks with Elixir and Livebook](https://news.livebook.dev/distributed2-machine-learning-notebooks-with-elixir-and-livebook---launch-week-1---day-2-1aIlaw) (Nx, Livebook, Bumblebee)

  * [(2022) The Future AI Stack by Chris Grainer](https://www.youtube.com/watch?v=Y2Nr4dNu6hI) (Explorer, Axon)

  * [(2022) Announcing Bumblebee: pre-trained machine learning models for GPT2, StableDiffusion, and more](https://news.livebook.dev/announcing-bumblebee-gpt2-stable-diffusion-and-more-in-elixir-3Op73O) (Livebook, Bumblebee)
  
  * [(2022) Meta-programmable functional notebooks with Livebook @ Live Programming Splash 2022 by José Valim](https://www.youtube.com/watch?v=EhSNXWkji6o) (Livebook)
  
  * [(2022) Axon: functional programming for deep learning](https://www.youtube.com/watch?v=NWXSiZ-vi-o) (Axon)

  * [(2021) Build a neural network from scratch with Nx @ Lambda Days by José Valim ](https://www.youtube.com/watch?v=fPKMmJpAGWc) (Nx)
  
### Articles

  * [(2023) Audio Speech Recognition in Elixir with Whisper Bumblebee by Sean Moriarity](https://dockyard.com/blog/2023/03/07/audio-speech-recognition-in-elixir-with-whisper-bumblebee)
  
  * [(2002) Catching fraud with Elixir and Axon by Sean Moriarity](https://dockyard.com/blog/2022/04/07/catching-fraud-with-elixir-and-axon)

  * [(2022) An end-to-end example of running a Machine Learning model with Elixir in production by Philip Brown](https://fly.io/phoenix-files/recognize-digits-using-ml-in-elixir/)
  
  * [(2022) Nx for absolute beginners by Sean Moriarity](https://dockyard.com/blog/2022/03/15/nx-for-absolute-beginners)  
