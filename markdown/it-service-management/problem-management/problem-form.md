---
title: Problem form
description: Description of the field values for the problem form.
locale: en-US
release: zurich
product: Problem Management
classification: problem-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Reference, Problem Management, IT Service Management]
---

# Problem form

Description of the field values for the problem form.

<table id="table_ax1_swy_wxb"><thead><tr><th>

Name

</th><th>

Definition

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Read-only field. Unique number to identify the problem.

</td></tr><tr><td>

Origin task

</td><td>

Task that first identified this problem.

</td></tr><tr><td>

Category

</td><td>

Group to which the problem belongs to such as software, hardware. After selecting the category, select the subcategory, if applicable.

</td></tr><tr><td>

Service

</td><td>

Business service that the problem applies to.If you select a business service as the configuration item and that business service is also listed as the configuration item in any other active task, the active tasks icon \(![other active tasks](../../change-management/image/other-active-task.png)\) appears. Click the icon to view the list of all the other active tasks that are affecting the business service.

 You can view the BSM map \(dependency view\) of the selected business service by clicking the dependency icon ![dependency map icon](../../change-management/image/dependency-icon.png).

</td></tr><tr><td>

Service Offering

</td><td>

Consists of one or more service commitments that uniquely define the level of service in terms of availability, scope, pricing, and packaging options. Service offering enables you to receive different features and their levels of performance for a given service.

</td></tr><tr><td>

Configuration item

</td><td>

Configuration item \(CI\) that the problem applies to. The CI class of the selected configuration item identifies the type of problem, for example, hardware, network, or database.

</td></tr><tr><td>

State

</td><td>

For existing customers, the available states are: **Open**, **Pending Change**, **Known Error**, and **Closed** or **Resolved**.

 For new customers from Madrid, the state management process is applied. This state field is a read-only field. The field value changes as the problem proceeds from one state to another state. The states available are: **New**, **Assess**, **Root Cause Analysis**, **Fix in Progress**, **Resolved**, and **Closed**.

</td></tr><tr><td>

Resolution code

</td><td>

Indicates whether the problem is resolved, a fix is applied, a duplicate is available, or the problem coordinator accepts the risk.

**Note:** This field appears only for new customers from Madrid or a later release as it is part of the state management process.

</td></tr><tr><td>

Duplicate of

</td><td>

When **Resolution code** is **Duplicate**, the **Duplicate of** field is the reference to the Problem from which the current Problem is duplicated.

</td></tr><tr><td>

Impact

</td><td>

Effect that the problem has on business. Select the appropriate impact level \(**High**, **Medium**, or **Low**\).

</td></tr><tr><td>

Urgency

</td><td>

Extent to which the problem resolution can bear delay. Select the appropriate urgency level \(**High**, **Medium**, or**Low**\).

</td></tr><tr><td>

Priority

</td><td>

How quickly the service desk should address the problem \(**Critical**, **High**, **Moderate**, **Low**, or **Planning**\). The **Priority** field is read-only and is set according to the **Impact** and **Urgency** values entered.

</td></tr><tr><td>

Assignment group

</td><td>

The group who will work on the problem. The business rule **Populate Assignment Group based on CI/SO** populates the **Assignment group** field based on the support group available for the configuration item \(CI\) or the Service offering consecutively.

**Note:** The business rule is triggered when an incident is created or updated and when the **Assignment group** and the **Assigned to** field is empty.

If you want to override the default value, you need to create new properties and provide the field in the property value that must be used to populate the **Assignment group** field. Create the properties in the following order of preference:

-   **com.snc.problem.ci\_assignment\_group.field\_name**: identifies which CI field populates the **Assignment group** field.
-   **com.snc.problem.service\_offering\_assignment\_group.field\_name**: identifies which service offering field populates the **Assignment group** field.

 If the **Assignment group** field is blank, the incident is automatically assigned to a group.

</td></tr><tr><td>

Assigned to

</td><td>

Specific problem coordinator that the problem is assigned to. If an assignment rule applies, the problem is automatically assigned to the appropriate user or group.

</td></tr><tr><td>

Problem Statement

</td><td>

Description of the problem that the problem-solving team addressing. When you update the problem statement and move to another field, the **Related Search** field displays knowledge articles. If you configure the problem properties, then the **Related Search** field displays other related information related to the problem statement.

</td></tr><tr><td>

Description

</td><td>

Detailed description of the problem.

</td></tr><tr><td>

Related Search

</td><td>

Result of a search. **Note:** If you want to search and link a known error article or knowledge article to the Problem, click **Attach**.

</td></tr><tr><td class="sub-head" colspan="2">

Notes

</td></tr><tr><td>

Work notes list

</td><td>

Users who receive notification when work notes are added to the problem.

</td></tr><tr><td>

Work notes

</td><td>

Inscription about the work that you perform on the Problem.

</td></tr><tr><td class="sub-head" colspan="2">

Analysis Information

</td></tr><tr><td>

Workaround

</td><td>

Method that you have used to overcome the Problem. Providing a workaround if useful for fast Incident resolution. It can be a way of dealing with a problem or making something work despite the problem not being resolved.

 If a workaround is available, the problem coordinator can click the Communicate Workaround action to notify the related Incidents.

</td></tr><tr><td>

Cause notes

</td><td>

Inscription on what had caused the problem.

</td></tr><tr><td class="sub-head" colspan="2">

Resolution Information

</td></tr><tr><td>

Resolved by

</td><td>

Read-only field. Name of the user who resolved the issue.

**Note:** This field appears only for new customers from Madrid or a later release as it is part of the state management process.

</td></tr><tr><td>

Resolved

</td><td>

Read-only field. The date and time when the Problem is resolved. **Note:** This field appears only for new customers from Madrid or a later release as it is part of the state management process.

</td></tr><tr><td>

Fix notes

</td><td>

Inscription on how you have fixed the problem. If a fix is available, the problem coordinator can click the Communicate Fix action to notify the related Incidents.

</td></tr><tr><td class="sub-head" colspan="2">

Other Information

</td></tr><tr><td>

Opened by

</td><td>

Read-only field. Name of the user who opened the problem.

</td></tr><tr><td>

Opened

</td><td>

Read-only field. The date and time when the user opened the Problem.

</td></tr><tr><td>

Confirmed by

</td><td>

Read-only field. Name of the user who confirms that the problem is valid and needs a resolution. **Note:** This field appears only for new customers from Madrid or a later release as it is part of the state management process.

</td></tr><tr><td>

Confirmed

</td><td>

Read-only field. The date and time when the user confirms that the Problem is valid and needs a resolution. **Note:** This field appears only for new customers from Madrid or a later release as it is part of the state management process.

</td></tr><tr><td>

Fix by

</td><td>

Read-only field. Name of the user who started the fix.

</td></tr><tr><td>

Fix

</td><td>

Read-only field. The date and time when the user started the fix.

</td></tr></tbody>
</table>**Parent Topic:**[Reference section for Problem Management](../concept/reference-section-for-problem-management.md)

