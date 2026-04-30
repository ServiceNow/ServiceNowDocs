---
title: Add the ServiceNow app to Citrix XenMobile
description: Configure the ServiceNow for Cetrix XenMobile distribution.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Citrix XenMobile, Supported mobile device management vendors, Considerations before implementation, ServiceNow Mobile Platform configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Add the ServiceNow app to Citrix XenMobile

Configure the ServiceNow for Cetrix XenMobile distribution.

## Before you begin

Role required: admin

## Procedure

1.  Sign in to the XenMobile console.

2.  Click **Configure** &gt; **Apps**.

3.  Click **Add**, then choose **Public App Store**.

4.  In the App Information pane, complete the following information.

    |Field|Description|
    |-----|-----------|
    |**Name**|Type a descriptive name for the app. The name appears under App Name on the apps table.|
    |**Description**|Type an optional description of the app.|
    |**App category**|In the list, click the category you want to add the app to.|

5.  Click **Next**.

6.  Under Platform, select the following platforms, or the platforms that are applicable to your distribution plan.

    -   iPhone
    -   iPad
    -   Android for Work
7.  For each of the platforms, complete the following steps.

    1.  In the search bar, search for `ServiceNow`.

    2.  Click the ServiceNow tile.

        The App Details fields are pre-populated with information related to the app.

    3.  Configure the deployment rule depending on your organizations deployment plan.

    4.  Click **Next**.

    If Android for Work cannot find the ServiceNow application, the app might not be approved for your organization. You can [approve the app in the Google Play store](approve-app-google.md).

    If the search results still do not display in Citrix, click **Didn't find the app you were looking for?** then enter the URL for the app: `https://play.google.com/work/apps/details?id=com.servicenow.servicenow`.

8.  Click **Next**.

9.  From the Approvals page, configure the workflow for your company.

    You only need to use workflows when you need approval when creating user accounts. If you do not need to set up approval workflows, skip to the next step. For more information on configure workflows for Citrix, see the [Citrix product documentation](https://docs.citrix.com/en-us/xenmobile/server/apps.html).

10. From the Delivery Group Assignments page, select the delivery groups for users that you want to have the ServiceNow application. You can also configure a deployment schedule.


## What to do next

After successfully adding the ServiceNow app from the iOS store platforms, install the ServiceNow application from the Citrix Hub app from your devices. For Android, the ServiceNow app appears in the Google Play Store managed by your Android Work Profile.

**Parent Topic:**[Citrix XenMobile](../concept/citrix-mdm.md)

