---
title: Smart Assessment response assist skill
description: The GenAI-powered Smart Assessment Response Assist skill automatically drafts answers by using past smart assessments, classic assessments, and supporting documents.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/smart-assessment-engine/ai-generated-responses-for-smart-assessment.html
release: australia
product: Smart Assessment Engine
classification: smart-assessment-engine
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Explore, Now Assist, Smart Assessment Engine, Governance, Risk, and Compliance]
---

# Smart Assessment response assist skill

The GenAI-powered Smart Assessment Response Assist skill automatically drafts answers by using past smart assessments, classic assessments, and supporting documents.

## About Smart Assessment response assist skill

You can trigger draft AI responses while responding, review the proposed answers, and choose whether to accept, modify, or discard them. The approach maintains human oversight and enables for customization as needed. After the responses are created in the assessment, an AI summary is set to available, providing a consolidated view of all AI-generated suggestions for an assessment. The skill works at the template category level, enabling AI-powered response generation for assessments associated with that category.

While responses are being generated, the assessment displays a live progress indicator that reports how many questions have been processed. You can continue working on questions you have already started answering and your manual entries aren't overwritten.

When you generate draft responses, you can turn on the **Auto-apply top suggestions** option. With auto-apply turned on, the highest-ranked suggestion for each question is applied automatically as the response, so that you don't have to apply each suggestion manually. You can still review and edit any auto-applied response before you submit the assessment. With auto-apply turned off, the suggestions are surfaced as cards for you to review and apply manually.

The skill generates responses from two sources, previously answered questions and attached documents. For previously answered questions, the skill searches completed assessments with matching scope. It compares your current question with past ones to find the closest semantic matches and suggests the most relevant responses. For document-based suggestions, users can select up to 5 documents for the skill to analyze. These documents can come from attachments on the assessment instance. The default sources can be customized per template category through a scripted extension point; for details, see [Customizing AI Response Assist sources](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/smart-assessment-engine/customizing-ai-response-assist-sources.md). The skill matches relevant content to available answer choices and suggests the most appropriate response. Assessors can select which documents they want the skill to analyze. Documents must be in PDF, DOCX, JPEG, or PNG format and can be up to 20 MB and 200 pages each. When suggestions from both sources are needed, the skill runs both checks and combines the results for you. When a question has matching suggestions from both sources, the document-based suggestion takes precedence in the suggestion ranking.

**Note:** You can generate draft responses once per user per assessment. If you collaborate with others on the same assessment, each contributor can generate draft responses for themselves. The sources you select when you start drafting are final. Review your previous assessment and document selections carefully before generating responses, as you can't generate draft responses again or change the selected sources for that assessment.

In the document list, each document shows a compatibility state. The following states identify which files the skill can use:

-   **Supported** – the document meets the format, size, and page limits and can be selected.
-   **Unsupported format** – the document is in a file type that the skill can't read; select a PDF, DOCX, JPEG, or PNG file instead.
-   **Size too large** – the document exceeds the 20 MB limit and can't be selected.
-   **Too many pages** – the document exceeds the 200-page limit. The document can be selected, but the skill won't process it for suggestions.

**Note:** The list of supported document formats is controlled by the `sn_smart_ai_assist.allowed_document_types` system property. An administrator can add or remove MIME types from this property to change which document types the skill accepts.

Each question with AI suggestions is marked with an "AI assistance" tag, regardless of whether you have applied, modified, or discarded the suggestion. The tag indicates that suggestions were generated for that question, not that a suggestion was accepted. Use the AI filter to find and review all questions where AI has suggested a response. You can combine the AI filter with other filters, such as **Unanswered** or **Flagged**, to narrow your review further.

Sections and subsections that contain AI suggestions display a sparkle icon next to the section name. Use this icon in the assessment navigation pane to quickly jump to the next section that has AI-generated suggestions. Sections without any AI suggestions don't show the sparkle icon.

AI suggestion cards help assessment responders by offering context-aware suggestions drawn from previous answers to similar questions. When multiple similar answers are available, up to three suggestion cards may appear, each ranked by relevance and referencing its original source for context and reliability. Each card features "Apply" and "Discard" buttons. Selecting Apply inserts the suggested answer into your response, while Discard removes the suggestion card without changing any answer that you have already applied. You can't discard a suggestion that is already applied; deselect the response first if you no longer want to keep it. For long text suggestions, the card shows a truncated preview. Select **View complete answer** to read the full suggested response before deciding whether to apply or discard it.

Each suggestion card references its source, whether a past smart assessment, a classic assessment, or a supporting document. Responders can select the view sources icon \[Omitted image "rec-type-icon-observation.png"\] Alt text: next to a source to open and verify it directly within the same window, without leaving the assessment page. For document-based suggestions, the source preview highlights the snippet within the original document that the suggestion was drawn from, so responders can verify the citation in context.

When adding AI-generated responses to questions:

-   AI suggestions don't override the responses you have already entered manually, preserving and respecting user input.
-   Each user can generate draft responses once per assessment.
-   Your suggestions are private to you, but the applied answer on the assessment is shared with all collaborators, even when collaborating with others. Each contributor can generate draft responses for themselves. Suggestions are based on the documents and previous assessments that each contributor has access to. Two contributors on the same assessment may see different suggestions and a different AI summary. If another contributor has already applied an answer to a question, you see that applied answer when you open the question.
-   The AI summary panel can be collapsed at any time and reopened from the assessment header. The summary reports the percentage of the assessment for which AI suggested answers, along with the count of suggestions that were generated and applied.
-   If the skill can't find any relevant information in the selected sources, the assessment displays a message indicating that no suggestions could be generated. If suggestions were generated for some questions but the skill failed for others, the affected questions display an indicator. Select **Retry** from the AI summary to regenerate the failed suggestions.

**Note:** The AI-generated draft responses are also available for combined assessments.

## Usecase for Smart Assessment response assist skill

Consider a vendor undergoing a Third-Party Risk Management \(TPRM\) security assessment. Vendors frequently receive similar security questionnaires from multiple users. The Smart Assessment Response Assist skill is ideal for this scenario — it draws on two AI sources simultaneously: previously answered assessments and supporting documents. Here's how it works:

-   The system searches completed smart assessments, classic assessments even if not yet migrated to find questions that semantically match the current questionnaire.
-   In parallel, the skill analyzes vendor-maintained documents such as SOC 2 reports, security policies, and Data Processing Agreements \(DPAs\). These documents often contain answers to common security questions. They are provided as direct attachments to the assessment instance, or returned by an implementation of the Smart Assessment Response Assist scripted extension point.
-   Only documents that the user is permitted to view are considered.
-   Matching responses are ranked by relevance, and the top three suggestions are selected.
-   You can review each suggestion, view its source, and choose to apply or discard it. This workflow helps you create high-quality, consistent answers faster, reduces repetitive work, and confirms responses align with company standards.

## Benefits of Smart Assessment response assist skill

-   Reduce time spent on repetitive assessments by reusing validated responses.
-   Marks each question with an "AI assistance" tag and provides filters to track and review AI-supported responses easily.
-   Maintain human oversight — review, accept, or override every suggestion.
-   Improve consistency and quality across responses by drawing on past validated answers.
-   View the source of every AI suggestion, whether from a past smart assessment, classic assessment, or supporting document.
-   Generate AI responses directly from attached documents using document-based AI suggestions.
-   Auto-apply top suggestions to populate the assessment in a single action.
-   Jump to AI-assisted sections using the sparkle icon in the navigation pane.
-   See a real-time progress indicator while responses are being drafted, and continue working on questions you have already started without losing your manual answers.
-   Recover from partial failures with a retry option, so that questions for which no suggestion could be generated initially can be processed again.

