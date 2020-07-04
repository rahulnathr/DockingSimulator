## Instruction for creating a Development Environment for Testing

##### This instruction is based on a Shareable environment setup using  Vagrant. 

##### Prerequisites for Development 
1. Vagrant 
    - Install through [here](https://www.vagrantup.com/downloads)
2. VirtualBox (its a virtual environment provider for Vagrant and very much dependent for our GUI Visuals)
    - Install through [here](https://www.virtualbox.org/wiki/Downloads)


#### After Installation procedures
1. Check for correct installation of version in Command Prompt in Windows(tested there;should be fine in other OS) by
```
vagrant --version
```

2. Clone this repository

3. Add the files from the email to the repository(that is add all the python codes)
    - This process is much easier if using the Bitbucker repo where even the codes is hosted.So a single cloning would do the job.

4. Navigate to the repository folder and initialise the vagrant by
```
vagrant up
```

5. This would 
    - install an Ubuntu 18.04 version on Virtualbox
    - Create a Desktop Environment for the Linux(essential in our case)
    - Install all used dependencies for the current python code.Numpy,matplotlib etc.
    - Create a login screen for the Linux :
        ![Login Screen](https://github.com/rahulnathr/DockingSimulator/blob/master/loginscreen.JPG)
    

6. In the login screen of the Linux in Virtualbox
    - Navigate to Vagrant User
    - Use password as ```vagrant ```
    
7. In the Linux desktop, open Terminal
    - Navigate to the synced_folder(folder from host and vagrant) using ``` cd /vagrant/ ```
    - You should be able to see our python files and Csv files if you have copied the files as per step 3.
    - Run application using ```python3 controller.py```
    - Add the ship information using load button on GUI and select "shipinfo.csv".
    - Can play around the final GUI using the sliders.
8. All code is based on python 3.6.9
