---
title: Assign the workplace user role to employees
description: Set rules in Workplace Core to assign the workplace user role to employees and apply conditions accordingly.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/workplace-core/assign-workplace-user-role-to-employees-of-a-location-wsd.html
release: brazil
product: Workplace Core
classification: workplace-core
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 4
breadcrumb: [Manage, Workplace Core, Workplace Service Delivery, Employee Service Management]
---

# Assign the workplace user role to employees

Set rules in Workplace Core to assign the workplace user role to employees and apply conditions accordingly.

## Before you begin

Ensure that the user profiles of all your employees have required details. You can review the employee user profiles by navigating to **User Administration** &gt; **Users**.

Role required: admin or sn\_wsd\_core.admin

## Procedure

1.  Navigate to **Workplace Safety Management** &gt; **Administration**.

2.  Select **Client Role Assignment Rules**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Unique name for this assignment rule.|
    |Role|This value is auto-generated with the workplace user role \(sn\_wsd\_core.workplace\_user\).|
    |Active|Option for indicating whether this assignment rule is active.|
    |Condition|Option to add filter conditions that a user profile must match. To add a condition, select **Add filter condition**. To add a OR clause, select **Add "OR" clause**.|
    |Table|Table on which the conditions must be built. The field is automatically selected as `sys_user`.|

4.  Select **Submit**.


## Result

The workplace user roles are assigned. If a record is created or updated on this table, a role assignment process is triggered in the background.

**Note:**

-   When a user no longer satisfies the Workplace Client Role Rule criteria, the role assignment framework deactivates the existing sys\_user\_has\_role record by setting its state to Pending Approval.
-   The Pending Approval state is equivalent to the inactive state — the user does not hold the role. Role evaluation grants a role only when the assignment state is active.
-   When the user satisfies the criteria again, the same record is moved back to active. No new record is created.

**Parent Topic:**[Manage workplace safety activities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/workplace-core/manage-wsd-activites.md)

**Related topics**  


[Import your workspaces data from an Excel spreadsheet]()

[Add a space type configuration]()

[Configure a workplace card]()

[Block a workplace location]()

[Configure Workplace entity and entity types]()

[Managing Neighborhoods]()

[Enable favorites option for Workplace Service Portal]()

[Create a workplace performer criteria]()

[Mapping employees to their designated workspaces]()

[Configuring shifts for your workplace]()

[Managing workplace shifts that you own]()

[Managing workplace reservations for employees]()

[Setting and tracking arrivals at the workplace]()

[Approve employee workplace reservation requests]()

[Managing workplace tasks]()

[Workplace knowledge management]()

[QR code management]()

[Location migration]()

[View workplace service usage analytics with Usage Insights]()

