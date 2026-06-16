---
title: Customer Life Cycle Management Workflows release notes
description: Version history for the Customer Life Cycle Management Workflows application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-csm-customer-lifecycle-mgmt-workflows.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 3
breadcrumb: [ServiceNow Store - Customer Service Management release notes, ServiceNow Store release notes]
---

# Customer Life Cycle Management Workflows release notes

Version history for the Customer Life Cycle Management Workflows application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 5.4.0 - June 2026**
    -   New: Enhanced the agent workspace with a hierarchical view for Sold Products and Product Inventory, making it easier to navigate and manage complex product relationships in configurable workspaces.
    -   Changed: Refined the Modify action for Sold Products to ensure only root-level records can be modified. The option is automatically hidden or disabled for child records across all views, preventing unintended modifications to dependent records.
    -   Fixed: Fixed defects in order fulfillment flows.
-   **Version 5.3.30 - May 2026**
    -   Changed:
        -   Resolved defects within the sales order management processes, related to ramps and split use cases.
        -   The sold product state is now determined based on the start and end dates if populated in change order fulfillment.
        -   Handled line actions and line types in renewal reconfiguration for swap use cases and amend use cases
-   **Version 5.3.0 - April 2026**
    -   Changed:
        -   Minor Enhancements in the following use-cases:
            -   Order and quote renewal reconfiguration
            -   Split scenarios for ramps.
-   **Version 5.2.0 - March 2026**
    -   Changed:
        -   Sold Product states now align with the subscription start date, ensuring accurate lifecycle management. WhenStart Date andEnd Date are populated on the Order Line Item and the Start Date is in the future, the Sold Product is created in theIn-Preparation state; if today or in the past, it is created in theActive state.
        -   Minor enhancements.
-   **Version 5.1.2 - January 2026**

    Changed: Minor defect fix.

-   **Version 5.1.1 - December 2025**

    Changed: Minor enhancements.

-   **Version 4.3.0 - August 2025**

    New:

    -   Improved mappings to support Delta pricing in the MACD Flows.
        -   Added Sold Product Adjustment table entity mappings to the MACD Flows.
    Changed:

    -   Expanded support for the following columns in the Order to SP and Quote to SP MACD Flows.
        -   -   Unit base price
-   Unit list price
-   Sales agreement line
    Fixes: Fixed minor bugs.

-   **Version 2.3.0 - August 2025**

    Fixed: Minor fixes and improvements.

-   **Version 4.2.0 - May 2025**

    Minor fixes and improvements.

-   **Version 2.2.0 - May 2025**

    Minor fixes and improvements.

-   **Version 4.0.0 - February 2025**
    -   Create a Modify, Suspend, Resume, and Disconnect order for single or multiple root product inventory records that are associated with a service specification.
    -   Select multiple root product inventories to perform the Modify action to create both orders and quotes.
    -   Track the status of the Modify, Suspend, Resume, and Disconnect flows on sold products and product inventory record by using the Sales and Order Management Request Tracker \(sn\_tmt\_core\_inbound\_queue\) table.
    -   The Specification class field on the Product Inventory related list provides information on whether the selected product inventory record has a product specification or service specification that is associated with it.
-   **Version 2.0.0 - November 2024**
    -   MACD on Product Inventory records
        -   Perform Modify, Suspend, Resume, and Disconnect actions on product inventory records from the Product Inventories related list.
            -   Note: If you're using the Washington or Xanadu releases, you can manually add the Product Inventories related list. If you wish to retain both the Product Inventories and Sold Products related lists, you can filter out the product inventory records from the Sold Products list and then use the Product Inventories related list to perform MACD actions. The Product Inventories related list will be available out of the box starting with the Yokohama release.
        -   Enable quote or order generation with the Modify action on product inventory records.
        -   Enable the multi-selection of product inventory records to perform the Suspend, Resume, and Disconnect actions.
-   **Version 1.3.1 - August 2024**
    -   New: MACD flows can be performed on sold products that have a specification associated with it. Upgrade to Xanadu to enable MACD flows for configuring sold products with specifications.
    -   Changed: Users can now select multiple sold products at the same time to trigger the Suspend, Resume, and Disconnect flows.
-   **Version 1.2.1 - May 2024**
    -   New: Enable the creation of quotes through the sold product 'modify' flow.
    -   Changed: Sold product modify flow only resulted in order modifications in the version 1 release. Starting from version 2, the modify flow can result in a quote or an order, depending on the result of the decision table "Sold Product Modify Flow Policy".
    -   Fixed: Performance enhancements in Order to Sold product flows.
-   **Version 1.0.0 - February 2024**

    Provides workflows to manage the life cycle of sold products by updating their configurations and to suspend, resume, and disconnect the sold product to meet customer's business needs.


**Parent Topic:**[ServiceNow Store - Customer Service Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-csm.md)

