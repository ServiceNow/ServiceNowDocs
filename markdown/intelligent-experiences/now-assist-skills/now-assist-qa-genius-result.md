---
title: Now Assist Q&amp;A Genius Results
description: The Now Assist Q&amp;A Genius Results skill enables users to get answers to their questions from knowledge articles, external sources, and uploaded files directly in the Now Assist panel.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/now-assist-skills/now-assist-qa-genius-result.html
release: zurich
product: Now Assist Skills
classification: now-assist-skills
topic_type: concept
last_updated: "2026-05-07"
reading_time_minutes: 2
breadcrumb: [Skills in the Platform workflow, Now Assist skills, Now Assist AI assets, Enable AI experiences]
---

# Now Assist Q&amp;A Genius Results

The Now Assist Q&amp;A Genius Results skill enables users to get answers to their questions from knowledge articles, external sources, and uploaded files directly in the Now Assist panel.

## Overview of Now Assist Q&amp;A Genius Results

Now Assist Q&amp;A Genius Results answers your questions in the Now Assist panel using content from knowledge base articles, external sources, such as Microsoft SharePoint, Google Drive, and Confluence Cloud, and files you upload. You can also attach images or documents to get answers grounded in that content. Answers are summarized from the most relevant content across one or more sources, so you get a single, consolidated response instead of a list of articles to read through. Each response shows the source so you can refer back to the original article or document. If the skill can't find a relevant answer, it returns a no-result response instead of a generic reply.

The skill supports multi-turn conversations by retaining your conversation history so that follow-up questions are answered in the context of what you previously asked without re-uploading your file or repeating yourself.

The skill is part of the Platform workflow and is turned on by default. To turn it off, navigate to **Now Assist Admin** &gt; **Now Assist Skills** &gt; **Platform** and select **Deactivate skill** on the skill card.

## Use cases

Now Assist Q&amp;A Genius Results is useful in the following use cases:

-   Search across knowledge articles and external sources such as SharePoint or Confluence to get a single consolidated answer.
-   Ask follow-up questions to build on a previous answer within the same session, without repeating context.
-   Upload a screenshot of an error and ask Now Assist what it means and how to resolve it, without describing the image manually in text.
-   Upload a PDF crash log or SLA document and ask questions about its contents, without reading through the full document.

\[Omitted image "now-assist-multiturn-qna.png"\] Alt text: The Now Assist panel displaying an AI-generated answer to the question "What is spam?" with a KB article source reference and next step options.

## Supported file types and limits

You can upload one file per session. The following file types are supported:

-   Images: PNG, JPG \(maximum 10 MB\)
-   Documents: PDF, DOCX \(maximum 10 MB\)

**Parent Topic:**[Now Assist skills in the Platform workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/now-assist-skills/now-assist-on-now-platform.md)

