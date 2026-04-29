---
title: Legacy Problem form
description: Description of the field values for the legacy problem form.
locale: en-US
release: australia
product: Problem Management
classification: problem-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Reference section for Problem Management, Problem Management, IT Service Management]
---

# Legacy Problem form

Description of the field values for the legacy problem form.

<table id="table_qwq_5wy_wxb"><thead><tr><th>

Name

</th><th>

Definition

</th></tr></thead><tbody><tr><td>

Business service

</td><td>

Business service that the problem applies to.If you select a business service as the configuration item and that business service is also listed as the configuration item in any other active task, the active tasks icon \(![other active tasks](../../change-management/image/other-active-task.png)\) appears. Click the icon to view the list of all the other active tasks that are affecting the business service.

 You can view the BSM map \(dependency view\) of the selected business service by clicking the dependency icon ![dependency map icon](../../change-management/image/dependency-icon.png).

</td></tr><tr><td>

Configuration item

</td><td>

Configuration item \(CI\) that the problem applies to. The CI class of the selected configuration item identifies the type of problem, for example, hardware, network, or database.

</td></tr><tr><td>

Change request

</td><td>

Change request associated with the problem.

</td></tr><tr><td>

Major problem

</td><td>

Check box to prioritize a problem and highlight that it needs a review.

</td></tr><tr><td>

Knowledge

</td><td>

Check box to automatically submit a knowledge article when a problem is closed.

</td></tr><tr><td>

State

</td><td>

State of the problem: -   **Open**: Open and unassigned.
-   **Pending Change**: Waiting for the corresponding change request to be closed.
-   **Known Error**: This problem is not going to be fixed and there is a workaround. Users with the itil role have access to the **Known Errors** module.
-   **Closed/Resolved**: The problem is fixed and closed.

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

The group who will work on the incident. The business rule **Populate Assignment Group based on CI/SO** populates the **Assignment group** field based on the support group available for the configuration item \(CI\) or the Service offering consecutively.

**Note:** The business rule is triggered when an incident is created or updated and when the **Assignment group** and the **Assigned to** field is empty.

If you want to override the default value, you need to create new properties and provide the field in the property value that must be used to populate the **Assignment group** field. Create the properties in the following order of preference:

-   **com.snc.problem.ci\_assignment\_group.field\_name**: identifies which CI field populates the **Assignment group** field.
-   **com.snc.problem.service\_offering\_assignment\_group.field\_name**: identifies which service offering field populates the **Assignment group** field.

 **Note:** The sys\_user\_group **read** ACL calls the SNCRoleUtil function. The function verifies whether the group that is reviewed contains either the admin role or security\_admin role. The function allows the user to view the group only if the user has the same role. As a result, a user with the itil role cannot assign an incident to a group that has the admin role or security\_admin role nor to any group whose parent has those role.

</td></tr><tr><td>

Assigned to

</td><td>

Specific user that the problem is assigned to. If an assignment rule applies, the problem is automatically assigned to the appropriate user or group.

</td></tr><tr><td>

Parent

</td><td>

The parent task for this problem.

</td></tr><tr><td>

Short description

</td><td>

Summary of the problem.

</td></tr><tr><td>

Description

</td><td>

Detailed description of the problem.

</td></tr><tr><td>

Work notes list

</td><td>

Users who receive notification when work notes are added to the problem. Click the **Add me** icon to add yourself to the work notes list for problems you are interested in monitoring.

</td></tr></tbody>
</table>**Parent Topic:**[Reference section for Problem Management](reference-section-for-problem-management.md)

