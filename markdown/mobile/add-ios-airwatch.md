---
title: Add the ServiceNow app for iOS to Workspace ONE UEM
description: Configure the ServiceNow app for iOS for Workspace ONE UEM distribution.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Workspace ONE UEM, Device management, Before implementation, Configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Add the ServiceNow app for iOS to Workspace ONE UEM

Configure the ServiceNow app for iOS for Workspace ONE UEM distribution.

## Before you begin

Role required: admin

## Procedure

1.  Sign in to the Workspace ONE UEM portal.

2.  Navigate to **Apps &amp; Books** &gt; **Applications** &gt; **Native** &gt; **Public**.

3.  Click **Add Application**.

4.  In the Platform field, select **Apple iOS**.

5.  In the Source field, select **Search App Store** then search for **ServiceNow**.

6.  Next to the ServiceNow App search result, click **Select**.

7.  Click **Save &amp; Assign**.

8.  Click **Add Assignment**.

9.  Click **Assignment Group**.

10. From the Assignment Group list, select **Application Configuration Policy**.

11. From the Application Configuration field, select **Enabled**.

12. In the Application Configuration section, enter the following information.

    |Field|Description|
    |-----|-----------|
    |Configuration key|SNDefaultInstanceURL|
    |Value type|String|
    |Configuration value|`https://<instance name>.service-now.com/`|

    ![Application Configuration page for Workspace ONE UEM](../image/AWiOSAppConfig.png "App Workspace ONE UEM configuration")

13. Click **Add**.

14. Click **Save &amp; Publish**.

15. Click **Publish**.


## Result

After adding the app to Workspace ONE UEM, it appears in the **Apps &amp; Books** &gt; **Applications** &gt; **Native** &gt; **Public** section of the Workspace ONE UEM portal. Mobile users can download the app from the Workspace ON UEM App Catalog app.

**Parent Topic:**[Workspace ONE UEM Mobile Device Management \(MDM\)](../concept/airwatch-mdm.md)

