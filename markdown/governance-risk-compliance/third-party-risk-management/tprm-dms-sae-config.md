---
title: Configure AI-assisted questionnaire pre-fill for TPRM
description: Turn on AI-assisted questionnaire pre-fill for a smart assessment template category by selecting the Is AI response enabled check box.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/third-party-risk-management/tprm-dms-sae-config.html
release: australia
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: task
last_updated: "2026-05-27"
reading_time_minutes: 2
keywords: [Now Assist, Third-party Risk Management, Smart Assessment Engine, DMS, document-assisted drafting, AI-assisted questionnaire pre-fill]
breadcrumb: [Smart Assessment Engine assessments, Configure, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Configure AI-assisted questionnaire pre-fill for TPRM

Turn on AI-assisted questionnaire pre-fill for a smart assessment template category by selecting the **Is AI response enabled** check box.

## Before you begin

-   Now Assist for Smart Assessment Engine is installed and the Smart Assessment Response Assist skill is active.

    For more information, see [Activate smart assessment response assist skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/smart-assessment-engine/activate-smart-assessment-response-assist-skill.md).

-   Smart Assessment Engine is enabled and your TPRM smart assessment and questionnaire templates are active.

    For more information, see [Smart assessment configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-sae-assessment-config.md).

-   Documents relevant to the assessment are available in the Document Management System \(DMS\).

    For more information, see [Document Management system in Third-party Risk Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-dms.md).


Roles required:

-   Third-party risk admin \[sn\_vdr\_risk\_asmt.vendor\_risk\_admin\]
-   Now Assist admin \[sn\_nowassist\_admin.nsa\_admin\]
-   Script writer — required to edit the SmartAsmtResponseAssistExtensionPoint script.

## About this task

When the Smart Assessment Response Assist skill is active and template categories are configured for AI-assisted responses, the skill uses the assessment context to retrieve relevant documents from DMS and make them available for document-assisted drafting in TPRM smart assessments.

Assessors can review the retrieved documents and use them to generate draft responses. Generated content must be reviewed and submitted manually as part of the assessment workflow.

## Procedure

1.  Navigate to **All** &gt; **Generative AI** &gt; **Smart Assessment Engine** &gt; **Template Categories**.

2.  Select the template category associated with the assessment you want to configure.

3.  Select the **Is AI response enabled** check box.

    A default script is provided as part of seeded TPRM template categories. You can copy or adapt this script when creating or modifying template categories. To customize retrieval behavior, use the Smart Assessment Response Extension Point \(SmartAsmtResponseAssistExtensionPoint\).


## Result

Relevant documents from DMS are available during smart assessments to support AI-assisted drafting. Assessors can review these documents and generate draft responses as part of the assessment process.

## What to do next

To use AI-assisted drafting in an active assessment, see [Generate AI-assisted draft responses in a TPRM assessment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-dms-sae-assess-doc.md).

**Related topics**  


[AI-assisted questionnaire pre-fill using the Document Management System](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-dms-sae.md)

[Generate AI-assisted draft responses in a TPRM assessment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-dms-sae-assess-doc.md)

[Document Management system in Third-party Risk Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-dms.md)

