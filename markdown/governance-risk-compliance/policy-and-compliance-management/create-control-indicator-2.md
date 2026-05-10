---
title: Manage control indicators
description: Continuous monitoring involves activities related to identifying and creating key risk and controls indicators. The Compliance Overview is available to compliance administrators and compliance managers, providing an executive view into compliance requirements, overall compliance, and compliance breakdowns.Indicator data for controls, risk, and audit evidence are measured differently depending on the GRC application.Compliance or risk managers create indicator templates from which many indicators can be created.
locale: en-US
release: australia
product: Policy and Compliance Management
classification: policy-and-compliance-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 11
breadcrumb: [Mandatory setup, Implement, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Manage control indicators

Continuous monitoring involves activities related to identifying and creating key risk and controls indicators. The Compliance Overview is available to compliance administrators and compliance managers, providing an executive view into compliance requirements, overall compliance, and compliance breakdowns.

Supporting information can be collected for indicators through automatic data collection or manual tasks. Indicator results are then used to create issues for controls, update risk scores, and provide supporting information for audit activities and control testing.

-   **Indicators**

    Indicators collect data to monitor controls and risks, and collect audit evidence. Indicators monitor a single control or risk.

-   **Indicator templates**

    Indicator templates allow the creation of multiple indicators for similar controls or risks.


**Note:** The Entity Based Access provides a framework for more granular approach to management of data access to objects associated with an entity. Administrators can grant access to an entity's related records by adding users or user groups, or by using entity user fields for entity-based access configuration. For more information, see [Entity Based Access](../../grc-common/concept/entity-based-access.md). When a user is qualified based on these configurations and has the minimum required roles, they will have access to the following tables:

-   Indicator
-   Indicator task
-   Indicator result

## Compliance Overview

|Name|Visual|Description|
|----|------|-----------|
|Compliance Requirements|Donut chart|Select a wedge to focus on a specific compliance area.|
|Overall Compliance|Donut chart|Displays the overall compliance of all the control requirements in the system. Selecting a specific wedge in the previous widget brings that area into focus.|
|Entity|Drop down list|Select one or more entities to view and compare their compliance across multiple items.|
|Control State|Check list|Select or clear check boxes to view filter reports by control state.|
|Compliance by Authority Document|Bar Chart|Compare level of compliance depending on the selected entity and/or authority document.|
|Compliance breakdown|Multi-level Pivot|View a breakdown of control compliance by related authority documents and policies.|
|Non Compliant Entities|Column Chart|Count of non-compliant control requirements grouped by entity.|

## Authority Documents

Authority documents define policies, risks, controls, audits, and other processes to ensure adherence to the authoritative content. Each authority document is defined in a record and the related lists on that record contain the individual conditions of the authority document.

The relationships of these authority document related list items are visible in the GRC Workbench in the Policy and Compliance Management application.

**Note:** You can [add content reference tags to authority documents](../../grc-common/concept/content-references.md#). Content reference tags allow you to filter records in order to more easily identify the content packs, integrations, and use case accelerators associated with the authority documents.

## Citations

Citations contain the provisions of the authority document, which can be interrelated. Citations break down an authority document into manageable themes.

You can create citations or import them from UCF authority documents and then create any necessary relationships between the citations.

**Note:** You can [add content reference tags to citations](../../grc-common/concept/content-references.md#). Content reference tags allow you to filter records in order to more easily identify the content packs, integrations, and use case accelerators associated with the citations.

**Parent Topic:**[Classic UI for Policy and Control Management](using-policy-compliance-legacy-ui.md)

## Create a control indicator

Indicator data for controls, risk, and audit evidence are measured differently depending on the GRC application.

### Before you begin

Role required: sn\_compliance\_admin, sn\_compliance\_manager

### Procedure

1.  Navigate to one of the following locations:

    -   **Policy and Compliance** &gt; **Indicators** &gt; **Indicators**.
    -   **Risk** &gt; **Indicators** &gt; **Indicators**.
    -   **Audit** &gt; **Indicators** &gt; **Indicators**.
2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_ynl_yjz_dv"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Category

</td><td>

Select **Compliance Indicator** for a control indicator and **Risk Indicator** for a risk indicator.

</td></tr><tr><td>

Name

</td><td>

Name of the indicator.

</td></tr><tr><td>

Applies to

</td><td>

Entity related to the **Item**.

</td></tr><tr><td>

Owning group

</td><td>

Group that owns the indicator.

</td></tr><tr><td>

Owner

</td><td>

Indicator owner.

</td></tr><tr><td>

Number

</td><td>

Unique identification number.

</td></tr><tr><td>

Active

</td><td>

Option that indicates whether the indicator is active.

</td></tr><tr><td>

Item

</td><td>

Related control or risk.

</td></tr><tr><td>

Template

</td><td>

Related indicator template.

</td></tr><tr><td>

Override Template

</td><td>

Option that indicates whether to override the indicator template associated to this indicator

</td></tr><tr><td>

Last result passed

</td><td>

Option that indicates whether the last result passed.

</td></tr><tr class="sub-head"><td colspan="2">

Schedule

</td></tr><tr><td>

Collection frequency

</td><td>

Collection frequency for indicator results. Indicator tasks and results are generated automatically based on the indicator schedule.

</td></tr><tr><td>

Next run time

</td><td>

Next collection time for indicator results.

</td></tr><tr class="sub-head"><td colspan="2">

Method

</td></tr><tr><td>

Type

</td><td>

Results can be gathered manually using task assignment or automatically using basic filter conditions, Performance Analytics, or a script.-   Manual
-   Basic


</td></tr><tr><td>

Short Description

</td><td>

If Type is **Manual**, this field is present. Brief description of the issue.

</td></tr><tr><td>

Instructions

</td><td>

If Type is **Manual**, this field is present. Instructions for the collection of indicator results.

</td></tr><tr><td>

Value Mandatory

</td><td>

If Type is **Manual**, this field is present.

</td></tr><tr><td>

Passed/Failed

</td><td>

If Type is **Basic**, this field is present. Indicator passes or fails.

</td></tr><tr><td>

PA Threshold

</td><td>

If Type is **PA Indicator**, this field is present. The associated PA Threshold.

</td></tr><tr><td>

Script

</td><td>

If Type is **Script**, this field is present. Script that obtains the desired system information.

</td></tr><tr class="sub-head"><td colspan="2">

Supporting Data

</td></tr><tr><td colspan="2">

**Note:** Starting with Version 10.1, the actual historical data for the supporting data records from the indicator results or indicator tasks is displayed. Earlier, only the real-time state of the records collected could be viewed.

</td></tr><tr><td>

Table

</td><td>

Use supporting data to gather supporting evidence from other applications.

</td></tr><tr><td>

Supporting data fields

</td><td>

Supporting data fields based on the selected table.

</td></tr></tbody>
</table>4.  Select **Submit**.

    **Note:** As a compliance manager or compliance admin, you can assign the indicator task to a user with Business User Lite role. If you assign a user with a Business User Lite role as an owner in the **Owner** field and **Execute** the indicator, an indicator task is created in the Open Tasks related list. This indicator task is assigned to the owner with the Business User Lite role.

    As a user with the Business User Lite role, you can navigate to **Policy and Compliance** &gt; **Indicators** &gt; **My Indicator Tasks** to view the indicator tasks that are assigned to you. You can view the indicator by selecting the information icon next to the Indicator field. You can also update the **Result** field, **State** field, **Value** field, **Additional comments**, and **Work notes** in the Indicator Task form.

    To accomplish similar tasks from the employee center, see [GRC tasks in the employee center portal](../task/grc-assessments-employee-center.md#grc-tasks-bu-lite).


### What to do next

If you’re implementing the [Policy and Compliance Management](../../grc-policy-compliance-implementation/task/policy-compliance-impl-checklist.md) software, then you've completed the required setup steps. Return to the [Policy and Compliance Management setup checklist](../../grc-policy-compliance-implementation/task/policy-compliance-impl-checklist.md) and proceed to the optional steps, as needed.

**Parent Topic:**[Policy and Compliance Management mandatory setup](../../grc-policy-compliance-implementation/concept/policy-compliance-mandatory-setup.md)

## Create a GRC indicator template

Compliance or risk managers create indicator templates from which many indicators can be created.

### Before you begin

Role required:

-   sn\_compliance.admin or sn\_compliance.manager
-   sn\_risk.admin or sn\_risk.manager
-   sn\_audit.admin or sn\_audit.manager
-   sn\_grc.user

### Procedure

1.  Navigate to one of the following locations:

    -   **All** &gt; **Policy and Compliance** &gt; **Indicators** &gt; **Indicator Templates**.
    -   **All** &gt; **Risk** &gt; **Indicators** &gt; **Indicator Templates**.
2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_ynl_yjz_dv"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the indicator.

</td></tr><tr><td>

Description

</td><td>

Description of the indicator.

</td></tr><tr><td>

Category

</td><td>

Category for which you’re creating an indicator template. For example, select **Risk Indicator Template** to create a risk indicator template.

</td></tr><tr><td>

Active

</td><td>

Option that determines whether the indicator template is active.

</td></tr><tr><td class="sub-head" colspan="2">

Method

</td></tr><tr><td>

Type

</td><td>

The method used to determine the type of indicator template. The choices are as follows:-   **Manual**: Manual indicators are used for data that cannot be retrieved from a ServiceNow instance because it comes from an external system, such as customer data from a third-party sales system.
-   **Basic**: Basic indicators are automated indicators based on an indicator source. The indicator source specifies a table and a frequency at which the scores from this table are saved.
-   **Script**: Scripted indicators use a custom script to collect the data.


</td></tr><tr><td>

Result if the value meets or exceeds the target value

</td><td>

Result configuration field. The choices are as follows:-   **Passed**
-   **Failed**
 For example, assume you enter `100` in this field. If the indicator result output is more than 100, then the indicator status will pass or fail based on the value configured in this field.

</td></tr><tr><td>

Target Type

</td><td>

Type of the target value. The choices are as follows:-   **None**: Use this option if you do not want to set up any target or threshold for the indicator.
-   **Percentage**: Use this option to determine the indicator result by a percentage value.
-   **Count**: Use this option to determine the indicator result by a count value or total number.


</td></tr><tr><td>

Target

</td><td>

The value that determines if the indicator should pass or fail.

</td></tr><tr><td>

Instructions

</td><td>

Additional instructions for the template.

</td></tr><tr><td>

Value mandatory

</td><td>

Option to decide if a value must be compulsory in the indicator task for a manual indicator. **Note:** This option appears only if **Manual** is selected from the **Type** field. This option is automatically selected if **Count** or the **Percentage** is selected from the **Target type** field.

</td></tr><tr><td class="sub-head" colspan="2">

Supporting Data

</td></tr><tr><td colspan="2">

**Note:** Starting with version 10.1, the actual historical data for the supporting data records from the indicator results or indicator tasks are displayed. Earlier, only the real-time state of the records collected could be viewed.

</td></tr><tr><td>

Collect supporting data

</td><td>

Option to enable collecting supporting data or evidence every time the indicator runs.

</td></tr><tr><td>

Table

</td><td>

Table used for collecting supporting data.

</td></tr><tr><td>

Supporting data fields

</td><td>

Fields of the source table to be used for collecting the supporting data.

</td></tr><tr><td>

Sample collection type

</td><td>

Type of supporting data collection, such as count or percentage.

</td></tr><tr><td>

Sample size

</td><td>

Minimum number of records that must be used for collecting supporting data.For example, a basic indicator could query a large table, returning thousands of records with each indicator execution. You do not need to save all of them; just a sample of those records. If you enter a sample size of 100, only 100 records are saved, even though the query returned thousands.

</td></tr><tr><td class="sub-head" colspan="2">

Basic Criteria

</td></tr><tr><td>

Criteria

</td><td>

Criteria to filter the data from the source table.

</td></tr><tr><td>

Use reference field

</td><td>

Option to enable the use of the **Reference field**.

</td></tr><tr><td>

Reference field

</td><td>

Connection between the supporting data table and the **Applies to record** field of the entity.

</td></tr><tr><td class="sub-head" colspan="2">

Additional Criteria

</td></tr><tr><td colspan="2">

To create indicators with targets, use the advanced filter criteria. This section appears only when you select **Basic** from the **Type** field. This section is used to provide more filter criteria.

</td></tr><tr><td>

Additional criteria

</td><td>

More criteria to filter the data to calculate the target value. This section only appears when **Percentage** is selected from the **Target type** field.

</td></tr><tr class="sub-head"><td class="sub-head" colspan="2">

Schedule

</td></tr><tr><td>

Collection frequency

</td><td>

Collection frequency for indicator results. Indicator tasks and results are generated automatically based on the indicator schedule.

</td></tr><tr><td>

First run date

</td><td>

First collection time for indicator results. This field is automatically set based on when an indicator or an indicator template runs for the first time. The value in this field can't be modified.

</td></tr><tr><td>

Next run date

</td><td>

Next run time to collect indicator results of all downstream indicators for this indicator template.

</td></tr><tr><td>

Due date duration \(days\)

</td><td>

Due date duration in days between the creation and due date of the indicator task and generation of its results.The due date duration added to the creation date reflects as the **Due date** of the indicator task.

This field appears only when **Manual** is selected from the **Type** field.

For more information, see [Performance enhancements for Indicator nightly job](../../grc-workspace-compliance/concept/performance-enhancements-indicator-jobs.md).

</td></tr></tbody>
</table>4.  When you have completed these entries, you can also view information on the following related lists:

    -   Control Objectives/Risk Statements
    -   Content References
    **Note:** The **Control Objectives/Risk Statements** tab enables you to reuse the same template for multiple control objectives or risk statements, or both of them.

5.  Select **Submit**.


