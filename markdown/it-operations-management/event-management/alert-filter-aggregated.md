---
title: Apply alert group filters to aggregated groups
description: Reduce noise by locating only aggregated alert groups that match a configured filter. Aggregated groups are groups created for alerts with identical CIs and pattern identifiers.
locale: en-US
release: zurich
product: Event Management
classification: event-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure filters for automatic alert groups, Scheduled jobs and parameters for alert grouping, Alert grouping, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Apply alert group filters to aggregated groups

Reduce noise by locating only aggregated alert groups that match a configured filter. Aggregated groups are groups created for alerts with identical CIs and pattern identifiers.

## Before you begin

**Note:** This procedure is relevant for advanced configuration only.

Role required: evt\_mgmt\_admin

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **Administration** &gt; **Automatic Group Filters**.

2.  On the Automatic Group Filters page, add the **Aggregated** column.

    1.  Select the Personalize List icon \( ![Personalize List icon](../../cloud-management-v2/image/icon-gear-system-settings.png)\) in the upper right corner.

    2.  Move the **Aggregated** entry from the **Available** list to the **Selected** list.

    3.  Select the up/down arrows to determine where the **Aggregated** entry is to appear on the form.

    4.  Select **OK**.

3.  On the Automatic Group Filters page, double-click the value in the **Aggregated** column.

    Aggregated groups apply only to automated alert groups. When the Aggregated option appears, it is automatically activated for an automated alert group.

    **Note:** If the value of the **Automated** field changes, the value of the **Aggregated** field also changes. You can change the value of the **Aggregated** field only if the value of the **Automated** field is true.

4.  Select **true** for the specified filter to apply to groups with identical CIs and pattern identifiers or select **false** to ignore the filter and create aggregated groups for all alerts in the system.


**Related topics**  


[Specify and manage pattern identifier attributes for alert grouping](ptrn-attributes-alrt-aggregate.md)

