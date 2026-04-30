---
title: View KPI Signals
description: Access KPI Signals from the KPI Details page.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [KPI Signals, Platform Analytics]
---

# View KPI Signals

Access KPI Signals from the KPI Details page.

## Before you begin

Role required: Any roles necessary to access the workspace. The access control lists \(ACLs\) for indicators and breakdowns are also respected.

## Procedure

1.  Open KPI Details for an indicator as described in [View KPI Details](../../performance-analytics/task/view-kpi-details.md).

2.  Open the **Filters** \(![](../image/filter-icon.png)\) panel and select one breakdown and one element.

    KPI Signals can monitor each first-level breakdown and element applied to an indicator. It cannot monitor second-level breakdowns.

    **Note:** In the context of KPI Signals, the term KPI refers to an indicator with optionally a first-level breakdown and element.

3.  Select the Open KPI Signals icon.

    ![](../image/open-kpi-signals-icon.png)

    The KPI Signals panel opens.

4.  If KPI Signals monitoring is not active for this KPI, you can follow the instructions in [Activate KPI Signals monitoring for an indicator \(KPI\)](activate-signals-monitor.md).

    If you do not have a role that allows you to activate KPI Signals monitoring for a KPI, contact an administrator instead.


## KPI Signals with a breakdown element

In the following example, you see the KPI Signals panel for the Number of open incidents indicator. This indicator is filtered on the Priority: 1 - Critical breakdown element. No signals have been detected.

![KPI Signals panel with one breakdown and element filtering the indicator](../image/kpi-signals-one-element.png)

