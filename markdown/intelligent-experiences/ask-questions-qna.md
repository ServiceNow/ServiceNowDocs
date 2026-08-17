---
title: Ask questions about documents and images
description: Use question and answer \(QnA\) to ask the Content Insights AI agent specific questions about document or image and get cited answers. QnA is the agent's default mode.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/ask-questions-qna.html
release: australia
topic_type: task
last_updated: "2026-08-17"
reading_time_minutes: 1
keywords: [QnA, question and answer, Content Insights, document analysis]
breadcrumb: [Content insights AI agent, Use, Content Understanding, Enable AI experiences]
---

# Ask questions about documents and images

Use question and answer \(QnA\) to ask the Content Insights AI agent specific questions about document or image and get cited answers. QnA is the agent's default mode.

## Before you begin

Role required: sn\_aia.admin

## About this task

Use QnA when you:

-   Have a specific question about document or image.
-   Want to classify or categorize a document.
-   Want to extract values without a predefined template.
-   Are asking multiple questions about one or more attachments.

QnA requires a document or image, provided by record reference or upload, and your specific question.

**Note:** The agent may produce inaccurate results. Review all AI-generated answers before using them.

## Procedure

1.  Configure the Content Insights AI agent.

    For more information, see [Configure Content insights AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/configure-content-insights-ai-agent.md).

2.  Open the ServiceNow Otto panel or ServiceNow Otto for Virtual Agent.

3.  Start a conversation with the agent by typing an utterance.

    Include the document, image, incident, or record that you need the agent to process.

4.  Ask your question in natural language.

    -   Ask clear, specific questions, such as `What is the total invoice amount?` rather than `Tell me about the invoice.`
    -   Use simple language and avoid complex logic or conditionals.
    -   Combine multiple questions into a single query, such as `What is the effective date, termination clause, and governing law?`
    -   Frame requests as questions starting with words such as `What`, `Who`, `When`, or `How much`.
5.  Review the AI-generated response.

    Verify the answer against the source document before using the results.


## Result

The agent displays the answer with citations from the source document or image.

## Example utterances

With uploaded documents:

-   `What is the main obligation in this document?`
-   `Who are the parties in the attached file?`
-   `What type of document is this?`
-   `What are the confidentiality terms in this PDF?`

With record references:

-   `What is the subject of the document attached to incident INC001234?`
-   `Who is the client in the file attached to record TASK123456?`
-   `What are the payment terms in the document linked to TASK456789?`
-   `What is shown in the screenshot attached to INC001234?`

With an attachment sys\_id:

-   `What is the governing law in attachment sys_id abc123?`
-   `Who wrote the document with sys_id 123 from table abc?`

