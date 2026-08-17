---
title: Product Catalog Search API
description: The Product Catalog Search API searches the product catalog and retrieves the eligible catalog-category hierarchy for a given context. Search supports multiple catalog types, with paginated and sortable results.Searches the product catalog and returns a paginated list of products that match the supplied search parameters.Retrieves the product catalog-category hierarchy filtered by eligibility rules. Resolves the input header context request object \(currency, pricelist, address, etc.\), and applies eligibility encoded queries to filter out ineligible catalogs/categories to construct the tree.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/api-reference/rest-apis/product-catalog-search-api.html
release: australia
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2026-06-26"
reading_time_minutes: 21
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# Product Catalog Search API

The Product Catalog Search API searches the product catalog and retrieves the eligible catalog-category hierarchy for a given context. Search supports multiple catalog types, with paginated and sortable results.

The Product Catalog Search API provides the ability to:

-   Search products by search term across one or all catalogs and across one or all categories within a catalog.
-   Retrieve the eligible catalog-category hierarchy for a context, with ineligible catalogs and categories filtered out.
-   Filter results by catalog, category, and catalog type \(defaults to Product Offering\).
-   Supply a header context object to apply account-specific pricing, price lists, currency, channel, shipping/billing address, and sales agreement to search results.
-   Page through result sets using a zero-based page index and page limit.
-   Control sort order and sort field \(for example, by relevance score\).
-   Optionally pass an AI Search suggestion ID to support AI-assisted search flows.

This API delegates all data retrieval to the existing script include, ensuring consistent behavior between the UI and the REST interface. Endpoints are independent and can be called individually. There is no required call order and no dependency on other APIs.

The REST API wraps the JavaScript API [CatalogSearchAPI - Scoped, Global](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/CatalogSearchAPI-scoped_global.md).

## Requirements

This API is included in the Product Catalog Management Core application, which is available on the ServiceNow Store.

This API is provided within the `sn_prd_pm` namespace and requires the Product Catalog Management Core plugin \(sn\_prd\_pm\) to access it.

The calling user must have the sn\_prd\_pm.product\_catalog\_viewer or sn\_prd\_pm.external\_product\_viewer roles.

**Parent Topic:**[REST API reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/rest-apis/api-rest.md)

## Product Catalog Search - POST /api/sn\_prd\_pm/catalog/search

Searches the product catalog and returns a paginated list of products that match the supplied search parameters.

Use this endpoint whenever an external application or agent needs to retrieve products from the catalog. For example, to populate a shopping interface, drive an AI recommendation flow, or validate catalog availability. The endpoint delegates to the existing script include entry point and supports the same context-aware pricing and eligibility logic available in the Product Catalog UI.

### Additional usage notes

-   If **headerContext** is provided only with `account` but other context values such as **pricelist**, **currency** aren't provided, they are automatically fetched based on the given account to evaluate eligibility rules.
-   If user has their own context variables for eligibility, those can be passed in **headerContext**.
-   If **headerContext** isn't provided, the currency will default to the system currency and standard price list.
-   Pass **sortOrder**, **sortBy** and **aiSearchSuggestionId** request parameters only if AI Search + RAG setup for product catalog search is done on the instance.

### URL format

Base URL: `/api/sn_prd_pm/{api_version}/catalog/search`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td>

Required. Version of the endpoint to access. Valid value: `v1`.

Requests made without the version fails with a "Requested URI doesn't represent any resource" error.

Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

aiSearchSuggestionId

</td><td>

Sys\_id of an AI Search suggestion record to associate with this search request. Used to support AI-assisted search flows.Data type: String

Default: empty string

</td></tr><tr><td>

catalogType

</td><td>

Type of catalog items to search. Case-sensitive.Valid values:

-   `PRODUCT_OFFERING`: Fetch product offerings.
-   `SERVICE_SPECIFICATION`: Fetch service specifications.

Data type: String

</td></tr><tr><td>

headerContext

</td><td>

Context object that controls pricing, eligibility, and localization applied to search results. When omitted, the API derives context from the account if one is provided.Data type: Object

```
"headerContext": {
      "account": "String",
      "pricelist": "String",
      "currency": "String",
      "suppressPricing": String,
      "transaction_date": "String",
      "shipping_city": "String",
      "shipping_country": "String",
      "shipping_location": "String",
      "shipping_state": "String",
      "shipping_street": "String",
      "shipping_zip": "String",
      "billing_city": "String",
      "billing_country": "String",
      "billing_location": "String",
      "billing_state": "String",
      "billing_street": "String",
      "billing_zip": "String",
      "sales_agreement": "String"
    }
```

</td></tr><tr><td>

headerContext.account

</td><td>

Sys\_id of the account to use for context resolution. When provided and other context fields are omitted, pricing and eligibility are resolved from the account.Data type: String

</td></tr><tr><td>

headerContext.billing\_city

</td><td>

City for the billing address. Data type: String

</td></tr><tr><td>

headerContext.billing\_country

</td><td>

Country for the billing address. Example: `USA`Data type: String

</td></tr><tr><td>

headerContext.billing\_location

</td><td>

Sys\_id of the billing location record.Table: Location \[location\]

Data type: String

</td></tr><tr><td>

headerContext.billing\_state

</td><td>

State or province for the billing address. Example: `TX`Data type: String

</td></tr><tr><td>

headerContext.billing\_street

</td><td>

Street address for billing.Data type: String

</td></tr><tr><td>

headerContext.billing\_zip

</td><td>

Postal code for the billing address. Example: `75254-7536`Data type: String

</td></tr><tr><td>

headerContext.currency

</td><td>

Currency code to use for pricing. Example: `USD`.Data type: String

Default: Derived from account if not supplied. If account not provided, resolves to system currency.

</td></tr><tr><td>

headerContext.pricelist

</td><td>

Sys\_id of the price list to apply.Table: Pricing List \[sn\_csm\_pricing\_price\_list\]

Default: Derived from account if not supplied.

Data type: String

</td></tr><tr><td>

headerContext.sales\_agreement

</td><td>

Sys\_id of the sales agreement to apply.Table: Sales Agreement \[sn\_sales\_agmt\_core\_sales\_agreement\]

Data type: String

</td></tr><tr><td>

headerContext.shipping\_city

</td><td>

City for the shipping address. Data type: String

</td></tr><tr><td>

headerContext.shipping\_country

</td><td>

Country for the shipping address. Example: `USA`Data type: String

</td></tr><tr><td>

headerContext.shipping\_location

</td><td>

Sys\_id of the shipping location record.Table: Location \[location\]

Data type: String

</td></tr><tr><td>

headerContext.shipping\_state

</td><td>

State or province for the shipping address. Example: `TX`Data type: String

</td></tr><tr><td>

headerContext.shipping\_street

</td><td>

Street address for shipping. Data type: String

</td></tr><tr><td>

headerContext.shipping\_zip

</td><td>

Postal code for the shipping address. Example: `75254-7536`Data type: String

</td></tr><tr><td>

headerContext.suppressPricing

</td><td>

Optional. Flag that indicates whether to suppress pricing information in the response. Valid values:

-   `true`: Pricing is suppressed.
-   `false`: Pricing is included.

Data type: Boolean

Default: false

</td></tr><tr><td>

headerContext.transaction\_date

</td><td>

Date and time of the transaction.Format: `yyyy-MM-dd HH:mm:ss` \(Example: 2026-03-30 20:20:08\)

Data type: String

</td></tr><tr><td>

pageIndex

</td><td>

Zero-based index of the page of results to return. Data type: Number \(integer\)

Minimum value: 0

Default: 0

</td></tr><tr><td>

pageLimit

</td><td>

Number of search results per page.Data type: Number

Default: 10

</td></tr><tr><td>

searchTerm

</td><td>

Keyword or phrase to search for in the product catalog. When null or empty, returns all products in the specified catalog.Data type: String

Default: null

</td></tr><tr><td>

selectedCatalog

</td><td>

Sys\_id of the catalog to search. Table: Product Offering Catalog \[sn\_prd\_pm\_product\_offering\_catalog\]

Data type: String

Default: “allCatalog” \(searches across all catalogs\)

</td></tr><tr><td>

selectedCategory

</td><td>

Sys\_id of the category to filter results by. If providing this value, you must pass the **selectedCatalog** to which that particular category belongs to.Table: Product Offering Category \[sn\_prd\_pm\_product\_offering\_category\]

Data type: String

Default: “showAll” \(returns results from all categories within the catalog\)

</td></tr><tr><td>

sortBy

</td><td>

Field to sort results by. Accepted values are dependent on the value of **catalogType**.Valid values:

-   PRODUCT\_OFFERING:
    -   `code`
    -   `description`
    -   `display_name`
    -   `name`
    -   `score`
-   For SERVICE\_SPECIFICATION:
    -   `description`
    -   `display_name`
    -   `name`
    -   `score`
    -   `specification_code`

Data type: String

</td></tr><tr><td>

sortOrder

</td><td>

Sort direction for results.Valid values:

-   `ascending`
-   `descending`

Data type: String

Default: descending

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/rest-api-explorer/c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Accept|Media type accepted by the client. Set to application/json.|
|Content-Type|Media type of the request body. Set to application/json.|
|Authorization|Access to the instance. \(OOB default ACL for scripted REST execute\)|

|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/rest-api-explorer/c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|OK. The search completed successfully. The response body contains the paginated list of matching products.|
|401|Unauthorized. The calling user isn't authenticated.|
|403|Forbidden. The calling user doesn't have the sn\_prd\_pm.product\_catalog\_viewer or sn\_prd\_pm.external\_product\_viewer role required to access this endpoint.|
|500|Internal Server Error. Custom message - “The request couldn't be processed due to an internal server error. Please retry later."|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

selectedCatalogHierarchy

</td><td>

List of all eligible catalog objects when no default catalog is configured and "All Catalogs" is the selected view.Data type: Array of Objects

```
"selectedCatalogHierarchy": [
  {
   "id": "String",
   "label": "String",
   "children": [] 
  }
]
```

</td></tr><tr><td>

selectedCatalogHierarchy.id

</td><td>

Category identifier. A sys\_id for catalog categories, or the literal `showAll` for the "Show all" option.Data type: String

</td></tr><tr><td>

selectedCatalogHierarchy.label

</td><td>

Display name of the category.Data type: String

</td></tr><tr><td>

selectedCatalogHierarchy.children

</td><td>

Child category nodes. Dependent on the value set for **selectedCategory** in the request:

-   Value is empty or `showAll` \(default\): Returns an empty array \(`[]`\) when there are no children; the `showAll` node returns an empty object \(`{}`\).
-   Value is a sys\_id: Returns the child sys ID, display value, and any nested children associated with the given category sys\_id.

 Data type: Object or Array

 ```
//'selectedCategory' is 'showAll'

{
   "id": "showAll",
   "label": "Show all",
   "children": {}
}

```

 ```
//'selectedCategory' is sys_id

{
 "id": "String",
 "label": "String",
 "children": [
  {
   "id": "String",
   "label": "String",
   "children": [Array]
  }
 ]
}
```

</td></tr><tr><td>

leafCategoryList

</td><td>

A comma-separated string of eligible leaf category sys\_ids used to filter product offerings, derived from the selected catalog and category hierarchy. Only included in the output when not already provided in the input filter.

Data type: String

</td></tr><tr><td>

response

</td><td>

An array matching the current filter criteria, including search terms, selected category, and eligibility rules.Data type: Array of Objects

```
"response": [
 {
   "productOfferingSysId": {Object},
   "code": {Object},
   "name": {Object},
   "description": {Object},
   "offerType": {Object},
   "pricingMethod": "String",
   "uom": {Object},
   "offerTypeVariation": "String",
   "listPrice": "String",
   "priceList": "String"
 }
]
```

</td></tr><tr><td>

response. productOfferingSysId

</td><td>

List containing the sys\_id\(s\) of the product offering record\(s\).Data type: Object

```
"productOfferingSysId": {
  "value": "String",
  "displayValue": "String"
}
```

</td></tr><tr><td>

response.productOfferingSysId.value

</td><td>

Stored \(raw\) value of the field.Data type: String

</td></tr><tr><td>

response.productOfferingSysId.displayValue

</td><td>

Display value of the field.Data type: String

</td></tr><tr><td>

response.code

</td><td>

Product offering code.Data type: Object

```
"code": {
  "value": "String",
  "displayValue": "String"
}
```

</td></tr><tr><td>

response.code.value

</td><td>

Stored \(raw\) value of the field.Data type: String

</td></tr><tr><td>

response.code.displayValue

</td><td>

Display value of the field.Data type: String

</td></tr><tr><td>

response.name

</td><td>

Display name of the product offering.Data type: Object

```
"name": {
  "value": "String",
  "displayValue": "String"
}
```

</td></tr><tr><td>

response.name.value

</td><td>

Stored \(raw\) value of the field.Data type: String

</td></tr><tr><td>

response.name.displayValue

</td><td>

Display value of the field.Data type: String

</td></tr><tr><td>

response.description

</td><td>

Details about the product offering.Data type: Object

```
"description": {
  "value": "String",
  "displayValue": "String"
}
```

</td></tr><tr><td>

response.description.value

</td><td>

Stored \(raw\) value of the field.Data type: String

</td></tr><tr><td>

response.description.displayValue

</td><td>

Display value of the field.Data type: String

</td></tr><tr><td>

response.offerType

</td><td>

Type of the product offering \(for example, `simple`, `config`, or `simple_with_spec`\).Data type: Object

```
"offerType": {
  "value": "String",
  "displayValue": "String"
}
```

</td></tr><tr><td>

response.offerType.value

</td><td>

Stored \(raw\) value of the field.Data type: String

</td></tr><tr><td>

response.offerType.displayValue

</td><td>

Display value of the field.Data type: String

</td></tr><tr><td>

response.pricingMethod

</td><td>

Pricing method for the offering.Possible values:

-   `one_time`
-   `recurring`

Data type: String

</td></tr><tr><td>

response.uom

</td><td>

Unit of measure for the offering.Data type: Object

```
"uom": {
  "sysId": "String",
  "name": "String"
}
```

</td></tr><tr><td>

response.uom.sys\_id

</td><td>

Sys\_id of the unit-of-measure record.Data type: String

</td></tr><tr><td>

response.uom.name

</td><td>

Display name of the unit of measure \(for example, `Each`\).Data type: String

</td></tr><tr><td>

response.offerTypeVariation

</td><td>

Variation type of the offering, typically matching offerType.Data type: String

</td></tr><tr><td>

response.listPrice

</td><td>

Formatted list price of the product offering \(for example, `"$50.00"`\). May be absent if no price is configured.Data type: String

</td></tr><tr><td>

response.priceList

</td><td>

Sys\_id of the associated price list record. May be absent if no price list is assigned.Data type: String

</td></tr><tr><td>

response.visual

</td><td>

URL to the product offering's image/thumbnail, if configured and if sn\_prd\_pm.show\_product\_visuals system property is enabled.Data type: String

</td></tr><tr><td>

response.derivedPrice

</td><td>

Flag that indicates whether the product's price is calculated dynamically based on related products, product characteristics, or predefined pricing rules rather than having a fixed catalog list price.Valid values:

-   true: Product's price is calculated dynamically.
-   false: Product's price is calculated using a fixed catalog list price.

Data type: Boolean

</td></tr><tr><td>

response.items.semanticSimilarity

</td><td>

Relevance or semantic score assigned to this result by the AI search engine. Field is absent from non-AI Search responses.Data type: Number

</td></tr><tr><td>

spellCorrectedTerm

</td><td>

Spell-corrected version of the search term, returned when AI Search + RAG is enabled and a correction is available. Field is absent from non-AI Search responses.Data type: String

</td></tr><tr><td>

suggestedRecordDisplayName

</td><td>

Display name of a suggested record, returned when AI Search + RAG is enabled and a direct match suggestion exists.Data type: String

</td></tr><tr><td>

count

</td><td>

Number of product offerings in the `response` array.Data type: Number

</td></tr></tbody>
</table>### cURL request

The following example searches for offerings matching the term 'modem' within a specific catalog and category, with an account context for pricing and eligibility.

```
curl "https://instance.servicenow.com/api/sn_prd_pm/v1/catalog/search" \ 
--request POST \ 
--header "Accept:application/json" \ 
--header "Content-Type:application/json" \ 
--data "{\"searchTerm\":\"modem\",\"selectedCatalog\":\"eaf0159fd0a63110f8770dbf976be178\",\"selectedCategory\":\"e6f0159fd0a63110f8770dbf976be18c\",\"headerContext\":{\"account\":\"ffc68911c35420105252716b7d40dd55\"}}" \ 
--user 'username':'password' 
```

Response body.

```
{
  "selectedCatalogHierarchy": [
    { "id": "showAll", "label": "Show all", "children": {} },
    { "id": "eaf0159fd0a63110f8770dbf976be18a", "label": "Connected Car", "children": [] },
    { "id": "7e6d2c02742e4a10f877468e695efae1", "label": "Connectivity Services", "children": [] },
    { "id": "aef0159fd0a63110f8770dbf976be185", "label": "Elevators", "children": [] },
    { "id": "50605f1a49e0b210f8777676c00265b6", "label": "Enterprise SaaS Solutions", "children": [] },
    { "id": "6ef0159fd0a63110f8770dbf976be189", "label": "Home Automation", "children": [] },
    { "id": "e6f0159fd0a63110f8770dbf976be18c", "label": "Internet", "children": [] },
    { "id": "6af0159fd0a63110f8770dbf976be18b", "label": "MultiPlay", "children": [] },
    { "id": "eef0159fd0a63110f8770dbf976be188", "label": "OTT", "children": [] },
    { "id": "8eb87bb3ff1ef61081adffffffffff53", "label": "Solana US Catalog_all_offers", "children": [] }
  ],
  "leafCategoryList": "e6f0159fd0a63110f8770dbf976be18c",
  "response": [
    {
      "productOfferingSysId": {
        "value": "0b61dd9fd0a63110f8770dbf976be171",
        "displayValue": "0b61dd9fd0a63110f8770dbf976be171"
      },
      "code": {
        "value": "SOLANAMODE2",
        "displayValue": "SOLANAMODE2"
      },
      "name": {
        "value": "Solana Modem M Series",
        "displayValue": "Solana Modem M Series"
      },
      "description": {
        "value": "Solana Modem M Series",
        "displayValue": "Solana Modem M Series"
      },
      "offerType": {
        "value": "simple",
        "displayValue": "simple"
      },
      "pricingMethod": "one_time",
      "uom": {
        "sysId": "cb2795d553020110286eddeeff7b12ff",
        "name": "Each"
      },
      "offerTypeVariation": "simple",
      "listPrice": "$130.00",
      "priceList": "19d29513d0e63110f8770dbf976be122"
    },
    {
      "productOfferingSysId": {
        "value": "0761dd9fd0a63110f8770dbf976be173",
        "displayValue": "0761dd9fd0a63110f8770dbf976be173"
      },
      "code": {
        "value": "SOLANAMODE1",
        "displayValue": "SOLANAMODE1"
      },
      "name": {
        "value": "Solana Modem N Series",
        "displayValue": "Solana Modem N Series"
      },
      "description": {
        "value": "The Solana Modem N Series is engineered to deliver exceptional performance, reliability, and seamless connectivity for both residential and business environments. Designed for users who demand high-speed internet, the N Series modem offers cutting-edge technology that supports the latest broadband standards, providing a robust solution for all your data needs.   Technical Specifications Modem Type: - Cable Modem (DOCSIS 3.1) - Wi-Fi Standards: 802.11ac (Dual-Band) - Ethernet Ports: 4x Gigabit Ethernet Ports - Wi-Fi Range: Up to 1500 sq. ft. (coverage may vary based on environment) - Speed: Supports up to [Insert Maximum Speed] ",
        "displayValue": "The Solana Modem N Series is engineered to deliver exceptional performance, reliability, and seamless connectivity for both residential and business environments. Designed for users who demand high-speed internet, the N Series modem offers cutting-edge technology that supports the latest broadband standards, providing a robust solution for all your data needs.   Technical Specifications Modem Type: - Cable Modem (DOCSIS 3.1) - Wi-Fi Standards: 802.11ac (Dual-Band) - Ethernet Ports: 4x Gigabit Ethernet Ports - Wi-Fi Range: Up to 1500 sq. ft. (coverage may vary based on environment) - Speed: Supports up to [Insert Maximum Speed] "
      },
      "offerType": {
        "value": "simple",
        "displayValue": "simple"
      },
      "pricingMethod": "one_time",
      "uom": {
        "sysId": "cb2795d553020110286eddeeff7b12ff",
        "name": "Each"
      },
      "offerTypeVariation": "simple",
      "listPrice": "$120.00",
      "priceList": "19d29513d0e63110f8770dbf976be122"
    }
  ],
  "count": 2
}
```

### cURL request

The following example searches for service specifications matching the term “firewall service”.

```
curl "https://instance.servicenow.com/api/sn_prd_pm/v1/catalog/search" \ 
--request POST \ 
--header "Accept:application/json" \ 
--header "Content-Type:application/json" \ 
--data "{\"searchTerm\":\"firewall service\", \"catalogType\":\"SERVICE_SPECIFICATION\"}" \ 
--user 'admin':'admin'
```

Response body.

```
{
  "response": [
    {
      "productOfferingSysId": {
        "value": "f99546ff07266010a7955b7e0ad300a8",
        "displayValue": "f99546ff07266010a7955b7e0ad300a8"
      },
      "code": {
        "value": "MANAGEDFIREWALLSERVICE",
        "displayValue": "MANAGEDFIREWALLSERVICE"
      },
      "name": {
        "value": "Managed Firewall Service",
        "displayValue": "Managed Firewall Service"
      },
      "description": {
        "value": "Managed Firewall Service",
        "displayValue": "Managed Firewall Service"
      },
      "offerType": {
        "value": "config",
        "displayValue": "config"
      }
    },
    {
      "productOfferingSysId": {
        "value": "52c6b30d773301108b2a1e599a5a9954",
        "displayValue": "52c6b30d773301108b2a1e599a5a9954"
      },
      "code": {
        "value": "MANAGEDFIREWALLSERVICEV2",
        "displayValue": "MANAGEDFIREWALLSERVICEV2"
      },
      "name": {
        "value": "Managed Firewall Service v2",
        "displayValue": "Managed Firewall Service v2"
      },
      "description": {
        "value": "Managed Firewall Service",
        "displayValue": "Managed Firewall Service"
      },
      "offerType": {
        "value": "config",
        "displayValue": "config"
      }
    },
    {
      "productOfferingSysId": {
        "value": "35d077304f3e1110b915b2e76e72e06e",
        "displayValue": "35d077304f3e1110b915b2e76e72e06e"
      },
      "code": {
        "value": "MANAGEDFIREWALLSERVICEV3",
        "displayValue": "MANAGEDFIREWALLSERVICEV3"
      },
      "name": {
        "value": "Managed Firewall Service v3",
        "displayValue": "Managed Firewall Service v3"
      },
      "description": {
        "value": "Managed Firewall Service",
        "displayValue": "Managed Firewall Service"
      },
      "offerType": {
        "value": "config",
        "displayValue": "config"
      }
    },
    {
      "productOfferingSysId": {
        "value": "14735356775131108e191e599a5a99c9",
        "displayValue": "14735356775131108e191e599a5a99c9"
      },
      "code": {
        "value": "MANAGEDFIREWALLSERVICEV4",
        "displayValue": "MANAGEDFIREWALLSERVICEV4"
      },
      "name": {
        "value": "Managed Firewall Service v4",
        "displayValue": "Managed Firewall Service v4"
      },
      "description": {
        "value": "Managed Firewall Service",
        "displayValue": "Managed Firewall Service"
      },
      "offerType": {
        "value": "config",
        "displayValue": "config"
      }
    }
  ],
  "count": 4
}
```

### cURL request

The following example performs a search request using the full set of parameters and a complete header context.

```
curl "https://instance.servicenow.com/api/sn_prd_pm/v1/catalog/search" \
  --request POST \
  --header "Accept: application/json" \
  --header "Content-Type: application/json" \
  --user 'username:password' \
  --data '{
    "searchTerm": "sensor",
    "selectedCatalog": "eaf0159fd0a63110f8770dbf976be178",
    "selectedCategory": "6ef0159fd0a63110f8770dbf976be189",
    "pageIndex": 0,
    "pageLimit": 10,
    "catalogType": "PRODUCT_OFFERING",
    "sortOrder": "descending",
    "sortBy": "score",
    "aiSearchSuggestionId": "",
    "headerContext": {
      "account": "ffc68911c35420105252716b7d40dd55",
      "pricelist": "19d29513d0e63110f8770dbf976be122",
      "currency": "USD",
      "suppressPricing": false,
      "transaction_date": "2026-03-30 20:20:08",
      "shipping_city": "Dallas",
      "shipping_country": "USA",
      "shipping_location": "25aba2ed0a0a0bb300b69ce49ae72211",
      "shipping_state": "TX",
      "shipping_street": "13770 Noel Road, Dallas",
      "shipping_zip": "75254-7536",
      "billing_city": "Dallas",
      "billing_country": "USA",
      "billing_location": "25aba2ed0a0a0bb300b69ce49ae72211",
      "billing_state": "TX",
      "billing_street": "13770 Noel Road, Dallas",
      "billing_zip": "75254-7536",
      "sales_agreement": ""
    }
  }'
```

Response body.

```
{
  "selectedCatalogHierarchy": [
    { "id": "showAll", "label": "Show all", "children": {} },
    { "id": "eaf0159fd0a63110f8770dbf976be18a", "label": "Connected Car", "children": [] },
    { "id": "7e6d2c02742e4a10f877468e695efae1", "label": "Connectivity Services", "children": [] },
    { "id": "aef0159fd0a63110f8770dbf976be185", "label": "Elevators", "children": [] },
    { "id": "50605f1a49e0b210f8777676c00265b6", "label": "Enterprise SaaS Solutions", "children": [] },
    { "id": "6ef0159fd0a63110f8770dbf976be189", "label": "Home Automation", "children": [] },
    { "id": "e6f0159fd0a63110f8770dbf976be18c", "label": "Internet", "children": [] },
    { "id": "6af0159fd0a63110f8770dbf976be18b", "label": "MultiPlay", "children": [] },
    { "id": "eef0159fd0a63110f8770dbf976be188", "label": "OTT", "children": [] },
    { "id": "8eb87bb3ff1ef61081adffffffffff53", "label": "Solana US Catalog_all_offers", "children": [] }
  ],
  "leafCategoryList": "6ef0159fd0a63110f8770dbf976be189",
  "response": [
    {
      "productOfferingSysId": {
        "value": "fe5d203e11307110f877366201dea631",
        "displayValue": "fe5d203e11307110f877366201dea631"
      },
      "code": {
        "value": "DOORSENSOR1",
        "displayValue": "DOORSENSOR1"
      },
      "name": {
        "value": "Door Sensor",
        "displayValue": "Door Sensor"
      },
      "description": {
        "value": "Door Sensor",
        "displayValue": "Door Sensor"
      },
      "offerType": {
        "value": "simple",
        "displayValue": "simple"
      },
      "pricingMethod": "one_time",
      "uom": {
        "sysId": "cb2795d553020110286eddeeff7b12ff",
        "name": "Each"
      },
      "offerTypeVariation": "simple",
      "listPrice": "$10.00",
      "priceList": "19d29513d0e63110f8770dbf976be122"
    },
    {
      "productOfferingSysId": {
        "value": "1b20347e11307110f877366201dea67f",
        "displayValue": "1b20347e11307110f877366201dea67f"
      },
      "code": {
        "value": "WINSENSOR1",
        "displayValue": "WINSENSOR1"
      },
      "name": {
        "value": "Window Sensor",
        "displayValue": "Window Sensor"
      },
      "description": {
        "value": "Window Sensor",
        "displayValue": "Window Sensor"
      },
      "offerType": {
        "value": "simple",
        "displayValue": "simple"
      },
      "pricingMethod": "one_time",
      "uom": {
        "sysId": "cb2795d553020110286eddeeff7b12ff",
        "name": "Each"
      },
      "offerTypeVariation": "simple",
      "listPrice": "$15.00",
      "priceList": "19d29513d0e63110f8770dbf976be122"
    }
  ],
  "count": 2
}
```

## Product Catalog Search - POST /api/sn\_prd\_pm/v1/catalog/eligible-catalog-category-hierarchy

Retrieves the product catalog-category hierarchy filtered by eligibility rules. Resolves the input header context request object \(currency, pricelist, address, etc.\), and applies eligibility encoded queries to filter out ineligible catalogs/categories to construct the tree.

### URL format

Default URL: `/api/sn_prd_pm/{api_version}/catalog/eligible-catalog-category-hierarchy`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td>

Required. Version of the endpoint to access. Valid value: `v1`.

Requests made without the version fails with a "Requested URI doesn't represent any resource" error.

Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

headerContext

</td><td>

Context object that controls the eligibility used to resolve the catalog-category hierarchy. When omitted, the API derives context from the account if one is provided.Data type: Object

```
"headerContext": {
    "account": "String",
    "billing_city": "String",
    "billing_country": "String",
    "billing_location": "String",
    "billing_state": "String",
    "billing_street": "String",
    "billing_zip": "String",
    "currency": "String",
    "pricelist": "String",
    "sales_agreement": "String",
    "shipping_city": "String",
    "shipping_country": "String",
    "shipping_location": "String",
    "shipping_state": "String",
    "shipping_street": "String",
    "shipping_zip": "String",
    "transaction_date": "String"
  }
```

</td></tr><tr><td>

headerContext.account

</td><td>

Optional. Sys\_id of the account to use for context resolution. When provided and other context fields are omitted, pricing and eligibility are resolved from the account.Table: Accounts \[customer\_account\]

Data type: String

</td></tr><tr><td>

headerContext.billing\_city

</td><td>

Optional. City for the billing address.Data type: String

</td></tr><tr><td>

headerContext.billing\_country

</td><td>

Optional. Country for the billing address.Data type: String

</td></tr><tr><td>

headerContext.billing\_location

</td><td>

Optional. Sys\_id of the billing location record.Table: Location \[location\]

Data type: String

</td></tr><tr><td>

headerContext.billing\_state

</td><td>

Optional. State or province code of the billing address.Data type: String

</td></tr><tr><td>

headerContext.billing\_street

</td><td>

Optional. Street address for billing.Data type: String

</td></tr><tr><td>

headerContext.billing\_zip

</td><td>

Postal code for the billing address.Example: 75254-7536

Data type: String

</td></tr><tr><td>

headerContext.currency

</td><td>

Currency code to use for pricing.Example: USD

Data type: String

Default: Derived from account if not supplied. If account not provided, resolves to system currency.

</td></tr><tr><td>

headerContext.pricelist

</td><td>

Optional. Sys\_id of the price list.Table: Pricing List \[sn\_csm\_pricing\_price\_list\]

Data type: String

Default: Derived from account if not supplied.

</td></tr><tr><td>

headerContext.sales\_agreement

</td><td>

Optional. Sys\_id of the sales agreement to apply. Table: Sales Agreement \[sn\_sales\_agmt\_core\_sales\_agreement\]

Data type: String

</td></tr><tr><td>

headerContext.shipping\_city

</td><td>

Optional. City for the shipping address.Data type: String

</td></tr><tr><td>

headerContext.shipping\_country

</td><td>

Optional. Country for the shipping address.Example: USA

Data type: String

</td></tr><tr><td>

headerContext.shipping\_location

</td><td>

Sys\_id of the shipping location record.Table: Location \[location\]

Data type: String

</td></tr><tr><td>

headerContext.shipping\_state

</td><td>

State or province for the shipping address.Example: TX

</td></tr><tr><td>

headerContext.shipping\_street

</td><td>

Optional. Street address for shipping.Data type: String

</td></tr><tr><td>

headerContext.shipping\_zip

</td><td>

Optional. Postal code for the shipping address. Example: 75254-7536

Data type: String

</td></tr><tr><td>

headerContext.transaction\_date

</td><td>

Date and time of the transaction.Format: yyyy-MM-dd HH:mm:ss

Example: 2026-03-30 20:20:08

Data type: String

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/rest-api-explorer/c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Accept|Media type accepted by the client. Set to application/JSON.|
|Content-Type|Media type of the request body. Set to application/JSON.|
|Authorization|Access to the ServiceNow instance \(default ACL for scripted REST execute\).|

|Header|Description|
|------|-----------|
|None|No custom response headers returned by this endpoint.|

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/rest-api-explorer/c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|OK. The request completed successfully. The response body contains the eligible catalog-category hierarchy for the resolved context.|
|401|Unauthorized. The calling user isn't authenticated.|
|403|Forbidden. The calling user doesn't have the sn\_prd\_pm.product\_catalog\_viewer or sn\_prd\_pm.external\_product\_viewer role required to access this endpoint.|
|500|Internal Server Error. Custom message: `The request couldn't be processed due to an internal server error. Please retry later.`|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

defaultCatalog

</td><td>

The primary catalog configured as the default for the current context, containing its full category hierarchy tree. Only present when a published catalog with `is_default=true` exists and has eligible categories beyond "Show all".

Data type: Object

```
{
  "id": "String",
  "label": "String",
  "categories": [Array]
}
```

</td></tr><tr><td>

defaultCatalog.id

</td><td>

Sys\_id of the default product offering catalog record.Table: Product Offering Catalog \[sn\_prd\_pm\_product\_offering\_catalog\]

Data type: String

</td></tr><tr><td>

defaultCatalog.label

</td><td>

Display name of the default catalog. Data type: String

</td></tr><tr><td>

defaultCatalog.categories

</td><td>

Top-level categories within the default catalog, each containing a recursive children tree of subcategories. Always includes a synthetic "Show all" entry as the first element. Data type: Array of Objects

```
[
  {
    "id": "String",
    "label": "String",
    "children": [Array]
  }
]
```

</td></tr><tr><td>

catalogList

</td><td>

An alphabetically sorted array of all other eligible published product offering catalogs \(excluding the default\), each with its own category hierarchy tree. Present even when empty. Data type: Array of Objects

```
[
  {
    "id": "String",
    "label": "String",
    "categories": [Array]
  }
]
```

</td></tr><tr><td>

catalogList.id

</td><td>

Sys\_id of the product offering catalog record.Table: Product Offering Catalog \[sn\_prd\_pm\_product\_offering\_catalog\]

Data type: String

</td></tr><tr><td>

catalogList.label

</td><td>

Display name of the catalog.Data type: String

</td></tr><tr><td>

catalogList.categories

</td><td>

Top-level categories within the catalog, each containing a recursive children tree of subcategories. Always includes a synthetic "Show all" entry as the first element. Catalogs that would contain only "Show all" \(no eligible categories\) are removed entirely from the response.

Data type: Array of Objects

```
[
  {
    "id": "String",
    "label": "String",
    "children": [Array]
  }
]
```

</td></tr><tr><td>

categories.id

</td><td>

Sys\_id of the category record, or the literal string "showAll" for the default catch-all entry.Table: Product Category \[sn\_prd\_pm\_product\_category\]

Data type: String

</td></tr><tr><td>

categories.label

</td><td>

Localized display name of the category. Translated via gs.getMessage for "Show all", via getDisplayValue\('name'\) for real categories.Data type: String

</td></tr><tr><td>

categories.children

</td><td>

Child category objects following the same structure recursively \(id, label, children\). Empty array \[\] when the category is a leaf node. Empty object \{\} for the "Show all" entry. Data type: Array of Objects

```
[
  {
    "id": "String",
    "label": "String",
    "children": [Array]
  }
]
```

</td></tr></tbody>
</table>### cURL request

The following example retrieves a complete product catalog-category hierarchy.

```
curl "https://instance.servicenow.com/api/sn_prd_pm/v1/catalog/eligible-catalog-category-hierarchy" \ 
--request POST \ 
--header "Accept:application/json" \  
--header "Content-Type:application/json" \ 
--user 'username':'password' 
```

Response:

```
{
  "defaultCatalog": {
    "id": "eaf0159fd0a63110f8770dbf976be178",
    "label": "Solana US Catalog",
    "categories": [
      {
        "id": "showAll",
        "label": "Show all",
        "children": {}
      },
      {
        "id": "eaf0159fd0a63110f8770dbf976be18a",
        "label": "Connected Car",
        "children": []
      },
      {
        "id": "7e6d2c02742e4a10f877468e695efae1",
        "label": "Connectivity Services",
        "children": []
      }
    ]
  },
  "catalogList": [
    {
      "id": "caecc5fd4f12e110c5ff2624b2ce0b0e",
      "label": "Business Ethernet Plan",
      "categories": [
        {
          "id": "showAll",
          "label": "Show all",
          "children": {}
        },
        {
          "id": "9fe305a143b631105029d1529ab8f27b",
          "label": "Business Ethernet Plan_all_offers",
          "children": []
        }
      ]
    },
    {
      "id": "c835d8792b11525047f3f3e30391bf31",
      "label": "Food and Beverage Processing",
      "categories": [
        {
          "id": "showAll",
          "label": "Show all",
          "children": {}
        },
        {
          "id": "1c7950f12b51525047f3f3e30391bfac",
          "label": "Beverage Processing",
          "children": [
            {
              "id": "5c8814712b51525047f3f3e30391bf3f",
              "label": "Boiling Water Treatment",
              "children": []
            },
            {
              "id": "2da810b12b51525047f3f3e30391bf48",
              "label": "Cooling Water Treatment",
              "children": []
            }
          ]
        },
        {
          "id": "1ca954f12b51525047f3f3e30391bfee",
          "label": "Food Processing",
          "children": [
            {
              "id": "60c95cb12b51525047f3f3e30391bf94",
              "label": "Automation Data & Digital",
              "children": [
                {
                  "id": "c4ae46362b519e5021e4f1e04391bf3a",
                  "label": "Asset Performance Management",
                  "children": []
                }
              ]
            }
          ]
        }
      ]
    }
  ]
}
```

### cURL request

The following example shows a response with eligibility filtering applied.

Eligibility rules can restrict which catalogs and categories are returned based on the resolved context \(e.g., account, currency, pricelist, address, or any combination configured in the eligibility rule matrix\). When a catalog/category is deemed ineligible, it is removed entirely from the response - it does not appear in defaultCatalog or catalogList.

In this example, eligibility rules configured on the instance exclude "Solana US Catalog" for the given context. As a result, the next eligible catalog marked as default - "Configurable Products" - is promoted to defaultCatalog.

```
curl "https://instance.servicenow.com/api/sn_prd_pm/v1/catalog/eligible-catalog-category-hierarchy" \
--request POST \ 
--header "Accept:application/json" \ 
--header "Content-Type:application/json" \ 
--data "{\"headerContext\":{\"account\":\"86837a386f0331003b3c498f5d3ee4ca\"}}" \ 
--user 'username':'password'
```

Response:

```
{
  "defaultCatalog": {
    "id": "b3082af8ff30bad005aafffffffffff9",
    "label": "Configurable Products",
    "categories": [
      {
        "id": "showAll",
        "label": "Show all",
        "children": {}
      },
      {
        "id": "7f082af8ff30bad005aafffffffffff9",
        "label": "Configurable Products",
        "children": []
      }
    ]
  },
  "catalogList": [
    {
      "id": "caecc5fd4f12e110c5ff2624b2ce0b0e",
      "label": "Business Ethernet Plan",
      "categories": []
    }
  ]
}
```

