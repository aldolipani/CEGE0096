# Installing Anaconda for Apple silicon (M1 and M2)

This is a guide to installing Anaconda on your Macbook that has M1 or M2 Chip. 
Further instructions will be provided on how to install the necessary geospatial packages.

In this module, we shall be using the Anaconda distribution of Python. 
Anaconda also includes a dedicated package management system. 
The Anaconda distribution and package manager are installed on the UCL desktop.

## Why there is a special instruction for M1?
If you follow the instruction for non-M1 chip, you may suffer from the Chip difference due to some packages that’s only built for Intel chips. 
For libraries written in pure Python, there should be no issue running those on any architecture/chips. 
However, if the library uses or depends on other libraries that are written in C/C++, it needs to be compiled specifically for M1 chips.
One way to figure out this problem is to install a binary translator (Rosetta) that translates x86_64 executions to that of arm64.
However, if you choose this way, you will run all the executions on emulation which largely degrades the performance.
To avoid the problem, you need to download a specific Anaconda distribution for arm64 with specific versions of libraries.

## Instructions for installing Anaconda

### Download and Install

The standard distribution of Anaconda is bundled together with an extensive library of packages that are commonly used by data scientists. 
There are two ways to install Conda for arm64.
If you already have Anaconda installed on your computer, you do not need to reinstall it again.

#### 1. Anaconda distribution

Go to the [Anaconda](https://www.anaconda.com/distribution/) website and click **Get Additional Installers**.
Then choose to download the **64-Bit (M1) Graphical Installer**.

#### 2. Miniforge3

Go to the [Miniforge](https://github.com/conda-forge/miniforge) GitHub repository.
Check the README section to download the **Miniforge3-MacOSX-arm64**.
This will download a shell script (normally in a `Downloads` directory).

To run the script, run the following command:
```
$ bash Miniforge3-MacOSX-arm64.sh
```

### Activate Conda

Open a terminal window and type the command (note that when you find string beginning with `$`, it means that this is a command to be run on a terminal and that you need to copy the part on the RH side of this sign):

```
$ conda activate
```

You will see the prompt `(base) $`. This means that you are working now within the _base_ environment of Anaconda.

### Create a Geospatial Environment

Anaconda is installed with a single environment called _base_. It is good practice to never use this environment. Therefore we shall create a new environment called _geospatial_.

For instructive purposes we provide two equivalent ways to set this up, manually or using an anaconda configuration file. The first way it is generally used when you start a new project and you are not sure which python modules and tools you will be using. The latter is used when you know already what you need.

#### Manually (not recommended for M1)
_Unlike the instruction for intel-chips, manual way is not recommended as you will need a very specific versions of packages to avoid any possible errors._

We shall set up the environment to run Python 3.8. If you wanted to create another environment with a different version of Python, change the version number accordingly.

Type the following (type Y to proceed when prompted).

```
(base) $ conda create -n geospatial python=3.8
```

After the environment has been created, activate the environment.

```
(base) $ conda activate geospatial
```

You now have created a new environment in which you can install modules and tools as needed.

Into this new _geospatial_ environment, we will install the basic modules for using Jupyter notebooks. Type the following (typing 'y' when prompted).

```
(geospatial) $ pip install jupyter==1.0.0
```

This installation will take a bit of time so may want to run them in the background whilst you are engaged on another task.

We shall be using two more packages in the not too distant future (which are also referred briefly in the Slides) and we shall install these as well.

```
(geospatial) $ pip install matplotlib==3.6.0
(geospatial) $ pip install numpy==1.23.3
```

Further instructions shall be provided in due course on how to install the geospatial packages that we will use later in the module.

#### Using a Config file

To create the _geospatial_ environment from a configuration file you first need to make sure to have the `geospatial.m1.yml` configuration file. Then, you can run the command:

```
(base) $ conda env create --file geospatial.m1.yml
```

This file will install all python modules and tools needed for you to work in this module. To check the content of this file you can open it with your favourite text editor or type:

```
$ cat geospatial.m1.yml
```

After the environment has been created, activate the environment.

```
(base) $ conda activate geospatial
```

## Test the Installation

Unlike the Anaconda for intel-chip, Anaconda for M1-chip does not support Anaconda-Navigator yet.

To use jupyter notebook, you should type `jupyter notebook` in the command line.