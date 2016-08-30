# variational Bayes expectation maximization of multivariate gaussians for single particle tracking diffusion analysis

This is a collection of MATLAB scripts to employ vbem analysis.  The main script is main_VBEM.m. The script simulates a set of particle tracks with properties specified by the user and then performs variational inference for the diffusion state properties using the expectation-maximization algorithm.  The algorithm will inherently prune excessive number of states and determine the number of diffusion states supported by the data as well as each state's underlying diffusion properties.  This is not very commented well and is a work in progress.  In some cases when there are many diffusive states that have similar properties, vbem will yield the wrong number of diffusive states.  This may be due to strong priors.  I ended up opting for pEMv2 instead, but I still feel like this elegant approach can yield good results with better prior tuning.