---
title: Define a job in the job register
description: Define jobs and their steps \(if any\), in the job register to predefine hazards and controls for each job type in your organization.
locale: en-US
release: australia
product: Health and Safety Risk Management
classification: health-and-safety-risk-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Configure, Health and Safety Risk Management, Health and Safety, Employee Service Management]
---

# Define a job in the job register

Define jobs and their steps \(if any\), in the job register to predefine hazards and controls for each job type in your organization.

## Before you begin

Role required: sn\_hs\_rm.risk\_manager or sn\_hs\_rm.risk\_data\_manager

## About this task

A job register is a list that safety managers and line managers can use to add jobs, along with their steps, if any, for their organization. Depending on the complexity, a job can be single-step or multi-step.

Each job and job step can have associated hazards and controls. Jobs with predefined hazards and controls for each step enable you to:

-   quickly submit job safety analyses \(JSAs\) and
-   perform risk assessments.

Consequently, these predefined jobs simplify the process of submitting JSAs and conducting risk assessments by automatically populating hazards and controls.

## Procedure

1.  Navigate to **Workspaces** &gt; **Health and Safety Workspace**.

2.  Select the configuration icon \(![Configuration icon](../image/icon-config.png)\).

3.  In the **Configuration** tab, select **Job register** and then **All**.

4.  Create a job.

<table id="choicetable_l1q_grs_dcc"><thead><tr><th align="left" id="d745544e115">

Option

</th><th align="left" id="d745544e118">

Steps

</th></tr></thead><tbody><tr><td id="d745544e124">

**Using the New button**

</td><td>

To define a job from scratch, select **New** in the list.-   If the job has multiple steps and you want to outline the hazards and controls for each, select **Multi step**.
-   If the job is one step and you want to outline hazards and controls on the job level, select **Single step**.


</td></tr><tr><td id="d745544e150">

**Copying an existing job**

</td><td>

Use details from an existing job to create a new one in the job register. Copying lets you have a quick start to creating a job that is similar in details or is applicable to a new location. To copy a job:1.  In the list, open the job that you want to copy.
2.  Select **Copy job**.
**Note:** The **Location** field value is not copied in the duplicated job.

</td></tr></tbody>
</table>5.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of this job.|
    |Short description|Description of the job.|
    |Job location|Location that this job or task applies to.|
    |Active|Option for making the job available for use. A job must be active to be used.|

6.  Select **Save**.

7.  If it's a multi-step job, add job steps.

    **Note:** Create a job step for each task involved in the job.

    1.  In the **Job steps** tab, select **New**.

        This tab appears only when **Multi step** is selected when creating the job.

    2.  On the form, fill in the fields.

    3.  In the **Order** field, select the order in which the job step appears.

        The value in this field determines the sequence in which job steps appear when submitting a JSA from the Employee Center.

    4.  Select **Save**.

8.  Associate hazards and controls with the job.

<table id="choicetable_k4d_sw3_dcc"><thead><tr><th align="left" id="d745544e330">

Job type

</th><th align="left" id="d745544e333">

Steps

</th></tr></thead><tbody><tr><td id="d745544e339">

**For multi-step job**

</td><td>

Add hazards and controls for each step.1.  Navigate to **Job steps** tab.
2.  In the list, open the job step to add hazards and controls to.
3.  In the **Hazards and controls** tab, select **New**.


</td></tr><tr><td id="d745544e368">

**For single-step job**

</td><td>

Navigate to the **Hazards and controls** tab and select **New**.

</td></tr></tbody>
</table>    1.  On the form, fill in the fields.

<table id="table_vfy_tgj_dcc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

System-generated unique number for the hazard and its controls for the job or the job step.

</td></tr><tr><td>

Hazard

</td><td>

Hazard associated with the job or the job step. The hazards in this field display items from the Hazard \[sn\_hs\_rm\_hazard\] table.

</td></tr><tr><td>

Available control measures

</td><td>

All active control measures that are in place and can be added for the selected hazard. The controls in this field display items from the Control measure \[sn\_hs\_rm\_control\_measure\] table.Select the check box for a control measure to add it to the **Selected control measure** list.

</td></tr><tr><td>

Selected control measures

</td><td>

Controls that are selected to be added for the hazard.

</td></tr></tbody>
</table>    2.  Select **Save**.

    If a job or a job step includes more than one hazard, create a hazard and controls record for each.

9.  In the **Document links** tab, select **New** to add any document links related to the job.

10. Select **Save**.


## Result

-   The job is listed in the **Job register** list under **Configuration** on the Health and Safety Workspace. The job is saved in the Job \[sn\_hs\_rm\_job\] table and job steps are saved in the Job step \[sn\_hs\_rm\_job\_step\] table.
-   The job is available for selection on these forms:
    -   JSA form when submitting a JSA. For more information, see [Submit JSA form](../reference/hs-submit-jsa-form.md).
    -   Risks and controls form when conducting a risk assessment. For more information, see [Assess safety hazards and risk levels for a risk analysis](add-a-risk-and-its-controls-for-a-safety-risk-assessment.md).
-   The job is also available to import hazards and controls from when performing a risk assessment. For more information, see [Create a risk analysis for a safety risk assessment from a job](import-hazards-and-controls.md).

**Parent Topic:**[Setting up Health and Safety Risk Management](../concept/hs-setting-up-risk-mgmt.md)

