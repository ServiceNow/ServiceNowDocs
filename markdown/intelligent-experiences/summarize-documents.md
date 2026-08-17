---
title: Summarize documents and images
description: Use the Content Insights AI agent to generate a concise summary of document or image from a record reference or uploaded attachment.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/summarize-documents.html
release: australia
topic_type: task
last_updated: "2026-08-17"
reading_time_minutes: 1
breadcrumb: [Content insights AI agent, Use, Content Understanding, Enable AI experiences]
---

# Summarize documents and images

Use the Content Insights AI agent to generate a concise summary of document or image from a record reference or uploaded attachment.

## Before you begin

Role required: AI Agent Admin \[sn\_aia.admin\]

## About this task

Use summarization when you need a high-level overview of document or image, are reviewing multiple attachments, or need to understand a document's purpose before reviewing its details.

Summarization requires only a document or image, provided by record reference or upload.

## Procedure

1.  Configure the Content Insights AI agent.

    For more information, see [Configure the Content Insights AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/configure-content-insights-ai-agent.md).

2.  Open the ServiceNow Otto panel or ServiceNow Otto for Virtual Agent.

3.  Start the AI agent by entering a request.

    Provide the document or image that you want the agent to process.

4.  Request a summary using clear language.

    Include the word "summarize" or "summary" in your request, and specify which document or attachment to summarize.


## Result

The agent displays a concise summary of the document or image.

## Example utterances

Basic requests:

``

-   `"Summarize these attachments."`
-   `"Provide a summary of the uploaded document."`
-   `"What does this file contain? Summarize it."`

With record references:

-   `"Summarize the attachment from incident INC001234."`
-   `"Summarize the document attached to record TASK123456."`
-   `"Summarize the images attached to INC001234."`

With an attachment sys\_id:

-   `"Write a summary of the attachment with sys_id ABC123."`
-   `"Give me a summary of attachment sys_id 12234 from table incident."`

