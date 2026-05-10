---
title: Create an alert query
description: An alert query is a set of alerts that meet specific criteria for a particular service.
locale: en-US
release: australia
product: Event Management
classification: event-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Application services in Event Management, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Create an alert query

An alert query is a set of alerts that meet specific criteria for a particular service.

## Before you begin

Navigate to **Event Management** &gt; **Administration** &gt; **Event Management Properties** and ensure that the **Enable alert query support** \(**evt\_mgmt.impact\_calulation.alert\_group\_support**\) property is set to **Yes**.

Role required: evt\_mgmt\_admin or evt\_mgmt\_operator

## About this task

The main motivation to use alert queries is a modeling solution based on data contained in the alert itself, as an alternative to using either discovered, application, or technical services.

Create an alert query to combine similar alerts that meet the specific criteria.

You can learn about Event Management basics, including alert queries, from this video:

Getting started with Event Management

## Procedure

1.  Navigate to **Event Management** &gt; **Services** &gt; **Alert Queries**.

2.  Select **New**.

3.  On the **Alert Query** form, fill in the fields.

    For a description of the field values, see [Alert Query form](../reference/alert-query-form.md)

    **Note:** In the **Filter** field:

    -   When defining an alert query filter, include only fields that appear in the Alert Histories \[em\_alert\_history\] table. Impact calculation is based on Alert History data and fields such as Overall Event Count, Priority, and Priority group are not copied to the Alert Histories \[em\_alert\_history\] table.
    -   Do not specify a dynamic time condition. For example, in the filter, do not specify `Created` condition of `Last 45 minutes` because impact calculation is triggered by a change of alert or alert query. However, for the dynamic time condition, none of these conditions have changed. ![Do not specify a dynamic time condition](../image/dynamic-time-condition.png)
    -   Some filters may slow down impact calculation. To solve this problem, adjust your alert query by adding an appropriate index, as described in [Index suggestions for slow queries](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/platform-performance/index-suggestions.md).
4.  Select **Update**.


**Parent Topic:**[Application services in Event Management](../concept/application-service-event-management.md)

**Related topics**  


[Create alert group manually](t_SAAddAlertCorrelatedAlertGrp.md)

