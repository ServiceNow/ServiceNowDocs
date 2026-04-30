---
title: Specify and manage pattern identifier attributes for alert aggregation
description: Alert aggregation learns the alerts and then forms patterns based on a set of alert and CI attributes. You can specify the set of CI and alert attributes that are used as the pattern identifier attributes for learning patterns that result in alert groups that are meaningful in your environment.
locale: en-US
release: xanadu
product: Event Management
classification: event-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Automated alert grouping, Alert grouping types, Alert grouping, Configuring Event Management, Event Management, ITOM Health, IT Operations Management]
---

# Specify and manage pattern identifier attributes for alert aggregation

Alert aggregation learns the alerts and then forms patterns based on a set of alert and CI attributes. You can specify the set of CI and alert attributes that are used as the pattern identifier attributes for learning patterns that result in alert groups that are meaningful in your environment.

## Before you begin

Role required: evt\_mgmt\_admin

## About this task

## Procedure

1.  Navigate to **Event Management** &gt; **Administration** &gt; **Manage Pattern Identifier**.

2.  On the **SA Alert Aggregation Pattern Attributes** page select **New**.

3.  Select the **Feature Identifier Attributes** icon and move attributes from the **Available** list to the **Selected** list.

    The **Configuration Item** attribute is automatically included as an identifier with all selections.

4.  Select **Submit**.

5.  Activate the newly specified pattern identifier attributes by selecting the pattern identifier attributes that you want to activate and selecting **Deploy**.


## What to do next

After specifying a new set of pattern identifier attributes, ensure that a matching event rule exists that populates the respective alert attributes. Also, run the **Service Analytics Attribute Populator for Historical Alerts** job to populate the respective attributes of historical alerts, if values are missing in existing alerts.

