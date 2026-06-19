---
title: Register the Discovery Sensor for OT
description: When you have installed the Discovery Console for OT and the Discovery Sensor for OT, register the Sensor to the Console with the Console's Device Management Interface \(DMI\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/operational-technology/registering-ot-sensor.html
release: australia
product: Operational Technology
classification: operational-technology
topic_type: task
last_updated: "2026-03-24"
reading_time_minutes: 2
breadcrumb: [Configure the Discovery Sensor for OT, Discovery Sensor for Operational Technology \(OT\), Operational Technology Native Discovery components, Operational Technology Discovery, Operational Technology]
---

# Register the Discovery Sensor for OT

When you have installed the Discovery Console for OT and the Discovery Sensor for OT, register the Sensor to the Console with the Console's Device Management Interface \(DMI\).

## Before you begin

Role required: admin

## About this task

Confirm you that you have installed the Sensor. You must register the Sensor to the Console with the DMI. The DMI is a web-based interface that lets you configure and register the Sensor with the Console. For more information on the DMI, see [Device Management Interface](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/dmi.md). Registering the Sensor confirms it can communicate with the Console.

## Procedure

1.  Access the DMI for a Discovery Sensor for OT by opening a browser and entering the URL displayed on the screen when the Sensor is installed and boots up.

    **Note:** Currently, there isn't a serial number portion since there's no active hardware. These input steps are still valid. But the `[serial number]` is likely to be the Sensor name at the time of its creation. This is an example of how to find the URL for the DMI. Your IP address will be different from this example:

    ```
    https://[device type]-[serial number] with either .local:443 or .[domain name]:443 
    ```

    Be sure to make a note of the DMI URL displayed after the Sensor is installed. You can use this URL for the DMI. This image shows the DMI URL as https://172.16.241.131:443.

    \[Omitted image "dmi-url.png"\] Alt text: DMI URL

2.  In the DMI, log in using your credentials.

    -   DMI \(Web Interface\):
        -   Username: admin
        -   Password: password
    -   SSH login:
        -   Username: serviceadmin
        -   Password: devpassword
    **Note:** After the initial log in is completed, the DMI prompts you to change the password.

3.  In a separate tab or browser, log in to the Discovery Console for OT.

4.  In the Console, navigate to **Appliances &gt; Certificates**.

5.  Under Sensor Credentials, select the **Generate Bundle**.

    In the prompt window, select **Generate Bundle** again.

6.  The bundle generates and downloads to your designated download folder.

7.  Switch back to the DMI.

8.  In the DMI, navigate to **Console &gt; Credentials**.

9.  Select **Bundle File Input** and from this window, select the generated Sensor bundle.

10. Select **Upload Credentials Bundle** to upload the Sensor bundle to the DMI.

    After the bundle is uploaded, the **Certificate Update Logs** appears and confirms the completed process.

11. The DMI automatically extracts the certificate from the bundle and registers the Sensor.

12. From the DMI menu, select the **Network** tab.

13. Select the **Edit** button.

14. Select an IP Address or Hostname for the Console endpoint and enter a valid value.

    Enter a valid Gateway IP Address.

15. Select **Save &amp; Deploy**.

16. Navigate back to the **Console** tab and select the **Register** button.

17. In the Console, confirm that the Sensor is online.

    The device briefly shows online and then offline. Then it shows a steady online status in the Console.


## Result

The Sensor and the Console can now communicate and generate queries.

