# TensorRT Installation

This tutorial aims to record the procedure of how to install TensorRT on Ubuntu 16.04. For more details, please refer to [here](https://developer.nvidia.com/blog/speeding-up-deep-learning-inference-using-tensorrt/).

Note that the TensorRT relies on the corresponding cuda and cudnn library. Install them using the deb files by following the tutorial in [here](https://developer.nvidia.com/cuda-10.2-download-archive).

- Download the TensorRT files from [here](https://developer.nvidia.com/nvidia-tensorrt-7x-download);
- Download `TensorRT 7.0.0.11 for Ubuntu 16.04 and CUDA 10.2 deb package`;
```shell
os="ubuntu1604"
tag="cuda10.2-trt7.0.0.11-ga-20191216"
sudo dpkg -i nv-tensorrt-repo-${os}-${tag}_1-1_amd64.deb
sudo apt-key add /var/nv-tensorrt-repo-${tag}/7fa2af80.pub

sudo apt-get update
sudo apt-get install tensorrt

sudo apt-get install python-libnvinfer-dev  # for python2
sudo apt-get install python3-libnvinfer-dev  # for python3
sudo apt-get install uff-converter-tf  # for tensorflow
```

