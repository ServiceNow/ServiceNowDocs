---
title: Cloud Configuration Governance actions reference
description: Cloud Configuration Governance \(CCG\) uses Integration Hub subflows to interact with the cloud and update the configuration data in the Configuration Management Database \(CMDB\).
locale: en-US
release: zurich
product: ITOM Cloud Accelerate
classification: itom-cloud-accelerate
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Cloud Configuration Governance reference, Cloud Configuration Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Cloud Configuration Governance actions reference

Cloud Configuration Governance \(CCG\) uses Integration Hub subflows to interact with the cloud and update the configuration data in the Configuration Management Database \(CMDB\).

## CCG – Read Config Setting

Use this action to read the configuration data of the resource.

To use this action, insert an action and then navigate to **Action** &gt; **Cloud Configuration Governance** &gt; **Utils** &gt; **CCG – Read Config Setting**.

|Field|Description|
|-----|-----------|
|Resource \[Resource\]|Resource record that contains the configuration data.|
|Configuration key \[Configuration Key\]|Configuration key you want to read.|

## Assign Subflow Outputs

<table id="table_kcq_vpw_gsb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Report issue

</td><td>

Option to enable the subflow to report the audit violation.

 Select the **Report Issue** option in the Data column or clear this check box to set or clear this field.

 -   Selected: Report the issue as per the violation definition selected in the **Audit Violation Reporting** field of the policy.
-   Cleared: Cloud Configuration Governance doesn’t report the violation. Create a custom record for the audit violation. You can specify conditions to control the creation of the audit violation record.

</td></tr><tr><td>

Details

</td><td>

Violation definition that you want to report for the violation.Enter the violation definition in the **Details** field in the Data column. This field is required if you've selected the **Report Issue** option.

</td></tr></tbody>
</table>## Create Record

Use this action to create a record in the CMDB.

To use this action, insert an action and then navigate to **Action** &gt; **ServiceNow Core** &gt; **Default** &gt; **Create Record**.

<table id="table_stf_wqw_gsb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Table

</td><td>

Name of the Configuration Management Database \(CMDB\) table where the audit result is stored. Set this field to Audit Result \[sn\_itom\_ccg\_audit\_result\].

</td></tr><tr><td>

Fields

</td><td>

Details of the record that you want to create in the Configuration Management Database \(CMDB\).Add the following fields and configure input for them:

 -   **Scan Run**: Scan run during which Cloud Configuration Governance has identified the audit issue.
-   **Is Test Run**: Indicates whether Cloud Configuration Governance has reported the audit issue during a test run.
-   **Details**: Details of the violation.
-   **Violation Definition**: Violation definition of the audit issue.
-   **Resource**: Cloud resource for which Cloud Configuration Governance has raised the audit issue.
-   **Severity**: Severity of the audit issue.

</td></tr></tbody>
</table>## CCG – Insert Resource Record

Use this action to insert a resource record to the Configuration Management Database \(CMDB\).

To use this action, insert an action and then navigate to **Action** &gt; **Cloud Configuration Governance** &gt; **Utils** &gt; **CCG – Insert Resource Record**.

|Field|Description|
|-----|-----------|
|Scan run|Scan run for which the subflow must create the resource record.|
|Service account|Service account to which the resource is attached.|
|Logical datacenter|Logical datacenter to which the resource is attached.|
|Identifier|Identifier of the resource record.|
|Name|Name of the resource.|
|Type|Resource type.|
|Provider|Cloud provider that hosts the resource.|
|Details|Details of the object that you want to store in the resource record.|
|Attributes|Any additional resource attribute that you want to import to the CMDB.|

**Parent Topic:**[Cloud Configuration Governance reference](ccg-reference.md)

