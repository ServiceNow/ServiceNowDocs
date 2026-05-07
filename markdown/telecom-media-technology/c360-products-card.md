---
title: Products card
description: The products card displays a list of all products associated with the account, consumer, or contact.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Home page, Use, Telecommunications Customer 360, Telecommunications, Media, and Technology \(TMT\)]
---

# Products card

The products card displays a list of all products associated with the account, consumer, or contact.

The top 5 active sold products sorted by state and name are displayed. For each sold product, the following details are displayed:

-   Heading: The name of the sold product by default. Configurable to any field from the product data table.
-   Subheading: The product specification category by default. Configurable to any field from the product data table.
-   Count indicators: Shows the count of the following related records associated with the sold product:

    -   Cases
    -   Service problem cases
    -   Incidents
    -   Test results
    Each related record indicator shows the total count. Select a record indicator to view a pop-up dialog box listing showing the top 3 records sorted by created date. Select the link to drill down to the record page.


**Note:** Only top-level sold products are shown in the table. Products with a parent sold product are excluded.

You can do the following:

-   Filter the list of sold products displayed by Location but this can be configured.
-   Specify a search criteria to view the list of sold products that meet the criteria. You can search either by name or product characteristic values.

    **Note:** Search by product characteristic values is available only if the **Enable search on product characteristics** flag is enabled. For more information, see [Configure the products card variables](../task/c360-configure-products-card.md).

-   Select the ![](../../../reuse/icons/product-icons/open-link-right-outline-24.svg) icon to drill down to the sold product record page.
-   Select the **Run diagnostics** icon to run diagnostics against a sold product.
-   If there are more than 5 sold products, select **View all** to view all the products on the Sold Product page. Product actions, including Modify, are also available for each product in the View all list.
-   You can modify the existing configurations, suspend, resume, or disconnect the sold products and their hierarchy. Select the ![](../../../reuse/icons/product-icons/ellipsis-vertical-fill-24.svg) icon and select one of the following actions:

    -   Modify: This opens the page for the selected product. Modify the details as required and select **Update**. This creates a customer order record with the associated line items.
    -   Suspend: Create an order to suspend a sold product and its hierarchy. Specify the **Start date and time**, the **Reason for Suspension**, and select **Suspend**.
    -   Resume: Create an order to resume a sold product and its hierarchy. If a sold product is in an **Inactive** or **Suspended** state, specify the **Start date and time** and select **Resume**.
    -   Disconnect: Disconnect a sold product and its services after fulfillment. Specify the **Start date and time**, the **Reason for disconnection**, and select **Disconnect**.
    **Note:** These actions are available only for customer accounts.

    You can perform these actions for multiple sold products from the View all list. For more details about these actions and the required conditions, see [Customer Life Cycle Management Workflows](https://www.servicenow.com/docs/access?context=customer-life-cycle-management-workflows&version=australia&pubname=australia-customer-service-management&ft:locale=en-US).


## Run diagnostics

Use this option to initiate service tests such as a speed test or connection test against a customer's sold products. Tests must be configured against the sold product's model ID before they appear as available options.

You can run diagnostics from:

-   A specific product: Select the **Run diagnostics** icon on a sold product list item. The available tests configured against that product's model ID are shown.
-   Page level: Select **Run diagnostics** without a product selected. All sold products associated with the current account are listed. The agent selects a product, and the available tests for that product are shown.

After selecting a test and initiating it, a confirmation is shown that the test has been initiated. Once a test is run, the result is created as a record. Refresh the page to view the test results counter updated. Select the test results to view the top 3 three test results sorted by creation date. Select the link to drill down to the record page.

You can configure variables such as tables, display fields, and query conditions. See [Configure the products card variables](../task/c360-configure-products-card.md) for details.

**Parent Topic:**[Telecommunications Customer 360 home page](c360-home-page.md)

**Related topics**  


[Creating pages and page variants](https://www.servicenow.com/docs/access?context=config-csm-ws-create-page-variant&version=australia&pubname=australia-customer-service-management&ft:locale=en-US)

