# pi-topOS Archive Keyring

This repository contains the GnuPG archive keys of the pi-topOS archive, used for signing the releases of pi-topOS apt software repository archives.

## How To Add pi-topOS As A Source

* Install this package
* Add to sources

### Example (RPi OS)

```
apt update
apt install -y pi-top-os-archive-keyring
echo "deb [signed-by=/usr/share/keyrings/pi-top-os-archive-keyring.gpg] https://pkg.pi-top.com/os-release/debian/ bullseye main" > /etc/apt/sources.list.d/pi-top.list
apt update
```
