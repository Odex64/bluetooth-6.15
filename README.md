Since kernel 6.15 Linux has removed the `quirks` struct in favor to `quirk_flags` prior to my knowledge.
This is a fix for bluetooth adapters drivers when running newer kernel versions.

Remove the previous module if already installed:
```
sudo dkms remove btusb/4.3
```

Then run the following commands:
```
git clone https://github.com/Odex64/bluetooth-6.15
sudo dkms add bluetooth-6.15/
sudo dkms install btusb/4.3
```

and reboot.