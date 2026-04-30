---
title: Add the ServiceNow app for Android to MobileIron
description: Configure the ServiceNow app for Android for MobileIron distribution.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [MobileIron Mobile Device Management \(MDM\), Supported mobile device management vendors, Considerations before implementation, ServiceNow Mobile Platform configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Add the ServiceNow app for Android to MobileIron

Configure the ServiceNow app for Android for MobileIron distribution.

## Before you begin

Role required: admin

## Procedure

1.  Sign in to the MobileIron portal.

2.  Navigate to **Apps** &gt; **App Catalog**, then click **Add**.

3.  From the search menu list, select the Google Play store.

4.  In the search bar, type `ServiceNow`.

5.  Select the ServiceNow app from the results.

6.  Click **Next**.

7.  Describe and add screenshots of the app.

8.  Click **Next**.

9.  Set a distribution level for this configuration of the app.

    -   Everyone: The app is added to all user-compatible devices.
    -   No one: The app is staged for distribution at a later date.
    -   Custom: The app is distributed only to users or groups you choose.
10. In the App Configuration Summary section, click **Managed Configurations for Android**.

11. Add the name and configuration value for the default instance configuration.

    |Field|Description|
    |-----|-----------|
    |Name|Name for the configuration, for example, Default instance.|
    |Configuration value|The full instance URL, for example, `https://<instance name>.service-now.com/` .|

12. Set a distribution level for this configuration of the app.

    -   Everyone: The app is added to all user-compatible devices.
    -   No one: The app is staged for distribution at a later date.
    -   Custom: The app is distributed only to users or groups you choose.
    ![App configuration page for Android on MobileIron](../image/mobileIron-12.png "MobileIron app config")

13. Click **Next**.

14. Click **Done**.


## Result

The ServiceNow app for Android from the Google Play store appears in the App Catalogs section on the MobileIron Portal. Mobile users can download it from the MobileIron App Catalog.

For more information on the MobileIron App Catalog, see the [MobileIron documentation](http://mi.extendedhelp.mobileiron.com/49/all/en/desktop/App_Catalog.htm).

If your instance is on an internal network, you might need to configure the VPN. For more information, see the MobileIron documentation on [VPN configuration](http://mi.extendedhelp.mobileiron.com/49/all/en/desktop/VPN_Configuration.htm).

**Parent Topic:**[MobileIron Mobile Device Management \(MDM\)](../concept/mobileiron-mdm.md)

