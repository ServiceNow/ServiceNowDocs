---
title: Create New Impact analysis form
description: Use the Create New Impact analysis form to add details about the business impact analysis, assessments, approvals, and so on in BCM Configurable Workspace.
locale: en-US
release: yokohama
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Create a business impact analysis, Structured workflows for BIAs, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Create New Impact analysis form

Use the Create New Impact analysis form to add details about the business impact analysis, assessments, approvals, and so on in BCM Configurable Workspace.

## Create New Impact analysis form

For description of the field values, see the table.

<table id="table_FloorForm"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Overview tab \(Displayed when an analysis is created.\)

</td></tr><tr><td>

State

</td><td>

Stepper component for the states of the business impact analysis.

</td></tr><tr><td class="sub-head" colspan="2">

Details tab

</td></tr><tr><td>

Name

</td><td>

Name of the business impact analysis. Describe the business impact analysis within 255 characters length.

</td></tr><tr><td>

Template

</td><td>

Template that you can use as a model to create the business impact analysis.The BIA template has the primary elements \(applications, business processes, and locations\), impact categories, and the dependent assets identified for the type of assessment.

</td></tr><tr><td>

Applies to table

</td><td>

Business process, business application, or any other asset that is assessed in the business impact analysis. This field is auto-filled according to the template selected.

</td></tr><tr><td>

Applies to

</td><td>

Process that the analysis applies to.

</td></tr><tr><td>

BCM Lead

</td><td>

BCM lead assigned to the analysis.

</td></tr><tr><td>

Business unit

</td><td>

Table that stores the template's primary element data.

</td></tr><tr><td>

Department

</td><td>

Department that uses the business process. You can select the department based on the business unit selected.

</td></tr><tr><td>

BIA Owner

</td><td>

Person who owns and is responsible for completing the business impact analysis. BCM lead can review the business impact analysis.

</td></tr><tr><td>

Expires

</td><td>

Expiration date for the analysis. This field is auto-filled.

</td></tr><tr><td>

Description

</td><td>

Description of the process.

</td></tr><tr><td class="sub-head" colspan="2">

Results

</td></tr><tr><td>

Maximum tolerable period of disruption

</td><td>

Maximum amount of time that a product or service can be unavailable before it causes unacceptable consequences for an organization.**Note:** Beginning with Yokohama release, you can tag a question in the assessment to a specific field in the BIA or to the entire assessment. Similarly, you can tag questions from multiple assessments to be addressed in the BIA. One question can also provide value for multiple fields.

</td></tr><tr><td>

Recovery time objective

</td><td>

Read-only. System calculated value of the recovery time objective for the impact analysis. Represents the maximum acceptable downtime \(recovery time objective - RTO\) before normal operations are restored for users.

</td></tr><tr><td>

Recovery point objective

</td><td>

Read-only. System calculated value of the recovery point objective for the impact analysis.

</td></tr><tr><td>

Finalized RTO

</td><td>

Column shown in the chart and list views, replacing the previously shown RTO and Adjusted RTO columns. Auto-calculates values according to the values in the **Recovery time objective** and **Adjusted RTO** fields available on the same form.

 The **Finalized RTO** field provides an accurate time calculation and comparison for the RTO.

 It reflects either the original RTO or an adjusted RTO if changes were made during the recovery planning process. If only Recovery Time Objective \(RTO\) is set, the value of the field is set to the RTO itself. If adjusted RTO is set, the value of the field is set to the adjusted RTO.

</td></tr><tr><td>

Finalized RPO

</td><td>

Column shown in the chart and list views, replacing the previously shown RPO and Adjusted RPO columns. Auto-calculates values according to the values in the **Recovery point objective** and **Adjusted RPO** fields available on the same form.

 Finalized value for the recovery point objective \(RPO\). The finalized recovery point objective is the suggested acceptable data loss measured in time from a failure. If there is no adjusted RPO, this is the recovery point objective. If there is an adjusted RPO, this is the adjusted RPO.

 If only RPO is set, the value of the field is set to the RPO itself. If adjusted RPO is set, the value of the field is set to the adjusted RPO.

</td></tr><tr><td>

Confidentiality

</td><td>

Confidentiality information for the analysis.

</td></tr><tr><td>

Availability

</td><td>

Integrity information for the analysis.

</td></tr><tr><td>

Integrity

</td><td>

Confidentiality information for the analysis. You can also have one questionnaire for calculating confidentiality, availability, and integrity of the data and assets in the assessment.

</td></tr><tr><td>

Recovery tier

</td><td>

Recovery tier for the business impact analysis.

</td></tr><tr><td>

Adjusted RTO

</td><td>

RTO that is adjusted manually.

</td></tr><tr><td>

Adjusted RPO

</td><td>

RPO that is adjusted manually.

</td></tr><tr><td class="sub-head" colspan="2">

Compose section

</td></tr><tr><td>

Work notes

</td><td>

Work notes for the business impact analysis. This field is auto-filled.

</td></tr><tr><td>

Activity

</td><td>

Activity details of the BIA such as dates on the field changes, impact, state, severity, and so on.

</td></tr><tr><td class="sub-head" colspan="2">

Icons displayed in the side-bar of the record

</td></tr><tr><td>

Contributors

</td><td>

Icon to populate the side-panel in the record. You can add contributors to the business impact analysis from the panel.

</td></tr><tr><td>

Attachment

</td><td>

Panel where the PDF of the business impact analysis is attached.

</td></tr><tr><td>

Template

</td><td>

Panel to populate the template for the business impact analysis. You can view all or customized templates in this panel.

</td></tr></tbody>
</table>**Parent Topic:**[Create a business impact analysis](../task/create-bia-in-uib-ws.md)

