---
title: Create a control objective
description: A control objective is an objective, direction, or standard that acts as guidance for company interactions and operations. Control objectives can be categorized, classified, and related to policies.
locale: en-US
release: australia
product: Policy and Compliance Management
classification: policy-and-compliance-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Mandatory setup, Implement, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Create a control objective

A control objective is an objective, direction, or standard that acts as guidance for company interactions and operations. Control objectives can be categorized, classified, and related to policies.

## Before you begin

Role required: sn\_compliance.admin, sn\_compliance.manager, sn\_compliance.user

## About this task

To understand the difference between a control objective and a control, see [Structural overview of Policy and Compliance Management](../concept/pc-structural-overview-policy-comp.md).

## Procedure

1.  Navigate to **All** &gt; **Policy and Compliance** &gt; **Control Objectives**.

2.  Click **New**.

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

Source of the control objective. For example, if the control objective is from a third-party provider, indicate which one.

</td></tr><tr><td>

Source ID

</td><td>

Unique identification number used by the source to catalog this control objective.

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

Compliance score percentage calculated for this control objective and it's color code: -   80 and higher in green
-   80 to 50 in yellow
-   below 50 in red


</td></tr><tr><td>

Active

</td><td>

Option that indicates whether a control objective is active.

</td></tr><tr><td>

Creates controls automatically

</td><td>

Option that indicates that controls are automatically created from the control objective. **Note:** Select this option if the control objective can also serve as the control.

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
-   Third Party and supply chain oversight
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

Attestation

</td><td>

List of options. -   **GRC Attestation** is chosen by default
-   **Note:** If the user changes the control attestation, the related control objective attestation type is changed also.

</td></tr><tr><td>

Issue group rule

</td><td>

Group rule assigned to this control objective.

</td></tr><tr><td>

Description

</td><td>

Description of the control objective.

</td></tr></tbody>
</table>4.  Click **Submit**.

    The control objective is created and all related lists are visible.

    -   A control is created for every control objective when a policy is associated with an entity.
    -   The control attributes default to the same attributes as the related control objective.

## What to do next

If you are implementing the [Policy and Compliance Management](../../grc-policy-compliance-implementation/task/policy-compliance-impl-checklist.md) software, return to the [Policy and Compliance Management setup checklist](../../grc-policy-compliance-implementation/task/policy-compliance-impl-checklist.md) and proceed to the next step.

**Parent Topic:**[Policy and Compliance Management mandatory setup](../../grc-policy-compliance-implementation/concept/policy-compliance-mandatory-setup.md)

**Parent Topic:**[Manage control objectives and policies](../reference/r_PoliciesAndProcedures.md)

