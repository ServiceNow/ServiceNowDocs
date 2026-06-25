---
title: Document and visual insights AI agent
description: The document and visual insights AI agent gathers context from user input and document or image attachments, generates the requested information based on the content, and provides the information along with any relevant task details.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/now-assist-in-document-intelligence/document-and-visual-insights-ai-agent.html
release: australia
product: Now Assist in Document Intelligence
classification: now-assist-in-document-intelligence
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [Now Assist, Gen AI, Generative AI, Document Intelligence]
breadcrumb: [Reference, Now Assist in Document Intelligence, Enable AI experiences]
---

# Document and visual insights AI agent

The document and visual insights AI agent gathers context from user input and document orimage attachments, generates the requested information based on the content, and provides the information along with any relevant task details.

## Document and visual insights AI agent overview

The document and visual insights AI agent performs tasks to process documents and images.

-   **Data extraction**

    Extract specific information.

-   **Summarization**

    Summarize the key topics of documents and images.

-   **Question answering \(Q&amp;A\)**

    Answer questions about the document or image content.


The document and visual insights AI agent is not typically used in standalone mode and any use case can access it. For more information on AI agents, see [Now Assist AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/na-ai-agents.md).

AI agents use [role masking](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aia-role-masking.md) to determine which users can access them. Ones installed with Now Assist applications have specific roles that come included with the application. If you select **Users with specific roles** for user access, you must configure the security controls to include these roles. For the instructions to change the security controls, see [Define security controls for an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/define-sec-controls-aia.md).

## AI agent actions

When used, the AI agent may attempt the following actions:

-   Determine the type of task to perform based on information provided by the user.

    -   Data extraction
    -   Summarization
    -   Question answering \(Q&amp;A\)
-   Retrieve the relevant record details.
-   Initiate the process based on the type of task.
-   Provide the task results as directed.
-   Prompt the user to upload a file for processing.
-   Display the results of the AI agent actions in a document view screen.
-   Provide citation sources.
-   Notify the user of task completion and next steps.

**Parent Topic:**[Now Assist in Document Intelligence reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-in-document-intelligence/now-assist-in-document-intelligence-reference.md)

**Related topics**  


[Components installed with Now Assist in Document Intelligence]()

[Data extraction modes in Now Assist in Document Intelligence]()

[Document Intelligence tool for Now Assist Skill Kit]()

[Field types in Now Assist in Document Intelligence]()

[Now Assist in Document Intelligence forms]()

[Limitations in Now Assist in Document Intelligence]()

[Large language models used by Now Assist in Document Intelligence]()

[Languages supported by Now Assist in Document Intelligence]()

