# Histopathology Image Registration Enhancement

**Research paper:** *Iterative Landmark Pair Pruning for Large-Scale Histopathology Image Registration Enhancement*  
**Author:** Runze Leng  
**Affiliation:** Department of Mathematics and Statistics, Georgia State University

[**Read the full paper (PDF)**](paper.pdf)

## Overview

Accurate alignment of serial histopathology images is essential for three-dimensional (3D) tissue reconstruction and digital pathology analysis. Large image sizes and tissue deformation make reliable registration challenging, particularly when initially matched landmarks contain errors.

This paper presents an **iterative landmark pair pruning** method that improves image registration by identifying spatially consistent landmark matches, removing outliers, and progressively updating a set of trusted landmark pairs.

## Method

The proposed registration enhancement procedure has three main stages:

1. **Initial landmark matching:** Detect candidate landmarks and match them across reference and target images using normalized cross-correlation (NCC).
2. **Trusted pair identification:** Evaluate local spatial consistency to identify reliable landmark pairs.
3. **Iterative refinement:** Remove inconsistent matches, expand and update the trusted landmark set, and use the refined matches to estimate the spatial transformation.

The method is intended as a fine-tuning step for registration of large-scale serial histopathology images.

## Experimental Results

The method was evaluated on simulated landmark pairs and **40 hematoxylin-and-eosin (H&E)-stained histopathology images** of serial tissue sections.

| Evaluation | Reported improvement |
| --- | ---: |
| Landmark-pair accuracy in simulation | **42.6%** on average |
| Correlation (real images) | **35.23%** |
| Structural similarity (real images) | **17.56%** |
| Mutual information (real images) | **6.30%** |

The paper reports improved registration quality across multiple similarity measures. A noted limitation is that the procedure can fail to identify trusted matches when the initial proportion of correct landmark pairs is very low (typically below 30%).

## Paper

The complete methodology, algorithm, experimental setup, figures, and references are available in [**paper.pdf**](paper.pdf).

*This repository shares the research paper and its summary; it does not include an implementation of the algorithm.*
