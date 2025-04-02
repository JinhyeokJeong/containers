# Containers

This repository contains singularity (apptainer) images that I routinely use. 

- ```python311.def```:
  - basic python environment with numpy, scipy, pandas, matplotlib, and numba.
  - mainly for running Monte Carlo simulations using numpy and scipy.

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

Run Python script inside of the container:

- singularity exec <container.sif> <command>
  ```bash
  singularity exec python311.sif python program.py
  ```
