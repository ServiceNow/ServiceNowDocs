---
title: Combined Quote Management release notes for upgrades from Yokohama to Australia
description: Consolidated page of all release notes for Quote Management from Yokohama to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-yokohama-australia/australia-yokohama-quotemanagement-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-06-22"
reading_time_minutes: 10
breadcrumb: [Products combined by family]
---

# Combined Quote Management release notes for upgrades from Yokohama to Australia

Consolidated page of all release notes for Quote Management from Yokohama to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Quote Management release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Yokohama to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Quote Management to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Australia, new features were introduced for Quote Management.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   **[Apply a sales agreement to a quote in Quote Management](https://www.servicenow.com/docs/access?context=quote-add-sales-agreement-quotes&family=yokohama&ft:locale=en-US)**

Create a new sales agreement or apply an existing sales agreements to a quote. When a sales agreement is enabled in a quote, the products and services added to the quote are also added to a sales agreement. When an existing sales agreement is added to a new quote, the catalog is filtered to show the products and options from the sales agreement, the price list is set to the agreement price list, and the sales agreement line is referenced on quote line.

-   **[View price adjustment details for a quote line item](https://www.servicenow.com/docs/access?context=view-price-adjustment-details-for-quote-lines&family=yokohama&ft:locale=en-US)**

Agents gain visibility into the price adjustments that were applied to the base and list price of the product ordered. This provides sales agent the visibility of how the net price is determined.


-   **[Quote PDF documents generation](https://www.servicenow.com/docs/access?context=quote-create-pdf-document&family=yokohama&ft:locale=en-US)**

Generate a quote PDF document. Quote PDF documents can have designated signers and be emailed to customers for signatures through Docusign. Customers can also create PDF templates that reflect customer branding and logos.


-   **[Hierarchical quote line list view](https://www.servicenow.com/docs/access?context=quote-management-view-hierarchical-line-items&family=yokohama&ft:locale=en-US)**

View quote lines as a hierarchical list. Agents can then view parent and child relationships for quote line items.


-   **[Product offer recommendations for quotes](https://www.servicenow.com/docs/access?context=quote-get-product-offer&family=yokohama&ft:locale=en-US)**

Enable your agents to get product offer recommendations that complement or supplement existing products within a quote.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Add pricing adjustment to a line item](https://www.servicenow.com/docs/access?context=quote-management-add-pricing-adjustment&family=zurich&ft:locale=en-US)**

Enables sales agents to quickly view, add, and edit manual price adjustments for quote line items directly from the list view, making it easier to manage both automatic and manual adjustments. The new experience streamlines the quoting process and allows adjustments to be applied to individual or multiple line items at once.


-   **[Price and quantity ramps on quote line items](https://www.servicenow.com/docs/access?context=add-price-ramps-on-a-quote-line-item&family=zurich&ft:locale=en-US)**

Create price and quantity ramps for product offerings in quotes to define incremental price and quantity changes over time. Product offerings eligible for ramps have the Ramps enabled option and Recurring price method selected. Agents can define ramps in two ways:

    1.  Ramp the parent line item, which automatically applies ramps to all child line items.
    2.  Leave the parent unramped, allowing child product offerings to have ramps defined individually.

Agents can also make manual price adjustments per segment. When a quote with ramps is converted to an order, ramps become read-only.


-   **[Quote header discount](https://www.servicenow.com/docs/access?context=add-header-discount-to-a-quote&family=zurich&ft:locale=en-US)**

Added a quote header discount feature that enables sales agents to apply a discount across multiple quote lines at once. This simplifies the quoting process and ensures consistent discount application, thereby improving overall sales efficiency and customer satisfaction.


-   **[Subscription revenue metrics](https://www.servicenow.com/docs/access?context=som-subscription-pricing&family=zurich&ft:locale=en-US)**

Provides sales agents better visibility of the entire quote cost and profit with the addition of Cost and Margin calculations to the following levels:

    -   **Quote Header**: Total one-time cost, Total monthly cost, Total cost, Total one-time margin, Total monthly margin, Total margin amount, Total one-time margin %, Total monthly margin %, and Total margin %.
    -   **Quote Line**: One-time cost, Monthly recurring cost, Cumulative one-time cost, Cumulative monthly cost, Cumulative margin %, and Cumulative Net Cost.
The automated calculation rules introduced at Quote Header and Quote Line levels enable informed discounting decisions and help prevent unprofitable deals.


</td></tr><tr><td>

Australia

</td><td>

-   **[Consolidate quotes](https://www.servicenow.com/docs/access?context=consolidate-quotes&family=australia&ft:locale=en-US)**

Maintain traceability from orders to all originating contract lines when creating orders from consolidated quotes. Additional calculated fields on order lines provide visibility into uplift values derived from consolidation rules.

-   **[Add price ramps on a quote line item](https://www.servicenow.com/docs/access?context=add-price-ramps-on-a-quote-line-item&family=australia&ft:locale=en-US)**

Enable agents to create and manage custom ramp structures with flexible segment durations. Make ramp changes across the quote life cycle, including amendments and renewals, while maintaining pricing and quantity consistency across ramp segments.

-   **[Quote approvals](https://www.servicenow.com/docs/access?context=explore-advanced-approval-for-sales&family=australia&ft:locale=en-US)**

Use the Advanced Approval Management to create approval workflows for end-to-end visibility and control of quote approvals.

    -   Track approval status, steps, sequencing, approvers, and comments in real time
    -   Manage quote states and edit permissions automatically as quotes move through Draft, In Review, Approved, and Rejected states
    -   Receive email notifications for approvers and requesters as approval actions are taken
    -   Configure approval conditions and sequencing across quotes, quote lines, and related entities using serial, parallel, or hybrid flows driven by business and compliance rules
    -   Preserve approval history across submissions and quote versions for a complete audit trail

-   **[Customer entities on Quote](https://www.servicenow.com/docs/access?context=quote-detail-form-fields&family=australia&ft:locale=en-US)**

Capture the deal type \(Direct or Indirect deals\) and align it with different routes to market for consistency, compliance, and operational efficiency across systems and teams.


-   **[Australia Patch 1](https://www.servicenow.com/docs/access?context=australia-patch-1&family=australia&ft:locale=en-US)[Summarize a quote using quote summarization with Now Assist](https://www.servicenow.com/docs/access?context=summarize-quote&family=australia&ft:locale=en-US)**

Generate a summary of a quote to:

    -   Summarize key quote components during early customer discussions or pre‑discovery.
    -   Provide an updated view of the quote after revisions, without requiring review of multiple records.
    -   Provide a single, consolidated snapshot of all actions, tasks, and notes derived from a quote in one place.
    -   Highlight custom pricing, discounts, and negotiated changes made during the quoting process.
    -   Review the quote prior to sending it to the customer to confirm accuracy and completeness.
    -   Support internal handoffs by summarizing the quoted offer for internal teams.

</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing Quote Management features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

-   **[Enhancements to price ramps on quote lines](https://www.servicenow.com/docs/access?context=add-price-ramps-on-a-quote-line-item&family=australia&ft:locale=en-US)**

Modify active ramp segments on amendment quotes to better manage pricing changes over time.

    -   Split an active ramp segment into multiple shorter segments within the original term, with the system automatically assigning the correct line types and effective dates for each resulting segment.
    -   Merge split segments back into the original ramp while the quote is in draft state.
    -   Remove segments that are no longer needed.
    -   Edit the quantity in the product configurator. The quantity field for the last ramp segment of configurable and bundled products is read-only.
-   **[Quote approvals](https://www.servicenow.com/docs/access?context=explore-advanced-approval-for-sales&family=australia&ft:locale=en-US)**

Build on existing quote approval workflows with greater control and flexibility

    -   Receive automated reminder notifications for pending approvals steps based on reminder schedules configured by your administrator.
    -   View the escalated approver on the approval step card when an approval step is escalated, so you can clearly identify who is responsible for the next action.
    -   Add ad-hoc approvers to an approval request outside the configured approval workflow when additional review is needed.
    -   Override an approval to advance a quote when permitted by your organization's approval configuration.

 See [Advanced Approval Management release notes](https://www.servicenow.com/docs/access?context=advanced-approval-management-for-sales-rn&family=australia&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some Quote Management features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Australia, some Quote Management features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

The Subscription start date and Subscription end date have been deprecated starting with the Q2 2024 release. Use the Contract start date and Contract end date to calculate Terms for setting subscriptions for recurring products.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Quote Management.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

Install Quote Management by requesting it from the ServiceNow Store.

 To add Docusign plugin to the Quote Management PDF document function, use the Docusign eSignature Spoke plugin \(sn\_docusign\_spoke\).

 Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=yokohama&ft:locale=en-US).

</td></tr><tr><td>

Zurich

</td><td>

Install Quote Management by requesting it from the ServiceNow Store.

 To add Docusign plugin to the Quote Management PDF document function, use the Docusign eSignature Spoke plugin \(sn\_docusign\_spoke\).

 Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=zurich&ft:locale=en-US).

</td></tr><tr><td>

Australia

</td><td>

Install Quote Management by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=australia&ft:locale=en-US).

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Quote Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Quote Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Quote Management, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

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

If there are specific localization considerations for Quote Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Quote Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   Enable agents to manage sales agreements in quotes.
-   Enable agents to view the price adjustments that are applied to the base and list price of a product in a quote.
-   Enable agents to create PDF documents from a quote using the ServiceNow PDF generator.
-   Use the hierarchical list view to view parent and child relationships within quote lines.
-   Provide agents with offer recommendations to upsell or cross-sell products that complement products in quotes.

 See [Quote Management](https://www.servicenow.com/docs/access?context=quote-management&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

Zurich

</td><td>

-   Support quote header discounts​.
-   View the cost and profit of the entire quote to support informed discounting decisions and avoid unprofitable deals.

 See [Quote Management](https://www.servicenow.com/docs/access?context=quote-management&family=zurich&ft:locale=en-US) for more information.

</td></tr><tr><td>

Australia

</td><td>

-   Quickly understand the financial outcome of quote changes, making it easier to review, approve, and act on updated quotes with visibility into exact amounts owed.
-   Enable sales agents to set a target outcome for a quote and let automated adjustments handle header-level discounting, removing manual trial-and-error and speeding up quote approvals.
-   Improve quote data consistency by validating contract start and end dates across quote headers, parent lines, and child lines, preventing date conflicts during updates.
-   Enable greater flexibility in managing amendment quotes by splitting active ramp segments into shorter intervals, adjusting quantities, and maintaining accurate line types throughout the quote life cycle.
-   Enhance quote approval workflows with automated reminders, escalations, override capabilities, and ad-hoc approvals for greater control and accountability throughout the approval process.
-   [Australia Patch 1](https://www.servicenow.com/docs/access?context=australia-patch-1&family=australia&ft:locale=en-US)Summarize a quote with Now Assist for immediate, comprehensive insights into quote details \(product, pricing, and terms\) to improve quote accuracy, help teams align, reduce manual review, catch issues early, and accelerate quote turnaround.

 See [Quote Management](https://www.servicenow.com/docs/access?context=quote-management&family=australia&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-yokohama-australia/rn-combined-intro.md)

