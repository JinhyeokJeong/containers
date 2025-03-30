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
