---
title: Control Requirement Details View
description: The CAM view of the Control form has fields that have been added to capture the control requirement details.
locale: en-US
release: zurich
product: Continuous Risk Monitoring
classification: continuous-risk-monitoring
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Reference, Continuous Authorization and Monitoring, Governance, Risk, and Compliance]
---

# Control Requirement Details View

The CAM view of the Control form has fields that have been added to capture the control requirement details.

To accommodate the control requirement details in the CAM view of a Control objective form a Control objective requirements related list is added.

**Note:** The views of the Control objective form and Control form in the CAM view are almost the same as the Control objective and Control forms used in Policy and Compliance Management. However, some fields have been removed and some added in the forms to capture the control requirement details.

## CAM view of a Control objective form

<table id="table_FloorForm"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Reference

</td><td>

Unique numerical identifier or the content reference number.

</td></tr><tr><td>

Family

</td><td>

Control objectives grouped into a family.

</td></tr><tr><td>

Active

</td><td>

Option to activate a control objective.

</td></tr><tr><td>

Family ID

</td><td>

Unique identification for a family of control objectives.

</td></tr><tr><td>

Name

</td><td>

Name of the control objective.

</td></tr><tr><td>

Source

</td><td>

Source of the control objective, which is NIST 800-53 revision 5 for which the test templates are provided.

</td></tr><tr><td>

Parent

</td><td>

Control objective that is not a child of the current control objective. This relationship is to avoid cyclic parent – child relationship.

</td></tr><tr><td>

Compliance Score \(%\)

</td><td>

Compliance score percentage calculated for this control objective and its color code: -   80 and higher in green
-   80 to 50 in yellow
-   below 50 in red

</td></tr><tr><td>

Creates controls automatically

</td><td>

Option to indicate that controls are automatically created when an entity is associated from the Additional entities related list by selecting **Add relationship** and the entity.

</td></tr><tr><td>

Create control requirements

</td><td>

Option to generate control requirements automatically for the control objective.**Note:** If there are no control objective requirements, then there won’t be any control requirements either.

</td></tr><tr><td>

Attestation

</td><td>

Reference to the metric type. **GRC Attestation** is chosen by default.**Note:** If the user changes the control attestation, the related control objective attestation type is changed also.

</td></tr><tr><td>

Impact

</td><td>

Potential impact to business functions because of loss of confidentiality, integrity, or availability of target and data.

</td></tr><tr><td>

Organizational guidance

</td><td>

Security control definitions from NIST, which when designated as common control definitions by organizations, are inheritable by one or more organizational targets.

</td></tr><tr><td>

Description

</td><td>

Description of the control objective.

</td></tr><tr><td>

Supplemental guidance

</td><td>

If it is control objective sourced by NIST 800-53 revision 4, then a direction for the control objective implementation.

</td></tr><tr><td>

Discussion

</td><td>

If it’s a control objective sourced by NIST 800-53 revision 5, then content-related information that is sourced by NIST.

</td></tr></tbody>
</table>Control objectives are just guidelines and aren’t specific to an entity or any object. You can link one control objective with any control objective requirement, and one control objective requirement with any number of control objectives, as the relationship between the control objective and the control objective requirement is many-to-many.

|Field|Description|
|-----|-----------|
|Requirement number|Requirement number of the control objective.|
|Active|Option to make the requirement active.|
|Description|Detailed description about the requirement for the control objective.|

In the Control objective requirements related list, you can select **New** to create a requirement for the control objective if necessary, based on which requirements are generated. Or, select **Edit** to add an existing control objective requirement to the control objective.

**Note:**

-   If the control objective is in the Inactive state, you cannot create or add control objective requirements. Therefore, **New** and **Edit** are not available.
-   If the control objective requirement is inactive, you cannot add a control objective to the control objective requirement.

## CAM view of the Control form

<table id="table_psx_jhy_qzb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Reference

</td><td>

Unique identifier.

</td></tr><tr><td>

Name

</td><td>

Name of the control.

</td></tr><tr><td>

Number

</td><td>

Unique identification number of the control.

</td></tr><tr><td>

Entity

</td><td>

Related entity.**Note:** If you change the state of the entity to Active from Retired state, then the manually created control on the entity also moves to the Draft state.

</td></tr><tr><td>

Control objective

</td><td>

Related control objective.

</td></tr><tr><td>

Owner

</td><td>

User who owns the policy.**Note:** The owner is always added as a respondent. The control owner that you select belongs to the owning group.

</td></tr><tr><td>

Status

</td><td>

Control status. Possible choices are:-   **Compliant**
-   **Non-compliant**
-   **Not applicable**

</td></tr><tr><td>

State

</td><td>

Control state. Possible choices are: -   **Draft**: When the control is created from a control objective, controls are in this state. In this state, all compliance users can modify the control. Only available when creating a one-off control. One-off controls are possible but not recommended.
-   **Attest**: When you select **Attest** and take attestations, the control moves to this state.

**Note:** When a control is set back to draft, the attestation is canceled.

-   **Review**: Controls are automatically moved to review from the attestation phase.
-   **Monitor**: In this state, all compliance managers can move the control from review to monitor.
-   **Retired**: Compliance managers or administrators can move a control from Monitor to Retired.

**Note:** When a control is retired:

    -   Associated indicators don’t run
    -   Associated attestations are canceled
    -   Changes to associated control objectives don’t update the control

</td></tr><tr><td>

Authorization package

</td><td>

The authorization package that the control is associated with or originating from.

</td></tr><tr><td>

Frequency

</td><td>

List of options:-   Event Driven
-   Daily
-   Weekly
-   Monthly
-   Quarterly
-   Semi-Annually
-   Annually

Attestation is sent based on the value selected for the control or control requirement.

**Note:** For information on the difference between the **Frequency** field for a control and the **Attestation Frequency** field in an entity, see [KB0694607](https://support.servicenow.com/kb_view.do?sysparm_article=KB0694607).

</td></tr><tr><td>

Weighting

</td><td>

Value used when calculating control score effectiveness.

</td></tr><tr><td>

Owning group

</td><td>

Group that owns the policy.

</td></tr><tr><td>

Control allocation

</td><td>

Type of control that is created: either system-specific or hybrid.

</td></tr><tr><td>

Description

</td><td>

Description of the control.

</td></tr><tr><td>

Discussion

</td><td>

Content-related information from NIST 800-53 revision 5.

</td></tr><tr><td>

Supplemental guidance

</td><td>

If it’s a control sourced by NIST 800-53 revision 4, then a direction for the control implementation.

</td></tr><tr><td>

Implementation statement

</td><td>

An explanation on how the control will be implemented.This information is required if the control is created from an authorization package and in the Draft state.

</td></tr><tr><td class="sub-head" colspan="2">

Attestation

</td></tr><tr><td>

Take attestation at requirement level

</td><td>

Option to send attestations at the control requirement level and not at the control level.

</td></tr><tr><td>

Attestation

</td><td>

Select from a list of options.

 -   Other attestation types can be configured.
-   If this field is populated, then the **Attestation Respondents** value is required, and the owner is made the respondent.

 **Note:** If the user changes the attestation type in the control objective, all related controls are also changed.

</td></tr><tr><td>

Attestation respondents

</td><td>

-   Users assigned to the attestation of this control.
-   Only a user with the sn\_grc.user role can be added as a respondent.

**Note:** When both the **Attestation** and **Attestation respondents** fields are set, attestations are created when you select **Attest**.

</td></tr><tr><td class="sub-head" colspan="2">

Activity Journal

</td></tr><tr><td>

Additional comments

</td><td>

Public information about the control.

</td></tr><tr><td>

Activities

</td><td>

Message logs of control state change.

</td></tr></tbody>
</table><table id="table_dwg_zqz_qzb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Control requirement's unique number.

</td></tr><tr><td>

Requirement number

</td><td>

Reference number.

</td></tr><tr><td>

Control

</td><td>

Control to which the control requirement is associated.

</td></tr><tr><td>

Status

</td><td>

Status of the control requirement.

</td></tr><tr><td>

State

</td><td>

Requirement state.

</td></tr><tr><td>

Frequency

</td><td>

Control frequency.

</td></tr><tr><td>

Description

</td><td>

Description of the control requirement.

</td></tr><tr><td class="sub-head" colspan="2">

Attestation

</td></tr><tr><td>

Attestation

</td><td>

Attestation metric type.

</td></tr><tr><td>

Attestation respondents

</td><td>

Users who attest the control requirement.

</td></tr><tr><td class="sub-head" colspan="2">

Activity Journal

</td></tr><tr><td>

Additional comments

</td><td>

Information about the control requirement.When the control objective requirement is dissociated, that is removed or deleted, the control requirement becomes manual. This information is logged in this field.

</td></tr><tr><td>

Activities

</td><td>

Message logs of control requirement's state change.

</td></tr></tbody>
</table>**Parent Topic:**[CAM reference](../concept/reference-grc-cam.md)

