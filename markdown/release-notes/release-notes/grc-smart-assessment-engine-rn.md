---
title: Smart Assessment Engine release notes
description: The ServiceNow Smart Assessment Engine \(SAE\) enables you to create customizable assessment templates with detailed instructions and questions to gather information from assessors. SAE was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 5
---

# Smart Assessment Engine release notes

The ServiceNow® Smart Assessment Engine \(SAE\) enables you to create customizable assessment templates with detailed instructions and questions to gather information from assessors. SAE was enhanced and updated in the Australia release.

## Smart Assessment Engine highlights for the Australia release

[Australia Patch 2](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-patch-2.md)

-   Collaborate inline with question-level flags, question-level comments, and a new Work Notes tab.
-   Draft assessment responses automatically with AI Response Assist, which suggests answers from prior assessments and attached documents with full source traceability.
-   Embed assessments inside any parent record, playbook, or workspace with the new embedded assessments capability and configurable UI Builder properties
-   Update published templates safely with template versioning while preserving auditability of in-flight assessments.
-   Streamline the responder experience with continuous scrolling inside sections and sub-sections, fully hidden conditional questions, multi-filter support on the question list, and scope item fields visible directly in the assessment task list.

[Australia Patch 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-patch-1.md)

-   Edit published templates quickly with inline edits and built‑in audit tracking.
-   Enable efficient, role-based collaboration by allowing primary owners to delegate assessment sections to subject matter experts \(SMEs\).

See [Smart Assessment Engine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/smart-asmnt-engine-landing-page.md) for more information.

**Important:** Smart Assessment Engine is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Australia release

-   **[Now assist for smart assessment engine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/now-assist-for-smart-assessment-engine.md)**

    Starting with version 22.3.5, responders can use AI Response Assist to draft answers to assessment questions and auto-apply the top suggestion — drawing from multiple sources with citations instead of starting from scratch.

    -   **Previous assessments:** Reuse answers from past SAE and classic assessments, eliminating re-entry across annual refreshes, new regulations, and recurring questionnaires.
    -   **Documents:** Generate answers from documents attached to the assessment or pulled from a document management system \(DMS\). Responders can upload or select PDF, Word, and image \(up to 5 documents, 200 pages each\), preview the document, and trace each answer to a source snippet within the original document.
    Responders choose suggestion only mode \(review each suggestion with Apply or Discard\) or Auto-apply mode \(the top suggestion is applied to each question automatically\). Either way, responders can edit any answer before submission.

-   **[Embedded assessments](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/embedded-assessments.md)**

    Starting with version 22.3.X, bring assessments directly into the parent workflow. Embedded assessments run inside host record pages, playbooks, and workflow, letting respondents complete their work without leaving the parent context. Configuration is per template category and doesn't require code change. Embedded assessments inherit read access from the parent record—only users with read access to the parent record can read the embedded assessment.

-   **[Template versioning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/template-versioning.md)**

    Starting with version 22.3.X, update published assessment templates without copying and deprecating the original. When a template manager publishes a new version, the prior version is automatically retired and future assessments use the new version. Template versioning preserves auditability for in-flight assessments while letting template managers publish new versions to reflect corrections, regulatory changes, or annual content refreshes.

    -   A version-info bar on every published template shows the current version and exposes a create new version action that returns the template to Draft.
    -   A full version history view captures who created each version, when, and which prior version it was branched from.
    -   A new Delete template version action is available from the version actions menu.
-   **[SAE Enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/sae-template-designer.md)**

    These SAE enhancements are available in version 22.3.X and later:

    -   Flag individual questions that need attention with a single click. Flags move through three states—Flagged, Resolved, and Unflagged—and every transition is captured in the assessment activity log.
    -   Add comments at the question level so responders, reviewers, and collaborators can resolve clarifications inline instead of relying on email or external tools. A new Work Notes tab next to the Comments tab provides a separate, role-gated conversation for reviewers or administrators.
    -   Hide conditional questions that don't meet their visibility criteria so responders see only the questions relevant to them, eliminating **Skipped** clutter and reducing assessment fatigue.
    -   Scroll continuously through questions within a section or sub-section instead of paginating, giving responders an uninterrupted answer flow.
    -   Apply multiple filters at once on the question list \(for example, **Unanswered** + **Flagged** + **With comments**\) to focus on exactly the questions that need attention.
    -   View scope item fields directly in the assessment task list so reviewers and assignees can see scope context without opening each assessment.
    -   Programmatically create a combined assessment from multiple assessment IDs using any custom logic, removing the need for manual combine actions. For example, combine all control attestations belonging to an entity group into a single assessment.

-   **[Collaboration in assessments](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/collaboration-in-assessments.md)**

    Starting with version 22.3.X, use granular delegation as a primary owner to assign individual assessment sections to SMEs. Respondents can view the entire assessment for context but can edit only their assigned sections. Monitor overall assessment progress and maintain final review and submission capabilities.

-   **[Quick edit for published templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/quick-edit-for-published-templates.md)**

    Starting with version 22.3.X, edit published templates inline as a template manager, including edits to the titles, descriptions, and reader roles.


## UI changes

-   **[Filtering questions in an assessment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/filtering-questions-in-an-assessment.md)**

    Apply multiple assessment filters at once \(for example, **Unanswered** + **AI-assisted**\). The navigation pane dynamically grays out sections with no matching questions so responders see exactly where attention is needed.

-   **[Create an assessment template category](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/sae-asmnt-template-category-create.md)**

    Starting with version 22.3.X, the **Category Role** field in the assessment template category form is replaced with the **Category Roles** field.


## Changed in this release

-   **[Hide conditional questions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/sae-q-text-create.md)**

    Conditional questions that don't meet their visibility criteria are now fully hidden from the assessment and are no longer displayed as **Skipped**. Respondents see only the questions relevant to them, reducing assessment fatigue and eliminating "Skipped" clutter.

-   **[Create an assessment template category](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/sae-asmnt-template-category-create.md)**

    Enables one or more roles to access a template category with the multiselect **Category Roles** field.


## Activation information

Install Smart Assessment Engine by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

**Parent Topic:**[Governance, Risk, and Compliance release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/grc-rn-landing.md)

