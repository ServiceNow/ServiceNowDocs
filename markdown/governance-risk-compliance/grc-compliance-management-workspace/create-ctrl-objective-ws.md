---
title: Create a control objective using the Compliance Workspace
description: A control objective is an objective, direction, or standard that acts as guidance for company interactions and operations. Control objectives can be categorized, classified, and related to policies using the Compliance Workspace.
locale: en-US
release: yokohama
product: GRC: Compliance Management Workspace
classification: grc-compliance-management-workspace
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Manage control objectives and policies using the Compliance Workspace, Using the Compliance Workspace, Performing compliance tasks in Compliance Workspace, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Create a control objective using the Compliance Workspace

A control objective is an objective, direction, or standard that acts as guidance for company interactions and operations. Control objectives can be categorized, classified, and related to policies using the Compliance Workspace.

## Before you begin

Role required: sn\_compliance.admin, sn\_compliance.manager, sn\_compliance.user

## Procedure

1.  Navigate to **All** &gt; **Policy and Compliance** &gt; **Compliance Workspace**.

2.  Click the **Create** list and select **Control objective**.

3.  On the form, fill in the fields.

<table id="table_FloorForm"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the control objective.

</td></tr><tr><td>

Source

</td><td>

Source of the policy. For example, if the statement is from the a third-party provider, indicate which one.

</td></tr><tr><td>

Source ID

</td><td>

Unique identification number used by the source to catalog this authority document.

</td></tr><tr><td>

Reference

</td><td>

Unique numerical identifier.

</td></tr><tr><td>

Parent

</td><td>

Control objective that is not a child of the current control objective. This is to avoid cyclic parent – child relationship.

</td></tr><tr><td>

Compliance Score Percentage

</td><td>

Compliance score percentage calculated for this control objective and its color code: -   Green: 80 and higher
-   Yellow: 80 to 50
-   Red: below 50


</td></tr><tr><td>

Active

</td><td>

Option that indicates whether a policy is active.

</td></tr><tr><td>

Creates controls automatically

</td><td>

Option that indicates that controls are automatically created from the control objective. **Note:** Select this option if the control objective can also serve as the control.

</td></tr><tr><td>

Create control requirements

</td><td>

Option to generate control requirements automatically for every control generated under an entity.

 If no control objective requirements exist, then no control requirements are generated.

 The number of control requirements that are generated equals the number of control objective requirements.

</td></tr><tr><td>

Category

</td><td>

List of options:-   Acquisition or sale of facilities, technology, and services
-   Audits and risk management
-   Compliance and Governance Manual of Style
-   Human Resources management
-   Leadership and high-level objectives
-   Monitoring and measurement
-   Operational management
-   Physical and environmental protection
-   Privacy protection for information and data
-   Records management
-   System hardening through configuration management
-   Systems continuity
-   Systems design, build, and implementation
-   Technical security
-   Third party and supply chain oversight
-   Root
-   Deprecated


</td></tr><tr><td>

Classification

</td><td>

List of options:-   Preventive
-   Corrective
-   Detective


</td></tr><tr><td>

Type

</td><td>

List of options:-   Acquisition/Sale of Assets or Services
-   Actionable Reports or Measurements
-   Audits and Risk Management
-   Behavior
-   Business Processes
-   Communicate
-   Configuration
-   Data and Information Management
-   Duplicate
-   Establish Roles
-   Establish/Maintain Documentation
-   Human Resources Management
-   Investigate
-   IT Impact Zone
-   Log Management
-   Maintenance
-   Monitor and Evaluate Occurrences
-   Physical and Environmental Protection
-   Process or Activity
-   Records Management
-   Systems Continuity
-   Systems Design, Build, and Implementation
-   Technical Security
-   Testing
-   Training


</td></tr><tr><td>

Attestation method

</td><td>

List of options:-   Classic attestation: ServiceNow AI Platform classic method of control assessment.
-   Attestation: Method by which controls are assessed.

**Note:** If you select Attestation, then the Attestation field is populated with **GRC Attestation**

</td></tr><tr><td>

Attestation

</td><td>

**GRC Attestation** is chosen by default.**Note:** If the user changes the control attestation, the related control objective attestation type is also changed.

</td></tr><tr><td>

Issue group rule

</td><td>

Group rule assigned to this control objective.

</td></tr><tr><td>

Description

</td><td>

Description of the control objective.

</td></tr></tbody>
</table>4.  Click **Save**.

    To view and manage the details of the control objective that you created, see [Manage a control objective from the overview page](../concept/co-overview-pc-ws.md).

    The control objective is created and all related lists are visible.

    -   A control is created for every control objective when a policy is associated with an entity.
    -   The control attributes default to the same attributes as the related control objective.
5.  From the **Overview** page, click the **More** tabs and select **Issues** tab.

    You can add existing one or more related issues to the control objective that you created. By mapping the existing issues to the control objective, you can reduce the count of open issues on the control objective.

    1.  Click the **Add** button.

    2.  Select the related issue or issues from the Issues pop-up.

    3.  Click **Add**.

        The selected issues are added to the control objective as related issues and an m2m relationship is created between the control objective and the issues in issue to control objective \[sn\_grc\_m2m\_issue\_content\] table. You can also create an issue for the control objective by clicking the **New** button.

    4.  To remove an issue that is mapped to the control objective, select the issue and click **Remove**.

        The remove action only removes the mapping between the control objective and the issue. The action doesn’t delete the issue record.

        **Note:** The UI action buttons such as New, Add, Remove aren’t available if the control objective is in Retired state.


## What to do next

If you’re implementing the [Policy and Compliance Management](../../grc-policy-compliance-implementation/task/policy-compliance-impl-checklist.md) software, return to the [Policy and Compliance Management setup checklist](../../grc-policy-compliance-implementation/task/policy-compliance-impl-checklist.md) and proceed to the next step.

