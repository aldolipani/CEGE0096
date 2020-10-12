# Using a Virtual Machine

A Virtual Machine (VM) is a software that creates a virtual environment that emulates the behaviour of 
a physical machine. Here you can install various Operative Systems (OS) like Windows and Linux, and you can 
configure them with the pre-installed software and data you need.
In other words, it is like having a PC inside your PC, and this first PC can be easily copied and run in other PC.
For this module I have compiled a VM that contains all the software and data you need to use in order to successfully pass this 
module. 

You should use this VM if:
1) you had issues following my instructions in installing software or Python 
modules in your own PC. This may happen due to previous installations or conflicting versions of Python modules; 
2) you want to test that your software runs in other machines. This will help you check if your assignment will run 
when tested in my PC;
3) you want to try out a Linux environment.

## VirtualBox Installation

VirtualBox is an open-source software that is able to execute VMs. To run my VM 
you need to download and install Virtual Box 6.0.24 following this link 
[www.virtualbox.org/wiki/Download_Old_Builds_6_0](https://www.virtualbox.org/wiki/Download_Old_Builds_6_0). 
In this page you should select the installation version for your current OS.

## The VM Image
 
The VM image is based on a Linux OS called [Zorin OS](https://zorinos.com/). 
I picked this because version of Linux because it looks a lot like Windows, and this may make your migration to this new 
OS easier.
You need to download and unzip the VM image you find at this link 
[Geospatial Programming VM.zip](https://liveuclac-my.sharepoint.com/:u:/g/personal/ucaclip_ucl_ac_uk/EYrhcrXc2d1DvPvMXFz-ZXYBRocUxiwDdNyq2Mvy6jiUbQ?e=kjnbrC). 
You will need to be logged in using your UCL account to be able to download the VM. 
Note that this VM is 9.3 GiB when compressed and around 20 GiB when uncompressed. Please make sure to have enough disk 
space before starting working with it.

Place the 3 files in a safe and permanent location in your PC and add this VM to VirtualBox. Then you can start the VM. 
Username and password are `student` and `student`. 
In the VM you will find the material of the first week. Use `$ git pull` in the CEGE0096 folder to update this 
folder with the material of the last week.