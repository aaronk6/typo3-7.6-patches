# Patches for TYPO3 7.6.32

This repository contains patches for TYPO3 7.6.32, which is the latest version from the 7.6 branch.

## Included Patches

1. **Support for MariaDB 10.2** – Apply workaround mentioned in https://forge.typo3.org/issues/83414#note-7 to support MariaDB 10.2.
2. **Fix RTE not working in Chrome 91** – Apply fix suggested in https://github.com/FriendsOfTYPO3/rtehtmlarea/issues/46#issuecomment-860512586 to make rtehtmlarea work in newer Chrome versions.

## Instructions

Download and extract TYPO3 7.6.32:

```
wget --content-disposition get.typo3.org/7.6.32/tar.gz
tar xfz typo3_src-7.6.32.tar.gz
```

Download and apply patches:

```
git clone https://github.com/aaronk6/typo3-7.6-patches.git
cd typo3_src-7.6.32
patch -p0 < ../typo3-7.6-patches/typo3-mariadb10_2.patch
patch -p0 < ../typo3-7.6-patches/typo3-rtehtmlarea_chrome_fix.patch
```
