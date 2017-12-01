# MRIQC from poldracklab

BootStrap: docker
From: poldracklab/mriqc:latest

%runscript
    exec /usr/local/miniconda/bin/mriqc "$@"

%environment

%labels
Author zhifang.ye.fghm@gmail.com
Build-date 1/12/2017
Vendor Ubuntu
Version 0.10.0

%post
    #------------------------------------------------------------------------------
    # Change timezone to Shanghai
    #------------------------------------------------------------------------------
    ln -fs /usr/share/zoneinfo/Asia/Shanghai /etc/localtime
    dpkg-reconfigure --frontend noninteractive tzdata
    #------------------------------------------------------------------------------
    # Fix possible permission issue, from docker2singularity.sh code
    #------------------------------------------------------------------------------
    chmod -R a+rX /usr/local/miniconda
    chmod +x /usr/local/miniconda/bin/*
