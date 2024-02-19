# Sora-XL

A method for eXtremely Long-form video generation using a combination of Sora and NUWA-XL.

## 1. Introduction

[Sora](https://openai.com/sora) is a SOTA video synthesis diffusion model, capable of generating samples of unprecedented realism. However, samples are limited to ~1m. While impressive, this is not sufficient for eXtremely Long-form (XL) video generation. [NUWA-XL](https://arxiv.org/abs/2303.12346) is a framework for producing XL video content using a hieararchical cascade of video diffusion models. NUWA-XL starts by sampling a set of coarse keyframes, representing the overall narrative of the video. Then, local diffusion models are used to sample increasingly fine keyframes in a recursive fashion. This hieararchical approach leads to coherent dynamics over long durations (e.g. 10+ minutes). However, the frame rate and fidelity of samples remains far lower than Sora. The idea of Sora-XL is to combine both approaches, using Sora as the bottom layer diffusion model to interpolate between keyframes. This could allow for XL video with exceptional fidelity.
