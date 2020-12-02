# cuda_setup
Setting up cuda libraries on linux and (possibly) PyTorch

I am tired of always having to deal with conflicting installation of binaries, so I adapted a few utility scripts to manage CUDA and CudNN installation across (possibly different) python environments.

This is just a condensed version of what is available in the specific documentation.

# Setting environment variables
```
export CUDA_HOME=/usr/local/cuda-10.0 
export CUDA_ROOT=/usr/local/cuda-10.0 
export CUDA_PATH=/usr/local/cuda-10.0 
export CUDA_HOST_COMPILER=/usr/bin/gcc-7
export PATH=/usr/local/cuda-10.0/bin${PATH:+:${PATH}}  
export LIBRARY_PATH=$LIBRARY_PATH:/usr/local/cuda-10.0/lib64
export LD_LIBRARY_PATH=$LD_LIBRARY_PATH:/usr/local/cuda-10.0/lib64  
```

## Make sure that you install the right version of nvcc with the right cudatoolkit version for pytorch:
```
/usr/local/cuda/bin/nvcc --version
```
this value must match the PyTorch install binaries version (cudatoolkit)

