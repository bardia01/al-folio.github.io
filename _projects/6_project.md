---
layout: page
title: Hardware-based mixed-format arithmetic accelerator
description: an exploration into optimizing datapaths
importance: 1
img: /assets/img/fpga.jpg
category: work
---

This project was exploratory, we set out with a goal of investigating how to optimise datapath design while limited by resource constraints. To be able to measure progress, at each milestone we tested the design by computing the same mathematical expression, which was a summation involving exponential and sinusoid factors. 

The development process began by using a primitive design (implementing the function in software without any DSPs enabled on the soft-processor), and measuring the performance. Using this, we could analyse the data and hypothesize where the bottlenecks of the system lied. Then, we used simulations and experimentation to collect data about the performance gain versus resource cost of any suggested changes. Using this information, we were able to iterate the system architecture and measure the resultant performance.

Within the design phase, it was important to make sure each module implemented was verified with thorough and versatile testing so as to not lose accuracy in the output.


In the graph below, you can see the progress made across various milestones.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/dsd_full_diagram.jpg" title="Micro-architecture" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col">
        <div class="col-sm mt-3 mt-md-0">
            {% include figure.html path="assets/img/dma_diag.jpg" title="System" class="img-fluid rounded z-depth-1" %}
        </div>
        <div class="col-sm mt-3 mt-md-0">
            {% include figure.html path="assets/img/performance.jpg" title="Data" class="img-fluid rounded z-depth-1" %}
        </div>
    </div>
</div>
<div class="caption">
    On the left, the micro-architecture of the arithmetic block deployed on an entry level FPGA. On the right, the full system diagram including the DMA module, and the performance against resource usage and execution time across various milestones in the development process.
</div>
In any digital design, the architecture is created by balancing resource usage and performance. As a result, all our performance data is complemented by the resource usage for each respective milestone in development. Resource usage recorded was a function of memory utilisation, LUT usage, register utilisation and DSP utilisation.


The design had single-precision floating-point input and output. However, to accelerate computation of sinusoids, we implemented the <a href="https://en.wikipedia.org/wiki/CORDIC">CORDIC algorithm</a>. This meant that we had to experiment with floating-point to fixed-point conversions. To ensure that the loss of accuracy was limited to a known bound, we conducted Monte-Carlo simulations on the accuracy with various fixed-point word lengths using MATLAB. The same experiment methodology was repeated for various number of CORDIC iterations.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/monte_carlo_wordlength.jpg" title="Monte-Carlo" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

To increase performance, it is important to consider the entire datapath and the bottle-necks within it. For example, the data shows that improvements in the compute unit were increasing performance, however, the design was eventually bottle-necked by the speed of memory accesses. As a result, optimising the compute units further was not improving performance. Therefore, we implemented a DMA access, which enabled for much faster memory accesses.