---
title: Install the Discovery Console for OT
description: Install the Service Graph Connector for OT Discovery before accessing the Discovery for OT packages. You must also install a Linux distribution on the same machine the Discovery Console for OT is installed on.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/operational-technology/install-discovery-console-ot.html
release: australia
product: Operational Technology
classification: operational-technology
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configure the Discovery Console for OT, Discovery Console for Operational Technology \(OT\), Operational Technology Native Discovery components, Operational Technology Discovery, Operational Technology]
---

# Install the Discovery Console for OT

Install the Service Graph Connector for OT Discovery before accessing the Discovery for OT packages. You must also install a Linux distribution on the same machine the Discovery Console for OT is installed on.

## Before you begin

Role required: user

## About this task

Once the Linux OS is installed on the device with the Discovery Console for OT installed on it, do the following.

**Note:** When running the installation for any of the supported distributions, you’ll want to use the minimal installation, no desktop environment, but include an SSH server in the package selection.

Important when setting up your VM environment:

-   Verify that the CPU settings for the VM are set to `host`; the hypervisor/host system must include support for the AVX/AVX2 instruction set.

    **Note:** Be sure you have set this correctly; otherwise, MongoDB may crash when you attempt to restart the VM.

-   Allocate 16 GB RAM for the Linux installation.
-   The OT Discovery Console requires a minimum of 100 GB of storage. Increase the storage based on Deep packet capture inspection requirements. See  or [Operational Technology Discovery deployment scenarios](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/deployment-scenarios.md) for information on storage requirements.
-   You must be on a VM to access images in the Discovery Console for OT.

## Procedure

1.  On your ServiceNow instance, navigate to the [Service Graph Connector for ServiceNow Operational Technology \(OT\) Discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/sgc-ot-discovery.md) Guided Setup page.

2.  Select **Get Started**.

    The **Download &amp; Deploy OT Discovery** page opens.

3.  In the first section of the setup, select Download &amp; Deploy OT Discovery.

4.  Select **Configure** and the **Downloads** page opens.

    \[Omitted image "downloads-page-containerized2.png"\] Alt text: Downloads page

    **Note:** For information on downloading and installing the containerized Console and Collector packages, see [Air-gapped networks and OT Discovery installation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/air-gapped-networks-installation.md).

5.  On the OT Discovery page, download the Discovery packages:

    1.  First download and install the Discovery Console for OT package.

    2.  After the Console, download and install the Discovery Sensor for OT package.

    3.  Finally, download and install the OT Discovery Collector package that is compatible with your machine's OS.

    **Note:** Read the End User License Agreement \(EULA\) carefully and then check Agree.

6.  From the Discovery Console for OT install package, unzip the `ConsoleInstaller` ZIP file.

7.  Use the secure copy protocol \(SCP\) to move the ConsoleInstaller folder onto your Linux server.

    1.  Push to the console:

        ```
        scp -r ConsoleInstaller serviceadmin@IP:/home/serviceadmin$
        ```

        For example:

        ```
        $ scp -r ~/Users/Zelda/Downloads/ConsoleInstaller SL serviceadmin@192.168.2.2:/home/serviceadmin
        ```

        **Note:** The ConsoleInstaller folder name can vary if so desired.

    2.  Pull from the user computer:

        ```
        $ scp -r $USER@$IP:~/ConsoleInstaller /home/serviceadmin/
        ```

8.  Run the console initiation script \(`console.init`\) via SSH.

    1.  Enter the password when prompted.

        ```
        ssh serviceadmin@$IP
        ```

    2.  When asked if you're sure you want to continue, type `Yes`.

    3.  You can enter: `chmod +x console-init.sh`.

    4.  Then enter `sudo /bin/bash console-init.sh`.

    5.  Select the default answer for all prompts.

9.  Verify that the web console is running.

    1.  Open a browser and navigate to the web console via `https://$IP:8443`.

    2.  When warned of a self-signed certificate error, select **Advance** and accept the EULA.

    3.  Create account information that conforms to your company policy and add:

        -   Username as the user primary admin
        -   Enter an email address
        -   Create a password \(that conforms to the company policy\)
        -   Log the username and password in a secure location
        -   Then select **Register**.
        **Note:** This user is the primary local admin, and it's recommended that the password is secured as well as 2FA enabled.

10. Reboot the console by entering `reboot` in the terminal window.


## Result

The installation for the Discovery Console for OT is complete. Before you install the Discovery Sensor for OT package, install the Discovery Console for OT certificate.

**Note:** If you encounter any errors, [Contact Customer Service and Support.](https://support.servicenow.com/now?draw=case)

