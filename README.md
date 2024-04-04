# pi-topOS Apt Source: Archive Keyring and Automatic Apt Source Configuration

This repository provides packages as a quick way of adding pi-topOS apt repositories to a machine (`pi-top-os{,-testing,-unstable,-experimental}-apt-source`) so that it can easily install pi-top software.

It also contains the GnuPG archive keys of the pi-topOS archive, used for signing the releases of pi-topOS apt software repository archives.

# Installation

## Via apt in Raspberry Pi OS

The packages this repository generates can be found in Raspberry Pi OS apt repositories, so you can add the main pi-topOS source by running:

```
apt update
apt install -y pi-top-os-apt-source
apt update
```

More information about using pi-top hardware with Raspberry Pi-OS can be found [here](https://knowledgebase.pi-top.com/knowledge/pi-top-and-raspberry-pi-os).


## Manually

You can also manually add the source you want by cloning this repository, copying the required keys and running the install script.

```
# Clone repository
git clone https://github.com/pi-top/pi-topOS-Apt-Source.git
cd pi-topOS-Apt-Source
# Copy keys
sudo cp keys/* /usr/share/keyrings/
# Install source by executing the 'pi-top-os-apt-source-manager' script with the repository name
sudo usr/lib/pi-top-os-apt-installer/pi-top-apt-source-manager install pi-top-os
# Update apt
sudo apt update
```

# After Installing

By this point, you can install all the software from pi-topOS into your device.

## Basic hardware support

To provide hardware support for your device (e.g.: hub communication, working miniscreen, ...) install `pt-device-support`, which will take care of installing all the packages your pi-top needs to work properly:

```
sudo apt install -y pt-device-support
```

## pi-topOS Software

To install all the software from pi-topOS into your device, install the `pt-os` package. This will install everything your pi-top needs to work properly plus other software and features that exist in pi-topOS, such as the web portal.

```
sudo apt install -y pt-os
```
