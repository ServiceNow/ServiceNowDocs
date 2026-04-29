---
title: Configure the Discovery Console for OT
description: This section is an overview of the steps for installing the Discovery Console for OT.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-24"
reading_time_minutes: 3
breadcrumb: [Discovery Console for Operational Technology \(OT\), Operational Technology Native Discovery components, Operational Technology Discovery, Operational Technology]
---

# Configure the Discovery Console for OT

This section is an overview of the steps for installing the Discovery Console for OT.

**Note:** During the installation of the non-containerized version of Discovery Console for OT, you need to access the internet to download and install dependent third-party packages such as Mongo and RabbitMQ. The Console installation automatically installs these packages as long as there's an internet connection. After installation of the third-party packages, the internet connection is unnecessary.

## Workflow

In the ServiceNow instance, navigate to the Service Graph Connector Guided Setup page and select Get Started. In the top section, select the Download &amp; Deploy OT Discovery link. The Download &amp; Deploy OT Discovery page opens. Select **Configure** and the Downloads page opens. Download the OT component packages.

Review the steps in the installation process listed in the Installation Workflow table.

<table id="table_xsx_5vd_f3c"><tbody><tr><td>

**Task**

</td><td>

**Description**

</td></tr><tr><td>

Install virtual machine

</td><td>

You can use any type 1 or type 2 hypervisor. For example: -   VMware
-   Hyper-V
-   Azure
-   AWS
-   Google Cloud
-   Proxmox

</td></tr><tr><td>

Install Linux distribution on the VM.

</td><td>

Install Linux or install a compatible Linux distribution such as:-   Red Hat/Rocky 8.x and 9.x
-   Debian 12
-   Ubuntu 22.04 and 24.04

</td></tr><tr><td>

Hardware requirements

</td><td>

-   RAM: 16 GB \(Recommended\)
-   Hard Disk drive: 100 GB
-   CPUs: 2

</td></tr><tr><td>

Connection

</td><td>

Confirm that you have access to the ServiceNow instance.

</td></tr><tr><td>

Installation packages

</td><td>

As previously stated, from the Downloads page, download the Discovery Console for OT, Discovery Sensor for OT, and the OT Discovery Collector packages.

</td></tr><tr><td>

Containerized packages

</td><td>

For closed network systems, you can download and install containerized packages for the Console and the Collector.

</td></tr><tr><td>

Install the Discovery Console for OT

</td><td>

Install the Discovery Console for OT before you install the Discovery Sensor for OT.

</td></tr><tr><td>

Move the package into the VM

</td><td>

Move the Console installer package into the VM.

</td></tr><tr><td>

Extract the installer

</td><td>

From the Console package, extract the ConsoleInstaller zip file.

</td></tr><tr><td>

Run the installation script

</td><td>

Execute ./console-init.sh. This script ensures all the required components are installed. **Note:** If you are using the traditional console package \(that is, non-containerized package\) you need access to internet to download dependent 3rd party packages such as Mongo and RabbitMQ.

</td></tr><tr><td>

Accessing the web console

</td><td>

To access the web console UI, please open the browser and navigate to https://&lt;IP address of the console VM&gt;:8443.

</td></tr><tr><td>

Register initial user

</td><td>

Before you can log into the Console for the first time, you must register as a user. In the log in window:1.  Enter your username and an email.
2.  Create your own password or generate a random password.
3.  **Copy and save this password.**
4.  Enter the password.
5.  Select the check box, **I acknowledge I saved my password**.
6.  Select **Enter**.

**Note:** Make sure to save the password, to avoid getting locked out of the system. See [Logging onto the Discovery Console for OT](../../operational-technology-discovery-deployment-guide/concept/logging-onto-ot-discovery-console.md) for more instruction.

</td></tr><tr><td>

EULA Agreement

</td><td>

Next, the EULA appears on the screen. Accept the EULA by checking the box next to **Agree**.

</td></tr></tbody>
</table>**Note:** Once installation is complete, and you log onto the Console, you may choose to use the interactive configuration wizard. If so, the wizard guides you to upload your Console license. For more on the wizard, see [Use the Discovery Console for OT interactive configuration wizard](console-onboarding-wizard.md)

## What to do next

To complete installation and configuration of the Discovery Console for OT, continue with the following steps.

1.  See [Logging onto the Discovery Console for OT](../../operational-technology-discovery-deployment-guide/concept/logging-onto-ot-discovery-console.md) for initially logging onto the Console.
2.  Review the [Requirements for Discovery Console for OT installation](../concept/requirements-installation-deployment.md) sections. The requirement section includes information about the Console license.
3.  [Install a Linux operating system](install-linux-os.md).
4.  [Install the Discovery Console for OT](ot-discovery-console-installation.md).
5.  [Generate a certificate](generate-new-certificate-discovery-for-ot.md).

