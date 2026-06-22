---
title: Combined Accounts Payable Operations release notes for upgrades from Zurich to Australia
description: Consolidated page of all release notes for Accounts Payable Operations from Zurich to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-zurich-australia/australia-zurich-accountspayableoperations-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-06-22"
reading_time_minutes: 7
breadcrumb: [Products combined by family]
---

# Combined Accounts Payable Operations release notes for upgrades from Zurich to Australia

Consolidated page of all release notes for Accounts Payable Operations from Zurich to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Accounts Payable Operations release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Zurich to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Accounts Payable Operations to Australia

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

Between your current release family and Australia, new features were introduced for Accounts Payable Operations.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   **[Tax Engine Integration](https://www.servicenow.com/docs/access?context=tax-engine-integration&family=zurich&ft:locale=en-US)**

The tax engine integration framework validates supplier-provided tax against system tax at invoice line level, maintains compliance with regional and global tax regulations. This integration triggers automatic tax validation, handles exceptions for tax variance and missing data, enables manual revalidation and rolling up of system tax.


-   **[Convert invoice type](https://www.servicenow.com/docs/access?context=convert-invoice-case&family=zurich&ft:locale=en-US)**

Enable your accounts payable specialist to manually change the invoice type, which results in improved accuracy and compliance. For example, changing a non-purchase order \(PO\) invoice to a PO invoice type.

-   **[Using Playbook in Accounts Payable Operations](https://www.servicenow.com/docs/access?context=how-to-use-playbook&family=zurich&ft:locale=en-US)**

Process your invoices more efficiently, adhere to compliance, and provide financial accuracy across processes by using new exceptions such as the Missing tax code invoice and currency mismatch between invoices and purchase orders.

-   **[IT Asset Management purchase order invoice processing](https://www.servicenow.com/docs/access?context=apo-integration-with-itam&family=zurich&ft:locale=en-US)**

Confirm that ITAM receipts are available and the received quantity is updated in the purchase orders through the integration between the IT Asset Management and Accounts Payable Operations applications.

-   **[Set APO properties](https://www.servicenow.com/docs/access?context=set-apo-properties&family=zurich&ft:locale=en-US)**

The recommend invoice owner AI agent auto-suggests and fills in the appropriate business owner based on historical patterns. This process sets up auto-confirmation from suppliers, resulting in shorter invoice processing cycles.


-   **[Universal Request in Accounts Payable Operations](https://www.servicenow.com/docs/access?context=universal-request-in-apo&family=zurich&ft:locale=en-US)**

Employees and suppliers can raise general case requests and track case activity updates from their respective portals by using the ServiceNowUniversal Request \(UR\) application. Universal requests eliminate confusion about which department to contact for assistance.


-   **[Distribution set in Accounts Payable Operations](https://www.servicenow.com/docs/access?context=distribution-sets-in-apo&family=zurich&ft:locale=en-US)**

Apply predefined distribution sets to split invoice amounts across multiple cost centers or GL accounts without having to do manual entry for each invoice line in PO invoices and non-PO invoices. This process helps distribute costs to multiple cost centers automatically, reducing manual work for Accounts Payable specialists.


</td></tr><tr><td>

Australia

</td><td>

-   **[Tax Engine Integration](https://www.servicenow.com/docs/access?context=tax-engine-integration&family=australia&ft:locale=en-US)**

The tax engine integration framework validates supplier-provided tax against system tax at invoice line level, and supports regional and global tax requirements. This integration triggers automatic tax validation, handles exceptions for tax variance and missing data, enables manual re validation and rolling up of system tax.

-   **[Email parser agent for APO](https://www.servicenow.com/docs/access?context=email-parser-agent-for-apo&family=australia&ft:locale=en-US)**

The Email parser is an AI agent that automatically processes incoming emails \(Level 1 support cases and tasks\) from suppliers and invoice owners, identifies actionable requests, classifies them, and creates invoice cases.


-   **[Invoice rejection modes](https://www.servicenow.com/docs/access?context=invoice-rejection-modes&family=australia&ft:locale=en-US)**

APO supports configurable rejection modes for invoice exception handling. Administrators can configure rejection mode behavior per exception type to align with organizational policies and audit requirements.


</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing Accounts Payable Operations features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   **[Invoice exceptions](https://www.servicenow.com/docs/access?context=work-with-invoice-exceptions&family=zurich&ft:locale=en-US)**

The Insufficient goods receipt exception has been enhanced to validate line-level quantities accurately when multiple invoices are submitted against a single purchase order even if a sufficient goods receipt exist.

The Insufficient Funds \(Line Amount\) functionality has been enhanced to perform validation of available funds at the invoice line level, matching each invoice line against its respective purchase order line when multiple invoices are generated for the same purchase order line.

The Insufficient Funds \(Header Amount\) logic has been enhanced to validate available funds at the invoice header level against the corresponding purchase order when multiple invoices are created for the same purchase order.


</td></tr><tr><td>

Australia

</td><td>

-   **[Invoice exceptions](https://www.servicenow.com/docs/access?context=work-with-invoice-exceptions&family=australia&ft:locale=en-US)**

Accounts Payable Operations flags invoices received from unrecognized or unverified supplier sources as exceptions. The system compares sender email addresses and identities against registered supplier contacts; invoices from unmatched sources are held for verification. This helps reduce the risk of invoice fraud, verifies payment accuracy, and maintains supplier control by requiring verification before processing invoices from unknown sources.


</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some Accounts Payable Operations features or functionality were removed.

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

-   Roll up logic applies only to system tax, not to supplier-declared tax. Supplier tax roll up is removed. This replaces the previous approach, which lacked independent validation of supplier-provided tax amounts.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Australia, some Accounts Payable Operations features or functionality were deprecated.

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

Review information on how to activate Accounts Payable Operations.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

Install Accounts Payable Operations by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=zurich&ft:locale=en-US).

</td></tr><tr><td>

Australia

</td><td>

Install Accounts Payable Operations by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=australia&ft:locale=en-US).

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Accounts Payable Operations we have noted them here.

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
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Accounts Payable Operations we have noted them here.

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

Review details on accessibility information for Accounts Payable Operations, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   **Dark theme**

The new Coral theme includes a dark theme option for web and mobile experiences. This option is commonly used to alleviate eye strain and improve readability.


</td></tr><tr><td>

Australia

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

Zurich

</td><td>

Accounts Payable Operations supports multiple languages. However, the current DocIntel model is trained to extract invoices in the English language only. If you want to process an invoice in the multiple languages supported by DocIntel, you must train the DocIntel model.

</td></tr><tr><td>

Australia

</td><td>

Accounts Payable Operations supports multiple languages. However, the current DocIntel model is trained to extract invoices in the English language only. To process an invoice in the multiple languages supported by DocIntel, you must train the DocIntel model.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Accounts Payable Operations we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   Leverage Accounts payable document classification skill to classify email attachments into invoice, credit memo, or supporting documents based on the AI recommended confidence score resulting in error free invoice data extraction.
-   Validate supplier provided tax against a system-calculated tax by integrating an enterprise-grade tax engine resulting in straight-through processing of invoice while improving accuracy, compliance, and operational efficiency.
-   Process your invoice more effectively and accurately with the new missing tax code invoice exception and currency mismatch.
-   Handle various AP related inquiries and tasks through a single entry point by using the Universal Request \(UR\) as a multi-purpose request form.
-   Leverage AI-powered agentic workflow to recommend the appropriate business owner for non-PO invoices based on historical patterns.
-   Automate cost allocations in the invoice lines using distribution sets.

 See [Accounts Payable Operations](https://www.servicenow.com/docs/access?context=acc-pay-mgmt-landing-page&family=zurich&ft:locale=en-US) for more information.

</td></tr><tr><td>

Australia

</td><td>

-   Suppliers can submit, track, and confirm resolutions without portal navigation.
-   Configure rejection modes to customize workflows so that AI workers focus on resolution quality rather than administrative tasks.
-   Use automated email parsing and LLM-assisted responses to handle cases with less manual effort.

 See [Accounts Payable Operations](https://www.servicenow.com/docs/access?context=acc-pay-mgmt-landing-page&family=australia&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-zurich-australia/rn-combined-intro.md)

