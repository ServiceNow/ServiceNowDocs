---
title: Activate a scheduled job
description: Activate and run the Add Manager Hub user role scheduled job to assign the Manager Hub user role to new people managers. When the scheduled job runs, it considers delta changes and assigns the Manager Hub user role to new managers only.
locale: en-US
release: yokohama
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configure Manager Hub, Manager Hub, Persona Based Experiences, HR Service Delivery, Employee Service Management]
---

# Activate a scheduled job

Activate and run the Add Manager Hub user role scheduled job to assign the Manager Hub user role to new people managers. When the scheduled job runs, it considers delta changes and assigns the Manager Hub user role to new managers only.

## Before you begin

-   Role required: admin
-   An administrator must review the criteria before assigning the Manager Hub user role to managers. Default criteria: The manager field of sys\_user table is considered for assigning the Manager Hub user role.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled jobs**.

2.  Open the Add Manager Hub user role scheduled job.

3.  Set up the time and schedule at which you want to run the scheduled job.

4.  Enable the **Active** check box.

5.  Click **Update**.


**Parent Topic:**[Configure Manager Hub](../task/set-up-managerhub.md)

**Related topics**  


[RCA approvals for Manager Hub](../task/run-rca-mh.md)

[Configure important dates](../task/configure-imp-dates.md)

[Configure team requests](../task/configure-team-requests.md)

[Configure team data](../task/configure-team-data.md)

[Configure team column data](../task/configure-team-columndata.md)

[Configure team filters](../task/configure-team-filter.md)

[Set up View as Direct Reports](../../employee-center/task/view-direct-reportee.md)

[Configure daily stats](../task/configure-daily-stats.md)

[Configure to do mappings](../task/use-to-do-map.md)

[Configure widgets](../task/configure-team-insights.md)

