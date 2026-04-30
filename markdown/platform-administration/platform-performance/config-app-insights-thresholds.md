---
title: Configure Application Insights thresholds
description: Configure conditional thresholds to trigger an alert that notifies you when one or more metrics, such as response time, is outside of the desired range.
locale: en-US
release: xanadu
product: Platform Performance
classification: platform-performance
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Application Insights, Monitoring platform performance, Platform performance, Maintain and monitor, Administer the ServiceNow AI Platform]
---

# Configure Application Insights thresholds

Configure conditional thresholds to trigger an alert that notifies you when one or more metrics, such as response time, is outside of the desired range.

## Before you begin

Role required: sn\_app\_insights.admin or admin

## Procedure

1.  Navigate to **All** &gt; **Application Insights** &gt; **Application Insights**.

2.  Select **Thresholds**.

3.  Select **New**.

4.  Enter a name.

5.  Select a metric.

6.  Select an operator.

7.  Enter a value in the **Threshold** field.

8.  Enter the number of minutes in the **Sustained for \(min\)** field.

9.  To add an additional metric, select **and**.

10. To add an alternate metric, select **or**.

11. Select **Save**.

12. To edit a threshold, select it from the Thresholds list.

13. Edit the threshold and select **Save**.

14. To create a trigger action, select the threshold from the Thresholds list and from the ellipsis, select **Create flow**.

    The ServiceNow® Workflow Studio opens with a default template in place. For more information about configuring triggers, see [Configure Application Insights threshold triggers](conf-app-insights-thresh-triggers.md).

15. To delete a threshold, select it from the Thresholds list and from the ellipsis, select **Delete**.

16. To create a new threshold based on an existing threshold:

    1.  Select the existing threshold from the Thresholds list.

    2.  Edit the name and other values.

    3.  From the ellipses, select **Insert and Stay**.


## Result

The threshold is listed on the **Thresholds** tab and is shown as a horizontal dotted red line on the associated graph.

**Parent Topic:**[Application Insights](../concept/application-insights.md)

