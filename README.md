# chaos-yocto-manifest
Repo manifest to setup Yocto build system for Raspberry Pi

## Setup the Yocto environment

Create a directory for your project.

```
mkdir chaos-raspberrypi && cd chaos-raspberrypi
```

Initialise repo manifest:
```
repo init -u https://github.com/mkilivan/chaos-yocto-manifest \
          -m raspberrypi.xml \
          -b dunfell
```
Fetch layers in manifest:
```
repo sync
```
## Setup build environment
Initialize the build environment:

```
source setup-environment raspberrypi
```

## Building the image
You can now proceed with building an image:
```
bitbake core-image-minimal
```
## Using the build output
After a successful build, the images and build artifacts are:

## Credit
Inspired by [Mender.io](https://mender.io/)