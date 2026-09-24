---
title: Purchase Order Management release notes
description: The ServiceNow Purchase Order Management application helps you identify, track, and resolve anomalies or irregularities in the purchase order \(PO\) execution process. See the following sections for release notes by version.The Brazil Early Availability release adds features to create purchase order confirmations via an agentic workflow and the Supplier Collaboration Portal.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/purchase-order-management-rn.html
release: brazil
topic_type: topic
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Source-to-Pay Operations release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# Purchase Order Management release notes

The ServiceNow® Purchase Order Management application helps you identify, track, and resolve anomalies or irregularities in the purchase order \(PO\) execution process. See the following sections for release notes by version.

## About Purchase Order Management

-   Provide prompt visibility for the appropriate buyer by reporting delivery plan issues related to a purchase order.
-   Expedite detection and resolution of purchase order exceptions.
-   Use agentic workflow to identify and execute mitigation strategies by analyzing delivery gaps and proposing order changes with alternative suppliers.

See [Purchase Order Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/source-to-pay-operations/purchase-order-mgmt-landing-page.md) for more information.

## Activation and other requirements

-   **Activation information**

    Purchase Order Management is available in the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).


**Parent Topic:**[Source-to-Pay Operations release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/source-to-pay-operations-rn-landing.md)

## Brazil Early Availability

The Brazil Early Availability release adds features to create purchase order confirmations via an agentic workflow and the Supplier Collaboration Portal.

### What's new

-   **[Automated purchase order confirmation creation from emails](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/source-to-pay-operations/automated-po-confirmation-creation-emails.md)**

    Reduce manual tracking of supplier emails by automatically converting emails with purchase order details into draft confirmations.

-   **[Create a purchase order confirmation in Supplier Collaboration Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/source-to-pay-operations/create-po-confirmation-in-supplier-portal.md)**

    Provide buyers certainty about their orders by creating purchase order confirmations directly from the Supplier Collaboration Portal.


### What's changed

-   **[Automated purchase order exception creation from emails](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/source-to-pay-operations/convert-emails-to-exceptions.md)**

    Previously, emails containing multiple intents would create only a single case for the dominant intent and default to a Universal Request for others. Now each identified intent triggers its own case creation, eliminating manual conversion work.

-   **[Changes to the Purchase Order Confirmation Data Model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/source-to-pay-operations/po-confirmation-line-table.md)**

    The Confirmation source and Status fields in the Purchase Order Confirmation \[sn\_poem\_po\_confirmation\] table have new values: AI Agent and Draft Retracted.


### What's deprecated or removed

-   **Now LLM Service**

    Starting with the September 2026 release, Gemma 4 joins our growing portfolio of open-weight models available through Now LLM Service. The latest industry advancements are available alongside sovereignty-focused options. All models are hosted and governed by ServiceNow with the same infrastructure and data protections. Older models will remain available for existing published AI skills, agents, and agentic workflows, but will no longer be available for new development or configuration. For details, see the [KB3066214: ServiceNow Otto Model Upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3066214) article in the Now Support Knowledge Base.


