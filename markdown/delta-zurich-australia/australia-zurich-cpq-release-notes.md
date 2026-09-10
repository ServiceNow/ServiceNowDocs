---
title: Combined CPQ release notes for upgrades from Zurich to Australia
description: Consolidated page of all release notes for CPQ from Zurich to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-zurich-australia/australia-zurich-cpq-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 7
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

-   **[\[Placeholder link text to key cpq-transaction-converse\]](https://www.servicenow.com/docs/access?context=cpq-transaction-converse&family=australia&ft:locale=en-US)**

Manage transaction lines using natural language. You can upload CSV or XLSX files directly in the chat to add or update lines, map file columns to transaction fields through a guided conversation, preview the changes, and apply or cancel them before execution. Target specific transaction lines by referencing line numbers or ranges in your prompts, enabling precise updates such as modifying field values or removing selected lines.

-   **Upload context documents for AI-assisted configuration and quoting**

Upload organizational documents — such as pricing policies, standard operating procedures, product specifications, and playbooks — to provide Config AI and Quote AI with company-specific context during configuration and quoting. Supported formats include Excel, Word, PDF, text, markdown, and images \(with OCR support\). These documents are also used by Transaction AI to improve recommendations, product matching, and event suggestions during transaction sessions.

-   **Transaction edit history**

Use the event start time column in the transaction edit history to help admins track the duration of individual transaction events.

-   **[Price and quantity ramps in the CPQ Configurator](https://www.servicenow.com/docs/access?context=cpq-modify-a-product-subscription-with-ramped-pricing-and-quantities&family=australia&ft:locale=en-US)**

Use the CPQ Configurator to configure price and quantity ramps for subscription products with recurring pricing. View and manage ramp segments directly within the configuration session through a summary table and detailed modal. Apply quantity updates as a delta across segments from the effective date, and save all changes back to the source. Relaunch the configurator for ramped products to support MACD scenarios, with child lines inheriting the correct ramp associations.


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

-   **Activation information**

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

-   **Accessibility information**

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

-   **Localization information**

Japanese Localization for CPQ admin UI: The CPQ admin UI supports internationalization for the CPQ Configurator and Transaction Manager. Static user interface elements, including labels, headings, and system text, can be displayed in Japanese. This is part of an initial pilot to support SoftBank onboarding. Administrators can select their preferred language through the ServiceNow platform. If any static content is not translated, the system automatically falls back to English. It also supports Japanese character input across applicable fields and controls. User-generated content remains in the language in which it is entered.

Enhanced localization in CPQ: Translation and localization support is enhanced to include product offering labels, definitions, and field text in CPQ. Content is translated at compile time, enabling multilingual configuration workflows and a more consistent localized experience.


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

