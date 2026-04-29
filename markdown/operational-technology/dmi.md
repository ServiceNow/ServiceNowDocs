---
title: Device Management Interface
description: The Device Management Interface \(DMI\) is a web-based interface that lets you configure and register a Sensor to the Discovery Console for OT.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure the Discovery Sensor for OT, Discovery Sensor for Operational Technology \(OT\), Operational Technology Native Discovery components, Operational Technology Discovery, Operational Technology]
---

# Device Management Interface

The Device Management Interface \(DMI\) is a web-based interface that lets you configure and register a Sensor to the Discovery Console for OT.

## DMI overview

With the DMI, you can register a Sensor to allow the Sensor to communicate with the Discovery Console for OT. By registering the Sensor, you are ready to start using the Console.

**Note:** The Console and the DMI are separate web-based interfaces that you access with an HTTPS web address. You need to open both interfaces when registering the Sensor. During the first log into the DMI, the username admin and the password `devpassword` are provided.

Once the Console is deployed and you have registered the Sensor, you can create these necessary components on the Console to discover assets in your environment.

-   Site
-   Network Zone
-   Auto Query
-   Quick Scan

For more information about these Console features, see [Discovery Console for Operational Technology \(OT\)](ot-discovery-console-landing.md).

## DMI pages

The following sections describe the pages available on the DMI.

-   **Device**

    The Device page includes a summary of the basic configuration information for the Sensor. This page includes details about the Sensor’s name, type, description, serial number, firmware version, build date, model, and revision.

    On the Device page, you can edit the Sensor name. If you change the name before you register the Sensor, the updated name appears in the Console. Otherwise, if you change the name after registering the Sensor, you must update the Sensor name in the Console itself.

-   **Network**

    The Network page includes a diagram of the Sensor and information about its connection to the Console, management interface, and bridge or span interface. You can edit the information on this page as needed when registering the Sensor.

-   **Console**

    The Console page enables you to register the Sensor with the Console. If needed, you can edit the Console endpoint and Console gateway from this page. Selecting the **Edit Settings** button redirects you to the Network page, where you can make your changes. After your register the Sensor with the Console, the Sensor appears in the Console on the Sensors page.

-   **Location**

    The Location page includes the following fields that describe the location of the Sensor.

    -   Latitude
    -   Longitude
    -   Description of the physical location
    You can add or change the location information for a Sensor by selecting the **Edit** button.

-   **Password**

    ThePassword page provides the option to update the password of the DMI. You can change the password by selecting **Edit** and entering the updated password.




-   **Certificate**

    The Certificate page enables you to upload a certificate downloaded from the Discovery Console for OT. This certificate is needed for registering the Sensor with the Discovery Console for OT.

-   **Help**

    The Help page includes information about keyboard shortcuts related to the DMI.




![DMI page](../images/dmi-sans-rabbitmq.png)

