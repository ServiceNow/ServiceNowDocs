---
title: Smart Assessment Engine release notes
description: The ServiceNow Smart Assessment Engine application enables you to create customizable assessment templates with instructions and questions to gather information from assessors.Smart Assessment Engine, version 23.0, introduces a centralized question bank, assessment delegation, question-level change history, and UX enhancements.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/grc-smart-assessment-engine-rn.html
release: brazil
topic_type: topic
last_updated: "2026-09-10"
reading_time_minutes: 3
keywords: [smart assessment engine, smart assessment engine, question bank, delegation, change history]
breadcrumb: [Governance, Risk, and Compliance release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# Smart Assessment Engine release notes

The ServiceNow® Smart Assessment Engine application enables you to create customizable assessment templates with instructions and questions to gather information from assessors.

## About Smart Assessment Engine

-   Create customizable assessment templates with structured instructions and questions to gather information from assessors.
-   Reuse questions across multiple assessment templates with a centralized question bank.
-   Collaborate on assessments with question-level comments, work notes, flags, and change history, and delegate assessments to another user when needed.
-   Score and report on assessment results to gain actionable insights.

See [Smart Assessment Engine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/smart-asmnt-engine-landing-page.md) for more information.

## Activation and other requirements

**Note:** Smart Assessment Engine is available in the ServiceNow Store. For details, see the following activation information.

-   **Activation information**

    Install Smart Assessment Engine by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).


**Parent Topic:**[Governance, Risk, and Compliance release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/grc-rn-landing.md)

## September 2026

Smart Assessment Engine, version 23.0, introduces a centralized question bank, assessment delegation, question-level change history, and UX enhancements.

### What's new

-   **[Question bank](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/question-bank.md)**

    With Smart Assessment version 23.0.2, you can create, manage, and reuse questions across multiple assessment templates with a centralized question bank. Questions move through a Draft, Ready to publish, Published, and Retired lifecycle. Add published questions to assessment templates as independent copies. Changes to the original or the copy don't affect each other.

-   **[Migrate a classic question bank or assessment template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/sae-asmnt-migrate-question-bank.md)**

    With Smart Assessment Migration Tools version 23.0.3, you can migrate an existing classic question bank or the sections and questions of a Smart Assessment template into a new or existing question bank. Track migration status and review errors from the Question Bank Migrations list.

-   **[Delegation in Smart Assessment Engine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/delegation-in-sae.md)**

    With Smart Assessment version 23.0.2, you can delegate your assessments to another user for a set period using the platform delegation feature. A delegate of the primary responder can respond to and submit the assessment; a delegate of the requestor can cancel, reassign, and edit the due date. Delegation is off by default and is enabled from the template category.

-   **[Question change history](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/sae-question-change-history.md)**

    With Smart Assessment version 23.0.2, you can review a log of every response, justification, and flag-state change made to a question throughout the lifecycle of an assessment, including who made each change and when. Consecutive changes to the same field by the same user within a configurable time window are merged into a single entry, while flag-state changes are logged individually.


### What's changed

-   **[Create an assessment template category](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/sae-asmnt-template-category-create.md)**

    With Smart Assessment version 23.0.2, the assessment template category form includes two new fields: **QB category roles**, which controls access to the question banks associated with the category, and **Allow user delegation**, which lets users delegate their assessments in the category.

-   **UX improvements to assessment questions and responses**
    -   [Drop-down list question](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/sae-q-drop-down-create.md) — With Smart Assessment Designer version 23.0.5, reopening a drop-down list question now shows all response options again, not just the ones you previously selected.
    -   [Reference question search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/sae-respond-to-asmnt.md) — With Smart Assessment Core version 23.0.2, for single-select and multi-select reference questions, when a table has more than 10 matching records, select the search icon to browse the full set. This replaces the default behavior of showing only the first 10 records.
    -   [Default focus when opening or reopening an assessment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/sae-respond-to-asmnt.md) — With Smart Assessment Core version 23.0.2, the view defaults to the assessment instructions, if configured, or the first question of the first section or subsection. This applies even if you, a collaborator, or response automation has already answered later questions.

