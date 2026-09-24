---
title: Accounts Payable Operations release notes
description: The ServiceNow Accounts Payable Operations application helps Accounts Payable specialists to manage invoices, exceptions, inquiries, and track payments.The Brazil Early Availability release introduces case exclusion rules for AP administrators to create condition-based rules that stop unnecessary emails from opening cases. AP agents reopen closed or cancelled invoice inquiry cases with their full history intact.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/accounts-payable-operations-static-rn.html
release: brazil
topic_type: topic
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Source-to-Pay Operations release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# Accounts Payable Operations release notes

The ServiceNow® Accounts Payable Operations application helps Accounts Payable specialists to manage invoices, exceptions, inquiries, and track payments.

## About Accounts Payable Operations

-   Automate invoice processing with purchase order matching to reduce manual effort.
-   Prevent duplicate payments by detecting invoices that have already been processed.
-   Expedite supplier payments by verifying, processing, and reconciling invoices efficiently.
-   Protect against fraud by identifying invoice exceptions before processing.
-   Synchronize invoice data with ERP systems through bidirectional integration for ingestion and posting.

For an overview of Accounts Payable Operations capabilities, see [Accounts Payable Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/source-to-pay-operations/acc-pay-mgmt-landing-page.md).

## Activation and other requirements

**Note:** Accounts Payable Operations is available in the ServiceNow Store.

-   **Activation information**

    Install Accounts Payable Operations by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).

-   **Upgrade information**

    If you're an APO user upgrading from a previous release and want to configure the case exclusion rules, copy the out-of-box flow **Create Inquiry Case on Invoice email**, customize it as needed, and activate it.


## Accessibility and localization

-   **Localization information**

    Accounts Payable Operations supports multiple languages. However, the current DocIntel model is trained to extract invoices in the English language only. To process an invoice in the multiple languages supported by DocIntel, you must train the DocIntel model.


**Parent Topic:**[Source-to-Pay Operations release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/source-to-pay-operations-rn-landing.md)

## Brazil Early Availability

The Brazil Early Availability release introduces case exclusion rules for AP administrators to create condition-based rules that stop unnecessary emails from opening cases. AP agents reopen closed or cancelled invoice inquiry cases with their full history intact.

### What's new

-   **[Case exclusion rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/source-to-pay-operations/case-exclusion-rules.md)**

    Defines condition-based rules that reduce unnecessary emails from creating cases. Case exclusion rules keep the case queue focused on genuine invoice inquiries, reducing redundant work and unnecessary notifications so AP agents can spend more time on real supplier and invoice issues. Manually reopen an inquiry case that is in the closed state and reuse the existing case history than starting over.


-   **[Generate a knowledge article from a case](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/source-to-pay-operations/create-knowledge-article-single-case.md)**

    Invoice case resolutions can be shared in the form of searchable knowledge articles — reducing repeated effort on recurring supplier issues, driving more consistent outcomes across the AP team, and preserving a clear case-to-article link for compliance.


### What's changed

-   **[Email parser agent for APO](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/source-to-pay-operations/email-parser-agent-for-apo.md)**

    The Email parser agent in Accounts Payable Operations has been updated to remove the Universal Request \(UR\) path. When an incoming email contains multiple intents, the agent now processes it through the standard AP intent-handling flow instead of routing the email into a Universal Request.


### What's deprecated or removed

-   **Now LLM Service**

    Starting with the September 2026 release, Gemma 4 joins our growing portfolio of open-weight models available through Now LLM Service. The latest industry advancements are available alongside sovereignty-focused options. All models are hosted and governed by ServiceNow with the same infrastructure and data protections. Older models will remain available for existing published AI skills, agents, and agentic workflows, but will no longer be available for new development or configuration. For details, see the [KB3066214: ServiceNow Otto Model Upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3066214) article in the Now Support Knowledge Base.


