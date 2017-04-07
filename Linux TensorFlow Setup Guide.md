# Linux TensorFlow Setup Guide for Azure #

This documentation was originally created by James Hong who was a Teaching Assistant for cs224n: Deep Learning with <Title> at Stanford University 

## Option 1: Leveraging the Microsoft Data Science VM ##

### Create the VM ###
NOTE: This is machine is running Open Logic 7.2 CentOS-based linux.  It comes pre-installed with [key software components,](https://docs.microsoft.com/en-us/azure/machine-learning/machine-learning-data-science-linux-dsvm-intro) including Anaconda Python, JupyterHub, and RStudio. 

** Spin it up on a GPU ** 


### Install NVIDIA Cuda Drivers ### 

### Install TensorFlow ### 
Note: These directions are from the [TensorFlow website.](https://www.tensorflow.org/install/install_linux#InstallingAnaconda)
1. Start a terminal
2. Activate your Anaconda container
3. Create a conda environment named tensorflow to run a version of Python by invoking the following command: 
>`$ conda create -n tensorflow`
4. Activate the conda environment by issuing the following command: 
> `$ source activate tensorflow`
> `(tensorflow)$  # Your prompt should change`
5. Issue a command of the following format to install TensorFlow inside your conda environment:
>   ` (tensorflow)$ pip install --ignore-installed --upgrade TF_PYTHON_URL`

where `TF_PYTHON_URL` is the URL of the [TensorFlow Python Package](https://www.tensorflow.org/install/install_linux#the_url_of_the_tensorflow_python_package) For Example, the following command installs the GPU-only version of TensorFlow for Python 3.5 
> `https://storage.googleapis.com/tensorflow/linux/gpu/tensorflow_gpu-1.0.1-cp35-cp35m-linux_x86_64.whl`

#### Validate your TensorFlow Installation ####
You can validate your TensorFlow Installation by following the steps listed under "[Validate your installation](https://www.tensorflow.org/install/install_linux#validate_your_installation)" 