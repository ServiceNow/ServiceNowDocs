---
title: Combined Purchase Order Management release notes for upgrades from Xanadu to Brazil
description: Consolidated page of all release notes for Purchase Order Management from Xanadu to Brazil.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-xanadu-brazil/brazil-xanadu-purchaseordermanagement-release-notes.html
release: brazil
topic_type: reference
last_updated: "2026-09-24"
reading_time_minutes: 7
breadcrumb: [Products combined by family]
---

# Combined Purchase Order Management release notes for upgrades from Xanadu to Brazil

Consolidated page of all release notes for Purchase Order Management from Xanadu to Brazil.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Purchase Order Management release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Xanadu to Brazil.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Purchase Order Management to Brazil

Before you upgrade to Brazil, review these pre- and post-upgrade tasks and complete the tasks as needed.

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

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Brazil, new features were introduced for Purchase Order Management.

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

-   **[Reporting delivery plan issues](https://www.servicenow.com/docs/access?context=reporting-delivery-plan-issues&family=zurich&ft:locale=en-US)**

Suppliers can report delivery plan issues related to purchase order line through the Supplier Collaboration Portal, ensuring prompt visibility for the appropriate buyer. Suppliers can also track and collaborate with the buyers on the purchase order exception on the related record in Supplier Lifecycle Operations.


 -   **[Centralized interface for purchase order exceptions](https://www.servicenow.com/docs/access?context=purch-order-mgmt-ws&family=zurich&ft:locale=en-US)**

The Purchase Order Management page provides operational buyers with a centralized interface to monitor and review purchase order exceptions. Users can quickly identify urgent issues, view recent tasks, and take approval actions, improving workflow visibility and exception handling.


 -   **[Resolving purchase order exceptions](https://www.servicenow.com/docs/access?context=resolving-purchase-order-exceptions&family=zurich&ft:locale=en-US)**

Enables buyers to resolve purchase order exceptions directly from the exception page, with options to accept supplier proposals or make custom edits. It also allows buyers to find alternative suppliers with open orders for the same materials and request order expediting or increased quantities.


</td></tr><tr><td>

Australia

</td><td>

-   **[Support for purchase order confirmation data](https://www.servicenow.com/docs/access?context=master-data-tables-for-pom&family=australia&ft:locale=en-US)**

Purchase order confirmation and confirmation line tables are available by default when you install the Purchase Order Management plugin, enabling import of this information from external systems. These tables capture supplier acknowledgment and provide buyers visibility into order execution readiness. Note: Integration with external systems is not provided by default.


 -   **[Enhancements to the automatic purchase order exception creation from email workflow](https://www.servicenow.com/docs/access?context=convert-emails-to-exceptions&family=australia&ft:locale=en-US)**

The Create purchase order exception from email workflow is enhanced to automatically identify purchase order lines. The workflow automatically identifies PO lines when the email contains an ERP PO and PO line ID instead of just a ServiceNow PO line ID. The workflow also supports additional languages \(French, Canadian French, German, Japanese, and Dutch\) for emails. These enhancements help in improving supplier communication and reducing manual intervention.


</td></tr><tr><td>

Brazil

</td><td>

-   **[Automated purchase order confirmation creation from emails](https://www.servicenow.com/docs/access?context=automated-po-confirmation-creation-emails&family=brazil&ft:locale=en-US)**

Reduce manual tracking of supplier emails by automatically converting emails with purchase order details into draft confirmations.

-   **[Create a purchase order confirmation in Supplier Collaboration Portal](https://www.servicenow.com/docs/access?context=create-po-confirmation-in-supplier-portal&family=brazil&ft:locale=en-US)**

Provide buyers certainty about their orders by creating purchase order confirmations directly from the Supplier Collaboration Portal.


</td></tr></tbody>
</table>## Changes

Between your current release family and Brazil, some changes were made to existing Purchase Order Management features.

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

</td></tr><tr><td>

Australia

</td><td>

-   **[Changes in the purchase order exception page](https://www.servicenow.com/docs/access?context=purch-order-exception-details&family=australia&ft:locale=en-US)**

The New activity today section on the Purchase Order Management landing page has been expanded to list the most recent exceptions and tasks.

The **Exception intelligence** tab is enhanced to show the supplier spend patterns over time.


</td></tr><tr><td>

Brazil

</td><td>

-   **[Automated purchase order exception creation from emails](https://www.servicenow.com/docs/access?context=convert-emails-to-exceptions&family=brazil&ft:locale=en-US)**

Previously, emails containing multiple intents would create only a single case for the dominant intent and default to a Universal Request for others. Now each identified intent triggers its own case creation, eliminating manual conversion work.

-   **[Changes to the Purchase Order Confirmation Data Model](https://www.servicenow.com/docs/access?context=po-confirmation-line-table&family=brazil&ft:locale=en-US)**

The Confirmation source and Status fields in the Purchase Order Confirmation \[sn\_poem\_po\_confirmation\] table have new values: AI Agent and Draft Retracted.


</td></tr></tbody>
</table>## Removed

Between your current release family and Brazil, some Purchase Order Management features or functionality were removed.

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

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Brazil, some Purchase Order Management features or functionality were deprecated.

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

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

-   **Now LLM Service**

Starting with the September 2026 release, Gemma 4 joins our growing portfolio of open-weight models available through Now LLM Service. The latest industry advancements are available alongside sovereignty-focused options. All models are hosted and governed by ServiceNow with the same infrastructure and data protections. Older models will remain available for existing published AI skills, agents, and agentic workflows, but will no longer be available for new development or configuration. For details, see the [KB3066214: ServiceNow Otto Model Upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3066214) article in the Now Support Knowledge Base.


</td></tr></tbody>
</table>## Activation information

Review information on how to activate Purchase Order Management.

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

-   **Activation information**

Install Purchase Order Management by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=zurich&ft:locale=en-US).


</td></tr><tr><td>

Australia

</td><td>

-   **Activation information**

Install Purchase Order Management by requesting it from the ServiceNow Store. 


</td></tr><tr><td>

Brazil

</td><td>

-   **Activation information**

Purchase Order Management is available in the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=brazil&ft:locale=en-US).


</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Purchase Order Management we have noted them here.

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

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Purchase Order Management we have noted them here.

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

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Purchase Order Management, such as specific requirements or compliance levels.

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

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Purchase Order Management we have noted them here.

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

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Purchase Order Management we have noted them here.

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

-   Use a collaborative workspace to coordinate with suppliers and relevant stakeholders simultaneously.
-   Receive automatic notifications, automatically prioritize them, and assign them to the appropriate person.
-   Utilize resolution tools to automatically update orders and review order plans for the affected material and location.

 See [Purchase Order Management](https://www.servicenow.com/docs/access?context=purchase-order-mgmt-landing-page&family=zurich&ft:locale=en-US) for more information.

</td></tr><tr><td>

Australia

</td><td>

-   **[Now Assist &gt; ServiceNow Otto® announcement](https://www.servicenow.com/docs/access?context=sn-ai-implementation-landing&family=australia&ft:locale=en-US)**

ServiceNow Otto introduced AI on the platform. As that experience has evolved, there's a new name for the experience. ServiceNow Otto® is the conversational AI platform integrated into ServiceNow workflows. It provides agentic capabilities, supports multimodal interactions across web, mobile, and messaging channels, and enables autonomous orchestration for cross-system workflows.

-   **[ServiceNow product tiers](https://www.servicenow.com/docs/access?context=ai-native-sku-overview&family=australia&ft:locale=en-US)**

The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.


 -   Create PO exceptions from universal requests during triage.
-   Create PO exception tasks and track their progress directly from the PO exception.
-   Get relevant data insights with improved visualization of new purchase order exceptions and PO exception workload distribution.
-   Convert supplier emails into purchase order exceptions automatically when a registered supplier contact sends emails to a supplier inbox.
-   Analyze delivery gaps and view suggested edits to orders with alternative suppliers with the Define purchase order exception mitigation strategy agentic workflow
-   Support for purchase order confirmation data.
-   Enhancements to the automatic purchase order exception creation from email workflow.

 See [Purchase Order Management](https://www.servicenow.com/docs/access?context=purchase-order-mgmt-landing-page&family=australia&ft:locale=en-US) for more information.

</td></tr><tr><td>

Brazil

</td><td>

-   Provide prompt visibility for the appropriate buyer by reporting delivery plan issues related to a purchase order.
-   Expedite detection and resolution of purchase order exceptions.
-   Use agentic workflow to identify and execute mitigation strategies by analyzing delivery gaps and proposing order changes with alternative suppliers.

 See [Purchase Order Management](https://www.servicenow.com/docs/access?context=purchase-order-mgmt-landing-page&family=brazil&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/delta-xanadu-brazil/rn-combined-intro.md)

