---
title: Spendint API - POST /sn\_spend\_intg/spendint/catalog
description: Allows suppliers to post multiple catalogs for creating supplier products, model products, contracts, and pricing records.
locale: en-US
release: xanadu
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 9
breadcrumb: [Spendint API, Integrating Sourcing and Procurement Operations with other applications, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Spendint API - POST /sn\_spend\_intg/spendint/catalog

Allows suppliers to post multiple catalogs for creating supplier products, model products, contracts, and pricing records.

In the catalog API integration, when you receive data from a third-party catalog, you can:

1.  Create any new third-party categories and map these categories to model categories.
    -   If available, use the United Nations Standard Products and Services Code \(UNSPSC\) and then the category name.
    -   If UNSPSC is not available, use just the category name.
2.  After you map a third-party category to a model category, use the Manufacturer Part Number \(MPN\) to find an existing product model, if one is available.
    1.  If a product model is found for the MPN, update the product model with any changes, and then create or update any supplier products that are related to the product model.
    2.  If a product model does not exist for the MPN, do the following:
        1.  A product model class is usually available on the model category that is referenced by the third-party category for the product. Use this product model class to get the product model table in which the product model should be created, for example, hardware, software, consumable, and so on. If no product model class is available, create the product model in the base product model table.
        2.  After the correct product model class is identified, create a new product model in the correct class as follows:
            -   Manufacturer, publisher, or provider should map to the manufacturer on the product model.
            -   Product name from the API should map to the name on the product model.
            -   MPN from the API should update the model number.
            -   Product description from the API should update the description on the product model.
            -   Model category should be updated with the product category referenced on the third-party category record.
            -   Product category should be updated with the product category referenced on the third-party category record.
            -   If there are values in the substitute products in the API, create the substitute product records between the current product model and the other product models.
            -   If there are values in the compatible products in the API, create the compatible product records between the current product model and the other product models.
            -   Product attributes from the API should be created or updated in the product attribute related list for the product model.
3.  If a product model is available, use the supplier part number to create or update the supplier products that are related to the product model.

## Third-party mapping

Use the following tables to perform the third-party category, model, and unit mappings:

-   Third-Party Categories: Stores all the third-party category records for the Shopping Hub administrator to map with internal existing model categories.
-   Third-Party Model Mappings: Stores all the mapping information between product models and third-party model categories.
-   Third-Party Units: Stores all the third-party unit records for the Shopping Hub administrator to map with supplier product units.
-   Third-Party Unit Mappings: Stores all the mapping information between product models and third-party units.

**Note:** A third-party integration product is auto-published when both the third-party category and third-party unit are mapped appropriately.

## Supplier product sales dates

A supplier product is discontinued and no longer published in the catalog when it has reached its sales end date. The **Sales start date** and **Sales end date** fields on the Supplier product form are populated through third-party integration from theCatalog API.

## Status tables

To know the status of the bulk product import request, make a REST call into the ServiceNow database using the Table REST API. The response from the API lists the records where the bulk import request failed. For bulk product import response, query the Catalog Error table with the following parameter:

`sysparm_query=outbound_error.supplier_id=<supplier_id>^outbound_error.state=20`

Details on the customer id, supplier id, error type, unique import set id, and state can be found in the Outbound Status table, which is the parent error table.

## URL format

`/api/sn_spend_intg/spendint/catalog`

## Supported request parameters

|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

mode

</td><td>

Support for asynchronous and synchronous modes for third-party integration.Data type: String

 Valid values:

-   async: Asynchronous mode.
-   sync: Synchronous mode.

 Default: async

</td></tr></tbody>
</table><table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

customer\_id

</td><td>

Identifier for the customer.Data type: String

 Maximum length: 100

</td></tr><tr><td>

catalog\_id

</td><td>

Identifier for the catalog content that can be purchased by a customer.Data type: String

 Maximum length: 100

</td></tr><tr><td>

products

</td><td>

List of objects that define products to create or update. Each transaction has a limit of 1000 products.Data type: Array

 ```
"products": [
  {
    "available_units": "String",
    "available_for_country": [Array],
    "bundled_components": [Array],
    "contract_agreement": {Object},
    "delivery_time": "String",
    "images": [Array],
    "manufacturer": "String",
    "mpn": "String",
    "parent_bundle": "String",
    "product_attributes": {Object},
    "product_category_name": "String",
    "product_description": "String",
    "product_name": "String",
    "sku": "String",
    "unit": "String",
    "unspsc": "String",
  }
]
```

</td></tr><tr><td>

products.available\_units

</td><td>

Required for products that are kept in stock. This value indicates the quantity of units that are available for this product.Data type: String

 Maximum length: 40

</td></tr><tr><td>

products.available\_for\_country

</td><td>

List of country codes where the supplier product can be purchased. If no country is provided, a user from any country can purchase the product.Data type: Array

 ```
"available_for_country": ["US","IN","GB"]
```

</td></tr><tr><td>

products.bundled\_components

</td><td>

Valid only for scenarios when sending a product bundle as part of the catalog payload, and applicable only for the parent bundle payloads. This value contains the reference to the child bundle components. The list of the MPN and quantities for the child bundle components are maintained here.**Note:** Since the same child bundle component can be added more than once within a bundle, the entered quantity is the differentiator between the same children bundle components.

The child bundle components and their details \(MPN and quantities\) should be mapped to the same supplier.Data type: Array

 ```
"bundled_components": [
  {
    "mpn": "String",
    "quantity": "String"
  }
]
```

</td></tr><tr><td>

products.contract\_agreement

</td><td>

Details of the contract for a product.**Note:** This is not required for child bundle components.

 Data type: Object

 ```
"contract_agreement": {
  "contract_end_date": "String",
  "contract_number": "String",
  "contract_start_date": "String",
  "negotiated_currency ": "String",
  "negotiated_price": "String"
}
```

</td></tr><tr><td>

products.contract\_agreement.contract\_end\_date

</td><td>

Date on which the contract term ends.Data type: String

 Maximum length: 40

 Format: YYYY-MM-DD

</td></tr><tr><td>

products.contract\_agreement.contract\_number

</td><td>

Required. Number of the active contract that is associated with the product.Data type: String

 Maximum length: 100

</td></tr><tr><td>

products.contract\_agreement.contract\_start\_date

</td><td>

Date on which the contract term starts.Data type: String

 Maximum length: 40

 Format: YYYY-MM-DD

</td></tr><tr><td>

products.contract\_agreement.negotiated\_currency

</td><td>

Required. Currency of the negotiated price.Data type: String

 Maximum length: 40

</td></tr><tr><td>

products.contract\_agreement.negotiated\_price

</td><td>

Required. Unit price of a product as negotiated through a contract with the supplier or reseller.Data type: String

 Maximum length: 40

</td></tr><tr><td>

products.delivery\_time

</td><td>

Estimated number of days it takes to ship a product to the customer. This value must represent the number of days and be a whole integer.Data type: String

 Maximum length: 40

</td></tr><tr><td>

products.images

</td><td>

List of strings that specify the image URLs for the supplier product.Data type: Array

</td></tr><tr><td>

products.manufacturer

</td><td>

Required. Company that manufactures, publishes, or provides the product. This is not the supplier or reseller of the product.Data type: String

 Maximum length: 100

</td></tr><tr><td>

products.mpn

</td><td>

Required. Identifier for a product that is provided by the manufacturer, publisher, or provider.**Note:** This is not required for reseller parent bundles if the SKU value is available.

 Data type: String

 Maximum length: 100

</td></tr><tr><td>

products.parent\_bundle

</td><td>

Valid only for scenarios when sending a product bundle as part of the catalog payload, and applicable only for the child bundle component payloads. In the case of a child bundle component, the reference to the parent is maintained here. The parent MPN and SKU values are also set here.Data type: String

 Maximum length: 100

</td></tr><tr><td>

products.product\_attributes

</td><td>

List of key-value pairs that define product attributes, for example, `"Color": "Space Grey"`. Multiple attributes for a product are allowed. However, only those attributes that impact pricing or stock availability should be provided through the API.Data type: Object

</td></tr><tr><td>

products.product\_category\_name

</td><td>

Required. Name that you enter if you are not setting the **unspsc** property. This name is the category to which a product belongs. This category name can be used in a commerce scenario to shop for the product. For example, a power strip product could belong to an Office Equipment category.Data type: String

 Maximum length: 100

</td></tr><tr><td>

products.product\_description

</td><td>

Full description of the product that appears to a shopper within a commerce experience.**Note:** It is recommended that the supplier be as descriptive as possible here, especially for product bundle catalog items where there are child bundle components.

 Data type: String

 Maximum length: 65000

</td></tr><tr><td>

products.product\_name

</td><td>

Required. Name of the product.Data type: String

 Maximum length: 1000

</td></tr><tr><td>

products.sku

</td><td>

Required. Number that is generated by a supplier that uniquely identifies a product that is sold by that supplier.Data type: String

 Maximum length: 100

</td></tr><tr><td>

products.unit

</td><td>

Required. Unit or rate at which the product is sold by the supplier. For example, pieces, hours, and so on.Data type: String

 Maximum length: 40

</td></tr><tr><td>

products.unspsc

</td><td>

Required. Identifier that you enter if you are not setting the **product\_category\_name** property. This identifier is the UNSPSC for the category to which a product belongs. For example, UNSPSC code 43210000 is the identifier for the product category Computers.Data type: String

 Maximum length: 100

</td></tr><tr><td>

supplier\_id

</td><td>

Required. Identifier for the reseller or supplier with whom the customer can place orders.Data type: String

 Maximum length: 100

</td></tr><tr><td>

third\_party\_import\_id

</td><td>

Identifier that enables a third party to pass a string value to uniquely identify a set of imported data.Data type: String

 Maximum length: 100

</td></tr></tbody>
</table>## Headers

The following request and response headers apply to this HTTP action only or apply to this action in a distinct way.

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-entry-RESTAPI">

Data format of the response body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr></tbody>
</table>**Note:** Only the **application/json** data format is supported for Procurement Integration Framework.

|Header|Description|
|------|-----------|
|None| |

## Status codes

The following status codes apply to this HTTP action.

|Status code|Description|
|-----------|-----------|
|success|Successful. The request was successfully processed.|
|failure|Unsuccessful. The request was processed with errors.|

## Response body parameters \(JSON\)

These response body parameters are received when queried in synchronous mode.

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

error\_response\_body

</td><td>

Description of the errors, listed by sku, mpn, and the error message.Data type: Array

</td></tr><tr><td>

error\_response\_body.error\_message

</td><td>

Detailed error message.Data type: String

</td></tr><tr><td>

status\_code

</td><td>

Response status such as "success" or "failure."Data type: String

</td></tr></tbody>
</table>## cURL request

```
curl "https://instance.service-now.com/api/sn_spend_intg/spendint/catalog" \
--request POST \
--header "Accept:application/json" \
--user 'username':'password'
{"root": [{
  "customer_id": "AB-1234323",
  "catalog_id": "ACME CORP-12347898",
  "supplier_id": "SUP-123456",
  "third_party_import_id": "DELL1234567",
  "products": [
    {
      "product_name": "Apple MacBook Pro 13 Core i7",
      "mpn": "Z0WQ-20004301931",
      "sku": "55788741",
      "manufacturer": "Apple",
      "product_category_name": "Computer",
      "parent_bundle": "920-0045362002",
      "bundled_components": {
        "mpn": "Z0WQ-20004301931",
        "quantity": "4",
       },
      "unspsc": "43211500",
      "product_description": "Apple MacBook Pro 13 Core i7 2.8GHz 16GB 512GB - Touch Bar - Space Gray",
      "product_attributes": {
        "Color": "Space Grey",
        "RAM": "16GB",
        "Screen Size": "13inch"
      },
      "images": ["http://test123.image1.png", "http://test123.image2.jpeg"],
      "unit": "Each",
      "available_units": "4",
      "available_for_country": ["US","IN","GB"],
      "delivery_time": "4",
      "contract_agreement": {
        "contract_number": "34567892",
        "contract_start_date": "YYYY-MM-DD",
        "contract_end_date": "YYYY-MM-DD",
        "negotiated_price": "456",
        "negotiated_currency ": "USD"
      }
    }
  ]
}
]}

```

Possible responses:

```
// Success response:
{
    "result": {
        "response": "success"
    }
}

// Error response:
{
    "result": {
        "response": [
            {
                "customer_id": "AB-1234323",
                "supplier_id": "SUP-123456",
                "third_party_import_id": "DELL1234567",
                "status_code": "failure",
                "error_response_body": [
                    {
                        "sku": "55788741",
                        "mpn": "Z0WQ-20004301931",
                        "error_message": "Field Value empty/Formatting issue Negotiated currency \n"
                    }
                ]
            }
        ]
    }
}
```

**Parent Topic:**[Spendint API](../concept/spendint-api.md)

