---
title: Configure the Discovery Sensor for OT
description: Configuring the Discovery Sensor for OT provides discovery of all assets in your OT environment. The Sensor requires a Linux operating system that is installed either as a virtual machine or on a Bare-metal computer that is x86.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/operational-technology/configure-discovery-sensor-ot.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Discovery Sensor for Operational Technology \(OT\), Operational Technology Native Discovery components, Operational Technology Discovery, Operational Technology]
---

# Configure the Discovery Sensor for OT

Configuring the Discovery Sensor for OT provides discovery of all assets in your OT environment. The Sensor requires a Linux operating system that is installed either as a virtual machine or on a Bare-metal computer that is x86.

## Discovery Sensor for OT System requirements

<table id="table_i5f_kpx_vgc"><thead><tr><th>

Component

</th><th>

System Requirements

</th></tr></thead><tbody><tr><td>

Discovery Sensor for OT

</td><td>

-   16 GB RAM
-   100 GB Hard drive
-   2 CPUs
-   2 virtual NIC cards

</td></tr></tbody>
</table>## Workflow

Review the steps in the Sensor installation process from the table.

<table id="table_xsx_5vd_f3c"><tbody><tr><td>

**Task**

</td><td>

**Description**

</td></tr><tr><td>

Navigate to the Download &amp; Deploy OT Discovery page.

</td><td>

In the ServiceNow instance, navigate to the Service Graph Connector for ServiceNow Operational Technology \(OT\) Discovery Guided Setup page and select Download &amp; Deploy OT Discovery.

</td></tr><tr><td>

The **Downloads** page opens.

</td><td>

Download the Discovery Sensor for OT package.

</td></tr><tr><td>

EULA Agreement

</td><td>

Ready the EULA appears on the **Downloads** page. Accept the EULA by checking the box next to **Agree**.

</td></tr><tr><td>

ISO image

</td><td>

Unzip the Sensor package. The ISO image is included in the Sensor package.

</td></tr><tr><td>

Create a virtual machine.

</td><td>

Select **Other Linux 64-bit** as the OS.

</td></tr><tr><td>

CD/DVD

</td><td>

Attach the Sensor ISO to the CD/DVD to boot the VM.

</td></tr><tr><td>

Run the installation.

</td><td>

Follow the installation steps in [Install the Discovery Sensor for OT](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/install-discovery-sensor-for-ot.md).

</td></tr><tr><td>

Register the Sensor

</td><td>

Register the Sensor with the DMI and Console. This confirms that the Console and Sensor can communicate with each other. For more information, see [Register the Discovery Sensor for OT](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/registering-ot-sensor.md) for more information.

</td></tr></tbody>
</table>-   **[Install the Discovery Sensor for OT](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/install-discovery-sensor-for-ot.md)**  
Download the Discovery Sensor for OT package and install the ISO image. Then install the Discovery Sensor for OT.
-   **[Register the Discovery Sensor for OT](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/registering-ot-sensor.md)**  
When you have installed the Discovery Console for OT and the Discovery Sensor for OT, register the Sensor to the Console with the Console's Device Management Interface \(DMI\).
-   **[Device Management Interface](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/dmi.md)**  
The Device Management Interface \(DMI\) is a web-based interface where you configure and register a Discovery Sensor for OT to the Discovery Console for OT.
-   **[Deregister a Discovery Sensor for OT](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/deregister-sensor-console.md)**  
Deregister a Discovery Sensor for OT from the Discovery Console for OT that is no longer available on your system.
-   **[Remove a lost Sensor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/remove-lost-sensor-console.md)**  
Remove a Sensor that no longer functions or is otherwise reported as having a lost connection from the Discovery Console for OT.

**Parent Topic:**[Discovery Sensor for Operational Technology \(OT\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/ot-discovery-sensor-landing.md)

