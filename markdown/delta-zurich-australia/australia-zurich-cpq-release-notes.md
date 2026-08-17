---
title: Combined CPQ release notes for upgrades from Zurich to Australia
description: Consolidated page of all release notes for CPQ from Zurich to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-zurich-australia/australia-zurich-cpq-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-08-17"
reading_time_minutes: 13
breadcrumb: [Products combined by family]
---

# Combined CPQ release notes for upgrades from Zurich to Australia

Consolidated page of all release notes for CPQ from Zurich to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family CPQ release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Zurich to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading CPQ to Australia

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

Between your current release family and Australia, new features were introduced for CPQ.

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

-   **[Product pickers](https://www.servicenow.com/docs/access?context=product_picker_overview&family=australia&ft:locale=en-US)**

Enable administrators to create and manage fields, options, or actions of product pickers in ServiceNow CPQ Administrator.

-   **[Price and quantity ramps in the CPQ Configurator](https://www.servicenow.com/docs/access?context=defining-products-with-ramps&family=australia&ft:locale=en-US)**

Use the CPQ Configurator to configure price and quantity ramps for subscription products with recurring pricing. View and manage ramp segments through a summary table and detailed modal, apply quantity updates as a delta across segments, and relaunch the configurator for ramped products to support MACD scenarios.

-   **[Source line configuration field mappings](https://www.servicenow.com/docs/access?context=enable-solution-configuration&family=australia&ft:locale=en-US)**

Reduce manual data entry during configuration by defining mappings in the CPQ admin UI that automatically populate config fields when a session initializes. Map incoming request data such as line or characteristics to product picker subfields and other config fields, and import or export mappings as part of a blueprint export or standalone CSV.

-   **[Config AI Agent-to-Agent \(A2A\) support](https://www.servicenow.com/docs/access?context=cpq-transaction-manager-rn&family=australia&ft:locale=en-US)**

Allow agents to communicate directly with Config AI using the A2A protocol to generate and validate product configurations as part of broader agentic workflows. Onboarding and offboarding of the Config AI agent is handled automatically based on a tenant setting.

-   **[ServiceNow CPQ Configurator guided setup](https://www.servicenow.com/docs/access?context=setup-cpq-integrator&family=australia&ft:locale=en-US)**

Use the guided setup for initial configuration of the CPQ configurator to define product pricing, create pricing rules, and create complex product bundles. The guided setup provides a structured step-by-step process that streamlines the initial setup process.

-   **[Transaction Access Control](https://www.servicenow.com/docs/access?context=cpq-transaction-manager-transaction-access-control&family=australia&ft:locale=en-US)**

Control precisely who can view and edit each transaction to improve security and compliance using Transaction Access Control. Admins and creators automatically receive full access and can grant access to others. Any user with access can also grant or remove access for others.

-   **[Transaction AI – Bulk Line Update via File Upload](https://www.servicenow.com/docs/access?context=cpq-transaction-converse&family=australia&ft:locale=en-US)**

Enables AI column and line item mapping to allow for seamless transition from third-party systems. Transaction AI can be used to add items from favorites enabling users to quickly add commonly used products via voice or text. Triggers events for users via voice or chat

-   **[AI Admin Uploads for Advanced Product Configurator and Transaction Manager](https://www.servicenow.com/docs/access?context=ai-admin-uploads&family=australia&ft:locale=en-US)**

Enables admins to upload business and blueprint related context documents to provide Configuration AI and Transaction AI more context of business, standards product information etc.

-   **[Export Lines UI Effect](https://www.servicenow.com/docs/access?context=transaction-manager-layouts-ui-effects&family=australia&ft:locale=en-US)**

Export Transaction Lines to a .csv file via a new UI effect. The exported file includes all lines in the transaction that meet the current line sort, filter, and column show/hide settings.

-   **[Layout editor](https://www.servicenow.com/docs/access?context=layout_editor&family=australia&ft:locale=en-US)**

Design and maintain layouts in a visual-based editor. Add and organize layout components, configure UI Effect and element properties, manage theming and more, all in an intuitive visual interface.

-   **Share product favorites**

Improve collaboration and user efficiency by sharing saved favorite products and configurations with other users, enabling sharing and reuse of product configurations.

-   **Tenant-configurable namespace prefixes for Salesforce fields**

Configure a custom namespace at the tenant level to align Salesforce fields and references with your managed package. When a custom namespace is set, CPQ uses it for all generated Salesforce fields and all field lookups instead of the default LGK\_ prefix. If no custom namespace is configured, the system defaults to LGK\_ to preserve compatibility with existing tenants.

-   **[Dynamic selection of Sales CRM catalog items in the CPQ admin UI](https://www.servicenow.com/docs/access?context=dynamic-catalog-item-selection&family=australia&ft:locale=en-US)**

Select product offerings, product specifications, and product characteristic values directly in the CPQ admin UI without manually entering system IDs. Search and select Sales CRM catalog items using built-in UI selectors when configuring products, creating product rules, or setting up pickers, advanced product actions, BOM enrichments, and library functions.

-   **[Node cloning](https://www.servicenow.com/docs/access?context=node-cloning-for-solution-configuration&family=australia&ft:locale=en-US)**

Duplicate an existing solution configuration node in a set, directly from the solution configuration navigation sidebar to use it as the starting point for a new node. The original node in a set must be in the valid state.

-   **[\[Placeholder link text to key cpq-transaction-converse\]](https://www.servicenow.com/docs/access?context=cpq-transaction-converse&family=australia&ft:locale=en-US)**

Manage transaction lines using natural language. You can upload CSV or XLSX files directly in the chat to add or update lines, map file columns to transaction fields through a guided conversation, preview the changes, and apply or cancel them before execution. Target specific transaction lines by referencing line numbers or ranges in your prompts, enabling precise updates such as modifying field values or removing selected lines.

-   **Upload context documents for AI-assisted configuration and quoting**

Upload organizational documents — such as pricing policies, standard operating procedures, product specifications, and playbooks — to provide Config AI and Quote AI with company-specific context during configuration and quoting. Supported formats include Excel, Word, PDF, text, markdown, and images \(with OCR support\). These documents are also used by Transaction AI to improve recommendations, product matching, and event suggestions during transaction sessions.

-   **[Config Converse](https://www.servicenow.com/docs/access?context=cpq-config-converse&family=australia&ft:locale=en-US)**

Configure complex products using natural language. Buyers can submit a configuration request through a prompt field on an administrator-designed landing page. The request is processed by an AI agent, which interprets the input and drives the product configuration session. For renewal scenarios, Config AI can reuse a previous configuration as a starting point, enabling faster upsell and cross-sell opportunities while maintaining continuity across renewal cycles. Using Config AI, you can:

    -   Submit product configuration requests using natural language through a prompt field on the landing page.
    -   Complete product configuration through a conversational interface within the buying experience.
    -   Design the Config Converse landing page using the CPQ layout editor with configurable elements such as text, images, fields, and a prompt component.
    -   Allow buyers to skip the landing page using a dismissal preference in the layout editor.
    -   Check for a predicted configuration after the initial buyer request. Apply it automatically when Smart Predict is enabled for both the tenant and the layout. Smart Predict must be enabled separately at the tenant level and at the layout level.
-   **Transaction edit history**

Use the event start time column in the transaction edit history to help admins track the duration of individual transaction events.

-   **[Price and quantity ramps in the CPQ Configurator](https://www.servicenow.com/docs/access?context=cpq-modify-a-product-subscription-with-ramped-pricing-and-quantities&family=australia&ft:locale=en-US)**

Use the CPQ Configurator to configure price and quantity ramps for subscription products with recurring pricing. View and manage ramp segments directly within the configuration session through a summary table and detailed modal. Apply quantity updates as a delta across segments from the effective date, and save all changes back to the source. Relaunch the configurator for ramped products to support MACD scenarios, with child lines inheriting the correct ramp associations.

-   **[Manage quotes using the Quote AI Agent](https://www.servicenow.com/docs/access?context=manage-quote-using-quote-ai-agent&family=australia&ft:locale=en-US)**

Automating quote creation, product configuration, discount application, and client communication through the Quote AI Agent in Now Assist.

-   **[CPQ Quote Experience in CPQ](https://www.servicenow.com/docs/access?context=sales-crm-tm-quoting-configure&family=australia&ft:locale=en-US)**

Create and manage quotes in the Quote Experience within Sales CRM, a modern quoting interface built on the configurable ServiceNow quoting engine. Configure the quote layout with refined UI features. Users can build quotes, submit them for approval directly from the quoting experience, and advance them through configurable approval stages before an order is created. Approvals integrate with the standard ServiceNow approval engine.

-   **[Approvals in the CPQ Quote Experience](https://www.servicenow.com/docs/access?context=configuring-advanced-approval-management&family=australia&ft:locale=en-US)**

Configure a complete approval framework for quotes in the Quote Experience in Sales CRM. Define approval workflows through configurable stages, rules, and trigger conditions that integrate with the standard ServiceNow approval engine. Set up the approver experience, including notification channels \(email, in-app, and dashboard\), escalation rules for overdue requests, delegation for approver coverage, and comment requirements for audit purposes. Approvers receive notifications through their configured channels and can review, approve, reject, or delegate requests directly from the quote record or approval dashboard before an order is created.

-   **[Opportunity and quote synchronization](https://www.servicenow.com/docs/access?context=sync-quote-to-opportunity&family=australia&ft:locale=en-US)**

Enable sales users to designate a quote as the primary quote for an opportunity and synchronize its lines back to the source opportunity record. The Enable Sync and Disable Sync events, integration, rules, and fields are productized into the Sales CRM quoting experience. Only one quote can be primary at a time per opportunity.

-   **[Enable order creation from a quote](https://www.servicenow.com/docs/access?context=configure-create-order-integration&family=australia&ft:locale=en-US)**

Create an order directly from a quote in the CPQ Quote experience. Convert an entire quote into an order in a single step, or select specific top-level line items to order only part of a quote. Quote line items and their related details carry straight onto the order as order lines, giving sales teams a faster, more accurate quote-to-order handoff with less manual rework.


</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing CPQ features.

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
</table>## Removed

Between your current release family and Australia, some CPQ features or functionality were removed.

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
</table>## Deprecations

Between your current release family and Australia, some CPQ features or functionality were deprecated.

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

Review information on how to activate CPQ.

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

Features such as product and configuration sharing in ServiceNow Quote Experience features, require activation by ServiceNow. Submit a support ticket to enable these features.

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for CPQ we have noted them here.

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

If any specific browser requirements were introduced or changed for CPQ we have noted them here.

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

Review details on accessibility information for CPQ, such as specific requirements or compliance levels.

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

The CPQ runtime configuration experience includes the following keyboard and screen reader accessibility improvements.

-   Navigate and select options in single-select picklists, selectable product cards, and the product picker grid using a keyboard.
-   Shopping cart and bill of materials \(BOM\) column headers are announced as text with full, untruncated labels, and table cells reference their row and column headers for screen reader context.
-   Field labels are read across transaction runtime fields, keyboard focus returns to the date input after a calendar selection, and the field edit page provides more descriptive context for related item tiles and tooltips.
-   The CPQ and ServiceNow Quote Experience runtime interface supports 400% zoom without loss of content or functionality, meeting the WCAG 2.2 success criterion 1.4.10 \(Reflow\). Users who rely on screen magnification can navigate and interact with the quoting experience at 400% zoom on a standard viewport.

 The CPQ admin UI includes the following keyboard and screen reader accessibility improvements:

-   Skip links on list pages allow keyboard users to bypass navigation and go directly to main content or grid rows.
-   Grid column headers announce sort direction, and sort indicators appear as separate elements to reduce announcement clutter.
-   The New button announces the specific entity type to be created, field edit page tooltips are read aloud on focus, and related item tiles provide more descriptive context for assistive technology users.

 The CPQ runtime configuration and transaction experience includes the following keyboard and screen reader accessibility improvements:

-   Navigate and select options in single-select picklists, selectable product cards, and the product picker grid using a keyboard.
-   Radio button groups and rectangular pushbutton groups retain their selection when navigating away using a screen reader.
-   The complete text of shopping cart or BOM column headers is announced; table cells reference their row and column headers for screen reader context.
-   Field labels are read across transaction runtime fields, and keyboard focus returns to the date input after a calendar selection.
-   Expandable section headers announce error indicators, field-level error messages are read aloud on input focus, and help popover content is reachable by screen readers.

 The CPQ AI runtime experience includes the following keyboard and screen reader accessibility improvements:

-   The Config AI view is reachable and navigable using a keyboard, so users aren't misdirected to fields in the main layout during configuration sessions.
-   Quote AI is accessible using keyboard navigation and screen readers.
-   Smart Predict runtime experience elements, including trigger icons, notification icons, and modal interactions, are accessible using keyboard navigation and screen readers.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for CPQ we have noted them here.

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

Japanese Localization for CPQ admin UI: The CPQ admin UI supports internationalization for the CPQ Configurator and Transaction Manager. Static user interface elements, including labels, headings, and system text, can be displayed in Japanese. This is part of an initial pilot to support SoftBank onboarding. Administrators can select their preferred language through the ServiceNow platform. If any static content is not translated, the system automatically falls back to English. It also supports Japanese character input across applicable fields and controls. User-generated content remains in the language in which it is entered.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for CPQ we have noted them here.

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

-   Configure price and quantity ramps for subscription products directly in the CPQ Configurator, with support for split lines, reconfiguration, and delta pricing.
-   Pre-populate configuration fields at the start of a configuration session by mapping incoming request data, such as line attributes and characteristics, to config fields directly in the CPQ admin UI.
-   Enable agents to invoke Config AI capabilities directly using the Agent-to-Agent \(A2A\) protocol, without requiring manual integration setup.
-   Upload deal-specific documents such as customer emails, RFPs, and meeting notes so that Config AI and Quote AI have full deal context when generating configurations and quotes.
-   Upload organizational documents such as pricing policies, standard operating procedures, and product specifications so that Config AI and Quote AI reference your company's specific rules and standards during configuration and quoting sessions.
-   Manage transaction lines more precisely using natural language by targeting specific line numbers, adding favorited products, triggering events, updating header fields, and clearing field values directly from a prompt.
-   Review and act on Smart Predict recommendations directly inline in the configuration layout, with controls to accept or dismiss individual values or accept all recommendations at once at the layout or group level.
-   Use the guided setup to step through the initial configuration of the CPQ configurator.
-   Configure and manage thousands of line items with a single‑page, scalable transaction user experience that includes search, filtering, rollups, and in‑memory rule execution.
-   Achieve consistent pricing, validations, and process control without heavy scripting using attribute‑based rules, events, calculations, and workflow stages.
-   Integrate with Salesforce, ServiceNow, and downstream systems using ServiceNow Quote Experience API‑first design, which acts as the system of record for transaction data while remaining CRM‑agnostic.
-   Duplicate an existing solution configuration node in a set, directly from the solution configuration navigation sidebar to use it as the starting point for a new node.
-   Enable AI-assisted quote creation, modification, and automated generation by interpreting user intent and contextual triggers with Quote AI Agent.

 For more information, see [ServiceNow CPQ Configurator](https://www.servicenow.com/docs/access?context=explore-servicenowcpq&family=australia&ft:locale=en-US).

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-zurich-australia/rn-combined-intro.md)

