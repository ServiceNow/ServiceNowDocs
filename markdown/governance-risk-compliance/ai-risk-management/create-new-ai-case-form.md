---
title: Create New AI case form
description: Use the Create New AI case form in the AI Risk and Compliance workspace to report an AI case with the necessary details.
locale: en-US
release: zurich
product: AI Risk Management
classification: ai-risk-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Create an AI case in the AI Risk and Compliance workspace, Use, AI Risk and Compliance, Governance, Risk, and Compliance]
---

# Create New AI case form

Use the Create New AI case form in the AI Risk and Compliance workspace to report an AI case with the necessary details.

See the following table for a description of the field values.

<table id="table_uj1_q5x_nvb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Number of the request. This field is automatically set to a request number.

</td></tr><tr><td>

Name

</td><td>

Name of the AI case. For example, `Credit Scoring Algorithm Glitch`.

</td></tr><tr><td>

Description

</td><td>

Description about the AI case in detail. For example, include information such as the expected recommendation, actual suggestion, context, impact, and steps to reproduce the issue, especially for cases such as Incorrect AI Recommendation.

</td></tr><tr><td>

Type

</td><td>

Type of the AI case. This field is automatically set to **AI case**.

</td></tr><tr><td>

Sub-type

</td><td>

Subtype of the case. For example, Adversarial attacks \(Deliberate manipulation of AI models to produce incorrect results\).

</td></tr><tr><td>

State

</td><td>

Workflow state of the request. This field is automatically set to **New**.

</td></tr><tr><td>

Priority

</td><td>

Urgency of the AI case. It enables the AI case team to triage requests effectively and responds based on how critical the request is. The options are as follows:-   **Critical**
-   **High**
-   **Moderate**
-   **Low**
-   **Planning**

</td></tr><tr><td>

Requester

</td><td>

Name of the person who raised the request.

</td></tr><tr><td>

Requested on behalf of

</td><td>

Name of the person that you created the request for.

</td></tr><tr><td>

Primary entity

</td><td>

Entity impacted by the AI case. Only the entities identified in the impacted areas are available for selection as the primary entity.

</td></tr><tr><td>

Entity owner

</td><td>

User who is the owner of the entity. This field is automatically set based on the entity selected in the Impacted areas related list.

</td></tr><tr><td class="sub-head" colspan="2">

Assignment

</td></tr><tr><td>

Assignment group

</td><td>

Group that is assigned to the request.**Note:** The assignment group is preconfigured to the request type during the configuration setup.

</td></tr><tr><td>

Case analyst

</td><td>

Analyst who analyzes and works on the AI case. The AI case analyst is a part of the Assignment group.

</td></tr><tr><td>

Watch list

</td><td>

Person who must be informed about the AI case.

</td></tr><tr><td>

Accountable executive

</td><td>

Person who is accountable for the AI case.

</td></tr><tr><td class="sub-head" colspan="2">

Primary origin

</td></tr><tr><td>

Location

</td><td>

Location where the AI case occurred. For example, Japan.

</td></tr><tr><td>

Sub-location

</td><td>

Sub location of the AI case occurrence. For example, the sub location is Tokyo.

</td></tr><tr><td>

Impacted business unit

</td><td>

Business unit that is affected by the reported AI case. For example, Finance.

</td></tr><tr><td>

Impacted department

</td><td>

Department that is affected by the AI case. For example, Customer support.

</td></tr><tr><td>

Source

</td><td>

Source of the AI case creation. This field is automatically set to Manual when the case is manually created. If the case is reported from the Employee Center, the field displays the source as Employee Center.

</td></tr><tr><td>

Additional source

</td><td>

Mode of how the AI case is reported when the case is created manually. This field is available only when **Manual** is selected from the **Source** field and the record is saved. The choices are as follows:-   Email
-   Phone

</td></tr><tr><td class="sub-head" colspan="2">

Schedule

</td></tr><tr><td>

Date of occurrence

</td><td>

Date when the AI case occurred. For example, the case may have occurred on 18-02-2025.

</td></tr><tr><td>

Date of discovery

</td><td>

Date when the case was discovered. For example, the case may have occurred on 18-02-2025, but was discovered on 12-03-2025.

</td></tr><tr><td>

Reported date

</td><td>

Date the case is reported.

</td></tr><tr><td>

Case closure SLA

</td><td>

Expected date of case closure.

</td></tr><tr><td>

Investigation planned start

</td><td>

Planned start date to investigate the case.

</td></tr><tr><td>

Investigation actual start

</td><td>

Actual start date of case investigation.

</td></tr><tr><td>

Remediation planned start

</td><td>

Planned start date to remediate the case.

</td></tr><tr><td>

Remediation actual start

</td><td>

Actual start date of case remediation.

</td></tr><tr><td>

Investigation planned end

</td><td>

Planned end date to investigate the case.

</td></tr><tr><td>

Investigation actual end

</td><td>

Actual end date of case investigation.

</td></tr><tr><td>

Remediation planned end

</td><td>

Planned end date of case remediation.

</td></tr><tr><td>

Remediation actual end

</td><td>

Actual end date of case remediation.

</td></tr><tr><td class="sub-head" colspan="2">

Breach analysis

</td></tr><tr><td>

Breach status

</td><td>

Status to indicate if a breach has occurred or not. The choices are as follows:-   **To be determined**: This value is the default value.
-   **Breach detected**: If the breach is confirmed.
-   **Future potential**: If the breach hasn’t occurred but may occur in the future.
-   **Not a breach**: When there’s no breach detected.

</td></tr><tr><td>

Breach start

</td><td>

Date the breach started. This field only appears when **Breach detected** or **Future potential** is selected from the **Breach status** field.

</td></tr><tr><td>

Reporting status

</td><td>

Status of the AI case being reported to the regulators. This field is automatically set based on the reporting status of the regulations associated with the case. If an AI case has many regulations and even if one regulation is identified as reportable, then the reporting status of the case is set to **Reportable**. The default value of this field is **To be determined**.

</td></tr><tr><td>

Breach end

</td><td>

Date the breach ended. This field only appears when **Breach detected** or **Future potential** is selected from the **Breach status** field.

</td></tr><tr><td>

Breach significance identified

</td><td>

Date when the user identifies that the breach is significant. This field only appears when **Breach detected** or **Future potential** is selected from the **Breach status** field.

</td></tr><tr><td class="sub-head" colspan="2">

Root cause analysis

</td></tr><tr><td>

Primary cause

</td><td>

Primary cause of the AI case occurrence. This field is automatically set to the primary cause that is selected in the Cause and consequences related list.

</td></tr><tr><td>

Primary consequence

</td><td>

Consequences of the primary cause for the AI case.

</td></tr><tr><td>

Overall observations

</td><td>

Observations made regarding the AI case.

</td></tr><tr><td>

Remediation taken

</td><td>

Field to indicate if remediation measures have been taken to address the AI case. The choices are as follows:-   **Yes**
-   **No**

</td></tr><tr><td>

Overall preventive measures

</td><td>

Preventive measures taken toward the case.

</td></tr><tr><td class="sub-head" colspan="2">

Activity

</td></tr><tr><td>

Work notes \(Private\)

</td><td>

Notes or information about the request.

</td></tr><tr><td>

Additional comments \(Customer visible\)

</td><td>

Additional information about the request that you want to share with your customers.

</td></tr></tbody>
</table>**Parent Topic:**[Create an AI case in the AI Risk and Compliance workspace](../task/create-ai-case-in-the-ai-risk-and-compliance-workspace.md)

