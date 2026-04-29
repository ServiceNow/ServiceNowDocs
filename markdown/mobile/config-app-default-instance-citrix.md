---
title: Configure the ServiceNow app for the default instance
description: Configure apps that support managed configuration by deploying an XML configuration file to users' iOS devices.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Citrix XenMobile, Device management, Before implementation, Configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Configure the ServiceNow app for the default instance

Configure apps that support managed configuration by deploying an XML configuration file to users' iOS devices.

## Before you begin

Role required: admin

## About this task

Configuring the app for a default instance is only available for iOS devices.

## Procedure

1.  In the XenMobile console, click **Configure** &gt; **Device Policies**.

2.  Click **Add**.

3.  In the Add a New Policy page, under Apps, click **App Configuration**.

4.  On the Policy Information page, enter the following information.

    |Field|Description|
    |-----|-----------|
    |**Policy Name**|Type a descriptive name for the policy.|
    |**Description**|Optionally, type a description of the policy|

5.  Click **Next**.

6.  In the Policy Platforms panel, select **iOS**.

7.  In the Identifier list, select **Add new**.

8.  Enter the following in the add new identifier field: `com.servicenow.servicenow`.

9.  In the Dictionary content field, enter the following text.

    ```
    <dict>
    	<key>SNDefaultInstanceURL</key>
           <string>https://<instance_name>.service-now.com</string>
    </dict>
    ```

    Use the name of your own instance where it says &lt;instance\_name&gt;.

10. Click **Check Dictionary** to verify the XML.

11. Depending on the deployment rules for your organization, use the Deployment Rules section to configure deployment rules.

12. Click **Next**.

13. From the Delivery Group Assignments page, select the delivery groups for users that you want to have the ServiceNow application. You can also configure a deployment schedule.

14. Click **Save**.


**Parent Topic:**[Citrix XenMobile](../concept/citrix-mdm.md)

**Related topics**  


[Citrix: Add apps](https://docs.citrix.com/en-us/xenmobile/server/apps.html)

[Citrix: Android for Work](https://docs.citrix.com/en-us/xenmobile/server/provision-devices/android-for-work.html)

[Citrix: App configuration policy](https://docs.citrix.com/en-us/xenmobile/server/policies/app-configuration-policy.html)

[Citrix: VPN policy](https://docs.citrix.com/en-us/xenmobile/server/policies/vpn-policy.html)

