# Steps to setup Android SDK with QEMU Support on MAC
## Step 1: Install QEMU
This can be done either via home-brew.
`brew install qemu`
Use ‘sudo’ if necessary for admin privileges.
Install QEMU before you install the Android SDK, in this way, the Android SDK automatically recognises the QEMU libraries and executables stored in the default directory.

You can validate successful QEMU installation by looking for the following folder in the HOMEBREW path.
`/usr/local/Cellar/`

[image:8D49E050-7A1D-4AD2-8DBD-02A4EBBB6F0B-71043-00001F3756598A11/Screenshot 2019-03-25 at 8.55.48 AM.png]

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
[image:0CCB56F6-3691-42CB-8229-8BF7438ECAB8-71043-00001FBB9ED404E7/Screenshot 2019-03-25 at 9.04.26 AM.png]

* Ensure that Intel x86 Emulator Accelerator (HAXM) is installed in the SDK Tools tab of SDK Manager

[image:C0785977-A2C3-4E92-B19E-579345008FDA-71043-00001FDEAFD7F27A/Screenshot 2019-03-25 at 9.07.20 AM.png]

## Step 4: Launch Device
Devices can be setup and launched via the AVD manager. Once the device is launched, you should see QEMU_[devicearchitecture] on the top menu bar

[image:8EA1C709-A3FB-4D46-9DC7-7FE92CF6A9C9-71043-00001FFD92167F40/Screenshot 2019-03-25 at 9.09.32 AM.png]

Then you are good to go! And launch more virtual devices.
