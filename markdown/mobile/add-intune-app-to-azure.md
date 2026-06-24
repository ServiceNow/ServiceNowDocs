---
title: Add an Intune integrated app to Microsoft Azure
description: Configure your ServiceNow app for distribution with Microsoft Intune.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/mobile/add-intune-app-to-azure.html
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Intune, Device management, Considerations before implementation, Configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Add an Intune integrated app to Microsoft Azure

Configure your ServiceNow app for distribution with Microsoft Intune.

## Before you begin

Role required: Microsoft Intune admin

## Procedure

1.  Log in to the Microsoft Endpoint Manager admin center at `https://endpoint.microsoft.com`.

2.  In the menu on the left side of the screen, navigate to **Apps**.

    \[Omitted image "intune-mdm-config-select-apps.png"\] Alt text: Microsoft Endpoint Manager admin center menu showing the 'Apps' option.

3.  On the Apps page, select **All apps** &gt; **Add**.

    \[Omitted image "intune-mdm-config-add-apps.png"\] Alt text: Microsoft Endpoint Manager admin center showing the 'Add' apps option.

4.  Select the app type and then click **Select**.

    \[Omitted image "intune-mdm-config-select-app-type.png"\] Alt text: Microsoft Endpoint Manager admin center showing where to select the app type.

5.  Select **Search the App Store**.

    \[Omitted image "intune-mdm-config-search-app-store.png"\] Alt text: Microsoft Endpoint Manager admin center showing how to search the App Store for a ServiceNow mobile app.

6.  Select the ServiceNow mobile app that you want to add.

7.  Add additional information as appropriate on the App information tab in the Add App page, and select **Next**.

8.  On the Assignments tab, add the specific groups or all users who will be using this app.

    \[Omitted image "intune-mdm-config-add-assignments.png"\] Alt text: Microsoft Endpoint Manager admin center Assignments tab.

9.  Click **Next**.

10. Review the information you entered and when you are finished, click **Create**.


**Parent Topic:**[Intune mobile device management \(MDM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/mobile/intune-mdm.md)

