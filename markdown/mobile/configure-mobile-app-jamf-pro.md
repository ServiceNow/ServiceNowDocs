---
title: Configure the ServiceNow mobile app for Jamf Pro
description: Use app configuration to pre-configure the instance URL in Jamf Pro.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Jamf Pro mobile device management \(MDM\), Supported mobile device management vendors, Considerations before implementation, ServiceNow Mobile Platform configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Configure the ServiceNow mobile app for Jamf Pro

Use app configuration to pre-configure the instance URL in Jamf Pro.

## Before you begin

Role required: admin

## Procedure

1.  Log in to Jamf Pro.

2.  Click **Devices**.

3.  In the Devices panel, click **Mobile Device Apps**.

4.  On the mobile device apps page, click **New**.

5.  Under Choose an App type, select **App Store app or VPP store app**.

6.  Click **Next**.

7.  In the search field, type `ServiceNow`.

8.  Next to the ServiceNow app, click **Add**.

9.  On the New Mobile Device App page, click the **App Configuration** tab.

10. In the Preferences field, paste the following string.

    ```
    <dict>
        <key>SNDefaultInstanceURL</key> 
        <string>https://<instance_name>.service-now.com</string> 
    </dict>
    ```

    Use the name of your own instance where it says &lt;instance\_name&gt;.

11. Click **Save**.

    ![Jamf mobile device configuration with the code block in the preferences field](../image/JamfMDM.png)


## What to do next

After the instance is configured for the mobile app, configure the app settings to distribute the app to mobile devices in the scope.

**Parent Topic:**[Jamf Pro mobile device management \(MDM\)](../concept/jamf-mdm.md)

**Related topics**  


[Configure app scope](https://docs.jamf.com/10.1.0/jamf-pro/administrator-guide/Scope.html)

