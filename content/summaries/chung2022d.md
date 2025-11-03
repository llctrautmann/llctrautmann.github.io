---
date: '2025-10-31'
draft: false
toc: false
title: 'Parallel Diffusion Models of Operator and Image for Blind Inverse Problems'
---

# Introduction

## Abstract
> Diffusion model-based inverse problem solvers have demonstrated state-of-the-art performance in cases where the forward operator is known (i.e. non-blind). However, the applicability of the method to blind inverse problems has yet to be explored. In this work, we show that we can indeed solve a family of blind inverse problems by constructing another diffusion prior for the forward operator. Specifically, parallel reverse diffusion guided by gradients from the intermediate stages enables joint optimization of both the forward operator parameters as well as the image, such that both are jointly estimated at the end of the parallel reverse diffusion procedure. We show the efficacy of our method on two representative tasks – blind deblurring, and imaging through turbulence – and show that our method yields state-of-the-art performance, while also being flexible to be applicable to general blind inverse problems when we know the functional forms.

![Fig_1](/imgs/chung2022d_1.png/)


## Three points 
### Blind vs non-blind inverse problems

Blind inverse problems are basically the evil twin of regular inverse problems. In a regular inverse problem, we have a good understanding of the forward operator and we have some form of mathematical way to write it down, which introduces a lot less instabilities into the optimization process because we fundamentally just have to optimize for the image that we want to recreate, but not the forward operator itself. In a blind inverse problem, what we get is basically multiple unknowns. So we have some mapping between the measurements and our image provided by the forward operator, but at the same time, we have no idea what the forward operator really is. So we need to also approximate the forward operator and this makes optimization naturally quite a less stable and quite more fragile compared to the regular inverse problem setup. 

In the regular inverse problem setup we usually operate with the following equation: 

$$\tag{1}\large \boldsymbol{y}=\mathcal{H}(\boldsymbol{x})+\boldsymbol{n}$$
And the physics of the operator H are known. This could, for example, be a Fourier transform, some subsampling operation,  combined with some sensitivity maps from multiple coils in an MRI machine, which can be formulated as a matrix operator operating on the image that we want to reconstruct. Hence we can deconstruct the forward operator into linear sub-operations that are sequentially occurring on the image. 

$$\tag{2}\large\mathcal{H}= \mathcal{F}\mathcal{S}\mathcal{D}^\downarrow$$
This makes the forward operator hard to work with and the problem is still ill-posed or ill-conditioned, but at least we can formulate it in a mathematically analytical way, and we can just use it as a plug-and-play forward operator. In the blind inverse problem scenario, we don't have full access to the information of the forward operator, which makes the problem considerably harder because now we have multiple variables that need to be optimized. So for the blind inverse case we get the following equation: 

$$\tag{3} \large \boldsymbol{y}=\mathcal{H}_{\varphi}(\boldsymbol{x})+\boldsymbol{n}$$
Where we do not have the ability to decompose the forward operator linearly,

$$\tag{4}\large\mathcal{H}= \text{?}$$

 but we can describe it as a function that is parameterized that can be learned. 

