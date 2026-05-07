---
title: Install the Discovery Console for OT
description: Install the Service Graph Connector for ServiceNow OT Discovery prior to accessing the Discovery for OT packages. You must also install a Linux distribution on the same machine that has the installed Discovery Console for OT.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-27"
reading_time_minutes: 3
breadcrumb: [Configure the Discovery Console for OT, Discovery Console for OT, Operational Technology Native Discovery components, Operational Technology Discovery, Operational Technology]
---

# Install the Discovery Console for OT

Install the Service Graph Connector for ServiceNow OT Discovery prior to accessing the Discovery for OT packages. You must also install a Linux distribution on the same machine that has the installed Discovery Console for OT.

## Before you begin

Role required: serviceadmin

## About this task

The Linux OS and the Discovery Console for OT must be installed on the same device. After you install the Linux OS, do the following.

**Note:** When running the installation for any of the supported distributions, use the minimal installation, no desktop environment, but include an SSH server in the package selection.

You must be aware of the following information when setting up your VM environment:

-   Ensure that the CPU settings for the VM are set to `host`; the hypervisor/host system must include support for the AVX/AVX2 instruction set.

    **Note:** Be sure you have set this correctly; otherwise, Mongo may crash when you attempt to restart the VM.

-   Allocate 16 GB RAM for the Linux installation.
-   The Discovery Console for OT requires a minimum of 100 GB of storage. See [Requirements for Discovery Console for OT installation](../concept/requirements-installation-deployment.md) for information on storage requirements.
-   You must be on a VM to access images in the Discovery Console for OT.

## Procedure

1.  On your instance, navigate to the Service Graph Connector for ServiceNow OT Discovery Guided Setup page.

2.  Click the **Get Started**.

    The **Download &amp; Deploy OT Discovery** page opens.

3.  In the first section of the setup, select **Download &amp; Deploy OT Discovery**.

4.  Select **Configure** and the **Downloads** page opens.

    **Note:** Read the End User License Agreement \(EULA\) carefully and then check **Agree**.

5.  Download the OT Discovery packages:

    1.  Download and install the Discovery Console for OT package.
    2.  Download and install the Discovery Sensor for OT package \(ISO and OVR\).
    3.  Download and install the OT Discovery Collector package that's compatible with your OS.
6.  From the Discovery Console for OT install package, unzip the `ConsoleInstaller` zip file.

7.  Use the secure copy protocol \(SCP\) to move the `ConsoleInstaller` folder onto your Linux server.

    1.  Push to the Console using following command:

        ```
        scp -r ConsoleInstaller serviceadmin@IP:/home/serviceadmin$
        ```

        For example:

        ```
        $ scp -r ~/Users/Zelda/Downloads/ConsoleInstaller SL serviceadmin@192.168.2.2:/home/serviceadmin
        ```

        **Note:** The ConsoleInstaller folder name can vary if desired.

    2.  Pull from the user computer using the following command:

        ```
        $ scp -r $USER@$IP:~/ConsoleInstaller /home/serviceadmin/
        ```

8.  Run the Console initiation script `Console.init` via SSH.

    1.  Enter the password when prompted.

        ```
        ssh serviceadmin@$IP
        ```

    2.  When asked if you are sure you want to continue, enter `Yes`.

    3.  Navigate to the ConsoleInstaller folder by entering `cd ConsoleInstaller` at the prompt.

        **Note:** If you already have placed your existing `service_credetials.txt````` in the `config` folder, you need to copy this file to the Console's root directory.

        ```
        sudo cp /home/serviceadmin/ConsoleInstaller/config/service_credentials.txt /root
        ```

    4.  Enter `chmod +x Console-init.sh`.

    5.  Enter `sudo /bin/bash Console-init.sh`.

    6.  Select the default answers for all prompts.

9.  Verify that the web Console is running.

    1.  Open a browser and navigate to the web Console via `https://$IP address:8443`.

    2.  If you get a warning for a self-signed certificate error, select **Advance** and accept the EULA.

    3.  Create your account information that conforms to your company policy and add:

        -   username as the user primary admin
        -   email address
        -   password
        **Note:** This user is the primary local admin, and it is recommended that the password is secured as well as 2FA enabled.

10. Reboot the Console by entering `reboot`.


## Result

The installation of the Discovery Console for OT is complete. Before you install the Sensor and Collector, install the Console certificates.

## What to do next

After installation is complete, go to [Generate a certificate](generate-new-certificate-discovery-for-ot.md) for the next steps.

