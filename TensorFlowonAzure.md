# Intro to TensorFlow on Azure #
The [Data Science Virtual Machine for Linux on Azure](https://docs.microsoft.com/en-us/azure/machine-learning/machine-learning-data-science-dsvm-ubuntu-intro) is an Ubuntu-based virtual machine image that makes it easy to get started with deep learning on Azure. Deep learning tools include:
- [Caffe](http://caffe.berkeleyvision.org/): A deep learning framework built for speed, expressivity, and modularity
- [Keras](https://keras.io/): A high-level neural network API in Python for Theano and TensorFlow
- [TensorFlow](https://www.tensorflow.org/): An open-source library for machine intelligence from Google
- [Theano](http://deeplearning.net/software/theano/): A Python library for defining, optimizing, and efficiently evaluating mathematical expressions involving multi-dimensional arrays
- CUDA, cuDNN, and the NVIDIA driver
- Many sample Jupyter notebooks
- And more not listed here

## Create your Data Science Virtual Machine for Linux ##
Here are the steps to create an instance of the Data Science Virtual Machine for Linux:
- Navigate to the virtual machine listing on the Azure portal or to http://aka.ms/UbuntuDataScience 

<img src="http://i.imgur.com/nBgI7RS.jpg" width="500">

- Click Create (at the bottom) to bring up the wizard, and search for Microsoft Data Science Virtual Machine (Ubuntu)

<img src="https://docs.microsoft.com/en-us/azure/machine-learning/media/machine-learning-data-science-dsvm-ubuntu-intro/configure-data-science-virtual-machine.png" width="500">

- The following sections provide the inputs for each of the steps in the wizard (enumerated on the right of the preceding figure) used to create the Microsoft Data Science Virtual Machine. Here are the inputs needed to configure each of these steps:
#### Basics ####
**Name:** Name of your data science server you are creating.

**VM disk type:** HDD (we don't yet support SSDs for GPUs)

**User Name**: First account sign-in ID.

**Password**: First account password (we suggest a password for the first VM you create).

**Subscription**: Use your BizSpark or Academic Subscription

**Resource Group**: We suggest creating a new one

**Location**: Select one of the following locations: East US, South Central US, US West 2, North Europe


### Size ###
Select one of the server types that meets your functional requirement and cost constraints. Select **View All** to see more choices of VM sizes. Select an NC-class VM for GPU training. Then select **create**

<img src="http://i.imgur.com/HvPfNuZ.jpg" width="400">


### Settings ###
You can just leave these as is, hit **OK**

### Summary ###
Make sure that these are right, then hit **OK**

### Purchase ###
To start the provisioning, click **Buy**. A link is provided to the terms of the transaction. The VM does not have any additional charges beyond the compute for the server size you chose in the Size step.

### Done ###
The provisioning should take about 5-10 minutes. The status of the provisioning is displayed on the Azure portal. 
You'll be able to SSH into this VM via your preferred method.

## Connecting to the Data Science VM via Jupyter Notebooks##

The easiest way for us to get started is using the built-in Jupyter Notebook 

We can access the Jupyter notebook server from any host. Just type https://<VM DNS name or IP Address>:8000/
**NOTE:** Your username and password will be the same as your VM

<img src="http://i.imgur.com/HTvhnM8.jpg" width="400">

Once you log in, you'll end up at a screen like this:

<img src="http://i.imgur.com/VfM2b0t.jpg" width="400">

### If you're new to Jupyter Notebooks ###
Start with **IntroToJupyterPython.ipynb**

<img src="http://i.imgur.com/4VEfaYl.jpg" width="400">


### If you're ready to start with TensorFlow ###
1. Head to the **tensorflow** folder
2. Open **1_notmnist** and you'll start learning how to classify characters as actual letters (aka solving captchas programmatically)

<img src="http://i.imgur.com/BS6Eb0D.jpg" width="400">

## Connecting to the VM with a graphical desktop ##
If you prefer a graphical interface - The Linux VM is already provisioned with X2Go server and ready to accept client connections. To connect to the Linux VM graphical desktop, do the following on your client:

1. Download and install the X2Go client for your client platform from X2Go. 
2. Run the X2Go client, and select **New Session**. It opens a configuration window with multiple tabs. Enter the following configuration parameters:
	**Host:** The host name or IP of your VM
	**Login:** User name on the Linux VM.
	**SSH Port:** Leave it at 22, the default value.
	**Session Type:** Change the value to XFCE. Currently the Linux VM only supports XFCE desktop.
	**Media** You can turn off sound support and client printing if you don't need to use them.
	**Shared folders:** If you want directories from your client machines mounted on the Linux VM, add the client machine directories that you want to share with the VM on this tab.

After you sign in to the VM by using either the SSH client or XFCE graphical desktop through the X2Go client, you are ready to start using the tools that are installed and configured on the VM. On XFCE, you can see applications menu shortcuts and desktop icons for many of the tools.	
