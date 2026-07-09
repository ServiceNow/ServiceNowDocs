---
title: Activate a scheduled job in Manager Hub
description: Activate and run the Add Manager Hub user role scheduled job to assign the Manager Hub user role to new people managers. When the scheduled job runs, it considers delta changes and assigns the Manager Hub user role to new managers only.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/employee-service-management/hr-service-delivery/activate-sj-mh.html
release: zurich
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure, Manager Hub, HR Service Delivery, Employee Service Management]
---

# Activate a scheduled job in Manager Hub

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


**Parent Topic:**[Configure Manager Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/hr-service-delivery/set-up-managerhub.md)

**Related topics**  


[RCA approvals for Manager Hub]()

[Configure important dates in Manager Hub]()

[Configure team requests in Manager Hub]()

[Configure team data in Manager Hub]()

[Configure team column data in Manager Hub]()

[Configure team filters in Manager Hub]()

[Set up View as Direct Reports]()

[Configure daily stats in Manager Hub]()

[Configure to do mappings in Manager Hub]()

[Configure widgets in Manager Hub]()

