# Upgrading from a 10 year old Macbook Air to Macbook Air M3

## Background

Updating from old Macbook to Macbook M3 2023.


## Overview of Project

### Purpose

Quick and fastest transfer method while maintaining BAU. Most importantly, all the files must be transfered and codes & scripts must work without any downtime.


```
# =========================================================================
# Continous Scroll To The End Of Page
# =========================================================================

time.sleep(30)

SCROLL_PAUSE_TIME = 30

# Get scroll height
last_height = driver.execute_script("return document.body.scrollHeight")

while True:
    # Scroll down to bottom
    driver.execute_script("window.scrollTo(0, document.body.scrollHeight);")

    # Wait to load page
    time.sleep(SCROLL_PAUSE_TIME)

    # Calculate new scroll height and compare with last scroll height
    new_height = driver.execute_script("return document.body.scrollHeight")
    if new_height == last_height:
        break
    last_height = new_height
```
