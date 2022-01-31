# pi-topOS Apt Source: Archive Keyring and Automatic Apt Source Configuration

This repository contains the GnuPG archive keys of the pi-topOS archive, used for signing the releases of pi-topOS apt software repository archives.

It also provides packages as a quick way of adding pi-topOS as a source (`pi-top-os{,-testing,-unstable,-experimental}-apt-source`).

For example, to add pi-topOS as a fully configured source to Raspberry Pi OS:

```
apt update
apt install -y pi-top-os-apt-source
apt update
```

Optionally, you can now install much of pi-topOS:
```
apt install pt-os
```

Note: the apt cache needs updating after the package has been installed, as the packages available in the pi-topOS apt repositories are not yet known.
