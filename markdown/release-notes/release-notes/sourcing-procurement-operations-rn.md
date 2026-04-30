---
title: Sourcing and Procurement Operations release notes
description: The ServiceNow Sourcing and Procurement Operations application provides your employees with generative AI through ServiceNow Now Assist in Virtual Agent, to streamline how they can shop for the goods and services that they need at work. Sourcing and Procurement Operations was enhanced and updated in the Xanadu release.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 7
---

# Sourcing and Procurement Operations release notes

The ServiceNow® Sourcing and Procurement Operations application provides your employees with generative AI through ServiceNow® Now Assist in Virtual Agent, to streamline how they can shop for the goods and services that they need at work. Sourcing and Procurement Operations was enhanced and updated in the Xanadu release.

## Sourcing and Procurement Operations highlights for the Xanadu release

-   Summarize procurement records using Now Assist for SPO and use generative AI to perform common tasks via the Now Assist for SPOVirtual Agent.
-   Use AI-powered search across internal and external supplier products, and streamlined checkout for third-party items.
-   Configure conditions for automatic and manual PR merging.
-   Use AI-powered search across internal and external supplier products, and streamlined checkout for third-party items in Shopping Hub.
-   Add users to watchlists for real-time notifications and visibility on sourcing and purchasing processes.
-   Introduce editable fields for purchase requisitions and purchase orders, improving flexibility in managing orders.
-   Develop a standardized approach for calculating supplier response close dates for sourcing requests and negotiation events.
-   Manage a catalog of goods and services that your employees can use to order the items that they need for their jobs.
-   Provide transparency into the procurement process with regular updates.
-   Automate the end-to-end procurement process workflows, from sourcing through requisitioning, to order fulfillment, receipt, and payment.
-   Enable procurement specialists to source, negotiate, procure goods and services for an organization, and work on procurement tasks.

See [Sourcing and Procurement Operations](https://www.servicenow.com/docs/access?context=psm-overview&version=xanadu&pubname=xanadu-source-to-pay-operations&ft:locale=en-US) for more information.

**Important:** Sourcing and Procurement Operations is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Xanadu release

-   **[Now Assist for Sourcing and Procurement Operations \(SPO\)](https://www.servicenow.com/docs/access?context=now-assist-spo&version=xanadu&pubname=xanadu-source-to-pay-operations&ft:locale=en-US)**

    With Now Assist for Sourcing and Procurement Operations \(SPO\), fulfillers can easily summarize procurement-related records, providing real-time progress updates and action items. Available summarization skills include:

    -   Sourcing request summarization
    -   Purchase requisition summarization
    -   Procurement case summarization
    If you're entitled to Source-to-Pay Operations Pro SKU and Sourcing and Procurement Operations Pro SKU, you can install this application.

-   **[Request the generative AI capabilities by using the Now Assist for SPO Virtual Agent](https://www.servicenow.com/docs/access?context=now-assist-spo-va-using&version=xanadu&pubname=xanadu-source-to-pay-operations&ft:locale=en-US)**

    Requesters can leverage contextual generative AI using the Now Assist for SPO Virtual Agent to complete self-service tasks, such as purchasing products or tracking the status of purchase requisitions, sourcing requests, or procurement cases.

-   **[Log in to Shopping Hub for the first time](https://www.servicenow.com/docs/access?context=login-shoppinghub-first-time&version=xanadu&pubname=xanadu-source-to-pay-operations&ft:locale=en-US)**

    Specify a default delivery address when logging in to Shopping Hub for the first time after initial setup to ensure supplier products display correctly.

-   **[Complete sourcing checkout](https://www.servicenow.com/docs/access?context=complete-sourcing-checkout&version=xanadu&pubname=xanadu-source-to-pay-operations&ft:locale=en-US)**

    Add users to the watch list on sourcing requests and purchase requisitions:

    -   Provide visibility into state changes of purchase requisitions and sourcing requests to the users who aren't submitters or business owners.
    -   Configure the number of users allowed to be added to the watch list.
    -   Enable fulfillers to add users to the watch list at any stage of the request life cycle.
    -   Configure notifications to include watch list users regarding updates on the request.
-   **[Edit a purchase requisition line](https://www.servicenow.com/docs/access?context=edit-request&version=xanadu&pubname=xanadu-source-to-pay-operations&ft:locale=en-US)**

    Fulfillers can use the enhanced **Edit a purchase** option to edit the service date, delivery date, delivery address, and quantity on purchase requisition lines and purchase order lines. For more information, see [Edit a purchase order line](https://www.servicenow.com/docs/access?context=edit-purchase-order&version=xanadu&pubname=xanadu-source-to-pay-operations&ft:locale=en-US).

-   **[Purchasing from punchout or third-party suppliers](https://www.servicenow.com/docs/access?context=purch-punchout-third-party-supp&version=xanadu&pubname=xanadu-source-to-pay-operations&ft:locale=en-US)**

    Shoppers can search for all the products, including those from external suppliers, directly within Shopping Hub. The configuration of the Search API, Order API, and Product Details API determines whether shoppers can complete their purchases directly in Shopping Hub or are redirected to external supplier websites. Products from third-party suppliers with configured Order API and Product details API can be viewed, added to cart, and purchased from within Shopping Hub. For suppliers without this configuration, a notification appears, redirecting shoppers to the supplier’s external site to add items to the cart and place the order. The shopper is subsequently redirected to Shopping Hub where they can continue with the checkout process. For more information, see [Configure punchout for third-party site purchases](https://www.servicenow.com/docs/access?context=configure-supplier-punchout&version=xanadu&pubname=xanadu-source-to-pay-operations&ft:locale=en-US).

-   **[Configure punchout for third-party site purchases](https://www.servicenow.com/docs/access?context=configure-supplier-punchout&version=xanadu&pubname=xanadu-source-to-pay-operations&ft:locale=en-US)**

    Set up cXML and API connections through a configuration framework to enable your shoppers to use AI search within Shopping Hub, enabling them to browse both third-party and native catalog items.

-   **[Process visibility](https://www.servicenow.com/docs/access?context=process-visibility&version=xanadu&pubname=xanadu-source-to-pay-operations&ft:locale=en-US)**

    Render end-to-end process visibility in Shopping Hub so that your shoppers have transparency into the procurement process after they submit a request. You can also configure this feature to meet your own business processes. For example, you can use a default content and configuration framework to modify and edit your own content.

    -   Configure end-to-end process visibility through a configuration framework that enables administrators to define and modify steps, and the work that is within each step. You can also sequence and change labels to promote flexibility and alignment with your business processes.
    -   Provide your shoppers with the following end-to-end visibility on sourcing requests, purchase requisitions, and purchase orders in Shopping Hub:
        -   Progress of the requests and expected completion timelines.
        -   Step dependencies and progress of the sequential and concurrent steps.
        -   Completed, current, and future steps, enabling oversight of the status of the work within steps.
        -   Sequencing of work, such as approvals, cases, and tasks.
        -   Enhanced communication for your shoppers so that they can message task assignees and task assigners directly from within the platform. You can track this communication through audit trails.
        -   Record of your shoppers' page navigation between My Purchases List and Details view pages on Shopping Hub.

## Changed in this release

-   **[SPO list page](https://www.servicenow.com/docs/access?context=procurement-specialist-list-page&version=xanadu&pubname=xanadu-source-to-pay-operations&ft:locale=en-US)**

    All playbooks in SPO have been standardized to deliver a consistent look and feel, enhancing the overall user experience.

-   **[Configure conditions for merging purchase requisitions](https://www.servicenow.com/docs/access?context=config-pr-merge&version=xanadu&pubname=xanadu-source-to-pay-operations&ft:locale=en-US)**

    Set the conditions for merging purchase requisitions \(PRs\). Procurement administrators can define which fields must match for PR merges, ensuring flexibility to align with specific business processes.

-   **[Add a sourcing request to a negotiation event](https://www.servicenow.com/docs/access?context=add-a-sourcing-request-to-a-negotiation-event&version=xanadu&pubname=xanadu-source-to-pay-operations&ft:locale=en-US)**

    Introduced a unified logic for calculating supplier response close dates when adding sourcing requests to new or existing negotiation events. This ensures consistency in date calculations, regardless of whether the dates are system-generated or manually defined by procurement fulfillers.

-   **[Sourcing and Procurement Operations integration with third-party sourcing solutions](https://www.servicenow.com/docs/access?context=psm-integration-third-party-sourcing&version=xanadu&pubname=xanadu-source-to-pay-operations&ft:locale=en-US)**

    Enhanced the Source-to-Pay Integration Framework for integrations with third-party sourcing tools. You can now support negotiation-event-based integrations that consist of multiple sourcing requests.

    Enhanced the purchase order cancellation flow when it's updated from the purchase order outbound table.

-   **[Inbound staging tables for Sourcing and Procurement Operations](https://www.servicenow.com/docs/access?context=spo-inbound-staging-tables&version=xanadu&pubname=xanadu-source-to-pay-operations&ft:locale=en-US)**

    Made the following updates related to inbound staging tables:

    -   Introduced the following staging table and transform map:
        -   **Staging table**: Spend Shipment Import inbound \[sn\_spend\_intg\_imp\_shipment\]

        -   **Transform map**: Spend Shipment Import
    -   Transferred attachments from the Enterprise Resource Planning \(ERP\) system staging table to the main Purchase Order table. These attachments are also visible on the purchase order.
-   **[Source-to-Pay integration framework](https://www.servicenow.com/docs/access?context=sap-integration-overview-2&version=xanadu&pubname=xanadu-source-to-pay-operations&ft:locale=en-US)**

    Updated some fields and processes in the Source-to-Pay Integration Framework to build connection points and to work with other ERP systems, including the following fields and processes:

    -   Turned off the buttons to update purchase order when the integration status in the staging table is New or In Process.
    -   Disallowed purchase order lines to be created when purchase orders haven’t been brought in yet from the ERP system. Added a scheduled job to retry adding purchase order lines after a purchase order is created.
    -   Added missing columns and removed some columns in some staging and primary tables such as the outbound receipt, purchasing group primary and staging, cost center staging, and Fx currency tables. Updated the transform map logic for some of these tables to render these columns.
    -   Created the ERP plant address mapping staging table.

## Deprecations

-   SAP ECC and SAP4HANA are deprecated and no longer supported or available for new activation. Source-to-Pay Integration with SAP ECC and SAP S4 HANA provides the latest experience for this functionality.
-   The SPO classic dashboards are now deprecated and no longer supported or available for new activation. The following Next Experience dashboards provide the latest experience for this functionality:
    -   Procurement Buyer Dashboard
    -   Procurement Strategy &amp; Ops Dashboard
    -   Procurement Team Performance Dashboard
    -   Procurement Case Management Dashboard
-   The classic ShoppingHub \[com.snc.sn\_shop\] portal is now deprecated and no longer supported or available for new activation. The new Shopping Hub \[com.snc.sn\_spend\_uib\] portal provides the latest UIB-enabled experience for this functionality.

## Activation information

Install Sourcing and Procurement Operations by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

**Parent Topic:**[Source-to-Pay Operations release notes](source-to-pay-operations-rn-landing.md)

