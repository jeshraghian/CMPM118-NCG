# Spiking Neural Networks
Let's now look at how the brain does its thing. 
Actually tbh, we don't really know.
But we have some different views on what makes the brain efficient.

As one example, biological neurons rely on voltage bursts known as "action potentials", or "spikes", to communicate.
Can these be used to make deep learning more efficient? 

## Spiking Neural Networks
* [Action Potentials in the Neuron](https://www.youtube.com/watch?v=oa6rvUJlg7o)
* [Training Spiking Neural Networks Using Lessons from Deep Learning: Sections 3 onwards](https://arxiv.org/abs/2109.12894)

## Coding up SNNs
* [Hands-on with snnTorch](https://youtu.be/aUjWRpisRRg?si=_i7K9oD4-S1XSkx4)
* [snnTorch Tutorial series: Tutorial 2,5,7 at least](https://snntorch.readthedocs.io/en/latest/tutorials/index.html)

I want to make it very clear that SNNs can be a pain in the ass to train compared to non-spiking neural networks.
Compressing activations to 1/0 is extremely lossy, and modern computers can do computation pretty cheaply anyway. 
For most deep learning workloads, it's memory access that is the most expensive part. 
So it's primarily sparsity that makes the most sense here. 
As a result, my opinions on what aspect of SNNs to focus on have evolved a bit in the past couple of years.

* [A talk that summarizes my take on SNNs in 2025](https://youtu.be/5tzA72tOlRw?si=abL3v3NWKcYFDzw9)

In this above talk, I start to dive deeper into state-space models. 
Spiking neural networks share a ton of similarities with SSMs. If you wish to dive deeper into SSMs, then check out the following material on RNNs:

# Recurrent Neural Networks

RNNs are neural networks that process sequences and time-varying data. Think: audio signals, language, biomedical signals, etc. 

We used to use RNNs in language pre-2017. But then the Transformer architecture became popularized thanks to language models.
Some people will say RNNs are totally redundant now. I disagree - they're significantly more efficient than Transformers, can be useful in modelling the brain (a chunky time-varying machine), and my lab is developing RNN-variants that meet Transformer-level performance under certain scenarios.

From here, this material starts becoming much more tightly related to the work in my lab.

## RNNs 101
* [Josh Starmer Lecture Series: Videos 15-18](https://www.youtube.com/playlist?list=PLblh5JKOoLUIxGDQs4LFFD--41Vzf-ME1)
* [Andrew Ng's video on Sequence Models](https://youtu.be/S7oA5C43Rbc?si=Wmd-DrbmV7wf4LW8) - Andrew actually deleted this from his main channel. My guess is it's because Transformers dominated the scene. I still think it's valuable. Pay particular attention to Backprop-Through-Time. 

## Optional viewing
Recurrent neural networks have a lot of problems with them. With some slight modifications, they become extremely powerful.
My lab has been paying a lot of attention to *State-Space Models*. 
* [Some basics of state-space models](https://www.youtube.com/watch?v=5tzA72tOlRw&t=2567s) - Note, state-space models are just a fancy name for recurrent networks that are linear through time.
* [A paper on hybrid linear attention](https://arxiv.org/abs/2507.06457) - This combines linear RNNs with Transformers (which you'll learn next week). This was a paper co-led by a former undergraduate at UCSC who I met through CMPM 118! 
* [HGRN2](https://arxiv.org/abs/2404.07904) - A very powerful linear recurrent neural network used in language modeling
* [Linear Attention](https://www.youtube.com/watch?v=d0HJvGSWw8A&ab_channel=SashaRush)
* [Flash Linear Attention Library](https://github.com/fla-org/flash-linear-attention)
