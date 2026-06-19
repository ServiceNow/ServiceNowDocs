---
title: Create alert group manually
description: Manually create an alert group to organize and manage related alerts when not using scheduled jobs. This provides flexibility to group alerts on-demand for effective resolution.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/event-management/t\_SAAddAlertCorrelatedAlertGrp.html
release: zurich
product: Event Management
classification: event-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Manual alert grouping, Alert grouping types and creation methods, Alert grouping, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Create alert group manually

Manually create an alert group to organize and manage related alerts when not using scheduled jobs. This provides flexibility to group alerts on-demand for effective resolution.

## Before you begin

Role required: evt\_mgmt\_admin

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **All Alerts**.

2.  Select the alert number to open the alert.

    The alert will be used to create an alert group, designated as the primary alert, to which you can add secondary alerts.

    **Note:** A closed alert cannot be assigned as a parent alert.

3.  Scroll down and in the **Secondary Alerts** tab, select **Add To Group**.

    \[Omitted image "em-secondary-alert-1.png"\] Alt text: Option to add secondary alerts to the group.

4.  Select the check boxes for all alerts you want to add to the group as secondary alerts and select **Add Selected**.

    \[Omitted image "em-secondary-alert-2.png"\] Alt text: Select the alerts that you want to add as secondary alerts to the group.

5.  In the **Secondary Alerts** tab, view the alerts that have been added as secondary.

    \[Omitted image "em-secondary-alert-3.png"\] Alt text: Secondary alerts are added to the group.


**Parent Topic:**[Manual alert grouping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/manual-alert-grouping.md)

