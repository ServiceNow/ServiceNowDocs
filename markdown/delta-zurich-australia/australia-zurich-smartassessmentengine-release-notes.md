---
title: Combined Smart Assessment Engine release notes for upgrades from Zurich to Australia
description: Consolidated page of all release notes for Smart Assessment Engine from Zurich to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-zurich-australia/australia-zurich-smartassessmentengine-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-08-17"
reading_time_minutes: 8
breadcrumb: [Products combined by family]
---

# Combined Smart Assessment Engine release notes for upgrades from Zurich to Australia

Consolidated page of all release notes for Smart Assessment Engine from Zurich to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Smart Assessment Engine release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Zurich to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Smart Assessment Engine to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Australia, new features were introduced for Smart Assessment Engine.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   **[Collaboration in assessments](https://www.servicenow.com/docs/access?context=collaboration-in-assessments&family=zurich&ft:locale=en-US)**

Enhance assessments with the new collaboration feature, enabling owners to add multiple contributors to work together in real time. This update enables assessors to collaborate efficiently by adding several contributors to an assessment. Real-time updates reflect each contributor's changes, and presence indicators show who is present on the assessment.

-   **[Normalization in assessments](https://www.servicenow.com/docs/access?context=normalization-in-assessment&family=zurich&ft:locale=en-US)**

Adjust assessment scores to a common scale to promote fair comparison and prioritization. This normalization process helps standardize these measurements, enabling different metrics or scores to be evaluated on the same scale.

-   **[Creating code questions](https://www.servicenow.com/docs/access?context=sae-q-code-create&family=zurich&ft:locale=en-US)**

Capture data quickly and accurately from physical documents using a new barcode and QR code question type for assessments. By scanning barcodes or entering QR codes, the system can instantly retrieve and input relevant information.

-   **[Creating an assessment template from legacy metric types](https://www.servicenow.com/docs/access?context=sae-asmnt-template-migrating&family=zurich&ft:locale=en-US)**

Migrate question dependencies with an improved migration utility, which now supports the check box question type and conditional visibility criteria defined on templates.

-   **[Combining assessments and copying responses](https://www.servicenow.com/docs/access?context=combine-assessments&family=zurich&ft:locale=en-US)**

Combine assessments from different templates into a single, streamlined view. Eliminating the need to open each assessment separately, preserving context, and improving efficiency.


</td></tr><tr><td>

Australia

</td><td>

-   **[ServiceNow Otto for SAE](https://www.servicenow.com/docs/access?context=servicenow-otto-for-smart-assessment-engine&family=australia&ft:locale=en-US)**

Starting with version 22.3.5, responders can use AI Response Assist to draft answers to assessment questions and auto-apply the top suggestion — drawing from multiple sources with citations instead of starting from scratch.

    -   **Previous assessments:** Reuse answers from past SAE and classic assessments, eliminating re-entry across annual refreshes, new regulations, and recurring questionnaires.
    -   **Documents:** Generate answers from documents attached to the assessment or pulled from a document management system \(DMS\). Responders can upload or select PDF, Word, and image files \(up to 5 documents, 200 pages each\). Responders can also preview documents and trace each answer to a source snippet.
Responders choose suggestion only mode \(review each suggestion with Apply or Discard\) or Auto-apply mode \(the top suggestion is applied to each question automatically\). Either way, responders can edit any answer before submission.

-   **[Embedded assessments](https://www.servicenow.com/docs/access?context=embedded-assessments&family=australia&ft:locale=en-US)**

Starting with version 22.3.X, bring assessments directly into the parent workflow. Embedded assessments run inside host record pages, playbooks, and workflow, letting respondents complete their work without leaving the parent context. Configuration is per template category and doesn't require code change. Embedded assessments inherit read access from the parent record—only users with read access to the parent record can read the embedded assessment.

-   **[Template versioning](https://www.servicenow.com/docs/access?context=template-versioning&family=australia&ft:locale=en-US)**

Starting with version 22.3.X, update published assessment templates without copying and deprecating the original. When a template manager publishes a new version, the prior version is automatically retired and future assessments use the new version. Template versioning preserves auditability for in-flight assessments while letting template managers publish new versions to reflect corrections, regulatory changes, or annual content refreshes.

    -   A version-info bar on every published template shows the current version and exposes a create new version action that returns the template to Draft.
    -   A full version history view captures who created each version, when, and which prior version it was branched from.
    -   A new Delete template version action is available from the version actions menu.
-   **[SAE Enhancements](https://www.servicenow.com/docs/access?context=sae-template-designer&family=australia&ft:locale=en-US)**

These SAE enhancements are available in version 22.3.X and later:

    -   Flag individual questions that need attention with a single click. Flags move through three states—Flagged, Resolved, and Unflagged—and every transition is captured in the assessment activity log.
    -   Add comments at the question level so responders, reviewers, and collaborators can resolve clarifications inline instead of relying on email or external tools. A new Work Notes tab next to the Comments tab provides a separate, role-gated conversation for reviewers or administrators.
    -   Hide conditional questions that don't meet their visibility criteria so responders see only the questions relevant to them, eliminating **Skipped** clutter and reducing assessment fatigue.
    -   Scroll continuously through questions within a section or sub-section instead of paginating, giving responders an uninterrupted answer flow.
    -   Apply multiple filters at once on the question list \(for example, **Unanswered** + **Flagged** + **With comments**\) to focus on exactly the questions that need attention.
    -   View scope item fields directly in the assessment task list so reviewers and assignees can see scope context without opening each assessment.
    -   Programmatically create a combined assessment from multiple assessment IDs using any custom logic, removing the need for manual combine actions. For example, combine all control attestations belonging to an entity group into a single assessment.

-   **[Collaboration in assessments](https://www.servicenow.com/docs/access?context=collaboration-in-assessments&family=australia&ft:locale=en-US)**

Starting with version 22.3.X, use granular delegation as a primary owner to assign individual assessment sections to SMEs. Respondents can view the entire assessment for context but can edit only their assigned sections. Monitor overall assessment progress and maintain final review and submission capabilities.

-   **[Quick edit for published templates](https://www.servicenow.com/docs/access?context=quick-edit-for-published-templates&family=australia&ft:locale=en-US)**

Starting with version 22.3.X, edit published templates inline as a template manager, including edits to the titles, descriptions, and reader roles.


</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing Smart Assessment Engine features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

[Australia Patch 5](https://www.servicenow.com/docs/access?context=australia-patch-5&family=australia&ft:locale=en-US)

-   **[ServiceNow Otto® name announcement](https://www.servicenow.com/docs/access?context=sn-ai-implementation-landing&family=australia&ft:locale=en-US)**

Now Assist introduced AI on the platform. As that experience has evolved, there's a new name for the experience. ServiceNow Otto® is the conversational AI platform integrated into ServiceNow workflows. It provides agentic capabilities, supports multimodal interactions across web, mobile, and messaging channels, and enables autonomous orchestration for cross-system workflows.

-   **[Large language models on the ServiceNow AI Platform](https://www.servicenow.com/docs/access?context=exploring-large-language-models&family=australia&ft:locale=en-US)**

The Now LLM Service is no longer the default model provider for new or inactive AI assets. A third-party LLM is now selected by default, while existing configurations using the Now LLM Service continue unchanged. The Now LLM Service is still available for manual selection.

-   **[ServiceNow product tiers](https://www.servicenow.com/docs/access?context=ai-native-sku-overview&family=australia&ft:locale=en-US)**

The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.

-   **[Hide conditional questions](https://www.servicenow.com/docs/access?context=sae-q-text-create&family=australia&ft:locale=en-US)**

Conditional questions that don't meet their visibility criteria are now fully hidden from the assessment and are no longer displayed as **Skipped**. Respondents see only the questions relevant to them, reducing assessment fatigue and eliminating "Skipped" clutter.

-   **[Create an assessment template category](https://www.servicenow.com/docs/access?context=sae-asmnt-template-category-create&family=australia&ft:locale=en-US)**

Enables one or more roles to access a template category with the multiselect **Category Roles** field.


</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some Smart Assessment Engine features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Australia, some Smart Assessment Engine features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Smart Assessment Engine.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

Install Smart Assessment Engine by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=zurich&ft:locale=en-US).

</td></tr><tr><td>

Australia

</td><td>

Install Smart Assessment Engine by requesting it from the ServiceNow Store. 

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Smart Assessment Engine we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

Check your entitlements to determine whether you have access to the collaboration features in the SAE application.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Smart Assessment Engine we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Smart Assessment Engine, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Smart Assessment Engine we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Smart Assessment Engine we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   Collaborate on assessments in real time with multiple contributors.
-   Normalize assessment question scores to a common scale for fair comparison.
-   Capture data from physical documents quickly and accurately with barcode and QR code scanning.
-   Migrate question dependencies with an improved migration utility.
-   Simplify your workflow by combining assessments from different templates in a single and unified view.

 See [Smart Assessment Engine](https://www.servicenow.com/docs/access?context=smart-asmnt-engine-landing-page&family=zurich&ft:locale=en-US) for more information.

</td></tr><tr><td>

Australia

</td><td>

[Australia Patch 5](https://www.servicenow.com/docs/access?context=australia-patch-5&family=australia&ft:locale=en-US)ServiceNow Otto® is the new name for the Now Assist experience in SAE. All Now Assist references have been updated to ServiceNow Otto.

 [Australia Patch 2](https://www.servicenow.com/docs/access?context=australia-patch-2&family=australia&ft:locale=en-US)

-   Collaborate inline with question-level flags, question-level comments, and a new Work Notes tab.
-   Draft assessment responses automatically with AI Response Assist, which suggests answers from prior assessments and attached documents with full source traceability.
-   Embed assessments inside any parent record, playbook, or workspace with the new embedded assessments capability and configurable UI Builder properties
-   Update published templates safely with template versioning while preserving auditability of in-flight assessments.
-   Streamline the responder experience with continuous scrolling inside sections and sub-sections, fully hidden conditional questions, and multi-filter support on the question list. View scope item fields directly in the assessment task list.

 [Australia Patch 1](https://www.servicenow.com/docs/access?context=australia-patch-1&family=australia&ft:locale=en-US)

-   Edit published templates quickly with inline edits and built‑in audit tracking.
-   Enable efficient, role-based collaboration by allowing primary owners to delegate assessment sections to subject matter experts \(SMEs\).

 See [Smart Assessment Engine](https://www.servicenow.com/docs/access?context=smart-asmnt-engine-landing-page&family=australia&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-zurich-australia/rn-combined-intro.md)

