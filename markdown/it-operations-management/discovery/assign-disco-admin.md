---
title: Assign Discovery admins
description: Assign the discovery\_admin role to users who will be in charge of Discovery configuration and operational control.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/discovery/assign-disco-admin.html
release: australia
product: Discovery
classification: discovery
topic_type: task
last_updated: "2026-04-28"
reading_time_minutes: 1
keywords: [ITOM, user roles, Now Assist]
breadcrumb: [ITOM Configuration Console, Discovery setup, Configuring Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Assign Discovery admins

Assign the discovery\_admin role to users who will be in charge of Discovery configuration and operational control.

## Before you begin

Verify the following:

-   You're using the Zurich Patch 8 or later version of the ServiceNow AI Platform.
-   You have installed the ITOM Visibility plugin. For more information, see [Install ITOM Visibility using Setup Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-visibility/install-nowassist-setup-itom-visibility.md).
-   You have installed the Now Assist for IT Operations Management plugin. For more information, see [Install Now Assist for IT Operations Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/install-na-itom.md).
-   You're on the Configure IT Operations Management page of the Configuration Console. For more information, see [Access the ITOM Configuration Console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/access-itom-config-console-disco.md).

Role required: admin

## About this task

The discovery\_admin role provides users with the necessary permissions to configure and manage Discovery settings, including MID Servers, credentials, IP ranges, and Discovery schedules.

## Procedure

1.  Navigate to **Configuration Summary** &gt; **Discovery** &gt; **Platform foundations**.

2.  Expand **Platform foundations**.

3.  Select **Assign Discovery admins**.

4.  In the **User** field, select the user to assign the role to.

    The **Role** field is read-only and displays discovery\_admin.

5.  Select **Assign role**.

    The role is assigned to the selected user.

6.  To complete the setup, select **Mark as configured**.


