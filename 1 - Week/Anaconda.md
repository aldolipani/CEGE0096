# Installing Anaconda

_This is a guide to installing Anaconda on your personal machine. Further instructions will be provided on how to install the necessary geospatial packages._

In this module, we shall be using the Anaconda distribution of Python. Anaconda also includes a dedicated package management system. The Anaconda distribution and package manager are installed on the UCL desktop.

## Instructions for installing Anaconda

### Download and Install

The standard distribution of Anaconda is bundled together with an extensive library of packages that are commonly used by data scientists. If you already have Anaconda installed on your computer, you do not need to reinstall it again.

Firstly, go to the [Anaconda](https://www.anaconda.com/distribution/) website and choose to download **Python 3.7** for your particular operating system. You will need to decide whether to install Anaconda in your home directory (the **just me** installation) or in a system folder (**all users** installation). For **Windows** users, it is recommended that you install in the system directory.

### Activate Conda

**Windows:** From the Search Box in the LH corner, search for "anaconda prompt". Right-click _**Anaconda Prompt**_ and _**Run as administrator**_.

**Mac/Linux:** Open a terminal window and type after the prompt `$`

```
$ source activate
```

You will see the prompt `(base) >` or on Mac/Linux `(base) $`.

### Create an Environment

Anaconda is installed with a single environment called _base_. It is good practice to never use the base or root environment. Therefore we shall create a new environment called _geospatial_. We shall set up the environment to run Python 3.6\. If you wanted to create another environment with a different version of Python, change the version number accordingly.

Type the following (type Y to proceed when prompted).

```
(base)> conda create -n geospatial python=3.6
```

After the environment has been created, activate the environment.

**Windows:**

```
(base)> activate geospatial
```

**Mac/Linux:**

```
(base)$ conda activate geospatial
```

In future whenever you see the command `activate`, Mac/Linux users should type `source activate`.

### Install the basics

Into this new _geospatial_ environment, we will install the basic packages for using Jupyter notebooks and the Spyder IDE. Type the following (typing 'y' when prompted).

```
(geospatial)> conda install jupyter
```

_This installation will take a bit of time so may want to run them in the background whilst you are engaged on another task._

We shall be using two more packages in the not too distant future (which are also referred briefly in the Slides) and we shall install these as well.

```
(geospatial)>  conda install numpy=1.17.2
(geospatial)>  conda install matplotlib=3.1.1
```

Further instructions shall be provided in due course on how to install the geospatial packages that we will use later in the module.

## Test the installation

You can launch Anaconda-Navigator by searching among your installed applications. Its application icon should have been pinned to your start bar (Windows) or created in your Applications folder (Mac).

In the Anaconda Navigator window, you should see a menu on the left-hand side of the application. In the **Home** folder, you will see various applications. They will have a button marked _Install_ underneath them. Change the environment at the top of the application window to _geospatial_ and you will see that the button under _Jupyter_ has changed to _Launch_. Click _Launch_ to test it.

After you have tried out _Jupyter_, go back to Anaconda Navigator window and press the _Environments_ on the left-hand menu. You will see the two environments _base_ and _geospatial_. Click the arrow icon to the right of these environments and you will be given the option to launch in a terminal window.

On the right-hand side of the window you will see a list of environments that have been installed. You can use this pane to install and remove packages. For more control on which repository (referred to as **channel**) to install from, it is safer to use the command prompt.
