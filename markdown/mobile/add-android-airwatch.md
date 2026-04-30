---
title: Add the ServiceNow app for Android to Workspace ONE UEM
description: Configure the ServiceNow app for Android for Workspace ONE UEM distribution.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Workspace ONE UEM Mobile Device Management \(MDM\), Supported mobile device management vendors, Considerations before implementation, ServiceNow Mobile Platform configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Add the ServiceNow app for Android to Workspace ONE UEM

Configure the ServiceNow app for Android for Workspace ONE UEM distribution.

## Before you begin

Role required: admin

## Procedure

1.  Sign in to the Workspace ONE UEM portal.

2.  Navigate to **Apps &amp; Books** &gt; **Applications** &gt; **Native** &gt; **Public**.

3.  Click **Add Application**.

4.  In the Platform field, select **Android**.

5.  In the Source field, select **Search App Store** then search for **ServiceNow**.

    If the search cannot find the ServiceNow application, the app might not be approved for your organization. You can [approve the app in the Google Play store](approve-app-google.md).

6.  Next to the ServiceNow App search result, click **Select**.

7.  Click **Save &amp; Assign**.

8.  Click **Add Assignment**.

9.  Click **Assignment Group**.

10. From the Assignment Group list, select **Application Configuration Policy**.

11. From the Application Configuration field, select **Enabled**.

12. In the Application Configuration section, enter the following information.

    |Field|Description|
    |-----|-----------|
    |Title|Server URL|
    |Description|The full ServiceNow instance URL|
    |Value|`https://<instance name>.service-now.com/`|

    ![Application Configuration page for Workspace ONE UEM](../image/AWAndroidAppConfig.png "Workspace ONE UEM configuration")

13. Click **Add**.

14. Click **Save &amp; Publish**.

15. Click **Publish**.


## Result

After adding the app to Workspace ONE UEM, it appears in the **Apps &amp; Books** &gt; **Applications** &gt; **Native** &gt; **Public** section of the Workspace ONE UEM portal. Mobile users can download the app from the Workspace ONE UEM App Catalog app.

If your instance is on an internal network, you might need to configure the VPN. For more information on configuring the VPN, see the Workspace ONE UEM documentation on [Configure Tunnel Profile for Android](https://docs.vmware.com/en/VMware-Workspace-ONE-UEM/2306/Tunnel_Linux/GUID-AWT-CONFIGURE-PAT-ANDROID.html?hWord=N4IghgNiBcIMYHsB2AzAlgcwK4CcCmABAG4AOSBKCOBYSAJjgmnQXXkWnHiAL5A).

For more information on app distribution with Workspace ONE UEM, see the [official Workspace ONE UEM documentation](https://docs.vmware.com/en/VMware-Workspace-ONE-UEM/index.html).

**Parent Topic:**[Workspace ONE UEM Mobile Device Management \(MDM\)](../concept/airwatch-mdm.md)

