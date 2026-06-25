---
title: Create a workplace performer criteria
description: Configure the users who are permitted to perform important actions in Workplace Service Delivery. Add approvers to approve workplace cases and reservations that are created through Workplace services.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/workplace-core/create-workplace-performer-criteria.html
release: australia
product: Workplace Core
classification: workplace-core
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Manage workplace safety activities, Workplace Core, Workplace Service Delivery, Employee Service Management]
---

# Create a workplace performer criteria

Configure the users who are permitted to perform important actions in Workplace Service Delivery. Add approvers to approve workplace cases and reservations that are created through Workplace services.

## Before you begin

Role required: sn\_wsd\_core.admin

## About this task

Configure workplace performer criteria and enable a set of users to perform actions such as approval and more. The configured users can perform approval actions, workplace-related activities, and reservation-related approvals. The users configured in the criteria are used to perform various important actions throughout the Workplace Service Delivery application.

## Procedure

1.  Navigate to **Workplace Core** &gt; **Administration** &gt; **Performer Criteria**.

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_wyq_zx4_fsb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the performer criteria.

</td></tr><tr><td>

Table

</td><td>

Table for which you want to create the performer criteria. This field appears only if the **Is dynamic** option is selected.

</td></tr><tr><td>

User criteria

</td><td>

User criteria for the performer criteria for approvals. This field appears only if the **Is dynamic** option isn’t selected. To add a user criteria, refer to [Create a user criteria record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-reservation-management/create-user-criteria.md).

</td></tr><tr><td>

Active

</td><td>

Option to activate the performer criteria.

</td></tr><tr><td>

Is dynamic

</td><td>

Option to create the performer criteria with a dynamic behavior. If you enable the option, you can select the user fields directly that you want to set as approvers.

</td></tr><tr><td>

User field

</td><td>

Users or user groups who perform any important Workplace Service Delivery application-related actions. This field appears only if the **Is dynamic** option is enabled.

</td></tr></tbody>
</table>4.  Select **Submit**.


## Result

The performer criteria are added for the selected table.

-   **[Create an approval definition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-core/create-approval-defintion.md)**  
Add an approval definition so that you can implement an approval process that is over that definition. The approval is applied on reservations that match the conditions.
-   **[Add a workplace approval configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-core/add-workplace-approval-configuration.md)**  
Add approvers to an approval definition. The assigned approvers receive the approval requests of those reservations that match the conditions defined in the approval definition.

**Parent Topic:**[Manage workplace safety activities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-core/manage-wsd-activites.md)

**Related topics**  


[Import your workspaces data from an Excel spreadsheet]()

[Add a space type configuration]()

[Configure a workplace card]()

[Block a workplace location]()

[Configure Workplace entity and entity types]()

[Managing Neighborhoods]()

[Enable favorites option for Workplace Service Portal]()

[Mapping employees to their designated workspaces]()

[Assign the workplace user role to employees]()

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

