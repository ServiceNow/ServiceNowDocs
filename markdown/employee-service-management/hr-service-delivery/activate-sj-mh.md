---
title: Activate a scheduled job
description: Activate and run the Add Manager Hub user role scheduled job to assign the Manager Hub user role to new people managers. When the scheduled job runs, it considers delta changes and assigns the Manager Hub user role to new managers only.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/hr-service-delivery/activate-sj-mh.html
release: australia
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, Manager Hub, HR Service Delivery, Employee Service Management]
---

# Activate a scheduled job

Activate and run the Add Manager Hub user role scheduled job to assign the Manager Hub user role to new people managers. When the scheduled job runs, it considers delta changes and assigns the Manager Hub user role to new managers only.

## Before you begin

-   Role required: sn\_mh.admin
-   An administrator must review the criteria before assigning the Manager Hub user role to managers. Default criteria: The manager field of sys\_user table is considered for assigning the Manager Hub user role.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled jobs**.

2.  Open the Add Manager Hub user role scheduled job.

3.  Set up the time and schedule at which you want to run the scheduled job.

4.  Enable the **Active** check box.

5.  Click **Update**.


**Parent Topic:**[Configure Manager Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/hr-service-delivery/set-up-managerhub.md)

**Related topics**  


[RCA approvals for Manager Hub]()

[Configure important dates]()

[Configure team requests]()

[Configure team data]()

[Configure team column data]()

[Configure team filters]()

[Set up View as Direct Reports]()

[Configure daily stats]()

[Configure to do mappings]()

[Configure widgets]()

