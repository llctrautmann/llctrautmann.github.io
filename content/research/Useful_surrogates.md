---
title: "Are voxel uncertainties useful surrogates for MRI?"
date: 2025-09-01
tags: ["mri", "deep learning", "uncertainty quantification"]
---

## Introduction

### What is Accelerated MRI?

MRI scans are invaluable for diagnosing diseases and planning treatments, but they come with a major drawback: they're slow. Patients must lie still for extended periods, which is uncomfortable and can lead to motion artifacts that degrade image quality. To address this, researchers have been developing deep learning methods to reconstruct high-quality images from undersampled data, which promises cutting scan times significantly.

But here's the catch: when you undersample MRI data, you're asking an AI to fill in the gaps. This introduces uncertainty, and before these methods can be safely deployed in hospitals, we need to know how reliable they really are.

## Voxelwise and structural uncertainty

## Do they correlate?

The short answer is: **No, they do not correlate.**

Looking at the plot below we can see that for a range of image statistics for the voxelwise variance no correlation exists between the value and the volume variance for each segmented structure.

{{< figure src="/imgs/MICCAI2025/VN_fast_correlation_analysis.png" width="600px" alt="Profile"  caption="Corrlation between the normalised volume variance and the voxelwise variance for the Variational Network">}}

## Where to go (maybe)
