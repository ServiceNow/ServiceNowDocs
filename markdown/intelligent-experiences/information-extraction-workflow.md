---
title: Information Extraction skill workflow
description: Information Extraction is a skill that analyzes documents to provide values for defined fields, table columns, and questions in a use case. It populates ServiceNow records with extracted data from documents.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/information-extraction-workflow.html
release: australia
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [information extraction, document processing, skill workflow]
breadcrumb: [Information Extraction skill, Explore, Content Understanding, Enable AI experiences]
---

# Information Extraction skill workflow

Information Extraction is a skill that analyzes documents to provide values for defined fields, table columns, and questions in a use case. It populates ServiceNow records with extracted data from documents.

## Processing stages

When a document enters a workflow, the Information Extraction skill examines its content and retrieves the requested information according to the use case. The use case defines what to extract from a document and where to write the results. After a use case is configured, the skill follows these stages at run time:

-   **Stage 1: Document task creation**

    A trigger — such as a document upload, an inbound email, or an attachment added to a record — creates a document task.

-   **Stage 2: Prediction**

    The Information Extraction skill processes the document and returns a prediction for each field, table column, or question in the use case.

-   **Stage 3: Review or automation**

    In full automation mode, the predictions populate the fields in the target table. In agent review mode, the document task goes to a fulfiller, who validates or corrects the predicted values.

-   **Stage 4: Completion**

    After the document task is complete, the predictions populate the target fields and the integrated workflow continues.


**Related topics**  


[Content Understanding personas](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/personas.md)

[Predictions in Information Extraction skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/predictions.md)

[Use cases in Information Extraction skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/cu-use-cases.md)

[Automation modes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/automation-modes.md)

