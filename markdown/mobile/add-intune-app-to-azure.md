---
title: Add an Intune integrated app to Microsoft Azure
description: Configure your ServiceNow app for distribution with Microsoft Intune.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Intune mobile device management \(MDM\), Supported mobile device management vendors, Considerations before implementation, ServiceNow Mobile Platform configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Add an Intune integrated app to Microsoft Azure

Configure your ServiceNow app for distribution with Microsoft Intune.

## Before you begin

Role required: Microsoft Intune admin

## Procedure

1.  Log in to the Microsoft Endpoint Manager admin center at `https://endpoint.microsoft.com`.

2.  In the menu on the left side of the screen, navigate to **Apps**.

    ![Microsoft Endpoint Manager admin center menu showing the 'Apps' option.](../image/intune-mdm-config-select-apps.png)

3.  On the Apps page, select **All apps** &gt; **Add**.

    ![Microsoft Endpoint Manager admin center showing the 'Add' apps option.](../image/intune-mdm-config-add-apps.png)

4.  Select the app type and then click **Select**.

    ![Microsoft Endpoint Manager admin center showing where to select the app type.](../image/intune-mdm-config-select-app-type.png)

5.  Select **Search the App Store**.

    ![Microsoft Endpoint Manager admin center showing how to search the App Store for a ServiceNow mobile app.](../image/intune-mdm-config-search-app-store.png)

6.  Select the ServiceNow mobile app that you want to add.

7.  On the App information tab in the Add App page, the application details automatically populate. Add additional information as appropriate and select **Next**.

8.  On the Assignments tab, add the specific groups or all users who will be using this app.

    ![Microsoft Endpoint Manager admin center Assignments tab.](../image/intune-mdm-config-add-assignments.png)

9.  Click **Next**.

10. Review the information you entered. When you are finished, click **Create**.


**Parent Topic:**[Intune mobile device management \(MDM\)](../concept/intune-mdm.md)

