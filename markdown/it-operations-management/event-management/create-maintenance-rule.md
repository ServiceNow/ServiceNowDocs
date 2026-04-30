---
title: Create maintenance rules
description: Use maintenance rules to mark CIs in maintenance status. When in maintenance status, these CIs are excluded from impact calculation.
locale: en-US
release: xanadu
product: Event Management
classification: event-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Manage and monitor alerts, Configuring Event Management, Event Management, ITOM Health, IT Operations Management]
---

# Create maintenance rules

Use maintenance rules to mark CIs in maintenance status. When in maintenance status, these CIs are excluded from impact calculation.

## Before you begin

Role required: evt\_mgmt\_admin

## About this task

You can define rules to mark CIs that match the specified criteria as being in maintenance status. The marked CIs populate the Impact Maintenance CIs \[em\_impact\_maint\_ci\] table.

**Note:** When running maintenance rules, the cmdb\_ci status of matching CIs is not changed. However, matching CIs are flagged in the em\_impact\_maint\_ci table by these rules and this status is considered for impact and alert calculations.

The field flagged by this rule as being in maintenance status is the CMDB status field.

**Note:** To activate a maintenance rule, select the **Active** field in the maintenance rule. To deactivate a maintenance rule, clear the **Active** field.

The maintenance rules provided with the base instance are:

<table id="table_qvy_w5f_qz"><thead><tr><th>

Default maintenance rule

</th><th>

Description

</th></tr></thead><tbody><tr><td>

CI in Change Window

</td><td>

Where the CI has an active change window, the matching CIs are marked as being in maintenance status.The rule runs a query against the change request \[change\_request\] table to determine whether the rule is applied. All these conditions in the change\_request table must be met:

-   **State** is one of these options: Scheduled, Implement, Work in Progress, or Open/New \(state in \(-2, -1, 1, 2\)\).
-   **Approval** is Approved \(approval = 'approved'\).
-   The change request window is active, that is, the current time is between **Planned start date** and **Planned end date**, or the current time is between **Actual start date** and **Actual end date**.
-   The change request record is not an on-hold record \(on\_hold='false'\).

 **Note:** All these conditions must be present for the CI to be placed in maintenance status by this rule. For example, if the **State** of the change request approval status is `Change is waiting for approval`, then the change is not added to the em\_impact\_maint\_ci table.

</td></tr><tr><td>

Maintenance status of CI

</td><td>

CIs whose CMDB status field is **In Maintenance** are flagged by this rule as being in maintenance status.By default, retired CIs are not included in CIs that are **In Maintenance**. To include retired CIs:

1.  Navigate to **All Properties**.
2.  Select **New**.
3.  Configure the **evt\_mgmt.maintenance\_rule\_include\_retired** property with **Value = true**.

 **Note:**

Including thousands of retired CIs may decrease system performance.

</td></tr></tbody>
</table>## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **Rules** &gt; **Maintenance Rules**.

2.  Click **New**.

3.  Fill in the fields, as appropriate.

<table id="table_osj_py4_dx"><thead><tr><th>

Column heading

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The maintenance rule name.

</td></tr><tr><td>

Active

</td><td>

Select to activate the maintenance rule.

</td></tr><tr><td>

Advanced

</td><td>

Select to enable the optional script section to display.

</td></tr><tr><td>

Description

</td><td>

Information that describes this maintenance rule.

</td></tr><tr><td>

Flag CIs that run on this host

</td><td>

Select to flag all applications running on the recognized host as being in maintenance.

</td></tr><tr><td>

Table

</td><td>

Select the table that contains the CI that you require.

</td></tr><tr><td>

Filter

</td><td>

Specify how to select the data.

</td></tr><tr><td>

CI field name

</td><td>

Select the CI from the list. The list is populated according to your selection in the **Table** field. If a CMDB table, or a table derived from CMDB, was selected, specify `sys_id` for the **CI field name**. Otherwise, specify the required CI field that you want to use. See the examples.

</td></tr></tbody>
</table>4.  Click **Submit**.


## Example

Example of a maintenance rule using a CMDB table.

Assume that a company defines a CI as being in maintenance when the Operational Status of the CI is either **Repair in Progress** or **DR Standby**.

![Event Management rule](../image/create-maintenance-rule-example.jpeg)

Example of a maintenance rule using a table other than CMDB.

Assume that a company uses Incident records to track maintenance. Any maintenance request is translated to an incident when it has a description that starts with “Performing maintenance on CI”. As long as the status of such an incident is open, this status indicates that the maintenance is in progress. For the **CI field name** field, specify a CI name from the table that was chosen, in this case **Incident**.

![Event Management table](../image/create-maintenance-rule-not-cmdb.png)

Example of a maintenance rule that uses the advanced script feature.

In the Maintenance Rule page, select the **Advanced** option. Customize the provided example script:

```
var now_GR = new GlideRecord('cmdb_ci');
gr.addQuery('name', 'your_name_here');
gr.query();
while (gr.next()){
 result.push(gr.sys_id +'');}
```

The return value for this example script is a text string that represents an array of CI IDs, for example, \['sys\_id1','sys\_id2','sys\_id3'\].

You can use this script as an example to prepare your own customized script.

![Event Management script](../image/maintenance-rule-script.png)

**Parent Topic:**[Manage and monitor alerts](../concept/c_EMAlert.md)

**Related topics**  


[How alerts work with CIs in maintenance](../concept/c_EMHowImpactTree.md)

[Place an alert into maintenance](t_EMPutAnAlertIntoMaintenance.md)

