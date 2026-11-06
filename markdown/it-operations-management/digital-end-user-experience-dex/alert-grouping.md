---
title: DEX alert grouping
description: When several alerts are triggered from events governed by the same metric rule in DEX, the alert grouping mechanism automatically consolidates them. This mechanism reduces the need for users to manage individual alerts, streamlines the response process, and enables faster issue resolution.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-operations-management/digital-end-user-experience-dex/alert-grouping.html
release: australia
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [DEX alerts, Monitor application performance, Manage employee experience, Digital End-User Experience, IT Operations Management]
---

# DEX alert grouping

When several alerts are triggered from events governed by the same metric rule in DEX, the alert grouping mechanism automatically consolidates them. This mechanism reduces the need for users to manage individual alerts, streamlines the response process, and enables faster issue resolution.

When alerts are grouped, you see the total count of secondary alerts grouped next to the primary alert number.

## DEX events and alerts representation

In the Events \[em\_event\] table, any event with the **Source** field value as DEX is classified as a DEX event. For DEX, the **Type** field displays **DEX Metric Rules** because DEX alerts are generated based on DEX metric rules. When the **State** of an event is **Processed**, an alert is generated and saved in the Alerts \[em\_alert\] table.

In the Alerts table, select any alert to access its details. An alert that is created from a DEX event displays the **Source** field value as DEX. The **Metric name** field value appears as either DEX App Metric or DEX Device Metric. For an alert, the **Metric name** field value is DEX Device Metric. The **Configuration item** field shows the name of the corresponding application or device. Alerts whose **Group** field shows **Rules-based** are DEX alert groups.

## Rule for alert correlation

In **All** &gt; **Event Management** &gt; **Rules** &gt; **Alert Correlation Rules**, the DEX Metric Correlation Rule determines when alerts must be grouped and provides necessary details.

**Note:** For one application and one metric rule, there’s only one alert in DEX. DEX creates alert groups when the metric rule is the same, regardless of whether the configuration items are the same or different. When the problem is resolved, closing the primary alert also closes the secondary alerts within the same group.

## Time-based alert grouping

Time-based alert grouping automatically groups alerts according to predefined time intervals, which is advantageous for services generating numerous alerts. Consolidated alerts result in fewer disruptions for responders and contribute to shorter resolution times.

In the System Property \[sys\_properties\] table, the property **sn\_dex.alert.correlation\_rule.device.period** defines the time period in seconds for grouping and correlating similar metric rule-based DEX alerts. In the **Value** field, you can enter the desired time duration in seconds. For example, to set a 5-minute gap between alert groupings, enter `300`. Entering `0` turns off the rule.

For example, alert A1 is generated for rule R1 from device D1. After two minutes, alerts A2 and A3 are generated for the same rule R1, but from devices D2 and D3 respectively. Because A1 is the first alert, it's designated as the primary alert, and A2 and A3 are grouped as secondary alerts under A1.

Suppose you set the time duration to 300 seconds \(5 minutes\). If rule R1 generates no alerts within five minutes and alerts A4, A5, and A6 are then generated for the same rule, a new group is formed. Alert A4 is set as the primary alert, and A5 and A6 are grouped under A4.

However, if any alert is generated for rule R1 within five minutes, it's considered a secondary alert to A1 and grouped accordingly.

