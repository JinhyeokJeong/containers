# Containers

This repository contains singularity (apptainer) images that I routinely use. 

- ```python311.def```:
  - basic python environment with numpy, scipy, pandas, matplotlib, and numba.
  - mainly for running Monte Carlo simulations using numpy and scipy.

- ```torch.def```:
  - PyTorch (2.x) environment with CUDA 11.x (python 3.10)
  - for using PyTorch to use neural network models.
  - should use ```--nv``` argument to use GPU
 
- ```bayesflow.def```:
  - Bayesflow, Keras3, PyTorch (2.x), JAX, with CUDA 11.x (python 3.10)
  - for using Bayesflow to do simulation-based Amortized Bayesian Inference with neural network models.
  - should use ```--nv``` argument to use GPU


Build a container based on the def file
- singularity build <my_container.sif> <my_container.def>
  ``` bash
  singularity build python311.sif python311.def
  ```


Open shell inside of the container:

- singularity shell <container.sif>
  ```bash
  singularity shell python311.sif
  ```
  ```bash
  singularity shell --nv bayesflow.sif
  ```

Run Python script inside of the container:

- singularity exec <container.sif> <command>
  ```bash
  singularity exec python311.sif python program.py
  ```
  ```bash
  singularity exec --nv torch.sif python3 program.py 
  ```
