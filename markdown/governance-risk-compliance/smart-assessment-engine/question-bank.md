---
title: Question bank
description: A question bank is a centralized repository for creating, managing, and reusing questions with preconfigured settings. Use it to share questions across multiple assessment templates without re-creating them.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/smart-assessment-engine/question-bank.html
release: australia
product: Smart Assessment Engine
classification: smart-assessment-engine
topic_type: concept
last_updated: "2026-09-03"
reading_time_minutes: 3
keywords: [question bank, assessment questions, question repository, question lifecycle, assessment templates]
breadcrumb: [Use template designer, Manage, Smart Assessment Engine, Governance, Risk, and Compliance]
---

# Question bank

A question bank is a centralized repository for creating, managing, and reusing questions with preconfigured settings. Use it to share questions across multiple assessment templates without re-creating them.

## Question bank overview

The question bank supports the same question types as assessment templates and adds dedicated user roles and a publishing workflow for managing questions independently of any single template. The question bank hub is the central landing page within the Assessment Workspace. From this hub, you can access every question bank that you have access to, create question banks, and manage the question lifecycle across your organization. You can also migrate a classic question bank or an existing assessment template into a question bank. See [Migrate a classic question bank or assessment template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/smart-assessment-engine/sae-asmnt-migrate-question-bank.md).

**Note:** This feature is available starting with Australia Patch 2.

\[Omitted image "question-bank-hub.png"\] Alt text: Question bank hub listing question banks with their template name, description, purposes, draft and published question counts, and a Create question bank button to create a question bank.

## Access to question banks

Access to a question bank depends on both a base question bank role and a category role. A base question bank role, such as **question\_bank\_manager** or **question\_bank\_reader**, lets you create or view question banks in general. You also need one of the roles configured in that category's **Question bank category roles** field, which controls access to question banks associated with that specific category. For more information, see [Roles installed in Smart Assessment Engine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/smart-assessment-engine/sae-roles-defined.md) and [Create an assessment template category](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/smart-assessment-engine/sae-asmnt-template-category-create.md).

## Question lifecycle

Questions in a question bank follow a structured lifecycle with four states:

|State|Description|
|-----|-----------|
|**Draft**|The question is being created or edited and isn't available to add to templates.|
|**Ready to publish**|The question is complete and waiting for a question bank manager to publish it.|
|**Published**|The question is available for template managers to add to assessment templates.|
|**Retired**|The question is no longer available for new imports but continues to work in templates that already added it.|

Each question card includes a state menu that authorized users use to move a question through these stages. You can also select multiple ready-to-publish questions and publish them together. For more information, see [Publish questions in a question bank](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/smart-assessment-engine/sae-asmnt-question-bank-publish.md).

## Limitations of question bank questions

A question bank question isn't tied to a single assessment template, so some question attributes aren't available while the question lives in a question bank:

-   Conditional visibility isn't supported on question bank questions, because it depends on other questions in a specific template.
-   Response automation isn't supported on question bank questions.
-   Scoring isn't supported on question bank questions.
-   Post-assessment actions aren't supported on question bank questions.

The following condition types are supported on question bank questions and carry over when a template manager adds the question to a template:

-   Justification conditions
-   Attachment conditions
-   Preferred answer conditions

## Question bank and template independence

When a template manager adds a question from a question bank to an assessment template, the system creates an independent copy of the question in the template. After the copy is added:

-   Changes to the original question in the question bank don't affect any copy that was already added to an assessment template.
-   Changes to a copy in an assessment template don't affect the original question in the question bank or copies of that question in other assessment templates.

Each copy is independent. Template managers can further configure a copy, such as adding scoring or conditional visibility, without affecting the question bank or other templates that use the same question.

