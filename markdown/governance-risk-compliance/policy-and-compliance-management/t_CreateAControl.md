---
title: Create a control
description: Controls are automatically generated when you associate a policy with an entity type or an entity type with a control objective. A control is created for each entity listed in the entity type for the control objective. Controls can also be manually created.
locale: en-US
release: xanadu
product: Policy and Compliance Management
classification: policy-and-compliance-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Manage controls, Using the Classic user interface for Policy and Compliance tasks, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Create a control

Controls are automatically generated when you associate a policy with an entity type or an entity type with a control objective. A control is created for each entity listed in the entity type for the control objective. Controls can also be manually created.

## Before you begin

Role required: sn\_compliance.admin or sn\_compliance.manager

## Procedure

1.  Navigate to **All** &gt; **Policy and Compliance** &gt; **Controls** &gt; **All Controls**.

2.  Click **New**.

3.  On the form, fill in the fields.

<table id="table_FloorForm"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the control.

</td></tr><tr><td>

Number

</td><td>

Unique identification number.

</td></tr><tr><td>

Entity

</td><td>

Related entity.**Note:** If you change the state of the entity to Active from Retired state, then the manually created control on the entity also moves to the Draft state.

</td></tr><tr><td id="mutliple-control-entity-co">

Inherit from control objective

</td><td>

Option to indicate whether the control is created through item generation process. For more information, see [Multiple controls for a unique entity–control objective combination](../concept/support-multiple-controls-same-entity-control-objective.md).

</td></tr><tr><td>

Control Objective

</td><td>

Related control objective.

</td></tr><tr><td>

Owning group

</td><td>

Group that owns the policy.

</td></tr><tr><td>

Owner

</td><td>

User that owns the policy.**Note:** The owner is always added as a respondent. The control owner that you select belongs to the owning group.

</td></tr><tr><td>

Key control

</td><td>

Indicator that the control is a key control.

</td></tr><tr><td>

Weighting

</td><td>

Value used to calculate the control score effectiveness. Based on the control weighting, in the control score effectiveness value is calculated ​

</td></tr><tr><td>

Status

</td><td>

Control status. Possible choices are:-   **Compliant**
-   **Non-compliant**
-   **Not applicable**


</td></tr><tr><td>

State

</td><td>

Control state. Possible choices are: -   **Draft** In this state, all compliance users can modify the control. Only available when creating a one-off control. One-off controls are possible but not recommended.
-   **Attest** When the control is created from a control objective, controls are in this state.

**Note:** When a control is set back to draft, the attestation is canceled.

-   **Review** Controls are automatically moved to review from the attestation phase.
-   **Monitor** In this state, all compliance managers can move the control from review to monitor.
-   **Retired** Compliance managers or administrators can move a control from Monitor to Retired.

**Note:** When a control is retired:

    -   Associated indicators do not run
    -   Associated attestations are canceled
    -   Changes to associated control objectives do not update the control


</td></tr><tr><td>

Exempt

</td><td>

Mark the control as exempted.

</td></tr><tr><td>

Enforcement

</td><td>

List of options:-   Mandated
-   Voluntary


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

Classification

</td><td>

List of options:-   Preventive
-   Corrective
-   Detective
-   IT Impact Zone


</td></tr><tr><td>

Frequency

</td><td>

Frequency at which the control is tested. This field is for the control's testing and reporting purpose.List of options:

-   Event Driven
-   Daily
-   Weekly
-   Monthly
-   Quarterly
-   Semi-Annually
-   Annually
**Note:** For information on the difference between the**Frequency** field for a control and the**Attestation Frequency** field in an entity, see [KB0694607](https://support.servicenow.com/kb_view.do?sysparm_article=KB0694607).

</td></tr><tr><td>

Description

</td><td>

Description of the control.

</td></tr><tr><td>

Additional Information

</td><td>

Additional information about the control.

</td></tr><tr><td class="sub-head" colspan="2">

Assignment

</td></tr><tr><td>

Owning group

</td><td>

Group that owns the control.

</td></tr><tr><td>

Owner

</td><td>

User that owns the control.

</td></tr><tr><td class="sub-head" colspan="2">

Attestation

</td></tr><tr><td>

Attestation

</td><td>

Select from a list of options.

 -   Other attestation types can be configured.
-   If this field is populated, then the **Attestation Respondents** field automatically becomes mandatory, and the owner is made the respondent.
 **Note:** If the user changes the attestation type in the control objective, all the related controls are changed also.

</td></tr><tr><td>

Attestation respondents

</td><td>

-   Users assigned to the attestation of this control.
-   Only a user with the sn\_grc.user role can be added as a respondent.
**Note:** When both the **Attestation** and **Attestation respondents** fields are set, attestations are created when you click **Attest**.

</td></tr><tr><td>

Attestation frequency

</td><td>

Frequency at which attestations on the control are triggered. If the field has no value selected, then the associated entity's **Attestation frequency** value defaults to this field.Options for attestation frequency:

-   Daily
-   Weekly
-   Monthly
-   Quarterly
-   Semi-Annually
-   Annually
**Note:** After the attestation is complete, the control moves to Review and Monitor states. The control is then monitored for its next due date of attestation. You have the option to trigger the control's attestation frequency based on the attestation's **Created date** or the last completed attestation's **Updated date**. This option is based on the value in **Trigger control attestations based on the created or updated date of the last completed attestation** system property.

</td></tr><tr><td class="sub-head" colspan="2">

Activity Journal

</td></tr><tr><td>

Additional comments

</td><td>

Public information about the control.

</td></tr></tbody>
</table>4.  Select **Copy entity frequency** related link to copy the value of the **Attestation frequency** field of the entity to the **Attestation frequency** field of the control.

    When you select the **Copy entity frequency** related link, the respective entity’s attestation frequency gets copied to the **Attestation frequency** field in the Attestation section of the control table, and does not update the **Frequency** field of the control table.

5.  Click **Submit**.


## What to do next

After you create a control, you can convert the control to a common control and add reliant entities and reliant entity types to it. For more information, see [Testing common control and implementing results on multiple reliant entities](../../grc-workspace-compliance/concept/common-controls-multiple-rel-entities.md).

