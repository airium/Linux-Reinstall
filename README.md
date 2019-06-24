# Linux-Reinstall

This repo includes modified scripts from <https://moeclub.org>, with credit to Vicer.

## template-YYMMDD.sh

The original scripts. See <https://moeclub.org/2018/04/03/603/> for detailed usage.

## install.sh

The modified script, mainly differing in:

1. use `en_US.UTF-8` instead of `en_US` for debian/ubuntu.
2. use `ifupdown` instead of `netplan` for newer ubuntu releases.
3. use UEFI/GPT instead, for single partition of 2TB or larger.
4. use boot-root-noswap partition style instead of built-in atomic.

## install-raid0.sh

Same flavor as `install.sh`, but offer to install software RAID-0.

Currently:

1. The machine must have `/dev/sda` and `/dev/sdb` of **identical** size.
2. RAID1 is used for `/boot` and RAID0 is used for `/`.
3. SWAP is disabled. You can enable it by `swapon`.

   **Installing Debian 8 on ikoula machines will fail.**
