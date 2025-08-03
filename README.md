# *baal-nf* vignette
Vignette to run the *baal-nf* pipeine with a real ChIP-Seq dataset presented in the *baal-nf* paper. Here we will investigate the transcription factor TAL1. We recommend running this on a high-performance compute cluster (HPC) to allow efficient parallelization of the nextflow pipeline. *baal-nf* is currently configure to run on the University of Edinburgh cluster, Eddie, but could be run on another HPC system if the appropriate profile is added. nf-core provides configurations for many institutions that could be leveraged by the user: https://github.com/nf-core/configs/tree/master/conf. Multiple profiles can be used in a single run, and we recommend always using the `singularity` profile for package management, as this establishes reproducible software environments for the entire pipeline.  

## Setup

This code can be easily parallelized on the University of Edinburgh cluster, Eddie. In order to run this analysis, you must have nextflow and singularity installed prior. This can easily be done using the package manager conda. To install conda, follow the instructions here: https://www.anaconda.com/docs/getting-started/miniconda/install#linux-terminal-installer. Once installed, you can create the required environment using:

```
conda install -n nextflow conda-forge::singularity=3.7.1 bioconda::nextflow=24.10.0
```

Make sure to activate your conda environment prior to running nextflow with:

```
conda activate nextflow
```

This repository will act as a base for running *baal-nf*. Please clone this repository and run from here:

```
git clone https://github.com/BAAL-NF/vignette.git 
```

## Input files

Input files can be downloaded from the `vignette` directory on the Open Science Framework (OSF) at https://osf.io/rwjec/files/osfstorage. Please download these to match the same directory substructure imposed on OSF. 

```
nextflow pull BAAL-NF/baal-nf
```

```
nextflow run BAAL-NF/baal-nf -c nextflow.config -profile eddie
```


