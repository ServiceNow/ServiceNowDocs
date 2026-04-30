---
title: Create a control using the Compliance Workspace
description: Controls are automatically generated when you associate a policy with an entity type, or an entity type with a control objective, or when an entity is added to a control objective. A control is created for each entity listed in the entity type for the control objective. Controls can also be manually created using the Compliance Workspace.
locale: en-US
release: yokohama
product: GRC: Compliance Management Workspace
classification: grc-compliance-management-workspace
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 6
breadcrumb: [Manage controls using the Compliance Workspace, Using the Compliance Workspace, Performing compliance tasks in Compliance Workspace, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Create a control using the Compliance Workspace

Controls are automatically generated when you associate a policy with an entity type, or an entity type with a control objective, or when an entity is added to a control objective. A control is created for each entity listed in the entity type for the control objective. Controls can also be manually created using the Compliance Workspace.

## Before you begin

Role required: sn\_compliance\_ws.corporate\_compliance\_analyst, sn\_compliance\_ws.corporate\_compliance\_manager, sn\_compliance\_ws.it\_compliance\_manager

## Procedure

1.  Navigate to **All** &gt; **Policy and Compliance** &gt; **Compliance Workspace**.

2.  Select the **Create** list and click **Control**.

3.  On the form, fill in the fields.

<table id="table_FloorForm"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Unique identification number.

</td></tr><tr><td>

Name

</td><td>

Name of the control.

</td></tr><tr><td>

Entity

</td><td>

Related entity.**Note:** If you change the state of the entity to Active from Retired state, then the manually created control on the entity also moves to the Draft state.

</td></tr><tr><td>

Status

</td><td>

Control status. Possible choices are:-   **Compliant**
-   **Non-compliant**
-   **Not applicable**


</td></tr><tr><td>

Inherit from control objective

</td><td>

Option to indicate whether the control is created through an item generation process. For more information, see [Multiple controls for a unique entity–control objective combination](../../grc-policy-and-compliance/concept/support-multiple-controls-same-entity-control-objective.md).

</td></tr><tr><td>

State

</td><td>

Control state. Possible choices are: -   **Draft** In this state, all compliance users can modify the control. Only available when creating a one-off control. One-off controls are possible but not recommended.
-   **Attest** When the control is created from a control objective, the controls are in this state.

**Note:** When a control is set back to draft, the attestation is canceled.

-   **Review** Controls are automatically moved to review from the attestation phase.
-   **Monitor** In this state, all compliance managers can move the control from review to monitor.
-   **Retired** Compliance managers or administrators can move a control from Monitor to Retired.

**Note:** When a control is retired:

    -   Related indicators do not run
    -   Associated attestations are canceled
    -   Changes to the associated control objectives do not update the control


</td></tr><tr><td>

Key control

</td><td>

Indicator that the control is a key control.

</td></tr><tr><td>

Exempt

</td><td>

Mark the control as exempted.

</td></tr><tr><td>

Control Objective

</td><td>

Related control objective. If you're creating a common control, you must select a control objective.

</td></tr><tr><td>

Enforcement

</td><td>

List of options:-   Mandated
-   Voluntary


</td></tr><tr><td>

Function

</td><td>

Read-only function field. All controls created are **Standard control** by default. When you convert the control to a common control, the value changes to **Common control**.

</td></tr><tr><td>

Weighting

</td><td>

Weight used to calculate the control failure factor of a risk. Set the weighting between one and 10.

</td></tr><tr><td>

Frequency

</td><td>

Frequency at which the control is tested. This field is for the control's testing and reporting purpose.List of options:-   Event Driven
-   Daily
-   Weekly
-   Monthly
-   Quarterly
-   Semi-annually
-   Annually
**Note:** For information on the difference between the**Frequency** field for a control and the**Attestation Frequency** field in an entity, see [KB0694607](https://support.servicenow.com/kb_view.do?sysparm_article=KB0694607).

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

Description

</td><td>

Description of the control.

</td></tr><tr><td>

Additional Information

</td><td>

Additional information about the control.

</td></tr><tr class="sub-head"><td class="sub-head" colspan="2">

Assignment

</td></tr><tr><td>

Owning group

</td><td>

Group that owns the policy.

</td></tr><tr><td>

Owner

</td><td>

User that owns the policy.**Note:** The owner is always added as a respondent. The control owner that you select belongs to the owning group.

</td></tr><tr><td class="sub-head" colspan="2">

Attestation

</td></tr><tr><td>

Attestation method

</td><td>

Defaults to Classic attestation.-   Classic attestation: ServiceNow AI Platform classic method of control assessment.
-   Attestation: Method by which controls are assessed.


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

Take attestation at requirement level

</td><td>

Option to generate attestation tasks for each control requirement.This provides the ability to attest compliance at the control requirement level, not just at the control level.

If a control requirement fails attestation, an issue is generated. The issue status impacts the parent control and rolls up to the entity and control objective level.

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

5.  Click **Save**.

    The control is created and all related lists are visible.

    If you had created a common control, then there are Reliant entities and Reliant entity types related lists along with other related lists of the control. Use the Reliant entities related list to associate entities to the common control. Or, you can use the Reliant entity types related list to add a group of entities of an entity type instead of associating them one by one.

    ![Related lists to associate entities as reliant entities.](../image/RelEntitiesRelList.png "Related lists for common controls")

    **Note:** For more information on the reliant entity association for a common control, see [Convert standard control to common control and add reliant entities](convert-standard-control-common.md).

6.  From the **Overview** page, click the **Issues**.

    You can add existing one or more related issues to the control that you created. By mapping the existing issues to the control, you can reduce the count of open issues on the document.

    When you add an issue to a control, a record is created associating the item that is the control with the issue, in the Issue to Control \[sn\_grc\_m2m\_issue\_item\] table.

    1.  To add an issue to the control, click the **Add** button.

    2.  Select the issue or issues related to the control from the Issues pop-up.

    3.  Click the **Add** button.

        The selected issues are added to the control as related issues. You can also create an issue for the control by clicking the **New** button.

    4.  To remove an issue that is already added to the control, select the issue and click **Remove**.

        The associated record mapping between the issue and control is removed from the Issue to Item table.

        **Note:** The UI action buttons such as New, Add, Remove aren’t available if the control is in Retired state.


