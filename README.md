# Linux Compiler System
## Section 1
Setting up a Linux WSL environment with GCC.

This tutorial guide provides step-by-step instructions for setting up a Linux environment with GCC on Windows 10/11 using Windows Subsystem for Linux (WSL).

<p align="center">
  <img src="https://user-images.githubusercontent.com/95499848/226253104-4d6df8a5-99b6-4a8a-b66b-d9f9f00299a3.jpg" width="600" height="400" align="centre">
</p>

1. Prerequisites:
   You will need the following:
   - A Windows 10 machine.
   - Linux Distro : Ubuntu 22.04 or 18.04
   - Windows Subsystem for Linux (WSL) installed.
   - Basic knowledge of the Linux command-line interface.

2. Brief overview of what's covered:
   - Installing a Linux Distribution on WSL.
   - Updating and Upgrading the Linux Distribution.
   - Installing GCC on the Linux Distribution.
   - Testing the GCC Installation.

## Section 2
Setting up a Linux environment using VMWare.

# Linux-Environment-VMWare
![440b912ad466ecde8ff70a263b91d63a](https://user-images.githubusercontent.com/95499848/230808702-d22e67d4-b942-4159-8864-e00037716253.jpg)

1. Download & Install VMWare.
   - VMWare
     https://customerconnect.vmware.com/en/downloads/details?downloadGroup=WKST-PLAYER-1701&productId=1377&rPId=100675
   - Recommended Setup:

     | Minimum | Recommended |
     |----------|----------|
     | 2GB Memory | 4GB Memory |
     | 20GB Default Storage | 50GB Storage |
   
   - Ubuntu Images
     https://ubuntu.com/download/desktop
  
2. Prerequisite update & install package:
   
   ``` 
   sudo apt-get update && sudo apt-get upgrade
   sudo apt install gcc-arm-none-eabi
   sudo apt install git
   ```
   
3. Kernel build & configuration:
   
   ``` 
   sudo apt install libncurses-dev 	
   sudo apt install flex bison openssl libssl-dev dkms 
   sudo apt install libelf-dev libudev-dev libpci-dev libiberty-dev 
   sudo apt install autoconf 
   ```
   
4

4. Optional:
   
   ```
   sudo apt install vim python3 python-pip
   ```
   
4. Setup Share Directory.
   - Enable shared file in VMWare.
   ![Untitled](https://user-images.githubusercontent.com/95499848/230808056-2bd3292d-97e1-4d21-a20c-527850545f08.png)
   - Check added shared file.
    
      ``` 
       wmware-hgfsclient
      ```
  
5. Configure File System Table and Mount.
   
   ``` 
   sudo vim /etc/fstab
   
   vmhgfs-fuse           /mnt/hgfs     fuse      /defaults,allow_other    0   0
   ```
   ``` 
   mkdir /mnt/hgfs
   mount -a
   ```

## Section 3
Compiling/Run Make file in Linux environment.

1. Example of output of make file for both project folders.

<p align="center">
  <img src="https://user-images.githubusercontent.com/95499848/226252351-676b01e4-5a63-4d89-a144-9930d461c3ef.png" width="880" height="300" align="centre">
  <img src="https://user-images.githubusercontent.com/95499848/226252371-34a34c59-48b3-4cde-af19-d2b63cf09f3f.png" width="880" height="300" align="centre">
</p>


2. Click Download button to start. The progress bar will show the transmit progress of each image. You can also get the message of operation successfully or errors from the log window.

<p align="center">
  <img src="https://user-images.githubusercontent.com/95499848/226252889-1bdd0cce-da77-4dde-8254-2b1b6aefc256.png" width="500" height="600" align="centre">
</p>

## Section 4
Disclaimer.

1. Contributing:
    - If you would like to contribute to this tutorial guide, you can submit a pull request with your changes. Please make sure that your changes are relevant and useful.
   

2. Disclaimer:
   - This tutorial guide is provided "as is" and without warranties of any kind, either express or implied. The author and contributors will not be liable for any damages or injuries arising from the use of this guide.
