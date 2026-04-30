---
title: Assign a leader or supporter role to a user record
description: Provide organizational leaders and supporters with access to Leader Hub by assigning the required roles to their user record.
locale: en-US
release: yokohama
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Installing and configuring Leader Hub, Leader Hub, Persona Based Experiences, HR Service Delivery, Employee Service Management]
---

# Assign a leader or supporter role to a user record

Provide organizational leaders and supporters with access to Leader Hub by assigning the required roles to their user record.

## Before you begin

You must create an active employee definition to generate employee profiles. For more information about this process, refer to [Create an active employee definition](../../employee-center/task/generate-profile-definition.md).

You must enable the new employee details and design. For more information, see [Opt in to the employee profile](../../employee-center/task/profile-opt-in.md).

You must provide employees of your organization with a license to enable access to Leader Hub. For more information about employee licensing, refer to [License Talent Development Core users](../../employee-service-management/task/egd-employee-profile-licensing.md).

Define eligible users to show up in the org chart. For more information, see [Organization chart in Employee Center Pro](../../employee-center/concept/employee-profile-org-chart.md). Select **Employee Profile** in the **Table** field.

Role required: admin \[sn\_egd\_lh.admin\]

## Procedure

1.  Navigate to **All** &gt; **User Administration** &gt; **Users**.

    The Users \[sys\_user\] table appears.

2.  Select a record in the list associated with an employee who is an organizational leader or supporter.

    The form for a user record appears.

3.  On the **Roles** tab, select **Edit**.

4.  Enter `sn_egd` in the **Collection** field.

    A list of roles beginning with "sn\_egd" appears.

5.  Double-click the role that corresponds to the employee's occupation in your organization.

    |Role|Occupation|
    |----|----------|
    |**sn\_egd\_lh.leader**|Organizational leader|
    |**sn\_egd\_lh.supporter**|Organizational supporter|

    The role appears in the Roles List.

6.  Select **Save**.


## Result

Organizational leaders and supporters have the required role assigned to their user record to access Leader Hub. Use the navigation path that corresponds to the employee's role to view a list of employees with the leader or supporter role assigned to their user record:

|Role|Path|
|----|----|
|Organizational leader|**All** &gt; **Leader Hub** &gt; **Leaders**|
|Organizational supporter|**All** &gt; **Leader Hub** &gt; **Supporters**|

**Parent Topic:**[Installing and configuring Leader Hub](../concept/td-lh-install-config.md)

