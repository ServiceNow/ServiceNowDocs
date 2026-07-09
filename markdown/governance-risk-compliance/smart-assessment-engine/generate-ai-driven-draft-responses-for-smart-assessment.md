---
title: Generate AI-driven draft responses for smart assessment
description: In Smart Assessment Engine, use generative AI to create draft responses for assessment questions by analyzing context and using previously answered similar questions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/smart-assessment-engine/generate-ai-driven-draft-responses-for-smart-assessment.html
release: australia
product: Smart Assessment Engine
classification: smart-assessment-engine
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Use generative AI skills, Now Assist, Smart Assessment Engine, Governance, Risk, and Compliance]
---

# Generate AI-driven draft responses for smart assessment

In Smart Assessment Engine, use generative AI to create draft responses for assessment questions by analyzing context and using previously answered similar questions.

## Before you begin

Role required: sn\_smart\_asmt.actor

The **Is AI response enabled** option must be selected on the template category that the assessment is created from. For configuration details, see [Create an assessment template category](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/smart-assessment-engine/sae-asmnt-template-category-create.md).

## About this task

When you’re assigned to a task to respond to an assessment, you submit your responses to the assessment within the relevant workspace. For example, smart assessments are available for use with Control attestation and Risk identification. Your responses can help with gathering evidence to prove that a control is implemented or help identify gaps that can lead to potential risk.

## Procedure

1.  Navigate to your workspace and then to your list of assessments.

    Here’s an example of how to navigate to this list in the Compliance Workspace.

    1.  Navigate to **All** &gt; **Policy and Compliance** &gt; **Compliance Workspace**.
    2.  Select the tasks icon \(\[Omitted image "TasksIcon.jpg"\] Alt text: Tasks icon.\).
    3.  Select the **Control attestations** on the left panel.
    4.  In the **My pending tasks** related list, the assessments are displayed.
2.  Navigate to your list of assigned assessments and select an assessment.

3.  On the assessment, select **Draft responses with AI**.

4.  On the **Draft responses with AI** dialog box, select what you want the skill to analyze:

    1.  Turn on **Previous assessments** to search previously answered questions from completed assessments you have access to.

    2.  Turn on **Documents** to view the available documents.

    3.  From the list of available documents, select the ones you want the skill to analyze for generating responses.

    4.  Turn on **Auto-apply top suggestions** to automatically apply the highest-ranked suggestion to each question.

        You can still review and edit any auto-applied response before submitting the assessment. The assessment is not submitted automatically.

    5.  Select **Generate draft responses**.

    **Note:**

    -   To use a document that is not in the list, upload it as an attachment to the assessment and it will appear as an available option.
    -   You can select up to 5 documents per assessment. Each document must be in PDF, DOCX, JPEG, or PNG format and can be up to 20 MB and 200 pages.
    -   For supported document types and file size limits, see [Limitations in Now Assist in Document Intelligence](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-document-intelligence-limitations.md).
    -   The sources you select are final. After you generate draft responses, you can't change the selected sources or run the AI feature again for this assessment. Review your selections carefully before continuing.
5.  Review the AI‑generated suggestions and select **View sources** to view the source details

    \[Omitted image "suggestion\_source\_details.png"\] Alt text: Source details for an AI-generated suggestion.

6.  After reviewing the suggestion and its sources, select **Apply** to accept a suggestion or **Discard** to remove it.

    If you did not turn on **Auto-apply top suggestions** when you started the skill, suggestions aren't applied automatically. Each suggestion is displayed as a card for you to review. When multiple similar answers exist, up to three AI suggestion cards may appear, each with “Apply” and “Discard” options.

    \[Omitted image "AI\_suggestion\_card.png"\] Alt text: An AI suggestion card showing Apply and Discard options.

7.  If the AI summary indicates that some suggestions could not be generated, select **Retry** to regenerate the failed suggestions.

    If the skill could not find any relevant information in the selected sources, the assessment displays a message stating that no suggestions were generated. In that case, you respond to the questions manually.

8.  Complete all required questions and select **Submit**.

9.  On the **Submit** dialog box, select the check box to confirm you have reviewed all answers and understand that no further changes can be made after you submit.

    Before submitting, review the AI summary in the Submit dialog box to understand and verify all AI-generated contribution.

10. Select **Submit**.


## Result

The assessment is submitted with your reviewed AI-assisted responses.

