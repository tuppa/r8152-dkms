# r8152-dkms
r8152 dkms.conf for Ubuntu 20.04, based on [amrik/r8152-dkms](https://www.realtek.com/en/component/zoo/category/network-interface-controllers-10-100-1000m-gigabit-ethernet-usb-3-0-software).


# Instructions
* Download the Linux driver from [here](https://www.realtek.com/en/component/zoo/category/network-interface-controllers-10-100-1000m-gigabit-ethernet-usb-3-0-software)
* Extract the files from the downloaded tarball into /usr/src/r8152-<version>
* Copy the dkms.conf into the directory above, make sure the version in the dkms.conf file matches the version downloaded
* Run
```
sudo dkms add -m r8152 -v $VERSION
sudo dkms build -m r8152 -v $VERSION
sudo dkms install -m r8152 -v $VERSIOn
```
