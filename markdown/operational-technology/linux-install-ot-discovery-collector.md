---
title: Install OT Discovery Collector on a Linux system
description: Install the OT Discovery Collector on a Linux system.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-27"
reading_time_minutes: 1
breadcrumb: [Configure the OT Discovery Collector, Operational Technology \(OT\) Discovery Collector, Operational Technology Native Discovery components, Operational Technology Discovery, Operational Technology]
---

# Install OT Discovery Collector on a Linux system

Install the OT Discovery Collector on a Linux system.

## Before you begin

-   SCP the `linuxCollectorinstaller_[version number]_[build number].tar.gz` over to the Linux system.

    **Note:** An example of the file name format is`linuxCollectorinstaller_3.3.1_20250917.1.tar.gz`.

-   You need to SCP the `CollectorBundle` file you generated and downloaded from the Discovery Console to the Linux system.
-   To go into OT Discovery Collector Linux host, use `ssh`.
-   Use `su` or `sudo -s` to switch to the root user.

Role required: admin

## Procedure

1.  On your instance, navigate to the Service Graph Connector for ServiceNow OT Discovery Guided Setup page.

2.  Click the **Get Started**.

    The **Download &amp; Deploy OT Discovery** page opens.

3.  In the first section of the setup, select **Download &amp; Deploy OT Discovery**.

4.  Select **Configure** and the **Downloads** page opens.

    **Note:** Read the End User License Agreement \(EULA\) carefully and then check **Agree**.

5.  Download the OT Discovery Collector installation and deployment package for Linux.

6.  Install the Collector on the Discovery Console for OT you intend to use.

7.  On a RHEL-based distribution, install tar.

    ```
    sudo dnf install -y tar
    ```

8.  On all Linux distributions, run the following command:

    ```
    tar -xvf linuxCollectorinstaller_[version number]_[build number].tar.gz
    ```

9.  Copy the `CollectorBundle` file into the `CollectorInstaller` directory.

    ```
    chmod +x Collector-init.sh
    
    ./Collector-init.sh
    ```

10. When the script starts, the system locates the pdf version of the EULA.

    When prompted to accept the EULA, enter `Y` for yes.

11. After the script completes successfully, the OT Discovery Collector can be seen in the console.

    To check the service status, run this command: `systemctl status SNDiscoveryCollector`. If you would like to view the journal output for the service to troubleshoot issues, as the root user you can run `journalctl -f -a -u SNDiscoveryCollector`.


## Result

After the script completes successfully, the OT Discovery Collector can now be seen in the console.

To check the service status, run this command:

```
systemctl status SNDiscoveryCollector
```

.

If you would like to view the journal output for the service \(usually as a troubleshooting measure\), as the root user you can run:

```
journalctl -f -a -u SNDiscoveryCollector
```

.

