---
title: Edit installed integrations
description: Edit an installed integration for streaming log data to Health Log Analytics on the Integrations Launchpad. For example, you can switch to a different service instance.
locale: en-US
release: xanadu
product: Health Log Analytics
classification: health-log-analytics
topic_type: task
last_updated: "2024-12-01"
reading_time_minutes: 1
keywords: [editing, data input, integrations, ServiceNow, Health Log Analytics, HLA]
breadcrumb: [Set up integrations from Integrations Launchpad, Health Log Analytics data input setup, Configuring Health Log Analytics, Health Log Analytics, ITOM Health, IT Operations Management]
---

# Edit installed integrations

Edit an installed integration for streaming log data to Health Log Analytics on the Integrations Launchpad. For example, you can switch to a different service instance.

## Before you begin

Role required: evt\_mgmt\_admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

2.  From the left pane, select the Integrations Launchpad icon \(![Integration Launchpad icon](../../service-operations-workspace-itom/image/integrations-launchpad.png)\)

3.  In the **Installed integrations** tab, search for and select the tile for the integration you want to edit.

4.  Select a tab that you want to edit.

5.  Select **Deactivate** to deactivate the integration.

    **Note:** You must deactivate the integration before you can edit it.

6.  Select **Edit**.

7.  Edit the integration per your requirements.

8.  Select **Test and save**.

    Health Log Analytics tests the MID Server connectivity, returning either success or an error. If an error is returned, make adjustments to your configuration as suggested on the screen, and then select **Test and save** again. When the test is successful, you can reactivate the integration.

9.  Select **Activate**.


**Parent Topic:**[Set up integrations from Integrations Launchpad](../concept/hla-data-input-setup-integrations.md)

