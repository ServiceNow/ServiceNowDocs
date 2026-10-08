---
title: Define HRBP data access and data access rules
description: Define which employees each HR business partner covers so that HR cases are assigned to HR business partners based on data access rules. The HRBP productivity assistant and the weekly digest use these assignments to list the cases that are open for each HR business partner.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/hr-service-delivery/define-hrbp-scopes-scope-rules.html
release: brazil
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2026-08-19"
reading_time_minutes: 4
keywords: [HRBP scope, scope rule, responsibility scope, case assignment, HRBP productivity assistant]
breadcrumb: [Configure, HRBP productivity assistant, HR Service Delivery, Employee Service Management]
---

# Define HRBP data access and data access rules

Define which employees each HR business partner covers so that HR cases are assigned to HR business partners based on data access rules. The HRBP productivity assistant and the weekly digest use these assignments to list the cases that are open for each HR business partner.

## Before you begin

-   The HRBP Productivity app is installed.
-   The HR business partners to which you plan to assign cases have the sn\_hrbp\_hub.user role.
-   The departments and locations you plan to include in your data access rules exist in the Department \[cmn\_department\] and Location \[cmn\_location\] tables.
-   Automatic HR business partner assignment is enabled on each HR service whose cases you want assigned by data access rules.

Role required: HRBP administrator \[sn\_hrbp\_hub.admin\]

## About this task

A data access record defines a group of employees and the HR business partners who cover them. Data access rules determine which employees belong to the group, based on leaders, departments, or locations. Each leader, department, or location in a rule also covers the employees below it in the hierarchy:

-   **Leader**

    The leader and their direct and indirect reports

-   **Department**

    Employees in the department and its sub-departments

-   **Location**

    Employees at the location and its child locations


Data access assignments link HR business partners to the data access record.

Data access determines the following:

-   **Case assignment**

    When an HR case is created, it's assigned to the HR business partners linked to any data access record whose rules match the subject person of the case.

-   **Employee information**

    An HR business partner can ask the HRBP productivity assistant about new hires, employees on leave, and the knowledge available to an employee. The results include only the employees that the business partner covers.


## Procedure

1.  Navigate to **All** &gt; **HRBP Productivity** &gt; **Human Resources Talent Data Access** &gt; **Administration**.

2.  Select **New**.

3.  Fill in the fields on the form.

<table id="table_scope_fields"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the data access, such as the business unit or region that it covers.

</td></tr><tr><td>

Description

</td><td>

Description of the employees that the data access covers.

</td></tr><tr><td>

Active

</td><td>

Option to include the data access in case assignment and in the employee information that the HRBP productivity assistant returns. This option is selected by default.

</td></tr></tbody>
</table>4.  Select **Submit**.

5.  Open the data access record that you created.

6.  In the **HRBP Data Access Rules** related list, select **New**.

7.  Fill in the fields on the form.

<table id="table_scope_rule_fields"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Data access

</td><td>

Data access record that the rule belongs to.

</td></tr><tr><td>

Leaders

</td><td>

Leaders whose organizations the rule covers.

</td></tr><tr><td>

Departments

</td><td>

Departments that the rule covers.

</td></tr><tr><td>

Locations

</td><td>

Locations that the rule covers.

</td></tr><tr><td>

Match all

</td><td>

Option to require an employee to match every field that has a value, such as both a department and a location. When this option is cleared, an employee who matches any field that has a value is covered. This option is cleared by default.

</td></tr></tbody>
</table>    A rule with no leaders, departments, or locations defined doesn't apply to any employees.

8.  Select **Submit**.

    The rule is added to the data access record.

    **Note:** Each data access record can have only one rule with the **Match all** check box cleared. To cover more employees, edit that rule instead of creating a new one. If a field lists both a record and one of its descendants, such as a department and one of its sub-departments, an error message appears and the rule isn't saved.

9.  In the **HRBP Data Access Assignments** related list, select **New**.

10. Fill in the fields on the form.

<table id="table_scope_assignment_fields"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

User

</td><td>

The HR business partner who covers the employees that match the data access rules. Only active users with the sn\_hrbp\_hub.admin role are available.

</td></tr><tr><td>

Data access

</td><td>

Data access record to which the user is assigned.

</td></tr><tr><td>

Active

</td><td>

Option to include the assignment in case assignment and in the employee information that the HRBP productivity assistant returns.This option is selected by default.

</td></tr></tbody>
</table>11. Select **Submit**.

    The user is assigned to the data access record.

    **Note:** IF the user already has an active assignment to the same data access record, an error message appears and the assignment isn't saved.

12. Repeat these steps for each group of employees that a different HR business partner covers.


## Result

HR cases are assigned to the HR business partners linked to each data access record whose rules match the subject person of the case. Assignments are recorded in the HRBP Case Assignment \[sn\_hrbp\_hub\_hrbp\_case\_assignment\] table.

Assignments are re-evaluated when you change rules or assignments, when you activate or deactivate a data access record, and when an employee's department, location, or manager changes. The HRBP assignment weekly reconciliation scheduled job also re-evaluates active cases every week.

## What to do next

Set the HRBP productivity assistant link in a system property so that the button in the weekly digest and critical urgency notifications opens your assistant. For more information, see [Configure the HRBP productivity assistant](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/hr-service-delivery/configure-hrbp-pa.md).

