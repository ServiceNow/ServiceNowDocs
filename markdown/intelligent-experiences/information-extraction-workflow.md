---
title: Information Extraction skill workflow
description: Information Extraction is a skill that analyzes documents to provide values for defined fields, table columns, and questions in a use case. It populates ServiceNow records from documents without manual data entry.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/information-extraction-workflow.html
release: australia
topic_type: concept
last_updated: "2026-08-17"
reading_time_minutes: 1
breadcrumb: [Information Extraction skill, Explore, Content Understanding, Enable AI experiences]
---

# Information Extraction skill workflow

Information Extraction is a skill that analyzes documents to provide values for defined fields, table columns, and questions in a use case. It populates ServiceNow records from documents without manual data entry.

## Processing stages

When a document enters a workflow, the skill examines its content and retrieves the requested information according to the use case. These values may include specific field data, table entries, or responses to particular questions. The skill processes each document based on the use case set by the administrator. The use case defines what to extract from a document and where to write the results. At run time, the skill follows these stages:

1.  A trigger, such as a document upload, an inbound email, or an attachment added to a record, creates a document task.
2.  The Information Extraction skill processes the document and returns a prediction for each field, table column, or question in the use case.
3.  In full automation mode, the predictions populate the fields in the target table. In agent review mode, the document task goes to a fulfiller, who validates or corrects the predicted values.
4.  After the document task is complete, the predictions populate the target fields, and the integrated workflow continues.

**Related topics**  


[Content Understanding personas](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/personas.md)

[Predictions in Information Extraction skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/predictions.md)

[Use cases in Information Extraction skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/cu-use-cases.md)

[Automation modes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/automation-modes.md)

