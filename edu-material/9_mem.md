# Memory Circuits
It turns out that the most expensive operation in computation is accessing memory, and moving that data from memory to the processor. E.g., doing a DRAM access can be 1000x more expensive (energy-wise) than doing floating point arithmetic in a processor. Neural networks are heavily dependent on memory. Especially given that modern, large-scale neural networks have billions of parameters nowadays, and many of these parameters must be stored in memory. So we will learn more about memory circuits. We will also learn about how memory circuits can be combined with processors, as "in-memory processors" to accelerate deep learning workloads. This makes sense from a neuroscience perspective, because neurons and synapses don't separate memory and processing, like CPUs do.

## Optional YouTube Content
* [SRAM vs DRAM](https://www.youtube.com/watch?v=r787m_IaR1I)
* [How does Flash work?](https://www.youtube.com/watch?v=r2KaVfSH884)
* [Emerging Memory Technologies](https://www.youtube.com/watch?v=aDzUu0L-rdg)
