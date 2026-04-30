---
title: Add the ServiceNow app for iOS to MobileIron
description: Configure the ServiceNow app for iOS for MobileIron distribution.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [MobileIron Mobile Device Management \(MDM\), Supported mobile device management vendors, Considerations before implementation, ServiceNow Mobile Platform configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Add the ServiceNow app for iOS to MobileIron

Configure the ServiceNow app for iOS for MobileIron distribution.

## Before you begin

Role required: admin

## Procedure

1.  Sign in to the MobileIron portal.

2.  Navigate to **Apps** &gt; **App Catalog**, then click **Add**.

3.  From the search menu list, select the Apple App Store.

4.  In the search bar, type `ServiceNow`.

5.  Select the ServiceNow app from the results.

6.  Click **Next**.

7.  Describe and add screenshots of the app.

8.  Select a distribution level for this configuration of the app.

    -   Everyone: The app is added to all user-compatible devices.
    -   No one: The app is staged for distribution at a later date.
    -   Custom: The app is distributed only to users or groups you choose.
9.  Click **Next**.

10. In the App Configuration section, click the add icon \(![MobileIron add icon](../image/MIPlusIcon.png)\) next to **iOS Managed App Configuration**.

11. In the **Name** field, enter a name for the configuration, for example, Default Instance.

12. Enter the key and value pairing.

    |Field|Description|
    |-----|-----------|
    |Key|SNDefaultInstanceURL|
    |Value|The URL for the instance, for example, `https://<instance name>.service-now.com/` .|

13. Set a distribution level for this configuration of the app.

    -   Everyone: The app is added to all user-compatible devices.
    -   No one: The app is staged for distribution at a later date.
    -   Custom: The app is distributed only to users or groups you choose.
14. Click **Next**.

15. Click **Done**.


## Result

The ServiceNow app for iOS appears in the App Catalogs section on the MobileIron Portal. Mobile users can download it from the MobileIron App Catalog.

**Parent Topic:**[MobileIron Mobile Device Management \(MDM\)](../concept/mobileiron-mdm.md)

