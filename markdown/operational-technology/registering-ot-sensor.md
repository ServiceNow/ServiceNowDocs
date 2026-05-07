---
title: Register the Discovery Sensor for OT
description: After you have installed the Discovery Console for OT and the Discovery Sensor for OT, register the Sensor to the Console with the Console's Device Management Interface \(DMI\).
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-24"
reading_time_minutes: 2
breadcrumb: [Configure the Discovery Sensor for OT, Discovery Sensor for OT, Operational Technology Native Discovery components, Operational Technology Discovery, Operational Technology]
---

# Register the Discovery Sensor for OT

After you have installed the Discovery Console for OT and the Discovery Sensor for OT, register the Sensor to the Console with the Console's Device Management Interface \(DMI\).

## Before you begin

Role required: admin

## About this task

Verify you [Install the Discovery Sensor for OT](install-discovery-sensor-for-ot.md) before registering your Sensor. You must register the Sensor to the Console with the DMI. The DMI is a web-based interface that lets you configure and register the Sensor with the Console. For more information on the DMI, see [Device Management Interface](../concept/dmi.md). Registering the Sensor confirms it can communicate with the Console.

## Procedure

1.  To access the DMI for a Discovery Sensor for OT, open a browser and type in the URL displayed on the screen after the Sensor is installed and boots up.

    **Note:** Currently, there isn't a serial number portion since there's no active hardware. These input steps are still valid. But, the `[serial number]` is likely to be the Sensor name at the time of its creation. This is an example of how to find the URL for the DMI. Your IP address will be different from this example:

    ```
    https://[device type]-[serial number] with either .local:443 or .[domain name]:443 
    ```

    Be sure to make a note of the DMI URL displayed after the Sensor is installed. You can use this URL for the DMI. This image shows the DMI URL as https://172.16.241.131:443.

    ![DMI URL](../concept/ot-discovery-console-user-guide/image/dmi-url.png)

2.  Using your credentials, log into the DMI.

    -   DMI \(Web Interface\):
        -   Username: admin
        -   Password: password
    -   SSH login:
        -   Username: serviceadmin
        -   Password: devpassword
    **Note:** Once the initial log in has been completed, the DMI prompts you to change the password.

3.  In a separate tab or browser, if you haven't already, log into the Console.

4.  Generate and upload a bundle.

    1.  In the Console, navigate to **Sensors &gt; Certificates**.

    2.  Under **Sensor Credentials**, select **Generate Bundle**.

    3.  Download and save the generated bundle zip file.

    4.  Unzip the file.

        By unzipping the file, you get a `password.txt` file, a `Sensorbundle` file, and a `service_credentials.txt` file.

    5.  Switch back to the DMI browser window or tab.

    6.  Select the **Certificate** tab.

    7.  In the **Certificate Bundle** field, select **Browse** and upload the `Sensorbundle` file.

    8.  In the **Password** field, copy and paste the password from the `password.txt` file.

    9.  Select **Upload Certificate**.

        Once the certificate is uploaded, the **Certificate Update Logs** appears and confirms the completed process.

5.  Edit the Console settings.

    1.  In the DMI, select the **Network** tab.

    2.  Select the **Edit** button.

    3.  Select an IP Address or Hostname as the Console endpoint and enter a valid value.

        Enter a valid Gateway IP Address.

    4.  Select **Save &amp; Deploy**.

    5.  Navigate back to the **Console** tab and select the **Register** button.

6.  Navigate back to the Console and verify that the Sensor is online.

    The device briefly shows online and then offline. Then it shows a steady online status in the Console.


## Result

The Sensor and the Console can now communicate.

