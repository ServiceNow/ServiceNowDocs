---
title: Configure an employee relations case restriction
description: Define what groups can view or access employee relations cases using Case Restriction Configuration.
locale: en-US
release: xanadu
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Setting up Employee Relations, Employee Relations cases, Case and Knowledge Management, HR Service Delivery, Employee Service Management]
---

# Configure an employee relations case restriction

Define what groups can view or access employee relations cases using Case Restriction Configuration.

## Before you begin

Role required: admin and sn\_hr\_er.admin

**Warning:** When creating case restrictions, be sure that you have at least one configuration that enables you to read these cases.

## Procedure

1.  Navigate to **All** &gt; **Employee Relations** &gt; **Administration** &gt; **Case Restriction Configuration**.

2.  Click **New**.

3.  On the form, fill in the fields.

<table id="table_hzl_qtx_zkb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

COE

</td><td>

Center of Excellence \(COE\) that you want to restrict access to.**Note:** For more information on COE, see [HR Centers of Excellence data model](../concept/hr-centers-of-excellence-coes.md).

</td></tr><tr><td>

Able to restrict cases

</td><td>

Option to enable members of a group to restrict access to all HR cases for the COE.

</td></tr><tr><td>

Able to view restricted cases

</td><td>

Option that enables a group to view restricted HR cases for the COE.

</td></tr><tr><td>

Application

</td><td>

The application that the case restriction configuration applies to. This field is automatically set to Human Resources: Employee Relations.

</td></tr><tr><td>

Active

</td><td>

Option to activate the case restriction configuration record.

</td></tr></tbody>
</table>4.  Click **Save** or **Submit**.

5.  Add the groups that you want the case restriction configuration to apply to.

    **Note:** You can also restrict by role. Agents with the sn\_hr\_er.confidential role can access restricted ER cases.

    ![HR ER Case Restriction Configuration](../image/hr-er-case-restrict-config.png)

6.  Click **Update**.

    **Note:** Collaborators on an HR or ER case can override COE security. But, ER cases with restrictions override collaborators. For more information, see [Create COE security](../concept/hr-service-categorization.md#).

    COE security policies are a way to easily restrict access to different COEs via configuration. The underlying COE security policy implementations are [ServiceNow ACLs](https://www.servicenow.com/docs/access?context=access-control-rules&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).


