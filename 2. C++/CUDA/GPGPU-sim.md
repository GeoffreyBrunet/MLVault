**MOC**:: [[2. C++ MOC]]
**Tags**:: #cplusplus #cuda

# Introduction
GPGPU-Sim provides a detailed simulation model of a contemporary GPU running CUDA and/or OpenCL workloads.

# Use GPGPU-sim
## Installation
> Prerequisites: A computer with docker installed, no GPU needed.
- Dowload docker image:
```shell
docker pullsocalucr/gpgpu-sim
```
- Start container in interactive mode
```shell
docker run -w /root -it socalucr/gpgpu-sim /bin/bash
```
- Compile GPGPU-sim
```shell
cd ~/gpgpu-sim_distribution
```
```shell
source setup_environment
```
```shell
make clean
```
```shell
make
```
- Check installation and **nvcc** (Nvidia Cuda Compiler) version:
```shell
nvcc --version
```
