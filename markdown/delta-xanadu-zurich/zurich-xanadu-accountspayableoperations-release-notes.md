---
title: Combined Accounts Payable Operations release notes for upgrades from Xanadu to Zurich
description: Consolidated page of all release notes for Accounts Payable Operations from Xanadu to Zurich.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/delta-xanadu-zurich/zurich-xanadu-accountspayableoperations-release-notes.html
release: zurich
topic_type: reference
last_updated: "2026-06-20"
reading_time_minutes: 10
breadcrumb: [Products combined by family]
---

# Combined Accounts Payable Operations release notes for upgrades from Xanadu to Zurich

Consolidated page of all release notes for Accounts Payable Operations from Xanadu to Zurich.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Accounts Payable Operations release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Xanadu to Zurich.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Accounts Payable Operations to Zurich

Before you upgrade to Zurich, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

If you are upgrading from a previous release, you must configure the reference field in the Tax Code \[sn\_fin\_tax\_code\] table. The exception engine validates the invoice using the tax code and raises exceptions if necessary.

</td></tr><tr><td>

Yokohama

</td><td>

If you’re upgrading from a previous release, you must configure the reference field in the Tax Code \[sn\_fin\_tax\_code\] table. The exception engine validates the invoice using the tax code and raises exceptions if necessary.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Zurich, new features were introduced for Accounts Payable Operations.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   **[Tolerance Rules and Variances for invoices](https://servicenow-staging.fluidtopics.net/access?context=tolerance-rules-and-variance&family=xanadu&ft:locale=en-US)**
    -   The **tax tolerance** rule, which defines the variance limit set on the tax amount variance in an invoice.
    -   The **under tax amount** variance exception, which is raised when the supplier-provided tax amount is less than the system-calculated tax amount.
    -   The**over tax amount** variance exception, which is raised when the supplier-provided tax amount is greater than the system-calculated tax amount.
-   **[Playbook for updating the invoice primary data](https://servicenow-staging.fluidtopics.net/access?context=playbooks&family=xanadu&ft:locale=en-US)**
    -   Add tax lines to invoice lines through a playbook activity.
    -   Apply the new tax lines to single or multiple invoice lines.
-   **[Tax calculations](https://servicenow-staging.fluidtopics.net/access?context=tax-calculations-in-apo&family=xanadu&ft:locale=en-US)**

As a tax owner or tax manager, add tax lines and tax codes.


-   **[\[Placeholder link text to key invoice-line-cost-allocation\]](https://servicenow-staging.fluidtopics.net/access?context=invoice-line-cost-allocation&family=xanadu&ft:locale=en-US)**

The Invoice cost allocation feature allocates invoice costs across various business functions, which increases the accuracy of financial reporting, and informs strategic decision-making.

In the cost center-based approval rule for invoices, costs can be allocated to multiple cost centers, enabling cost center owners to approve the invoice only for the amount allocated to their cost center.

-   **[\[Placeholder link text to key now-assist-apo\]](https://servicenow-staging.fluidtopics.net/access?context=now-assist-apo&family=xanadu&ft:locale=en-US)**

The ServiceNow® Now Assist for APO application guides APO fulfillers to generate a case summary and quickly understand the case context by using the case summarization skill.


</td></tr><tr><td>

Yokohama

</td><td>

-   **[Using Supplier Collaboration Portal in APO](https://servicenow-staging.fluidtopics.net/access?context=using-supplier-collaboration-portal&family=yokohama&ft:locale=en-US)**

In the supplier collaboration portal home page, the supplier contact can choose to view invoice and inquiry cases associated with their account.

Supplier contacts can be assigned with multiple suppliers.


-   **[Set APO properties](https://servicenow-staging.fluidtopics.net/access?context=set-apo-properties&family=yokohama&ft:locale=en-US)**

The one-stop property page provides great flexibility and ease of configuration to users with admin roles. AP admin and integrator use the APO properties page to set the parameters that control the invoice line mapping, invoice ingestion API, and exception management. Depending on the invoice line-mapping properties set, AP admin and integrator can choose to review and confirm the invoice line mapping results generated by rule-based engine and Now Assist.


-   **[Using Playbook in Accounts Payable Operations](https://servicenow-staging.fluidtopics.net/access?context=how-to-use-playbook&family=yokohama&ft:locale=en-US)**

Playbook activity card displays updated invoice statuses. AP specialist reviews and acts on the mapping recommendations by Now Assist.


-   **[Now Assist for Accounts Payable Operations \(APO\)](https://servicenow-staging.fluidtopics.net/access?context=now-assist-apo&family=yokohama&ft:locale=en-US)**

Activate the purchase order line-mapping skill in the Now Assist Admin console to enable automatic mapping of invoice lines with purchase order lines using Now Assist.

Activate the invoice data extraction skill in the Now Assist Admin console to leverage GPT-4o capabilities in extracting invoice information using Document Intelligence and reducing the manual effort.

Generate invoice case summarization in multiple languages with the multi-language support in the Now Assist console.

With the Now Assist panel, you can get assistance from generative AI to solve invoice case-related issues faster.

As a fulfiller, you can learn about the details of a purchase order and its associated cases from record summarization generated by Now Assist.

Take advantage of the translation capabilities available in the Now Assist for user-generated content.

A new requester role is added to access Now Assist Accounts Payable Operations features powered by generative AI. Customers need to explicitly grant these roles to users for access to GenAI features and capabilities.


-   **[\[Placeholder link text to key using-apo-ai-agents\]](https://servicenow-staging.fluidtopics.net/access?context=using-apo-ai-agents&family=yokohama&ft:locale=en-US)**

Use agentic workflows in Accounts Payable Operations to resolve invoice inquiry cases raised by employees and suppliers. These workflows also help track associated invoice records efficiently. With an agentic workflow, you can process a high volume of invoice inquiries that come through email attachments to significantly reduce the workload of human agents.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Convert invoice type](https://servicenow-staging.fluidtopics.net/access?context=convert-invoice-case&family=zurich&ft:locale=en-US)**

Enable your accounts payable specialist to manually change the invoice type, which results in improved accuracy and compliance. For example, changing a non-purchase order \(PO\) invoice to a PO invoice type.

-   **[Using Playbook in Accounts Payable Operations](https://servicenow-staging.fluidtopics.net/access?context=how-to-use-playbook&family=zurich&ft:locale=en-US)**

Process your invoices more efficiently, adhere to compliance, and provide financial accuracy across processes by using new exceptions such as the Missing tax code invoice and currency mismatch between invoices and purchase orders.

-   **[IT Asset Management purchase order invoice processing](https://servicenow-staging.fluidtopics.net/access?context=apo-integration-with-itam&family=zurich&ft:locale=en-US)**

Confirm that ITAM receipts are available and the received quantity is updated in the purchase orders through the integration between the IT Asset Management and Accounts Payable Operations applications.

-   **[Set APO properties](https://servicenow-staging.fluidtopics.net/access?context=set-apo-properties&family=zurich&ft:locale=en-US)**

The recommend invoice owner AI agent auto-suggests and fills in the appropriate business owner based on historical patterns. This process sets up auto-confirmation from suppliers, resulting in shorter invoice processing cycles.


-   **[Universal Request in Accounts Payable Operations](https://servicenow-staging.fluidtopics.net/access?context=universal-request-in-apo&family=zurich&ft:locale=en-US)**

Employees and suppliers can raise general case requests and track case activity updates from their respective portals by using the ServiceNowUniversal Request \(UR\) application. Universal requests eliminate confusion about which department to contact for assistance.


-   **[Distribution set in Accounts Payable Operations](https://servicenow-staging.fluidtopics.net/access?context=distribution-sets-in-apo&family=zurich&ft:locale=en-US)**

Apply predefined distribution sets to split invoice amounts across multiple cost centers or GL accounts without having to do manual entry for each invoice line in PO invoices and non-PO invoices. This process helps distribute costs to multiple cost centers automatically, reducing manual work for Accounts Payable specialists.


</td></tr></tbody>
</table>## Changes

Between your current release family and Zurich, some changes were made to existing Accounts Payable Operations features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   **[APO landing page](https://servicenow-staging.fluidtopics.net/access?context=acc-pay-workspace-landing-page&family=xanadu&ft:locale=en-US)**

Task owners can view and handle invoice tasks more efficiently using task filters, widgets and bar charts in the Accounts Payable Operations workspace.

-   **[Accounts Payable Operations integration framework](https://servicenow-staging.fluidtopics.net/access?context=using-integration-to-create-invoice&family=xanadu&ft:locale=en-US)**

Updated invoice integration using tax fields enables you to process invoices more quickly.


</td></tr><tr><td>

Yokohama

</td><td>

-   **[Work with invoices](https://servicenow-staging.fluidtopics.net/access?context=work-with-invoices&family=yokohama&ft:locale=en-US)**
    -   Invoice line statuses are updated as:
        -   PO matching error to Mapping error
        -   PO matching completed to Mapping complete
        -   Matching error to Mapping error
        -   Review mapping

-   **[Invoice ingestion process when Document Intelligence is unavailable](https://servicenow-staging.fluidtopics.net/access?context=invoice-ingest-docintel-unavailable&family=yokohama&ft:locale=en-US)**

Accounts Payable Operations integration with Document Intelligence enables AP admin to create invoice manually when DocIntel is down. The capture invoice details activity card displays the **Create invoice** option.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Invoice exceptions](https://servicenow-staging.fluidtopics.net/access?context=work-with-invoice-exceptions&family=zurich&ft:locale=en-US)**

The Insufficient goods receipt exception has been enhanced to validate line-level quantities accurately when multiple invoices are submitted against a single purchase order even if a sufficient goods receipt exist.

The Insufficient Funds \(Line Amount\) functionality has been enhanced to perform validation of available funds at the invoice line level, matching each invoice line against its respective purchase order line when multiple invoices are generated for the same purchase order line.

The Insufficient Funds \(Header Amount\) logic has been enhanced to validate available funds at the invoice header level against the corresponding purchase order when multiple invoices are created for the same purchase order.


</td></tr></tbody>
</table>## Removed

Between your current release family and Zurich, some Accounts Payable Operations features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Zurich, some Accounts Payable Operations features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

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

Xanadu

</td><td>

Install Accounts Payable Operations by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://servicenow-staging.fluidtopics.net/access?context=sn-store-release-notes&family=xanadu&ft:locale=en-US).

</td></tr><tr><td>

Yokohama

</td><td>

Install Accounts Payable Operations by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://servicenow-staging.fluidtopics.net/access?context=sn-store-release-notes&family=yokohama&ft:locale=en-US).

</td></tr><tr><td>

Zurich

</td><td>

Install Accounts Payable Operations by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://servicenow-staging.fluidtopics.net/access?context=sn-store-release-notes&family=zurich&ft:locale=en-US).

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Accounts Payable Operations we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

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

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

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

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

-   **Dark theme**

The new Coral theme includes a dark theme option for web and mobile experiences. This option is commonly used to alleviate eye strain and improve readability.


</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Accounts Payable Operations we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

Accounts Payable Operations supports multiple languages. The current DocIntel model is trained to extract invoices in the English language only. If you want to process an invoice in the multiple languages supported by DocIntel, you must train the DocIntel model.

</td></tr><tr><td>

Yokohama

</td><td>

Accounts Payable Operations supports multiple languages. The current DocIntel model is trained to extract invoices in the English language only. If you want to process an invoice in the multiple languages supported by DocIntel, you must train the DocIntel model.

</td></tr><tr><td>

Zurich

</td><td>

Accounts Payable Operations supports multiple languages. However, the current DocIntel model is trained to extract invoices in the English language only. If you want to process an invoice in the multiple languages supported by DocIntel, you must train the DocIntel model.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Accounts Payable Operations we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   Provides support for tax compliance.
-   Enables tax managers or tax specialists to create, edit, and update tax types and tax codes.
-   Validate supplier taxes and ensure tax regulatory compliance with added tax-related exceptions.
-   Check for invoices configured with Tax variance tolerance rules through the exception engine.
-   Allocate invoice cost across various business functions using the invoice cost allocation feature, which increases the accuracy of financial reporting and informs strategic decision-making.

</td></tr><tr><td>

Yokohama

</td><td>

-   Introduced Agentic workflow in Accounts Payable Operations to resolve invoice inquiry cases raised by employees and suppliers thereby significantly reducing the involvement of human agents.
-   The ServiceNow® Now Assist offers generative AI purchase order line-mapping to improve accuracy and reduce manual work.
-   Experience the new generative AI skill for invoice data extraction, designed to enhance accuracy and reduce manual effort.
-   Leverage AI-powered GPT-4o-driven invoice data extraction with Document Intelligence for improved accuracy and reduced manual effort.
-   Get instant, real-time assistance from generative AI to summarize invoice case details through the Now Assist panel.
-   Use the Accounts Payable Operations properties page to control the configuration of APO properties.

</td></tr><tr><td>

Zurich

</td><td>

-   Process your invoice more effectively and accurately with the new missing tax code invoice exception and currency mismatch.
-   Handle various AP related inquiries and tasks through a single entry point by using the Universal Request \(UR\) as a multi-purpose request form.
-   Leverage AI-powered agentic workflow to recommend the appropriate business owner for non-PO invoices based on historical patterns.
-   Automate cost allocations in the invoice lines using distribution sets.

 See [Accounts Payable Operations](https://servicenow-staging.fluidtopics.net/access?context=acc-pay-mgmt-landing-page&family=zurich&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/delta-xanadu-zurich/rn-combined-intro.md)

