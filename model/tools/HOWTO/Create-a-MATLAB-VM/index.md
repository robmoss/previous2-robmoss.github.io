---
title: 'HOW-TO: Create a MATLAB Virtual Machine'
is_post: true
---


# Creating a VM

Create a new NeCTAR VM using one of the large templates (e.g., `m1.xxlarge`, which comprises 16 VCPUs, 10 GB root disk, 480 GB ephemeral disk, and 64 GB RAM) and the `NeCTAR Debian 9 (Stretch) amd64` image.

Give it a descriptive name (e.g., `username-matlab-vm`) and make sure to select a key pair (under &ldquo;Access & Security&rdquo;).

# Installing required packages

Connect to the VM, noting that the default user account is `debian`:

```sh
ssh debian@144.6.224.174
```

Once you&rsquo;ve logged into the VM, make sure that the system packages are all up to date:

```sh
sudo apt update
sudo apt upgrade
```

Restart the VM so that updated kernel images and other system services are reloaded (this will disconnect you from the VM):

```sh
sudo shutdown -r now
```

Install required packages:

```sh
sudo apt install gcc g++ gfortran xfce4
```

Note that `xfce4` pulls in `Xorg` dependencies; MathWorks [do not identify](https://au.mathworks.com/matlabcentral/answers/229857-why-do-i-see-preparing-installation-files-installing-finished-in-the-terminal-window-wh) a precise list of required `Xorg` packages:

> Even if you intend to run MATLAB only in non-graphical mode, MATLAB requires some X11 libraries to run. Unfortunately, we are not able to specify the X11 requirements down to the exact set of packages required because different distributions may package the libraries differently. MATLAB will work out of the box on desktop installations of any supported distribution.

You could also install OpenJDK for Java support, but the MATLAB installer bundles its own JVM and it isn&rsquo;t clear whether it will use an installed JVM instead.

# Installing MATLAB

1.  Create a MathWorks account, if you don&rsquo;t already have one. Make sure that you use your institutional email address (e.g., `username@unimelb.edu.au`).
2.  Download the &ldquo;Linux (64-bit)&rdquo; installer from the [MathWorks website](https://au.mathworks.com/downloads/web_downloads/). This will be a single archive named, e.g., `matlab_R2018a_glnxa64.zip` for MATLAB R2018a.
3.  Transfer the installer to the virtual machine (**important:** note the trailing colon after the virtual machine&rsquo;s IP address):
    ```sh
    scp matlab_R2018a_glnxa64.zip 144.6.224.174:
    ```
4.  Connect to the VM, making sure that X11 forwarding is **enabled**, and launch the installer:
    ```sh
    ssh -XC debian@144.6.224.174
    mkdir matlab-installer
    mv matlab_R2018a_glnxa64.zip matlab-installer
    cd matlab-installer
    unzip matlab_R2018a_glnxa64.zip
    sudo su
    xauth merge /home/debian/.Xauthority
    ./install -verbose
    ```
    The graphical installer should appear on your desktop.
5.  During the installation process, associate your MathWorks account with the University of Melbourne&rsquo;s [site license](https://github.com/resbaz/lessons/blob/master/matlab/unimelb_matlab_install.md):
    -   Staff: `24759-36418-71647-13382-89362`
    -   Students: `18098-22076-81253-90866-03229`
6.  Install MATLAB to the ephemeral disk (i.e., somewhere on `/mnt`, such as `/mnt/MATLAB/R2018a`).
7.  Install the following toolboxes **at a minimum**:
    -   The Parallel Computing Toolbox (provides `parpool`).
    -   The Statistics and Machine Learning Toolbox (provides `betainv`, etc).
    -   The Neural Network Toolbox (provides `combvec`).

    These toolboxes are sufficient for using the LHS framework and running the pandemic influenza simulation model, but you may require additional toolboxes depending on your project.
8.  Once the installation is completed, add symbolic links so that MATLAB is found in your $PATH:
    ```sh
    sudo ln -s /mnt/MATLAB/R2018a/bin/matlab /usr/local/bin/matlab
    ```

# Launching MATLAB

To use the GUI:

```sh
ssh -XC debian@144.6.224.174
matlab &
```

To use the text interface:

```sh
ssh debian@144.6.224.174
matlab -nodisplay
```

Note that in order to use the Parallel Computing Toolbox (i.e., `parpool` and `parfor`) the Java Virtual Machine (JVM) [must be enabled](https://au.mathworks.com/matlabcentral/answers/230285-parpool-r2014a-fails-on-linux), so do not start MATLAB with the `-nojvm` command-line option.

# Other materials

See the [Virtual Wranglers](https://espaces.edu.au/vwrangler) community knowledge base, intended for people managing Nectar virtual machines; in particular, see their [Nectar HOW-TOs](https://espaces.edu.au/vwrangler/nectar-topics/nectar-how-tos) and their [Installing MATLAB](https://espaces.edu.au/vwrangler/nectar-topics/nectar-how-tos/installing-matlab-on-a-nectar-instance) guide.
