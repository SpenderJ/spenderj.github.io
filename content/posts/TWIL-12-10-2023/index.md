---
author: Jules Spender
title: TWIL Pandas vs Polars
date: 2023-12-10
description: "This week I learnt, pandas vs polars 12-10-2023"
toc: false
---

# Pandas, Polars what are these what's their usecases

### Why this topic ?

Hello folks, this week, while browsing through Github I found out this library named [polars](https://github.com/pola-rs/polars).
It seemed to be an alternative to the well known [pandas](https://github.com/pandas-dev/pandas) library. As a big fan of pandas
and having used it for so long, I decided to give it a try and figure if it would solve the few limitations that I had using pandas.

### Pandas: The safe solution

Pandas is the safe path, whoever has already done data anylisis on Python knows Panda. It's been around for years, there's a huge community,
extensive documentation, tons of librairies built around it, and I don't want to know the number of Stack Overflow articles about it (which I contributed to !).
It's familiar, reliable, and gets the job done, especially for smaller datasets and interactive exploration.

**Strengths:** 

- Mature and stable.
- Pythonic and intuitive.
- Visualization capabilities.
- Community and articles.

**Weaknesses:**

- Performance bottlenecks: *Pandas can chug with large datasets, especially when operations involve heavy computation.*
- Memory hungry: *Pandas data structures can be memory-intensive, especially for complex manipulations.*
- Not thread-safe: *Multithreaded operations in Pandas require careful handling to avoid errors.*

### Polars: The new generation

PolaRS is written in Rust. I think that it already scores points in a lot of engineers heart. We've seen more and more
tools written in Rust coming into the Python ecosystem replacing historical tools with better performances (the best example
could be [ruff](https://github.com/astral-sh/ruff) which will make your CI so much faster when it comes to linters).

Polars is the Usain Bolt of the processing, it's extremly fast, efficient and powerfull! Everything is thought about performance,
but on the down side, the community is way smaller, and the visualization tools are lacking (for the moment).

**Strengths:**

- Polars can outperform Pandas.
- Polars memory consumption is really low compared to Pandas on huge Datasets
- Thread-safe and parallel: Polars leverages Rust's concurrency features for efficient multithreaded processing.
- Focus on immutability: Polars data is immutable, leading to cleaner and more predictable code.

**Weaknesses:**

- Newcomer: *Polars is still under development, with a smaller community and fewer libraries compared to Pandas.*
- Less familiar syntax: *Polars borrows some concepts from Rust, which can feel less Pythonic than Pandas.*
- Limited visualization capabilities


### Benchmark

If you want to find a perfectly detailled benchmark, you should consult this medium article that will do way better
than me [PolaRS vs Pandas](https://medium.com/cuenex/pandas-2-0-vs-polars-the-ultimate-battle-a378eb75d6d1).

### What's my take ?

Ultimately, both Pandas and Polars are valuable tools in the data wrangler's arsenal. Understanding their strengths and
weaknesses will help you choose the right weapon for your next data project.
For a simple research I'd stick with Pandas, but if it becomes a bigger challenge, you'll have a better tool with Polars.

Have a great day, and have fun !

Cya
