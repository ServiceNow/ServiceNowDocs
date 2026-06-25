---
title: AI-assisted questionnaire pre-fill using the Document Management System
description: Use the Document Management System \(DMS\) with the Smart Assessment Engine \(SAE\) to automatically generate draft responses for third‑party risk assessment questionnaires using vendor documents and previously answered assessments.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/third-party-risk-management/tprm-dms-sae.html
release: australia
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: concept
last_updated: "2026-05-12"
reading_time_minutes: 4
keywords: [document management, smart assessment engine, vendor risk, third-party risk assessments, AI-assisted questionnaire pre-fill, draft responses]
breadcrumb: [Explore, Third-party Risk Management, Governance, Risk, and Compliance]
---

# AI-assisted questionnaire pre-fill using the Document Management System

Use the Document Management System \(DMS\) with the Smart Assessment Engine \(SAE\) to automatically generate draft responses for third‑party risk assessment questionnaires using vendor documents and previously answered assessments.

## AI-assisted questionnaire pre-fill overview

The Smart Assessment Response Assist skill generates draft responses for assessment questionnaires from two sources: documents stored in the Document Management System \(DMS\) and previously completed assessments. Assessors review, edit, and apply suggestions before submitting — responses are never submitted automatically. The skill is available for both internal and external assessments, with no difference in experience between the two.

When a vendor document is uploaded or updated in DMS, the file and its metadata become available to the skill during active assessments. For previously answered questions, the skill searches completed smart and classic assessments with matching scope, compares questions semantically, and surfaces the most relevant past responses. When both sources are enabled, the skill runs both checks and combines the results.

**Note:** A minimum of 50 completed assessments is required for the previous assessments source to return suggestions. When generating suggestions, the skill draws from the last 10 completed assessments.

The skill determines which past assessments to search based on the level at which the current assessment is being conducted:

-   For assessments conducted at the vendor level, the skill searches only past assessments completed at the vendor level.
-   For assessments conducted at the engagement or element level, the skill searches past assessments for the same engagement first. If no completed assessments are found at the engagement level, the skill falls back to vendor-level assessments.

## How it works

When an assessor selects **Draft responses with AI** in an active assessment, they choose which sources to analyze — previous assessments, documents, or both. For the documents source, assessors can select up to 5 documents from a list that includes attachments on the assessment instance and documents retrieved based on the template category configuration.

Each question with an AI suggestion is marked with an **AI Assistance** tag. Up to three suggestion cards may appear per question, each ranked by relevance and showing its source. Assessors select **Apply** to insert a suggestion or **Discard** to remove it. Applied suggestions can be edited before submission.

Important constraints to be aware of:

-   Each assessor can generate AI suggestions once per assessment. The sources selected at generation time are final and cannot be changed.
-   Suggestions are private to the assessor who generated them. Collaborators must each generate their own suggestions independently.
-   AI suggestions do not override responses already entered manually.
-   Only documents the assessor has permission to access in DMS are available for AI-assisted drafting.

## Key capabilities

-   Document-based drafting: Retrieves and analyzes vendor documents from DMS, including SOC 2 reports, security policies, and Data Processing Agreements, to generate responses to matching questionnaire items.
-   Previous assessment reuse: Searches completed smart and classic assessments for semantically similar questions and surfaces the top matching responses, reducing repetition across recurring questionnaires.
-   Source transparency: Each suggestion card identifies its source — a past smart assessment, a classic assessment, or a document. Assessors can select the source to open and verify it without leaving the assessment page.
-   AI summary: After generation, assessors can select **View AI summary** to see a consolidated count of generated and applied responses. The count updates as responses are manually edited.
-   Configurable document retrieval: Organizations can customize document retrieval behavior for a given assessment by configuring the template category. To further customize retrieval, use the Smart Assessment Response Extension Point \(SmartAsmtResponseAssistExtensionPoint\). For more information, see [Configure AI-assisted questionnaire pre-fill for TPRM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-dms-sae-config.md).

## What to do next

To configure this feature for your TPRM assessments, see [Configure AI-assisted questionnaire pre-fill for TPRM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-dms-sae-config.md).

To use AI-assisted draft responses in an active assessment, see [Generate AI-assisted draft responses in a TPRM assessment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-dms-sae-assess-doc.md).

For information about uploading and managing vendor documents in DMS, see [Document Management system in Third-party Risk Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-dms.md).

**Related topics**  


[Configure AI-assisted questionnaire pre-fill for TPRM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-dms-sae-config.md)

[Generate AI-assisted draft responses in a TPRM assessment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-dms-sae-assess-doc.md)

[Document Management system in Third-party Risk Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-dms.md)

