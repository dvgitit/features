## Compatibility

This Feature adds shared libraries for NVIDIA CUDA and is only useful for devcontainers that run on a host machine with an NVIDIA GPU. Within your devcontainer, use the `nvidia-smi` command to ensure that your GPU is available for CUDA.

If the `nvidia-smi` command is not available within your devcontainer, you may need to complete the following steps:

### Install the NVIDIA Container Toolkit

Follow [NVIDIA's instructions to install the NVIDIA Container Toolkit](https://docs.nvidia.com/datacenter/cloud-native/container-toolkit/overview.html) on your host machine. The NVIDIA Container Toolkit is available on a variety of Linux distributions. Make sure you have installed the NVIDIA driver for your Linux distribution before installing the NVIDIA Container Toolkit.

### Enable GPU passthrough

Enable GPU passthrough to your devcontainer by adding `["--gpus", "all"]` to your devcontainer's `runArgs` property. Here's an example of a devcontainer with this property:

```json
{
  "runArgs": ["--gpus", "all"]
}
```
