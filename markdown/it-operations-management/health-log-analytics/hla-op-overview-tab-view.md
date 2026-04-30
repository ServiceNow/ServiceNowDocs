---
title: Start remediation of a Log Analytics alert from the Overview tab
description: Begin the remediation process of a Log Analytics alert from the alert Overview tab. This tab provides information on the alert, the log data associated with the anomalous behavior, CIs associated with the alert, and services impacted by it.
locale: en-US
release: zurich
product: Health Log Analytics
classification: health-log-analytics
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Analyzing and resolving alerts, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Start remediation of a Log Analytics alert from the Overview tab

Begin the remediation process of a Log Analytics alert from the alert **Overview** tab. This tab provides information on the alert, the log data associated with the anomalous behavior, CIs associated with the alert, and services impacted by it.

## Before you begin

**Important:** From the Vancouver release onward, the **Operator Workspace** is deprecated and replaced with Service Operations Workspace.

Role required: evt\_mgmt\_operator, or evt\_mgmt\_user, or evt\_mgmt\_admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

2.  In the Service Operations Workspace, select the lists icon \(![Lists icon.](../image/icon-lists-sow.png)\).

3.  Select the appropriate list in the Alerts sub-list and navigate to the relevant alert or group.

    All Health Log Analytics alerts have the value **Log Analytics** in the **Source** column. The value in the **Group** column identifies the type of Log Analytics alert. See [Types of Health Log Analytics alerts](../reference/hla-op-log-analytics-alert-types.md) for a more detailed description of each type of alert or group.

    **Tip:** To preview an alert in the list, click its info icon \(![Info icon.](../image/icon-info.png)\).

4.  Select the alert number.

    The **Overview** tab displays.

5.  View the section of the **Overview** tab that provides the information that you need.

    For a description of the sections and cards, see [Sections and cards on the alert Overview tab in Health Log Analytics](../../health-log-analytics-admin/concept/hla-alert-overview-tab.md).

    **Note:** Because some sections on the **Overview** tab show only a portion of the information, many sections include a link that displays different or more complete information.

6.  Run predefined remediation tasks to resolve alert issues.

    1.  Select **Launch playbook**.
    2.  Select the **Playbook** tab.

        The **Run remediation** card displays the available remediation actions.

    3.  Select the tile corresponding to the action you want to run.
    When the action is complete, it appears in the **Completed** card.


**Parent Topic:**[Analyzing and resolving Log Analytics alerts](../concept/hla-analyzing-resolving-hla-alert.md)

