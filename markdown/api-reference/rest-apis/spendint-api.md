---
title: Spendint API
description: The Spendint API provides endpoints that push the catalog, price, availability, order, shipment, and invoice information from a third party to the ServiceNow instance. This API is part of the Source-to-Pay Integration Framework application.Allows suppliers to post multiple catalogs for creating supplier products, model products, contracts, and pricing records.Updates any pricing for supplier product records.Updates the availability for supplier product records.Updates order information for when a user shops for a product from a third-party catalog. When the user checks out, a purchase line is created so that approvals or other tasks for the purchase can be completed.Use this endpoint to accept updates on purchases from third parties.Accepts invoices from third-party providers.
locale: en-US
release: australia
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 32
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# Spendint API

The Spendint API provides endpoints that push the catalog, price, availability, order, shipment, and invoice information from a third party to the ServiceNow instance. This API is part of the Source-to-Pay Integration Framework application.

This API requires the Procurement Integration Framework \(com.glide.sn\_spend\_intg\) store application and is provided within the `sn_spend_intg` namespace. For information, see Procurement File Transfer Framework.

To access this API, you must have the sn\_spend\_intg.procurement\_integrator role.

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## Spendint API - POST /sn\_spend\_intg/spendint/catalog

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

### Third-party mapping

Use the following tables to perform the third-party category, model, and unit mappings:

-   Third-Party Categories: Stores all the third-party category records for the ShoppingHub administrator to map with internal existing model categories.
-   Third-Party Model Mappings: Stores all the mapping information between product models and third-party model categories.
-   Third-Party Units: Stores all the third-party unit records for the ShoppingHub administrator to map with supplier product units.
-   Third-Party Unit Mappings: Stores all the mapping information between product models and third-party units.

**Note:** A third-party integration product is auto-published when both the third-party category and third-party unit are mapped appropriately.

### Supplier product sales dates

A supplier product is discontinued and no longer published in the catalog when it has reached its sales end date. The **Sales start date** and **Sales end date** fields on the Supplier product form are populated through third-party integration from theCatalog API.

### Status tables

To know the status of the bulk product import request, make a REST call into the ServiceNow database using the Table REST API. The response from the API lists the records where the bulk import request failed. For bulk product import response, query the Catalog Error table with the following parameter:

`sysparm_query=outbound_error.supplier_id=<supplier_id>^outbound_error.state=20`

Details on the customer id, supplier id, error type, unique import set id, and state can be found in the Outbound Status table, which is the parent error table.

### URL format

`/api/sn_spend_intg/spendint/catalog`

### Supported request parameters

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
</table>### Headers

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

### Status codes

The following status codes apply to this HTTP action.

|Status code|Description|
|-----------|-----------|
|success|Successful. The request was successfully processed.|
|failure|Unsuccessful. The request was processed with errors.|

### Response body parameters \(JSON\)

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
</table>### cURL request

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

## Spendint API - POST /sn\_spend\_intg/spendint/price

Updates any pricing for supplier product records.

When pricing is available for supplier product records, the API uses the product SKU to find an existing supplier product. If a matching supplier product exists, the corresponding contract price is updated. If no matching supplier product is found, an error message is generated, stating that the product for which you are trying to update pricing for does not exist.

### Status tables

To know the status of the price import request, make a REST call into the ServiceNow database using the Table REST API. The response from the API lists the records where the price import request failed. For a price import response, query the Price Error table with the following parameter:

`sysparm_query=outbound_error.supplier_id=<supplier_id>^outbound_error.state=20`

You can find the details on the customer ID, supplier ID, error type, unique import set ID, and state can in the Outbound Status table, which is the parent error table.

### URL format

`/api/sn_spend_intg/spendint/price`

### Supported request parameters

|Name|Description|
|----|-----------|
|None| |

<table id="table_bdb_dck_ymb" class="rest_api_query_parameters"><thead><tr><th>

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

catalog\_id

</td><td>

Required. Identifier for the catalog content that can be purchased by a customer.Data type: String

 Maximum length: 100

</td></tr><tr><td>

customer\_id

</td><td>

Required. Identifier for the customer.Data type: String

 Maximum length: 100

</td></tr><tr><td>

products

</td><td>

List of objects that define products to create or update. Each transaction has a limit of 1000 products.Data type: Array

 ```
"products": [
  {
    "contract_agreement": {Array},
    "sku": "String"
  }
]
```

</td></tr><tr><td>

products.contract\_agreement

</td><td>

Details of the contract for a product.Data type: Object

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

products.sku

</td><td>

Required. Number that is generated by a supplier that uniquely identifies a product that is sold by that supplier.Data type: String

 Maximum length: 100

</td></tr><tr><td>

supplier\_id

</td><td>

Required. Identifier for the reseller or supplier that the customer can place orders with.Data type: String

 Maximum length: 100

</td></tr><tr><td>

third\_party\_import\_id

</td><td>

Identifier that enables a third party to pass a string value to uniquely identify a set of imported data.Data type: String

 Maximum length: 100

</td></tr></tbody>
</table>### Headers

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

### Status codes

The following status codes apply to this HTTP action.

|Status code|Description|
|-----------|-----------|
|success|Successful. The request was successfully processed.|
|failure|Unsuccessful. The request was processed with errors.|

### Response body parameters \(JSON\)

These response body parameters are received when queried in synchronous mode.

<table id="table_jy2_1hk_ymb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

error\_response\_body

</td><td>

Description of the errors, listed by sku and the error message.Data type: Array

</td></tr><tr><td>

error\_response\_body.error\_message

</td><td>

Detailed error message.Data type: String

</td></tr><tr><td>

status\_code

</td><td>

Response status such as "success" or "failure."Data type: String

</td></tr></tbody>
</table>### cURL request

```
curl "https://instance.service-now.com/api/sn_spend_intg/spendint/price" \
--request POST \
--header "Accept:application/json" \
--user 'username':'password'
{"root": [{
  "customer_id": "ACME CORP",
  "catalog_id": "AB-1234323",
  "supplier_id": "SUP-123456",
  “third_party_import_id”: “DEL789876",
  "products": [
    {
      "sku": "5578874",
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
    “result”: {
        “response”: “success”
    }
}

// Error response:
{
    “result”: {
        “response”: [
            {
                “customer_id”: “ACME CORP”,
                “supplier_id”: “SUP-123456”,
                “third_party_import_id”: “DEL789876",
                “status_code”: “failure”,
                “error_response_body”: [
                    {
                        “sku”: “5578874”,
                        “error_message”: “The product for which you are trying to update pricing does not exist\nField Value empty/Formatting issue Negotiated currency\nField Value empty/Formatting issue Contract start date\nField Value empty/Formatting issue Contract end date\n”
                    }
                ]
            }
        ]
    }
}
```

## Spendint API - POST /sn\_spend\_intg/spendint/availability

Updates the availability for supplier product records.

When supplier product records are available, the API uses the product SKU to find an existing supplier product. If a matching supplier product exists, the corresponding **available\_units** field is updated. If no matching supplier product is found, an error message generates stating that the product for which you are trying to update availability for does not exist.

### Status tables

To know the status of the update availability request, make a REST call into the ServiceNow database using the Table REST API. The response from the API lists the records where the update availability request failed. For update availability response, query the Availability Error table with the following parameter:

`sysparm_query=outbound_error.supplier_id=<supplier_id>^outbound_error.state=20`

The details on the customer ID, supplier ID, error type, unique import set ID, and state can be found in the Outbound Status table, which is the parent error table.

### URL format

`/api/sn_spend_intg/spendint/availability`

### Supported request parameters

|Name|Description|
|----|-----------|
|None| |

<table id="table_rdf_2ck_ymb" class="rest_api_query_parameters"><thead><tr><th>

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

catalog\_id

</td><td>

Required. Identifier for the catalog content that can be purchased by a customer.Data type: String

 Maximum length: 100

</td></tr><tr><td>

customer\_id

</td><td>

Required. Identifier for the customer.Data type: String

 Maximum length: 100

</td></tr><tr><td>

products

</td><td>

List of objects that define the products to update. Each transaction has a limit of 1000 products.Data type: Array

 ```
"products": [
  {
    "available_units": "String",
    "sku": "String",
    "unit": "String"
  }
]
```

</td></tr><tr><td>

products.available\_units

</td><td>

Required for products that are kept in stock. Number of units available for this product.Data type: String

 Maximum length: 40

</td></tr><tr><td>

products.sku

</td><td>

Required. Number that is generated by a supplier that uniquely identifies a product sold by that supplier.Data type: String

 Maximum length: 100

</td></tr><tr><td>

products.unit

</td><td>

Required. Unit or rate at which the product is sold by the supplier. For example, pieces, hours, and so on.Data type: String

 Maximum length: 100

</td></tr><tr><td>

supplier\_id

</td><td>

Identifier for the reseller or supplier that the customer can place orders with.Data type: String

 Maximum length: 100

</td></tr><tr><td>

third\_party\_import\_id

</td><td>

Allows a third-party to pass a string value to uniquely identify a set of imported data.Data type: String

 Maximum length: 100

</td></tr></tbody>
</table>### Headers

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

### Status codes

The following status codes apply to this HTTP action.

|Status code|Description|
|-----------|-----------|
|success|Successful. The request was successfully processed.|
|failure|Unsuccessful. The request was processed with errors.|

### Response body parameters \(JSON\)

These response body parameters are received when queried in synchronous mode.

<table id="table_vsm_1hk_ymb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

error\_response\_body

</td><td>

Description of the errors, listed by sku and the error message.Data type: Array

</td></tr><tr><td>

error\_response\_body.error\_message

</td><td>

Detailed error message.Data type: String

</td></tr><tr><td>

status\_code

</td><td>

Response status such as "success" or "failure."Data type: String

</td></tr></tbody>
</table>### cURL request

```
curl "https://instance.servicenow.com/api/sn_spend_intg/spendint/availability" \
--request POST \
--header "Accept:application/json" \
--user 'username':'password'
{"root": [{
  "customer_id": "AB-1234323",
  "catalog_id": "ACME CORP",
  "supplier_id": "SUP-123456",
  "third_party_import_id": "DEL6789876",
  "products": [
    {
      "sku": "5578874",
      "unit": "Each",
      "available_units": "20"
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

Error response: 
{
    "result": {
        "response": [
            {
                "customer_id": "AB-1234323",
                "supplier_id": "SUP-123456",
                "third_party_import_id": "DEL6789876",
                "status_code": "failure",
                "error_response_body": [
                    {
                        "sku": "5578874",
                        "error_message": "The product for which you are trying to update availability does not exist\nField Value empty/Formatting issue Unit\n"
                    }
                ]
            }
        ]
    }
}
```

## Spendint API - POST /sn\_spend\_intg/spendint/orderack

Updates order information for when a user shops for a product from a third-party catalog. When the user checks out, a purchase line is created so that approvals or other tasks for the purchase can be completed.

When a purchase order is generated in the ServiceNow database, the order is pushed into the following tables:

-   Outbound Order: Contains the order header.
-   Outbound Order Line: Contains the order lines.

Suppliers need to query these tables and fetch the orders that are pending against them. Suppliers should create a scoped app for Workflow Studio actions for integrating with the ServiceNow database.

Query the tables with the following parameters:

-   `sysparm_query=supplier_id=<supplier_id>^purchase_order.status=20 for header`
-   `sysparm_query=purchase_order.supplier_id=<supplier_id>^purchase_order.status=20 for header`

When a purchase line is converted to a purchase order line, the following processes are run:

1.  The purchase order and purchase order line are submitted to the Enterprise Resource Planning \(ERP\), if applicable.
2.  The purchase order and purchase order line are transferred through integration to the third party with the customer ID, supplier ID, purchase order number, order date, purchase order amount, purchase order amount currency, and purchase order lines.
3.  The purchase order and purchase order line remain in the Pending Submission state until confirmation messages are received by both the third-party catalog integration and the ERP. After confirmation is received, the state is updated to Ordered. If there is no ERP integration involved, a confirmation message is required only from the third-party integration.

### Status tables

To know the status of the order acknowledgment request, make a REST call into the ServiceNow database using the Table REST API. The response from the API lists the records where the order acknowledgment request failed. For an order acknowledgment response, query the Order Acknowledgment Error table with the following parameter:

`sysparm_query=outbound_error.supplier_id=<supplier_id>^outbound_error.state=20`

The details on the customer ID, supplier ID, error type, unique import set ID, and state can be found in the Outbound Status table, which is the parent error table.

### URL format

`/api/sn_spend_intg/spendint/orderack`

### Supported request parameters

|Name|Description|
|----|-----------|
|None| |

<table id="table_sd3_lck_ymb" class="rest_api_query_parameters"><thead><tr><th>

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

Required. Identifier for the customer.Data type: String

 Maximum length: 100

</td></tr><tr><td>

order\_number

</td><td>

Required. Purchase order number provided by the customer for this order.Data type: String

 Maximum length: 40

</td></tr><tr><td>

sales\_order\_lines

</td><td>

List of objects that define the sales order lines with unique updates for the purchases in this order.Data type: Array

 ```
"sales_order_lines":[
  {
    "estimated_arrival_date": "String",
    "line_number": "String",
    "sales_order_line_number": "String"
  }
]
```

</td></tr><tr><td>

sales\_order\_lines.estimated\_arrival\_date

</td><td>

Estimated arrival date of the order.Data type: String

 Maximum length: 40

 Format: YYYY-MM-DD

</td></tr><tr><td>

sales\_order\_lines.line\_number

</td><td>

Required. Purchase order line number that was generated by the customer for a particular purchase.Data type: String

 Maximum length: 40

</td></tr><tr><td>

sales\_order\_lines.sales\_order\_line\_number

</td><td>

Sales order line number that was generated by the supplier. This number is required only for revisions to this purchase.Data type: String

 Maximum length: 40

</td></tr><tr><td>

sales\_order\_number

</td><td>

Number or value that is generated by the supplier for this order.Data type: String

 Maximum length: 40

</td></tr><tr><td>

status\_code

</td><td>

Required. Status of the submitted order that confirms if the order was successfully placed.Data type: String

 Valid values:

-   confirmed: Order placed successfully.
-   rejected: Order not placed.

</td></tr><tr><td>

status\_message

</td><td>

Message that is attached to a status code. For example, the message could be that the order was successfully placed and is on back order.Data type: String

 Maximum length: 1000

</td></tr><tr><td>

supplier\_id

</td><td>

Required. Identifier for the reseller or supplier that the customer can place orders with.Data type: String

 Maximum length: 100

</td></tr><tr><td>

third\_party\_import\_id

</td><td>

Identifier that enables a third party to pass a string value to uniquely identify a set of imported data.Data type: String

 Maximum length: 100

</td></tr></tbody>
</table>### Headers

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

### Status codes

The following status codes apply to this HTTP action.

|Status code|Description|
|-----------|-----------|
|success|Successful. The request was successfully processed.|
|failure|Unsuccessful. The request was processed with errors.|

### Response body parameters \(JSON\)

These response body parameters are received when queried in synchronous mode.

<table id="table_dq5_1hk_ymb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

error\_response\_body

</td><td>

Description of the errors, listed by the sales order number, sales order line number, and the error message.Data type: Array

</td></tr><tr><td>

error\_response\_body.error\_message

</td><td>

Detailed error message.Data type: String

</td></tr><tr><td>

status\_code

</td><td>

Response status such as "success" or "failure."Data type: String

</td></tr></tbody>
</table>### cURL request

```
curl "https://instance.service-now.com/api/sn_spend_intg/spendint/orderack" \
--request POST \
--header "Accept:application/json" \
--user 'username':'password'
{"root":[{
  "customer_id": "ACME CORP",
  "supplier_id": "SUP-123456",
  "third_party_import_id": "undefined",
  "order_number": "PO08903323",
  "sales_order_number": "SO03323212",
  "status_code": "CONFIRMED",
  "status_message": "BACKORDERED",
  "sales_order_lines":[
    {
      "line_number": "POL6789876",
      "sales_order_line_number": "SOL5678909",
      "estimated_arrival_date": "YYYY-MM-DD"
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
                "customer_id": "ACME CORP",
                "supplier_id": "SUP-123456",
                "third_party_import_id": "undefined",
                "status_code": "failure",
                "error_response_body": [
                    {
                        "sales_order_number": "SO03323212",
                        "sales_order_line_number": "SOL5678909",
                        "error_message": "Field Value empty/Formatting issue Purchase order number\nField Value empty/Formatting issue Purchase order line number\n"
                    }
                ]
            }
        ]
    }
}
```

## Spendint API - POST /sn\_spend\_intg/spendint/shipment

Use this endpoint to accept updates on purchases from third parties.

When you receive data, you must match the shipment data to a purchase order line by using the sales order line number. You can use the tracking number to find an existing shipment detail record that is related to the purchase order line. If no such record is found, create a new shipment detail record. If no purchase order or purchase order line exists for the shipment data, you see an error message that states that the purchase order for this shipment does not exist.

**Note:** If the purchase order and purchase order lines are in the Pending Submission status, and the sales order and sales order lines are not populated, then the shipment and invoice posting from the third-party reseller is not allowed. It is only allowed when the status of the purchase order and purchase order lines are Ordered. Also, there is no sequential restriction on shipment and invoice posting.

### Status tables

To know the status of the shipping request, make a REST call into the ServiceNow database using the Table REST API. The response from the API lists the records where the shipping update failed. To get a shipping response, query the Shipment Error table with the following parameter:

`sysparm_query=outbound_error.supplier_id=<supplier_id>^outbound_error.state=20`

The details on the customer ID, supplier ID, error type, unique import set ID, and state can be found in the Outbound Status table, which is the parent error table.

### URL format

`/api/sn_spend_intg/spendint/shipment`

### Supported request parameters

|Name|Description|
|----|-----------|
|None| |

<table id="table_igy_fck_ymb" class="rest_api_query_parameters"><thead><tr><th>

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

order\_number

</td><td>

Required. Purchase order number that is provided by the customer for this order.Data type: String

 Maximum length: 40

</td></tr><tr><td>

sales\_order\_number

</td><td>

Required. Number or value that is generated by the supplier for this order.Data type: String

 Maximum length: 40

</td></tr><tr><td>

shipment\_lines

</td><td>

List of shipment lines that can contain the serial number, IMEI number, and asset tag details of the assets.Data type: Array

 ```
"shipment_lines": [
  {
    "actual_shipment_date": "String",
    "estimated_arrival_date": "String",
    "line_number": "String",
    "planned_shipment_date": "String",
    "product_details": [Array],
    "sales_order_line_number": "String",
    "shipping_address": {Object},
    "shipping_carrier": "String",
    "shipment_quantity": "String",
    "ship_to": "String",
    "tracking_number": "String"
  }
]
```

</td></tr><tr><td>

shipment\_lines.actual\_shipment\_date

</td><td>

Date on which the shipment leaves the supplier’s location.Data type: String

 Maximum length: 40

 Format: YYYY-MM-DD

</td></tr><tr><td>

shipment\_lines.estimated\_arrival\_date

</td><td>

Date on which the shipment is expected to arrive at the specified location.Data type: String

 Maximum length: 40

 Format: YYYY-MM-DD

</td></tr><tr><td>

shipment\_lines.line\_number

</td><td>

Required. Purchase order line number that is generated by the customer for a particular purchase.Data type: String

 Maximum length: 40

</td></tr><tr><td>

shipment\_lines.planned\_shipment\_date

</td><td>

Date on which the shipment is planned to leave the supplier’s location.Data type: String

 Maximum length: 40

 Format: YYYY-MM-DD

</td></tr><tr><td>

shipment\_lines.product\_details

</td><td>

List of objects that define the details about the products being shipped. Options include the serial number, IMEI number, and asset tag details.Data type: Array

 ```
"product_details": [
  {
    "asset_tag": "String",
    "imei": "String",
    "serial_number": "String"
  }
]
```

</td></tr><tr><td>

shipment\_lines.product\_details.asset\_tag

</td><td>

Asset tag of the shipped product.Data type: String

 Maximum length: 100

</td></tr><tr><td>

shipment\_lines.product\_details.imei

</td><td>

IMEI number of the shipped product.Data type: String

 Maximum length: 100

</td></tr><tr><td>

shipment\_lines.product\_details.serial\_number

</td><td>

Required. Serial number of the shipped product.Data type: String

 Maximum length: 100

</td></tr><tr><td>

shipment\_lines.sales\_order\_line\_number

</td><td>

Sales order line number that is generated by the supplier. This number is required only for revisions to this purchase.Data type: String

 Maximum length: 40

</td></tr><tr><td>

shipment\_lines.shipping\_address

</td><td>

Address where the products are being shipped to.Data type: Object

 ```
"shipping_address":
  {
    "city": "String",
    "country": "String",
    "name": "String",
    "state": "String",
    "street": "String",
    "zip_code": "String"
  }
```

</td></tr><tr><td>

shipment\_lines.shipping\_address.city

</td><td>

Name of the city where the products are shipped to.Data type: String

 Maximum length: 1000

</td></tr><tr><td>

shipment\_lines.shipping\_address.country

</td><td>

Country where the products are shipped to.Data type: String

 Maximum length: 40

</td></tr><tr><td>

shipment\_lines.shipping\_address.name

</td><td>

Name of the customer that the products are being shipped to.Data type: String

 Maximum length: 1000

</td></tr><tr><td>

shipment\_lines.shipping\_address.state

</td><td>

State where the products are shipped to.Data type: String

 Maximum length: 1000

</td></tr><tr><td>

shipment\_lines.shipping\_address.street

</td><td>

Name of the street where the products are shipped to.Data type: String

 Maximum length: 1000

</td></tr><tr><td>

shipment\_lines.shipping\_address.zip\_code

</td><td>

Zip code or pin code where the products are shipped to.Data type: String

 Maximum length: 40

</td></tr><tr><td>

shipment\_lines.shipment\_quantity

</td><td>

Required. Number of the products being shipped as physical goods. The number should contain the quantity of the products that are in the shipment.Data type: String

 Maximum length: 40

</td></tr><tr><td>

shipment\_lines.shipping\_carrier

</td><td>

Shipping carrier that is delivering the product to the specified location such as FedEx, UPS, USPS, and so on.Data type: String

 Maximum length: 100

</td></tr><tr><td>

shipment\_lines.ship\_to

</td><td>

Name of the recipient that the products are shipped to.Data type: String

 Maximum length: 100

</td></tr><tr><td>

shipment\_lines.tracking\_number

</td><td>

Tracking number that is provided by the shipping carrier for the whole or a portion of the purchase.Data type: String

 Maximum length: 100

</td></tr><tr><td>

supplier\_id

</td><td>

Required. Identifier for the reseller or supplier that the customer can place orders with.Data type: String

 Maximum length: 100

</td></tr><tr><td>

supplier\_shipment\_number

</td><td>

Required. Identification number that is generated for this shipment. Typically, this number is generated by an Enterprise Resource Planning \(ERP\) or order tracking system.Data type: String

 Maximum length: 100

</td></tr><tr><td>

third\_party\_import\_id

</td><td>

Identifier that enables a third party to pass a string value to uniquely identify a set of imported data.Data type: String

 Maximum length: 100

</td></tr></tbody>
</table>### Headers

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

### Status codes

The following status codes apply to this HTTP action.

|Status code|Description|
|-----------|-----------|
|success|Successful. The request was successfully processed.|
|failure|Unsuccessful. The request was processed with errors.|

### Response body parameters \(JSON\)

These response body parameters are received when queried in synchronous mode.

<table id="table_igg_bhk_ymb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

error\_response\_body

</td><td>

Description of the errors, listed by the sales order line number, sales order number, supplier shipment number, and the error message.Data type: Array

</td></tr><tr><td>

error\_response\_body.error\_message

</td><td>

Detailed error message.Data type: String

</td></tr><tr><td>

status\_code

</td><td>

Response status such as "success" or "failure."Data type: String

</td></tr></tbody>
</table>### cURL request

```
curl "https://instance.service-now.com/api/sn_spend_intg/spendint/shipment" \
--request POST \
--header "Accept:application/json" \
--user 'username':'password'
{"root":[{
  "customer_id" : "ACME CORP",
  "supplier_id" : "SUP-123456",
  "third_party_import_id": "DEL2134324",
  "supplier_shipment_number" : "TN-YU67898723",
  "order_number": "PO0001002",
  "sales_order_number": "SO00223002",
  "shipment_lines": [
    {
      "line_number": "POL0001005",
      "sales_order_line_number": "SOL0231325",
      "shipment_quantity": "4",
      "shipping_carrier": "FedEx",
      "tracking_number": "E-901290092",
      "shipping_address":
        {
          "name" : "1640 Camino Del Rio North #202, San Diego,CA",
          "street" : "1640 Camino Del Rio North",
          "city" : "San Diego",
          "state" : "CA",
          "zip_code" : "92108-1512",
          "country" : "US"
        },
      "ship_to": "John doe",
      "planned_shipment_date": "YYYY-MM-DD",
      "actual_shipment_date": "YYYY-MM-DD",
      "estimated_arrival_date": "YYYY-MM-DD",
      "product_details": [
        {
          "serial_number": "FL1234-23242319001",
          "imei": "2134890294",
          "asset_tag": ""
        },{
          "serial_number": "FL1234-23242319110",
          "imei": "245499003",
          "asset_tag": ""
        }
      ]
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
                "customer_id": "ACME CORP",
                "supplier_id": "SUP-123456",
                "third_party_import_id": "DEL2134324",
                "status_code": "failure",
                "error_response_body": [
                    {
                        "sales_order_line_number": "SOL0231325",
                        "sales_order_number": "SO00223002",
                        "supplier_shipment_number": "TN-YU67898723",
                        "error_message": "The purchase order for this shipment does not exist\nThe purchase order line for this shipment does not exist\n"
                    }
                ]
            }
        ]
    }
}
```

## Spendint API - POST /sn\_spend\_intg/spendint/invoice

Accepts invoices from third-party providers.

If the purchase order and purchase order lines are in the Pending Submission status, and the sales order and sales order lines are not populated, then the shipment and invoice posting from the third-party reseller is not allowed. It is only allowed when the status of the purchase order and purchase order lines are Ordered. Also, there is no sequential restriction on shipment and invoice posting.

After an invoice is submitted, the invoice and invoice lines are mapped to a purchase order. On a successful mapping, the state of the invoice is set as follows:

-   Awaiting Delivery: When no receipts exist, the order is partially delivered, or the invoice requires approval.
-   Invoice Confirmed: When the purchase order is delivered and the amount invoiced matches the purchase order total amount.
-   Requires Review: When the purchase order is delivered and the amount invoiced does not match the purchase order total amount.

When a valid invoice is posted for a line item, the same invoice cannot be updated.

If the provided invoice does not have a purchase order number, the invoice is rejected and you see an error message that states that one or more of the provided invoices does not have a purchase order number. If the provided invoice has a purchase order number, but it doesn't match the purchase order or no purchase order exists, you see an error message. The message states that one or more invoices do not have a corresponding purchase order that matches the purchase order number of the invoice. Also, if the amount invoiced sent from the third-party reseller does not match with the invoiced amount, the invoice is rejected.

### Status tables

To know the status of the invoice request, make a REST call into the ServiceNow database using the Table REST API. The response from the API lists the records where the invoice creation failed. For invoice response, query the Invoice Error table with the following parameter:

`sysparm_query=outbound_error.supplier_id=<supplier_id>^outbound_error.state=20`

The details on the customer ID, supplier ID, error type, unique import set ID, and state can be found in the Outbound Status table, which is the parent error table.

### URL format

`/api/sn_spend_intg/spendint/invoice`

### Supported request parameters

|Name|Description|
|----|-----------|
|None| |

<table id="table_jhz_gck_ymb" class="rest_api_query_parameters"><thead><tr><th>

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

currency

</td><td>

Required. Currency for subtotal, tax, and shipping. The subtotal, tax, and shipping should be in the same currency.Data type: String

 Maximum length: 40

</td></tr><tr><td>

customer\_id

</td><td>

Identifier for the customer.Data type: String

 Maximum length: 100

</td></tr><tr><td>

discounts

</td><td>

Discounts that are applied toward the invoice. This is an editable field.Data type: String

 Maximum length: 100

</td></tr><tr><td>

invoice\_date

</td><td>

Required. Date on which the customer was invoiced.Data type: String

 Maximum length: 40

 Format: YYYY-MM-DD

</td></tr><tr><td>

invoice\_lines

</td><td>

List of objects that define the lines that are being invoiced for purchases within this order.Data type: Array

 ```
"invoice_lines": [
  {
    "invoiced_line_amount": "String",
    "invoiced_quantity": "String",
    "line_number": "String",
    "supplier_invoice_line_number": "String",
    "sales_order_line_number": "String"
  }
]
```

</td></tr><tr><td>

invoice\_lines.invoiced\_line\_amount

</td><td>

Required. Total cost, excluding taxes and shipping, that a customer is being invoiced for a given purchase order line.Data type: String

 Maximum length: 40

</td></tr><tr><td>

invoice\_lines.invoiced\_quantity

</td><td>

Required. Quantity of goods or services that a customer is being invoiced for.Data type: String

 Maximum length: 40

</td></tr><tr><td>

invoice\_lines.line\_number

</td><td>

Required. Purchase order line number that is generated by the customer for a particular purchase.Data type: String

 Maximum length: 40

</td></tr><tr><td>

invoice\_lines.sales\_order\_line\_number

</td><td>

Required. Sales order line number that is generated by the supplier.Data type: String

 Maximum length: 40

</td></tr><tr><td>

invoice\_lines.supplier\_invoice\_line\_number

</td><td>

Required. Identification number that is generated by a supplier for this invoice line.Data type: String

 Maximum length: 100

</td></tr><tr><td>

other\_charges

</td><td>

Other additional charges associated to the invoice. This is an editable field.Data type: String

 Maximum length: 100

</td></tr><tr><td>

order\_number

</td><td>

Required. Purchase order number that is provided by the customer for this order.Data type: String

 Maximum length: 40

</td></tr><tr><td>

remit\_to\_address

</td><td>

Required. Location to which a payment is made.Data type: String

 Maximum length: 1000

</td></tr><tr><td>

sales\_order\_number

</td><td>

Required. Number or value that is generated by the supplier for this order.Data type: String

 Maximum length: 40

</td></tr><tr><td>

shipping

</td><td>

Required. Total shipping cost for the entire purchase.Data type: String

 Maximum length: 40

</td></tr><tr><td>

subtotal

</td><td>

Required. Total amount of money to be paid to the supplier excluding tax and shipping charges.Data type: String

 Maximum length: 40

</td></tr><tr><td>

supplier\_id

</td><td>

Required. Identifier for the reseller or supplier that the customer can place orders with.Data type: String

 Maximum length: 100

</td></tr><tr><td>

supplier\_invoice\_number

</td><td>

Required. Identification number that is generated by a supplier for this invoice.Data type: String

 Maximum length: 100

</td></tr><tr><td>

supplier\_tax\_id

</td><td>

Tax identifier that is associated to the third party reseller. This is an editable field.Data type: String

 Maximum length: 100

</td></tr><tr><td>

tax

</td><td>

Required. Total amount of taxes that are billed for the purchase.Data type: String

 Maximum length: 40

</td></tr><tr><td>

tax\_rate

</td><td>

Tax rate percentage that is applied for the order. This is an editable field.Data type: String

 Maximum length: 100

</td></tr><tr><td>

third\_party\_import\_id

</td><td>

Identifier that enables a third party to pass a string value to uniquely identify a set of imported data.Data type: String

 Maximum length: 100

</td></tr><tr><td>

total\_amount\_invoiced

</td><td>

Required. Total amount of money to be paid to the supplier including tax and shipping charges.Data type: String

 Maximum length: 40

</td></tr></tbody>
</table>### Headers

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

### Status codes

The following status codes apply to this HTTP action.

|Status code|Description|
|-----------|-----------|
|success|Successful. The request was successfully processed.|
|failure|Unsuccessful. The request was processed with errors.|

### Response body parameters \(JSON\)

These response body parameters are received when queried in synchronous mode.

<table id="table_jh4_bhk_ymb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

error\_response\_body

</td><td>

Description of the errors, listed by the sales order line number, sales order number, supplier invoice number, supplier invoice line number, and the error message.Data type: Array

</td></tr><tr><td>

error\_response\_body.error\_message

</td><td>

Detailed error message.Data type: String

</td></tr><tr><td>

status\_code

</td><td>

Response status such as "success" or "failure."Data type: String

</td></tr></tbody>
</table>### cURL request

```
curl "https://instance.service-now.com/api/sn_spend_intg/spendint/invoice" \
--request POST \
--header "Accept:application/json" \
--user 'username':'password'
{"root":[{
  "customer_id": "Customer - A",
  "supplier_id": "SUP-123456",
  "third_party_import_id": "undefined",
  "supplier_invoice_number": "QAAP89873220071",
  "supplier_tax_id": "TIN000000",
  "order_number": "POL7987633",
  "sales_order_number": "SO0000000081",
  "invoice_date": "YYYY-MM-DD",
  "subtotal": "6000",
  "tax_rate": "10%",
  "tax": "600",
  "shipping": "120",
  "other_charges": "100",
  "discounts": "200",
  "total_amount_invoiced": "6620",
  "remit_to_address": "1640 Camino Del Rio North #202, San Diego,CA",
  "currency": "USD",
  "invoice_lines": [
    {
      "supplier_invoice_line_number": "QA789A867877ABN32251",
      "line_number": "POL587667",
      "sales_order_line_number": "SOL00000081",
      "invoiced_quantity": "45",
      "invoiced_line_amount": "4000"
    },
    {
      "line_number": "POL587668",
      "supplier_invoice_line_number": "78987323",
      "sales_order_line_number": "SOL98769",
      "invoiced_quantity": "12",
      "invoiced_line_amount": "2000"
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
                "customer_id": "Customer - A",
                "supplier_id": "SUP-123456",
                "third_party_import_id": "undefined",
                "status_code": "failure",
                "error_response_body": [
                    {
                        "sales_order_line_number": "SOL00000081",
                        "sales_order_number": "SO0000000081",
                        "supplier_invoice_number": "QAAP89873220071",
                        "supplier_invoice_line_number": "QA789A867877ABN32251",
                        "error_message": "The invoice do not have a corresponding purchase order which matches the purchase order number of the invoice provided\n"
                    }
                ]
            }
        ]
    }
}
```

