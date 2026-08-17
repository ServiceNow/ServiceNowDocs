---
title: Configure the Discovery Console for OT
description: This section is an overview of the steps for installing the Discovery Console for OT.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/operational-technology/configure-ot-discovery-console.html
release: australia
topic_type: concept
last_updated: "2026-03-24"
reading_time_minutes: 4
breadcrumb: [Discovery Console for OT, Operational Technology Native Discovery components, Operational Technology Discovery, Operational Technology]
---

# Configure the Discovery Console for OT

This section is an overview of the steps for installing the Discovery Console for OT.

**Note:** During the installation of the non-containerized version of Discovery Console for OT, you must have access the internet to download and install dependent third-party packages such as MongoDB and RabbitMQ. The Console installation automatically installs these packages as long as there's an internet connection. After installation of the third-party packages, the internet connection is unnecessary.

## Workflow

In your instance, navigate to the Service Graph Connector for ServiceNow OT Discovery Guided Setup page and select Get Started. In the top section, select the Download &amp; Deploy OT Discovery link. The Download &amp; Deploy OT Discovery page opens. Select **Configure** and the Downloads page opens. Download the OT component packages.

**Note:** The required dependency version has been changed to .NET 10 from .NET 8

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

Install Linux or install a compatible Linux distribution such as:-   RedHat Enterprise Linux \(RHEL\) 8.x, 9x, and 10x
-   Rocky 8.x, 9x, and 10x
-   Debian 12 and 13
-   Ubuntu 22.04 and 24.04

</td></tr><tr><td>

Hardware requirements

</td><td>

-   RAM: 16 GB \(Recommended\)
-   Hard Disk drive: 100 GB
-   CPUs: 2

For more information, see [OT Discovery System Resources](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/ot-discovery-system-resources.md).

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

For closed network systems, you can download and install containerized packages for the Console and the Collector. Select the Collector package that is compatible to your machine's OS. For more information, see [Air-gapped networks and OT Discovery installation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/air-gapped-networks-installation.md).

</td></tr><tr><td>

Begin the install for the Discovery Console for OT

</td><td>

Install the Discovery Console for OT before you install the Discovery Sensor for OT. Install the OT Discovery Collector last.

</td></tr><tr><td>

Move the package into the VM

</td><td>

Move the Console installer package into the VM.

</td></tr><tr><td>

Extract the installer

</td><td>

From the Console package, extract the ConsoleInstaller .ZIP file.

</td></tr><tr><td>

Run the installation script

</td><td>

Execute ./console-init.sh. This script confirms all the required components are installed. **Note:** If you're using the traditional console package \(that is, non-containerized package\) you need access to internet to download dependent third-party packages such as MongoDB and RabbitMQ.

</td></tr><tr><td>

Accessing the web console

</td><td>

To access the web console UI, open the browser and navigate to https://&lt;IP address of the console VM&gt;:8443.

</td></tr><tr><td>

Register initial user

</td><td>

Before you can log in to the Console for the first time, you must register as a user. In the log in window:1.  Enter your username and an email.
2.  Create your own password or generate a random password.
3.  **Copy and save this password.**
4.  Enter the password.
5.  Select the check box, **I acknowledge I saved my password**.
6.  Select **Enter**.

**Note:** Make sure to save the password, to avoid getting locked out of the system. For more information, see [Log on to the Discovery Console for OT](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/log-onto-ot-console.md).

</td></tr><tr><td>

EULA Agreement

</td><td>

Next, the EULA appears on the screen. Accept the EULA by checking the box next to **Agree**.

</td></tr><tr><td>

Generate a new certificate

</td><td>

After the Console is installed, generate a new Console certificate. For more information, see [Generate a certificate](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/generate-new-certificate-discovery-for-ot.md).

</td></tr></tbody>
</table>**Note:** Once installation is complete, and you log in to the Console, you can choose to use the interactive configuration wizard. The wizard guides you to upload your Console license. It also takes you through the getting started with the system, such as: creating a Site, creating a Network Zone, and building your initial Auto Query. For more information, see [Use the Discovery Console for OT interactive configuration wizard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/console-onboarding-wizard.md).

-   **[Air-gapped networks and OT Discovery installation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/air-gapped-networks-installation.md)**  
This section explains the options for air-gapped and non-air-gapped network, installation of Discovery for OT components, and accessing data from scans and queries.
-   **[Requirements for Discovery Console for OT installation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/reqs-ot-console-installation.md)**  
For remote deployment at a facility or on a network, verify that the following requirements are met before installing the Discovery Console for OT.
-   **[Install a Linux operating system](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/install-linux-os.md)**  
Install a Linux operating system on a virtual machine and then install the Discovery Console for OT on the same VM.
-   **[Install the Discovery Console for Operational Technology \(OT\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/install-discovery-console-ot.md)**  
Install the Service Graph Connector for OT Discovery before accessing the Discovery for OT packages. You must also install a Linux distribution on the same machine the Discovery Console for OT is installed on.
-   **[Log on to the Discovery Console for OT](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/log-onto-ot-console.md)**  
This sections describes your initial log onto the OT Discovery Collector.
-   **[Generate a certificate](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/generate-new-certificate-discovery-for-ot.md)**  
Generate a certificate to use with the Discovery Console for OT or upload your own certificates. This certificate allows the Console to boot up.

**Parent Topic:**[Discovery Console for Operational Technology \(OT\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/ot-discovery-console-landing.md)

