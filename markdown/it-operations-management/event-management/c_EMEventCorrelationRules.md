---
title: Rule-based alert grouping
description: Rule-based alert grouping is created by alert correlation rules. These rules allow you to manually classify alerts as primary or secondary and establish a relationship between them. Use alert correlation rules to group related alerts. The rule runs only for new alerts or alerts whose status changed from close/flapping to open/reopen.
locale: en-US
release: xanadu
product: Event Management
classification: event-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Alert grouping types, Alert grouping, Configuring Event Management, Event Management, ITOM Health, IT Operations Management]
---

# Rule-based alert grouping

Rule-based alert grouping is created by alert correlation rules. These rules allow you to manually classify alerts as primary or secondary and establish a relationship between them. Use alert correlation rules to group related alerts. The rule runs only for new alerts or alerts whose status changed from close/flapping to open/reopen.

Example: If rule-based alert grouping is applied, secondary alerts indicating that virtual machines or applications on the offline server are also down and are grouped under the primary alert, which is the root alert for the server that is offline. You can view rule-based alert grouping in Express List of Service Operations Workspace \(ITOM\). For more information, see [Viewing links between alerts in rules-based alert groups](../../service-operations-workspace-itom/concept/el-rule-based-link-view.md).

## Primary and secondary alerts

-   Primary alert: Identifies the root cause of an alert group and represents its secondary alerts.
-   Secondary alert: Related to the same issue, they are grouped under the primary alert. The purpose of secondary alerts is to determine which alerts to suppress, reducing alert noise and allowing you to focus on the primary alert.

## How primary and secondary alerts interact

In rule-based alert grouping, one of the real alerts is designated as the primary alert. Primary and secondary alert filter conditions specify which alerts are classified as primary and which as secondary. The filter criteria are applied to the Alert \[em\_alert\] table.

In this alert grouping, both primary and secondary alerts are visible but secondary alerts are grouped under the primary alert. The property **Keep the secondary alert open even when primary closed. for manual or rule based** \(**evt\_mgmt.rule\_based\_manual\_closure**\) controls whether secondary alerts remain open or are closed when the primary alert is closed.

If the property is not selected \(i.e., set to No\), after the primary alert is closed, the parent reference is removed from the secondary alerts \(the grouping is dissolved\), and the secondary alerts are closed and become stand-alone. If you select the checkbox for the property \(i.e., set it to Yes\) and the primary alert is closed, the parent reference is removed from the secondary alerts \(the grouping is dissolved\), causing them to become stand-alone open alerts.

## Example: Alert hierarchy

Only one level of secondary alerts is permitted. In situations where a secondary alert has its own secondary alert, the Event Management application flattens the hierarchy to preserve only two levels.

For example, assume alert A is the primary alert and alert B is the secondary alert. If alert C becomes a secondary alert for alert B, the application flattens the hierarchy so that A remains the primary and B and C become sibling secondary alerts, one level below A.

As another example, assume that there are three correlation rules that produce the following results:

-   Rule 1 \(with an Order value of 1\): B becomes a primary alert for A.
-   Rule 2 \(with an Order value of 2\): A becomes a primary alert for C and D.
-   Rule 3 \(with an Order value of 3\): E becomes a primary alert for A.

When alerts B, C, D, and E are triggered, they all appear in the alert list separately because there are no correlations between them.

When alert A is triggered:

1.  Rule 1 makes A a secondary alert under alert B.
2.  Rule 2 makes both C and D secondary alerts under alert A, and the hierarchy is flattened so that A, C, and D become secondary alerts to the primary alert B.
3.  Rule 3 is not applied because multiple parents are not allowed—A already has B as its primary.

Therefore, if all alerts are triggered, only B appears as the primary alert for A, D, and C, while E remains a standalone alert.

-   **[Create an alert correlation rule](../task/t_EMConfigureAnEventCorrelationRule.md)**  
Create an alert correlation rule to designate primary and secondary alerts. The primary alert is identified as the root cause of the alert group and the secondary alerts are grouped under the primary alert.

**Parent Topic:**[Configuring Event Management](using-event-management.md)

