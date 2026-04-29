---
title: Products card
description: The products card displays a list of all products associated with the account, consumer, or contact.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
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
-   Specify a search criteria to view the list of sold products that meet the criteria.
-   Select the ![](../../../reuse/icons/product-icons/open-link-right-outline-24.svg) icon to drill down to the sold product record page.
-   Select the **Run diagnostics** icon to run diagnostics against a sold product.
-   Select the ![](../../../reuse/icons/product-icons/ellipsis-vertical-fill-24.svg) icon and select **Change order** to create a change order record. This creates a customer order record and sets the context \(account, consumer, or contact\) and updates the Order type field to Product, and Order action field to Change.
-   If there are more than 5 sold products, select **View all** to view all the products on the Sold Product page.

You can configure variables such as tables, display fields, and query conditions. See [Configure the products card variables](../task/c360-configure-products-card.md) for details.

## Run diagnostics

Use this option to initiate service tests such as a speed test or connection test against a customer's sold products. Tests must be configured against the sold product's model ID before they appear as available options.

You can run diagnostics from:

-   A specific product: Select the **Run diagnostics** icon on a sold product list item. The available tests configured against that product's model ID are shown.
-   Page level: Select **Run diagnostics** without a product selected. All sold products associated with the current account are listed. The agent selects a product, and the available tests for that product are shown.

After selecting a test and initiating it, a confirmation is shown that the test has been initiated. Once a test is run, the result is created as a record. Refresh the page to view the test results counter updated. Select the test results to view the top 3 three test results sorted by creation date. Select the link to drill down to the record page.

**Parent Topic:**[Telecommunications Customer 360 home page](c360-home-page.md)

