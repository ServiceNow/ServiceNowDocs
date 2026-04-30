---
title: Create an incident from an alert with Now Assist in Express List
description: Create an incident with a human-readable, AI-generated description from the Express List pane by using Now Assist.
locale: en-US
release: zurich
product: Now Assist for IT Operations Management
classification: now-assist-for-it-operations-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
keywords: [Generative AI for IT Operations Management, generative AI for ITOM, create an incident, alert, Express List, Now Assist]
breadcrumb: [Use generative AI, Now Assist for ITOM, IT Operations Management]
---

# Create an incident from an alert with Now Assist in Express List

Create an incident with a human-readable, AI-generated description from the Express List pane by using Now Assist.

## Before you begin

**Note:** Currently, Now Assist for ITOM only supports tag-based, CMDB, Log Analytics, Mixed, Automated, and Network Traffic-based alert groups. For all other alert group types, it only analyzes the parent alert.

Role required: evt\_mgmt\_operator, evt\_mgmt\_admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

2.  From the navigation bar, select the Express list icon: ![Express list icon](../../event-management/image/express-list1.png).

3.  Create an incident from a selected alert.

    1.  In the Express List pane, select the check box for the desired alert.

        **Note:** To display the individual alerts inside a group, select the chevron icon \(![Chevron icon.](../../service-operations-workspace-itom/image/icon-chevron.png)\) at the beginning of the alert group row.

    2.  Select the **Alert actions** drop-down list.

        ![Alert actions drop down arrow](../../service-operations-workspace-itom/image/alert-actions-tool-tip.png)

    3.  Under **Response actions**, select **Create Incident with Now Assist**.

    An incident with a human-readable, AI-generated description is created from the selected alert and a confirmation message is displayed.


**Parent Topic:**[Use generative AI in Now Assist for ITOM](../concept/now-assist-itom-use.md)

