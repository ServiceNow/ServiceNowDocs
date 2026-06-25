---
title: Configure punchout for third-party site purchases
description: Set up punchout configuration to allow shoppers or employees to make third-party site purchases​.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/sourcing-and-procurement-operations/configure-supplier-punchout.html
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 9
breadcrumb: [Configure, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Configure punchout for third-party site purchases

Set up punchout configuration to allow shoppers or employees to make third-party site purchases​.

## Before you begin

Role required: sn\_shop.procurement\_administrator

## Procedure

1.  Navigate to **All** &gt; **ShoppingHub** &gt; **Primary Data** &gt; **Suppliers**.

    You can also navigate to **Sourcing and Purchasing Automation** &gt; **Primary Data** &gt; **Supplier**.

2.  Ensure that the **Punchout** check box is selected for the designated third-party supplier.

    \[Omitted image "spo-configure-punchout-supplier.png"\] Alt text: Punchout check box is selected for the designated third-party supplier in the Purchasing view.

    **Note:** This **Punchout** option is only available in the Purchasing view. For more information on adding suppliers, see [Add a supplier](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/create-supplier.md).

3.  Navigate to **All** &gt; **Procurement Integrations** &gt; **Catalog** &gt; **Third-Party Categories**.

4.  Do the following:

    -   Add the required mapping records between SPO's model category and the punchout supplier's product category.
    -   Add the required mapping records between SPO's predefined units and the punchout supplier's units of measure.
    For more information, see [Mapping Product Categories and Units of Measure for seamless checkout in Shopping Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/product-category-mapping-shoppinghub.md)

5.  Navigate to **All** &gt; **Procurement Integrations** &gt; **Setup** &gt; **Third-Party Registration**.

6.  From the **Supplier** list, search for and select a supplier.

7.  Do either or both of the following depending on your implementation requirements.

    -   Select the **cXML punchout support** check box and fill in the fields in the **cXML punchout setup** tab.

        \[Omitted image "spo-configure-punchout-cxml-settings.png"\] Alt text: Entering cXML settings in the cXML punchout setup tab.

        The suppliers that do not have Search API and Order API or do not want to use them can upload catalog index files containing product catalog data. The uploaded data is stored in the Third-party Catalog \(sn\_spend\_intg\_third\_party\_catalog\) table. For more information, see [Add third-party catalog data in an Excel file](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/add-third-party-catalog-spo.md).

<table id="table_pdz_njg_xcc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Require catalog index file upload?

</td><td>

Option that enables you to upload the catalog index CSV file. For more information, see [Add third-party catalog data in an Excel file](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/add-third-party-catalog-spo.md).

</td></tr><tr><td>

cXML domain

</td><td>

The domain name associated with your organization for the punchout transaction.

</td></tr><tr><td>

cXML identity

</td><td>

A unique identifier used to represent your organization in the punchout transaction.

</td></tr><tr><td class="sub-head" colspan="2">

Third-party cXML - connections

</td></tr><tr><td>

Order request URL

</td><td>

The URL endpoint where the cXML order request is sent to the supplier.

</td></tr><tr><td>

Punchout group

</td><td>

The specific group for which this punchout configuration applies.

</td></tr><tr><td>

Punchout inbound credentials

</td><td>

The credentials that SPO uses to validate incoming cXML payloads from the supplier for Order Confirmation and Shipping Confirmation. Select a credential record of type **Basic Auth**. **Important:** Although the credential type is labelled **Basic Auth** in the UI, the fields carry cXML-specific values used to validate incoming supplier payloads:

-   **Username**: Enter the value that the supplier places in `<Header><To><Credential><Identity>` of its confirmation cXML payload. This must match exactly — SPO validates this value against the incoming `<To>` Identity.
-   **Password**: Enter the Shared Secret that the supplier places in `<Header><Sender><Credential><SharedSecret>` of its confirmation cXML payload. SPO decrypts and validates this value against the incoming payload.
Inbound credentials are required for Order Confirmation and Shipping Confirmation flows. If the inbound credential record is missing or invalid, SPO returns a validation error when the supplier sends a confirmation payload. Configure these credentials before going live with a cXML punchout supplier that sends order or shipping confirmations.

</td></tr><tr><td>

Punchout outbound credentials

</td><td>

The credentials that SPO uses to authenticate when sending cXML requests to the supplier system. Select a credential record of type **Basic Auth**. **Important:** Although the credential type is labelled **Basic Auth** in the UI, it does not function as standard HTTP Basic Authentication for punchout. The two fields in the credential record carry cXML-specific values:

-   **Username**: Enter the Sender Identity that identifies your organization in the punchout transaction. This value is written verbatim into both `<From><Credential><Identity>` and `<Sender><Credential><Identity>` in the cXML payload. If left blank, an empty `<Identity/>` element is transmitted.
-   **Password**: Enter the Shared Secret provided by the supplier for authentication. This value maps to `<Sender><Credential><SharedSecret>` in the cXML payload.
The **cXML identity** and **cXML domain** fields on this form identify the supplier's `<To>` side of the cXML transaction and are separate from the outbound credential fields described above.

</td></tr><tr><td>

Punchout start URL

</td><td>

The URL used to initiate the punchout session to the supplier system.

</td></tr></tbody>
</table>    -   Select the **APIs exchange** check box and fill in the fields in the **APIs configuration** tab.

        This option is designed for punchout suppliers using the Search API, Order API, and Product Details API, enabling shoppers to search for products, place orders, and view product details seamlessly within the Shopping Hub experience.

        |Field|Description|
        |-----|-----------|
        |Access token API|The URL/API used to authenticate and obtain an access token for API requests.|
        |API Key/Client ID|The unique identifier or key provided by the supplier to authenticate API requests.|
        |Order detail API|The endpoint URL for retrieving detailed information about a specific product.|
        |Place order request API|The endpoint URL for placing orders with the supplier.|
        |Product details API|The endpoint URL for retrieving detailed information about a specific product.|
        |Product search API|The endpoint URL for searching products within the supplier's catalog. For more information, see [Configure extension point for Product search API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/configure-ext-point-punchout.md).|
        |Punchout group|The specific group for which this punchout configuration applies.|

    **Important:** If a supplier uses the Search API for product searches and cXML for order placement, you should select both the **cXML punchout support** and **APIs exchange** check boxes and fill in the required fields in each corresponding section.

8.  Select **Submit**.


## What to do next

When integrating with a punchout supplier, customers are required to provide specific URLs for Order Confirmation and Shipping Confirmation. For more information, see [Providing Order and Shipping Confirmation URLs to Punchout Suppliers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/punchout-urls.md).

-   **[Providing Order and Shipping Confirmation URLs to Punchout Suppliers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/punchout-urls.md)**  
When integrating with a punchout supplier, customers are required to provide specific URLs for Order Confirmation and Shipping Confirmation.
-   **[Configure extension point for Product search API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/configure-ext-point-punchout.md)**  
The sn\_spend\_intg.ThirdPartySystemApiExtension scripted extension point provides the configuration that punchout suppliers can use to ensure that all details about their product, such as product's name, brand, manufacturer, price, availability, SKU, and so on, is displayed in Shopping Hub.
-   **[Mapping Product Categories and Units of Measure for seamless checkout in Shopping Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/product-category-mapping-shoppinghub.md)**  
You can map the product categories and units of measure for third-party products to the corresponding model categories. This ensures that during checkout, Shopping Hub accurately considers and displays the product category for the purchase order lines \(POL\) and purchase requisition lines \(PRL\) based on your predefined mappings.
-   **[Add third-party catalog data in an Excel file](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/add-third-party-catalog-spo.md)**  
You can download and add third-party catalog data in an Excel file template.

**Parent Topic:**[Configure Sourcing and Procurement Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/configuring-spo.md)

**Related topics**  


[Install Sourcing and Procurement Operations]()

[Setting up primary data for ShoppingHub]()

[Configuring work prioritization]()

[Add a button in Shopping Hub]()

[Customize your top suppliers on Shopping Hub]()

[Configure conditions for merging purchase requisitions]()

[Service portal configuration for ShoppingHub]()

[Install ShoppingHub Mobile]()

[Advanced Work Assignment for Source-to-Pay Operations]()

[Install Universal Request for Sourcing and Procurement Operations]()

[Install Sourcing and Procurement Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/activate-finance-spend-central.md)

[Application plugin installation sequence in Sourcing and Procurement Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/application-plugin-list.md)

[Setting up primary data for ShoppingHub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/set-up-master-data-shopping-hub.md)

[Service portal configuration for ShoppingHub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/service-portal-configuration-for-shoppinghub.md)

[Customize your top suppliers on Shopping Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/customize-top-suppliers.md)

[Using Shopping Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/use-shoppinghub-portal.md)

[My purchases on Shopping Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/my-purchases.md)

