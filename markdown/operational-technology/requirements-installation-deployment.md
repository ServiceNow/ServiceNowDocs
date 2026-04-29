---
title: Requirements for Discovery Console for OT installation
description: For remote deployment at a facility or on a network, verify that the following requirements are met before installing the Discovery Console for OT.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configure the Discovery Console for OT, Discovery Console for Operational Technology \(OT\), Operational Technology Native Discovery components, Operational Technology Discovery, Operational Technology]
---

# Requirements for Discovery Console for OT installation

For remote deployment at a facility or on a network, verify that the following requirements are met before installing the Discovery Console for OT.

## Infrastructure requirements

You must have a Linux operating system installed that can operate in a virtualization environment or on a Bare-metal server. Install the Discovery Console for OT on a virtual machine.

**Note:** After installing the Console and the Operating System \(OS\) on a virtual machine \(VM\), the VM must have a minimum of 10-GB of unused space available.

## System requirements

<table id="table_i5f_kpx_vgc"><thead><tr><th>

Component

</th><th>

System Requirements

</th></tr></thead><tbody><tr><td>

Discovery Console for OT

</td><td>

-   16 GB RAM
-   100 GB Hard drive
-   2 CPUs

</td></tr></tbody>
</table>## Network requirements

The Discovery Console for OT requires the following ports to be open inbound \(from the connection source to the Console\) to operate.

<table id="table_pxw_hym_33c"><thead><tr><th>

Ports

</th><th>

Description

</th></tr></thead><tbody><tr><td>

TCP 5671

</td><td>

Used by Discovery Sensor for OT to communicate with the Discovery Console for OT. This port is used by the Sensor to report data and receive configuration updates from the Console.

</td></tr><tr><td>

TCP 8443

</td><td>

Used to connect to the Discovery Console for OT Web interface. This port is used by the API.

</td></tr><tr><td>

TCP 5002

</td><td>

Enables Sensors to communicate with the Discovery Console for OT to receive updates.

</td></tr><tr><td>

TCP 443

</td><td>

Used for network communication from the Console to a ServiceNow instance or MID Server via the Service Graph Connector for OT Discovery.

</td></tr><tr><td>

UDP 123 \(Required\)

</td><td>

Enables Sensor devices to synchronize time \(real-time clock\) with the Discovery Console for OT to verify that the time associated with reported data and events is both precise and accurate.

 **Note:**Without port UDP 123 open on the firewall, the clocks of Sensors drift apart from the clock of the Console. When clock drift is present, various features that rely on precise clock synchronization do not work as expected.

</td></tr></tbody>
</table>**Note:** If there are problems accessing the Discovery Console for OT, check the firewall rules and unblock the specific IP addresses and ports used for the installation. If you have any errors or difficulties while using the Discovery Console for OT, [contact Customer Service and Support](https://support.servicenow.com/now?draw=case)

## Discovery Console for OT configuration wizard

The Discovery Console for OT now provides a configuration wizard to guide you through your initial setup and configuration of the Console. If you choose to use the interactive configuration wizard after logging into the Console, it alerts you automatically to upload a Console license. See [Use the Discovery Console for OT interactive configuration wizard](../task/console-onboarding-wizard.md) for more information.

## Discovery Console for OT license

**Note:** Before you can use the Console, you must have a license. Request a Console license from your ServiceNow account representative.

When you first sign into the Console, a warning banner alerts you that there is no license. To upload a license for the Discovery Console for OT, do the following:

1.  From the Home page, navigate to the Settings page.
2.  On the Settings page in the License section, select the **Upload License** button.
3.  Upload your license as a `.zip` file.
4.  Ensure the ZIP file contains the `license.pem` and `pubkey.pem` files.

Once you have uploaded your license, you can use the Console.

![Settings > Upload license](../images/settings-console-license.png)

## License-disabled Console features

It is important to understand that certain features could be disabled if the Discovery Console for OT license is expired. After the license expires, the locking mechanism is triggered and disables these features. No data is lost in the background. When a valid license is uploaded, the customers can start or continue working. When the license is about to expire, the Console displays a warning banner as an alert.

The license:

-   Enables the ability to run Auto Query and asset scans \(disabled on expiration\).
-   Enables the consumption of network connection data \(disabled on expiration\).
-   Enables the creation and viewing of API tokens \(disabled on expiration\).
-   Enables the export of collections \(for example, assets\) to files \(disabled on expiration\).

**Note:** You cannot export RAW XML results if your Console license is invalid \(absent or expired\).

