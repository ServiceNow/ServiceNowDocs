---
title: Content insights AI agent
description: The Content insights AI agent understands documents and images, answers questions, extracts structured data, and summarizes content within a single interface.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/cu-content-insights-ai-agent.html
release: australia
topic_type: concept
last_updated: "2026-08-17"
reading_time_minutes: 1
breadcrumb: [Explore, Content Understanding, Enable AI experiences]
---

# Content insights AI agent

The Content insights AI agent understands documents and images, answers questions, extracts structured data, and summarizes content within a single interface.

The Content insights AI agent processes context from user inputs and attached documents or images. It generates the requested information based on this content and returns it with any relevant task details. You can incorporate the agent into an agentic workflow to enhance document and image understanding within a multi-step automated process.

You configure the Content insights AI agent in AI Agent Studio. Sometimes, the AI agent uses a use case that extracts relevant fields and saves them to the target table. The use case is configured within the Information Extraction skill in the AI Admin Hub.

**Note:** AI-generated output may be inaccurate. Review all content the agent generates before using it in business processes.

You can provide documents or images to the agent in either of the following ways:

-   **Reference a record**

    Provide a record number, such as INC0010003, or a sys\_id and table name. The agent retrieves all attachments from that record.

-   **Upload a file directly**

    Upload a document or image directly in the chat window.


## Supported content

The Content insights AI agent processes documents and images, such as PDF, DOCX, PNG, and JPEG files.

## Agent capabilities

The agent provides three capabilities:

-   **Question and answer \(QnA\)**

    Ask specific questions about documents and images and get accurate answers with citations.

-   **Key information extraction \(KIE\)**

    Extract structured data using predefined templates.

-   **Document summarization**

    Get concise summaries of document and image content.


**Note:** Interact with the agent directly. The agent orchestrates the underlying tools automatically.

**Related topics**  


[Extract information from documents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/cu-extract-information-from-document.md)

[Use cases in Information Extraction skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/cu-use-cases.md)

