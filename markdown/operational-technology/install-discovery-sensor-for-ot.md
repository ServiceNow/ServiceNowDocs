---
title: Install the Discovery Sensor for OT
description: Download the Discovery Sensor for OT package and install the ISO image. Then install the Discovery Sensor for OT.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/operational-technology/install-discovery-sensor-for-ot.html
release: australia
product: Operational Technology
classification: operational-technology
topic_type: task
last_updated: "2026-03-27"
reading_time_minutes: 3
breadcrumb: [Configure the Discovery Sensor for OT, Discovery Sensor for Operational Technology \(OT\), Operational Technology Native Discovery components, Operational Technology Discovery, Operational Technology]
---

# Install the Discovery Sensor for OT

Download the Discovery Sensor for OT package and install the ISO image. Then install the Discovery Sensor for OT.

## Before you begin

Role required: admin

## About this task

You can register the Sensor after you have installed the OT Discovery Console and system. Before you can register a Sensor to the Console, you must confirm that you have completed the following.

-   From the Downloads page, download the Sensor package; the Sensor ISO file is in the same package.
-   Install the ISO image.
-   Determine if you're using the ISO as a Virtual Machine \(VM\) or are installing the ISO on hardware. If you're using the ISO as a VM, you can use any of the following VMs.
    -   VWware
    -   Hyper-V
    -   Proxmox
    -   Linux KVM

        If you choose to install the ISO on hardware through BareMetal, you must use a tool to create a USB ISO installer.

-   You must open both the Console and the DMI interfaces to complete the Sensor registration.

## Procedure

1.  On your instance, navigate to the [Service Graph Connector for ServiceNow Operational Technology \(OT\) Discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/sgc-ot-discovery.md) Guided Setup page.

2.  Select the **Get Started**.

    The **Download &amp; Deploy OT Discovery** page opens.

3.  In the first section of the setup, select **Download &amp; Deploy OT Discovery**.

4.  Select **Configure** and the **Downloads** page opens.

    \[Omitted image "downloads-page-containerized2.png"\] Alt text: Downloads page

    **Note:** Read the End User License Agreement \(EULA\) carefully and then check **Agree**.

5.  Download the Discovery Sensor for OT installation and deployment package.

6.  Unzip the Sensor package.

    The ISO image is included in the Sensor package.

7.  Create the virtual machine for the Discovery Sensor for OT.

8.  Install the Discovery Sensor for OT.

9.  Select the default answers for all prompts.

10. Upload the ISO image to your virtualization platform.

11. Create the hardware NICs which the VM uses to communicate with the Sensor.

    **Note:** The following images are examples specific to an ESXi 8.0 U2 virtual machine.

    \[Omitted image "image-sensor-iso-efi2.png"\] Alt text: ESXi 8.0 U2 example

    **Note:** For communications to work between Discovery components, two network adapters should be connected on the VM.

    \[Omitted image "image-sensor-two-nics2.png"\] Alt text: Select 2 NICs example

    **Note:** For other VM options, confirm that EFI is selected \(and not BIOS\) as the Firmware and that the "Enable Secure Boot" flag is not selected.

12. Install the ISO image.

13. After installing, when alerted, remove any install media.

    The alert message is: "System needs to reboot to complete installation. Please remove all install media and once complete press any key to reboot."

14. Reboot the system.

15. After removing any install media, the install process starts for the Sensor.

16. Create the virtual machine for the Sensor.

17. Select the OS as **Other Linux 64-bit**.

18. Attach the Sensor ISO to the CD/DVD to boot the VM.

19. Create 2 hardware NICs specifically for the VM.

20. For other VM options, confirm that EFI is selected \(and not BIOS\) as the Firmware and that the "Enable Secure Boot" flag is not selected.

21. Assign a minimum of 8 GB RAM and 60 GB HDD for the installation.

22. Power on the VM and the install starts.

    You see this screen:

    \[Omitted image "sensor-install-accept-defaults.png"\] Alt text: Select defaults?

23. Select `Yes` to start the install.

24. Once the install is complete, select **Enter** to reboot the VM.

    \[Omitted image "sensor-install-reboot.png"\] Alt text: Reboot the VM

    This screen displays after the Sensor boots up.

    \[Omitted image "sensor-install-servicenow.png"\] Alt text: Sensor is installed

25. On the VM page, the DMI page URL displays.

    \[Omitted image "sensor-install-dmi-ip.png"\] Alt text: DMI page URL

26. Use this URL to log into the DMI and register your Discovery Sensor for OT to the Console.

    See [Register the Discovery Sensor for OT](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/registering-ot-sensor.md) on how to register the Sensor.


## What to do next

[Register the Discovery Sensor for OT](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/registering-ot-sensor.md)

