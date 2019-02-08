# MRIQC from poldracklab

BootStrap: docker
FROM: poldracklab/mriqc:latest

%runscript
    exec /usr/local/miniconda/bin/mriqc "$@"

%environment

%labels
Author mnarayan@noreply.users.github.com
Build-date 2/5/2019
Vendor Ubuntu
Version 16.04

%post
    #------------------------------------------------------------------------------
    # Create local binding point for our HPC
    #------------------------------------------------------------------------------
    mkdir /scratch
    mkdir /share
    mkdir /oak
