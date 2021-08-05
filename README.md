# AlphaFold Singularity Container

This repo provides definition files to build a singularity container of AlphaFold v2 (https://github.com/deepmind/alphafold).

Build instructions from [non-docker setting](https://github.com/kalininalab/alphafold_non_docker) by kalininalab were used.


```
# build base container
singularity build --fakeroot base.sif base.def

# build alphafold container
singularity build --fakeroot alphafold.sif alphafold.def
```
