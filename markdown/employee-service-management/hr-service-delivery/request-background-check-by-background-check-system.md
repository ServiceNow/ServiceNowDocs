---
title: Request a background check through a third-party background check provider
description: Request a background check for an employee through a third-party background check provider such as First Advantage, Accurate, or Sterling.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/hr-service-delivery/request-background-check-by-background-check-system.html
release: australia
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create an HR case, Use HR Case Management, Case and Knowledge Management, HR Service Delivery, Employee Service Management]
---

# Request a background check through a third-party background check provider

Request a background check for an employee through a third-party background check provider such as First Advantage, Accurate, or Sterling.

## Before you begin

An HR integrations administrator must have set up the integration between HR Service Delivery and the third-party background check system before requests can be made. See [HR Integrations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/hr-service-delivery/scoped-hr-third-party-integrations.md) for more information.

Role required: sn\_hr\_core.case\_writer

## Procedure

1.  Navigate to **All** &gt; **HR Case Management** &gt; **Create New Case**.

2.  In the **Search for Employee** field, select the employee you are creating the case for.

3.  In the **Case Details** section, in the **HR service** field, select one of the following services to request a background check through the third-party background check provider.

    -   Request Background Check by First Advantage
    -   Request Background Check by Accurate
    -   Request Background Check by Sterling
    -   &lt;Name of HR service for a custom background check system integration&gt;
    \[Omitted image "request-background-check-1.png"\] Alt text: Select the employee you are creating the background check request case for.

4.  Fill in the other fields on the form, as appropriate.

    For further details on the form fields, see [Create an HR case](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/hr-service-delivery/search-hr-case.md).

5.  Click **Create Case**.

6.  In the **Background check package** field, select the background check package you want to use for the case.

    \[Omitted image "request-background-check-2.png"\] Alt text: Select the background check package you want to use for the case.

7.  Click **Ready for Work** to send the background check request to the appropriate third-party background check provider.


## Result

As the background check application progresses, the status is updated in the **Background check application status** field.

## What to do next

To view the background check details, navigate to the **Background Check Details** related list.

**Parent Topic:**[Create an HR case](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/hr-service-delivery/search-hr-case.md)

