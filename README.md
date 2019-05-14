# [fedora-secure-boot](https://github.com/fnkr/fedora-secure-boot)

The import process will ask for a password twice.
You can choose any password but you will need to remember it until the import has been completed.

```sh
# Clone repository
git clone https://github.com/fnkr/fedora-secure-boot.git secure-boot
cd secure-boot

# Generate MOK and start import
sudo ./install-mok YOUR_NAME

# Sign kernel modules with the newly generated MOK
# This is an example which will sign and load VirtualBox kernel modules:
sudo ./sign-and-load-vbox-modules

# Reboot to finish the MOK import
sudo reboot
```

To finish the import a reboot is required - UEFI will ask for the password at boot time.
Once the import has finished you can sign and load kernel modules at runtime.
