---
title: Configure punchout for third-party site purchases
description: Set up punchout configuration to allow shoppers or employees to make third-party site purchases​.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/source-to-pay-operations/sourcing-and-procurement-operations/configure-supplier-punchout.html
release: yokohama
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 6
breadcrumb: [Configuring Sourcing and Procurement Operations, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Configure punchout for third-party site purchases

Set up punchout configuration to allow shoppers or employees to make third-party site purchases​.

## Before you begin

Role required: admin or procurement administrator

## Procedure

1.  Navigate to **All** &gt; **ShoppingHub** &gt; **Primary Data** &gt; **Suppliers**.

    You can also navigate to **Sourcing and Purchasing Automation** &gt; **Primary Data** &gt; **Supplier**.

2.  Ensure that the **Punchout** check box is selected for the designated third-party supplier.

    **Note:** This **Punchout** option is only available in the Purchasing view. For more information on adding suppliers, see [Add a supplier](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/source-to-pay-operations/sourcing-and-procurement-operations/create-supplier.md).

3.  Navigate to **All** &gt; **Procurement Integrations** &gt; **Catalog** &gt; **Third-Party Categories**.

4.  Do the following:

    -   Add the required mapping records between SPO's model category and the punchout supplier's product category.
    -   Add the required mapping records between SPO's predefined units and the punchout supplier's units of measure.
    For more information, see [Mapping Product Categories and Units of Measure for seamless checkout in Shopping Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/source-to-pay-operations/sourcing-and-procurement-operations/product-category-mapping-shoppinghub.md)

5.  Navigate to **All** &gt; **Procurement Integrations** &gt; **Setup** &gt; **Third-Party Registration**.

6.  From the **Supplier** list, search for and select a supplier.

7.  Do either or both of the following depending on your implementation requirements.

    -   Select the **cXML punchout support** check box and fill in the fields in the **cXML punchout setup** tab.

        The suppliers that do not have Search API and Order API or do not want to use them can upload catalog index files containing product catalog data. The uploaded data is stored in the Third-party Catalog \(sn\_spend\_intg\_third\_party\_catalog\) table. For more information, see [Add third-party catalog data in an Excel file](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/source-to-pay-operations/sourcing-and-procurement-operations/add-third-party-catalog-spo.md).

        |Field|Description|
        |-----|-----------|
        |Require catalog index file upload?|Option that enables you to upload the catalog index CSV file. For more information, see [Add third-party catalog data in an Excel file](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/source-to-pay-operations/sourcing-and-procurement-operations/add-third-party-catalog-spo.md).|
        |cXML domain|The domain name associated with your organization for the punchout transaction.|
        |cXML identity|A unique identifier used to represent your organization in the punchout transaction.|
        |Third-party cXML - connections|
        |Order request URL|The URL endpoint where the cXML order request is sent to the supplier.|
        |Punchout group|The specific group for which this punchout configuration applies.|
        |Punchout inbound credentials|The credentials that the supplier uses to authenticate when connecting to your system for punchout transactions.|
        |Punchout outbound credentials|The credentials that you use to authenticate when connecting to the supplier system for punchout transactions.|
        |Punchout start URL|The URL used to initiate the punchout session to the supplier system.|

    -   Select the **APIs exchange** check box and fill in the fields in the **APIs configuration** tab.

        This option is designed for punchout suppliers using the Search API, Order API, and Product Details API, enabling shoppers to search for products, place orders, and view product details seamlessly within the Shopping Hub experience.

        |Field|Description|
        |-----|-----------|
        |Access token API|The URL/API used to authenticate and obtain an access token for API requests.|
        |API Key/Client ID|The unique identifier or key provided by the supplier to authenticate API requests.|
        |Order detail API|The endpoint URL for retrieving detailed information about a specific product.|
        |Place order request API|The endpoint URL for placing orders with the supplier.|
        |Product details APO|The endpoint URL for retrieving detailed information about a specific product.|
        |Product search API|The endpoint URL for searching products within the supplier's catalog. For more information, see [Configure extension point for Product search API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/source-to-pay-operations/sourcing-and-procurement-operations/configure-ext-point-punchout.md).|
        |Punchout group|The specific group for which this punchout configuration applies.|

    **Important:** If a supplier uses the Search API for product searches and cXML for order placement, you should select both the **cXML punchout support** and **APIs exchange** check boxes and fill in the required fields in each corresponding section.

8.  Select **Submit**.


## What to do next

When integrating with a punchout supplier, customers are required to provide specific URLs for Order Confirmation and Shipping Confirmation. For more information, see [Providing Order and Shipping Confirmation URLs to Punchout Suppliers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/source-to-pay-operations/sourcing-and-procurement-operations/punchout-urls.md).

-   **[Providing Order and Shipping Confirmation URLs to Punchout Suppliers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/source-to-pay-operations/sourcing-and-procurement-operations/punchout-urls.md)**  
When integrating with a punchout supplier, customers are required to provide specific URLs for Order Confirmation and Shipping Confirmation.
-   **[Configure extension point for Product search API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/source-to-pay-operations/sourcing-and-procurement-operations/configure-ext-point-punchout.md)**  
The sn\_spend\_intg.ThirdPartySystemApiExtension scripted extension point provides the configuration that punchout suppliers can use to ensure that all details about their product, such as product's name, brand, manufacturer, price, availability, SKU, and so on, is displayed in Shopping Hub.
-   **[Mapping Product Categories and Units of Measure for seamless checkout in Shopping Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/source-to-pay-operations/sourcing-and-procurement-operations/product-category-mapping-shoppinghub.md)**  
You can map the product categories and units of measure for third-party products to the corresponding model categories. This ensures that during checkout, Shopping Hub accurately considers and displays the product category for the purchase order lines \(POL\) and purchase requisition lines \(PRL\) based on your predefined mappings.
-   **[Add third-party catalog data in an Excel file](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/source-to-pay-operations/sourcing-and-procurement-operations/add-third-party-catalog-spo.md)**  
You can download and add third-party catalog data in an Excel file template.

**Parent Topic:**[Configuring Sourcing and Procurement Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/source-to-pay-operations/sourcing-and-procurement-operations/configuring-spo.md)

**Related topics**  


[Install Sourcing and Procurement Operations]()

[Setting up primary data for ShoppingHub]()

[Customize your top suppliers on Shopping Hub]()

[Configure conditions for merging purchase requisitions]()

[Service portal configuration for ShoppingHub]()

[Install ShoppingHub Mobile]()

[Advanced Work Assignment for Source-to-Pay Operations]()

[Install Sourcing and Procurement Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/source-to-pay-operations/sourcing-and-procurement-operations/activate-finance-spend-central.md)

[Application plugin installation sequence in Sourcing and Procurement Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/source-to-pay-operations/sourcing-and-procurement-operations/application-plugin-list.md)

[Setting up primary data for ShoppingHub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/source-to-pay-operations/sourcing-and-procurement-operations/set-up-master-data-shopping-hub.md)

[Service portal configuration for ShoppingHub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/source-to-pay-operations/sourcing-and-procurement-operations/service-portal-configuration-for-shoppinghub.md)

[Customize your top suppliers on Shopping Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/source-to-pay-operations/sourcing-and-procurement-operations/customize-top-suppliers.md)

[Using Shopping Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/source-to-pay-operations/sourcing-and-procurement-operations/use-shoppinghub-portal.md)

[My purchases on Shopping Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/source-to-pay-operations/my-purchases.md)

