## Summary

This repository contains the code (Java and Matlab) and data used in the manuscript "Spatially Fractionated GRID radiation potentiates immune-mediated tumor control" [link](https://www.researchsquare.com/article/rs-3934289/latest).

Specifically, it contains:
1. The HAL / Java code and data to generate agent-based model (ABM) domains from digitized head and neck cancer multiplex immunohistochemistry slides;
2. The HAL / Java code and parameter files necessary to run the ABM;
3. The resulting _in silico_ data files; and
5. The MATLAB code to analyze the data and generate the figures and hypothesis testing as reported in the manuscript.

## HAL / Java and MATLAB coding environments
The ABM related code was developed using the Hybrid Automata Library [HAL](https://halloworld.org/) framework, run in Java 17.2, on the Moffitt HPC. MATLAB version 2022b was mostly used, although updating to 2023a did not cause any differences. 

## Short summary of the process
In MATLAB:
1. Read in the csv file which contains the location of the left bottom and right top corner of the cells, as well as cell type as determined by the core.
2. Calculate the centers of the cells.
3. Assign a cell type flag which corresponds to the cell's type.
4. Do the "reduction".
5. Save the info to a new csv file (mapped.csv)

In java
1. Read in the mapped.csv line by line.
2. Place agents according to the (x,y) coordinate of the center.
3. Assign their correct type.
4. Initialize certain properties by sampling from distributions.
5. Save the generate ABM "model".

Every time a simulation is run, the saved ABM model (#5) is loaded and the random number generator (RNG) is assigned a new seed. (Otherwise they'd have the same random number generator and therefore make the same decisions all the time.)
