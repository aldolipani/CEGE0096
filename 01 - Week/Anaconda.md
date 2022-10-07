# Installing Anaconda

This is a guide to installing Anaconda on your personal machine. Further instructions will be provided on how to install the necessary geospatial packages.

In this module, we shall be using the Anaconda distribution of Python. Anaconda also includes a dedicated package management system. The Anaconda distribution and package manager are installed on the UCL desktop.

## Instructions for installing Anaconda

### Download and Install

The standard distribution of Anaconda is bundled together with an extensive library of packages that are commonly used by data scientists. If you already have Anaconda installed on your computer, you do not need to reinstall it again.

Firstly, go to the [Anaconda](https://www.anaconda.com/distribution/) website and choose to download **Python 3.8** for your particular operating system. You will need to decide whether to install Anaconda in your home directory (the **just me** installation) or in a system folder (**all users** installation). For **Windows** users, it is recommended that you install in the system directory.

### Activate Conda

**Windows:** From the Search Box in the LH corner, search for "anaconda prompt". Right-click _**Anaconda Prompt**_ and _**Run as administrator**_.

**Mac/Linux:** Open a terminal window and type the command (note that when you find string beginning with `$`, it means that this is a command to be run on a terminal and that you need to copy the part on the RH side of this sign):

```
$ conda activate
```

You will see the prompt `(base) $`. This means that you are working now within the _base_ environment of Anaconda.

### Create a Geospatial Environment

Anaconda is installed with a single environment called _base_. It is good practice to never use this environment. Therefore we shall create a new environment called _geospatial_.

For instructive purposes we provide two equivalent ways to set this up, manually or using an anaconda configuration file. The first way it is generally used when you start a new project and you are not sure which python modules and tools you will be using. The latter is used when you know already what you need.

#### Manually

We shall set up the environment to run Python 3.8\. If you wanted to create another environment with a different version of Python, change the version number accordingly.

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
(geospatial) $ pip install matplotlib==3.3.1
(geospatial) $ pip install numpy==1.19.1
```

Further instructions shall be provided in due course on how to install the geospatial packages that we will use later in the module.

#### Using a Config file

To create the _geospatial_ environment from a configuration file you first need to make sure to have the `geospatial.yml` configuration file. Then, you can run the command:

```
(base) $ conda env create --file geospatial.yml
```

This file will install all python modules and tools needed for you to work in this module. To check the content of this file you can open it with your favourite text editor or type:

```
$ cat geospatial.yml
```

After the environment has been created, activate the environment.

```
(base) $ conda activate geospatial
```

## Test the Installation

You can launch Anaconda-Navigator by searching among your installed applications. Its application icon should have been pinned to your start bar (Windows) or created in your Applications folder (Mac).

In the Anaconda Navigator window, you should see a menu on the left-hand side of the application. In the **Home** folder, you will see various applications. They will have a button marked _Install_ underneath them. Change the environment at the top of the application window to _geospatial_ and you will see that the button under _Jupyter_ has changed to _Launch_. Click _Launch_ to test it.

After you have tried out _Jupyter_, go back to Anaconda Navigator window and press the _Environments_ on the LH menu. You will see the two environments _base_ and _geospatial_. Click the arrow icon to the right of these environments and you will be given the option to launch in a terminal window.

On the right-hand side of the window you will see a list of environments that have been installed. You can use this pane to install and remove packages. For more control on which repository (referred to as **channel**) to install from, it is safer to use the command prompt.
