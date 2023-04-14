# Welcome to Numerical Elixir!

Numerical Elixir is an effort started in 2021 to bring the power of numerical computing to Elixir (and vice-versa).
This organization hosts several projects that empowers Elixir in the areas of data, machine learning, AI, and more.
Our beloved mascot is the [Numbat](https://en.wikipedia.org/wiki/Numbat).

## Key projects

There are 5 key projects in our Numerical Elixir effort. We will briefly summarize them below and draw comparisons
to other ecosystems to help developers familiarize with our work.

<h3><img src="https://github.com/elixir-nx/nx/raw/main/nx/nx.png" alt="Nx" width="120"></h3>

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

<a href="https://github.com/elixir-nx/axon">Explorer</a> brings series (one-dimensional) and dataframes (two-dimensional)
for fast data exploration to Elixir. It brings the power of Rust [via the Polars library](https://github.com/pola-rs/polars)
and it is inspired by [dplyr (from the R community)](https://dplyr.tidyverse.org/).

<h3><img src="https://github.com/elixir-nx/axon/raw/main/axon.png" alt="Axon" width="200" style="margin: 10px 0 -15px -15px"></h3>

<a href="https://github.com/elixir-nx/axon">Axon</a> is a Nx-powered Neural Network library. It splits out into four components:
a Functional API of numerical functions, a high-level Model Creation API, an Optimization API based on [Optax](https://github.com/deepmind/optax),
and a Training API inspired by [PyTorch Ignite](https://pytorch.org/ignite/index.html).

Also check out the <a href="https://github.com/elixir-nx/bumblebee">Bumblebee</a> project, which provides several pre-trained
Neural Networks with [Hugging Face Models integration](https://huggingface.co/models). Together with Livebook, [it only takes
3 clicks to get your first Neural Network running in Elixir](https://news.livebook.dev/announcing-bumblebee-gpt2-stable-diffusion-and-more-in-elixir-3Op73O).

<h3><img src="https://github.com/elixir-nx/scholar/raw/main/images/scholar.png" alt="Scholar" width="220" style="margin: 10px 0 -25px -15px"></h3>

<a href="https://github.com/elixir-nx/scholar">Scholar</a> is the most recent addition to the Nx ecosystem and it focus on
traditional machine learning techniques, such as classification, regression, clustering, dimensionality reduction, metrics,
and preprocessing. Because Scholar is fully built on top of Nx, it fully GPU-ready, vectorizable, distributable, and more.

