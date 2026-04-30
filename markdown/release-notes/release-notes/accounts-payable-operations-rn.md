---
title: Accounts Payable Operations release notes
description: The ServiceNow Accounts Payable Operations application enables Accounts Payable specialists and tax specialists to validate the taxes provided by suppliers and ensure tax compliance. The Accounts Payable Operations was enhanced and updated in the Xanadu release.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
---

# Accounts Payable Operations release notes

The ServiceNow® Accounts Payable Operations application enables Accounts Payable specialists and tax specialists to validate the taxes provided by suppliers and ensure tax compliance. The Accounts Payable Operations was enhanced and updated in the Xanadu release.

## Accounts Payable Operations highlights for the Xanadu release

-   Provides support for tax compliance.
-   Enables tax managers or tax specialists to create, edit, and update tax types and tax codes.
-   Validate supplier taxes and ensure tax regulatory compliance with added tax-related exceptions.
-   Check for invoices configured with Tax variance tolerance rules through the exception engine.
-   Allocate invoice cost across various business functions using the invoice cost allocation feature, which increases the accuracy of financial reporting and informs strategic decision-making.

**Important:** Accounts Payable Operations is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading Accounts Payable Operations to Xanadu

If you are upgrading from a previous release, you must configure the reference field in the Tax Code \[sn\_fin\_tax\_code\] table. The exception engine validates the invoice using the tax code and raises exceptions if necessary.

## New in the Xanadu release

-   **[Tolerance Rules and Variances for invoices](https://www.servicenow.com/docs/access?context=tolerance-rules-and-variance&version=xanadu&pubname=xanadu-source-to-pay-operations&ft:locale=en-US)**
    -   The **tax tolerance** rule, which defines the variance limit set on the tax amount variance in an invoice.
    -   The **under tax amount** variance exception, which is raised when the supplier-provided tax amount is less than the system-calculated tax amount.
    -   The**over tax amount** variance exception, which is raised when the supplier-provided tax amount is greater than the system-calculated tax amount.
-   **[Playbook for updating the invoice primary data](https://www.servicenow.com/docs/access?context=playbooks&version=xanadu&pubname=xanadu-source-to-pay-operations&ft:locale=en-US)**
    -   Add tax lines to invoice lines through a playbook activity.
    -   Apply the new tax lines to single or multiple invoice lines.
-   **[Tax calculations](https://www.servicenow.com/docs/access?context=tax-calculations-in-apo&version=xanadu&pubname=xanadu-source-to-pay-operations&ft:locale=en-US)**

    As a tax owner or tax manager, add tax lines and tax codes.


-   ****

    The Invoice cost allocation feature allocates invoice costs across various business functions, which increases the accuracy of financial reporting, and informs strategic decision-making.

    In the cost center-based approval rule for invoices, costs can be allocated to multiple cost centers, enabling cost center owners to approve the invoice only for the amount allocated to their cost center.

-   ****

    The ServiceNow® Now Assist for APO application guides APO fulfillers to generate a case summary and quickly understand the case context by using the case summarization skill.


## Changed in this release

-   **[APO landing page](https://www.servicenow.com/docs/access?context=acc-pay-workspace-landing-page&version=xanadu&pubname=xanadu-source-to-pay-operations&ft:locale=en-US)**

    Task owners can view and handle invoice tasks more efficiently using task filters, widgets and bar charts in the Accounts Payable Operations workspace.

-   **[Accounts Payable Operations integration framework](https://www.servicenow.com/docs/access?context=using-integration-to-create-invoice&version=xanadu&pubname=xanadu-source-to-pay-operations&ft:locale=en-US)**

    Updated invoice integration using tax fields enables you to process invoices more quickly.


## Activation information

Install Accounts Payable Operations by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Localization information

Accounts Payable Operations supports multiple languages. The current DocIntel model is trained to extract invoices in the English language only. If you want to process an invoice in the multiple languages supported by DocIntel, you must train the DocIntel model.

**Parent Topic:**[Source-to-Pay Operations release notes](source-to-pay-operations-rn-landing.md)

