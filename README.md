## Summary

This repository contains the code (Java and Matlab) and data used in the manuscript "Spatially Fractionated GRID radiation potentiates immune-mediated tumor control" [link](https://www.researchsquare.com/article/rs-3934289/latest).

Specifically, it contains:
1. The HAL / Java code and data to generate agent-based model (ABM) domains from digitized head and neck cancer multiplex immunohistochemistry slides;
2. The HAL / Java code and parameter files necessary to run the ABM;
3. The resulting _in silico_ data files; and
5. The MATLAB code to analyze said data and generate the figures and hypothesis testing as reported in the manuscript.

## HAL / Java and MATLAB coding environments
The ABM related code was developed using the Hybrid Automata Library [HAL](https://halloworld.org/) framework, run in Java 17.2, on the Moffitt HPC. MATLAB version 2022b was mostly used, although updating to 2023a did not cause any differences. 
