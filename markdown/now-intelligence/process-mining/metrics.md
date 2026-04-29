---
title: Set metrics
description: Set the metrics to evaluate the process better and improve the process efficiency.
locale: en-US
release: australia
product: Process Mining
classification: process-mining
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Scoping your analysis, Create a project or template using Project Builder, Use, Process Mining, Platform Analytics]
---

# Set metrics

Set the metrics to evaluate the process better and improve the process efficiency.

## Before you begin

Role required: sn\_process\_mining\_analyst, sn\_process\_mining\_power\_user, or sn\_process\_mining\_admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Process Mining Workspace**.

    If you continue from the **Set Objectives** page, you are on the **Scope your analysis** page.

2.  Select **Edit** for the project that you want to edit.

3.  Select the edit button for the **Scope your analysis** section.

4.  Select **Metrics** from the left bar.

    **Note:** The touchpoint and idle time metrics are not available in the Classic view.

    ![Set metrics](../image/metrics-project.png)

    There are two types of metrics:

    -   **Touchpoint metrics**: Touchpoint metrics are used to study specific interactions within a process to identify areas of high interaction, particularly spotlighting inefficient, redundant, or excessive activities. By pinpointing these areas, it enables process optimization through automation or other improvements, enhancing performance and reducing operational costs.
    -   **Idle time metrics**: Idle time metrics help track the duration when cases are awaiting assignment to agents but are expected to progress by the provider. These metrics identify delays during unassigned periods, highlighting inefficiencies where cases are stagnant in the process. By analyzing idle time, teams can improve task allocation and resource management, reducing delays and ensuring smooth case flow, ultimately boosting productivity and compliance with service level agreements.

        **Note:** If a field that is selected in the promin.blocked.tables list is selected in the Process details page, then the Idle time metrics is not available.

5.  Toggle each of the metrics to enable them.

    The fields that you have set for these metrics in the process configuration for the parent table, are include in the project.

    **Note:** These two metrics are not available without configuring in process configuration.

6.  Select **Set improvement opportunities**.


**Parent Topic:**[Scoping your analysis](../concept/scope-analysis.md)

