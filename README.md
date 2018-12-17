# Linux-Reinstall

This repo includes modified script from moeclub.org, with credit to Vicer.

## `install.sh`

The original script from Vicer.

Please refer to <https://moeclub.org/2018/04/03/603> for detailed usage.

## `install-raid0.sh`

Modified script to configure raid0 on a dual disk machine.

Note:

1. The machine must have `/dev/sda` and `/dev/sdb` of **identical** size.
2. RAID1 is used for `/boot` and RAID0 is used for `/`.
3. SWAP is disabled. You can enable it by `swapon`.

**The dd functionality to install Windows is temporarily not working.**
