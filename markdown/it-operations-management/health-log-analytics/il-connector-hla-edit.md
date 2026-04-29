---
title: Edit an installed integration in Health Log Analytics
description: Edit an installed integration for streaming log data to Health Log Analytics on the Integrations Launchpad. For example, you can switch to a different service instance.
locale: en-US
release: australia
product: Health Log Analytics
classification: health-log-analytics
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [editing, data input, integrations, ServiceNow, Health Log Analytics, HLA]
breadcrumb: [Set up integrations from Integrations Launchpad, Set up HLA on your instance, Configuring, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Edit an installed integration in Health Log Analytics

Edit an installed integration for streaming log data to Health Log Analytics on the Integrations Launchpad. For example, you can switch to a different service instance.

## Before you begin

Role required: evt\_mgmt\_admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

2.  From the bottom of the navigation pane, select the AIOps configuration center icon ![ITOM AIOps configuration center icon](../image/icon-itom-aiops-config.png).

    The ITOM AIOps configuration center page appears. The configuration center is a centralized workspace. Use it to configure and manage AIOps features from a single place.

3.  From the Integrate section, under Integrations, select **Manage installed integrations**.

    The Integrations Launchpad appears.

4.  In the **Installed integrations** tab, search for and select the tile for the integration you want to edit.

5.  Select a tab that you want to edit.

6.  Select **Deactivate** to deactivate the integration.

    **Note:** You must deactivate the integration before you can edit it.

7.  Select **Edit**.

8.  Edit the integration per your requirements.

9.  Select **Test and save**.

    Health Log Analytics tests the MID Server connectivity, returning either success or an error. If an error is returned, make adjustments to your configuration as suggested on the screen, and then select **Test and save** again. When the test is successful, you can reactivate the integration.

10. Select **Activate**.


**Parent Topic:**[Set up Health Log Analytics on your ServiceNow instance](../concept/hla-implement.md)

