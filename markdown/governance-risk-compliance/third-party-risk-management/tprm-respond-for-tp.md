---
title: Respond to a questionnaire for a third party or engagement
description: Answer questions, modify responses, or submit external questionnaires for a third party or engagement by using Third-party Risk Management. You can save valuable time by responding for a third party or engagement when they have already provided the required information for a previous questionnaire.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/third-party-risk-management/tprm-respond-for-tp.html
release: brazil
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Assess third-party risk, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Respond to a questionnaire for a third party or engagement

Answer questions, modify responses, or submit external questionnaires for a third party or engagement by using Third-party Risk Management. You can save valuable time by responding for a third party or engagement when they have already provided the required information for a previous questionnaire.

## Before you begin

The **Allow assessors to answer/edit questionnaires for third-party contacts** property \(**sn\_svdp.allow\_assessor\_edit**\) must be active. For more information on configuring this property, see [Configure TPRM properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/tprm-properties-configure.md).

Role required: sn\_vdr\_risk\_asmt.vendor\_assessor, sn\_vdr\_risk\_asmt.vendor\_risk\_manager, sn\_vdr\_risk\_asmt.vendor\_risk\_admin

**Important:** The **sn\_svdp.allow\_assessor\_edit** property applies only to Classic assessments. If your instance uses Smart Assessment Engine \(SAE\), this property has no effect and external assessment responses remain read-only for TPR assessors and TPR managers, even when the assessment is in the **Submitted to third party** state.

To edit responses for an external SAE assessment, TPR assessors \[sn\_vdr\_risk\_asmt.vendor\_assessor\] and TPR managers \[sn\_vdr\_risk\_asmt.vendor\_risk\_manager\] can use the assessment reassign \[sn\_smart\_asmt.reassign\] role, which is available to both roles by default, to reassign the in-progress assessment to themselves during the review process. Once reassigned, they are granted edit access to the responses. For more information on reassigning questionnaires, see [Smart assessments with Third-party Risk Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/tprm-sae-using.md).

## Procedure

1.  Navigate to **All** &gt; **Self-Service** &gt; **Third-party risk management** &gt; **External risk assessments** &gt; **All open**.

2.  Select the External assessment \(VRA\) number of an assessment that is in the **Draft** or **Submitted to third party** state.

3.  On the Risk overview tab, in the Questionnaires and document requests section, select the **Name** or **Questionnaire instance** to open the questionnaire that you want and then fill in the questions.

    **Note:** To respond to a questionnaire using a questionnaire template, see [Using a Microsoft Excel spreadsheet template for external questionnaires](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/tprm-excel-template-support.md) and [Respond using a Microsoft Excel template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/tprm-tpcontact-use-excel.md).

4.  Select **Submit**.


