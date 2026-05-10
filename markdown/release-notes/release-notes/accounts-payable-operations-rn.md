---
title: Accounts Payable Operations release notes
description: The ServiceNow Accounts Payable Operations application enables accounts payable specialists to automate cost allocations in the invoice lines using distribution sets. The AI-powered agent provides business owner recommendations for non-PO invoices based on historical patterns. The Accounts Payable Operations was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
---

# Accounts Payable Operations release notes

The ServiceNow® Accounts Payable Operations application enables accounts payable specialists to automate cost allocations in the invoice lines using distribution sets. The AI-powered agent provides business owner recommendations for non-PO invoices based on historical patterns. The Accounts Payable Operations was enhanced and updated in the Australia release.

-   **[ServiceNow product tiers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-native-sku-overview.md)**

    The ServiceNow AI Platform now brings you an AI native experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
    Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.


## Accounts Payable Operations highlights for the Australia release

-   Leverage Accounts payable document classification skill to classify email attachments into invoice, credit memo, or supporting documents based on the AI recommended confidence score resulting in error free invoice data extraction.
-   Validate supplier provided tax against a system-calculated tax by integrating an enterprise-grade tax engine resulting in straight-through processing of invoice while improving accuracy, compliance, and operational efficiency.

See  for more information.

**Important:** Accounts Payable Operations is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Australia release

-   ****

    The tax engine integration framework validates supplier-provided tax against system tax at invoice line level, maintains compliance with regional and global tax regulations. This integration triggers automatic tax validation, handles exceptions for tax variance and missing data, enables manual revalidation and rolling up of system tax.


## Changed in this release

-   ****

    The Document classification skill auto-classifies supplier email attachments as invoice, credit memo, or supporting documents with an AI-recommended confidence score. After the classification, separate invoice processing cases are created for invoices and credit memo with supporting documents linked to both the cases. The playbook allows you to configure the confidence threshold for auto-approval or involve AP specialists to manually review them.


## Activation information

Install Accounts Payable Operations by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Localization information

Accounts Payable Operations supports multiple languages. However, the current DocIntel model is trained to extract invoices in the English language only. If you want to process an invoice in the multiple languages supported by DocIntel, you must train the DocIntel model.

## Plugin information

-   **New plugins**

    The following plugins are new in Australia:

    Tax Engine Integration with Vertex \(com.sn\_fsc\_vertex\): This plugin enables the integration of APO with Vertex \(vendor\) to perform tax validation on invoices resulting in tax accuracy and compliance.


**Parent Topic:**[Source-to-Pay Operations release notes](source-to-pay-operations-rn-landing.md)

