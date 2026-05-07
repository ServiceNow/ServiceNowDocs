---
title: Sales CRM Pricing - POST /api/sn\_csm\_pricing/\{api\_version\}/pricingengine/computePrice
description: Enables callers to compute the price of products specified in the request payload. The pricing settings included in the payload determine and control the execution flow of the Pricing Engine, such as whether to apply validations, adjustments, or rollups.
locale: en-US
release: australia
product: REST APIs
classification: rest-apis
topic_type: reference
last_updated: "2019-10-16"
reading_time_minutes: 47
breadcrumb: [Sales CRM Pricing API, REST API reference, API reference, API implementation and reference]
---

# Sales CRM Pricing - POST /api/sn\_csm\_pricing/\{api\_version\}/pricingengine/computePrice

Enables callers to compute the price of products specified in the request payload. The pricing settings included in the payload determine and control the execution flow of the Pricing Engine, such as whether to apply validations, adjustments, or rollups.

## URL format

Versioned URL: `/api/sn_csm_pricing/{api_version}/pricingengine/computePrice`

Default URL: ``

## Supported request parameters

|Name|Description|
|----|-----------|
|None| |

|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

header

</td><td>

Required. Contains transaction-level details, line items, currency, pricelist, and transaction date.Data type: Object

```
{
  "header": {
    "source_system": "String",
    "requesting_record_id": "String",
    "currency": "String",
    "lineItems": [Array],
    "pricelist": "String",
    "transaction_date": "String"
  }
}
```

</td></tr><tr><td>

header.source\_system

</td><td>

Required. The system initiating the request.Data type: String

Example: `ServiceNow REST API`

</td></tr><tr><td>

header.requesting\_record\_id

</td><td>

Required. Unique identifier for this request.Data type: String

Example: `QT0001101`

</td></tr><tr><td>

header.currency

</td><td>

Required. Currency code for pricing. Supports only ServiceNow currencies.Data type: String

Example: `USD`

</td></tr><tr><td>

header.transaction\_date

</td><td>

Required. The date and time of the transaction.Format: Format: glide\_date\_time value, such as `yyyy-MM-dd HH:mm:ss`

Data type: datetime

Example: `2023-12-18 23:37:11`

</td></tr><tr><td>

header.pricelist

</td><td>

Required. The default pricelist ID to use for the transaction.Data type: String

Example: `19d29513d0e63110f8770dbf976be122`

</td></tr><tr><td>

header.lineItems

</td><td>

Required. Array of line-item objects detailing products, quantities, and pricing info.```
{
    "lineItems": [
        {
            "line_id": "String",
            "pricelist": "String",
            "product_offering": "String",
            "periodicity": "String",
            "quantity": "String",
            "unit_of_measure": "String",
            "transaction_date": "String",
            "account_tier": "String",
            "selected": "Boolean",
            "top_product_offer": "String",
            "parent_product_offer": "String",
            "settings": {Object}
        }
    ]
}

```

</td></tr><tr><td>

header.lineItems\[\].line\_id

</td><td>

Required. Unique identifier for this line item.Data type: String

Example: `CONNECTEDC1100`

</td></tr><tr><td>

header.lineItems\[\].pricelist

</td><td>

Required. Pricelist ID for this line item.Data type: String

Example: `19d29513d0e63110f8770dbf976be122`

</td></tr><tr><td>

header.lineItems\[\].product\_offering

</td><td>

Required. Product offering ID for this line item.Data type: String

Example: `db61dd9fd0a63110f8770dbf976be19c`

</td></tr><tr><td>

header.lineItems\[\].periodicity

</td><td>

Identifies the frequency. Possible values are `monthly`, `annually`, or null/undefined.Data type: String

Example: `monthly`

</td></tr><tr><td>

header.lineItems\[\].quantity

</td><td>

Required. Quantity of the product.Data type: String

Example: `1`

</td></tr><tr><td>

header.lineItems\[\].unit\_of\_measure

</td><td>

Required. Unit of measure ID.Data type: String

Example: `cb2795d553020110286eddeeff7b12ff`

</td></tr><tr><td>

header.lineItems\[\].transaction\_date

</td><td>

Required. Date of the transaction specific to this line item.Format: glide\_date\_time value

Data type: datetime

Example: `2023-12-18 23:37:11`

</td></tr><tr><td>

header.lineItems\[\].account\_tier

</td><td>

Optional account tier \(e.g., "gold"\) for pricing logic. If account\_tier is a context variable used in rule matrices.Data type: String

</td></tr><tr><td>

header.lineItems\[\].selected

</td><td>

Indicates if the line item is selected in a configurator scenario. Only applicable for child lines in bundle.Data type: Boolean

Example: `true`

</td></tr><tr><td>

header.lineItems\[\].top\_product\_offer

</td><td>

Identifier for top-level product in a configuration bundle.Data type: String

Example: `db61dd9fd0a63110f8770dbf976be19c`

</td></tr><tr><td>

header.lineItems\[\].parent\_product\_offer

</td><td>

Identifier for the parent product in a bundle line item.Data type: String

Example: `26d07c3211707110f877366201dea60c`

</td></tr><tr><td>

settings

</td><td>

Required. Contains pricing engine settings and options.Data type: Object

```
{
  "settings": {
    "pricing_elements": "String",
    "disable_validation": boolean
  }
}
```

</td></tr><tr><td>

settings.pricing\_elements

</td><td>

Required. Comma-separated list of elements to return.Data type: String

Example: `PRICE,COST,NET_PRICE,LINE_ROLLUPS,HEADER_ROLLUPS,ADJUSTMENTS`

</td></tr><tr><td>

settings.disable\_validation

</td><td>

Whether to disable validation checks on request.Data type: Boolean

Example: `true`

</td></tr><tr><td>

settings.config\_lines\_expanded

</td><td>

Indicates if all the lines for bundle are sent on the request. At this moment, for configurator we expect all lines to be sent for every pricing call coming from configurator.Data type: Boolean

Example: `true`

</td></tr><tr><td>

settings.scope

</td><td>

Scope of pricing.Data type: String

Example: `configurator`

</td></tr><tr><td>

settings.config\_top\_line\_identifier

</td><td>

The line ID of the top-level product in configuration.Data type: String

Example: `HOMEAUTOMA2000`

</td></tr><tr><td>

settings.use\_external\_code

</td><td>

Indicates if the system performs external code lookup.Data type: Boolean

Example: `true`

</td></tr></tbody>
</table>## Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](../concept/c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-entry-RESTAPI">

Data format of the response body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

## Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](../concept/c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|

## Response body parameters \(JSON or XML\)

<table id="table_twx_l3t_ygc"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

header.currency

</td><td>

Currency code used in the pricing response. Similar to the one sent in the request.Data type: String

Example: `USD`

</td></tr><tr><td>

header.costbook

</td><td>

Identifier of the costbook used for pricing.Data type: String \(Sys\_id\)

</td></tr><tr><td>

header.lineItems

</td><td>

Contains pricing details for each line item.Data type: Array&lt;Object&gt;

```
{
  "lineItems": [
    {
      "line_id": "String",
      "status": "String",
      "currency": "String",
      "base_price": {
        "value": "String",
        "displayValue": "String"
      },
      "list_price": {
        "value": "String",
        "displayValue": "String"
      },
      "pricelist": "String",
      "quantity": "",
      "price_list_line": "String",
      "product_offering": "String",
      "one_time_price": {
        "value": "String",
        "displayValue": "String"
      },
      "monthly_recurring_price": {
        "value": "String",
        "displayValue": "String"
      },
      "annual_recurring_price": {
        "value": "String",
        "displayValue": "String"
      },
      "unit_net_price": {
        "value": "String",
        "displayValue": "String"
      },
      "cumulative_net_price": {
        "value": "String",
        "displayValue": "String"
      },
      "cumulative_one_time_price": {
        "value": "String",
        "displayValue": "String"
      },
      "cumulative_monthly_recurring_price": {
        "value": "String",
        "displayValue": "String"
      },
      "cumulative_annual_recurring_price": {
        "value": "String",
        "displayValue": "String"
      },
      "unit_adjustment": {
        "value": "String",
        "displayValue": "String"
      },
      "term_month": {
        "value": Integer,
        "displayValue": Integer
      },
      "cumulative_annual_recurring_price_v1": {
        "value": Integer,
        "displayValue": Integer
      },
      "cumulative_monthly_recurring_price_v1": {
        "value": 0,
        "displayValue": 0
      },
      "total_recurring_price": {
        "value": "String",
        "displayValue": "String"
      },
      "pricingAdjustments": [],
      "total_adjustment_amount": []
    }
  ]
}
```

</td></tr><tr><td>

header.lineItems\[\].line\_id

</td><td>

Identifier of the line item.Data type: String

Example: `CONNECTEDC1100`

</td></tr><tr><td>

header.lineItems\[\].status

</td><td>

Status of the pricing calculation for the line item.Valid options:

-   Success
-   Failure

Data type: String

Example: `Success`

</td></tr><tr><td>

header.lineItems\[\].base\_price

</td><td>

Base price before adjustments.Data type: Object

```
{
  "base_price": {
    "value": "String",
    "displayValue": "String"
  }
}
```

</td></tr><tr><td>

header.lineItems\[\].list\_price

</td><td>

List price which is base price and attribute adjustments included.Data type: Object

```
{
  "list_price": {
    "value": "String",
    "displayValue": "String"
  }
}
```

</td></tr><tr><td>

header.lineItems\[\].pricelist

</td><td>

Price list reference.Data type: String \(Sys\_id\)

</td></tr><tr><td>

header.lineItems\[\].quantity

</td><td>

Quantity sent as part of request.Data type: String

Example: `1`

</td></tr><tr><td>

header.lineItems\[\].price\_list\_line

</td><td>

Price list line reference.Data type: String \(Sys\_id\)

Example: `3e93e785d07a7910f8770dbf976be1ee`

</td></tr><tr><td>

header.lineItems\[\].product\_offering

</td><td>

Product offering reference.Data type: String \(Sys\_id\)

Example: `db61dd9fd0a63110f8770dbf976be19c`

</td></tr><tr><td>

header.lineItems\[\].one\_time\_price

</td><td>

One-time price for the product, unit net price \* quantity.Data type: Object

```
{
  "one_time_price": {
    "value": "String",
    "displayValue": "String"
  }
}
```

</td></tr><tr><td>

header.lineItems\[\].monthly\_recurring\_price

</td><td>

Monthly recurring price for the product inclusive of all quantities.Data type: Object

```
{
  "monthly_recurring_price": {
    "value": Integer,
    "displayValue": Integer
  }
}
```

</td></tr><tr><td>

header.lineItems\[\].annual\_recurring\_price

</td><td>

Annual recurring price for the product inclusive of all quantities.Data type: Object

```
{
  "annual_recurring_price": {
    "value": "String",
    "displayValue": "String"
  }
}
```

</td></tr><tr><td>

header.lineItems\[\].unit\_net\_price

</td><td>

Net price per unit after auto adjustments.Data type: Object

```
{
  "unit_net_price": {
    "value": "String",
    "displayValue": "String"
  }
}
```

</td></tr><tr><td>

header.lineItems\[\].cumulative\_net\_price

</td><td>

\[One time price + \(Monthly Recurring price \* Term\)\] + \(if parent line\) sum of all CNP for immediate and grand child linesData type: Object

```
{
  "cumulative_net_price": {
    "value": "String",
    "displayValue": "String"
  }
}
```

</td></tr><tr><td>

header.lineItems\[\].cumulative\_one\_time\_price

</td><td>

For Child- One time price for the line item. For Parent line item - One time price for the line item + One time price for all child and grand child line items.Data type: Object

```
{
  "cumulative_one_time_price": {
    "value": "String",
    "displayValue": "String"
  }
}
```

</td></tr><tr><td>

header.lineItems\[\].cumulative\_monthly\_recurring\_price

</td><td>

If price method = recurring. Monthly Recurring price for the line + \(if parent line\) sum of all monthly recurring price of child lines.Data type: Object

```
{
  "cumulative_monthly_recurring_price": {
    "value": "String",
    "displayValue": "String"
  }
}
```

</td></tr><tr><td>

header.lineItems\[\].cumulative\_annual\_recurring\_price

</td><td>

If price method = recurring. Cumulative Monthly Recurring Price \* 12.Data type: Object

```
{
  "cumulative_annual_recurring_price": {
    "value": "String",
    "displayValue": "String"
  }
}
```

</td></tr><tr><td>

header.lineItems\[\].unit\_adjustment

</td><td>

Price adjustment applied per unit.Data type: Object

```
{
  "unit_adjustment": {
    "value": "String",
    "displayValue": "String"
  }
}
```

</td></tr><tr><td>

header.lineItems\[\].term\_month

</td><td>

Term duration in months.Data type: Object

```
{
  "term_month": {
    "value": Integer,
    "displayValue": Integer
  }
}
```

</td></tr><tr><td>

header.lineItems\[\].cost

</td><td>

Unit cost of the product.Data type: Object

```
{
  "cost": {
    "value": Integer,
    "displayValue": Integer
  }
}
```

</td></tr><tr><td>

header.lineItems\[\].unit\_margin\_amount

</td><td>

Profit margin amount per unit.Data type: Object

```
{
  "cost": {
    "value": Integer,
    "displayValue": Integer
  }
}
```

</td></tr><tr><td>

header.lineItems\[\].unit\_margin\_percentage

</td><td>

Profit margin percentage per unit.Data type: Object

</td></tr><tr><td>

header.lineItems\[\].one\_time\_cost

</td><td>

One-time cost for the product inclusive of all quantities.Data type: Object

</td></tr><tr><td>

header.lineItems\[\].monthly\_recurring\_cost

</td><td>

Monthly recurring cost for the product inclusive of all quantities.Data type: Object

</td></tr><tr><td>

header.lineItems\[\].cumulative\_one\_time\_cost

</td><td>

For Child- One time cost for the line item. For Parent line item - One time cost for the line item + One time cost for all child and grand child line items.Data type: Object

</td></tr><tr><td>

header.lineItems\[\].cumulative\_monthly\_recurring\_cost

</td><td>

If price method = recurring. Monthly Recurring cost for the line + \(if parent line\) sum of all monthly recurring cost of child lines.Data type: Object

</td></tr><tr><td>

header.lineItems\[\].cumulative\_net\_cost

</td><td>

\[One time cost + \(Monthly Recurring cost \* Term\)\] + \(if parent line\) sum of all CNC for immediate and grand child linesData type: Object

</td></tr><tr><td>

header.lineItems\[\].cumulative\_margin\_percentage

</td><td>

Overall margin percentage.Data type: Object

</td></tr><tr><td>

header.status

</td><td>

Status of the overall pricing request.Valid options are:

-   Success
-   Failure
-   Partial Failure

Data type: String

Example: `Success`

</td></tr><tr><td>

header.total\_monthly\_recurring\_price

</td><td>

Aggregated monthly recurring price.Data type: Object

</td></tr><tr><td>

header.total\_annual\_recurring\_price

</td><td>

Aggregated annual recurring price.Data type: Object

</td></tr><tr><td>

header.total\_amount

</td><td>

Total transaction amount.Data type: Object

</td></tr><tr><td>

header.total\_one\_time\_price

</td><td>

Aggregated one-time price.Data type: Object

</td></tr><tr><td>

header.total\_one\_time\_cost

</td><td>

Aggregated one-time cost.Data type: Object

</td></tr><tr><td>

header.total\_monthly\_cost

</td><td>

Aggregated monthly cost.Data type: Object

</td></tr><tr><td>

header.total\_cost

</td><td>

Total cost \(one-time + recurring\).Data type: Object

</td></tr><tr><td>

header.total\_one\_time\_margin

</td><td>

Total margin from one-time charges.Data type: Object

</td></tr><tr><td>

header.total\_monthly\_margin

</td><td>

Total margin from monthly charges.Data type: Object

</td></tr><tr><td>

header.total\_margin\_amount

</td><td>

Total profit margin amount.Data type: Object

</td></tr><tr><td>

header.total\_one\_time\_margin\_percentage

</td><td>

Margin percentage for one-time charges.Data type: Object

</td></tr><tr><td>

header.total\_monthly\_margin\_percentage

</td><td>

Margin percentage for monthly charges.Data type: Object

</td></tr><tr><td>

header.total\_margin\_percentage

</td><td>

Overall margin percentage.Data type: Object

</td></tr><tr><td>

settings.pricing\_elements

</td><td>

Elements included in the pricing response \(PRICE, COST, NET\_PRICE, etc.\).Data type: String

</td></tr><tr><td>

settings.pricing\_context\_id

</td><td>

Identifier for pricing session when scope is configurator.Data type: String

</td></tr></tbody>
</table>## Example usage

These examples demonstrate basic usage, to include:

-   Calculating a price for a single product
-   Calculate prices for multiple products with header roll-ups
-   Initiate a product configuration session
-   Update a product configuration \(change a characteristic option\)

## Calculate price for a single product

This example demonstrates a basic price calculation for a single product offering. The API is called with one line item, and the request specifies that the PRICE, COST,NET\_PRICE,LINE\_ROLLUPS,HEADER\_ROLLUPS and ADJUSTMENTS should be calculated and returned. This is a foundational request for getting the price of an individual item without any complex configurations or adjustments.

Example: cURL request.

```
curl "https://instance.servicenow.com/api/sn_csm_pricing/v1/pricingengine/computePrice" \
--request POST \
--header "Accept: application/json" \
--header "Content-Type: application/json" \
--data '{
    "header": {
        "source_system": "ServiceNow Headless API",
        "requesting_record_id": "QT0001101",
        "currency": "USD",
        "lineItems": [
            {
                "pricelist": "19d29513d0e63110f8770dbf976be122",
                "product_offering": "db61dd9fd0a63110f8770dbf976be19c",
                "periodicity" : "",
                "quantity": "1",
                "unit_of_measure": "cb2795d553020110286eddeeff7b12ff",
                "transaction_date": "2023-12-18 23:37:11",
                "line_id": "CONNECTEDC1100"
            }
        ],
        "pricelist": "19d29513d0e63110f8770dbf976be122",
        "transaction_date": "2023-12-18 23:37:11"
    },
    "settings": {
        "pricing_elements": "PRICE,COST,NET_PRICE,LINE_ROLLUPS,HEADER_ROLLUPS,ADJUSTMENTS",
        "disable_validation": true
    }
}' \
--user 'username:password'
```

```
{
      "result": {
        "header": {
            "currency": "USD",
            "lineItems": [
                {
                    "line_id": "CONNECTEDC1100",
                    "status": "Success",
                    "currency": "USD",
                    "base_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "list_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "pricelist": "19d29513d0e63110f8770dbf976be122",
                    "quantity": "",
                    "price_list_line": "3e93e785d07a7910f8770dbf976be1ee",
                    "product_offering": "db61dd9fd0a63110f8770dbf976be19c",
                    "one_time_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "monthly_recurring_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "annual_recurring_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "unit_net_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "cumulative_net_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "cumulative_one_time_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "cumulative_monthly_recurring_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "cumulative_annual_recurring_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "unit_adjustment": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "term_month": {
                        "value": 0,
                        "displayValue": 0
                    },
                    "cumulative_annual_recurring_price_v1": {
                        "value": 0,
                        "displayValue": 0
                    },
                    "cumulative_monthly_recurring_price_v1": {
                        "value": 0,
                        "displayValue": 0
                    },
                    "total_recurring_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "pricingAdjustments": [],
                    "total_adjustment_amount": []
                }
            ],
            "status": "Success",
            "total_monthly_recurring_price": {
                "value": "0.0000",
                "displayValue": "$0.00"
            },
            "total_monthly_recurring_price_v1": {
                "value": "0.0000",
                "displayValue": "$0.00"
            },
            "total_annual_recurring_price": {
                "value": "0.0000",
                "displayValue": "$0.00"
            },
            "total_annual_recurring_price_v1": {
                "value": "0.0000",
                "displayValue": "$0.00"
            },
            "total_amount": {
                "value": "0.0000",
                "displayValue": "$0.00"
            },
            "total_amount_v1": {
                "value": "0.0000",
                "displayValue": "$0.00"
            },
            "total_one_time_price": {
                "value": "0.0000",
                "displayValue": "$0.00"
            },
            "total_one_time_cost": {
                "value": "0.0000",
                "displayValue": "$0.00"
            },
            "total_monthly_cost": {
                "value": "0.0000",
                "displayValue": "$0.00"
            },
            "total_cost": {
                "value": "0.0000",
                "displayValue": "$0.00"
            },
            "total_one_time_margin": {
                "value": "0.0000",
                "displayValue": "$0.00"
            },
            "total_monthly_margin": {
                "value": "0.0000",
                "displayValue": "$0.00"
            },
            "total_margin_amount": {
                "value": "0.0000",
                "displayValue": "$0.00"
            },
            "total_one_time_margin_percentage": {
                "value": "0.0000",
                "displayValue": "$0.00"
            },
            "total_monthly_margin_percentage": {
                "value": "0.0000",
                "displayValue": "$0.00"
            },
            "total_margin_percentage": {
                "value": "0.0000",
                "displayValue": "$0.00"
            }
        },
        "settings": {
            "pricing_elements": "PRICE,COST,NET_PRICE,LINE_ROLLUPS,HEADER_ROLLUPS,ADJUSTMENTS"
        }
    }
}
```

## Calculate prices for multiple products with header roll-ups

This example shows how to send a list of multiple, distinct products to be priced in a single transaction. A key difference in this request is the inclusion sending multiple products in same request. This instructs the pricing engine to calculate the individual price for each line item and to compute and return the aggregated totals for the entire request.

Example: cURL request.

```
curl "https://instance.servicenow.com/api/sn_csm_pricing/v1/pricingengine/computePrice" \
--request POST \
--header "Accept: application/json" \
--header "Content-Type: application/json" \
--data '{
    "header": {
        "source_system": "Test Source System",
        "requesting_record_id": "QT0001101",
        "currency": "USD",
        "lineItems": [
            {
                "top_product_offer": "db61dd9fd0a63110f8770dbf976be19c",
                "pricelist": "19d29513d0e63110f8770dbf976be122",
                "product_offering": "db61dd9fd0a63110f8770dbf976be19c",
                "periodicity" : "",
                "quantity": "1",
                "unit_of_measure": "cb2795d553020110286eddeeff7b12ff",
                "transaction_date": "2023-12-18 23:37:11",
                "line_id": "CONNECTEDC1000"
            },
            {
                "top_product_offer": "9b61dd9fd0a63110f8770dbf976be1c6",
                "pricelist": "19d29513d0e63110f8770dbf976be122",
                "product_offering": "9b61dd9fd0a63110f8770dbf976be1c6",
                "periodicity" : "annually",
                "quantity": "1",
                "unit_of_measure": "cb2795d553020110286eddeeff7b12ff",
                "transaction_date": "2023-12-18 23:37:11",
                "line_id": "AUTOCOLLIS1001"
            },
            {
                "top_product_offer": "9361dd9fd0a63110f8770dbf976be1c4",
                "pricelist": "19d29513d0e63110f8770dbf976be122",
                "product_offering": "9361dd9fd0a63110f8770dbf976be1c4",
                "periodicity" : "annually",
                "quantity": "1",
                "unit_of_measure": "cb2795d553020110286eddeeff7b12ff",
                "transaction_date": "2023-12-18 23:37:11",
                "line_id": "WIFIHOTSPOT1002"
            }
        ],
        "pricelist": "19d29513d0e63110f8770dbf976be122",
        "transaction_date": "2023-12-18 23:37:11"
    },
    "settings": {
        "pricing_elements": "PRICE,COST,NET_PRICE,LINE_ROLLUPS,HEADER_ROLLUPS,ADJUSTMENTS",
        "disable_validation": true
    }
}' \
--user 'username:password'
```

```
{
    "result": {
        "header": {
            "currency": "USD",
            "lineItems": [
                {
                    "line_id": "CONNECTEDC1000",
                    "status": "Success",
                    "currency": "USD",
                    "base_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "list_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "pricelist": "19d29513d0e63110f8770dbf976be122",
                    "quantity": "1",
                    "price_list_line": "3e93e785d07a7910f8770dbf976be1ee",
                    "product_offering": "db61dd9fd0a63110f8770dbf976be19c",
                    "top_product_offer": "db61dd9fd0a63110f8770dbf976be19c",
                    "one_time_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "monthly_recurring_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "annual_recurring_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "unit_net_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "cumulative_net_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "cumulative_one_time_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "cumulative_monthly_recurring_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "cumulative_annual_recurring_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "unit_adjustment": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "term_month": {
                        "value": 0,
                        "displayValue": 0
                    },
                    "cumulative_annual_recurring_price_v1": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "cumulative_monthly_recurring_price_v1": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "total_recurring_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "pricingAdjustments": [],
                    "total_adjustment_amount": []
                },
                {
                    "line_id": "AUTOCOLLIS1001",
                    "status": "Success",
                    "currency": "USD",
                    "base_price": {
                        "value": "250.0000",
                        "displayValue": "$250.00"
                    },
                    "list_price": {
                        "value": "250.0000",
                        "displayValue": "$250.00"
                    },
                    "pricelist": "19d29513d0e63110f8770dbf976be122",
                    "quantity": "1",
                    "price_list_line": "4dc32f85d07a7910f8770dbf976be197",
                    "product_offering": "9b61dd9fd0a63110f8770dbf976be1c6",
                    "top_product_offer": "9b61dd9fd0a63110f8770dbf976be1c6",
                    "one_time_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "monthly_recurring_price": {
                        "value": "20.8333",
                        "displayValue": "$20.8333"
                    },
                    "annual_recurring_price": {
                        "value": "250.0000",
                        "displayValue": "$250.00"
                    },
                    "unit_net_price": {
                        "value": "250.0000",
                        "displayValue": "$250.00"
                    },
                    "cumulative_net_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "cumulative_one_time_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "cumulative_monthly_recurring_price": {
                        "value": "20.8333",
                        "displayValue": "$20.8333"
                    },
                    "cumulative_annual_recurring_price": {
                        "value": "250.0000",
                        "displayValue": "$250.00"
                    },
                    "unit_adjustment": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "term_month": {
                        "value": 0,
                        "displayValue": 0
                    },
                    "cumulative_annual_recurring_price_v1": {
                        "value": "250.0000",
                        "displayValue": "$250.00"
                    },
                    "cumulative_monthly_recurring_price_v1": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "total_recurring_price": {
                        "value": "250.0000",
                        "displayValue": "$250.00"
                    },
                    "pricingAdjustments": [],
                    "total_adjustment_amount": []
                },
                {
                    "line_id": "WIFIHOTSPOT1002",
                    "status": "Success",
                    "currency": "USD",
                    "base_price": {
                        "value": "100.0000",
                        "displayValue": "$100.00"
                    },
                    "list_price": {
                        "value": "100.0000",
                        "displayValue": "$100.00"
                    },
                    "pricelist": "19d29513d0e63110f8770dbf976be122",
                    "quantity": "1",
                    "price_list_line": "3ff3ef85d07a7910f8770dbf976be1ea",
                    "product_offering": "9361dd9fd0a63110f8770dbf976be1c4",
                    "top_product_offer": "9361dd9fd0a63110f8770dbf976be1c4",
                    "one_time_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "monthly_recurring_price": {
                        "value": "8.3333",
                        "displayValue": "$8.3333"
                    },
                    "annual_recurring_price": {
                        "value": "100.0000",
                        "displayValue": "$100.00"
                    },
                    "unit_net_price": {
                        "value": "100.0000",
                        "displayValue": "$100.00"
                    },
                    "cumulative_net_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "cumulative_one_time_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "cumulative_monthly_recurring_price": {
                        "value": "8.3333",
                        "displayValue": "$8.3333"
                    },
                    "cumulative_annual_recurring_price": {
                        "value": "100.0000",
                        "displayValue": "$100.00"
                    },
                    "unit_adjustment": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "term_month": {
                        "value": 0,
                        "displayValue": 0
                    },
                    "cumulative_annual_recurring_price_v1": {
                        "value": "100.0000",
                        "displayValue": "$100.00"
                    },
                    "cumulative_monthly_recurring_price_v1": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "total_recurring_price": {
                        "value": "100.0000",
                        "displayValue": "$100.00"
                    },
                    "pricingAdjustments": [],
                    "total_adjustment_amount": []
                }
            ],
            "status": "Success",
            "total_monthly_recurring_price": {
                "value": "29.1666",
                "displayValue": "$29.1666"
            },
            "total_monthly_recurring_price_v1": {
                "value": "0.0000",
                "displayValue": "$0.00"
            },
            "total_annual_recurring_price": {
                "value": "350.0000",
                "displayValue": "$350.00"
            },
            "total_annual_recurring_price_v1": {
                "value": "350.0000",
                "displayValue": "$350.00"
            },
            "total_amount": {
                "value": "0.0000",
                "displayValue": "$0.00"
            },
            "total_amount_v1": {
                "value": "350.0000",
                "displayValue": "$350.00"
            },
            "total_one_time_price": {
                "value": "0.0000",
                "displayValue": "$0.00"
            },
            "total_one_time_cost": {
                "value": "0.0000",
                "displayValue": "$0.00"
            },
            "total_monthly_cost": {
                "value": "0.0000",
                "displayValue": "$0.00"
            },
            "total_cost": {
                "value": "0.0000",
                "displayValue": "$0.00"
            },
            "total_one_time_margin": {
                "value": "0.0000",
                "displayValue": "$0.00"
            },
            "total_monthly_margin": {
                "value": "29.1666",
                "displayValue": "$29.1666"
            },
            "total_margin_amount": {
                "value": "0.0000",
                "displayValue": "$0.00"
            },
            "total_one_time_margin_percentage": {
                "value": "0.0000",
                "displayValue": "$0.00"
            },
            "total_monthly_margin_percentage": {
                "value": "100.0000",
                "displayValue": "$100.00"
            },
            "total_margin_percentage": {
                "value": "0.0000",
                "displayValue": "$0.00"
            }
        },
        "settings": {
            "pricing_elements": "PRICE,COST,NET_PRICE,LINE_ROLLUPS,HEADER_ROLLUPS,ADJUSTMENTS"
        }
    }
}
```

## Initiate a product configuration session

This example demonstrates how to start a stateful product configuration session. This is used for complex products that are sold as a bundle with multiple components and user-selectable options. By setting the scope to "configurator", we tell the pricing engine to create a persistent session. The engine processes the entire product hierarchy, calculates initial prices, and returns a unique pricing\_context\_id.

**Important:** The unique `pricing_context_id` must be captured and sent in all subsequent requests for this configuration \(e.g., when changing a quantity or selecting an option\) to maintain the session's state.

Example: cURL request.

```
curl "https://instance.servicenow.com/api/sn_csm_pricing/v1/pricingengine/computePrice" \
--request POST \
--header "Accept: application/json" \
--header "Content-Type: application/json" \
--data '{
    "header": {
        "source_system": "ServiceNow Headless API",
        "requesting_record_id": "QT0001101",
        "currency": "USD",
        "lineItems": [
            {
                "pricelist": "19d29513d0e63110f8770dbf976be122",
                "product_offering": "26d07c3211707110f877366201dea60c",
                "quantity": "1",
                "top_product_offer": "26d07c3211707110f877366201dea60c",
                "periodicity" : "",
                "unit_of_measure": "cb2795d553020110286eddeeff7b12ff",
                "transaction_date": "2025-08-28 22:46:39",
                "selected": true,
                "line_id": "HOMEAUTOMA2000"
            },
            {
                "parent_product_offer": "26d07c3211707110f877366201dea60c",
                "pricelist": "19d29513d0e63110f8770dbf976be122",
                "product_offering": "fe5d203e11307110f877366201dea631",
                "periodicity" : "",
                "quantity": "3",
                "top_product_offer": "26d07c3211707110f877366201dea60c",
                "unit_of_measure": "cb2795d553020110286eddeeff7b12ff",
                "transaction_date": "2025-08-28 22:46:39",
                "selected": true,
                "line_id": "DOORSENSOR1001"
            },
            {
                "parent_product_offer": "26d07c3211707110f877366201dea60c",
                "pricelist": "19d29513d0e63110f8770dbf976be122",
                "product_offering": "3f6111dfd0a63110f8770dbf976be149",
                "periodicity" : "",
                "quantity": "1",
                "top_product_offer": "26d07c3211707110f877366201dea60c",
                "unit_of_measure": "cb2795d553020110286eddeeff7b12ff",
                "characteristics": [
                    {
                        "characteristic": "4f31999fd0a63110f8770dbf976be178",
                        "characteristic_option": "0b31999fd0a63110f8770dbf976be179"
                    }
                ],
                "transaction_date": "2025-08-28 22:46:39",
                "selected": true,
                "line_id": "HOMEAUTOMA1002"
            },
            {
                "parent_product_offer": "26d07c3211707110f877366201dea60c",
                "pricelist": "19d29513d0e63110f8770dbf976be122",
                "product_offering": "376111dfd0a63110f8770dbf976be140",
                "periodicity" : "monthly",
                "quantity": "1",
                "top_product_offer": "26d07c3211707110f877366201dea60c",
                "unit_of_measure": "cb2795d553020110286eddeeff7b12ff",
                "transaction_date": "2025-08-28 22:46:39",
                "selected": true,
                "line_id": "BASICMONIT1003"
            },
            {
                "parent_product_offer": "26d07c3211707110f877366201dea60c",
                "pricelist": "19d29513d0e63110f8770dbf976be122",
                "product_offering": "e2619d9fd0a63110f8770dbf976be1ec",
                "periodicity" : "monthly",
                "quantity": "1",
                "top_product_offer": "26d07c3211707110f877366201dea60c",
                "unit_of_measure": "cb2795d553020110286eddeeff7b12ff",
                "transaction_date": "2025-08-28 22:46:39",
                "selected": true,
                "line_id": "PREMMONIT2004"
            },
            {
                "parent_product_offer": "26d07c3211707110f877366201dea60c",
                "pricelist": "19d29513d0e63110f8770dbf976be122",
                "product_offering": "3b6111dfd0a63110f8770dbf976be147",
                "periodicity" : "monthly",
                "quantity": "1",
                "top_product_offer": "26d07c3211707110f877366201dea60c",
                "unit_of_measure": "cb2795d553020110286eddeeff7b12ff",
                "transaction_date": "2025-08-28 22:46:39",
                "selected": true,
                "line_id": "ULTIMONIT1005"
            },
            {
                "parent_product_offer": "26d07c3211707110f877366201dea60c",
                "pricelist": "19d29513d0e63110f8770dbf976be122",
                "product_offering": "1761dd9fd0a63110f8770dbf976be196",
                "periodicity" : "",
                "quantity": "1",
                "top_product_offer": "26d07c3211707110f877366201dea60c",
                "unit_of_measure": "cb2795d553020110286eddeeff7b12ff",
                "transaction_date": "2025-08-28 22:46:39",
                "selected": true,
                "line_id": "INDOORCAM1006"
            },
            {
                "parent_product_offer": "26d07c3211707110f877366201dea60c",
                "pricelist": "19d29513d0e63110f8770dbf976be122",
                "product_offering": "6f6111dfd0a63110f8770dbf976be100",
                "periodicity" : "",
                "quantity": "1",
                "top_product_offer": "26d07c3211707110f877366201dea60c",
                "unit_of_measure": "cb2795d553020110286eddeeff7b12ff",
                "transaction_date": "2025-08-28 22:46:39",
                "selected": true,
                "line_id": "OUTCAMERA1007"
            },
            {
                "parent_product_offer": "26d07c3211707110f877366201dea60c",
                "pricelist": "19d29513d0e63110f8770dbf976be122",
                "product_offering": "1b20347e11307110f877366201dea67f",
                "periodicity" : "",
                "quantity": "3",
                "top_product_offer": "26d07c3211707110f877366201dea60c",
                "unit_of_measure": "cb2795d553020110286eddeeff7b12ff",
                "transaction_date": "2025-08-28 22:46:39",
                "selected": true,
                "line_id": "WINSENSOR1008"
            }
        ],
        "pricelist": "19d29513d0e63110f8770dbf976be122",
        "transaction_date": "2023-12-18 23:37:11"
    },
    "settings": {
        "pricing_elements": "PRICE,COST,NET_PRICE,LINE_ROLLUPS,HEADER_ROLLUPS,ADJUSTMENTS",
        "disable_validation": true,
        "scope": "configurator",
        "config_top_line_identifier": "HOMEAUTOMA2000",
        "config_lines_expanded": false
    }
}' \
--user 'username:password'
```

Example response:

The following result shows that the request status is successful.

```
{
    "result": {
        "header": {
            "currency": "USD",
            "lineItems": [
                {
                    "line_id": "HOMEAUTOMA2000",
                    "status": "Success",
                    "currency": "USD",
                    "base_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "list_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "pricelist": "19d29513d0e63110f8770dbf976be122",
                    "quantity": "1",
                    "price_list_line": "d6792b8dd07a7910f8770dbf976be1f8",
                    "product_offering": "26d07c3211707110f877366201dea60c",
                    "top_product_offer": "26d07c3211707110f877366201dea60c",
                    "one_time_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "monthly_recurring_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "annual_recurring_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "unit_net_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "cumulative_net_price": {
                        "value": "200.0000",
                        "displayValue": "$200.00"
                    },
                    "cumulative_one_time_price": {
                        "value": "200.0000",
                        "displayValue": "$200.00"
                    },
                    "cumulative_monthly_recurring_price": {
                        "value": "105.0000",
                        "displayValue": "$105.00"
                    },
                    "cumulative_annual_recurring_price": {
                        "value": "1260.0000",
                        "displayValue": "$1,260.00"
                    },
                    "unit_adjustment": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "term_month": {
                        "value": 0,
                        "displayValue": 0
                    },
                    "cumulative_annual_recurring_price_v1": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "cumulative_monthly_recurring_price_v1": {
                        "value": "105.0000",
                        "displayValue": "$105.00"
                    },
                    "total_recurring_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "pricingAdjustments": [],
                    "total_adjustment_amount": []
                },
                {
                    "line_id": "DOORSENSOR1001",
                    "status": "Success",
                    "currency": "USD",
                    "base_price": {
                        "value": "10.0000",
                        "displayValue": "$10.00"
                    },
                    "list_price": {
                        "value": "10.0000",
                        "displayValue": "$10.00"
                    },
                    "pricelist": "19d29513d0e63110f8770dbf976be122",
                    "quantity": "3",
                    "price_list_line": "2ec2a745d07a7910f8770dbf976be159",
                    "product_offering": "fe5d203e11307110f877366201dea631",
                    "parent_product_offer": "26d07c3211707110f877366201dea60c",
                    "top_product_offer": "26d07c3211707110f877366201dea60c",
                    "one_time_price": {
                        "value": "24.0000",
                        "displayValue": "$24.00"
                    },
                    "monthly_recurring_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "annual_recurring_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "unit_net_price": {
                        "value": "8.0000",
                        "displayValue": "$8.00"
                    },
                    "cumulative_net_price": {
                        "value": "24.0000",
                        "displayValue": "$24.00"
                    },
                    "cumulative_one_time_price": {
                        "value": "24.0000",
                        "displayValue": "$24.00"
                    },
                    "cumulative_monthly_recurring_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "cumulative_annual_recurring_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "unit_adjustment": {
                        "value": "-2.0000",
                        "displayValue": "($2.00)"
                    },
                    "term_month": {
                        "value": 0,
                        "displayValue": 0
                    },
                    "cumulative_annual_recurring_price_v1": {
                        "value": 0,
                        "displayValue": 0
                    },
                    "cumulative_monthly_recurring_price_v1": {
                        "value": 0,
                        "displayValue": 0
                    },
                    "total_recurring_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "pricingAdjustments": [
                        {
                            "adjustment_type": {
                                "value": "a96c83d653dd91105c0eddeeff7b12d8",
                                "displayValue": "MARKDOWN_PER"
                            },
                            "adjustment_value": {
                                "value": 20.0,
                                "displayValue": "20"
                            },
                            "adjustment_amount": {
                                "value": -2.0,
                                "displayValue": "($2.00)"
                            },
                            "adjustment_amount_total": {
                                "value": -6.0,
                                "displayValue": "($6.00)"
                            },
                            "adjustment_description": {
                                "displayValue": "door sensor bundle discount"
                            },
                            "adjustment_sequence_id": {
                                "value": 1.0
                            },
                            "adjustment_matrix_type": {
                                "displayValue": "Configuration Component Price Adjustment"
                            },
                            "adjustment_basis": {
                                "value": "prv_price_point"
                            },
                            "price_point": {
                                "value": "net_price"
                            },
                            "pricing_plan_step": {
                                "value": "97b61272ffe722101fb14ad013cb14d7"
                            },
                            "running_price": {
                                "value": 8.0,
                                "displayValue": "$8.00"
                            }
                        }
                    ],
                    "total_adjustment_amount": [
                        {
                            "pricePoint": "net_price",
                            "value": -6.0,
                            "displayValue": "($6.00)"
                        }
                    ]
                },
                {
                    "line_id": "HOMEAUTOMA1002",
                    "status": "Success",
                    "currency": "USD",
                    "base_price": {
                        "value": "100.0000",
                        "displayValue": "$100.00"
                    },
                    "list_price": {
                        "value": "100.0000",
                        "displayValue": "$100.00"
                    },
                    "pricelist": "19d29513d0e63110f8770dbf976be122",
                    "quantity": "1",
                    "price_list_line": "fe912705d07a7910f8770dbf976be147",
                    "product_offering": "3f6111dfd0a63110f8770dbf976be149",
                    "parent_product_offer": "26d07c3211707110f877366201dea60c",
                    "top_product_offer": "26d07c3211707110f877366201dea60c",
                    "one_time_price": {
                        "value": "80.0000",
                        "displayValue": "$80.00"
                    },
                    "monthly_recurring_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "annual_recurring_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "unit_net_price": {
                        "value": "80.0000",
                        "displayValue": "$80.00"
                    },
                    "cumulative_net_price": {
                        "value": "80.0000",
                        "displayValue": "$80.00"
                    },
                    "cumulative_one_time_price": {
                        "value": "80.0000",
                        "displayValue": "$80.00"
                    },
                    "cumulative_monthly_recurring_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "cumulative_annual_recurring_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "unit_adjustment": {
                        "value": "-20.0000",
                        "displayValue": "($20.00)"
                    },
                    "term_month": {
                        "value": 0,
                        "displayValue": 0
                    },
                    "cumulative_annual_recurring_price_v1": {
                        "value": 0,
                        "displayValue": 0
                    },
                    "cumulative_monthly_recurring_price_v1": {
                        "value": 0,
                        "displayValue": 0
                    },
                    "total_recurring_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "pricingAdjustments": [
                        {
                            "adjustment_type": {
                                "value": "a96c83d653dd91105c0eddeeff7b12d8",
                                "displayValue": "MARKDOWN_PER"
                            },
                            "adjustment_value": {
                                "value": 20.0,
                                "displayValue": "20"
                            },
                            "adjustment_amount": {
                                "value": -20.0,
                                "displayValue": "($20.00)"
                            },
                            "adjustment_amount_total": {
                                "value": -20.0,
                                "displayValue": "($20.00)"
                            },
                            "adjustment_description": {
                                "displayValue": "home automation hub bundle discount"
                            },
                            "adjustment_sequence_id": {
                                "value": 1.0
                            },
                            "adjustment_matrix_type": {
                                "displayValue": "Configuration Component Price Adjustment"
                            },
                            "adjustment_basis": {
                                "value": "prv_price_point"
                            },
                            "price_point": {
                                "value": "net_price"
                            },
                            "pricing_plan_step": {
                                "value": "97b61272ffe722101fb14ad013cb14d7"
                            },
                            "running_price": {
                                "value": 80.0,
                                "displayValue": "$80.00"
                            }
                        }
                    ],
                    "total_adjustment_amount": [
                        {
                            "pricePoint": "net_price",
                            "value": -20.0,
                            "displayValue": "($20.00)"
                        }
                    ]
                },
                {
                    "line_id": "BASICMONIT1003",
                    "status": "Success",
                    "currency": "USD",
                    "base_price": {
                        "value": "30.0000",
                        "displayValue": "$30.00"
                    },
                    "list_price": {
                        "value": "30.0000",
                        "displayValue": "$30.00"
                    },
                    "pricelist": "19d29513d0e63110f8770dbf976be122",
                    "quantity": "1",
                    "price_list_line": "bc53e785d07a7910f8770dbf976be1e7",
                    "product_offering": "376111dfd0a63110f8770dbf976be140",
                    "parent_product_offer": "26d07c3211707110f877366201dea60c",
                    "top_product_offer": "26d07c3211707110f877366201dea60c",
                    "one_time_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "monthly_recurring_price": {
                        "value": "25.0000",
                        "displayValue": "$25.00"
                    },
                    "annual_recurring_price": {
                        "value": "300.0000",
                        "displayValue": "$300.00"
                    },
                    "unit_net_price": {
                        "value": "25.0000",
                        "displayValue": "$25.00"
                    },
                    "cumulative_net_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "cumulative_one_time_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "cumulative_monthly_recurring_price": {
                        "value": "25.0000",
                        "displayValue": "$25.00"
                    },
                    "cumulative_annual_recurring_price": {
                        "value": "300.0000",
                        "displayValue": "$300.00"
                    },
                    "unit_adjustment": {
                        "value": "-5.0000",
                        "displayValue": "($5.00)"
                    },
                    "term_month": {
                        "value": 0,
                        "displayValue": 0
                    },
                    "cumulative_annual_recurring_price_v1": {
                        "value": 0,
                        "displayValue": 0
                    },
                    "cumulative_monthly_recurring_price_v1": {
                        "value": "25.0000",
                        "displayValue": "$25.00"
                    },
                    "total_recurring_price": {
                        "value": "25.0000",
                        "displayValue": "$25.00"
                    },
                    "pricingAdjustments": [
                        {
                            "adjustment_type": {
                                "value": "6e1c03d653dd91105c0eddeeff7b1232",
                                "displayValue": "MARKDOWN_AMT"
                            },
                            "adjustment_value": {
                                "value": 5.0,
                                "displayValue": "5"
                            },
                            "adjustment_amount": {
                                "value": -5.0,
                                "displayValue": "($5.00)"
                            },
                            "adjustment_amount_total": {
                                "value": -5.0,
                                "displayValue": "($5.00)"
                            },
                            "adjustment_description": {
                                "displayValue": "basic monitoring bundle discount"
                            },
                            "adjustment_sequence_id": {
                                "value": 1.0
                            },
                            "adjustment_matrix_type": {
                                "displayValue": "Configuration Component Price Adjustment"
                            },
                            "adjustment_basis": {
                                "value": "prv_price_point"
                            },
                            "price_point": {
                                "value": "net_price"
                            },
                            "pricing_plan_step": {
                                "value": "97b61272ffe722101fb14ad013cb14d7"
                            },
                            "running_price": {
                                "value": 25.0,
                                "displayValue": "$25.00"
                            }
                        }
                    ],
                    "total_adjustment_amount": [
                        {
                            "pricePoint": "net_price",
                            "value": -5.0,
                            "displayValue": "($5.00)"
                        }
                    ]
                },
                {
                    "line_id": "PREMMONIT2004",
                    "status": "Success",
                    "currency": "USD",
                    "base_price": {
                        "value": "40.0000",
                        "displayValue": "$40.00"
                    },
                    "list_price": {
                        "value": "40.0000",
                        "displayValue": "$40.00"
                    },
                    "pricelist": "19d29513d0e63110f8770dbf976be122",
                    "quantity": "1",
                    "price_list_line": "a663a785d07a7910f8770dbf976be115",
                    "product_offering": "e2619d9fd0a63110f8770dbf976be1ec",
                    "parent_product_offer": "26d07c3211707110f877366201dea60c",
                    "top_product_offer": "26d07c3211707110f877366201dea60c",
                    "one_time_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "monthly_recurring_price": {
                        "value": "35.0000",
                        "displayValue": "$35.00"
                    },
                    "annual_recurring_price": {
                        "value": "420.0000",
                        "displayValue": "$420.00"
                    },
                    "unit_net_price": {
                        "value": "35.0000",
                        "displayValue": "$35.00"
                    },
                    "cumulative_net_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "cumulative_one_time_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "cumulative_monthly_recurring_price": {
                        "value": "35.0000",
                        "displayValue": "$35.00"
                    },
                    "cumulative_annual_recurring_price": {
                        "value": "420.0000",
                        "displayValue": "$420.00"
                    },
                    "unit_adjustment": {
                        "value": "-5.0000",
                        "displayValue": "($5.00)"
                    },
                    "term_month": {
                        "value": 0,
                        "displayValue": 0
                    },
                    "cumulative_annual_recurring_price_v1": {
                        "value": 0,
                        "displayValue": 0
                    },
                    "cumulative_monthly_recurring_price_v1": {
                        "value": "35.0000",
                        "displayValue": "$35.00"
                    },
                    "total_recurring_price": {
                        "value": "35.0000",
                        "displayValue": "$35.00"
                    },
                    "pricingAdjustments": [
                        {
                            "adjustment_type": {
                                "value": "6e1c03d653dd91105c0eddeeff7b1232",
                                "displayValue": "MARKDOWN_AMT"
                            },
                            "adjustment_value": {
                                "value": 5.0,
                                "displayValue": "5"
                            },
                            "adjustment_amount": {
                                "value": -5.0,
                                "displayValue": "($5.00)"
                            },
                            "adjustment_amount_total": {
                                "value": -5.0,
                                "displayValue": "($5.00)"
                            },
                            "adjustment_description": {
                                "displayValue": "premium monitoring bundle discount"
                            },
                            "adjustment_sequence_id": {
                                "value": 1.0
                            },
                            "adjustment_matrix_type": {
                                "displayValue": "Configuration Component Price Adjustment"
                            },
                            "adjustment_basis": {
                                "value": "prv_price_point"
                            },
                            "price_point": {
                                "value": "net_price"
                            },
                            "pricing_plan_step": {
                                "value": "97b61272ffe722101fb14ad013cb14d7"
                            },
                            "running_price": {
                                "value": 35.0,
                                "displayValue": "$35.00"
                            }
                        }
                    ],
                    "total_adjustment_amount": [
                        {
                            "pricePoint": "net_price",
                            "value": -5.0,
                            "displayValue": "($5.00)"
                        }
                    ]
                },
                {
                    "line_id": "ULTIMONIT1005",
                    "status": "Success",
                    "currency": "USD",
                    "base_price": {
                        "value": "50.0000",
                        "displayValue": "$50.00"
                    },
                    "list_price": {
                        "value": "50.0000",
                        "displayValue": "$50.00"
                    },
                    "pricelist": "19d29513d0e63110f8770dbf976be122",
                    "quantity": "1",
                    "price_list_line": "72736f85d07a7910f8770dbf976be162",
                    "product_offering": "3b6111dfd0a63110f8770dbf976be147",
                    "parent_product_offer": "26d07c3211707110f877366201dea60c",
                    "top_product_offer": "26d07c3211707110f877366201dea60c",
                    "one_time_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "monthly_recurring_price": {
                        "value": "45.0000",
                        "displayValue": "$45.00"
                    },
                    "annual_recurring_price": {
                        "value": "540.0000",
                        "displayValue": "$540.00"
                    },
                    "unit_net_price": {
                        "value": "45.0000",
                        "displayValue": "$45.00"
                    },
                    "cumulative_net_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "cumulative_one_time_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "cumulative_monthly_recurring_price": {
                        "value": "45.0000",
                        "displayValue": "$45.00"
                    },
                    "cumulative_annual_recurring_price": {
                        "value": "540.0000",
                        "displayValue": "$540.00"
                    },
                    "unit_adjustment": {
                        "value": "-5.0000",
                        "displayValue": "($5.00)"
                    },
                    "term_month": {
                        "value": 0,
                        "displayValue": 0
                    },
                    "cumulative_annual_recurring_price_v1": {
                        "value": 0,
                        "displayValue": 0
                    },
                    "cumulative_monthly_recurring_price_v1": {
                        "value": "45.0000",
                        "displayValue": "$45.00"
                    },
                    "total_recurring_price": {
                        "value": "45.0000",
                        "displayValue": "$45.00"
                    },
                    "pricingAdjustments": [
                        {
                            "adjustment_type": {
                                "value": "6e1c03d653dd91105c0eddeeff7b1232",
                                "displayValue": "MARKDOWN_AMT"
                            },
                            "adjustment_value": {
                                "value": 5.0,
                                "displayValue": "5"
                            },
                            "adjustment_amount": {
                                "value": -5.0,
                                "displayValue": "($5.00)"
                            },
                            "adjustment_amount_total": {
                                "value": -5.0,
                                "displayValue": "($5.00)"
                            },
                            "adjustment_description": {
                                "displayValue": "ultimate monitoring bundle discount"
                            },
                            "adjustment_sequence_id": {
                                "value": 1.0
                            },
                            "adjustment_matrix_type": {
                                "displayValue": "Configuration Component Price Adjustment"
                            },
                            "adjustment_basis": {
                                "value": "prv_price_point"
                            },
                            "price_point": {
                                "value": "net_price"
                            },
                            "pricing_plan_step": {
                                "value": "97b61272ffe722101fb14ad013cb14d7"
                            },
                            "running_price": {
                                "value": 45.0,
                                "displayValue": "$45.00"
                            }
                        }
                    ],
                    "total_adjustment_amount": [
                        {
                            "pricePoint": "net_price",
                            "value": -5.0,
                            "displayValue": "($5.00)"
                        }
                    ]
                },
                {
                    "line_id": "INDOORCAM1006",
                    "status": "Success",
                    "currency": "USD",
                    "base_price": {
                        "value": "35.0000",
                        "displayValue": "$35.00"
                    },
                    "list_price": {
                        "value": "35.0000",
                        "displayValue": "$35.00"
                    },
                    "pricelist": "19d29513d0e63110f8770dbf976be122",
                    "quantity": "1",
                    "price_list_line": "81332f45d07a7910f8770dbf976be14e",
                    "product_offering": "1761dd9fd0a63110f8770dbf976be196",
                    "parent_product_offer": "26d07c3211707110f877366201dea60c",
                    "top_product_offer": "26d07c3211707110f877366201dea60c",
                    "one_time_price": {
                        "value": "28.0000",
                        "displayValue": "$28.00"
                    },
                    "monthly_recurring_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "annual_recurring_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "unit_net_price": {
                        "value": "28.0000",
                        "displayValue": "$28.00"
                    },
                    "cumulative_net_price": {
                        "value": "28.0000",
                        "displayValue": "$28.00"
                    },
                    "cumulative_one_time_price": {
                        "value": "28.0000",
                        "displayValue": "$28.00"
                    },
                    "cumulative_monthly_recurring_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "cumulative_annual_recurring_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "unit_adjustment": {
                        "value": "-7.0000",
                        "displayValue": "($7.00)"
                    },
                    "term_month": {
                        "value": 0,
                        "displayValue": 0
                    },
                    "cumulative_annual_recurring_price_v1": {
                        "value": 0,
                        "displayValue": 0
                    },
                    "cumulative_monthly_recurring_price_v1": {
                        "value": 0,
                        "displayValue": 0
                    },
                    "total_recurring_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "pricingAdjustments": [
                        {
                            "adjustment_type": {
                                "value": "a96c83d653dd91105c0eddeeff7b12d8",
                                "displayValue": "MARKDOWN_PER"
                            },
                            "adjustment_value": {
                                "value": 20.0,
                                "displayValue": "20"
                            },
                            "adjustment_amount": {
                                "value": -7.0,
                                "displayValue": "($7.00)"
                            },
                            "adjustment_amount_total": {
                                "value": -7.0,
                                "displayValue": "($7.00)"
                            },
                            "adjustment_description": {
                                "displayValue": "indoor camera bundle discount"
                            },
                            "adjustment_sequence_id": {
                                "value": 1.0
                            },
                            "adjustment_matrix_type": {
                                "displayValue": "Configuration Component Price Adjustment"
                            },
                            "adjustment_basis": {
                                "value": "prv_price_point"
                            },
                            "price_point": {
                                "value": "net_price"
                            },
                            "pricing_plan_step": {
                                "value": "97b61272ffe722101fb14ad013cb14d7"
                            },
                            "running_price": {
                                "value": 28.0,
                                "displayValue": "$28.00"
                            }
                        }
                    ],
                    "total_adjustment_amount": [
                        {
                            "pricePoint": "net_price",
                            "value": -7.0,
                            "displayValue": "($7.00)"
                        }
                    ]
                },
                {
                    "line_id": "OUTCAMERA1007",
                    "status": "Success",
                    "currency": "USD",
                    "base_price": {
                        "value": "40.0000",
                        "displayValue": "$40.00"
                    },
                    "list_price": {
                        "value": "40.0000",
                        "displayValue": "$40.00"
                    },
                    "pricelist": "19d29513d0e63110f8770dbf976be122",
                    "quantity": "1",
                    "price_list_line": "9a136f45d07a7910f8770dbf976be1b4",
                    "product_offering": "6f6111dfd0a63110f8770dbf976be100",
                    "parent_product_offer": "26d07c3211707110f877366201dea60c",
                    "top_product_offer": "26d07c3211707110f877366201dea60c",
                    "one_time_price": {
                        "value": "32.0000",
                        "displayValue": "$32.00"
                    },
                    "monthly_recurring_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "annual_recurring_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "unit_net_price": {
                        "value": "32.0000",
                        "displayValue": "$32.00"
                    },
                    "cumulative_net_price": {
                        "value": "32.0000",
                        "displayValue": "$32.00"
                    },
                    "cumulative_one_time_price": {
                        "value": "32.0000",
                        "displayValue": "$32.00"
                    },
                    "cumulative_monthly_recurring_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "cumulative_annual_recurring_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "unit_adjustment": {
                        "value": "-8.0000",
                        "displayValue": "($8.00)"
                    },
                    "term_month": {
                        "value": 0,
                        "displayValue": 0
                    },
                    "cumulative_annual_recurring_price_v1": {
                        "value": 0,
                        "displayValue": 0
                    },
                    "cumulative_monthly_recurring_price_v1": {
                        "value": 0,
                        "displayValue": 0
                    },
                    "total_recurring_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "pricingAdjustments": [
                        {
                            "adjustment_type": {
                                "value": "a96c83d653dd91105c0eddeeff7b12d8",
                                "displayValue": "MARKDOWN_PER"
                            },
                            "adjustment_value": {
                                "value": 20.0,
                                "displayValue": "20"
                            },
                            "adjustment_amount": {
                                "value": -8.0,
                                "displayValue": "($8.00)"
                            },
                            "adjustment_amount_total": {
                                "value": -8.0,
                                "displayValue": "($8.00)"
                            },
                            "adjustment_description": {
                                "displayValue": "outdoor camera bundle discount"
                            },
                            "adjustment_sequence_id": {
                                "value": 1.0
                            },
                            "adjustment_matrix_type": {
                                "displayValue": "Configuration Component Price Adjustment"
                            },
                            "adjustment_basis": {
                                "value": "prv_price_point"
                            },
                            "price_point": {
                                "value": "net_price"
                            },
                            "pricing_plan_step": {
                                "value": "97b61272ffe722101fb14ad013cb14d7"
                            },
                            "running_price": {
                                "value": 32.0,
                                "displayValue": "$32.00"
                            }
                        }
                    ],
                    "total_adjustment_amount": [
                        {
                            "pricePoint": "net_price",
                            "value": -8.0,
                            "displayValue": "($8.00)"
                        }
                    ]
                },
                {
                    "line_id": "WINSENSOR1008",
                    "status": "Success",
                    "currency": "USD",
                    "base_price": {
                        "value": "15.0000",
                        "displayValue": "$15.00"
                    },
                    "list_price": {
                        "value": "15.0000",
                        "displayValue": "$15.00"
                    },
                    "pricelist": "19d29513d0e63110f8770dbf976be122",
                    "quantity": "3",
                    "price_list_line": "91f26b45d07a7910f8770dbf976be19b",
                    "product_offering": "1b20347e11307110f877366201dea67f",
                    "parent_product_offer": "26d07c3211707110f877366201dea60c",
                    "top_product_offer": "26d07c3211707110f877366201dea60c",
                    "one_time_price": {
                        "value": "36.0000",
                        "displayValue": "$36.00"
                    },
                    "monthly_recurring_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "annual_recurring_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "unit_net_price": {
                        "value": "12.0000",
                        "displayValue": "$12.00"
                    },
                    "cumulative_net_price": {
                        "value": "36.0000",
                        "displayValue": "$36.00"
                    },
                    "cumulative_one_time_price": {
                        "value": "36.0000",
                        "displayValue": "$36.00"
                    },
                    "cumulative_monthly_recurring_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "cumulative_annual_recurring_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "unit_adjustment": {
                        "value": "-3.0000",
                        "displayValue": "($3.00)"
                    },
                    "term_month": {
                        "value": 0,
                        "displayValue": 0
                    },
                    "cumulative_annual_recurring_price_v1": {
                        "value": 0,
                        "displayValue": 0
                    },
                    "cumulative_monthly_recurring_price_v1": {
                        "value": 0,
                        "displayValue": 0
                    },
                    "total_recurring_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "pricingAdjustments": [
                        {
                            "adjustment_type": {
                                "value": "a96c83d653dd91105c0eddeeff7b12d8",
                                "displayValue": "MARKDOWN_PER"
                            },
                            "adjustment_value": {
                                "value": 20.0,
                                "displayValue": "20"
                            },
                            "adjustment_amount": {
                                "value": -3.0,
                                "displayValue": "($3.00)"
                            },
                            "adjustment_amount_total": {
                                "value": -9.0,
                                "displayValue": "($9.00)"
                            },
                            "adjustment_description": {
                                "displayValue": "window sensor bundle discount"
                            },
                            "adjustment_sequence_id": {
                                "value": 1.0
                            },
                            "adjustment_matrix_type": {
                                "displayValue": "Configuration Component Price Adjustment"
                            },
                            "adjustment_basis": {
                                "value": "prv_price_point"
                            },
                            "price_point": {
                                "value": "net_price"
                            },
                            "pricing_plan_step": {
                                "value": "97b61272ffe722101fb14ad013cb14d7"
                            },
                            "running_price": {
                                "value": 12.0,
                                "displayValue": "$12.00"
                            }
                        }
                    ],
                    "total_adjustment_amount": [
                        {
                            "pricePoint": "net_price",
                            "value": -9.0,
                            "displayValue": "($9.00)"
                        }
                    ]
                }
            ],
            "status": "Success",
            "total_monthly_recurring_price": {
                "value": "105.0000",
                "displayValue": "$105.00"
            },
            "total_monthly_recurring_price_v1": {
                "value": "105.0000",
                "displayValue": "$105.00"
            },
            "total_annual_recurring_price": {
                "value": "1260.0000",
                "displayValue": "$1,260.00"
            },
            "total_annual_recurring_price_v1": {
                "value": "0.0000",
                "displayValue": "$0.00"
            },
            "total_amount": {
                "value": "200.0000",
                "displayValue": "$200.00"
            },
            "total_amount_v1": {
                "value": "305.0000",
                "displayValue": "$305.00"
            },
            "total_one_time_price": {
                "value": "200.0000",
                "displayValue": "$200.00"
            },
            "total_one_time_cost": {
                "value": "0.0000",
                "displayValue": "$0.00"
            },
            "total_monthly_cost": {
                "value": "0.0000",
                "displayValue": "$0.00"
            },
            "total_cost": {
                "value": "0.0000",
                "displayValue": "$0.00"
            },
            "total_one_time_margin": {
                "value": "200.0000",
                "displayValue": "$200.00"
            },
            "total_monthly_margin": {
                "value": "105.0000",
                "displayValue": "$105.00"
            },
            "total_margin_amount": {
                "value": "200.0000",
                "displayValue": "$200.00"
            },
            "total_one_time_margin_percentage": {
                "value": "100.0000",
                "displayValue": "$100.00"
            },
            "total_monthly_margin_percentage": {
                "value": "100.0000",
                "displayValue": "$100.00"
            },
            "total_margin_percentage": {
                "value": "100.0000",
                "displayValue": "$100.00"
            }
        },
        "settings": {
            "pricing_context_id": "7049E245A667EABB226B16A2190FB92E",
            "pricing_elements": "PRICE,COST,NET_PRICE,LINE_ROLLUPS,HEADER_ROLLUPS,ADJUSTMENTS"
        }
    }
}
```

## Update a product configuration \(change a characteristic option\)

This example demonstrates how to update an active product configuration session by changing a user-selectable option \(characteristic\). This is a common action in a product configurator, such as changing a color, size, or feature.

Prerequisite: You need to include the `pricing_context_id` that is returned when initiating a [product configuration session](sales_crm_pricing-POST-compute-price.md#example_zbg_2jt_ygc). This tells the pricing engine which session to update.

Note: The lineItems array only needs to contain the specific item that is being modified, it is not necessary to send the entire product hierarchy again.

Example: cURL request.

```
curl "https://instance.servicenow.com/api/sn_csm_pricing/v1/pricingengine/computePrice" \
--request POST \
--header "Accept: application/json" \
--header "Content-Type: application/json" \
--data '{
    "header": {
        "source_system": "ServiceNow Headless API",
        "requesting_record_id": "QT0001101",
        "currency": "USD",
        "lineItems": [
            {
                "parent_product_offer": "26d07c3211707110f877366201dea60c",
                "pricelist": "19d29513d0e63110f8770dbf976be122",
                "product_offering": "3f6111dfd0a63110f8770dbf976be149",
                "periodicity": "",
                "quantity": "1",
                "top_product_offer": "26d07c3211707110f877366201dea60c",
                "unit_of_measure": "cb2795d553020110286eddeeff7b12ff",
                "characteristics": [
                    {
                        "characteristic": "4f31999fd0a63110f8770dbf976be178",
                        "characteristic_option": "8331999fd0a63110f8770dbf976be179"
                    }
                ],
                "transaction_date": "2025-08-28 22:46:39",
                "selected": true,
                "line_id": "HOMEAUTOMA1002"
            }
        ],
        "pricelist": "19d29513d0e63110f8770dbf976be122",
        "transaction_date": "2023-12-18 23:37:11"
    },
    "settings": {
        "pricing_elements": "PRICE,COST,NET_PRICE,LINE_ROLLUPS,HEADER_ROLLUPS,ADJUSTMENTS",
        "pricing_context_id": "7049E245A667EABB226B16A2190FB92E",
        "disable_validation": true,
        "scope": "configurator",
        "config_top_line_identifier": "HOMEAUTOMA2000",
        "config_lines_expanded": false
    }
}' \
--user 'username:password'
```

```
{
    "result": {
        "header": {
            "currency": "USD",
            "lineItems": [
                {
                    "line_id": "HOMEAUTOMA1002",
                    "status": "Success",
                    "currency": "USD",
                    "base_price": {
                        "value": "100.0000",
                        "displayValue": "$100.00"
                    },
                    "list_price": {
                        "value": "120.0000",
                        "displayValue": "$120.00"
                    },
                    "pricelist": "19d29513d0e63110f8770dbf976be122",
                    "quantity": "1",
                    "price_list_line": "fe912705d07a7910f8770dbf976be147",
                    "product_offering": "3f6111dfd0a63110f8770dbf976be149",
                    "parent_product_offer": "26d07c3211707110f877366201dea60c",
                    "top_product_offer": "26d07c3211707110f877366201dea60c",
                    "one_time_price": {
                        "value": "96.0000",
                        "displayValue": "$96.00"
                    },
                    "monthly_recurring_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "annual_recurring_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "unit_net_price": {
                        "value": "96.0000",
                        "displayValue": "$96.00"
                    },
                    "cumulative_net_price": {
                        "value": "96.0000",
                        "displayValue": "$96.00"
                    },
                    "cumulative_one_time_price": {
                        "value": "96.0000",
                        "displayValue": "$96.00"
                    },
                    "cumulative_monthly_recurring_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "cumulative_annual_recurring_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "unit_adjustment": {
                        "value": "-24.0000",
                        "displayValue": "($24.00)"
                    },
                    "term_month": {
                        "value": 0,
                        "displayValue": 0
                    },
                    "cumulative_annual_recurring_price_v1": {
                        "value": 0,
                        "displayValue": 0
                    },
                    "cumulative_monthly_recurring_price_v1": {
                        "value": 0,
                        "displayValue": 0
                    },
                    "total_recurring_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "pricingAdjustments": [
                        {
                            "adjustment_type": {
                                "value": "d88bc79653dd91105c0eddeeff7b12c1",
                                "displayValue": "MARKUP_AMT"
                            },
                            "adjustment_value": {
                                "value": 20.0,
                                "displayValue": "$20.00"
                            },
                            "adjustment_amount": {
                                "value": 20.0,
                                "displayValue": "$20.00"
                            },
                            "adjustment_amount_total": {
                                "value": 20.0,
                                "displayValue": "$20.00"
                            },
                            "adjustment_description": {
                                "displayValue": "Attribute Adjustments"
                            },
                            "adjustment_sequence_id": {
                                "value": 1.0
                            },
                            "adjustment_matrix_type": {
                                "displayValue": null
                            },
                            "adjustment_basis": {
                                "value": null
                            },
                            "price_point": {
                                "value": "list_price"
                            },
                            "pricing_plan_step": {
                                "value": "8bb61272ffe722101fb14ad013cb149d"
                            },
                            "running_price": {
                                "value": 120.0,
                                "displayValue": "$120.00"
                            }
                        },
                        {
                            "adjustment_type": {
                                "value": "a96c83d653dd91105c0eddeeff7b12d8",
                                "displayValue": "MARKDOWN_PER"
                            },
                            "adjustment_value": {
                                "value": 20.0,
                                "displayValue": "20"
                            },
                            "adjustment_amount": {
                                "value": -24.0,
                                "displayValue": "($24.00)"
                            },
                            "adjustment_amount_total": {
                                "value": -24.0,
                                "displayValue": "($24.00)"
                            },
                            "adjustment_description": {
                                "displayValue": "home automation hub bundle discount"
                            },
                            "adjustment_sequence_id": {
                                "value": 2.0
                            },
                            "adjustment_matrix_type": {
                                "displayValue": "Configuration Component Price Adjustment"
                            },
                            "adjustment_basis": {
                                "value": "prv_price_point"
                            },
                            "price_point": {
                                "value": "net_price"
                            },
                            "pricing_plan_step": {
                                "value": "97b61272ffe722101fb14ad013cb14d7"
                            },
                            "running_price": {
                                "value": 96.0,
                                "displayValue": "$96.00"
                            }
                        }
                    ],
                    "total_adjustment_amount": [
                        {
                            "pricePoint": "list_price",
                            "value": 20.0,
                            "displayValue": "$20.00"
                        },
                        {
                            "pricePoint": "net_price",
                            "value": -24.0,
                            "displayValue": "($24.00)"
                        }
                    ]
                },
                {
                    "line_id": "HOMEAUTOMA2000",
                    "status": "Success",
                    "currency": "USD",
                    "base_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "list_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "pricelist": "19d29513d0e63110f8770dbf976be122",
                    "quantity": "1",
                    "price_list_line": "d6792b8dd07a7910f8770dbf976be1f8",
                    "product_offering": "26d07c3211707110f877366201dea60c",
                    "top_product_offer": "26d07c3211707110f877366201dea60c",
                    "one_time_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "monthly_recurring_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "annual_recurring_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "unit_net_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "cumulative_net_price": {
                        "value": "216.0000",
                        "displayValue": "$216.00"
                    },
                    "cumulative_one_time_price": {
                        "value": "216.0000",
                        "displayValue": "$216.00"
                    },
                    "cumulative_monthly_recurring_price": {
                        "value": "105.0000",
                        "displayValue": "$105.00"
                    },
                    "cumulative_annual_recurring_price": {
                        "value": "1260.0000",
                        "displayValue": "$1,260.00"
                    },
                    "unit_adjustment": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "term_month": {
                        "value": 0,
                        "displayValue": 0
                    },
                    "cumulative_annual_recurring_price_v1": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "cumulative_monthly_recurring_price_v1": {
                        "value": "105.0000",
                        "displayValue": "$105.00"
                    },
                    "total_recurring_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "pricingAdjustments": [],
                    "total_adjustment_amount": []
                }
            ],
            "status": "Success",
            "total_monthly_recurring_price": {
                "value": "105.0000",
                "displayValue": "$105.00"
            },
            "total_monthly_recurring_price_v1": {
                "value": "105.0000",
                "displayValue": "$105.00"
            },
            "total_annual_recurring_price": {
                "value": "1260.0000",
                "displayValue": "$1,260.00"
            },
            "total_annual_recurring_price_v1": {
                "value": "0.0000",
                "displayValue": "$0.00"
            },
            "total_amount": {
                "value": "216.0000",
                "displayValue": "$216.00"
            },
            "total_amount_v1": {
                "value": "321.0000",
                "displayValue": "$321.00"
            },
            "total_one_time_price": {
                "value": "216.0000",
                "displayValue": "$216.00"
            },
            "total_one_time_cost": {
                "value": "0.0000",
                "displayValue": "$0.00"
            },
            "total_monthly_cost": {
                "value": "0.0000",
                "displayValue": "$0.00"
            },
            "total_cost": {
                "value": "0.0000",
                "displayValue": "$0.00"
            },
            "total_one_time_margin": {
                "value": "216.0000",
                "displayValue": "$216.00"
            },
            "total_monthly_margin": {
                "value": "105.0000",
                "displayValue": "$105.00"
            },
            "total_margin_amount": {
                "value": "216.0000",
                "displayValue": "$216.00"
            },
            "total_one_time_margin_percentage": {
                "value": "100.0000",
                "displayValue": "$100.00"
            },
            "total_monthly_margin_percentage": {
                "value": "100.0000",
                "displayValue": "$100.00"
            },
            "total_margin_percentage": {
                "value": "100.0000",
                "displayValue": "$100.00"
            }
        },
        "settings": {
            "pricing_context_id": "7049E245A667EABB226B16A2190FB92E",
            "pricing_elements": "PRICE,COST,NET_PRICE,LINE_ROLLUPS,HEADER_ROLLUPS,ADJUSTMENTS"
        }
    }
}
```

## Update a product configuration \(deselect a product\)

This example demonstrates how to update an active product configuration by deselecting or removing a product from the bundle. This is achieved by sending a request for the specific line item with its `selected` flag set to `false`.

Just like in the previous use case, this request must include the correct `pricing_context_id` to ensure the change is applied to the correct session. The pricing engine will then recalculate all prices for the entire bundle with that item removed, which may affect overall discounts and roll-ups.

Prerequisite: You need to include the `pricing_context_id` that is returned when initiating a [product configuration session](sales_crm_pricing-POST-compute-price.md). This tells the pricing engine which session to update.

Note: The lineItems array only needs to contain the specific item that is being modified, it is not necessary to send the entire product hierarchy again.

Example: cURL request.

```
curl "https://instance.servicenow.com/api/sn_csm_pricing/v1/pricingengine/computePrice" \ 

--request POST \ 
--header "Accept: application/json" \ 
--header "Content-Type: application/json" \ 
--data '{
    "header": {
        "source_system": "ServiceNow Headless API",
        "requesting_record_id": "QT0001101",
        "currency": "USD",
        "lineItems": [
            {
                "parent_product_offer": "26d07c3211707110f877366201dea60c",
                "pricelist": "19d29513d0e63110f8770dbf976be122",
                "product_offering": "3b6111dfd0a63110f8770dbf976be147",
                "quantity": "1",
                "periodicity": "monthly",
                "top_product_offer": "26d07c3211707110f877366201dea60c",
                "unit_of_measure": "cb2795d553020110286eddeeff7b12ff",
                "transaction_date": "2025-08-28 22:46:39",
                "selected": false,
                "line_id": "ULTIMONIT1005"
            }
        ],
        "pricelist": "19d29513d0e63110f8770dbf976be122",
        "costbook": "a3042cdce405c210f8773750028d6f72",
        "transaction_date": "2023-12-18 23:37:11"
    },
    "settings": {
        "pricing_elements": "PRICE,COST,NET_PRICE,LINE_ROLLUPS,HEADER_ROLLUPS,ADJUSTMENTS",
        "pricing_context_id": "7049E245A667EABB226B16A2190FB92E",
        "disable_validation": true,
        "scope": "configurator",
        "config_top_line_identifier": "HOMEAUTOMA2000",
        "config_lines_expanded": false
    }
}' \ 
--user 'username:password' 
```

```
{
    "result": {
        "header": {
            "currency": "USD",
            "costbook": "a3042cdce405c210f8773750028d6f72",
            "lineItems": [
                {
                    "line_id": "ULTIMONIT1005",
                    "status": "Success",
                    "currency": "USD",
                    "base_price": {
                        "value": "50.0000",
                        "displayValue": "$50.00"
                    },
                    "list_price": {
                        "value": "50.0000",
                        "displayValue": "$50.00"
                    },
                    "pricelist": "19d29513d0e63110f8770dbf976be122",
                    "quantity": "1",
                    "price_list_line": "72736f85d07a7910f8770dbf976be162",
                    "product_offering": "3b6111dfd0a63110f8770dbf976be147",
                    "parent_product_offer": "26d07c3211707110f877366201dea60c",
                    "top_product_offer": "26d07c3211707110f877366201dea60c",
                    "one_time_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "monthly_recurring_price": {
                        "value": "50.0000",
                        "displayValue": "$50.00"
                    },
                    "annual_recurring_price": {
                        "value": "600.0000",
                        "displayValue": "$600.00"
                    },
                    "unit_net_price": {
                        "value": "50.0000",
                        "displayValue": "$50.00"
                    },
                    "cumulative_net_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "cumulative_acv": {
                        "value": "600.0000",
                        "displayValue": "$600.00"
                    },
                    "cumulative_one_time_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "cumulative_monthly_recurring_price": {
                        "value": "50.0000",
                        "displayValue": "$50.00"
                    },
                    "cumulative_annual_recurring_price": {
                        "value": "600.0000",
                        "displayValue": "$600.00"
                    },
                    "unit_adjustment": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "term_month": {
                        "value": 0,
                        "displayValue": 0
                    },
                    "cumulative_annual_recurring_price_v1": {
                        "value": 0,
                        "displayValue": 0
                    },
                    "cumulative_monthly_recurring_price_v1": {
                        "value": "50.0000",
                        "displayValue": "$50.00"
                    },
                    "total_recurring_price": {
                        "value": "50.0000",
                        "displayValue": "$50.00"
                    },
                    "total_new_amount": {
                        "value": 0,
                        "displayValue": null
                    },
                    "total_upsell_downsell_amount": {
                        "value": 0,
                        "displayValue": null
                    },
                    "total_renewal_amount": {
                        "value": 0,
                        "displayValue": null
                    },
                    "pricingAdjustments": [],
                    "total_adjustment_amount": [],
                    "cost": {
                        "value": "25.0000",
                        "displayValue": "$25.00"
                    },
                    "unit_margin_amount": {
                        "value": "25.0000",
                        "displayValue": "$25.00"
                    },
                    "unit_margin_percentage": {
                        "value": "50.0000",
                        "displayValue": "50.0000"
                    },
                    "one_time_cost": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "monthly_recurring_cost": {
                        "value": "25.0000",
                        "displayValue": "$25.00"
                    },
                    "cumulative_one_time_cost": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "cumulative_monthly_recurring_cost": {
                        "value": "25.0000",
                        "displayValue": "$25.00"
                    },
                    "cumulative_net_cost": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "cumulative_margin_percentage": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    }
                },
                {
                    "line_id": "HOMEAUTOMA2000",
                    "status": "Success",
                    "currency": "USD",
                    "base_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "list_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "pricelist": "19d29513d0e63110f8770dbf976be122",
                    "quantity": "1",
                    "price_list_line": "d6792b8dd07a7910f8770dbf976be1f8",
                    "product_offering": "26d07c3211707110f877366201dea60c",
                    "top_product_offer": "26d07c3211707110f877366201dea60c",
                    "one_time_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "monthly_recurring_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "annual_recurring_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "unit_net_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "cumulative_net_price": {
                        "value": "270.0000",
                        "displayValue": "$270.00"
                    },
                    "cumulative_acv": {
                        "value": "270.0000",
                        "displayValue": "$270.00"
                    },
                    "cumulative_one_time_price": {
                        "value": "270.0000",
                        "displayValue": "$270.00"
                    },
                    "cumulative_monthly_recurring_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "cumulative_annual_recurring_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "unit_adjustment": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "term_month": {
                        "value": 0,
                        "displayValue": 0
                    },
                    "cumulative_annual_recurring_price_v1": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "cumulative_monthly_recurring_price_v1": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "total_recurring_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "total_new_amount": {
                        "value": "270.0000",
                        "displayValue": "$270.00"
                    },
                    "total_upsell_downsell_amount": {
                        "value": 0,
                        "displayValue": null
                    },
                    "total_renewal_amount": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "pricingAdjustments": [],
                    "total_adjustment_amount": [],
                    "cost": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "unit_margin_amount": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "unit_margin_percentage": {
                        "value": "0.0000",
                        "displayValue": "0.0000"
                    },
                    "one_time_cost": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "monthly_recurring_cost": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "cumulative_one_time_cost": {
                        "value": "130.0000",
                        "displayValue": "$130.00"
                    },
                    "cumulative_monthly_recurring_cost": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "cumulative_net_cost": {
                        "value": "130.0000",
                        "displayValue": "$130.00"
                    },
                    "cumulative_margin_percentage": {
                        "value": "51.8519",
                        "displayValue": "51.8519"
                    }
                }
            ],
            "status": "Success",
            "total_monthly_recurring_price": {
                "value": "0.0000",
                "displayValue": "$0.00"
            },
            "total_monthly_recurring_price_v1": {
                "value": "0.0000",
                "displayValue": "$0.00"
            },
            "total_annual_recurring_price": {
                "value": "0.0000",
                "displayValue": "$0.00"
            },
            "total_annual_recurring_price_v1": {
                "value": "0.0000",
                "displayValue": "$0.00"
            },
            "total_amount": {
                "value": "270.0000",
                "displayValue": "$270.00"
            },
            "total_acv": {
                "value": "270.0000",
                "displayValue": "$270.00"
            },
            "total_amount_v1": {
                "value": "270.0000",
                "displayValue": "$270.00"
            },
            "total_one_time_price": {
                "value": "270.0000",
                "displayValue": "$270.00"
            },
            "total_one_time_cost": {
                "value": "130.0000",
                "displayValue": "$130.00"
            },
            "total_monthly_cost": {
                "value": "0.0000",
                "displayValue": "$0.00"
            },
            "total_cost": {
                "value": "130.0000",
                "displayValue": "$130.00"
            },
            "total_one_time_margin": {
                "value": "140.0000",
                "displayValue": "$140.00"
            },
            "total_monthly_margin": {
                "value": "0.0000",
                "displayValue": "$0.00"
            },
            "total_margin_amount": {
                "value": "140.0000",
                "displayValue": "$140.00"
            },
            "total_one_time_margin_percentage": {
                "value": "51.8519",
                "displayValue": "$51.8519"
            },
            "total_monthly_margin_percentage": {
                "value": "0.0000",
                "displayValue": "$0.00"
            },
            "total_margin_percentage": {
                "value": "51.8519",
                "displayValue": "$51.8519"
            },
            "total_upsell_downsell_amount": {
                "value": "0.0000",
                "displayValue": "$0.00"
            },
            "total_renewal_amount": {
                "value": "0.0000",
                "displayValue": "$0.00"
            },
            "total_new_amount": {
                "value": "270.0000",
                "displayValue": "$270.00"
            },
            "total_new_amount_acv": {
                "value": "270.0000",
                "displayValue": "$270.00"
            }
        },
        "settings": {
            "pricing_context_id": "7E362E4CEDC0C3F684D346ED7A83D47E",
            "pricing_elements": "PRICE,COST,NET_PRICE,LINE_ROLLUPS,HEADER_ROLLUPS,ADJUSTMENTS"
        }
    }
}
```

## Stateless Pricing for a Multi-Line transaction

This example demonstrates how to price a complete, multi-line transaction in a single API call. The request includes a mix of standalone products and a product bundle.

By including HEADER\_ROLLUPS in the pricing\_elements, the API will calculate the price for each individual line item and also return the aggregated grand total for the entire transaction in the header.

Example: `"pricing_elements": "PRICE,COST,NET_PRICE,LINE_ROLLUPS,HEADER_ROLLUPS,ADJUSTMENTS"`

Example: cURL request.

```
curl "https://instance.servicenow.com/api/sn_csm_pricing/v1/pricingengine/computePrice" \
--request POST \
--header "Accept: application/json" \
--header "Content-Type: application/json" \
--data '{
    "header": {
        "source_system": "ServiceNow Headless API",
        "requesting_record_id": "QT0001101",
        "currency": "USD",
        "lineItems": [
            {
                "top_product_offer": "db61dd9fd0a63110f8770dbf976be19c",
                "pricelist": "19d29513d0e63110f8770dbf976be122",
                "product_offering": "db61dd9fd0a63110f8770dbf976be19c",
                "periodicity" : "",
                "quantity": "1",
                "unit_of_measure": "cb2795d553020110286eddeeff7b12ff",
                "transaction_date": "2023-12-18 23:37:11",
                "line_id": "CONNECTEDC1000"
            },
            {
                "top_product_offer": "9b61dd9fd0a63110f8770dbf976be1c6",
                "pricelist": "19d29513d0e63110f8770dbf976be122",
                "product_offering": "9b61dd9fd0a63110f8770dbf976be1c6",
                "periodicity" : "annually",
                "quantity": "1",
                "unit_of_measure": "cb2795d553020110286eddeeff7b12ff",
                "transaction_date": "2023-12-18 23:37:11",
                "line_id": "AUTOCOLLIS1001"
            },
            {
                "top_product_offer": "9361dd9fd0a63110f8770dbf976be1c4",
                "pricelist": "19d29513d0e63110f8770dbf976be122",
                "product_offering": "9361dd9fd0a63110f8770dbf976be1c4",
                "periodicity" : "annually",
                "quantity": "1",
                "unit_of_measure": "cb2795d553020110286eddeeff7b12ff",
                "transaction_date": "2023-12-18 23:37:11",
                "line_id": "WIFIHOTSPOT1002"
            },
             {
                "pricelist": "19d29513d0e63110f8770dbf976be122",
                "product_offering": "26d07c3211707110f877366201dea60c",
                "quantity": "1",
                "top_product_offer": "26d07c3211707110f877366201dea60c",
                "periodicity" : "",
                "unit_of_measure": "cb2795d553020110286eddeeff7b12ff",
                "transaction_date": "2025-08-28 22:46:39",
                "line_id": "HOMEAUTOMA2000"
            },
            {
                "parent_product_offer": "26d07c3211707110f877366201dea60c",
                "pricelist": "19d29513d0e63110f8770dbf976be122",
                "product_offering": "fe5d203e11307110f877366201dea631",
                "periodicity" : "",
                "quantity": "3",
                "top_product_offer": "26d07c3211707110f877366201dea60c",
                "unit_of_measure": "cb2795d553020110286eddeeff7b12ff",
                "transaction_date": "2025-08-28 22:46:39",
                "line_id": "DOORSENSOR1001"
            },
            {
                "parent_product_offer": "26d07c3211707110f877366201dea60c",
                "pricelist": "19d29513d0e63110f8770dbf976be122",
                "product_offering": "3f6111dfd0a63110f8770dbf976be149",
                "periodicity" : "",
                "quantity": "1",
                "top_product_offer": "26d07c3211707110f877366201dea60c",
                "unit_of_measure": "cb2795d553020110286eddeeff7b12ff",
                "characteristics": [
                    {
                        "characteristic": "4f31999fd0a63110f8770dbf976be178",
                        "characteristic_option": "0b31999fd0a63110f8770dbf976be179"
                    }
                ],
                "transaction_date": "2025-08-28 22:46:39",
                "line_id": "HOMEAUTOMA1002"
            },
            {
                "parent_product_offer": "26d07c3211707110f877366201dea60c",
                "pricelist": "19d29513d0e63110f8770dbf976be122",
                "product_offering": "376111dfd0a63110f8770dbf976be140",
                "periodicity" : "monthly",
                "quantity": "1",
                "top_product_offer": "26d07c3211707110f877366201dea60c",
                "unit_of_measure": "cb2795d553020110286eddeeff7b12ff",
                "transaction_date": "2025-08-28 22:46:39",
                "line_id": "BASICMONIT1003"
            },
            {
                "parent_product_offer": "26d07c3211707110f8770dbf976be122",
                "product_offering": "e2619d9fd0a63110f8770dbf976be1ec",
                "periodicity" : "monthly",
                "quantity": "1",
                "top_product_offer": "26d07c3211707110f877366201dea60c",
                "unit_of_measure": "cb2795d553020110286eddeeff7b12ff",
                "transaction_date": "2025-08-28 22:46:39",
                "line_id": "PREMMONIT2004"
            },
            {
                "parent_product_offer": "26d07c3211707110f877366201dea60c",
                "pricelist": "19d29513d0e63110f8770dbf976be122",
                "product_offering": "1761dd9fd0a63110f8770dbf976be196",
                "periodicity" : "",
                "quantity": "1",
                "top_product_offer": "26d07c3211707110f877366201dea60c",
                "unit_of_measure": "cb2795d553020110286eddeeff7b12ff",
                "transaction_date": "2025-08-28 22:46:39",
                "line_id": "INDOORCAM1006"
            },
            {
                "parent_product_offer": "26d07c3211707110f877366201dea60c",
                "pricelist": "19d29513d0e63110f8770dbf976be122",
                "product_offering": "6f6111dfd0a63110f8770dbf976be100",
                "periodicity" : "",
                "quantity": "1",
                "top_product_offer": "26d07c3211707110f877366201dea60c",
                "unit_of_measure": "cb2795d553020110286eddeeff7b12ff",
                "transaction_date": "2025-08-28 22:46:39",
                "line_id": "OUTCAMERA1007"
            },
            {
                "parent_product_offer": "26d07c3211707110f877366201dea60c",
                "pricelist": "19d29513d0e63110f8770dbf976be122",
                "product_offering": "1b20347e11307110f877366201dea67f",
                "periodicity" : "",
                "quantity": "3",
                "top_product_offer": "26d07c3211707110f877366201dea60c",
                "unit_of_measure": "cb2795d553020110286eddeeff7b12ff",
                "transaction_date": "2025-08-28 22:46:39",
                "line_id": "WINSENSOR1008"
            }
        ],
        "pricelist": "19d29513d0e63110f8770dbf976be122",
        "transaction_date": "2023-12-18 23:37:11"
    },
    "settings": {
        "pricing_elements": "PRICE,COST,NET_PRICE,LINE_ROLLUPS,HEADER_ROLLUPS,ADJUSTMENTS",
        "disable_validation": true
    }
}' \
--user 'username:password'
```

```
{
    "result": {
        "header": {
            "currency": "USD",
            "lineItems": [
                {
                    "line_id": "CONNECTEDC1000",
                    "status": "Success",
                    "currency": "USD",
                    "base_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "list_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "pricelist": "19d29513d0e63110f8770dbf976be122",
                    "quantity": "1",
                    "price_list_line": "3e93e785d07a7910f8770dbf976be1ee",
                    "product_offering": "db61dd9fd0a63110f8770dbf976be19c",
                    "top_product_offer": "db61dd9fd0a63110f8770dbf976be19c",
                    "one_time_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "monthly_recurring_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "annual_recurring_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "unit_net_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "cumulative_net_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "cumulative_one_time_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "cumulative_monthly_recurring_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "cumulative_annual_recurring_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "unit_adjustment": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "term_month": {
                        "value": 0,
                        "displayValue": 0
                    },
                    "cumulative_annual_recurring_price_v1": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "cumulative_monthly_recurring_price_v1": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "total_recurring_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "pricingAdjustments": [],
                    "total_adjustment_amount": []
                },
                {
                    "line_id": "AUTOCOLLIS1001",
                    "status": "Success",
                    "currency": "USD",
                    "base_price": {
                        "value": "250.0000",
                        "displayValue": "$250.00"
                    },
                    "list_price": {
                        "value": "250.0000",
                        "displayValue": "$250.00"
                    },
                    "pricelist": "19d29513d0e63110f8770dbf976be122",
                    "quantity": "1",
                    "price_list_line": "4dc32f85d07a7910f8770dbf976be197",
                    "product_offering": "9b61dd9fd0a63110f8770dbf976be1c6",
                    "top_product_offer": "9b61dd9fd0a63110f8770dbf976be1c6",
                    "one_time_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "monthly_recurring_price": {
                        "value": "20.8333",
                        "displayValue": "$20.8333"
                    },
                    "annual_recurring_price": {
                        "value": "250.0000",
                        "displayValue": "$250.00"
                    },
                    "unit_net_price": {
                        "value": "250.0000",
                        "displayValue": "$250.00"
                    },
                    "cumulative_net_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "cumulative_one_time_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "cumulative_monthly_recurring_price": {
                        "value": "20.8333",
                        "displayValue": "$20.8333"
                    },
                    "cumulative_annual_recurring_price": {
                        "value": "250.0000",
                        "displayValue": "$250.00"
                    },
                    "unit_adjustment": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "term_month": {
                        "value": 0,
                        "displayValue": 0
                    },
                    "cumulative_annual_recurring_price_v1": {
                        "value": "250.0000",
                        "displayValue": "$250.00"
                    },
                    "cumulative_monthly_recurring_price_v1": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "total_recurring_price": {
                        "value": "250.0000",
                        "displayValue": "$250.00"
                    },
                    "pricingAdjustments": [],
                    "total_adjustment_amount": []
                },
                {
                    "line_id": "WIFIHOTSPOT1002",
                    "status": "Success",
                    "currency": "USD",
                    "base_price": {
                        "value": "100.0000",
                        "displayValue": "$100.00"
                    },
                    "list_price": {
                        "value": "100.0000",
                        "displayValue": "$100.00"
                    },
                    "pricelist": "19d29513d0e63110f8770dbf976be122",
                    "quantity": "1",
                    "price_list_line": "3ff3ef85d07a7910f8770dbf976be1ea",
                    "product_offering": "9361dd9fd0a63110f8770dbf976be1c4",
                    "top_product_offer": "9361dd9fd0a63110f8770dbf976be1c4",
                    "one_time_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "monthly_recurring_price": {
                        "value": "8.3333",
                        "displayValue": "$8.3333"
                    },
                    "annual_recurring_price": {
                        "value": "100.0000",
                        "displayValue": "$100.00"
                    },
                    "unit_net_price": {
                        "value": "100.0000",
                        "displayValue": "$100.00"
                    },
                    "cumulative_net_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "cumulative_one_time_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "cumulative_monthly_recurring_price": {
                        "value": "8.3333",
                        "displayValue": "$8.3333"
                    },
                    "cumulative_annual_recurring_price": {
                        "value": "100.0000",
                        "displayValue": "$100.00"
                    },
                    "unit_adjustment": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "term_month": {
                        "value": 0,
                        "displayValue": 0
                    },
                    "cumulative_annual_recurring_price_v1": {
                        "value": "100.0000",
                        "displayValue": "$100.00"
                    },
                    "cumulative_monthly_recurring_price_v1": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "total_recurring_price": {
                        "value": "100.0000",
                        "displayValue": "$100.00"
                    },
                    "pricingAdjustments": [],
                    "total_adjustment_amount": []
                },
                {
                    "line_id": "HOMEAUTOMA2000",
                    "status": "Success",
                    "currency": "USD",
                    "base_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "list_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "pricelist": "19d29513d0e63110f8770dbf976be122",
                    "quantity": "1",
                    "price_list_line": "d6792b8dd07a7910f8770dbf976be1f8",
                    "product_offering": "26d07c3211707110f877366201dea60c",
                    "top_product_offer": "26d07c3211707110f877366201dea60c",
                    "one_time_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "monthly_recurring_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "annual_recurring_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "unit_net_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "cumulative_net_price": {
                        "value": "200.0000",
                        "displayValue": "$200.00"
                    },
                    "cumulative_one_time_price": {
                        "value": "200.0000",
                        "displayValue": "$200.00"
                    },
                    "cumulative_monthly_recurring_price": {
                        "value": "60.0000",
                        "displayValue": "$60.00"
                    },
                    "cumulative_annual_recurring_price": {
                        "value": "720.0000",
                        "displayValue": "$720.00"
                    },
                    "unit_adjustment": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "term_month": {
                        "value": 0,
                        "displayValue": 0
                    },
                    "cumulative_annual_recurring_price_v1": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "cumulative_monthly_recurring_price_v1": {
                        "value": "60.0000",
                        "displayValue": "$60.00"
                    },
                    "total_recurring_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "pricingAdjustments": [],
                    "total_adjustment_amount": []
                },
                {
                    "line_id": "DOORSENSOR1001",
                    "status": "Success",
                    "currency": "USD",
                    "base_price": {
                        "value": "10.0000",
                        "displayValue": "$10.00"
                    },
                    "list_price": {
                        "value": "10.0000",
                        "displayValue": "$10.00"
                    },
                    "pricelist": "19d29513d0e63110f8770dbf976be122",
                    "quantity": "3",
                    "price_list_line": "2ec2a745d07a7910f8770dbf976be159",
                    "product_offering": "fe5d203e11307110f877366201dea631",
                    "parent_product_offer": "26d07c3211707110f877366201dea60c",
                    "top_product_offer": "26d07c3211707110f877366201dea60c",
                    "one_time_price": {
                        "value": "24.0000",
                        "displayValue": "$24.00"
                    },
                    "monthly_recurring_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "annual_recurring_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "unit_net_price": {
                        "value": "8.0000",
                        "displayValue": "$8.00"
                    },
                    "cumulative_net_price": {
                        "value": "24.0000",
                        "displayValue": "$24.00"
                    },
                    "cumulative_one_time_price": {
                        "value": "24.0000",
                        "displayValue": "$24.00"
                    },
                    "cumulative_monthly_recurring_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "cumulative_annual_recurring_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "unit_adjustment": {
                        "value": "-2.0000",
                        "displayValue": "($2.00)"
                    },
                    "term_month": {
                        "value": 0,
                        "displayValue": 0
                    },
                    "cumulative_annual_recurring_price_v1": {
                        "value": 0,
                        "displayValue": 0
                    },
                    "cumulative_monthly_recurring_price_v1": {
                        "value": 0,
                        "displayValue": 0
                    },
                    "total_recurring_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "pricingAdjustments": [
                        {
                            "adjustment_type": {
                                "value": "a96c83d653dd91105c0eddeeff7b12d8",
                                "displayValue": "MARKDOWN_PER"
                            },
                            "adjustment_value": {
                                "value": 20.0,
                                "displayValue": "20"
                            },
                            "adjustment_amount": {
                                "value": -2.0,
                                "displayValue": "($2.00)"
                            },
                            "adjustment_amount_total": {
                                "value": -6.0,
                                "displayValue": "($6.00)"
                            },
                            "adjustment_description": {
                                "displayValue": "door sensor bundle discount"
                            },
                            "adjustment_sequence_id": {
                                "value": 1.0
                            },
                            "adjustment_matrix_type": {
                                "displayValue": "Configuration Component Price Adjustment"
                            },
                            "adjustment_basis": {
                                "value": "prv_price_point"
                            },
                            "price_point": {
                                "value": "net_price"
                            },
                            "pricing_plan_step": {
                                "value": "97b61272ffe722101fb14ad013cb14d7"
                            },
                            "running_price": {
                                "value": 8.0,
                                "displayValue": "$8.00"
                            }
                        }
                    ],
                    "total_adjustment_amount": [
                        {
                            "pricePoint": "net_price",
                            "value": -6.0,
                            "displayValue": "($6.00)"
                        }
                    ]
                },
                {
                    "line_id": "HOMEAUTOMA1002",
                    "status": "Success",
                    "currency": "USD",
                    "base_price": {
                        "value": "100.0000",
                        "displayValue": "$100.00"
                    },
                    "list_price": {
                        "value": "100.0000",
                        "displayValue": "$100.00"
                    },
                    "pricelist": "19d29513d0e63110f8770dbf976be122",
                    "quantity": "1",
                    "price_list_line": "fe912705d07a7910f8770dbf976be147",
                    "product_offering": "3f6111dfd0a63110f8770dbf976be149",
                    "parent_product_offer": "26d07c3211707110f877366201dea60c",
                    "top_product_offer": "26d07c3211707110f877366201dea60c",
                    "one_time_price": {
                        "value": "80.0000",
                        "displayValue": "$80.00"
                    },
                    "monthly_recurring_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "annual_recurring_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "unit_net_price": {
                        "value": "80.0000",
                        "displayValue": "$80.00"
                    },
                    "cumulative_net_price": {
                        "value": "80.0000",
                        "displayValue": "$80.00"
                    },
                    "cumulative_one_time_price": {
                        "value": "80.0000",
                        "displayValue": "$80.00"
                    },
                    "cumulative_monthly_recurring_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "cumulative_annual_recurring_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "unit_adjustment": {
                        "value": "-20.0000",
                        "displayValue": "($20.00)"
                    },
                    "term_month": {
                        "value": 0,
                        "displayValue": 0
                    },
                    "cumulative_annual_recurring_price_v1": {
                        "value": 0,
                        "displayValue": 0
                    },
                    "cumulative_monthly_recurring_price_v1": {
                        "value": 0,
                        "displayValue": 0
                    },
                    "total_recurring_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "pricingAdjustments": [
                        {
                            "adjustment_type": {
                                "value": "a96c83d653dd91105c0eddeeff7b12d8",
                                "displayValue": "MARKDOWN_PER"
                            },
                            "adjustment_value": {
                                "value": 20.0,
                                "displayValue": "20"
                            },
                            "adjustment_amount": {
                                "value": -20.0,
                                "displayValue": "($20.00)"
                            },
                            "adjustment_amount_total": {
                                "value": -20.0,
                                "displayValue": "($20.00)"
                            },
                            "adjustment_description": {
                                "displayValue": "home automation hub bundle discount"
                            },
                            "adjustment_sequence_id": {
                                "value": 1.0
                            },
                            "adjustment_matrix_type": {
                                "displayValue": "Configuration Component Price Adjustment"
                            },
                            "adjustment_basis": {
                                "value": "prv_price_point"
                            },
                            "price_point": {
                                "value": "net_price"
                            },
                            "pricing_plan_step": {
                                "value": "97b61272ffe722101fb14ad013cb14d7"
                            },
                            "running_price": {
                                "value": 80.0,
                                "displayValue": "$80.00"
                            }
                        }
                    ],
                    "total_adjustment_amount": [
                        {
                            "pricePoint": "net_price",
                            "value": -20.0,
                            "displayValue": "($20.00)"
                        }
                    ]
                },
                {
                    "line_id": "BASICMONIT1003",
                    "status": "Success",
                    "currency": "USD",
                    "base_price": {
                        "value": "30.0000",
                        "displayValue": "$30.00"
                    },
                    "list_price": {
                        "value": "30.0000",
                        "displayValue": "$30.00"
                    },
                    "pricelist": "19d29513d0e63110f8770dbf976be122",
                    "quantity": "1",
                    "price_list_line": "bc53e785d07a7910f8770dbf976be1e7",
                    "product_offering": "376111dfd0a63110f8770dbf976be140",
                    "parent_product_offer": "26d07c3211707110f877366201dea60c",
                    "top_product_offer": "26d07c3211707110f877366201dea60c",
                    "one_time_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "monthly_recurring_price": {
                        "value": "25.0000",
                        "displayValue": "$25.00"
                    },
                    "annual_recurring_price": {
                        "value": "300.0000",
                        "displayValue": "$300.00"
                    },
                    "unit_net_price": {
                        "value": "25.0000",
                        "displayValue": "$25.00"
                    },
                    "cumulative_net_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "cumulative_one_time_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "cumulative_monthly_recurring_price": {
                        "value": "25.0000",
                        "displayValue": "$25.00"
                    },
                    "cumulative_annual_recurring_price": {
                        "value": "300.0000",
                        "displayValue": "$300.00"
                    },
                    "unit_adjustment": {
                        "value": "-5.0000",
                        "displayValue": "($5.00)"
                    },
                    "term_month": {
                        "value": 0,
                        "displayValue": 0
                    },
                    "cumulative_annual_recurring_price_v1": {
                        "value": 0,
                        "displayValue": 0
                    },
                    "cumulative_monthly_recurring_price_v1": {
                        "value": "25.0000",
                        "displayValue": "$25.00"
                    },
                    "total_recurring_price": {
                        "value": "25.0000",
                        "displayValue": "$25.00"
                    },
                    "pricingAdjustments": [
                        {
                            "adjustment_type": {
                                "value": "6e1c03d653dd91105c0eddeeff7b1232",
                                "displayValue": "MARKDOWN_AMT"
                            },
                            "adjustment_value": {
                                "value": 5.0,
                                "displayValue": "5"
                            },
                            "adjustment_amount": {
                                "value": -5.0,
                                "displayValue": "($5.00)"
                            },
                            "adjustment_amount_total": {
                                "value": -5.0,
                                "displayValue": "($5.00)"
                            },
                            "adjustment_description": {
                                "displayValue": "basic monitoring bundle discount"
                            },
                            "adjustment_sequence_id": {
                                "value": 1.0
                            },
                            "adjustment_matrix_type": {
                                "displayValue": "Configuration Component Price Adjustment"
                            },
                            "adjustment_basis": {
                                "value": "prv_price_point"
                            },
                            "price_point": {
                                "value": "net_price"
                            },
                            "pricing_plan_step": {
                                "value": "97b61272ffe722101fb14ad013cb14d7"
                            },
                            "running_price": {
                                "value": 25.0,
                                "displayValue": "$25.00"
                            }
                        }
                    ],
                    "total_adjustment_amount": [
                        {
                            "pricePoint": "net_price",
                            "value": -5.0,
                            "displayValue": "($5.00)"
                        }
                    ]
                },
                {
                    "line_id": "PREMMONIT2004",
                    "status": "Success",
                    "currency": "USD",
                    "base_price": {
                        "value": "40.0000",
                        "displayValue": "$40.00"
                    },
                    "list_price": {
                        "value": "40.0000",
                        "displayValue": "$40.00"
                    },
                    "pricelist": "19d29513d0e63110f8770dbf976be122",
                    "quantity": "1",
                    "price_list_line": "a663a785d07a7910f8770dbf976be115",
                    "product_offering": "e2619d9fd0a63110f8770dbf976be1ec",
                    "parent_product_offer": "26d07c3211707110f877366201dea60c",
                    "top_product_offer": "26d07c3211707110f877366201dea60c",
                    "one_time_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "monthly_recurring_price": {
                        "value": "35.0000",
                        "displayValue": "$35.00"
                    },
                    "annual_recurring_price": {
                        "value": "420.0000",
                        "displayValue": "$420.00"
                    },
                    "unit_net_price": {
                        "value": "35.0000",
                        "displayValue": "$35.00"
                    },
                    "cumulative_net_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "cumulative_one_time_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "cumulative_monthly_recurring_price": {
                        "value": "35.0000",
                        "displayValue": "$35.00"
                    },
                    "cumulative_annual_recurring_price": {
                        "value": "420.0000",
                        "displayValue": "$420.00"
                    },
                    "unit_adjustment": {
                        "value": "-5.0000",
                        "displayValue": "($5.00)"
                    },
                    "term_month": {
                        "value": 0,
                        "displayValue": 0
                    },
                    "cumulative_annual_recurring_price_v1": {
                        "value": 0,
                        "displayValue": 0
                    },
                    "cumulative_monthly_recurring_price_v1": {
                        "value": "35.0000",
                        "displayValue": "$35.00"
                    },
                    "total_recurring_price": {
                        "value": "35.0000",
                        "displayValue": "$35.00"
                    },
                    "pricingAdjustments": [
                        {
                            "adjustment_type": {
                                "value": "6e1c03d653dd91105c0eddeeff7b1232",
                                "displayValue": "MARKDOWN_AMT"
                            },
                            "adjustment_value": {
                                "value": 5.0,
                                "displayValue": "5"
                            },
                            "adjustment_amount": {
                                "value": -5.0,
                                "displayValue": "($5.00)"
                            },
                            "adjustment_amount_total": {
                                "value": -5.0,
                                "displayValue": "($5.00)"
                            },
                            "adjustment_description": {
                                "displayValue": "premium monitoring bundle discount"
                            },
                            "adjustment_sequence_id": {
                                "value": 1.0
                            },
                            "adjustment_matrix_type": {
                                "displayValue": "Configuration Component Price Adjustment"
                            },
                            "adjustment_basis": {
                                "value": "prv_price_point"
                            },
                            "price_point": {
                                "value": "net_price"
                            },
                            "pricing_plan_step": {
                                "value": "97b61272ffe722101fb14ad013cb14d7"
                            },
                            "running_price": {
                                "value": 35.0,
                                "displayValue": "$35.00"
                            }
                        }
                    ],
                    "total_adjustment_amount": [
                        {
                            "pricePoint": "net_price",
                            "value": -5.0,
                            "displayValue": "($5.00)"
                        }
                    ]
                },
                {
                    "line_id": "INDOORCAM1006",
                    "status": "Success",
                    "currency": "USD",
                    "base_price": {
                        "value": "35.0000",
                        "displayValue": "$35.00"
                    },
                    "list_price": {
                        "value": "35.0000",
                        "displayValue": "$35.00"
                    },
                    "pricelist": "19d29513d0e63110f8770dbf976be122",
                    "quantity": "1",
                    "price_list_line": "81332f45d07a7910f8770dbf976be14e",
                    "product_offering": "1761dd9fd0a63110f8770dbf976be196",
                    "parent_product_offer": "26d07c3211707110f877366201dea60c",
                    "top_product_offer": "26d07c3211707110f877366201dea60c",
                    "one_time_price": {
                        "value": "28.0000",
                        "displayValue": "$28.00"
                    },
                    "monthly_recurring_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "annual_recurring_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "unit_net_price": {
                        "value": "28.0000",
                        "displayValue": "$28.00"
                    },
                    "cumulative_net_price": {
                        "value": "28.0000",
                        "displayValue": "$28.00"
                    },
                    "cumulative_one_time_price": {
                        "value": "28.0000",
                        "displayValue": "$28.00"
                    },
                    "cumulative_monthly_recurring_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "cumulative_annual_recurring_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "unit_adjustment": {
                        "value": "-7.0000",
                        "displayValue": "($7.00)"
                    },
                    "term_month": {
                        "value": 0,
                        "displayValue": 0
                    },
                    "cumulative_annual_recurring_price_v1": {
                        "value": 0,
                        "displayValue": 0
                    },
                    "cumulative_monthly_recurring_price_v1": {
                        "value": 0,
                        "displayValue": 0
                    },
                    "total_recurring_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "pricingAdjustments": [
                        {
                            "adjustment_type": {
                                "value": "a96c83d653dd91105c0eddeeff7b12d8",
                                "displayValue": "MARKDOWN_PER"
                            },
                            "adjustment_value": {
                                "value": 20.0,
                                "displayValue": "20"
                            },
                            "adjustment_amount": {
                                "value": -7.0,
                                "displayValue": "($7.00)"
                            },
                            "adjustment_amount_total": {
                                "value": -7.0,
                                "displayValue": "($7.00)"
                            },
                            "adjustment_description": {
                                "displayValue": "indoor camera bundle discount"
                            },
                            "adjustment_sequence_id": {
                                "value": 1.0
                            },
                            "adjustment_matrix_type": {
                                "displayValue": "Configuration Component Price Adjustment"
                            },
                            "adjustment_basis": {
                                "value": "prv_price_point"
                            },
                            "price_point": {
                                "value": "net_price"
                            },
                            "pricing_plan_step": {
                                "value": "97b61272ffe722101fb14ad013cb14d7"
                            },
                            "running_price": {
                                "value": 28.0,
                                "displayValue": "$28.00"
                            }
                        }
                    ],
                    "total_adjustment_amount": [
                        {
                            "pricePoint": "net_price",
                            "value": -7.0,
                            "displayValue": "($7.00)"
                        }
                    ]
                },
                {
                    "line_id": "OUTCAMERA1007",
                    "status": "Success",
                    "currency": "USD",
                    "base_price": {
                        "value": "40.0000",
                        "displayValue": "$40.00"
                    },
                    "list_price": {
                        "value": "40.0000",
                        "displayValue": "$40.00"
                    },
                    "pricelist": "19d29513d0e63110f8770dbf976be122",
                    "quantity": "1",
                    "price_list_line": "9a136f45d07a7910f8770dbf976be1b4",
                    "product_offering": "6f6111dfd0a63110f8770dbf976be100",
                    "parent_product_offer": "26d07c3211707110f877366201dea60c",
                    "top_product_offer": "26d07c3211707110f877366201dea60c",
                    "one_time_price": {
                        "value": "32.0000",
                        "displayValue": "$32.00"
                    },
                    "monthly_recurring_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "annual_recurring_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "unit_net_price": {
                        "value": "32.0000",
                        "displayValue": "$32.00"
                    },
                    "cumulative_net_price": {
                        "value": "32.0000",
                        "displayValue": "$32.00"
                    },
                    "cumulative_one_time_price": {
                        "value": "32.0000",
                        "displayValue": "$32.00"
                    },
                    "cumulative_monthly_recurring_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "cumulative_annual_recurring_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "unit_adjustment": {
                        "value": "-8.0000",
                        "displayValue": "($8.00)"
                    },
                    "term_month": {
                        "value": 0,
                        "displayValue": 0
                    },
                    "cumulative_annual_recurring_price_v1": {
                        "value": 0,
                        "displayValue": 0
                    },
                    "cumulative_monthly_recurring_price_v1": {
                        "value": 0,
                        "displayValue": 0
                    },
                    "total_recurring_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "pricingAdjustments": [
                        {
                            "adjustment_type": {
                                "value": "a96c83d653dd91105c0eddeeff7b12d8",
                                "displayValue": "MARKDOWN_PER"
                            },
                            "adjustment_value": {
                                "value": 20.0,
                                "displayValue": "20"
                            },
                            "adjustment_amount": {
                                "value": -8.0,
                                "displayValue": "($8.00)"
                            },
                            "adjustment_amount_total": {
                                "value": -8.0,
                                "displayValue": "($8.00)"
                            },
                            "adjustment_description": {
                                "displayValue": "outdoor camera bundle discount"
                            },
                            "adjustment_sequence_id": {
                                "value": 1.0
                            },
                            "adjustment_matrix_type": {
                                "displayValue": "Configuration Component Price Adjustment"
                            },
                            "adjustment_basis": {
                                "value": "prv_price_point"
                            },
                            "price_point": {
                                "value": "net_price"
                            },
                            "pricing_plan_step": {
                                "value": "97b61272ffe722101fb14ad013cb14d7"
                            },
                            "running_price": {
                                "value": 32.0,
                                "displayValue": "$32.00"
                            }
                        }
                    ],
                    "total_adjustment_amount": [
                        {
                            "pricePoint": "net_price",
                            "value": -8.0,
                            "displayValue": "($8.00)"
                        }
                    ]
                },
                {
                    "line_id": "WINSENSOR1008",
                    "status": "Success",
                    "currency": "USD",
                    "base_price": {
                        "value": "15.0000",
                        "displayValue": "$15.00"
                    },
                    "list_price": {
                        "value": "15.0000",
                        "displayValue": "$15.00"
                    },
                    "pricelist": "19d29513d0e63110f8770dbf976be122",
                    "quantity": "3",
                    "price_list_line": "91f26b45d07a7910f8770dbf976be19b",
                    "product_offering": "1b20347e11307110f877366201dea67f",
                    "parent_product_offer": "26d07c3211707110f877366201dea60c",
                    "top_product_offer": "26d07c3211707110f877366201dea60c",
                    "one_time_price": {
                        "value": "36.0000",
                        "displayValue": "$36.00"
                    },
                    "monthly_recurring_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "annual_recurring_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "unit_net_price": {
                        "value": "12.0000",
                        "displayValue": "$12.00"
                    },
                    "cumulative_net_price": {
                        "value": "36.0000",
                        "displayValue": "$36.00"
                    },
                    "cumulative_one_time_price": {
                        "value": "36.0000",
                        "displayValue": "$36.00"
                    },
                    "cumulative_monthly_recurring_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "cumulative_annual_recurring_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "unit_adjustment": {
                        "value": "-3.0000",
                        "displayValue": "($3.00)"
                    },
                    "term_month": {
                        "value": 0,
                        "displayValue": 0
                    },
                    "cumulative_annual_recurring_price_v1": {
                        "value": 0,
                        "displayValue": 0
                    },
                    "cumulative_monthly_recurring_price_v1": {
                        "value": 0,
                        "displayValue": 0
                    },
                    "total_recurring_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "pricingAdjustments": [
                        {
                            "adjustment_type": {
                                "value": "a96c83d653dd91105c0eddeeff7b12d8",
                                "displayValue": "MARKDOWN_PER"
                            },
                            "adjustment_value": {
                                "value": 20.0,
                                "displayValue": "20"
                            },
                            "adjustment_amount": {
                                "value": -3.0,
                                "displayValue": "($3.00)"
                            },
                            "adjustment_amount_total": {
                                "value": -9.0,
                                "displayValue": "($9.00)"
                            },
                            "adjustment_description": {
                                "displayValue": "window sensor bundle discount"
                            },
                            "adjustment_sequence_id": {
                                "value": 1.0
                            },
                            "adjustment_matrix_type": {
                                "displayValue": "Configuration Component Price Adjustment"
                            },
                            "adjustment_basis": {
                                "value": "prv_price_point"
                            },
                            "price_point": {
                                "value": "net_price"
                            },
                            "pricing_plan_step": {
                                "value": "97b61272ffe722101fb14ad013cb14d7"
                            },
                            "running_price": {
                                "value": 12.0,
                                "displayValue": "$12.00"
                            }
                        }
                    ],
                    "total_adjustment_amount": [
                        {
                            "pricePoint": "net_price",
                            "value": -9.0,
                            "displayValue": "($9.00)"
                        }
                    ]
                }
            ],
            "status": "Success",
            "total_monthly_recurring_price": {
                "value": "89.1666",
                "displayValue": "$89.1666"
            },
            "total_monthly_recurring_price_v1": {
                "value": "60.0000",
                "displayValue": "$60.00"
            },
            "total_annual_recurring_price": {
                "value": "1070.0000",
                "displayValue": "$1,070.00"
            },
            "total_annual_recurring_price_v1": {
                "value": "350.0000",
                "displayValue": "$350.00"
            },
            "total_amount": {
                "value": "200.0000",
                "displayValue": "$200.00"
            },
            "total_amount_v1": {
                "value": "610.0000",
                "displayValue": "$610.00"
            },
            "total_one_time_price": {
                "value": "200.0000",
                "displayValue": "$200.00"
            },
            "total_one_time_cost": {
                "value": "0.0000",
                "displayValue": "$0.00"
            },
            "total_monthly_cost": {
                "value": "0.0000",
                "displayValue": "$0.00"
            },
            "total_cost": {
                "value": "0.0000",
                "displayValue": "$0.00"
            },
            "total_one_time_margin": {
                "value": "200.0000",
                "displayValue": "$200.00"
            },
            "total_monthly_margin": {
                "value": "89.1666",
                "displayValue": "$89.1666"
            },
            "total_margin_amount": {
                "value": "200.0000",
                "displayValue": "$200.00"
            },
            "total_one_time_margin_percentage": {
                "value": "100.0000",
                "displayValue": "$100.00"
            },
            "total_monthly_margin_percentage": {
                "value": "100.0000",
                "displayValue": "$100.00"
            },
            "total_margin_percentage": {
                "value": "100.0000",
                "displayValue": "$100.00"
            }
        },
        "settings": {
            "pricing_elements": "PRICE,COST,NET_PRICE,LINE_ROLLUPS,HEADER_ROLLUPS,ADJUSTMENTS"
        }
    }
}

```

## External ID resolution

This example shows setting the external ID resolution feature to true while setting the `pricelist` and `product_offering` to a custom-mapped variable called `DOORSENSOR1`.

Example:

-   `"use_external_code": true`: Enables external code resolution
-   `"pricelist": "DOORSENSOR1"`: Value maps to a custom context variable for the price
-   `"product_offering": "DOORSENSOR1"`: Value maps to a custom context variable for the product

Example: cURL request.

```
curl "https://instance.servicenow.com/api/sn_csm_pricing/v1/pricingengine/computePrice" \
--request POST \
--header "Accept: application/json" \
--header "Content-Type: application/json" \
--data '{
    "header": {
        "source_system": "ServiceNow Headless API",
        "requesting_record_id": "QT0001101",
        "currency": "USD",
        "lineItems": [
            {
                "pricelist": "DOORSENSOR1",
                "product_offering": "DOORSENSOR1",
                "periodicity" : "",
                "quantity": "1",
                "unit_of_measure": "cb2795d553020110286eddeeff7b12ff",
                "transaction_date": "2023-12-18 23:37:11",
                "line_id": "CONNECTEDC1100"
            }
        ],
        "pricelist": "19d29513d0e63110f8770dbf976be122",
        "transaction_date": "2023-12-18 23:37:11"
    },
    "settings": {
        "pricing_elements": "PRICE,COST,NET_PRICE,LINE_ROLLUPS,HEADER_ROLLUPS,ADJUSTMENTS",
        "disable_validation": true,
        "use_external_code": true
    }
}' \
--user 'username:password'
```

```
{
      "result": {
        "header": {
            "currency": "USD",
            "lineItems": [
                {
                    "line_id": "CONNECTEDC1100",
                    "status": "Success",
                    "currency": "USD",
                    "base_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "list_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "pricelist": "DOORSENSOR1",
                    "quantity": "",
                    "price_list_line": "3e93e785d07a7910f8770dbf976be1ee",
                    "product_offering": "DOORSENSOR1",
                    "one_time_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "monthly_recurring_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "annual_recurring_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "unit_net_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "cumulative_net_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "cumulative_one_time_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "cumulative_monthly_recurring_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "cumulative_annual_recurring_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "unit_adjustment": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "term_month": {
                        "value": 0,
                        "displayValue": 0
                    },
                    "cumulative_annual_recurring_price_v1": {
                        "value": 0,
                        "displayValue": 0
                    },
                    "cumulative_monthly_recurring_price_v1": {
                        "value": 0,
                        "displayValue": 0
                    },
                    "total_recurring_price": {
                        "value": "0.0000",
                        "displayValue": "$0.00"
                    },
                    "pricingAdjustments": [],
                    "total_adjustment_amount": []
                }
            ],
            "status": "Success",
            "total_monthly_recurring_price": {
                "value": "0.0000",
                "displayValue": "$0.00"
            },
            "total_monthly_recurring_price_v1": {
                "value": "0.0000",
                "displayValue": "$0.00"
            },
            "total_annual_recurring_price": {
                "value": "0.0000",
                "displayValue": "$0.00"
            },
            "total_annual_recurring_price_v1": {
                "value": "0.0000",
                "displayValue": "$0.00"
            },
            "total_amount": {
                "value": "0.0000",
                "displayValue": "$0.00"
            },
            "total_amount_v1": {
                "value": "0.0000",
                "displayValue": "$0.00"
            },
            "total_one_time_price": {
                "value": "0.0000",
                "displayValue": "$0.00"
            },
            "total_one_time_cost": {
                "value": "0.0000",
                "displayValue": "$0.00"
            },
            "total_monthly_cost": {
                "value": "0.0000",
                "displayValue": "$0.00"
            },
            "total_cost": {
                "value": "0.0000",
                "displayValue": "$0.00"
            },
            "total_one_time_margin": {
                "value": "0.0000",
                "displayValue": "$0.00"
            },
            "total_monthly_margin": {
                "value": "0.0000",
                "displayValue": "$0.00"
            },
            "total_margin_amount": {
                "value": "0.0000",
                "displayValue": "$0.00"
            },
            "total_one_time_margin_percentage": {
                "value": "0.0000",
                "displayValue": "$0.00"
            },
            "total_monthly_margin_percentage": {
                "value": "0.0000",
                "displayValue": "$0.00"
            },
            "total_margin_percentage": {
                "value": "0.0000",
                "displayValue": "$0.00"
            }
        },
        "settings": {
            "pricing_elements": "PRICE,COST,NET_PRICE,LINE_ROLLUPS,HEADER_ROLLUPS,ADJUSTMENTS",
            "use_external_code": true
        }
    }
}
```

**Parent Topic:**[Sales CRM Pricing API](../concept/sales-crm-pricing-api.md)

