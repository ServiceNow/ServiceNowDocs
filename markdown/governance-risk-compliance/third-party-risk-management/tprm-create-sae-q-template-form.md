---
title: Create New TPRM SAE questionnaire template form
description: Use the Create New TPRM questionnaire template form to capture all the information that you need to create a TPRM SAE questionnaire template using the Smart Assessment template designer. As a third-party risk admin, you can create a questionnaire template.
locale: en-US
release: zurich
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Third-party \(external\) risk assessment management, Reference, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Create New TPRM SAE questionnaire template form

Use the Create New TPRM questionnaire template form to capture all the information that you need to create a TPRM SAE questionnaire template using the Smart Assessment template designer. As a third-party risk admin, you can create a questionnaire template.

<table id="table_krg_p53_2yb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Template name

</td><td>

Unique meaningful name for the template.

</td></tr><tr><td>

Third-party risk area

</td><td>

The third-party risk area that applies to this questionnaire template.

 **Note:** This option is only available when you create an internal or external questionnaire template using the Vendor Management Workspace.

</td></tr><tr><td>

Purpose

</td><td>

Purpose for the new template.

**Note:** Known as Template classifications in the Classic assessment engine, TPRM has a **Purpose** for each classic template classification.

TPRM purpose options include:

-   TPRM external 3rd-party element questionnaire
-   TPRM external 4th-party questionnaire
-   TPRM external document request
-   TPRM external questionnaire
-   TPRM internal IRQ
-   TPRM internal tiering questionnaire

To view a TPRM TPRM questionnaire template you must have the TPR assessment reviewer role \[sn\_vdr\_risk\_asmt.vendor\_assessment\_reviewer\]. For more information on creating assessment template purposes, see [Create an assessment template category](../../assessment-engine/task/sae-asmnt-template-category-create.md)

**Note:** You can create an assessment only from a published assessment template. You can update a published template only if no active assessment is associated with the template.

</td></tr><tr><td>

Include previous responses

</td><td>

Option to pre-populate the questionnaire with responses from a completed questionnaire \(state is **Complete**\).

**Important:** If you have the TPR assessor \[sn\_vdr\_risk\_asmt.vendor\_assessor\] role, you can override the option that is specified in the questionnaire template while editing a questionnaire in the draft state.

 The entry in the Third-party portal notifies the third-party contact that responses were copied. The notification includes a link to the assessment that supplied the responses and its last updated date.

 -   The responses are populated when the new questionnaire is submitted to the third-party contact.
-   The source questionnaire must be based on the same template as the current questionnaire.
-   The responses are populated from the most recently completed questionnaire.
-   Answers of the attachment, duration, and signature type aren’t copied.
-   The setting can’t be changed after the questionnaire is sent to the third party.

 To specify the maximum age for source questionnaires, configure the **Maximum age for reusing responses** `sn_vdr_risk_asmt.max_age_for_questionnaire_reuse` system property. See [Configure TPRM properties](../../grc-vendor-risk-implementation/task/tprm-properties-configure.md).

 **Note:** This option is only available when you create a questionnaire template using the Vendor Management Workspace.

</td></tr><tr><td>

Instructions

</td><td>

Information that a responder might find useful when responding to a questionnaire.

</td></tr></tbody>
</table>**Parent Topic:**[Third-party \(external\) risk assessment management](../../grc-workspace-vrm/reference/tprm-ws-dd-mgt-pg-extrnl-assessment.md)

**Related topics**  


[Create a TPRM SAE questionnaire or document request template](../task/create-sae-q-template.md)

