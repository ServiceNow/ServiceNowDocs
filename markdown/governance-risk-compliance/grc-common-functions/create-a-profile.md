---
title: Create independent entities
description: Entities can be created manually, rather than generating them from the entity types. Entities can also be created without needing to refer to an existing ServiceNow table, like assets, applications, business services, or processes.
locale: en-US
release: yokohama
product: GRC Common Functions
classification: grc-common-functions
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Entity scoping, Explore entities, Common GRC features, Governance, Risk, and Compliance]
---

# Create independent entities

Entities can be created manually, rather than generating them from the entity types. Entities can also be created without needing to refer to an existing ServiceNow® table, like assets, applications, business services, or processes.

## Before you begin

Role required:

-   sn\_compliance.admin or sn\_compliance.manager,
-   n\_risk.admin or sn\_risk.manager
-   sn\_audit.admin or sn\_audit.manager

## Procedure

1.  Navigate to one of the following locations:

    -   **Policy and Compliance** &gt; **Scoping** &gt; **All Entities**.
    -   **Risk** &gt; **Scoping** &gt; **All Entities**.
    -   **Audit** &gt; **Scoping** &gt; **All Entities**.
2.  Do one of the following actions

<table id="choicetable_wn5_ds3_4w"><tbody><tr><td id="d362065e126">

**To create a new entity**

</td><td>

Click **New**.

</td></tr><tr><td id="d362065e138">

**To edit an entity**

</td><td>

Open the entity from the list.

</td></tr></tbody>
</table>3.  On the Entity form, fill the fields as appropriate.

<table id="table_yww_y2f_vs"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Refers to existing record

</td><td>

Select this checkbox if the entity is already part of a ServiceNow® table record. Clear this check box to create a stand-alone entity.

</td></tr><tr><td>

Applies to record

</td><td>

Select the table name and the corresponding document. This field is visible only when the **Refer to existing record**check box is selected.

</td></tr><tr><td>

Active

</td><td>

Check box to activate the entity.

</td></tr><tr><td>

Name

</td><td>

The name of the entity.

</td></tr><tr><td>

Compliance Score Percentage

</td><td>

Compliance percentage derived from Downstream controls.

</td></tr><tr><td>

Owned by

</td><td>

Select the control owner for this entity. Notifications are automatically sent to entity owners and risk managers in the event of a breach.**Note:** The control owner must be a valid, active user. If an entity is assigned to an inactive user, the entity will be neglected, unless it is observed in reports.

</td></tr><tr><td>

Class

</td><td>

Entity class to which the application belongs.

</td></tr><tr><td>

Generate target

</td><td>

Select this check box if you want to create a target. Every time an entity is created in the system, a target record is also created. This field is only visible if at least one of the use case accelerator applications is installed.

</td></tr></tbody>
</table>4.  In the Compliance related list, in the **Attestation frequency** field select the appropriate option.

    This field refers to the frequency with which the attestations are sent out to the attestation respondents. The value here defaults the control frequency. If the control owner wants to have a different frequency at the control level, it can be overwritten.

5.  Click Risk Rollup and Tolerance related list and fill in the form as appropriate.

    This related list is visible only when Advanced Risk has been downloaded.

<table id="table_zsl_ynj_t3b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Expected ALE

</td><td>

Annual Loss of Expectancy \(ALE\) refers to the product of the annual rate of occurrence \(ARO\) and the single loss expectancy \(SLE\). Expected ALE is the expected value of the ALE for the risk statement. Enter currency and amount for the expected ALE.**Note:** This value must be less than or equal to the **Maximum acceptable ALE**.

</td></tr><tr><td>

Maximum acceptable ALE

</td><td>

Threshold value for the ALE for the risk statement.**Note:** This value must be greater than or equal to the**Expected ALE**. This value has an impact on the Tolerance status field.

</td></tr><tr><td>

Sum of calculated ALE

</td><td>

This calculation is based on the sum of calculated ALE of all the underlying risks of the risk statement and its children risk statements.

</td></tr><tr><td>

Average calculated ALE

</td><td>

This calculation is based on the average of calculated ALE of all the underlying risks of the risk statement and its children risk statements.

</td></tr><tr><td>

Maximum calculated ALE

</td><td>

This calculation is based on the maximum of calculated ALE of all the underlying risks of the risk statement and its children risk statements.

</td></tr><tr><td>

Minimum calculated ALE

</td><td>

This calculation is based on the minimum of calculated ALE of all the underlying risks of the risk statement and its children risk statements.

</td></tr><tr><td>

Tolerance Status

</td><td>

Automatically calculated based on tolerance values. -   If the **Calculated ALE** is less than or equal to the **Expected ALE** = Acceptable in green
-   If the **Calculated ALE** is greater than the **Expected ALE**, but less than or equal to the **Max acceptable ALE** = Needs Attention in orange
-   If the **Calculated ALE** is greater than the **Maximum acceptable ALE** = Unacceptable in red
 **Note:** If the Tolerance Status changes to Needs Attention or Unacceptable, emails are automatically sent to the entity owner and risk manager to investigate.

</td></tr><tr><td>

Calculated Score

</td><td>

The corresponding score for the calculated ALE:-   Low
-   Med
-   High


</td></tr></tbody>
</table>6.  In the Basel Business Line related list, in the **Basel business lines** field, map your entity to the Basel lines of business.

7.  Click **Update downstream entities business line** if you want all the downstream entities to inherit the Basel business line that you have selected.

8.  Click **Submit** or **Update**.


**Parent Topic:**[Entity scoping in GRC](../concept/c_Scoping.md)

