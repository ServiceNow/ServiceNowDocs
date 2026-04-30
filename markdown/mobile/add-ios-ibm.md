---
title: Add the ServiceNow app for iOS to the IBM MaaS360 portal
description: Configure the ServiceNow app for iOS for IBM MaaS360 distribution.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [IBM MaaS360 mobile device management \(MDM\), Supported mobile device management vendors, Considerations before implementation, ServiceNow Mobile Platform configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Add the ServiceNow app for iOS to the IBM MaaS360 portal

Configure the ServiceNow app for iOS for IBM MaaS360 distribution.

## Before you begin

Role required: admin

## Procedure

1.  Sign in to the IBM MaaS360 portal.

2.  From the portal homepage, navigate to **Apps** &gt; **Catalog**.

3.  Click **Add** to display the list of apps.

4.  Select the Apple App Store App.

5.  In the App Details tab, type `ServiceNow` into the app field.

6.  Select the ServiceNow app from the results.

    ![Select the app from the search results](../image/imb-6.png)

7.  In the Policies and Distribution tab, select the applicable policies.

8.  In the Configuration tab, in the App Config Source list, select **Key/Value**.

9.  In the Key/Value section add the following information.

    |Field|Description|
    |-----|-----------|
    |Attribute name|SNDefaultInstanceURL|
    |Attribute value|The full URL for the instance. For example, `https://<instance name>.service-now.com/`|

10. Click **Add**.


## Result

After adding the ServiceNow app from the Apple store, it appears in the App Catalog application. Users can download the app to their iOS devices.

**Parent Topic:**[IBM MaaS360 mobile device management \(MDM\)](../concept/IBM-MaaS360-mdm.md)

