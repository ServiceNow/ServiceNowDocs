---
title: Problem form
description: Description of the field values for the problem form in Service Operations Workspace.
locale: en-US
release: australia
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Problem Management in Service Operations Workspace reference, Problem Management in Service Operations Workspace, Managing IT services in your organization, Service Operations Workspace for ITSM, IT Service Management]
---

# Problem form

Description of the field values for the problem form in Service Operations Workspace.

<table id="table_un2_dyl_n3b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Problem

</td></tr><tr><td>

Problem statement

</td><td>

Brief description of the problem.

</td></tr><tr><td>

Description

</td><td>

Detailed description of the problem.

</td></tr><tr><td>

Number

</td><td>

Unique number that identifies the problem record.

</td></tr><tr><td>

Origin task

</td><td>

Task that first identified this problem.

</td></tr><tr><td>

Category and Subcategory

</td><td>

Group to which the problem belongs, such as software or hardware. After selecting the category, select the subcategory, if applicable.

</td></tr><tr><td>

State

</td><td>

Value that changes as the problem proceeds from one state to another state.For information about state transitions of a problem, see [Life cycle of a problem](../../problem-management/concept/understanding-state-mgmt-transitions.md).

</td></tr><tr><td>

Impact

</td><td>

Effect that the problem has on business operations.

</td></tr><tr><td>

Urgency

</td><td>

Extent to which the problem resolution can bear delay.

</td></tr><tr><td>

Priority

</td><td>

How quickly the service desk should address the problem. The **Priority** field is automatically set to the **Impact** and **Urgency** values.

</td></tr><tr><td class="sub-head" colspan="2">

Impact

</td></tr><tr><td>

Service

</td><td>

Business service, such as email or IT Services, that the problem applies to.

</td></tr><tr><td>

Service Offering

</td><td>

Consists of one or more service commitments that uniquely define the level of service in terms of availability, scope, pricing, and packaging options. Service offering enables you to receive different features and their levels of performance for a given service.

</td></tr><tr><td>

Configuration item

</td><td>

Configuration item \(CI\) that the problem applies to. The CI class of the selected configuration item identifies the type of problem, for example, hardware, network, or database.

</td></tr><tr><td class="sub-head" colspan="2">

Assignment

</td></tr><tr><td>

Assignment group

</td><td>

Group to which the problem is assigned.You can populate the **Assignment group** field automatically based on the support group available for the respective configuration item \(CI\). If the CI does not have any support group, then the field gets populated with the support group available for service offerings. The business rule **Populate Assignment Group based on CI/SO** triggers the functionality when an incident, problem, or change request is created or updated and when the **Assignment group** and the **Assigned to** field is empty. The following properties identify the field whose value populates the **Assignment group** field:

-   **com.snc.problem.ci\_assignment\_group.field\_name**: This problem property identifies which CI field populates the **Assignment group** field.
-   **com.snc.problem.service\_offering\_assignment\_group.field\_name**: This problem property identifies which service offering field populates the **Assignment group** field.

</td></tr><tr><td>

Assigned to

</td><td>

Problem coordinator to whom the problem is assigned. If an assignment rule applies, the problem is automatically assigned to the appropriate user or group.

</td></tr><tr><td class="sub-head" colspan="2">

Notes

</td></tr><tr><td>

Work notes

</td><td>

Informative notes about the work performed on the problem.

</td></tr></tbody>
</table>**Parent Topic:**[Problem Management in Service Operations Workspace reference](../concept/reference-problem-management-sow.md)

