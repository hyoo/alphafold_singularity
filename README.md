# AlphaFold Singularity Container

This repo provides definition files to build a singularity container of AlphaFold v2 (https://github.com/deepmind/alphafold).

Build instructions from [non-docker setting](https://github.com/kalininalab/alphafold_non_docker) by kalininalab were used.

## Build container
```
# build base container
singularity build --fakeroot base.sif base.def

# build alphafold container
singularity build --fakeroot alphafold.sif alphafold.def
```

## Run Alphafold
```
singularity exec --nv -B <DATA_DIR> alphafold.sif bash
source /opt/miniconda3/etc/profile.d/conda.sh
conda activate alphafold
cd /opt/alphafold/
./run.sh -d <DATA_DIR>  -o <OUTPUT_DIR> -m model_1 -f <SEQUENCE_FILE> -t 2020-05-14
```

