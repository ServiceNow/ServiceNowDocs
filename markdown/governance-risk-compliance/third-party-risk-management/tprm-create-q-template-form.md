---
title: Assessment metric type form
description: Use the assessment metric type form to capture all the information that you need to create a questionnaire template using the Third-party Risk Management application. As a third-party risk admin, you can create a questionnaire template.
locale: en-US
release: australia
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Third-party \(external\) risk assessment management, Reference, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Assessment metric type form

Use the assessment metric type form to capture all the information that you need to create a questionnaire template using the Third-party Risk Management application. As a third-party risk admin, you can create a questionnaire template.

<table id="table_FloorForm"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The name of the template.

</td></tr><tr><td>

Third-party risk area

</td><td>

Select the third-party risk domain that applies to the type of third party that will receive the questionnaire or document request. For example, if you select the Security risk domain, then only third parties that are assigned that risk domain will receive the questionnaire or document request.

 For more information, see [Define a third-party risk domain](../task/tprm-risk-domain-define.md).

</td></tr><tr><td>

Third-party signature required

</td><td>

Option to require the third party's primary contact to provide an electronic signature in the Third-party portal.**Note:** You can use electronic signatures to certify that the third-party contact has successfully reviewed and approved the questionnaire responses or document request.

</td></tr><tr><td>

Reviewer signature required

</td><td>

Option to require the reviewer to review the validity of the assessment responses and provide an electronic signature as final approval.

</td></tr><tr><td>

Description

</td><td>

A description for the template.

</td></tr><tr><td>

Include previous responses

</td><td>

Option to pre-populate the questionnaire with responses from a completed questionnaire \(state is **Complete**\).

**Important:** If you have the TPR assessor \[sn\_vdr\_risk\_asmt.vendor\_assessor\] role, you can override the option that is specified in the questionnaire template while editing a questionnaire.

 The entry in the Third-party portal notifies the third-party contact that responses were copied. The notification includes a link to the assessment that supplied the responses and its last updated date.

 -   The responses are populated when the new questionnaire is submitted to the third-party contact.
-   The source questionnaire must be based on the same template as the current questionnaire.
-   The responses are populated from the most recently completed questionnaire.
-   Answers of the attachment, duration, and signature type aren’t copied.
-   The setting can’t be changed after the questionnaire is sent to the third party.

 To specify the maximum age for source questionnaires, configure the **Maximum age for reusing responses** `sn_vdr_risk_asmt.max_age_for_questionnaire_reuse` system property. See [Configure TPRM properties](../../grc-vendor-risk-implementation/task/tprm-properties-configure.md).

</td></tr></tbody>
</table>**Parent Topic:**[Third-party \(external\) risk assessment management](../../grc-workspace-vrm/reference/tprm-ws-dd-mgt-pg-extrnl-assessment.md)

**Related topics**  


[Create a questionnaire or document request template](../task/create-questionnaire-template.md)

[Create a questionnaire or document request template using the Designer](../task/create-question-template.md)

[Assessing your third-party risk](../concept/tprm-assessing-tpr.md)

