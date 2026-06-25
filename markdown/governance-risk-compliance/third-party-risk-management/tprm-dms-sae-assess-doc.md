---
title: Generate AI-assisted draft responses in a TPRM assessment
description: Use the Smart Assessment Response Assist skill to generate draft responses for assessment questionnaires using vendor documents from the Document Management System \(DMS\) and previously completed assessments.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/third-party-risk-management/tprm-dms-sae-assess-doc.html
release: australia
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: task
last_updated: "2026-05-12"
reading_time_minutes: 4
keywords: [AI-assisted questionnaire pre-fill, draft responses, smart assessment, DMS, third-party risk]
breadcrumb: [Assess third-party risk, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Generate AI-assisted draft responses in a TPRM assessment

Use the Smart Assessment Response Assist skill to generate draft responses for assessment questionnaires using vendor documents from the Document Management System \(DMS\) and previously completed assessments.

## Before you begin

-   The Smart Assessment Response Assist skill is active and template categories are configured for draft response generation.

    For more information, see [Configure AI-assisted questionnaire pre-fill for TPRM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-dms-sae-config.md).

-   SAE is enabled as the assessment engine.

    For more information, see [Smart assessment configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-sae-assessment-config.md).

-   You have permission to view and respond to assessments.

    For more information, see [Respond to an internal assessment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-irq-respond-to.md) and [Respond to a questionnaire for a third party or engagement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-respond-for-tp.md).

-   Upload vendor documents to DMS before running the assessment.

    For more information, see [Document Management system in Third-party Risk Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-dms.md).


**Note:** You can generate AI suggestions once per assessment. The sources you select at generation time are final and can't be changed. A minimum of 50 completed assessments is required for the **Previous assessments** source to return suggestions. When generating, the skill draws from the last 10 completed assessments.

Role required: snc\_internal \(internal assessments\). For external assessments, primary contacts can complete all assessment response actions; secondary contacts must be assigned read and write access.

## About this task

The skill generates draft responses from two sources: documents stored in DMS and previously completed assessments. You can use one or both sources. Suggestions are private to you. Collaborators must generate their own suggestions. AI suggestions don't override responses you have already entered manually.

## Procedure

1.  Open the assessment assigned to you.

    -   1.  In the My active items pane, select **GRC tasks**.
2.  In the My to-dos section, select the number that corresponds to the assessment state to open the list of assessments.
3.  Select the TPRM assessment that you want to respond to.
    -   1.  Log in to the Third-party portal at `https://<instance-name>.service-now.com/svdp`.
2.  Select the Assessments tab.
3.  Select the assessment and questionnaire you want to respond to.
    -   For internal assessments, navigate to your workspace and open the assessment from your assigned tasks.
    -   For external assessments, open the assessment in the Third-party portal.
2.  Select **Draft responses with AI**.

3.  Select the sources for the skill to analyze in the **Draft responses with AI** dialog box.

    1.  Turn on **Previous assessments** to search previously answered questions from completed assessments you have access to.

        You can generate AI suggestions once per assessment. The sources you select at generation time are final and can't be changed. A minimum of 50 completed assessments is required for the **Previous assessments** source to return suggestions. When generating, the skill draws from the last 10 completed assessments.

    2.  Turn on **Documents** to view the available documents.

    3.  From the documents list, select up to five documents you want the skill to analyze.

        The list includes documents retrieved based on the template category configuration, and any files attached directly to the assessment instance. To use a document not in the list, upload it as an attachment to the assessment and it appears as an available option. For supported document types and file size limits, see [Limitations in Now Assist in Document Intelligence](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-document-intelligence-limitations.md).

    4.  Select **Generate draft responses**.

4.  After generation completes, select **View AI summary** to see a consolidated count of generated responses.

    The AI summary count decreases as you manually edit applied responses. You can also use the **AI Assistance** filter to find all questions where AI has suggested a response.

5.  Review each AI suggestion card.

    Each suggestion card shows its source: a past smart assessment, a classic assessment, or a document. Select the source to open and verify it directly without leaving the assessment page. Up to three suggestion cards may appear per question, ranked by relevance.

6.  Select **View sources** to verify the source before applying a suggestion.

7.  Accept or remove each suggestion.

    Select **Apply** to accept a suggestion or **Discard** to remove it. Applied suggestions can be edited before submission. Selecting Apply does not submit the assessment.

8.  Complete all required questions and select **Submit**.

9.  In the **Submit** dialog box, review the AI summary and select the confirmation check box.

10. Select **Submit**.

    After submission, the assessment is locked and responses cannot be edited.


## Result

The assessment contains AI-generated draft responses based on the selected DMS documents and completed assessments. Review and edit each response before submitting.

**Related topics**  


[AI-assisted questionnaire pre-fill using the Document Management System](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-dms-sae.md)

[Configure AI-assisted questionnaire pre-fill for TPRM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-dms-sae-config.md)

[Document Management system in Third-party Risk Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-dms.md)

