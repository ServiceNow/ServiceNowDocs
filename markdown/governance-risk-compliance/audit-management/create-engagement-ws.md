---
title: Create an audit engagement in Audit Workspace
description: Create an engagement in the workspace and assign it to an audit supervisor. Use the workspace to schedule the engagement, plan the details, and budget the expenses.
locale: en-US
release: australia
product: Audit Management
classification: audit-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Audit Supervisor Workspace, Audit Workspace Overview, Audit Management, Governance, Risk, and Compliance]
---

# Create an audit engagement in Audit Workspace

Create an engagement in the workspace and assign it to an audit supervisor. Use the workspace to schedule the engagement, plan the details, and budget the expenses.

## Before you begin

Role required: sn\_audit.manager, sn\_audit\_ws.supervisor

## About this task

As an audit supervisor you can create an engagement to manage the audit information and collect entities, controls, and control tests that are relevant to the audit. You can supervise the audit engagement, monitor its execution, and verify its completion on time as directed.

## Procedure

1.  Navigate to **All** &gt; **Audit** &gt; **Audit Workspace**.

2.  Select the **Create** list and select **Engagement** from the **Home** page.

    You can also create an engagement by navigating to the Audit workspace List page.

    1.  Select the lists icon \(![List icon.](../image/ListsIcon.jpg)\).
    2.  Select **All engagements** or **My engagements** in the Execution list.
    3.  Select **New**.
3.  On the form, fill in the fields.

<table id="table_y4r_c1x_lqb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Unique identification number of the engagement.

</td></tr><tr><td>

Name

</td><td>

Name of the engagement.

</td></tr><tr><td>

Type

</td><td>

Audit type based on its specific use in the engagement.

</td></tr><tr><td>

State

</td><td>

State of the engagement. The default state is Scope.

</td></tr><tr><td>

Fieldwork complete \(%\)

</td><td>

Percentage of the engagement that is complete.

</td></tr><tr><td>

Description

</td><td>

General description of the engagement.

</td></tr><tr><td>

Objectives

</td><td>

Stated objectives of the engagement.

</td></tr><tr><td class="sub-head" colspan="2">

Assignment

</td></tr><tr><td>

Engagement lead

</td><td>

Audit supervisor who oversees and completes the engagement according to directions.

</td></tr><tr><td>

Auditors

</td><td>

Auditors assigned to the engagement.

</td></tr><tr><td>

Approvers

</td><td>

Approvers assigned to the engagement.

</td></tr><tr><td class="sub-head" colspan="2">

Engagement schedule

</td></tr><tr><td>

Fieldwork planned start

</td><td>

Estimated start date of the engagement.

</td></tr><tr><td>

Fieldwork planned end

</td><td>

Estimated end date of the engagement.

</td></tr><tr><td>

Fieldwork planned duration

</td><td>

Number of days and hours planned for fieldwork. The duration and planned start date of fieldwork are used to calculate the planned end date. If audit tasks are defined, this field is automatically set to the longest planned duration from the audit tasks.

</td></tr><tr><td>

Fieldwork actual start

</td><td>

Actual start date of the fieldwork. If audit tasks are defined, this field is automatically set to the earliest actual start date from the audit tasks.

</td></tr><tr><td>

Fieldwork actual end

</td><td>

Actual end date of the fieldwork. If audit tasks are defined, this field is automatically set to the latest actual end date from the audit tasks.

</td></tr><tr><td>

Fieldwork actual duration

</td><td>

Duration of fieldwork start date and end date.

</td></tr><tr><td class="sub-head" colspan="2">

Plan details

</td></tr><tr><td>

Parent plan

</td><td>

Plan that is to be associated with the engagement.

</td></tr><tr><td>

Start date

</td><td>

Start date of the plan.

</td></tr><tr><td>

End date

</td><td>

End date of the plan.

</td></tr><tr><td class="sub-head" colspan="2">

Expenses and resources

</td></tr><tr><td>

Budgeted expenses

</td><td>

Calculated expenses for the engagement.

</td></tr><tr><td>

Planned expenses

</td><td>

Estimated expenses for the engagement.

</td></tr><tr><td>

Actual expenses

</td><td>

Actual expenses incurred.

</td></tr><tr><td>

Budgeted resources

</td><td>

Budgeted resources for the engagement, in days,hours, minutes, and seconds.

</td></tr><tr><td>

Planned resources

</td><td>

Estimated resources for the engagement, in days,hours, minutes, and seconds. If resource plans are defined, this field is automatically set.

</td></tr><tr><td>

Actual resources

</td><td>

Actual resources for the engagement, in days,hours, minutes, and seconds.

</td></tr><tr><td class="sub-head" colspan="2">

Results

</td></tr><tr><td>

Result

</td><td>

Results of the engagement. The choices are as follows:-   Satisfactory
-   Adequate
-   Inadequate


</td></tr><tr><td>

Opinion

</td><td>

Justification for the selected result.

</td></tr><tr><td class="sub-head" colspan="2">

Report

</td></tr><tr><td>

Template type

</td><td>

Type of template used to generate the audit report for the engagement record.-   Classic report template: Generates the report using the classic report templates such as HTML, script, or XML, provided the engagement record is in Follow up or Closed states.

For more information, see [Create an audit report template in classic formats](../../grc-common/task/create-audit-report-temp.md) and [Generate a report for an engagement in a classic report template](generate-report-engagement-audit-ws.md).

-   Word report template: Generates the report using the Microsoft Word template, provided the engagement record is in Validate, Fieldwork, or Follow up states.

For more information, see [Generate an audit report for an engagement using Microsoft Word template](generate-audit-report.md).

The **Generate report** button is available in the engagement record only in the states mentioned for each **Template type**. You can generate only one report at a time.

</td></tr><tr><td>

Report template

</td><td>

Template used to generate the knowledge base article that reports the engagement results.This field is a reference field after a Word report is generated.

</td></tr><tr><td>

Report knowledge base

</td><td>

Knowledge base to be used.

</td></tr><tr><td>

Report

</td><td>

Reference field that displays the attachment.**Note:** This attachment field contains the URL if the Word template is Cloud enabled or a sys attachment if the Word template isn't Cloud enabled.

In addition, the report is also attached to the engagement record as an attachment. You can select the attachment \(![Attachment icon.](../../assessment-engine/image/attachment-icon.png)\) icon to view or download the Word document. If it's a cloud-based report, then the report is also present in the cloud file.

</td></tr><tr><td class="sub-head" colspan="2">

Activity

</td></tr><tr><td>

Additional comments

</td><td>

Comments that customers can also view.

</td></tr><tr><td>

Work notes \(Private\)

</td><td>

Comments that only the administrator and audit supervisor can view.

</td></tr><tr><td class="sub-head" colspan="2">

Confidentiality

</td></tr><tr><td>

Confidential

</td><td>

Option to enable confidentiality of the record. Only the assigned confidential users or confidential groups of users can access the record.For more information on the confidential option, see [Confidentiality flag for audit and compliance records](../../grc-audit/concept/confidentiality-flag-audit-pc.md).

</td></tr></tbody>
</table>    **Note:**

    -   If you had selected the **Classic report template** option in the **Template type** field while creating the engagement record, then the reports are created using HTML, script, or XML templates. For more information, see [Create an audit report template in classic formats](../../grc-common/task/create-audit-report-temp.md).
    -   If you had selected the **Word report template** option in the **Template type** field while creating the engagement, then the report is created using the Word template. For more information, see [Generate an audit report for an engagement using Microsoft Word template](generate-audit-report.md).
4.  Select **Save**.

    You can define the entities that are involved in the audit engagement.

5.  From the **Overview** page, select the **Other issues** tab.

    You can add the existing one or more related issues to the engagement that you created. By mapping the existing issues to the engagement, you can reduce the count of open issues.

    1.  Select the **Add** button.

    2.  Select a related issue or issues from the Issues pop-up.

    3.  Select **Add**.

        The selected issues are added to the engagement as related issues and an m2m relationship is created between the engagement and the issues in the Issue to Engagement \[sn\_grc\_m2m\_issue\_engagement\] table. You can also create an issue for the engagement by selecting the **New** button, which takes you to the Create New Issue form.

    4.  To remove an issue that is mapped to the engagement, select the issue and click **Remove**.

        The remove action only removes the mapping or the association between the engagement and the issue in the m2m table and doesn't delete the issue record.

        **Note:** The UI action buttons such as New, Add, Remove aren't available if the engagement is in the Retired state.


