# Steps to setup Android SDK with QEMU Support on MAC
## Step 1: Install QEMU
This can be done either via home-brew.
`brew install qemu`
Use ‘sudo’ if necessary for admin privileges.
Install QEMU before you install the Android SDK, in this way, the Android SDK automatically recognises the QEMU libraries and executables stored in the default directory.

You can validate successful QEMU installation by looking for the following folder in the HOMEBREW path.
`/usr/local/Cellar/`

![Image of QEMU Installation Path](https://github.com/reubenrajan/howto/blob/master/img/QEMU_Path.png)

## Step 2: Append QEMU path in the environment variables
QEMU path is not set on installation. Hence it has to be manually done. I prefer a simple text edit on the “bash profile” file in the user directory. 

The “bash profile” file is usually hidden. Press “CMD+Shift+.” to view hidden files.

Open the bash profile file with any text edit document, I use “vscode”.

Add the path variable like this.
`export PATH="/usr/local/Cellar/qemu/3.1.0_1/bin:$PATH"`

And you should be good to go

## Step 3: Install Android SDK and necessary virtualisation components:
Please ensure you download the following components during your installation:
* x86 and 64 images for the devices you wish to install (navigate to SDK manager in Tool Configuration)

![Image of Android SDK Images](https://github.com/reubenrajan/howto/blob/master/img/QEMU_AndroidSDK_Images.png)

* Ensure that Intel x86 Emulator Accelerator (HAXM) is installed in the SDK Tools tab of SDK Manager

![Image of Android HAXM Settings](https://github.com/reubenrajan/howto/blob/master/img/QEMU_AndroidSDK_HAXM.png)

## Step 4: Launch Device
Devices can be setup and launched via the AVD manager. Once the device is launched, you should see QEMU_[devicearchitecture] on the top menu bar

![Image of QEMU Device](https://github.com/reubenrajan/howto/blob/master/img/QEMU_Device.png) 

Then you are good to go! And launch more virtual devices.
