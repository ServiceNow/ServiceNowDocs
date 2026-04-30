---
title: Synchronizing alert response with automated alert grouping
description: Synchronize alert response with grouping by ensuring alert management jobs runs after alert grouping jobs—this prevents duplicate actions like incident creation on secondary alerts.
locale: en-US
release: yokohama
product: Event Management
classification: event-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Alert management rules for resolving alerts, Manage and monitor alerts, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Synchronizing alert response with automated alert grouping

Synchronize alert response with grouping by ensuring alert management jobs runs after alert grouping jobs—this prevents duplicate actions like incident creation on secondary alerts.

## Before you begin

Role required: admin

## About this task

By default, the alert grouping job \(**Service Analytics group alerts using RCA/Alert Aggregation**\) and the alert management job \(**Event Management - Evaluate Scoped Alert Rules Management0**\) run independently of each other. To synchronize the alert response with automated alert grouping \(for example, to avoid creating an incident on a secondary alert\), you must enable the property **evt\_mgmt.avoid\_int\_enabled**to ensure that the Alert Management job is executed after the Alert Grouping job is completed. This property is accessible from the Event Management Properties page \(**All** &gt; **Event Management** &gt; **Administration** &gt; **Event Management Properties**\). In addition, you must configure the relevant alert management rule \(for example, for incident creation\), to filter out all secondary alerts.

**Note:** If only one alert exists when the Alert Management job runs, an incident is created. When a second alert arrives later, the next Alert Grouping job forms a group, makes the new alert as secondary, and creates a new incident.

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **Administration** &gt; **Event Management Properties**.

2.  If you want to avoid incidents on secondary alerts, select the **Enable Avoid Incidents on Secondary alerts and wait for Grouping job to be executed** check box.

3.  Select **Save**.

4.  To filter out secondary alerts, navigate to **All** &gt; **Event Management** &gt; **Rules** &gt; **Alert Management Rules**.

5.  Select the relevant rule.

6.  In the Alert Management Rule form, select the **Alert Filter** tab.

7.  In the Condition area, select **And**.

8.  Add a condition:

    -   **Role in Group**
    -   **is not**
    -   **Secondary**
9.  Select **Update**.


**Parent Topic:**[Alert management rules for resolving alerts](../concept/alert-management-rule.md)

