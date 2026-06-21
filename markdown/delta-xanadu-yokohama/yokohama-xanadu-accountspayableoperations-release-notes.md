---
title: Combined Accounts Payable Operations release notes for upgrades from Xanadu to Yokohama
description: Consolidated page of all release notes for Accounts Payable Operations from Xanadu to Yokohama.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/delta-xanadu-yokohama/yokohama-xanadu-accountspayableoperations-release-notes.html
release: yokohama
topic_type: reference
last_updated: "2026-06-20"
reading_time_minutes: 7
breadcrumb: [Products combined by family]
---

# Combined Accounts Payable Operations release notes for upgrades from Xanadu to Yokohama

Consolidated page of all release notes for Accounts Payable Operations from Xanadu to Yokohama.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Accounts Payable Operations release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Xanadu to Yokohama.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Accounts Payable Operations to Yokohama

Before you upgrade to Yokohama, review these pre- and post-upgrade tasks and complete the tasks as needed.

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

</td></tr></tbody>
</table>## New features

Between your current release family and Yokohama, new features were introduced for Accounts Payable Operations.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   **[Tolerance Rules and Variances for invoices](https://www.servicenow.com/docs/access?context=tolerance-rules-and-variance&family=xanadu&ft:locale=en-US)**
    -   The **tax tolerance** rule, which defines the variance limit set on the tax amount variance in an invoice.
    -   The **under tax amount** variance exception, which is raised when the supplier-provided tax amount is less than the system-calculated tax amount.
    -   The**over tax amount** variance exception, which is raised when the supplier-provided tax amount is greater than the system-calculated tax amount.
-   **[Playbook for updating the invoice primary data](https://www.servicenow.com/docs/access?context=playbooks&family=xanadu&ft:locale=en-US)**
    -   Add tax lines to invoice lines through a playbook activity.
    -   Apply the new tax lines to single or multiple invoice lines.
-   **[Tax calculations](https://www.servicenow.com/docs/access?context=tax-calculations-in-apo&family=xanadu&ft:locale=en-US)**

As a tax owner or tax manager, add tax lines and tax codes.


-   **[\[Placeholder link text to key invoice-line-cost-allocation\]](https://www.servicenow.com/docs/access?context=invoice-line-cost-allocation&family=xanadu&ft:locale=en-US)**

The Invoice cost allocation feature allocates invoice costs across various business functions, which increases the accuracy of financial reporting, and informs strategic decision-making.

In the cost center-based approval rule for invoices, costs can be allocated to multiple cost centers, enabling cost center owners to approve the invoice only for the amount allocated to their cost center.

-   **[\[Placeholder link text to key now-assist-apo\]](https://www.servicenow.com/docs/access?context=now-assist-apo&family=xanadu&ft:locale=en-US)**

The ServiceNow® Now Assist for APO application guides APO fulfillers to generate a case summary and quickly understand the case context by using the case summarization skill.


</td></tr><tr><td>

Yokohama

</td><td>

-   **[Using Supplier Collaboration Portal in APO](https://www.servicenow.com/docs/access?context=using-supplier-collaboration-portal&family=yokohama&ft:locale=en-US)**

In the supplier collaboration portal home page, the supplier contact can choose to view invoice and inquiry cases associated with their account.

Supplier contacts can be assigned with multiple suppliers.


-   **[Set APO properties](https://www.servicenow.com/docs/access?context=set-apo-properties&family=yokohama&ft:locale=en-US)**

The one-stop property page provides great flexibility and ease of configuration to users with admin roles. AP admin and integrator use the APO properties page to set the parameters that control the invoice line mapping, invoice ingestion API, and exception management. Depending on the invoice line-mapping properties set, AP admin and integrator can choose to review and confirm the invoice line mapping results generated by rule-based engine and Now Assist.


-   **[Using Playbook in Accounts Payable Operations](https://www.servicenow.com/docs/access?context=how-to-use-playbook&family=yokohama&ft:locale=en-US)**

Playbook activity card displays updated invoice statuses. AP specialist reviews and acts on the mapping recommendations by Now Assist.


-   **[Now Assist for Accounts Payable Operations \(APO\)](https://www.servicenow.com/docs/access?context=now-assist-apo&family=yokohama&ft:locale=en-US)**

Activate the purchase order line-mapping skill in the Now Assist Admin console to enable automatic mapping of invoice lines with purchase order lines using Now Assist.

Activate the invoice data extraction skill in the Now Assist Admin console to leverage GPT-4o capabilities in extracting invoice information using Document Intelligence and reducing the manual effort.

Generate invoice case summarization in multiple languages with the multi-language support in the Now Assist console.

With the Now Assist panel, you can get assistance from generative AI to solve invoice case-related issues faster.

As a fulfiller, you can learn about the details of a purchase order and its associated cases from record summarization generated by Now Assist.

Take advantage of the translation capabilities available in the Now Assist for user-generated content.

A new requester role is added to access Now Assist Accounts Payable Operations features powered by generative AI. Customers need to explicitly grant these roles to users for access to GenAI features and capabilities.


-   **[\[Placeholder link text to key using-apo-ai-agents\]](https://www.servicenow.com/docs/access?context=using-apo-ai-agents&family=yokohama&ft:locale=en-US)**

Use agentic workflows in Accounts Payable Operations to resolve invoice inquiry cases raised by employees and suppliers. These workflows also help track associated invoice records efficiently. With an agentic workflow, you can process a high volume of invoice inquiries that come through email attachments to significantly reduce the workload of human agents.


</td></tr></tbody>
</table>## Changes

Between your current release family and Yokohama, some changes were made to existing Accounts Payable Operations features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   **[APO landing page](https://www.servicenow.com/docs/access?context=acc-pay-workspace-landing-page&family=xanadu&ft:locale=en-US)**

Task owners can view and handle invoice tasks more efficiently using task filters, widgets and bar charts in the Accounts Payable Operations workspace.

-   **[Accounts Payable Operations integration framework](https://www.servicenow.com/docs/access?context=using-integration-to-create-invoice&family=xanadu&ft:locale=en-US)**

Updated invoice integration using tax fields enables you to process invoices more quickly.


</td></tr><tr><td>

Yokohama

</td><td>

-   **[Work with invoices](https://www.servicenow.com/docs/access?context=work-with-invoices&family=yokohama&ft:locale=en-US)**
    -   Invoice line statuses are updated as:
        -   PO matching error to Mapping error
        -   PO matching completed to Mapping complete
        -   Matching error to Mapping error
        -   Review mapping

-   **[Invoice ingestion process when Document Intelligence is unavailable](https://www.servicenow.com/docs/access?context=invoice-ingest-docintel-unavailable&family=yokohama&ft:locale=en-US)**

Accounts Payable Operations integration with Document Intelligence enables AP admin to create invoice manually when DocIntel is down. The capture invoice details activity card displays the **Create invoice** option.


</td></tr></tbody>
</table>## Removed

Between your current release family and Yokohama, some Accounts Payable Operations features or functionality were removed.

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

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Yokohama, some Accounts Payable Operations features or functionality were deprecated.

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

Install Accounts Payable Operations by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=xanadu&ft:locale=en-US).

</td></tr><tr><td>

Yokohama

</td><td>

Install Accounts Payable Operations by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=yokohama&ft:locale=en-US).

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

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/delta-xanadu-yokohama/rn-combined-intro.md)

