---
title: CatalogSearchAPI - Scoped, Global
description: CatalogSearchAPI is a script include used to fetch product catalog data from all application scopes.Creates an instance of the CatalogSearchAPI class.Searches the product catalog and returns matching catalog items with optional pricing information. Supports searching across multiple catalog types.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/api-reference/server-api-reference/CatalogSearchAPI-scoped\_global.html
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-06-29"
reading_time_minutes: 10
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# CatalogSearchAPI- Scoped, Global

CatalogSearchAPI is a script include used to fetch product catalog data from all application scopes.

The CatalogSearchAPI API is available by default with the Product Catalog Management application and is offered as the script include sn\_prd\_pm.CatalogSearchAPI under the namespace sn\_prd\_pm. No special roles are required to access this API.

Find the REST version of this API at [Product Catalog Search API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/rest-apis/product-catalog-search-api.md).

**Note:** There are distinct differences between this API and [CatalogSearch - Scoped](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/c_CatalogSearchScoped.md) though they're almost identically named. CatalogSearch API is a native ServiceNow platform API documented in the public API reference under `com.glideapp.servicecatalog.CatalogSearch`. It provides basic catalog item search functionality available in scoped scripts via the standard platform.

This API, CatalogSearchAPI \(sn\_prd\_pm.CatalogSearchAPI\), is the script include wrapper API specific to the Product Catalog Management application. It extends beyond the native API to support product offerings and service specifications, with richer filtering, account-based pricing and eligibility via `headerContext`, and AI Search integration.

**Parent Topic:**[Server API reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/api-server.md)

## CatalogSearchAPI - CatalogSearch\(\)

Creates an instance of the CatalogSearchAPI class.

|Name|Type|Description|
|----|----|-----------|
|None| ||

The following example is a constructor for the CatalogSearchAPI class:

```
var catalogSearch = new sn_prd_pm.CatalogSearchAPI();
```

## CatalogSearchAPI – getCatalogData\(Object input\)

Searches the product catalog and returns matching catalog items with optional pricing information. Supports searching across multiple catalog types.

Capabilities provided:

-   Search products by search term across one or all catalogs and across one or all categories within a catalog.
-   Filter results by catalog, category, and catalog type \(defaults to Product Offering\).
-   Page through result sets using a zero-based page index and page limit.
-   Supply a header context object to apply account-specific pricing, price lists, currency, channel, shipping/billing address, and sales agreement to search results.
-   Control sort order and sort field \(for example, by relevance score\).
-   Optionally pass an AI Search suggestion ID to support AI-assisted search flows.

<table id="table_lsj_snd_tjc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

aiSearchSuggestionId

</td><td>

String

</td><td>

Sys\_id of an AI Search suggestion record to associate with this search request. Used to support AI-assisted search flows.Default: empty string

</td></tr><tr><td>

catalogType

</td><td>

String

</td><td>

Type of catalog items to search. Case-sensitive.Valid values:

-   `PRODUCT_OFFERING`: Fetch product offerings.
-   `SERVICE_SPECIFICATION`: Fetch service specifications.

</td></tr><tr><td>

headerContext

</td><td>

Object

</td><td>

Context object that controls pricing, eligibility, and localization applied to search results. When omitted, the API derives context from the account if one is provided.```
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

String

</td><td>

Optional. Sys\_id of the account to use for context resolution. When provided and other context fields are omitted, pricing and eligibility are resolved from the account.

</td></tr><tr><td>

headerContext. billing\_city

</td><td>

String

</td><td>

Optional. City for the billing address.

</td></tr><tr><td>

headerContext. billing\_country

</td><td>

String

</td><td>

Optional. Country for the billing address.

</td></tr><tr><td>

headerContext. billing\_location

</td><td>

String

</td><td>

Optional. Sys\_id of the billing location record.Table: Location \[location\]

</td></tr><tr><td>

headerContext. billing\_state

</td><td>

String

</td><td>

Optional. State or province code of the billing address.

</td></tr><tr><td>

headerContext. billing\_street

</td><td>

String

</td><td>

Optional. Street address for billing.

</td></tr><tr><td>

headerContext. billing\_zip

</td><td>

String

</td><td>

Postal code for the billing address. Example: `75254-7536`Data type: String

</td></tr><tr><td>

headerContext.currency

</td><td>

String

</td><td>

Currency code to use for pricing. Example: `USD`.Default: Derived from account if not supplied. If account not provided, resolves to system currency.

</td></tr><tr><td>

headerContext.pricelist

</td><td>

String

</td><td>

Optional. Sys\_id of the price list to apply.Table: Pricing List \[sn\_csm\_pricing\_price\_list\]

Default: Derived from account if not supplied.

</td></tr><tr><td>

headerContext. sales\_agreement

</td><td>

String

</td><td>

Optional. Sys\_id of the sales agreement to apply.Table: Sales Agreement \[sn\_sales\_agmt\_core\_sales\_agreement\]

</td></tr><tr><td>

headerContext. shipping\_city

</td><td>

String

</td><td>

Optional. City for the shipping address.

</td></tr><tr><td>

headerContext. shipping\_country

</td><td>

String

</td><td>

Optional. Country for the shipping address. Example: `USA`

</td></tr><tr><td>

headerContext. shipping\_location

</td><td>

String

</td><td>

Sys\_id of the shipping location record.Table: Location \[location\]

</td></tr><tr><td>

headerContext. shipping\_state

</td><td>

String

</td><td>

State or province for the shipping address. Example: `TX`

</td></tr><tr><td>

headerContext. shipping\_street

</td><td>

String

</td><td>

Optional. Street address for shipping.

</td></tr><tr><td>

headerContext. shipping\_zip

</td><td>

String

</td><td>

Optional. Postal code for the shipping address. Example: `75254-7536`

</td></tr><tr><td>

headerContext. suppressPricing

</td><td>

Boolean

</td><td>

Optional. Flag that indicates whether to suppress pricing information in the response. Valid values:

-   `true`: Pricing is suppressed.
-   `false`: Pricing is included.

Default: false

</td></tr><tr><td>

headerContext. transaction\_date

</td><td>

String

</td><td>

Date and time of the transaction.Format: `yyyy-MM-dd HH:mm:ss` \(Example: 2026-03-30 20:20:08\)

</td></tr><tr><td>

pageIndex

</td><td>

Number

</td><td>

Optional. Zero-based index of the page of results to return. Minimum value: 0

Default: 0

</td></tr><tr><td>

pageLimit

</td><td>

Number

</td><td>

Optional. Number of search results per page.Default: 10

</td></tr><tr><td>

searchTerm

</td><td>

String

</td><td>

Optional. Keyword or phrase to search for in the product catalog. When null or empty, returns all products in the specified catalog. Default: null

</td></tr><tr><td>

selectedCatalog

</td><td>

String

</td><td>

Sys\_id of the catalog to search. Table: Product Offering Catalog \[sn\_prd\_pm\_product\_offering\_catalog\]

Default: “allCatalog” \(searches across all catalogs\)

</td></tr><tr><td>

selectedCategory

</td><td>

String

</td><td>

Sys\_id of the category to filter results by. If providing this value, you must pass the **selectedCatalog** to which that particular category belongs to.Table: Product Offering Category \[sn\_prd\_pm\_product\_offering\_category\]

Default: “showAll” \(returns results from all categories within the catalog\)

</td></tr><tr><td>

sortBy

</td><td>

String

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
    -   `specificaton_code`

Data type: String

</td></tr><tr><td>

sortOrder

</td><td>

String

</td><td>

Optional. Sort direction for results.Valid values:

-   `ascending`
-   `descending`

Default: descending

</td></tr></tbody>
</table><table id="table_msj_snd_tjc" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

count

</td><td>

Number of product offerings in the `response` array.Data type: Number

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

response.code.displayValue

</td><td>

Display value of the field.Data type: String

</td></tr><tr><td>

response.code.value

</td><td>

Stored \(raw\) value of the field.Data type: String

</td></tr><tr><td>

response.derivedPrice

</td><td>

Flag that indicates whether the product's price is calculated dynamically based on related products, product characteristics, or predefined pricing rules rather than having a fixed catalog list price.Valid values:

-   true: Product's price is calculated dynamically.
-   false: Product's price is calculated using a fixed catalog list price.

Data type: Boolean

</td></tr><tr><td>

response.items.description

</td><td>

Details about the product offering.Data type: Object

```
"description": {
  "value": "String",
  "displayValue": "String"
}
```

</td></tr><tr><td>

response.items.description.displayValue

</td><td>

Display value of the description.Data type: String

</td></tr><tr><td>

response.items.description.value

</td><td>

Stored \(raw\) value of the description.Data type: String

</td></tr><tr><td>

response.items. listPrice

</td><td>

Formatted list price of the product offering \(for example, `"$50.00"`\). May be absent if no price is configured.Data type: String

</td></tr><tr><td>

response.items.offerType

</td><td>

Type of the product offering \(for example, `simple`, `config`, or `simple_with_spec`\).Data type: Object

```
"offerType": {
  "value": "String",
  "displayValue": "String"
}
```

</td></tr><tr><td>

response.items.offerType.displayValue

</td><td>

Display value of the field.Data type: String

</td></tr><tr><td>

response.items.offerType.value

</td><td>

Stored \(raw\) value of the field.Data type: String

</td></tr><tr><td>

response.items. offerTypeVariation

</td><td>

Variation type of the offering, typically matching offerType.Data type: String

</td></tr><tr><td>

response.items. priceList

</td><td>

Sys\_id of the associated price list record. May be absent if no price list is assigned.Data type: String

</td></tr><tr><td>

response.items.pricingMethod

</td><td>

Pricing method for the offering.Possible values:

-   `one_time`
-   `recurring`

Data type: String

</td></tr><tr><td>

response.items. productOfferingSysId

</td><td>

List containing the sys\_id\(s\) of the product offering record\(s\).Data type: Object

```
"productOfferingSysId": {
  "value": "String",
  "displayValue": "String"
}
```

</td></tr><tr><td>

response.items. semanticSimilarity

</td><td>

Relevance or semantic score assigned to this result by the AI search engine.Data type: Number

</td></tr><tr><td>

response.items.uom

</td><td>

Unit of measure for the offering.Data type: Object

```
"uom": {
  "sysId": "String",
  "name": "String"
}
```

</td></tr><tr><td>

response.items.uom.name

</td><td>

Display name of the unit of measure \(for example, `Each`\).Data type: String

</td></tr><tr><td>

response.items.uom.sysId

</td><td>

Sys\_id of the unit-of-measure record.Data type: String

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

response.name.displayValue

</td><td>

Display value of the field.Data type: String

</td></tr><tr><td>

response.name.value

</td><td>

Stored \(raw\) value of the field.Data type: String

</td></tr><tr><td>

response. productOfferingSysId.displayValue

</td><td>

Display value of the field.Data type: String

</td></tr><tr><td>

response. productOfferingSysId.value

</td><td>

Stored \(raw\) value of the field.Data type: String

</td></tr><tr><td>

response.visual

</td><td>

URL to the product offering's image/thumbnail, if configured and if sn\_prd\_pm.show\_product\_visuals system property is enabled.Data type: String

</td></tr><tr><td>

selectedCatalogHierarchy

</td><td>

List of all eligible catalog objects when no default catalog is configured and "All Catalogs" is the selected view.Data type: Array of Objects

```
"selectedCatalogHierarchy": [
  {
   "id": "String",
   "label": String",
   "children": [] 
  }
]
```

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
   "id": "String"
   "label": "String",
   "children": [Array]
  }
 ]
}
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

spellCorrectedTerm

</td><td>

Spell-corrected version of the search term, returned when AI Search + RAG is enabled and a correction is available.Data type: String

</td></tr><tr><td>

suggestedRecordDisplayName

</td><td>

Display name of a suggested record, returned when AI Search + RAG is enabled and a direct match suggestion exists.Data type: String

</td></tr></tbody>
</table>### Search by keyword within a catalog and category

The following example searches for offerings matching the term `router` within a specific catalog and category, with an account context for pricing and eligibility.

```
var req = {
    "searchTerm": "router",
    "selectedCatalog": "<catalog_sys_id>",
    "selectedCategory": "<category_sys_id>",
    "headerContext": {
        "account": "<account_sys_id>"
    }
};

var res = new sn_prd_pm.CatalogSearchAPI().getCatalogData(req);
gs.info(JSON.stringify(res));
```

Output:

```
{
  "selectedCatalogHierarchy": [
    {
      "id": "showAll",
      "label": "Show all",
      "children": {}
    },
    {
      "id": "<catalog_sys_id_1>",
      "label": "Networking",
      "children": []
    },
    {
      "id": "<catalog_sys_id_2>",
      "label": "Internet",
      "children": []
    }
  ],
  "leafCategoryList": "<category_sys_id>",
  "response": [
    {
      "productOfferingSysId": {
        "value": "<product_offering_sys_id_1>",
        "displayValue": "<product_offering_sys_id_1>"
      },
      "code": {
        "value": "ROUTERPRO1",
        "displayValue": "ROUTERPRO1"
      },
      "name": {
        "value": "Pro Router X100",
        "displayValue": "Pro Router X100"
      },
      "description": {
        "value": "High-performance dual-band router for home and business use.",
        "displayValue": "High-performance dual-band router for home and business use."
      },
      "offerType": {
        "value": "simple",
        "displayValue": "simple"
      },
      "pricingMethod": "one_time",
      "uom": {
        "sysId": "<uom_sys_id>",
        "name": "Each"
      },
      "offerTypeVariation": "simple",
      "listPrice": "$150.00",
      "priceList": "<pricelist_sys_id>",
      "derivedPrice": false
    }
  ],
  "count": 1
}
```

### Search using the full parameter set with a complete header context

The following example performs a search request using all available parameters and a complete header context, including explicit pricing, currency, and shipping and billing addresses.

```
var req = {
    "searchTerm": "laptop",
    "selectedCatalog": "<catalog_sys_id>",
    "selectedCategory": "<category_sys_id>",
    "pageIndex": 0,
    "pageLimit": 10,
    "catalogType": "PRODUCT_OFFERING",
    "sortOrder": "descending",
    "sortBy": "score",
    "aiSearchSuggestionId": "",
    "headerContext": {
        "account": "<account_sys_id>",
        "pricelist": "<pricelist_sys_id>",
        "currency": "USD",
        "suppressPricing": false,
        "transaction_date": "2026-01-15 09:00:00",
        "shipping_city": "Chicago",
        "shipping_country": "USA",
        "shipping_location": "<shipping_location_sys_id>",
        "shipping_state": "IL",
        "shipping_street": "123 Main Street, Chicago",
        "shipping_zip": "60601",
        "billing_city": "Chicago",
        "billing_country": "USA",
        "billing_location": "<billing_location_sys_id>",
        "billing_state": "IL",
        "billing_street": "123 Main Street, Chicago",
        "billing_zip": "60601"
    }
};

var res = new sn_prd_pm.CatalogSearchAPI().getCatalogData(req);
gs.info(JSON.stringify(res));
```

Output:

```
{
  "selectedCatalogHierarchy": [
    {
      "id": "showAll",
      "label": "Show all",
      "children": {}
    },
    {
      "id": "<catalog_sys_id_1>",
      "label": "Computers",
      "children": []
    },
    {
      "id": "<catalog_sys_id_2>",
      "label": "Mobile Devices",
      "children": []
    }
  ],
  "leafCategoryList": "<category_sys_id>",
  "response": [
    {
      "productOfferingSysId": {
        "value": "<product_offering_sys_id_1>",
        "displayValue": "<product_offering_sys_id_1>"
      },
      "code": {
        "value": "LAPTOPBIZ15",
        "displayValue": "LAPTOPBIZ15"
      },
      "name": {
        "value": "Business Laptop 15\"",
        "displayValue": "Business Laptop 15\""
      },
      "description": {
        "value": "15-inch business laptop with 16GB RAM and 512GB SSD.",
        "displayValue": "15-inch business laptop with 16GB RAM and 512GB SSD."
      },
      "offerType": {
        "value": "simple",
        "displayValue": "simple"
      },
      "pricingMethod": "one_time",
      "uom": {
        "sysId": "<uom_sys_id>",
        "name": "Each"
      },
      "offerTypeVariation": "simple",
      "listPrice": "$1,200.00",
      "priceList": "<pricelist_sys_id>",
      "derivedPrice": false
    }
  ],
  "count": 1
}
```

### Search for service specifications by keyword

The following example searches for service specifications matching the term `vpn service`.

```
var req = {
    "searchTerm": "vpn service",
    "catalogType": "SERVICE_SPECIFICATION"
};

var res = new sn_prd_pm.CatalogSearchAPI().getCatalogData(req);
gs.info(JSON.stringify(res));
```

Output:

```
{
  "response": [
    {
      "productOfferingSysId": {
        "value": "<product_offering_sys_id_1>",
        "displayValue": "<product_offering_sys_id_1>"
      },
      "code": {
        "value": "MANAGEDVPNSERVICE",
        "displayValue": "MANAGEDVPNSERVICE"
      },
      "name": {
        "value": "Managed VPN Service",
        "displayValue": "Managed VPN Service"
      },
      "description": {
        "value": "Managed VPN Service",
        "displayValue": "Managed VPN Service"
      },
      "offerType": {
        "value": "config",
        "displayValue": "config"
      }
    },
    {
      "productOfferingSysId": {
        "value": "<product_offering_sys_id_2>",
        "displayValue": "<product_offering_sys_id_2>"
      },
      "code": {
        "value": "MANAGEDVPNSERVICEV2",
        "displayValue": "MANAGEDVPNSERVICEV2"
      },
      "name": {
        "value": "Managed VPN Service v2",
        "displayValue": "Managed VPN Service v2"
      },
      "description": {
        "value": "Managed VPN Service",
        "displayValue": "Managed VPN Service"
      },
      "offerType": {
        "value": "config",
        "displayValue": "config"
      }
    }
  ],
  "count": 2
}
```

