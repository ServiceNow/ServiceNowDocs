---
title: Create a remediation catalog item
description: Create a custom remediation catalog item in Cloud Configuration Governance for the remediations that require additional input parameters to execute.
locale: en-US
release: australia
product: ITOM Cloud Accelerate
classification: itom-cloud-accelerate
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Remediation, Using Cloud Configuration Governance, Cloud Configuration Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Create a remediation catalog item

Create a custom remediation catalog item in Cloud Configuration Governance for the remediations that require additional input parameters to execute.

## Before you begin

Role required: sn\_itom\_ccg.governor

## About this task

Some remediation actions require additional operational information, such as resource hardware type, to execute. For such cases, create a remediation catalog item with custom input parameters or variables, and associate it with the appropriate remediation action and violation type. After you create the remediation catalog item, a user with the sn\_itom\_ccg.ccg\_operator role can use it to raise a remediation request.

## Procedure

1.  Navigate to **All** &gt; **Cloud Configuration Governance** &gt; **Remediation Catalog**.

2.  Open the CCG Remediation Default Catalog record.

3.  Select **Copy** to copy the catalog item.

4.  On the form, fill in the fields.

<table id="table_s12_sj5_f5b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the Cloud Configuration Governance catalog item.

</td></tr><tr><td>

Table name

</td><td>

The table in which the record producer creates records.Retain the default value.

</td></tr><tr><td>

Owner

</td><td>

Owner of the catalog item who has edit access to it​.

</td></tr><tr><td>

Short description

</td><td>

Business purpose of the remediation catalog item.Cloud Configuration Governance displays the short description to the operator.

</td></tr><tr><td>

Activate

</td><td>

Status of the catalog item.The copied catalog item is active by default.

</td></tr></tbody>
</table>5.  Select **Update**.

    The record producer creates the following items:

    -   A Workflow Studio action named &lt;Catalog item name&gt;\_Action.
    -   A Workflow Studio subflow named &lt;Catalog item name&gt;\_Subflow.
    -   A remediation record for the catalog item. The remediation record is associated with the catalog item and the &lt;Catalog item name&gt;\_Subflow.
6.  Define catalog item variables to collect additional information through the catalog item form.

    1.  From the Variables related list, select **New**.

    2.  On the form, fill in the fields.

        For more information on catalog variables, see Service catalog variables.

    3.  Save the form.

7.  Associate the remediation catalog item with the violation type.

    1.  On the Remediations related list, select **New**.

    2.  Double-click the violation cell.

    3.  Select the violation type.

    4.  Select the save icon \(![Save icon.](../image/save-icon.png)\).

8.  Update the &lt;Catalog item name&gt;\_Action to interact with the cloud resource.

    Cloud Configuration Governance uses Integration Hub action to execute the remediation on the cloud resource. As business needs dictate the remediation logic, the Record Producer only creates a boilerplate for the &lt;Catalog item name&gt;\_Action. You must implement the &lt;Catalog item name&gt;\_Action per the business needs.

    1.  Navigate to **All** &gt; **Flow Designer**.

    2.  Select the **Actions** tab.

    3.  Open the &lt;Catalog item name&gt;\_Action.

    4.  Refer to the cloud provider documentation and implement the &lt;Catalog item name&gt;\_Action per the business needs of your organization.

        For more information on building Integration Hub actions, see Building custom actions.

    5.  Save the updated &lt;Catalog item name&gt;\_Action.

    6.  Test the &lt;Catalog item name&gt;\_Action.

        For more information, see Test an action.

    7.  Publish the &lt;Catalog item name&gt;\_Action.

9.  Associate the &lt;Catalog item name&gt;\_Action with the &lt;Catalog item name&gt;\_Subflow.

    Cloud Configuration Governance uses the Integration Hub subflows to trigger the Integration Hub action and process the returned data.

    1.  Navigate to the Workflow Studio home page by selecting the flow designer home icon \(![Flow Designer home icon.](../image/flow-designer-home.png)\).

    2.  Select the **Subflows** tab.

    3.  Open the &lt;Catalog item name&gt;\_Subflow.

    4.  Select **Add an Action, Flow Logic, or Subflow**.

    5.  Select **Action**.

    6.  Search for `<Catalog item name>_Action` and select the action.

    7.  Add appropriate flow logic.

    8.  Assign the output of the subflow to the output variable.

    9.  Test the &lt;Catalog item name&gt;\_Subflow.

    10. Publish the &lt;Catalog item name&gt;\_Subflow to activate it.


## What to do next

Run the remediation action to fix the identified violation. For more information, see [Run remediation](ccg-run-remediation.md).

