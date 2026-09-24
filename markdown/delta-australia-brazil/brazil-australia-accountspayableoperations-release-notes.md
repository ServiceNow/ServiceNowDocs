---
title: Combined Accounts Payable Operations release notes for upgrades from Australia to Brazil
description: Consolidated page of all release notes for Accounts Payable Operations from Australia to Brazil.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-australia-brazil/brazil-australia-accountspayableoperations-release-notes.html
release: brazil
topic_type: reference
last_updated: "2026-09-24"
reading_time_minutes: 6
breadcrumb: [Products combined by family]
---

# Combined Accounts Payable Operations release notes for upgrades from Australia to Brazil

Consolidated page of all release notes for Accounts Payable Operations from Australia to Brazil.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Accounts Payable Operations release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Australia to Brazil.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Accounts Payable Operations to Brazil

Before you upgrade to Brazil, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

-   **Upgrade information**

If you're an APO user upgrading from a previous release and want to configure the case exclusion rules, copy the out-of-box flow **Create Inquiry Case on Invoice email**, customize it as needed, and activate it.


</td></tr></tbody>
</table>## New features

Between your current release family and Brazil, new features were introduced for Accounts Payable Operations.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   **[Tax engine integration](https://www.servicenow.com/docs/access?context=tax-engine-integration&family=australia&ft:locale=en-US)**

The tax engine integration framework validates supplier-provided tax against system tax at invoice line level, and supports regional and global tax requirements. This integration triggers automatic tax validation, handles exceptions for tax variance and missing data, enables manual re validation and rolling up of system tax.

-   **[Email parser agent for APO](https://www.servicenow.com/docs/access?context=email-parser-agent-for-apo&family=australia&ft:locale=en-US)**

The email parser agent is an AI agent that automatically processes incoming emails \(Level 1 support cases and tasks\) from suppliers and invoice owners. The email parser agent identifies actionable requests, classifies them, and creates invoice cases.


 -   **[Invoice rejection modes](https://www.servicenow.com/docs/access?context=invoice-rejection-modes&family=australia&ft:locale=en-US)**

APO supports configurable rejection modes for invoice exception handling. Administrators can configure rejection mode behavior per exception type to align with organizational policies and audit requirements.


</td></tr><tr><td>

Brazil

</td><td>

-   **[Case exclusion rules](https://www.servicenow.com/docs/access?context=case-exclusion-rules&family=brazil&ft:locale=en-US)**

Defines condition-based rules that reduce unnecessary emails from creating cases. Case exclusion rules keep the case queue focused on genuine invoice inquiries, reducing redundant work and unnecessary notifications so AP agents can spend more time on real supplier and invoice issues. Manually reopen an inquiry case that is in the closed state and reuse the existing case history than starting over.


 -   **[Generate knowledge base article from case](https://www.servicenow.com/docs/access?context=create-knowledge-article-single-case&family=brazil&ft:locale=en-US)**

Invoice case resolutions can be shared in the form of searchable knowledge articles — reducing repeated effort on recurring supplier issues, driving more consistent outcomes across the AP team, and preserving a clear case-to-article link for compliance.


</td></tr></tbody>
</table>## Changes

Between your current release family and Brazil, some changes were made to existing Accounts Payable Operations features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

-   **[Email parser agent for APO](https://www.servicenow.com/docs/access?context=email-parser-agent-for-apo&family=brazil&ft:locale=en-US)**

The Email parser agent in Accounts Payable Operations has been updated to remove the Universal Request \(UR\) path. When an incoming email contains multiple intents, the agent now processes it through the standard AP intent-handling flow instead of routing the email into a Universal Request.


</td></tr></tbody>
</table>## Removed

Between your current release family and Brazil, some Accounts Payable Operations features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Brazil, some Accounts Payable Operations features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   Roll up logic applies only to system tax, not to supplier-declared tax. Supplier tax roll up is removed. This replaces the previous approach, which lacked independent validation of supplier-provided tax amounts.

</td></tr><tr><td>

Brazil

</td><td>

-   **Now LLM Service**

Starting with the September 2026 release, Gemma 4 joins our growing portfolio of open-weight models available through Now LLM Service. The latest industry advancements are available alongside sovereignty-focused options. All models are hosted and governed by ServiceNow with the same infrastructure and data protections. Older models will remain available for existing published AI skills, agents, and agentic workflows, but will no longer be available for new development or configuration. For details, see the [KB3066214: ServiceNow Otto Model Upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3066214) article in the Now Support Knowledge Base.


</td></tr></tbody>
</table>## Activation information

Review information on how to activate Accounts Payable Operations.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   **Activation information**

Install Accounts Payable Operations by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=australia&ft:locale=en-US).


**Important:** Accounts Payable Operations is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

</td></tr><tr><td>

Brazil

</td><td>

-   **Activation information**

Install Accounts Payable Operations by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=brazil&ft:locale=en-US).


**Note:** Accounts Payable Operations is available in the ServiceNow Store.

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Accounts Payable Operations we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Accounts Payable Operations we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Accounts Payable Operations, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Accounts Payable Operations we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   **Localization information**

Accounts Payable Operations supports multiple languages. However, the current DocIntel model is trained to extract invoices in the English language only. To process an invoice in the multiple languages supported by DocIntel, you must train the DocIntel model.


</td></tr><tr><td>

Brazil

</td><td>

-   **Localization information**

Accounts Payable Operations supports multiple languages. However, the current DocIntel model is trained to extract invoices in the English language only. To process an invoice in the multiple languages supported by DocIntel, you must train the DocIntel model.


</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Accounts Payable Operations we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

Now Assist introduced AI on the platform. As that experience has evolved, there's a new name for the experience. ServiceNow Otto® is the conversational AI platform integrated into ServiceNow workflows. It provides agentic capabilities, supports multimodal interactions across web, mobile, and messaging channels, and enables autonomous orchestration for cross-system workflows.

 -   **[ServiceNow product tiers](https://www.servicenow.com/docs/access?context=ai-native-sku-overview&family=australia&ft:locale=en-US)**

The ServiceNow AI Platform now brings you an AI native experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.


 -   Invoice tax lines now capture the jurisdiction, jurisdiction type, and tax authority applied during tax calculation.
-   Suppliers can submit, track, and confirm resolutions without portal navigation.
-   Configure rejection modes to customize workflows so that AI workers focus on resolution quality rather than administrative tasks.
-   Use automated email parsing and LLM-assisted responses to handle cases with less manual effort.

 See [Accounts Payable Operations](https://www.servicenow.com/docs/access?context=acc-pay-mgmt-landing-page&family=australia&ft:locale=en-US) for more information.

</td></tr><tr><td>

Brazil

</td><td>

-   Automate invoice processing with purchase order matching to reduce manual effort.
-   Prevent duplicate payments by detecting invoices that have already been processed.
-   Expedite supplier payments by verifying, processing, and reconciling invoices efficiently.
-   Protect against fraud by identifying invoice exceptions before processing.
-   Synchronize invoice data with ERP systems through bidirectional integration for ingestion and posting.

 For an overview of Accounts Payable Operations capabilities, see [Accounts Payable Operations](https://www.servicenow.com/docs/access?context=acc-pay-mgmt-landing-page&family=brazil&ft:locale=en-US).

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/delta-australia-brazil/rn-combined-intro.md)

