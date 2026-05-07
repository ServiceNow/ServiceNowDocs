---
title: CPQ release notes
description: CPQ is a configuration engine that acts as the "C" in Configure, Price, Quote. It uses an attribute-based approach to simplify complex product logic. The engine delivers dynamic blueprints, real-time user interfaces, and a Commerce Logic Engine that generates accurate outputs like bills of materials.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 6
---

# CPQ release notes

CPQ is a configuration engine that acts as the "C" in Configure, Price, Quote. It uses an attribute-based approach to simplify complex product logic. The engine delivers dynamic blueprints, real-time user interfaces, and a Commerce Logic Engine that generates accurate outputs like bills of materials.

With CPQ, organizations gain speed, flexibility, and precision in every sales and configuration experience.

Transaction Manager is a high‑performance transaction and quoting application that centralizes complex commercial logic—products, pricing, rules, and life cycle—into a single, configurable user experience that scales across CRM and back-office ecosystems.

## CPQ highlights for the Australia release

-   Configure and manage thousands of line items with a single‑page, scalable transaction user experience that includes search, filtering, rollups, and in‑memory rule execution.
-   Achieve consistent pricing, validations, and process control without heavy scripting using attribute‑based rules, events, calculations, and workflow stages.
-   Integrate with Salesforce, ServiceNow, and downstream systems using Transaction Manager's API‑first design, which acts as the system of record for transaction data while remaining CRM‑agnostic.
-   Duplicate an existing solution configuration node in a set, directly from the solution configuration navigation sidebar to use it as the starting point for a new node.

For more information, see [CPQ Configurator](https://www.servicenow.com/docs/access?context=explore-servicenowcpq&version=australia&pubname=australia-order-management&ft:locale=en-US).

## New in the Australia release

-   **[Transaction Access Control](https://www.servicenow.com/docs/access?context=cpq-transaction-manager-transaction-access-control&version=australia&pubname=australia-order-management&ft:locale=en-US)**

    Control precisely who can view and edit each transaction to improve security and compliance using Transaction Access Control. Admins and creators automatically receive full access and can grant access to others. Any user with access can also grant or remove access for others.

-   **[Transaction AI – Bulk Line Update via File Upload](https://www.servicenow.com/docs/access?context=cpq-transaction-converse&version=australia&pubname=australia-order-management&ft:locale=en-US)**

    Enables AI column and line item mapping to allow for seamless transition from third-party systems. Transaction AI can be used to add items from favorites enabling users to quickly add commonly used products via voice or text. Triggers events for users via voice or chat

-   **AI Admin Uploads for Advanced Product Configurator and Transaction Manager**

    Enables admins to upload business and blueprint related context documents to provide Configuration AI and Transaction AI more context of business, standards product information etc.

-   **[Export Lines UI Effect](https://www.servicenow.com/docs/access?context=transaction-manager-layouts-ui-effects&version=australia&pubname=australia-order-management&ft:locale=en-US)**

    Export Transaction Lines to a .csv file via a new UI effect. The exported file includes all lines in the transaction that meet the current line sort, filter, and column show/hide settings.

-   **[Layout editor](https://www.servicenow.com/docs/access?context=layout_editor&version=australia&pubname=australia-order-management&ft:locale=en-US)**

    Design and maintain layouts in a visual-based editor. Add and organize layout components, configure UI Effect and element properties, manage theming and more, all in an intuitive visual interface.

-   **Share product favorites**

    Improve collaboration and user efficiency by sharing saved favorite products and configurations with other users, enabling sharing and reuse of product configurations.

-   **Tenant-configurable namespace prefixes for Salesforce fields**

    Configure a custom namespace at the tenant level to align Salesforce fields and references with your managed package. When a custom namespace is set, CPQ uses it for all generated Salesforce fields and all field lookups instead of the default LGK\_ prefix. If no custom namespace is configured, the system defaults to LGK\_ to preserve compatibility with existing tenants.

-   **Dynamic selection of Sales CRM catalog items in the CPQ admin UI**

    Select product offerings, product specifications, and product characteristic values directly in the CPQ admin UI without manually entering system IDs. Search and select Sales CRM catalog items using built-in UI selectors when configuring products, creating product rules, or setting up pickers, advanced product actions, BOM enrichments, and library functions.

-   **[Node cloning for solution configuration](https://www.servicenow.com/docs/access?context=node-cloning-for-solution-configuration&version=australia&pubname=australia-order-management&ft:locale=en-US)**

    Duplicate an existing solution configuration node in a set, directly from the solution configuration navigation sidebar to use it as the starting point for a new node. The original node in a set must be in the valid state.

-   ****

    Manage transaction lines using natural language. You can upload CSV or XLSX files directly in the chat to add or update lines, map file columns to transaction fields through a guided conversation, preview the changes, and apply or cancel them before execution. Target specific transaction lines by referencing line numbers or ranges in your prompts, enabling precise updates such as modifying field values or removing selected lines.

-   **Upload context documents for AI-assisted configuration and quoting**

    Upload organizational documents — such as pricing policies, standard operating procedures, product specifications, and playbooks — to provide Config AI and Quote AI with company-specific context during configuration and quoting. Supported formats include Excel, Word, PDF, text, markdown, and images \(with OCR support\). These documents are also used by Transaction AI to improve recommendations, product matching, and event suggestions during transaction sessions.

-   **[Config Converse](https://www.servicenow.com/docs/access?context=cpq-config-converse&version=australia&pubname=australia-order-management&ft:locale=en-US)**

    Configure complex products using natural language. Buyers can submit a configuration request through a prompt field on an administrator-designed landing page. The request is processed by an AI agent, which interprets the input and drives the product configuration session. For renewal scenarios, Config AI can reuse a previous configuration as a starting point, enabling faster upsell and cross-sell opportunities while maintaining continuity across renewal cycles. Using Config AI, you can:

    -   Submit product configuration requests using natural language through a prompt field on the landing page.
    -   Complete product configuration through a conversational interface within the buying experience.
    -   Design the Config Converse landing page using the CPQ layout editor with configurable elements such as text, images, fields, and a prompt component.
    -   Allow buyers to skip the landing page using a dismissal preference in the layout editor.
    -   Check for a predicted configuration after the initial buyer request. Apply it automatically when Smart Predict is enabled for both the tenant and the layout. Smart Predict must be enabled separately at the tenant level and at the layout level.
-   **Transaction edit history**

    Use the event start time column in the transaction edit history to help admins track the duration of individual transaction events.

-   **Price and quantity ramps in the CPQ Configurator**

    Use the CPQ Configurator to configure price and quantity ramps for subscription products with recurring pricing. View and manage ramp segments directly within the configuration session through a summary table and detailed modal. Apply quantity updates as a delta across segments from the effective date, and save all changes back to the source. Relaunch the configurator for ramped products to support MACD scenarios, with child lines inheriting the correct ramp associations.


## Activation information

Features such as product and configuration sharing in Transaction Manager features, require activation by ServiceNow. Submit a support ticket to enable these features.

## Accessibility information

The CPQ runtime configuration experience includes the following keyboard and screen reader accessibility improvements.

-   Navigate and select options in single-select picklists, selectable product cards, and the product picker grid using a keyboard.
-   Shopping cart and bill of materials \(BOM\) column headers are announced as text with full, untruncated labels, and table cells reference their row and column headers for screen reader context.
-   Field labels are read across transaction runtime fields, keyboard focus returns to the date input after a calendar selection, and the field edit page provides more descriptive context for related item tiles and tooltips.

## Localization information

Japanese Localization for CPQ admin UI: The CPQ admin UI supports internationalization for the CPQ Configurator and Transaction Manager. Static user interface elements, including labels, headings, and system text, can be displayed in Japanese. This is part of an initial pilot to support SoftBank onboarding. Administrators can select their preferred language through the ServiceNow platform. If any static content is not translated, the system automatically falls back to English. It also supports Japanese character input across applicable fields and controls. User-generated content remains in the language in which it is entered.

## Related ServiceNow applications and Features

-   **[Sales Customer Relationship Management](https://www.servicenow.com/docs/access?context=order-mgt-overview&version=australia&pubname=australia-order-management&ft:locale=en-US)**

    Sales Customer Relationship Management applications enable you to manage the product sales life cycle in your organization. This includes pre-sales leads and opportunities, sales quote generation, order capture, order fulfillment, order and invoice cases, and post-sales order changes and contract renewals.


**Parent Topic:**[Sales Customer Relationship Management release notes](sales-order-management-rn-landing.md)

