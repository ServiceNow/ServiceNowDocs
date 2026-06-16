---
title: Shopping Hub release notes
description: Version history for the Shopping Hub application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-psm-shoppinghub.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 8
breadcrumb: [ServiceNow Store - Sourcing and Procurement Operations release notes, ServiceNow Store - Source-to-Pay Operations release notes, ServiceNow Store release notes]
---

# Shopping Hub release notes

Version history for the Shopping Hub application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 9.7.1 - June 2026**

    Defect fixes.

-   **Version 11.0.0 - March 2026 \(Zurich\)**
    -   New:
        -   Enhanced the shopping experience by enabling users to shop on behalf of others, with improved visibility and management of these purchases. Users can select shoppers without the delegate route, view business owner purchases in My Purchases, and modify purchases made on behalf of others.
        -   Enabled decimal quantities for service items in Shopping Hub and Employee Center, configurable through the Unit of Measure Decimal Support decision table.
    -   Changed: Enhanced multi‑currency support to display localized currencies across To‑Dos, emails, and the product Bundles page.
-   **Version 9.5.0 - March 2026**
    -   New:
        -   Enhanced the shopping experience by enabling users to shop on behalf of others, with improved visibility and management of these purchases. Users can select shoppers without the delegate route, view business owner purchases in My Purchases, and modify purchases made on behalf of others.
        -   Enabled decimal quantities for service items in Shopping Hub and Employee Center, configurable through the Unit of Measure Decimal Support decision table.
    -   Changed: Enhanced multi‑currency support to display localized currencies across To‑Dos, emails, and the product Bundles page.
-   **Version 10.0.1 - December 2025 \(Zurich\)**
    -   New:
        -   Multi-currency: Supports shoppers and approvers in viewing and selecting their local currency throughout the Shopping Hub experience, including supplier cards, product detail pages, cart, checkout, My Purchases, and Request Tracker. Currency filtering has also been enhanced as part of this capability.
        -   Additional line-level questions: Enables procurement admins to configure and render unique question types for quick and full checkout experiences for each product or service line. Selections for each unique question persist in Workspace and Platform views on both purchase requisition lines and purchase order lines.
-   **Version 9.4.1 - December 2025 \(Yokohama\)**
    -   New:
        -   Multi-currency: Supports shoppers and approvers in viewing and selecting their local currency throughout the Shopping Hub experience, including supplier cards, product detail pages, cart, checkout, My Purchases, and Request Tracker. Currency filtering has also been enhanced as part of this capability.
        -   Additional line-level questions: Enables procurement admins to configure and render unique question types for quick and full checkout experiences for each product or service line. Selections for each unique question persist in Workspace and Platform views on both purchase requisition lines and purchase order lines.
-   **Version 9.12.0 - October 2025**

    New: Conversational intake for sourcing and procurement in Agentic workflow: Employees can request up to three items in a single session. The agent intelligently routes each item within the conversation before displaying a web form for Shopping Hub checkout \(on-catalog\) or Employee Center request forms \(off-catalog; I need a product and I need a service forms\).

-   **Version 9.9.0 - August 2025**

    New: Added support for decimal-based quantities during full and quick checkout flows in Shopping Hub.

-   **Version 9.3.0 - May 2025**

    Changed: The All categories option has been removed from the Categories tab in Shopping Hub due to low usage and its impact on search performance.

-   **Version 9.0.3 - March 2025**

    Fixed: Fixed an issue where the product details page appeared blank for API-enabled purchases after an API search.

-   **Version 9.0.0 - February 2025**
    -   New:
        -   With the unified request tracking feature, shoppers can gain complete transparency and visibility across the entire source-to-pay process. Key advantages include:
            -   Search for purchases using keywords and metadata.
            -   Identify purchases based on purchase requisition lines and purchase order lines.
            -   Track purchases through sourcing requests, purchase orders, and purchase requisitions, even if the associated records are in a closed or completed state.
            -   Gain visibility into prior records that contributed to the creation of the current record type.
-   **Version 8.3.2 - January 2025**

    Changed: A banner has been added to the Shopping Hub's cart page. It tells shoppers that products may not be available immediately when they are redirected to Shopping Hub's cart.

-   **Version 8.0.1 - November 2024**
    -   Introduced new processes in Shopping Hub to enable access to third-party system products, providing shoppers with a wider range of catalog items that can be configured to meet your business needs. This feature includes an out-of-the-box framework that allows you to modify and manage your third-party connections.
        -   Configure cXML and API connections using the configuration framework.
        -   Empower shoppers to search across both third-party and native catalog items within ServiceNow using AI-powered search.
        -   Enable checkout within ServiceNow for a combination of catalog items and third-party system products.
        -   Suppliers differ in the types of connections they offer to customers. For suppliers that do not support Order APIs, a redirection to their third-party system is required before completing checkout in ServiceNow.
        -   For both new and existing customers, no default content is provided with the new feature. Customers must use the third-party framework to establish supplier connections.
    -   Specify default delivery address when logging in to Shopping Hub for the first time.
        -   A default delivery address is required when you log in to Shopping Hub after initial setup to ensure supplier products display correctly in the UI.
        -   Both new and existing customers using Shopping Hub will experience the default behavior with this new feature.
-   **Version 7.0.1 - August 2024**
    -   New: Render end-to-end process visibility in Shopping Hub so that your shoppers have transparency into the procurement process after they submit a request. You can also configure this feature to meet your own business processes. For example, you can use a default content and configuration framework to modify and edit your own content.
    -   -   Configure end-to-end process visibility through a configuration framework that enables administrators to define and modify steps, and the work that is within each step. You can also sequence and change labels to promote flexibility and alignment with your business processes.
-   Provide your shoppers with the following end-to-end visibility on sourcing requests, purchase requisitions, and purchase orders in Shopping Hub:
    -   Progress of the requests and expected completion timelines.
    -   Step dependencies and progress of the sequential and concurrent steps.
    -   Completed, current, and future steps, enabling oversight of the status of the work within steps.
    -   Sequencing of work, such as approvals, cases, and tasks.
    -   Enhanced communication for your shoppers so that they can message task assignees and task assigners directly from within the platform. You can track this communication through audit trails.
    -   Record of your shoppers' page navigation between My Purchases List and Details view pages on Shopping Hub.
    -   If you're an existing customer who is using sourcing requests, purchase requisitions, and purchase orders, you can find the default content in this new user experience. You can use the configuration framework to modify the content to your business processes.
    -   If you're an existing customer who is not using sourcing requests, purchase requisitions, and purchase orders, you won't find the default content in this new user experience. You can use the configuration framework to modify the content to point to your tables and business processes.
    -   If you're a new customer, you can use the configuration framework to modify the content to point to your tables and business processes.
-   **Version 4.0.5 - August 2024 \(Vancouver\)**

    Fixed issues with setting a delivery location in Shopping Hub.

-   **Version 6.0.1 - May 2024**
    -   New:
        -   Shoppers can now navigate to punchout supplier sites and make purchases from external sites. Level 1 cXML-based punchout is now supported.
        -   Shoppers can now view and make single supplier internal bundle purchases from the Shopping Hub application.
-   **Version 5.0.0 - February 2024**

    Changed:

    -   Changed:
        -   Introduced minor content changes within the sourcing checkout for items without pricing in the Shopping Hub product catalog to align with the same intake questions in the off-catalog experience in Employee Center. Existing customers leveraging both Shopping Hub and Employee Center will see an alignment of questions in both experiences.
        -   A requester can now provide the contact details of a supplier that they are interested in working with during intake of catalog items where pricing is needed. A supplier contact record is stored and created for procurement fulfillers to use when reviewing sourcing or purchasing details. Both existing and new customers will see these changes.
        -   Introduced additional user experience analytics for Shopping Hub to track user sessions, page activity, and navigation within My Purchases, to better understand product usage and user experience. Existing and new customers with the user experience plugin will be able to see this event tracking to understand their users' Shopping Hub usage.
        -   Shoppers can now see tasks such as E-sign, Upload a document, and Submit a form in their to-do list in Shopping Hub.
-   **Version 4.0.2 - November 2023**

    New: Introduced User Experience Analytics for Shopping Hub to track user sessions, page activity, and navigation, to better understand product usage and user experience. Note: Existing and new customers with the User Experience plugin will be able to see this event tracking to understand their users' Shopping Hub usage.

-   **Version 3.0.1 - August 2023**
    -   New:
        -   Shoppers can now add attachments as part of the full checkout experience.
        -   Attachments added during quick and full checkouts will now appear in the approval notifications in Shopping Hub, Employee Center, and emails.
-   **Version 2.0.4 - June 2023**

    Fixed: Minor bug fixes.

-   **Version 2.0.3 - May 2023**

    New:

    -   Quick checkout now supports the usage of employee credits. Employees can be assigned one-time credits like Hardware Refresh, and such credits can now be used by employees when doing a quick checkout.
    -   When checking out products or services, employees can now attach supporting documents like emails from supplier or some communication associated with the purchase that is being made.

        **Note:** Existing customers will not be impacted as it is a new functionality which customers can choose to use.

-   **Version 1.0.2 - February 2023**
    -   The new ShoppingHub application enables configurable experiences using the Now Experience UI Builder, providing customers greater flexibility to provide streamlined employee experiences to meet their specific business needs. Customers can:
        -   Customize their portals by adding new filters, badges, rename labels, branding, and so on.
        -   Expose additional fields or hide fields as required, to meet their business needs.
        -   Streamline the quick checkout flow using record producer.
        -   Add pages to provide new experiences.

**Parent Topic:**[ServiceNow Store - Sourcing and Procurement Operations release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-psm-procurement-service-mgmt-landing.md)

