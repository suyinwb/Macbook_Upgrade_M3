# Upgrading from a 10 year old Macbook Air Intel Core i7 (2013) to Macbook Air M3 (2024)

## Background

Updating from old Macbook Intel Core i7 to Macbook M3 2023.



## Overview of Project

### Purpose

Quick and fastest transfer method while maintaining BAU. Most importantly, all the files must be transfered and codes & scripts must work without any downtime.

## Files transfer

Firstly I used Migration Assistant to transfer all files from old Macbook to new Macbook.
[Instructions here](https://support.apple.com/en-ca/102613)

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

Check brew and update any packages that are deprecated:
```
brew doctor
brew config
```

Install the necessary packages:
```
brew install python

brew install pipx
pipx ensure path

brew install jupyter
```


REPEAT FOR ALL CONDA ENVIRONMENTS:

==start==

```
conda activate <env>

conda activate /Users/vuvie/opt/anaconda3/envs/mlenv

pip list --outdated --format=freeze | grep -v '^\-e' | cut -d = -f 1 | xargs -n1 pip install -U

conda activate /Users/vuvie/opt/anaconda3/envs/PythonData

pip list --outdated --format=freeze | grep -v '^\-e' | cut -d = -f 1 | xargs -n1 pip install -U
```

==end==

Install chrome driver:
```
brew install chrome driver
```

I want to uninstall anaconda-navigator as I had it in the old Macbook but I don't care about it so I don't need it in my new M3 environment:
```
conda install anaconda-navigator
conda remove anaconda-navigator
```

Using anaconda-clean to clean up the environment. I said yes to all the cleanup the prompts asked:
```
conda install anaconda-clean
anaconda-clean
```

NOTE: I don't mind anaconda as jupyter will require a kernel to run after all but I really didn't want the anaconda-navigator. 
