---
title: Priority group
description: For better triage and focus, alerts that have a higher priority are brought to the top of the alert list. This placement brings to your attention those alerts that require you to handle them at a higher priority than other alerts.
locale: en-US
release: zurich
product: Event Management
classification: event-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [View alert information, Using Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Priority group

For better triage and focus, alerts that have a higher priority are brought to the top of the alert list. This placement brings to your attention those alerts that require you to handle them at a higher priority than other alerts.

The priority group indicates which alerts should be attended to first. Priority is [calculated](alert-priority.md) for each open alert and then mapped into one of four priority categories.

## Thresholds

Thresholds on the calculated priority are used to determine to which category the alert is mapped to. Alerts with a priority above the value of the **evt\_mgmt.top\_priority\_group\_threshold** property are categorized as **Urgent**, which is the highest priority. The default value of this threshold is 1M.

## Priority group categories

The priority groups into which alerts fall are listed in the following table.

|Priority group|Icon|
|--------------|----|
|Urgent|![Urgent priority](../image/priority-urgent.png)|
|High|![High priority](../image/priority-high.png)|
|Moderate|![Moderate priority](../image/priority-moderate.png)|
|Low|![Low priority value](../image/priority-low.png)|

The value of the alert priority group is more meaningful than the alert severity on its own. For example, an alert with a severity of Major, may not be in need of resolution ahead of an alert whose priority is Critical. The combined group priority value takes the weight of each factor into account, giving you a better indication of which alert to attend to first.

The alert priority group is available in alert lists in the Dashboard, Alert Intelligence, and All Alerts page. For example, in the **All Alerts** list, the alert priority group is displayed as depicted in the following image.

![Alert priority group](../image/alert-priority-group.png)

## Triggers that cause recalculation

Changes to open alerts trigger the recalculation of the priority and then the alert is again categorized into the relevant priority group. Closed alerts are not considered for alert priority group calculation.

**Parent Topic:**[View alert information](../task/t_EMViewAlert.md)

**Related topics**  


[Alert priority](alert-priority.md)

