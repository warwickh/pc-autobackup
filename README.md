# PC AutoBackup for Linux and OS X for Samsung digital cameras #

This project has been forked from https://github.com/n-i-x/pc-autobackup and updated for python3. Python2 code is now in another branch.

I am currently running this as a docker container and I have included the Dockerfile and docker compose files.

If you'd like to donate to the development of PC AutoBackup use the following link:

---


# Getting Started #

## Requirements ##
  * [Python 3+](http://python.org/download)
  * [Twisted](http://twistedmatrix.com/trac/wiki/Downloads)

## Configuring your camera ##
> ### If your camera has already been setup with PC AutoBackup for Windows ###
    * Mount your camera's SD card
    * pc_autobackup.py --import_camera_config=/path/to/camera
    * Uninstall PC AutoBackup on Windows **_(failure to do so will prevent this server from working)_**
> ### If you have never setup PC AutoBackup before ###
    * Mount your camera's SD card
    * pc_autobackup.py --create_camera_config=/path/to/camera

## Starting the server ##
  * pc_autobackup.py

> See _pc_autobackup.py --help_ for more options

## **Tested with the following cameras:** ##

  * DV300F
  * NX1000
  * WB150F
  * WB350F
  * ST200F
  * NX2000
  * NX300
  * EX2F
  * Does it work with your camera? Send me a pull request editing this README.

## **Tested on the following OS:** ##

  * Arch 64-bit
  * Ubuntu 12.04 (precise) 32/64-bit
  * Ubuntu 16.04 (xenial) 64-bit
  * Ubuntu 22.04 (jammy)
  * Mac OS X 10.8.2 (Mountain Lion)

## **Tested on the following Python versions:** ##

  * Python 2.7.2
  * Python 2.7.3
  * Python 2.7.11
  * Python 2.7.12
  * Python 3.10.12
---

**_This software is NOT created or supported by Samsung_**

**_Samsung is a registered trademark of Samsung Electronics Co., Ltd._**
