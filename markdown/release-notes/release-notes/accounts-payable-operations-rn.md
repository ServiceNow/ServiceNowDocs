---
title: Accounts Payable Operations release notes
description: The ServiceNow Accounts Payable Operations adds capabilities for supplier case resolution and confirmation workflows. The large language model \(LLM\)-aided email parser agent automatically classifies incoming supplier inquiries, eliminating manual intervention and routes invoice inquiry cases to the appropriate teams. Invoice exceptions in Accounts Payable Operations are enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
---

# Accounts Payable Operations release notes

The ServiceNow® Accounts Payable Operations adds capabilities for supplier case resolution and confirmation workflows. The large language model \(LLM\)-aided email parser agent automatically classifies incoming supplier inquiries, eliminating manual intervention and routes invoice inquiry cases to the appropriate teams. Invoice exceptions in Accounts Payable Operations are enhanced and updated in the Australia release.

-   **[ServiceNow product tiers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-native-sku-overview.md)**

    The ServiceNow AI Platform now brings you an AI native experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
    Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.


## Accounts Payable Operations highlights for the Australia release

-   Suppliers can submit, track, and confirm resolutions without portal navigation.
-   Configure rejection modes to customize workflows so that AI workers focus on resolution quality rather than administrative tasks.
-   Use automated email parsing and LLM-assisted responses to handle cases with less manual effort.

See [Accounts Payable Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/acc-pay-mgmt-landing-page.md) for more information.

**Important:** Accounts Payable Operations is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Australia release

-   **[Tax Engine Integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/tax-engine-integration.md)**

    The tax engine integration framework validates supplier-provided tax against system tax at invoice line level, and supports regional and global tax requirements. This integration triggers automatic tax validation, handles exceptions for tax variance and missing data, enables manual re validation and rolling up of system tax.

-   **[Email parser agent for APO](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/email-parser-agent-for-apo.md)**

    The Email parser is an AI agent that automatically processes incoming emails \(Level 1 support cases and tasks\) from suppliers and invoice owners, identifies actionable requests, classifies them, and creates invoice cases.


-   **[Invoice rejection modes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/invoice-rejection-modes.md)**

    APO supports configurable rejection modes for invoice exception handling. Administrators can configure rejection mode behavior per exception type to align with organizational policies and audit requirements.


## Changed in this release

-   **[Invoice exceptions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/work-with-invoice-exceptions.md)**

    Accounts Payable Operations flags invoices received from unrecognized or unverified supplier sources as exceptions. The system compares sender email addresses and identities against registered supplier contacts; invoices from unmatched sources are held for verification. This helps reduce the risk of invoice fraud, verifies payment accuracy, and maintains supplier control by requiring verification before processing invoices from unknown sources.


## Removed in this release

-   Roll up logic applies only to system tax, not to supplier-declared tax. Supplier tax roll up is removed. This replaces the previous approach, which lacked independent validation of supplier-provided tax amounts.

## Activation information

Install Accounts Payable Operations by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Localization information

Accounts Payable Operations supports multiple languages. However, the current DocIntel model is trained to extract invoices in the English language only. To process an invoice in the multiple languages supported by DocIntel, you must train the DocIntel model.

## Plugin information

-   **New plugins**

    The following plugins are new in Australia:

    Tax Engine Integration with Vertex \(com.sn\_fsc\_vertex\): This plugin enables the integration of APO with Vertex \(vendor\) to perform tax validation on invoices resulting in tax accuracy and compliance.


**Parent Topic:**[Source-to-Pay Operations release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/source-to-pay-operations-rn-landing.md)

