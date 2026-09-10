---
title: Create a question bank
description: Create a question bank in the Smart Assessment Engine application to store questions that you can reuse across multiple assessment templates.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/governance-risk-compliance/smart-assessment-engine/sae-asmnt-question-bank-create.html
release: zurich
product: Smart Assessment Engine
classification: smart-assessment-engine
topic_type: task
last_updated: "2026-09-03"
reading_time_minutes: 1
breadcrumb: [Question bank, Use template designer, Manage, Smart Assessment Engine, Governance, Risk, and Compliance]
---

# Create a question bank

Create a question bank in the Smart Assessment Engine application to store questions that you can reuse across multiple assessment templates.

## Before you begin

-   At least one active template category with a QB category role that matches one of your roles must exist. See [Create an assessment template category](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/smart-assessment-engine/sae-asmnt-template-category-create.md).
-   Role required: sn\_smart\_asmt.question\_bank\_manager or sn\_smart\_asmt.assessment\_admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Assessment Workspace**.

2.  Select \[Omitted image "question-bank.png"\] Alt text: Question bank icon.

    The question bank hub lists every question bank that you have access to.

3.  Create a question bank by selecting **Create question bank**, and then fill in the question bank details form.

    |Field|Description|
    |-----|-----------|
    |Question bank name|Unique meaningful name for the question bank.|
    |Description|Text that helps others to understand what the question bank is used for.|
    |Purposes|Multi-select field that specifies one or more purposes for the question bank. A template manager can add questions from this question bank to a template only when at least one purpose matches the template's purpose.|

4.  Select **Save**.


## What to do next

You can now add sections and questions to the question bank. See [Add sections and questions to a question bank](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/smart-assessment-engine/sae-asmnt-question-bank-populate.md).

**Related topics**  


[Create an assessment template category](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/smart-assessment-engine/sae-asmnt-template-category-create.md)

[Add sections and questions to a question bank](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/smart-assessment-engine/sae-asmnt-question-bank-populate.md)

