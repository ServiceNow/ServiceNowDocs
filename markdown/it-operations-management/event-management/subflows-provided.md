---
title: Event Management subflows in the base system
description: The subflows provided with the base system appear in the Remediation Subflows area of alert management rules.
locale: en-US
release: zurich
product: Event Management
classification: event-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Alert management rules for resolving alerts, Manage and monitor alerts, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Event Management subflows in the base system

The subflows provided with the base system appear in the Remediation Subflows area of alert management rules.

## Accessing the subflows

Navigate to **Event Management** &gt; **Rules** &gt; **Alert Management Rules** and click **New**. Click the **Actions** tab. In the Remediation Subflows area, double-click the **Insert a new row** field.

![Specify subflow](../image/new-subflow.png)

Click the search icon ![Search icon](../image/LookupUsingList.png) to add subflows. The list of subflows that are provided with the base system appears.

<table id="table_ffj_gwd_b2b"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Acknowledge Alert

</td><td>

Subflow to mark the alert as being Acknowledged. Acknowledge an alert to show that further attention is required.

</td></tr><tr><td>

Attach Knowledge Article \(legacy\)

</td><td>

Subflow to attach a knowledge article to the alert.This subflow is provided for instances that are migrated from legacy releases \(prior to the London release\).

 **Note:** Add the **Knowledge article** column to the Alert Management Rules \[em\_alert\_management\_rule\] table, and select an article to attach to an alert when the rule executes.

</td></tr><tr><td>

Change Alert to Maintenance Mode

</td><td>

Subflow to mark the alert as being in Maintenance.

</td></tr><tr><td>

Close Alert

</td><td>

Subflow to mark the alert as being Closed.

</td></tr><tr><td>

Create Incident

</td><td>

Subflow to create an incident. Fields from the alert are used to populate the matching fields in the incident that is created. **Note:**

-   If there is an existing incident that is attached to the alert, this subflow is not activated.
-   If the alert is in Maintenance, an incident is not created.
-   The alert management job runs even if the alert grouping job is not complete, if a specified time frame has passed. When this occurs, you can enable the **Avoid INTs on secondary alerts** rule to prevent incidents from being created for secondary alerts \(when the **evt\_mgmt.avoid\_int\_enabled** property is enabled\), since an incident already exists for the primary alert.

</td></tr><tr><td>

Create Major Incident Candidate

</td><td>

Subflow to create a major incident candidate. Fields from the alert populate the matching fields in the major incident candidate that is created. A major incident candidate can be upgraded to become a major incident.**Note:**

-   If there is an existing incident that is attached to the alert, this subflow is not activated.
-   If the alert is in Maintenance, a major incident candidate is not created.
-   If the **Role in group** is **Secondary**, the major incident candidate is not created.

</td></tr><tr><td>

Create Major Incident from Alert

</td><td>

Subflow to create a major incident from alert. Fields from the alert are used to populate the matching fields in the major incident that is created. **Note:**

-   If there is an existing incident that is attached to the alert, this subflow is not activated.
-   If the alert is in Maintenance, an incident is not created.
-   If the **Role in group** is **Secondary**, the major incident candidate is not created.

</td></tr><tr><td>

Create Major Incident with Impact

</td><td>

Subflow to create a major incident from an alert in which the **Impact** field is also taken as input. Fields from the alert are used to populate the matching fields in the major incident that is created. **Note:**

-   If there is an existing incident that is attached to the alert, this subflow is not activated.
-   If the alert is in Maintenance, an incident is not created.
-   If the **Role in group** is **Secondary**, the major incident candidate is not created.

</td></tr><tr><td>

Create Major Incident Candidate with Impact

</td><td>

Subflow to create a major incident candidate in which the **Impact** field is also taken as input. Fields from the alert populate the matching fields in the major incident candidate that is created. A major incident candidate can be upgraded to become a major incident.**Note:**

-   If there is an existing incident that is attached to the alert, this subflow is not activated.
-   If the alert is in Maintenance, a major incident candidate is not created.
-   If the **Role in group** is **Secondary**, the major incident candidate is not created.

</td></tr><tr><td>

Create Task \(legacy\)

</td><td>

This subflow uses a task template, if provided, or the **EventMgmtCustomIncidentPopulator** script for instances migrated from legacy releases \(prior to the London release\). If configured, apply the task template.**Note:** Add the **Task template** column to the Alert Management Rules \[em\_alert\_management\_rule\] table, and select a task template and task to apply when the rule executes.

</td></tr><tr><td>

Overwrite Alert Template \(legacy\)

</td><td>

This subflow applies the alert template.This subflow is provided for instances that are migrated from legacy releases \(prior to the London release\).

 **Note:** Add the **Task type** column to the Alert Management Rules \[em\_alert\_management\_rule\] table, and select an alert template to apply when the rule executes.

</td></tr></tbody>
</table>1.  Select the subflow that you need.
2.  To customize a subflow, see [Create a custom subflow for alerts](../task/create-custom-create-incident-subflow.md). This topic also describes the input parameters in a subflow.
3.  To specify when the workflow must be executed, double-click the cell under **Execution**.

    ![Subflow execution](../image/subflow-execution.png)

    .


**Parent Topic:**[Alert management rules for resolving alerts](../concept/alert-management-rule.md)

