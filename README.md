# Patches for TYPO3 7.6.32

This repository contains patches for TYPO3 7.6.32, which is the latest version from the 7.6 branch.

## Included Patches

1. **Support for MariaDB 10.2** – Apply workaround mentioned in https://forge.typo3.org/issues/83414#note-7 to support MariaDB 10.2.
2. **Fix `<!DOCTYPE html Error` in Editor** – Apply fix from https://github.com/FriendsOfTYPO3/rtehtmlarea/commit/02cc2beeb6069d8726f8120ffd82eb890c2c469e to make rtehtmlarea work in newer Chrome versions. Related GitHub issue: https://github.com/FriendsOfTYPO3/rtehtmlarea/issues/26.

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
patch -p0 < ../typo3-7.6-patches/*.patch
```
