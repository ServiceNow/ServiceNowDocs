---
title: Add the ServiceNow app for Android to the IBM MaaS360 portal
description: Configure the ServiceNow app for Android for IBM MaaS360 distribution.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [IBM MaaS360, Device management, Before implementation, Configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Add the ServiceNow app for Android to the IBM MaaS360 portal

Configure the ServiceNow app for Android for IBM MaaS360 distribution.

## Before you begin

Role required: admin

## Procedure

1.  Sign in to the IBM MaaS360 portal.

2.  From the portal homepage, navigate to **Apps** &gt; **Catalog**.

3.  Click **Add** to display the list of apps.

4.  Select the Google Play App.

5.  In the App Details tab, type `ServiceNow` into the app field.

6.  Select the ServiceNow app from the results.

7.  In the Policies and Distribution tab, select the applicable policies.

8.  In the Configuration tab, select the **Configure App Settings** checkbox.

9.  In the Server URL field, enter the full URL for the instance.

    For example, `https://<instance name>.service-now.com/`.

10. Click **Add**.


## Result

After adding the ServiceNow app from the Google Play store, it appears in the App Catalog application. Users can download the app to their Android devices.

If your instance is on an internal network, you might need to configure the VPN. For more information on configuring the VPN, see the IBM MaaS360 documentation on the [Maas360 VPN module](https://www.ibm.com/support/knowledgecenter/SS8H2S/com.ibm.mc.doc/ce_source/concepts/ce_vpn_overview.htm).

For more information on app distribution, see the following IBM documentation for each operating system.

-   [Add an iTunes App Store app to the App Catalog](https://www.ibm.com/support/knowledgecenter/SS8H2S/com.ibm.mc.doc/pag_source/tasks/pag_apps_add_itunes.htm)
-   [Add a Google Play app to the App Catalog](https://www.ibm.com/support/knowledgecenter/SS8H2S/com.ibm.mc.doc/pag_source/tasks/pag_apps_add_google_play.htm)

**Parent Topic:**[IBM MaaS360 mobile device management \(MDM\)](../concept/IBM-MaaS360-mdm.md)

