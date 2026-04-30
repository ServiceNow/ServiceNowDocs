---
title: Insights installed with Workplace Concierge
description: The following insights are installed with the Workplace Concierge and Proactive Prompts plugins.
locale: en-US
release: yokohama
product: Workplace Concierge
classification: workplace-concierge
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Reference, Workplace Concierge, Workplace Service Delivery, Employee Service Management]
---

# Insights installed with Workplace Concierge

The following insights are installed with the Workplace Concierge and Proactive Prompts plugins.

Installing the Workplace Concierge plugin with the Proactive Prompts plugin creates records in the following tables.

<table id="table_os4_ffz_z1c"><thead><tr><th>

Signal Configuration

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Employee reservations insight

</td><td>

Displays a message if the employee has a reservation on a day that is set to Remote. This insight is displayed in the calendar week view.

</td></tr><tr><td>

Percentage of collaborators in the office

</td><td>

Displays the percentage of collaborators that are in the office on a specific day. This insight is displayed in the calendar week view.

</td></tr><tr><td>

Routine compliance

</td><td>

Displays a message if the employee presence isn’t set to five days in the office. This insight is displayed on the Presence dashboard.This signal configuration is scheduled to run every week. After updating the routine, employees can still see the insight until the following week. This issue can be resolved by changing the schedule.

</td></tr></tbody>
</table>|Signal Data Source|Description|
|------------------|-----------|
|Collaborator data source|Data source for the Percentage of collaborators in the office signal configuration.|
|Employee reservations|Data source for the Employee reservations insight signal configuration.|
|Routine compliance|Data source for the Routine compliance signal configuration.|

|Signal Channel Configuration|Description|
|----------------------------|-----------|
|Presence dashboard|Channel configuration for the Presence dashboard in the Workplace Concierge application.|

| | |
|---|---|
|Presence Calendar Insight|Displays the insight in the calendar week view.|
|Presence Dashboard Insight|Displays the insight on the Presence dashboard.|

**Parent Topic:**[Workplace Concierge reference](../concept/workplace-concierge-reference.md)

