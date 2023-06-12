---
layout: page
title: Optimised double precision floating-point multiplier
description: an exploration into digital design with floating-point data formats
img: /assets/img/fp.jpg
importance: 1
category: work
---

The goal of this project was to design a high-performance <a href="https://en.wikipedia.org/wiki/Double-precision_floating-point_format">double precision floating-point</a>. multiplier using SystemVerilog. This project showcases my expertise in digital design, verification, and synthesis, along with my ability to iterate and optimize designs for improved timing and area performance.

The project began with the development of a fully combinatorial design for the double precision floating-point multiplier. I meticulously designed and implemented the multiplier using SystemVerilog, ensuring its functionality and correctness. To verify the design, I created comprehensive testbenches that covered both directed testing and constrained random testing scenarios. These testbenches allowed me to thoroughly validate the functionality and accuracy of the multiplier design.

To further enhance the design, I ran synthesis simulations using industry-standard tools. By analyzing the area and timing characteristics of the design, I identified areas for improvement and refinement. I employed a systematic approach by incrementally inserting pipeline stages while carefully analyzing timing performance. This iterative process ensured that the design remained within the specified limitations for pipeline stages as outlined in the architecture specification.

One of the key technical successes of this project was the utilization of the Karatsuba algorithm, a fast multiplication algorithm that optimizes performance. By implementing this algorithm, I achieved significant improvements in the multiplier's efficiency and overall performance.

Additionally, I implemented speculation techniques in the rounding logic of the multiplier. This speculation significantly contributed to meeting the timing requirements since rounding logic was no longer dependent on a certain control signal, and hence could be done at an earlier pipeline stage. This allowed for greater parallelism and hence enhanced the overall performance of the design.

To further optimize the design, I experimented with various physical synthesis configurations using Tcl scripting. I explored different synthesis options, including utilizing slow and fast cells, to fine-tune the design for improved timing and area trade-offs. Furthermore, I implemented clock gating techniques to improve power performance, ensuring that the multiplier design achieved a well-balanced profile.

The project showcases my expertise in digital design methodologies and the successful application of various techniques to optimize the double precision floating-point multiplier. It highlights my ability to analyze synthesis results, make informed design choices, and iterate to achieve superior timing, area, and power characteristics.
