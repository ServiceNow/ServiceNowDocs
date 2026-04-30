---
title: Accounts Payable Operations release notes
description: The ServiceNow Accounts Payable Operations application enables accounts payable specialists to automate cost allocations in the invoice lines using distribution sets. The AI-powered agent provides business owner recommendations for non-PO invoices based on historical patterns. The Accounts Payable Operations was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
---

# Accounts Payable Operations release notes

The ServiceNow® Accounts Payable Operations application enables accounts payable specialists to automate cost allocations in the invoice lines using distribution sets. The AI-powered agent provides business owner recommendations for non-PO invoices based on historical patterns. The Accounts Payable Operations was enhanced and updated in the Zurich release.

## Accounts Payable Operations highlights for the Zurich release

-   Leverage Accounts payable document classification skill to classify email attachments into invoice, credit memo, or supporting documents based on the AI recommended confidence score resulting in error free invoice data extraction.
-   Validate supplier provided tax against a system-calculated tax by integrating an enterprise-grade tax engine resulting in straight-through processing of invoice while improving accuracy, compliance, and operational efficiency.
-   Process your invoice more effectively and accurately with the new missing tax code invoice exception and currency mismatch.
-   Handle various AP related inquiries and tasks through a single entry point by using the Universal Request \(UR\) as a multi-purpose request form.
-   Leverage AI-powered agentic workflow to recommend the appropriate business owner for non-PO invoices based on historical patterns.
-   Automate cost allocations in the invoice lines using distribution sets.

See [Accounts Payable Operations](https://www.servicenow.com/docs/access?context=acc-pay-mgmt-landing-page&version=zurich&pubname=zurich-source-to-pay-operations&ft:locale=en-US) for more information.

**Important:** Accounts Payable Operations is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Zurich release

-   **[Tax Engine Integration](https://www.servicenow.com/docs/access?context=tax-engine-integration&version=zurich&pubname=zurich-source-to-pay-operations&ft:locale=en-US)**

    The tax engine integration framework validates supplier-provided tax against system tax at invoice line level, maintains compliance with regional and global tax regulations. This integration triggers automatic tax validation, handles exceptions for tax variance and missing data, enables manual revalidation and rolling up of system tax.


-   **[Convert invoice type](https://www.servicenow.com/docs/access?context=convert-invoice-case&version=zurich&pubname=zurich-source-to-pay-operations&ft:locale=en-US)**

    Enable your accounts payable specialist to manually change the invoice type, which results in improved accuracy and compliance. For example, changing a non-purchase order \(PO\) invoice to a PO invoice type.

-   **[Using Playbook in Accounts Payable Operations](https://www.servicenow.com/docs/access?context=how-to-use-playbook&version=zurich&pubname=zurich-source-to-pay-operations&ft:locale=en-US)**

    Process your invoices more efficiently, adhere to compliance, and provide financial accuracy across processes by using new exceptions such as the Missing tax code invoice and currency mismatch between invoices and purchase orders.

-   **[IT Asset Management purchase order invoice processing](https://www.servicenow.com/docs/access?context=apo-integration-with-itam&version=zurich&pubname=zurich-source-to-pay-operations&ft:locale=en-US)**

    Confirm that ITAM receipts are available and the received quantity is updated in the purchase orders through the integration between the IT Asset Management and Accounts Payable Operations applications.

-   **[Set APO properties](https://www.servicenow.com/docs/access?context=set-apo-properties&version=zurich&pubname=zurich-source-to-pay-operations&ft:locale=en-US)**

    The recommend invoice owner AI agent auto-suggests and fills in the appropriate business owner based on historical patterns. This process sets up auto-confirmation from suppliers, resulting in shorter invoice processing cycles.


-   **[Universal Request in Accounts Payable Operations](https://www.servicenow.com/docs/access?context=universal-request-in-apo&version=zurich&pubname=zurich-source-to-pay-operations&ft:locale=en-US)**

    Employees and suppliers can raise general case requests and track case activity updates from their respective portals by using the ServiceNowUniversal Request \(UR\) application. Universal requests eliminate confusion about which department to contact for assistance.


-   **[Distribution set in Accounts Payable Operations](https://www.servicenow.com/docs/access?context=distribution-sets-in-apo&version=zurich&pubname=zurich-source-to-pay-operations&ft:locale=en-US)**

    Apply predefined distribution sets to split invoice amounts across multiple cost centers or GL accounts without having to do manual entry for each invoice line in PO invoices and non-PO invoices. This process helps distribute costs to multiple cost centers automatically, reducing manual work for Accounts Payable specialists.


## Changed in this release

-   **[Invoice exceptions](https://www.servicenow.com/docs/access?context=work-with-invoice-exceptions&version=zurich&pubname=zurich-source-to-pay-operations&ft:locale=en-US)**

    The Insufficient goods receipt exception has been enhanced to validate line-level quantities accurately when multiple invoices are submitted against a single purchase order even if a sufficient goods receipt exist.

    The Insufficient Funds \(Line Amount\) functionality has been enhanced to perform validation of available funds at the invoice line level, matching each invoice line against its respective purchase order line when multiple invoices are generated for the same purchase order line.

    The Insufficient Funds \(Header Amount\) logic has been enhanced to validate available funds at the invoice header level against the corresponding purchase order when multiple invoices are created for the same purchase order.


## Activation information

Install Accounts Payable Operations by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Localization information

Accounts Payable Operations supports multiple languages. However, the current DocIntel model is trained to extract invoices in the English language only. If you want to process an invoice in the multiple languages supported by DocIntel, you must train the DocIntel model.

## Accessibility information

-   **Dark theme**

    The new Coral theme includes a dark theme option for web and mobile experiences. This option is commonly used to alleviate eye strain and improve readability.


**Parent Topic:**[Source-to-Pay Operations release notes](source-to-pay-operations-rn-landing.md)

