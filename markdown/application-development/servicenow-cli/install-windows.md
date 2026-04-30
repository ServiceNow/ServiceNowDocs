---
title: Install the ServiceNow CLI on Windows
description: Install ServiceNow CLI on a Windows OS using the installer.
locale: en-US
release: xanadu
product: ServiceNow CLI
classification: servicenow-cli
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Install the ServiceNow CLI, ServiceNow CLI, Building low-code applications, Developing your application, Building applications]
---

# Install the ServiceNow CLI on Windows

Install ServiceNow CLI on a Windows OS using the installer.

## Before you begin

You must have a 64-bit version of Windows 10 or later.

Role required: admin

## Procedure

1.  In your browser, [download the installer bundle from the ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/application/9085854adbb52810122156a8dc961910).

2.  Extract the OS-specific installers.

3.  Open the `snc-1.0.0-windows-x64-installer.exe` file.

4.  Follow the on-screen instructions.

    By default, the CLI installs to `C:\Program Files\ServiceNow CLI`.

5.  To confirm the installation, check the version in the command line using the following command.

    ```
    C:\>snc version
    
    {
     "extensions": {},
     "snc": "1.0.0"
    }
    ```

    If Windows is unable to find the program, close and reopen the command prompt window to refresh the path.


**Parent Topic:**[Install the ServiceNow CLI](download-cli.md)

