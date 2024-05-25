# Upgrading from a 10 year old Macbook Air to Macbook Air M3

## Background

Updating from old Macbook to Macbook M3 2023.



## Overview of Project

### Purpose

Quick and fastest transfer method while maintaining BAU. Most importantly, all the files must be transfered and codes & scripts must work without any downtime.

## Files transfer

Firstly I used Migration Assistant to transfer all files from old Macbook to new Macbook.[Instructions here](https://support.apple.com/en-ca/102613)

This is done through regular wi-fi overnight and completed in 4 hours. Note: When this is happening, both Macbooks are locked and cannot be use.

## Coding Environment Updates

MOST IMPORTANT!
Update Xcode using App Store first.

Uninstall homebrew:
```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/uninstall.sh)"
```

Install homebrew (follow the instructions on the screen):
```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

Rosetta 2 is a dynamic binary translator developed by Apple, designed to enable Apple Silicon Macs (which use ARM-based processors such as the M1 and M2 series) to run software that was originally built for Intel-based Macs (which use x86-64 architecture):
```
/usr/sbin/softwareupdate --install-rosetta --agree-to-license
```

Check brew:
```
brew doctor
brew config
```
