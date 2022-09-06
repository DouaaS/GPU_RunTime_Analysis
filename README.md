# GPU_RunTime_Analysis
Creditting the dataset to: 
Rafael Ballester-Ripoll, Enrique G. Paredes, Renato Pajarola.Sobol Tensor Trains for Global Sensitivity Analysis.In arXiv Computer Science / Numerical Analysis e-prints, 2017Cedric Nugteren and Valeriu Codreanu.
CLTune: A Generic Auto-Tuner for OpenCL Kernels.In: MCSoC: 9th International Symposium on Embedded Multicore/Many-core Systems-on-Chip. IEEE, 2015

Data set includes the following variables: 

Independent Variables: 
1-2. MWG, NWG: per-matrix 2D tiling at workgroup level: {16, 32, 64, 128} (integer)
KWG: inner dimension of 2D tiling at workgroup level: {16, 32} (integer)
4-5. MDIMC, NDIMC: local workgroup size: {8, 16, 32} (integer)
6-7. MDIMA, NDIMB: local memory shape: {8, 16, 32} (integer)
KWI: kernel loop unrolling factor: {2, 8} (integer)
9-10. VWM, VWN: per-matrix vector widths for loading and storing: {1, 2, 4, 8} (integer)
11-12. STRM, STRN: enable stride for accessing off-chip memory within a single thread: {0, 1} (categorical)
13-14. SA, SB: per-matrix manual caching of the 2D workgroup tile: {0, 1} (categorical)
Dependent Variables:
15-18. Run1, Run2, Run3, Run4: performance times in milliseconds for 4 independent runs using the same parameters. They range between 13.25 and 3397.08.

The goal: Predict GPU run time as a function of a number of independent variable using linear regression model. 
