---
title: Extract key information from documents
description: Use key information extraction \(KIE\) to extract structured data from documents with a predefined template, for processing standardized documents such as invoices, contracts, or forms.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/extract-key-information.html
release: australia
topic_type: task
last_updated: "2026-08-17"
reading_time_minutes: 1
breadcrumb: [Content insights AI agent, Use, Content Understanding, Enable AI experiences]
---

# Extract key information from documents

Use key information extraction \(KIE\) to extract structured data from documents with a predefined template, for processing standardized documents such as invoices, contracts, or forms.

## Before you begin

Before using KIE, verify that a use case \(task definition\) is created and configured for your document schema. Have the task definition name, the names of the keys to extract, and either the sys\_id of the task definition or search terms that match its name.

Role required: sn\_aia.admin

## About this task

Use KIE when you:

-   Have a predefined task definition \(template\) for your document type.
-   Want to extract specific, structured fields consistently.
-   Are processing multiple documents of the same type.

**Note:** If you request an extraction, for example "extract X and Y," without providing a task definition, the agent treats the request as a question-and-answer \(QnA\) request instead.

## Procedure

1.  Configure the Content Insights AI agent.

    For more information, see [Configure Content insights AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/configure-content-insights-ai-agent.md).

2.  Open the ServiceNow Otto panel or ServiceNow Otto for Virtual Agent.

3.  Start the AI agent by entering an initial message.

    Include the document that the agent should process.

4.  Specify the task definition.

    Provide the task definition sys\_id for the fastest processing, or use search terms that match your task definition name. For example:

    -   `Extract the values in the attachment of incident INC001234. Use task definition sys_456.`
    -   `Extract data from attachment sys_123 of record INC001234. Use task definition sys_987.`
    If you don't provide a task definition, the agent prompts you for a sys\_id or search query. For example, entering `Extract the values in the attachment of incident INC001234` causes the agent to ask for a task definition before proceeding.

5.  Confirm the task definition when prompted.

    When the agent displays search results, confirm which task definition to use before extraction proceeds.


## Result

The agent displays the extracted values and provides a link to the full extraction results. Processing time varies with document size and schema complexity.

