---
title: Target form
description: Use the Target form to track and measure the progress of the goals.
locale: en-US
release: australia
product: Scenario Planning in SPW
classification: scenario-planning-in-spw
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Form field information for Strategic Planning, Reference, Portfolio Planning in Strategic Planning Workspace, Strategic Planning, Strategic Portfolio Management]
---

# Target form

Use the Target form to track and measure the progress of the goals.

**Note:** For Operational Sustainability Workspace and Strategic Planning users, to view the other fields that aren't added to the default view or your custom form view on the form in the workspace, configure the default or custom form layout. For information on how to configure the form layout, see [Configuring the form layout](https://www.servicenow.com/docs/access?context=configure-form-layout&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

<table id="table_rlc_24d_gyb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the target.

</td></tr><tr><td>

Goal

</td><td>

Name of the associated goal. This field is auto-populated when creating a target from the Targets related list on the Goal form.

</td></tr><tr><td>

Description

</td><td>

Brief description of the target.You can refine target description using the Refine records skill, if the Now Assist for SPM application is installed.

</td></tr><tr><td>

State

</td><td>

State of the target. The state can be **Draft**, **In progress**, **Approved**, **Complete**, **Pending**, **Achieved**, **Not Achieved**, or **Cancelled**.

</td></tr><tr><td>

Status

</td><td>

Status of the target. The status indicates whether the target breakdown is likely to be completed by the planned end date.

</td></tr><tr><td>

Progress

</td><td>

Percentage of the target execution that is complete. The value is calculated automatically.If the **Type** field is set to **Maximize**, the progress value is calculated using the following formula:

 ```
Progress = (Actual value - Base value) / (Target value - Base value) x 100
```

 If the **Type** field is set to **Minimize**, the progress value is calculated using the following formula.

 ```
Progress = (Base value - Actual value) / (Base value - Target value) x 100
```

 For more information on how the progress value is calculated when the weight scale is defined, see [Progress value calculation](../../alignment-planner-workspace/concept/progress-value-calculation-egm.md).

</td></tr><tr><td>

Impact on goal

</td><td>

A numerical value that represents the importance of the target relative to the other targets of the goal. If there are any subgoals present, they are also considered for relative weights and consequent progress calculation. By default, the value is **\(1\) Neutral**.The available options are:

-   **\(0\) No impact**
-   **\(1\) Neutral**
-   **\(2\) Moderate**
-   **\(3\) High**
-   **\(4\) Very high**
-   **\(5\) Maximum**

 **Note:** This field is available only when the **sn\_gf.weighted\_average\_enabled** system property is set to **Yes**.

</td></tr><tr><td>

Assigned entity type

</td><td>

Entity type to which the target is assigned. For example, Business Unit, Department, Company, or Portfolio.

</td></tr><tr><td>

Assigned entity

</td><td>

Entity to which the target is assigned.

</td></tr><tr><td>

Owner

</td><td>

Owner of the target. By default, the name of the user creating the target is populated.

</td></tr><tr><td>

Contributors

</td><td>

Users who contributes to the achievement of the target. By default, the contributors of the associated goal are populated.

</td></tr></tbody>
</table>|Field|Description|
|-----|-----------|
|Start date|Start date for the target. By default, the start date of the associated goal is populated.|
|End date|End date for the target. By default, the end date of the associated goal is populated.|

<table id="table_gcn_szz_fdc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Unit of measure

</td><td>

Measure type for the specified value. Usage of the measure such as cost, time, and rate. The available measure types are stored in the Units \[sn\_gf\_units\] table. Unit of measure defines the type of the target as qualitative or quantitative. The available unit of measures for the quantitative target are **\#**, **$**, **%**, and **Days**. The available unit of measure for the qualitative target is **Yes/No**.

</td></tr><tr><td>

Type

</td><td>

Target type that signifies the direction of achievement.-   **Maximize**: The direction of the progress is toward the target value from the base value where the base value must be less than the target value.
-   **Minimize**: The direction of the progress is toward the target value from the base value where the target value must be less than the base value.
-   **Milestone**: Fixed type. Only the qualitative target values are allowed \(that are set in the **Unit of measure** field for the target\) to capture the achievement of the target. The **Milestone** option is applicable only for qualitative targets.

The **Type** field becomes read-only with the value populated as **Milestone** for qualitative targets \(when the **Unit of measure** field is set to a qualitative target value\).

</td></tr><tr><td>

Start value

</td><td>

Start value of the target. The start value can also be considered as the present or current value.This field becomes read-only when a value is entered in the **Actual value** field. Clear the **Actual value** field to update a value in the **Base value** field.

 This field is available when the **Type** field is set to **Maximize** or **Minimize**.

</td></tr><tr><td>

Final target value

</td><td>

Final target value of the target. The target value should be aspirational and should challenge the teams.This field is available when the **Type** field is set to **Maximize** or **Minimize**.

</td></tr><tr><td>

Baseline reference

</td><td>

Past achievement of the target to provide reference for future performance. This value is only for reference purpose and not considered for target progress calculation.

</td></tr><tr><td>

Actuals to date

</td><td>

Actual value of the target at a given time.This field is available when the **Type** field is set to **Maximize** or **Minimize**.

</td></tr><tr><td>

Check-in frequency

</td><td>

Option to specify breakdown intervals for the target and how frequently the owner or contributor should update the actual value of the target. Breaking down the target into smaller periods helps you set a target for smaller periods and focus on the specific breakdown targets. The available options are **Daily**, **Weekly**, **Monthly**, **Quarterly**, and **Yearly**. Target breakdowns are automatically created when you set this field to any of the available options other than **None**. For more details on target breakdowns, see [Target breakdowns in Strategic Planning](../concept/target-breakdowns.md).**Note:** The target breakdowns feature isn’t supported for qualitative targets.

</td></tr><tr><td>

Target value distribution

</td><td>

Option to specify the target to be calculated cumulatively or non-cumulatively. The available options are **Split equally across the time period \(non-cumulative\)** and **Spread linearly across the time period \(cumulative\)**.This field is available only when the **Check-in frequency** field is set to any of the available options other than **None**.

</td></tr><tr><td>

Remark

</td><td>

Remark entered by the user for business justification when updating the actuals.

</td></tr><tr><td>

Check-in due date

</td><td>

Due date that the owner or contributor of the target must update the actual value of the target to.

</td></tr><tr><td>

Confidential

</td><td>

Option to restrict the access for this target record to the specific users populated in the **Allowed groups** and **Allowed users** fields.This field is available when the Operational Sustainability Management application is installed and the **sn\_grc.enable\_record\_confidentiality** property is enabled. This field is applicable only when the **Classification** field in the goal form of the target is populated as Environmental, Social, or Governance. The required role to configure this field is sn\_esg.reader.

 **Note:** Irrespective of the target record set to confidential or not, the target progress value rolls up to its goal for calculating the progress value of the goal.

</td></tr><tr><td>

Allowed groups

</td><td>

User groups who can access the target record. This field is applicable only for the Operational Sustainability Workspace users.Even though a user group is populated in this field, the users can access the confidential record only if the user group has the sn\_esg.reader role.

 This field is available when the **Confidential** field is set to **true**.

</td></tr><tr><td>

Allowed users

</td><td>

Users who can access the target record. This field is applicable only for the Operational Sustainability Workspace users.Even though a user name is populated in this field, the user can access the confidential record only if the user has the sn\_esg.reader role.

 This field is available when the **Confidential** field is set to **true**.

</td></tr></tbody>
</table>|Field|Description|
|-----|-----------|
|Comments|Detailed comments for the target to facilitate collaboration.|

<table id="table_vgw_qzr_m3c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Automate actual value

</td><td>

Option to enable the target automation feature for the target.

</td></tr><tr><td>

Actual value source

</td><td>

Target source table that the data is fetched from to auto-update the actual value of the target on the target's review due date.This field is available when the **Automate actual value** field is set to **true**.

</td></tr></tbody>
</table>## Variables section of the Target form

This section appears based on the context variables available in the target source that is selected in the **Actual value source** field.

When you select Actual value source as Benefit Plans \([predefined target automation script for benefit plans](target-automation-script-benefit-plans-apw.md)\), the **Benefit Plan** field appears in this section, from which you can select the required benefit plans for automating the actual value of the target.

**Note:** You can use the Benefit Plans custom script only when PPM Standard \(Project Portfolio Management\) is installed. If you can't find the benefit plan that you want to select, you can find and select the same from Heisenberg UI by navigate to **Enterprise Goal Management** &gt; **Targets** and opening the Target form.

**Parent Topic:**[Form field information for Strategic Planning](../../alignment-planner-workspace/reference/form-field-information-for-strategic-planning.md)

