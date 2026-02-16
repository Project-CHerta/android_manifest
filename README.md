# Welcome to CHerta!

## Getting Started

To get started with the CHerta source code, you'll need to be
familiar with [Git and Repo](https://source.android.com/setup/build/downloading).

To initialize your local repository, run:

```bash
repo init --depth=1 -u https://github.com/Project-CHerta/android_manifest.git -b 25h2 --git-lfs
```

Then, sync the repository:

```bash
repo sync --force-sync --no-clone-bundle --no-tags --optimized-fetch --prune
```

## Building the System

Initialize the ROM build environment by sourcing the envsetup.sh script:

```bash
source build/envsetup.sh
```

After cloning the device-specific sources, use breakfast to configure the build for your device:

```bash
breakfast devicecodename
```

Start the compilation:

```bash
m cherta
```

The build system will then generate OTA sideload and fastboot update packages.

## Signing the Build

Simply follow [this](https://github.com/ItsVixano/android_vendor_lineage-priv_keys) guide to sign your builds with your own keys.
