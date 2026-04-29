---
title: Send campaign notifications automatically in Microsoft Teams
description: Automatically send campaign notifications in Microsoft Teams for better collaboration and efficient communication.
locale: en-US
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Working on campaigns in Microsoft Teams, Integration for Employee Experience, Setup for integrating self-configured apps, Setup the Servicenow instance, Integrating ServiceNow with Microsoft Teams and Microsoft 365, ServiceNow for Microsoft Teams and Microsoft 365, Unified Employee Experience, Employee Service Management]
---

# Send campaign notifications automatically in Microsoft Teams

Automatically send campaign notifications in Microsoft Teams for better collaboration and efficient communication.

## Before you begin

A manifest file to enable the campaign notification display in Microsoft Teams must exist.

If the configured Employee Center version is v.24 or above, then the Employee Center tab is present by default in your Microsoft Teams application. If the Employee Center version is lower than v.24, you must update the value of the portal in the `sn_now_teams.portal.suffix` property to `esc`. This value enables Employee Center in your instance.

Role required: admin

## About this task

## Procedure

1.  Navigate to **All** &gt; **ServiceNow for Microsoft 365** &gt; **Application Manifest** &gt; **ServiceNow for Teams**.

2.  Select **New**.

3.  Fill in the details in the **Generic Info** section.

    Select **Submit** and then select **Next**.

4.  Fill in the details in the **Configure Virtual Agent** section and select **Next**.

5.  In the **Configure Tab** section, verify that **Enable activity feed** is selected and select **Next**.

    **Note:** If you are modifying the base system manifest file, select **Enable activity feed** to receive notifications for campaigns.

6.  Verify the details in the **Ready** section and select **Download Manifest**.

    Manifest file downloads in the zip format.

7.  Upload the manifest file in Microsoft Teams.

    For more information about creating a manifest file, see [Create and download the manifest file for self-configured apps](download-manifest-file-st.md#). For more information about uploading a manifest file, see [Upload manifest file in Microsoft Teams](upload-manifest-ms-teams.md).


**Parent Topic:**[Working on campaigns in Microsoft Teams](../concept/using-campaigns-ms-teams.md)

