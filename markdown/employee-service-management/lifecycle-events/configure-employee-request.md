---
title: Configure Lifecycle Events Employee Requests
description: Enable your managers and employees to open employee requests directly from Lifecycle events so that they don't have to create a new HR case or request.
locale: en-US
release: zurich
product: Lifecycle Events
classification: lifecycle-events
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Lifecycle Events employee requests, Use, Lifecycle Events, Employee Journey Management, HR Service Delivery, Employee Service Management]
---

# Configure Lifecycle Events Employee Requests

Enable your managers and employees to open employee requests directly from Lifecycle events so that they don't have to create a new HR case or request.

## Before you begin

Role required: sn\_hr\_le.admin or admin

## Procedure

1.  Navigate to **All** &gt; **Lifecycle Events** &gt; **Administration** &gt; **Manage Lifecycle Events**.

2.  To add employee requests to the event, open a Lifecycle Event and click the **Activity Sets** tab.

3.  Navigate to **Add New** &gt; **Employee Request**.

4.  On the form, fill in the fields.

<table><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Title

</td><td>

Title that appears in the Action list menu in the HR case.

</td></tr><tr><td>

Description

</td><td>

Details about the request.

</td></tr><tr><td>

Requester

</td><td>

Person who has access to view and make requests.-   **Opened for**: Person that the Lifecycle Events case was opened for.
-   **Subject person**: Person that is the subject of the LE case. \(This person may or may not be the same person that the request was opened for.\)


</td></tr><tr><td>

Category

</td><td>

Employee Requests category types.-   For the HR Service category type, see [HR services](../concept/hr-service-administration.md).
-   For the Catalog Item category type, see [Service catalog items](https://www.servicenow.com/docs/access?context=c_IntroductionToCatalogItems&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).


</td></tr><tr><td>

HR Service

</td><td>

Requests and assistance that an HR organization provides its employees.

</td></tr><tr><td>

Catalog Item

</td><td>

Goods or services that are available for requests.

</td></tr><tr><td>

Active

</td><td>

Option that an employee or manager can select to make the request available.

</td></tr><tr><td>

Blocks activity set completion

</td><td>

-   When selected, the employee request must be completed before an activity set is marked as completed.
-   If unselected, the activity set completes if all the underlying activities are complete regardless of whether the employee request is fulfilled.


</td></tr><tr><td>

Activity Sets

</td><td>

Sets of activities that the employee request is available in.

</td></tr><tr><td>

Audience

</td><td>

Specific groups of users that have access to the employee request. For more information about these groups, see [Audiences](../../employee-center/concept/ecpro-audience.md).

</td></tr></tbody>
</table>5.  Click **Submit**.


**Parent Topic:**[Lifecycle Events employee requests](../concept/employee-requests.md)

**Related topics**  


[Verify Lifecycle Events Employee requests configuration](test-verify-employee-request.md)

[Filter lifecycle event activities](filter-lifecycle-event-activities.md)

