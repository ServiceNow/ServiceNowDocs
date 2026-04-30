---
title: Install the ServiceNow CLI on Mac
description: Install ServiceNow CLI on a Mac OS using the installer.
locale: en-US
release: xanadu
product: ServiceNow CLI
classification: servicenow-cli
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Install the ServiceNow CLI, ServiceNow CLI, Building low-code applications, Developing your application, Building applications]
---

# Install the ServiceNow CLI on Mac

Install ServiceNow CLI on a Mac OS using the installer.

## Before you begin

You must have an Apple-supported version of 64-bit Mac OS.

Role required: admin

## Procedure

1.  In your browser, [download the installer bundle from the ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/application/9085854adbb52810122156a8dc961910/1.1.0?referer=%2Fstore%2Fsearch%3Flistingtype%3Dallintegrations%25253Bancillary_app%25253Bcertified_apps%25253Bcontent%25253Bindustry_solution%25253Boem%25253Butility%25253Btemplate%26q%3Dcli%2520bundle&sl=sh).

2.  Extract the OS-specific installers.

3.  Open the `snc-1.0.0-osx-installer` file.

4.  Follow the on-screen instructions.

    1.  When prompted, ensure the **Add to PATH** option is selected.

        This option requires root account access.

5.  To verify that the installation succeeded, use the following commands.

    ```
    $ which snc
    
    /usr/local/bin/snc
    ```

    ```
    $ snc version
    
    {
     "extensions": {},
     "snc": "1.0.0"
    }
    ```


**Parent Topic:**[Install the ServiceNow CLI](download-cli.md)

