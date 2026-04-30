---
title: Send automatic campaign notifications in Microsoft Teams
description: Automatically send campaign notifications in Microsoft Teams for better collaboration and efficient communication.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Sending notifications to employees using Microsoft Teams, Integration for Employee Experience, Setup for integrating pre-published apps, Setup the Servicenow instance, Microsoft Teams and Microsoft 365, Integrate, ServiceNow for Microsoft Teams and Microsoft 365, Employee Service Management]
---

# Send automatic campaign notifications in Microsoft Teams

Automatically send campaign notifications in Microsoft Teams for better collaboration and efficient communication.

## Before you begin

After the upgrade process for a pre-published app configuration, you must reauthorize the SSO and Activity notifications application to enable your ServiceNow instance to make API calls to Microsoft Azure. ServiceNow for Microsoft Teams application work flow is then enabled and your consent for the new API permissions is ensured. For more information, see [Grant permissions to required Microsoft Azure apps](authorize-multi-tenant-apps-mt.md).

A manifest file to enable the campaign notification display in Microsoft Teams must exist.

If the configured Employee Center version is v.24 or above, then the Employee Center tab is present by default in your Microsoft Teams application. If the Employee Center version is lower than v.24, you must update the value of the portal in the `sn_now_teams.portal.suffix` property to `esc`. This value enables Employee Center in your instance.

Ensure that you enter the app ID of ServiceNow for Microsoft 365 in the **sn\_now\_azure.teams\_installed\_app\_id** system property. You can get the app ID from the Microsoft Teams admin center.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **ServiceNow for Microsoft 365** &gt; **Application Manifest** &gt; **ServiceNow for Teams**.

2.  Select **New**.

3.  Fill in the details in the **Generic Info** section.

    Select **Submit** and then select **Next**.

4.  Fill in the details in the **Configure Virtual Agent** section and select **Next**.

5.  In the **Configure Tab** section, verify that **Enable activity feed** is selected and select **Next**.

    **Note:** If you are modifying a base system manifest file, select **Enable activity feed** to receive notifications for campaigns.

6.  Verify the details in the **Ready** section and select **Download Manifest**.

    The manifest file downloads in zip format.

7.  Upload the manifest file in Microsoft Teams.

    For more information about creating a manifest file, see [Create and download the manifest file for pre-published apps](download-manifest-file-mt.md). For more information about uploading a manifest file, see [Upload manifest file in Microsoft Teams](upload-manifest-ms-teams.md).


**Parent Topic:**[Sending notifications to employees using Microsoft Teams](../concept/using-campaigns-ms-teams-mt.md)

