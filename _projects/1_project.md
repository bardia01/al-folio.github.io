---
layout: page
title: Master's Project - Learnable quantisation through paramaterised companding functions.
description: Investigating non-standard representations in ultra low precision neural networks.
importance: 1
img: /assets/img/fpga.jpg
category: work
---

This project was conducted as part of my Master's degree at Imperial College London. The project was supervised by Dr. George Constantinides. I self-proposed this project after reading various papers in the field of hardware for machine learning. My aim was to implement a trainable quantisation scheme optimised for LUT-based neural networks. The project was conducted over my fourth year at university was completed in 2024. The following is the abstract of the project.

<u> Abstract </u>


Neural networks have become integral to numerous computational tasks, yet their substantial re-
source demands pose significant challenges. Quantisation techniques have shown promise in reduc-
ing the computational load during neural network inference. However, the efficiency of these tech-
niques is often constrained by the necessity for uniform quantisation, in order to facilitate efficient
arithmetic particularly when deployed onto GPUs. PolyLUT, a novel lookup table (LUT)-based
neural network deployment strategy, offers a solution by encapsulating neurons into input-output
bit mappings, thereby mitigating the costs associated with non-standard data-type conversions
and arithmetic. This project investigates the application of non-standard data representations
within PolyLUT, focusing on parameterised non-uniform quantisation schemes that enable data
representation learning. The findings show that learned non-uniform quantisation can improve
network performance such that test accuracy is higher than uniformly quantised networks with
larger bit-widths. Therefore, networks can be deployed with lower bit-widths with no accuracy
loss, resulting in significant resource reductions. In some cases resources were reduced by a factor
of two with no accuracy loss.

<div class="row">
    <div class="Test accuracy of network with trained quantisation (PW per tensor) versus baseline (No transform)">
        {% include figure.html path="assets/img/original_polylut_zoom.drawio.png" title="Performance Zoom" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

<div class="caption">
    The test accuracy of a JSC-M-LITE (small 3-layer toy network designed for the jet tagging task) network when trained from scratch with bit-width 3 for each layer. The blue line represents the performance under uniform quantisation, and the
    red line represents the performance under non-uniform quantisation implemented via the piecewise
    learnable transform scheme.
</div>