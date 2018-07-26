---
title: Install TensorFlow on Ubuntu
layout: page
comments: true
social-share: true
show-avatar: true
---

tensorflow-gpu —Current release with GPU support
There are a few options to install TensorFlow on your machine:

* Use pip in virtual environment (recommended).
* Use pip in your system environment.
* Configure a docker container.
* Use pip in Anaconda.
* Install tensorflow from source.

Here i will discuss the first option:

**1.) Use pip in virtual environment**
				The Virtualenv tool creates virtual Python environments that are isolated from other Python development on the same machine. In this scenario, you install TensorFlow and its dependencies within a virtual environment that is available when activated. Virtualenv provides a reliable way to install and run TensorFlow while avoiding conflicts with the rest of the system.

**1. Install Python, pip, and virtualenv.**
		On Ubuntu, Python is automatically installed and pip is usually installed. Confirm the python and pip versions:
		
$ python -V        # or: python3 -V   
$  pip -V                # or: pip3 -V	 

To install these packages on Ubuntu:

$ sudo apt-get install python-pip python-dev python-virtualenv        # for Python 2.7

$ sudo apt-get install python3-pip python3-dev python-virtualenv  # for Python 3.n
	 
We recommend using pip version 8.1 or higher. If using a release before version 8.1, upgrade pip:

$ sudo pip install -U pip

If not using Ubuntu and setuptools is installed, use easy_install to install pip:

$ easy_install -U pip

**2. Create a directory for the virtual environment and choose a Python interpreter.**

$ mkdir ~/tensorflo         # somewhere to work out of

$ cd ~/tensorflow

$ virtualenv --system-site-packages venv                            # Use python default (Python 2.7)

$ virtualenv --system-site-packages -p python3 venv                        # Use Python 3.n

**3. Activate the Virtualenv environment.**

Use one of these shell-specific commands to activate the virtual environment:

$ source ~/tensorflow/venv/bin/activate

$ source ~/tensorflow/venv/bin/activate.csh

$ . ~/tensorflow/venv/bin/activate.fish

**4. Upgrade pip in the virtual environment.**

Within the active virtual environment, upgrade pip:

(venv)$ pip install -U pip

You can install other Python packages within the virtual environment without affecting packages outside the virtualenv.

**5. Install TensorFlow in the virtual environment.**

Choose one of the available TensorFlow packages for installation:

* tensorflow —Current release for CPU
* tensorflow-gpu —Current release with GPU support
* tf-nightly —Nightly build for CPU
*  tf-nightly-gpu —Nightly build with GPU support

Within an active Virtualenv environment, use pip to install the package:

 $ pip install -U tensorflow
 
 Success: TensorFlow is now installed.