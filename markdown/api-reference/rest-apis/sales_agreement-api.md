---
title: Sales Agreement API
description: The Sales Agreement API provides methods for creating a new sales agreement and retrieving an existing sales agreement of a given sys\_id.Retrieve a sales agreement associated with a given sys\_id.Creates a new sales agreement  according to details provided in the request body.
locale: en-US
release: yokohama
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 111
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# Sales Agreement API

The Sales Agreement API provides methods for creating a new sales agreement and retrieving an existing sales agreement of a given sys\_id.

This API works with data in the [Sales Agreement Management](https://www.servicenow.com/docs/access?context=sales-agreement-mgmt&version=yokohama&pubname=yokohama-order-management&ft:locale=en-US) application, which managers, agents, and administrators use to generate sales agreements from quotes.

The Sales Agreement API runs in the sn\_sales\_agmt\_core  namespace and requires three plugins to access it:

-   Sales Agreement Data Model \(com.sn\_sales\_agmt\_core\) ,
-   Product Catalog Management Core \(com.sn\_prd\_pm\),
-   Pricing \(com.sn\_csm\_pricing\)  

The API also requires the sn\_sales\_agmt\_core.sales\_agreement\_integrator  role to access it.

Most data is retrieved from or updated in the following tables upon calling this API and must be populated for its endpoints to work successfully:

-   Account \[customer\_account\],
-   Product Offering \[sn\_prd\_pm\_product\_offering\],
-   Product Model \[cmdb\_model\],
-   Quote \[quote\],
-   Quote Line \[quote\_line\],
-   Price List \[price\_list\]
-   Account \[customer\_account\]
-   Price List \[sn\_csm\_pricing\_price\_list\]
-   Product Model \[cmdb\_model\]
-   Product Offering \[sn\_prd\_pm\_product\_offering\]
-   Quote \[sn\_quote\_mgmt\_core\_quote\]
-   Quote Line \[sn\_quote\_mgmt\_core\_quote\_line\_item\]
-   Sales Agreement  \[sn\_sales\_agmt\_core\_sales\_agreement\]
-   Sales Agreement Line  \[sn\_sales\_agmt\_core\_sales\_agreement\_line\]
-   Sales Agreement Line Adjustments  \[sn\_sales\_agmt\_core\_sales\_agreement\_line\_adjustment\]
-   Sales Agreement Line Characteristics  \[sn\_sales\_agmt\_core\_sales\_agreement\_line\_characteristic\]

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## Sales Agreement - GET /api/sn\_sales\_agmt\_core/salesagreement/\{id\}

Retrieve a sales agreement associated with a given sys\_id.

### URL format

Versioned URL: `GET /api/sn_sales_agmt_core/v1/salesagreement/{id}`

Default URL: `GET /api/sn_sales_agmt_core/salesagreement/{id}`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`. Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr><tr><td>

id

</td><td>

Required. Sys\_id of the sales agreement to retrieve.Table: Sales Agreement  \[sn\_sales\_agmt\_core\_sales\_agreement\]

Data type: String

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

display\_value

</td><td>

Optional. Returns the sales agreement properties in a chosen format.Valid values:

-   all: Response contains the **name**, **label**, **value**, **display\_value**, and **type** properties for all fields   in the sales agreement. For example:

    ```
"state": {
  "display_name": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String"  
}
    ```

-   false: Response contains just the **value** property for all fields   in the sales agreement. For example:

    ```
"state": {   
  "value": "draft" 
}
    ```

-   true: Response contains just the **display\_value** property for all fields   in the sales agreement. For example:

    ```
"state": {   
  "display_value": "Draft" 
}
    ```


Default: false

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Only supports **application/json**.|
|Content-Type|Data format of the request body. Only supports **application/json**.|

|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|403|Forbidden. The user doesn't have access rights to the specified record.|
|404|Not found. The requested item wasn't found.|

### Response body parameters \(JSON or XML\)

<table id="id_axq_ryw_c2c"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

Results of the sales agreement with all its associated information.Data type: Object

```
"result": {
    "account": {Object},
    "billing_location": {Object},
    "consumer": {Object},
    "contact": {Object},
    "currency": {Object},
    "default_price_list": {Object},
    "ends": {Object},
    "number": {Object},
    "quote": {Object},
    "sales_agreement_lines": [Array]
    "shipping_location": {Object},
    "short_description": {Object},
    "starts": {Object},
    "state": {Object},
    "sys_id": {Object},
    "sys_created_by": {Object},
    "sys_created_on": {Object},
    "sys_updated_by": {Object},
    "sys_updated_on": {Object}
}
```

</td></tr><tr><td>

account

</td><td>

Account information associated with the sales agreement.Table: Account \[customer\_account\]

Data type: Object

```
"account": {
 "display_value": "String",
 "label": "String",
 "name": "String",
 "type": "String",
 "value": "String"
}
```

</td></tr><tr><td>

account.display\_value

</td><td>

Display value of the account. Matches **account.value**.Data type: String

</td></tr><tr><td>

account.label

</td><td>

Label of the account.Data type: String

</td></tr><tr><td>

account.name

</td><td>

Name of the account.Data type: String

</td></tr><tr><td>

account.type

</td><td>

Type of account. Value is always `reference`.Data type: String

</td></tr><tr><td>

account.value

</td><td>

Sys\_id of the account.Table: Account \[customer\_account\]

Data type: String

</td></tr><tr><td>

billing\_location

</td><td>

Billing address of the sales agreement.Updated table: Location \[cmn\_location\]

Data type: Object

```
"billing_location": { 
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String"
}
```

</td></tr><tr><td>

billing\_location.display\_value

</td><td>

Display value of the billing location. Matches **billing\_location.value**.Data type: String

</td></tr><tr><td>

billing\_location.label

</td><td>

Label of the billing location.Data type: String

</td></tr><tr><td>

billing\_location.name

</td><td>

Name of the billing location.Data type: String

</td></tr><tr><td>

billing\_location.type

</td><td>

Type of billing location. Value is always `reference`.Data type: String

</td></tr><tr><td>

billing\_location.value

</td><td>

Value of the billing location.Data type: String

</td></tr><tr><td>

consumer

</td><td>

Consumer details of the sales agreement.Table: Consumer \[csm\_consumer\]

Data type: Object

```
"consumer": { 
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String"
}
```

</td></tr><tr><td>

consumer.display\_value

</td><td>

Display value of the consumer. Matches **consumer.value**.Data type: String

</td></tr><tr><td>

consumer.label

</td><td>

Label of the consumer.Data type: String

</td></tr><tr><td>

consumer.name

</td><td>

Name of the consumer.Data type: String

</td></tr><tr><td>

consumer.type

</td><td>

Type of consumer. Value is always `reference`.Data type: String

</td></tr><tr><td>

consumer.value

</td><td>

Value of the consumer.Data type: String

</td></tr><tr><td>

contact

</td><td>

Contact information associated with the sales agreement.Table: Contact \[customer\_contact\]

Data type: Object

```
"contact": { 
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String"
}
```

</td></tr><tr><td>

contact.display\_value

</td><td>

Display value of the contact. Matches **contact.value**.Data type: String

</td></tr><tr><td>

contact.label

</td><td>

Label of the contact.Data type: String

</td></tr><tr><td>

contact.name

</td><td>

Name of the contact. Data type: String

</td></tr><tr><td>

contact.type

</td><td>

Type of contact. Value is always `reference`.Data type: String

</td></tr><tr><td>

contact.value

</td><td>

Value of the contact.Data type: String

</td></tr><tr><td>

currency

</td><td>

Currency code associated with the sales agreement.Table: Currency \[fx\_currency\]

Data type: Object

```
"currency": { 
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String"
}
```

</td></tr><tr><td>

currency.display\_value

</td><td>

Display value of the currency. Matches **currency.value**. For example, `USD`.Data type: String

</td></tr><tr><td>

currency.label

</td><td>

Label of the currency.Data type: String

</td></tr><tr><td>

currency.name

</td><td>

Name of the currency.Data type: String

</td></tr><tr><td>

currency.type

</td><td>

Type of currency. Value is always `reference`.Data type: String

</td></tr><tr><td>

currency.value

</td><td>

Country currency code of the currency. For example, `USD`.Data type: String

</td></tr><tr><td>

default\_price\_list

</td><td>

Details about the default price list of the sales agreement.Table: Price List \[sn\_csm\_pricing\_price\_list\]

Data type: Object

```
"default_price_list": {
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String" 
}
```

</td></tr><tr><td>

default\_price\_list.display\_value

</td><td>

Display value of the default price list.Data type: String

</td></tr><tr><td>

default\_price\_list.label

</td><td>

Label of the default price list.Data type: String

</td></tr><tr><td>

default\_price\_list.name

</td><td>

Name of the default price list.Data type: String

</td></tr><tr><td>

default\_price\_list.type

</td><td>

Type of default price list. Value is always `reference`.Data type: String

</td></tr><tr><td>

default\_price\_list.value

</td><td>

Sys\_id of the default price list.Data type: String

</td></tr><tr><td>

ends

</td><td>

End date of the sales agreement.Data type: Object

```
"ends": {
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String" 
}
```

</td></tr><tr><td>

ends.display\_value

</td><td>

Display value of the end date. Matches **end.value**.Data type: String

</td></tr><tr><td>

ends.label

</td><td>

Label of the end date.Data type: String

</td></tr><tr><td>

ends.label

</td><td>

Name of the end date.Data type: String

</td></tr><tr><td>

ends.type

</td><td>

Type of end date. Value is always `glide_date`.Data type: String

</td></tr><tr><td>

ends.value

</td><td>

Value of the end date.Format: YYYY-MM-DD

Data type: String

</td></tr><tr><td>

number

</td><td>

Automatically generated sales agreement number or the number posted .Table: Sales Agreement  \[sn\_sales\_agmt\_core\_sales\_agreement\]

Data type: Object

```
"number": { 
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String"
}
```

</td></tr><tr><td>

number.display\_value

</td><td>

Display value of the sales agreement number. Matches **number.value**.Data type: String

</td></tr><tr><td>

number.label

</td><td>

Label of the sales agreement number.Data type: String

</td></tr><tr><td>

number.name

</td><td>

Name of the sales agreement number.Data type: String

</td></tr><tr><td>

number.type

</td><td>

Type of sales agreement number. Value is always `String`.Data type: String

</td></tr><tr><td>

number.value

</td><td>

Value of the sales agreement number. For example, `SA0010106`.Data type: String

</td></tr><tr><td>

quote

</td><td>

Information about the sales agreement quote.Table: Quote \[sn\_quote\_mgmt\_core\_quote\]

Data type: Object

```
"quote": { 
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String"
}
```

</td></tr><tr><td>

quote.display\_value

</td><td>

Display value of the quote.Data type: String

</td></tr><tr><td>

quote.label

</td><td>

Label of the quote.Data type: String

</td></tr><tr><td>

quote.name

</td><td>

Name of the quote.Data type: String

</td></tr><tr><td>

quote.type

</td><td>

Type of quote. Value is always `reference`.Data type: String

</td></tr><tr><td>

quote.value

</td><td>

Sys\_id of the quote.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines

</td><td>

List of sales agreement lines under the  sales agreement. Table: Sales Agreement Line  \[sn\_sales\_agmt\_core\_sales\_agreement\_line\]

Data type: Array of objects

```
sales_agreement_lines": [
  {
  "child_sales_agreement_lines": [Array]
  "end_date": {Object},
  "number": {Object},
  "parent_line": {Object},
  "price_list": {Object},
  "product_model": {Object},
  "product_offering": {Object},
  "product_specification": {Object},
  "quantity": {Object},
  "quote_line": {Object},
  "sales_agreement": {Object},
  "sales_agreement_line_characteristics": [Array],
  "sales_agreement_line_adjustments": [Array],
  "shipping_location": {Object},
  "short_description": {Object},
  "start_date": {Object},
  "state": {Object},
  "sys_id": {Object},
  "sys_created_by": {Object},
  "sys_created_on": {Object},
  "sys_updated_by": {Object},
  "sys_updated_on": {Object},
  "top_sales_agreement_line": {Object},
  "total_one_time_price": {Object},
  "total_recurring_price": {Object},
  "unit_net_price": {Object},
  "unit_of_measure": {Object},
  }
]
```

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments

</td><td>

List of sales agreement line adjustments.Table: Sales Agreement Line Adjustments  \[sn\_sales\_agmt\_core\_sales\_agreement\_line\_adjustment\]

Data type: Array of objects

```
"sales_agreement_line_adjustments": [
  {
  "adjustment_source": {Object},
  "adjustment_type": {Object},
  "adjustment_value": {Object},
  "amount": {Object},
  "applicable_to": {Object},
  "number": {Object},
  "quantity": {Object},
  "sales_agreement": {Object},
  "sales_agreement_line": {Object},
  "short_description": {Object},
  "sys_id": {Object},
  "sys_created_by": {Object},
  "sys_updated_by": {Object},
  "sys_created_on": {Object},
  "sys_updated_on": {Object},
  "total_amount": {Object}
  }
]
```

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.adjustment\_source

</td><td>

Source information of the sales agreement line adjustment.Table: Sales Agreement Line Adjustments  \[sn\_sales\_agmt\_core\_sales\_agreement\_line\_adjustment\]

Data type: Object

```
"adjustment_source": { 
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String"
}
```

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.adjustment\_source.display\_value

</td><td>

Source display value of the sales agreement line adjustment. Matches **sales agreement line adjustment.value**.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.adjustment\_source.label

</td><td>

Source label of the sales agreement line adjustment.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.adjustment\_source.name

</td><td>

Source name of the sales agreement line adjustment.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.adjustment\_source.type

</td><td>

Source type of sales agreement line adjustment. Value is always `string`.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.adjustment\_source.value

</td><td>

Source value of the sales agreement line adjustment.Possible values:

-   auto
-   manual

Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.adjustment\_type

</td><td>

Information about the sales agreement line adjustment type.Data type: Object

```
"adjustment_type": { 
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String"
}
```

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.adjustment\_type.display\_value

</td><td>

Display value of the adjustment type.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.adjustment\_type.label

</td><td>

Label of the adjustment type.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.adjustment\_type.name

</td><td>

Name of the adjustment type.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.adjustment\_type.type

</td><td>

Type of adjustment type. Value is always `reference`.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.adjustment\_type.value

</td><td>

Sys\_id of the adjustment type.Table: Sales Agreement Line Adjustments  \[sn\_sales\_agmt\_core\_sales\_agreement\_line\_adjustment\]

Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.adjustment\_value

</td><td>

Information about the adjustment value.Table: Sales Agreement Line Adjustments  \[sn\_sales\_agmt\_core\_sales\_agreement\_line\_adjustment\]

Data type: Object

```
"adjustment_type": { 
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String"
}
```

</td></tr><tr><td>

sales\_agreement\_lines.agreement\_line\_adjustments.adjustment\_value.display\_value

</td><td>

Display value of the adjustment value. Matches **adjustment\_value.value**.Data type: Number \(decimal\)

</td></tr><tr><td>

sales\_agreement\_lines.agreement\_line\_adjustments.adjustment\_value.label

</td><td>

Label of the adjustment value.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.agreement\_line\_adjustments.adjustment\_value.name

</td><td>

Name of the adjustment value.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.agreement\_line\_adjustments.adjustment\_value.type

</td><td>

Type of adjustment. Value is always `decimal`.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.agreement\_line\_adjustments.adjustment\_value.value

</td><td>

Number value of the adjustment.Data type: Number \(decimal\)

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.amount

</td><td>

Information about the amount of the sales agreement line adjustment.Table: Sales Agreement Line Adjustments  \[sn\_sales\_agmt\_core\_sales\_agreement\_line\_adjustment\]

Data type: Object

```
"amount": { 
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String"
}
```

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.amount.display\_value

</td><td>

Display value of the adjustment amount. Matches **amount.value**. Automatically includes the dollar sign of the associated currency \(for example, `$0.00` when **currency** is set to `USD`\).Data type: Number \(decimal\)

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.amount.label

</td><td>

Label of the adjustment amount.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.amount.name

</td><td>

Name of the adjustment amount.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.amount.type

</td><td>

Type of the adjustment amount. Value is always `currency`.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.amount.value

</td><td>

Dollar value of the adjustment amount.Data type: Number

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.applicable\_to

</td><td>

Reference of the entity that the adjustment is applicable to.Table: Sales Agreement Line Adjustments  \[sn\_sales\_agmt\_core\_sales\_agreement\_line\_adjustment\]

Data type: Object

```
"applicable_to": { 
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String"
}
```

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.applicable\_to.display\_value

</td><td>

Display value of the entity that the adjustment is applicable to. Matches **applicable\_to.value**.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.applicable\_to.label

</td><td>

Label of the entity that the adjustment is applicable to.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.applicable\_to.name

</td><td>

Name of the entity that the adjustment is applicable to.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.applicable\_to.type

</td><td>

Type of the entity that the adjustment is applicable to. Value is always `String`.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.applicable\_to.value

</td><td>

Quantity type that the line adjustment is applicable to.Possible values:

-   LUMPSUM\_QTY: lipsum quantity
-   UNIT\_QTY: unit quantity

Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.number

</td><td>

Automatically generated sales agreement line adjustments number or the number posted.Table: Sales Agreement Line Adjustments  \[sn\_sales\_agmt\_core\_sales\_agreement\_line\_adjustment\]

Data type: Object

```
"number": { 
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String"
}
```

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.number.display\_value

</td><td>

Display value of the adjustments number. Matches **number.value**.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.number.label

</td><td>

Label of the adjustment number.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.number.name

</td><td>

Name of the adjustment number.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.number.type

</td><td>

Type of the adjustment number. Value is always `string`.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.number.value

</td><td>

Value of the adjustment number. For example, `SALA0010004`.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.quantity

</td><td>

Quantity of product adjusted on the sales agreement line.Table: Sales Agreement Line Adjustments  \[sn\_sales\_agmt\_core\_sales\_agreement\_line\_adjustment\]

Data type: Object

```
"quantity": { 
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String"
}
```

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.quantity.display\_value

</td><td>

Display value of the adjustment quantity. Matches **quantity.value**.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.quantity.label

</td><td>

Label of the adjustment quantity.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.quantity.name

</td><td>

Name of the adjustment quantity.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.quantity.type

</td><td>

Type of the adjustment quantity. Value is always `decimal`.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.quantity.value

</td><td>

Value of the adjustment quantity.Data type: Number

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.sales\_agreement

</td><td>

Reference to the sales agreement associated with the sales agreement line adjustment.Table: Sales Agreement Line Adjustments  \[sn\_sales\_agmt\_core\_sales\_agreement\_line\_adjustment\]

Data type: Object

```
"quantity": { 
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String"
}
```

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.sales\_agreement.display\_value

</td><td>

Display value of the sales agreement associated with the sales agreement line adjustment. For example, `SA0010106`.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.sales\_agreement.label

</td><td>

Label of the sales agreement associated with the sales agreement line adjustment.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.sales\_agreement.name

</td><td>

Name of the sales agreement associated with the sales agreement line adjustment.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.sales\_agreement.type

</td><td>

Type of the sales agreement associated with the sales agreement line adjustment. Value is always `reference`.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.sales\_agreement.value

</td><td>

Sys\_id of the sales agreement associated with the sales agreement line adjustment.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.sales\_agreement\_line

</td><td>

Reference to sales agreement line associated with the sales agreement line adjustment.Table: Sales Agreement Line Adjustments  \[sn\_sales\_agmt\_core\_sales\_agreement\_line\_adjustment\]

Data type: Object

```
"sales_agreement_line": { 
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String"
}
```

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.sales\_agreement\_line.display\_value

</td><td>

Number of the sales agreement associated with the sales agreement line adjustment. For example, `SAL0010126`.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.sales\_agreement\_line.label

</td><td>

Label of the sales agreement associated with the sales agreement line adjustment.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.sales\_agreement\_line.name

</td><td>

Name of the sales agreement associated with the sales agreement line adjustment.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.sales\_agreement\_line.type

</td><td>

Type of the sales agreement associated with the sales agreement line adjustment. Value is always `String`.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.sales\_agreement\_line.value

</td><td>

Sys\_id of the sales agreement associated with the sales agreement line adjustment.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.short\_description

</td><td>

Brief description detailing the sales agreement line adjustment.Table: Sales Agreement Line Adjustments  \[sn\_sales\_agmt\_core\_sales\_agreement\_line\_adjustment\]

Data type: Object

```
"short_description": { 
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String"
}
```

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.short\_description.display\_value

</td><td>

Display value of the short description detailing the particular line adjustment. Matches **short\_description.value**.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.short\_description.label

</td><td>

Label of the short description detailing the particular line adjustment.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.short\_description.name

</td><td>

Name of the short description detailing the particular line adjustment.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.short\_description.type

</td><td>

Type of the short description detailing the particular line adjustment. Value is always `string`.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.short\_description.value

</td><td>

Value of the short description detailing the particular line adjustment.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.sys\_created\_by

</td><td>

Name of the user who created the sales agreement line adjustment.Table: Sales Agreement Line Adjustments  \[sn\_sales\_agmt\_core\_sales\_agreement\_line\_adjustment\]

Data type: Object

```
"created_by": { 
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String"
}
```

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.sys\_created\_by.display\_value

</td><td>

Display value of the user who created the sales agreement line adjustment. Matches **created\_by.value**.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.sys\_created\_by.label

</td><td>

Label of the user who created the sales agreement line adjustment.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.sys\_created\_by.name

</td><td>

Name of the user who created the sales agreement line adjustment.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.sys\_created\_by.type

</td><td>

Type of the user who created the sales agreement line adjustment. Value is always `string`.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.sys\_created\_by.value

</td><td>

Value of the user who created the sales agreement line adjustment.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.sys\_created\_on

</td><td>

Date and time of when the sales agreement line adjustment was created.Data type: Object

```
"created_on": { 
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String"
}
```

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.sys\_created\_on.display\_value

</td><td>

Display value of the date and time that the line adjustment was created. Matches **created\_on.value**.Format: YYYY-MM-DD HH:mm:ss

Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.sys\_created\_on.label

</td><td>

Label of the date and time that the line adjustment was created.Format: YYYY-MM-DD HH:mm:ss

Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.sys\_created\_on.name

</td><td>

Name of the date and time that the line adjustment was created.Format: YYYY-MM-DD HH:mm:ss

Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.sys\_created\_on.type

</td><td>

Type of the date and time that the line adjustment was created. Value is always `glide_date_time`.Format: YYYY-MM-DD HH:mm:ss

Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.sys\_created\_on.value

</td><td>

Value of the date and time that the line adjustment was created.Format: YYYY-MM-DD HH:mm:ss

Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.sys\_id

</td><td>

Sys\_id of the sales agreement line adjustment.Table: Sales Agreement Line Adjustments  \[sn\_sales\_agmt\_core\_sales\_agreement\_line\_adjustment\]

Data type: Object

```
"sys_id": { 
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String"
}
```

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.sys\_id.display\_value

</td><td>

Display value of the line adjustment sys\_id. Matches **sys\_id.value**.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.sys\_id.label

</td><td>

Label of the line adjustment sys\_id.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.sys\_id.name

</td><td>

Name of the line adjustment sys\_id.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.sys\_id.type

</td><td>

Type of the line adjustment sys\_id. Value is always `string`.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.sys\_id.value

</td><td>

Value of the line adjustment sys\_id.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.sys\_updated\_by

</td><td>

Name of the user who last updated the sales agreement line adjustment.Table: Sales Agreement Line Adjustments  \[sn\_sales\_agmt\_core\_sales\_agreement\_line\_adjustment\]

Data type: Object

```
"updated_by": { 
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String"
}
```

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.sys\_updated\_by.display\_value

</td><td>

Display value of the user who last updated the sales agreement line adjustment. Matches **updated\_by.value**.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.sys\_updated\_by.label

</td><td>

Label of the user who last updated the sales agreement line adjustment.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.sys\_updated\_by.name

</td><td>

Name of the user who last updated the sales agreement line adjustment.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.sys\_updated\_by.type

</td><td>

Type of user who last updated the sales agreement line adjustment. Value is always `String`.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.sys\_updated\_by.value

</td><td>

Value of the user who last updated the sales agreement line adjustment.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.sys\_updated\_on

</td><td>

Date and time when the sales agreement line adjustment was updated.Data type: Object

```
"updated_on": { 
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String"
}
```

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.sys\_updated\_on.display\_value

</td><td>

Display value of the date and time that the line adjustment was last updated. Matches **updated\_on.value**.Format: YYYY-MM-DD HH:mm:ss

Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.sys\_updated\_on.label

</td><td>

Label of the date and time that the line adjustment was last updated.Format: YYYY-MM-DD HH:mm:ss

Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.sys\_updated\_on.name

</td><td>

Name of the date and time that the line adjustment was last updated.Format: YYYY-MM-DD HH:mm:ss

Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.sys\_updated\_on.type

</td><td>

Type of date and time that the line adjustment was last updated. Value is always `glide_date_time`.Format: YYYY-MM-DD HH:mm:ss

Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.sys\_updated\_on.value

</td><td>

Value of the date and time that the line adjustment was last updated.Format: YYYY-MM-DD HH:mm:ss

Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.total\_amount

</td><td>

Total amount of the sales agreement line adjustment.Table: Sales Agreement Line Adjustments  \[sn\_sales\_agmt\_core\_sales\_agreement\_line\_adjustment\]

Data type: Object

```
"total_amount": { 
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String"
}
```

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.total\_amount.display\_value

</td><td>

Display value of the total adjustment amount. Matches **total\_amount.value**.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.total\_amount.label

</td><td>

Label of the total adjustment amount.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.total\_amount.name

</td><td>

Name of the total adjustment amount.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.total\_amount.type

</td><td>

Type of the total adjustment amount. Value is always `currency`.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.total\_amount.value

</td><td>

Value of the total adjustment amount.Data type: String represented by a number \(float\)

</td></tr><tr><td>

sales\_agreement\_lines.child\_sales\_agreement\_lines

</td><td>

List of sales agreement lines. Follows the same object structure as the **sales\_agreement\_lines** object parameter.Table: Sales Agreement Line  \[sn\_sales\_agmt\_core\_sales\_agreement\_line\]

Data type: Array of objects

```
"child_sales_agreement_lines": [
  {
  "end_date": {Object},
  "number": {Object},
  "parent_line": {Object},
  "price_list": {Object},
  "product_model": {Object},
  "product_offering": {Object},
  "product_specification": {Object},
  "quantity": {Object},
  "quote_line": {Object},
  "sales_agreement": {Object},
  "sales_agreement_line_adjustments": [Array],
  "sales_agreement_line_characteristics": [Array],
  "shipping_location": {Object},
  "short_description": {Object},
  "start_date": {Object},
  "state": {Object},
  "sys_id": {Object},
  "sys_created_by": {Object},
  "sys_created_on": {Object},
  "sys_updated_by": {Object},
  "sys_updated_on": {Object},
  "top_sales_agreement_line": {Object},
  "total_one_time_price": {Object},
  "total_recurring_price": {Object},
  "unit_net_price": {Object},
  "unit_of_measure": {Object}
  }
]
```

</td></tr><tr><td>

sales\_agreement\_lines.end\_date

</td><td>

End date of the sales agreement line.Data type: Object

```
"end_date": {
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String" 
}
```

</td></tr><tr><td>

sales\_agreement\_lines.end\_date.display\_value

</td><td>

Display value of the end date for the sales agreement line. Matches **end.value**.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.end\_date.label

</td><td>

Label of the end date for the sales agreement line.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.end\_date.name

</td><td>

Name of the end date for the sales agreement line.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.end\_date.type

</td><td>

Type of end date for the sales agreement line. Value is always `glide_date_time`.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.end\_date.value

</td><td>

End date and time value of the sales agreement line.Format: YYYY-MM-DD HH:mm:ss

Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.number

</td><td>

Automatically generated sales agreement line number or the number posted .Table: Sales Agreement Line  \[sn\_sales\_agmt\_core\_sales\_agreement\_line\]

Data type: Object

```
"number": { 
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String"
}
```

</td></tr><tr><td>

sales\_agreement\_lines.number.display\_value

</td><td>

Display value of the sales agreement line number. For example, `SAL0010128`. Matches **number.value**.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.number.label

</td><td>

Label of the number.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.number.name

</td><td>

Name of the number.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.number.type

</td><td>

Type of number. Value is always `string`.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.number.value

</td><td>

Value of the sales agreement line number. For example, `SAL0010128`.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.parent\_line

</td><td>

Information about the parent sales agreement line.Table: Sales Agreement Line  \[sn\_sales\_agmt\_core\_sales\_agreement\_line\]

Data type: Object

```
"parent_line": { 
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String"
}
```

</td></tr><tr><td>

sales\_agreement\_lines.parent\_line.display\_value

</td><td>

Display number of the parent sales agreement line. For example, `SAL0010126`.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.parent\_line.label

</td><td>

Label of the parent sales agreement line.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.parent\_line.name

</td><td>

Name of the parent sales agreement line.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.parent\_line.type

</td><td>

Type of parent sales agreement line. Value is always `reference`.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.parent\_line.value

</td><td>

Sys\_id of the parent sales agreement line.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.price\_list

</td><td>

Price list details of the sales agreement line.Table: Sales Agreement Line  \[sn\_sales\_agmt\_core\_sales\_agreement\_line\]

Data type: Object

```
"price_list": {
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String" 
}
```

</td></tr><tr><td>

sales\_agreement\_lines.price\_list.display\_value

</td><td>

Display value of the sales agreement line's price list.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.price\_list.label

</td><td>

Label of the sales agreement line's price list.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.price\_list.name

</td><td>

Name of the sales agreement line's price list.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.price\_list.type

</td><td>

Type of sales agreement line's price list. Value is always `reference`.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.price\_list.value

</td><td>

Sys\_id of the price list associated with the sales agreement line.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.product\_model

</td><td>

Details about the product model on the sales agreement line.Table: Product Model \[cmdb\_model\]

Data type: Object

```
"product_model": {
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String" 
}
```

</td></tr><tr><td>

sales\_agreement\_lines.product\_model.display\_value

</td><td>

Display value of the product model on the sales agreement line. Matches **product\_model.value**.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.product\_model.label

</td><td>

Label of the product model on the sales agreement line.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.product\_model.name

</td><td>

Name of the product model on the sales agreement line.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.product\_model.type

</td><td>

Type of product model on the sales agreement line. Value is always `reference`.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.product\_model.value

</td><td>

Value of the product model on the sales agreement line.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.product\_offering

</td><td>

Details about the product offering on the sales agreement line.Table: Product Offering \[sn\_prd\_pm\_product\_offering\]

Data type: Object

```
"product_offering": {
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String" 
}
```

</td></tr><tr><td>

sales\_agreement\_lines.product\_offering.display\_value

</td><td>

Display value of the product offering on the sales agreement line.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.product\_offering.label

</td><td>

Label of the product offering on the sales agreement line.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.product\_offering.name

</td><td>

Name of the product offering on the sales agreement line.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.product\_offering.type

</td><td>

Type of product offering on the sales agreement line. Value is always `reference`.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.product\_offering.value

</td><td>

Value of the product offering on the sales agreement line.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.product\_specification

</td><td>

Reference to product specification of the sales agreement line.Table: Sales Agreement Line  \[sn\_sales\_agmt\_core\_sales\_agreement\_line\]

Data type: Object

```
"product_offering": {
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String" 
}
```

</td></tr><tr><td>

sales\_agreement\_lines.product\_specification.display\_value

</td><td>

Display value of the product offering on the sales agreement line. Matches **product\_specification.value**.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.product\_specification.label

</td><td>

Label of the product specification on the sales agreement line.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.product\_specification.name

</td><td>

Name of the product specification on the sales agreement line.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.product\_specification.type

</td><td>

Type of product specification on the sales agreement line. Value is always `reference`.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.product\_specification.value

</td><td>

Value of the product specification on the sales agreement line.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.quantity

</td><td>

Number of products to add to the sales agreement line.Table: Sales Agreement Line  \[sn\_sales\_agmt\_core\_sales\_agreement\_line\]

Data type: Object

```
"quantity": {
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String" 
}
```

</td></tr><tr><td>

sales\_agreement\_lines.quantity.display\_value

</td><td>

Display value of the product quantity on the sales agreement line. Matches **quantity.value**.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.quantity.label

</td><td>

Label of the product quantity on the sales agreement line.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.quantity.name

</td><td>

Name of the product quantity on the sales agreement line.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.quantity.type

</td><td>

Type of product quantity on the sales agreement line. Value is always `decimal`.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.quantity.value

</td><td>

Number of products on the sales agreement line. Data type: Number

</td></tr><tr><td>

sales\_agreement\_lines.quote\_line

</td><td>

Reference of the quote line item on the sales agreement line.Table: Quote Line \[sn\_quote\_mgmt\_core\_quote\_line\_item\]

Data type: Object

```
"quote_line": {
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String" 
}
```

</td></tr><tr><td>

sales\_agreement\_lines.quote\_line.display\_value

</td><td>

Display value of the quote line item on the sales agreement line.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.quote\_line.label

</td><td>

Label of the quote line item on the sales agreement line.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.quote\_line.name

</td><td>

Name of the quote line item on the sales agreement line.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.quote\_line.type

</td><td>

Type of quote line item on the sales agreement line. Value is always `reference`.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.quote\_line.value

</td><td>

Value of the quote line item on the sales agreement line.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement

</td><td>

Reference to the sales agreement of the sales agreement line.Table: Sales Agreement Line  \[sn\_sales\_agmt\_core\_sales\_agreement\_line\]

Data type: Object

```
"sales_agreement": {
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String" 
}
```

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement.display\_value

</td><td>

Display value of the sales agreement of the sales agreement line. For example, `SA0010106`.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement.label

</td><td>

Label of the sales agreement of the sales agreement line.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement.name

</td><td>

Name of the sales agreement of the sales agreement line.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement.type

</td><td>

Type of sales agreement of the sales agreement line. Value is always `reference`.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement.value

</td><td>

Sys\_id of the sales agreement of the sales agreement line.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics

</td><td>

List of sales agreement line characteristics.Table: Sales Agreement Line Characteristics \[sn\_sales\_agmt\_core\_sales\_agreement\_line\_characteristic\]

Data type: Array of objects

```
"sales_agreement_line_characteristics": [
 {
   "characteristic": {Object},
   "characteristic_option": {Object},
   "sales_agreement": {Object},
   "sales_agreement_line": {Object},
   "sys_id": {Object},
   "sys_created_by": {Object},
   "sys_updated_by": {Object},
   "sys_created_on": {Object},
   "sys_updated_on": {Object},
   "type": {Object},
   "value": {Object}
  }
]
```

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.characteristic

</td><td>

Characteristic associated with the sales agreement line.Table: sn\_prd\_pm\_characteristic

Data type: Object

```
"characteristic": {
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String" 
}
```

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.characteristic.display\_value

</td><td>

Display value of the characteristic on the sales agreement line.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.characteristic.label

</td><td>

Label of the characteristic on the sales agreement line.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.characteristic.name

</td><td>

Name of the characteristic on the sales agreement line.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.characteristic.type

</td><td>

Type of characteristic on the sales agreement line. Value is always `reference`.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.characteristic.value

</td><td>

Value of the characteristic on the sales agreement line.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.characteristic\_option

</td><td>

Information about the characteristic option on the sales agreement line.Table: Sales Agreement Line Characteristics \[sn\_sales\_agmt\_core\_sales\_agreement\_line\_characteristic\]

Data type: Object

```
"characteristic_option": {
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String" 
}
```

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.characteristic\_option.display\_value

</td><td>

Display value of the characteristic on the sales agreement line. Matches **characteristic\_option.value**. Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.characteristic\_option.label

</td><td>

Label of the characteristic option on the sales agreement line.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.characteristic\_option.name

</td><td>

Name of the characteristic option on the sales agreement line.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.characteristic\_option.type

</td><td>

Type of characteristic option on the sales agreement line. Value is always `reference`.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.characteristic\_option.value

</td><td>

Value of the characteristic option on the sales agreement line.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.sales\_agreement

</td><td>

Details of the sales agreement characteristic on the sales agreement line.Table: Sales Agreement Line Characteristics \[sn\_sales\_agmt\_core\_sales\_agreement\_line\_characteristic\]

Data type: Object

```
"sales_agreement": {
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String" 
}
```

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.sales\_agreement.display\_value

</td><td>

Display value of the sales agreement characteristic. Matches **sales\_agreement.value**. Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.sales\_agreement.label

</td><td>

Label of the sales agreement characteristic.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.sales\_agreement.name

</td><td>

Name of the sales agreement characteristic.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.sales\_agreement.type

</td><td>

Type of sales agreement characteristic. Value is always `reference`.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.sales\_agreement.value

</td><td>

Value of the sales agreement characteristic.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.sales\_agreement\_line

</td><td>

Details about the characteristic of the sales agreement line.Table: Sales Agreement Line Characteristics \[sn\_sales\_agmt\_core\_sales\_agreement\_line\_characteristic\]

Data type: Object

```
"sales_agreement_line": {
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String" 
}
```

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.sales\_agreement\_line.display\_value

</td><td>

Display value of the characteristic of the sales agreement line. Matches **sales\_agreement\_line.value**. Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.sales\_agreement\_line.label

</td><td>

Characteristic label of the sales agreement line.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.sales\_agreement\_line.name

</td><td>

Characteristic name of the sales agreement line.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.sales\_agreement\_line.type

</td><td>

Characteristic type of the sales agreement line. Value is always `reference`.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.sales\_agreement\_line.value

</td><td>

Characteristic value of the sales agreement line.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.sys\_created\_by

</td><td>

Name of the user who created the sales agreement line characteristic.Table: User \[user\]

Data type: Object

```
"sys_created_by": {
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String"
}
```

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.sys\_created\_by.display\_value

</td><td>

Display value of the Created by field. Matches **sys\_created\_by.value**.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.sys\_created\_by.label

</td><td>

Label of the Created by field.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.sys\_created\_by.name

</td><td>

Name of the Created by field.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.sys\_created\_by.type

</td><td>

Type of the Created by field. Value is always `string`.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.sys\_created\_by.value

</td><td>

Value of the Created by field.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.sys\_created\_on

</td><td>

Date and time the sales agreement line characteristic was created.Data type: Object

```
"sys_created_on": {
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String"
}
```

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.sys\_created\_on.display\_value

</td><td>

Display value of the Created on field. Matches **sys\_created\_on.value**.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.sys\_created\_on.label

</td><td>

Label of the Created on field.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.sys\_created\_on.name

</td><td>

Name of the Created on field.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.sys\_created\_on.type

</td><td>

Type of the Created on field. Value is always `glide_date_time`.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.sys\_created\_on.value

</td><td>

Value of the Created on field.Format: YYYY-DD-MM HH:mm:ss

Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.sys\_id

</td><td>

Sys\_id of the sales agreement line characteristic.Table: Sales Agreement Line Characteristics \[sn\_sales\_agmt\_core\_sales\_agreement\_line\_characteristic\]

Data type: Object

```
"sys_id": {
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String"
}
```

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.sys\_id.display\_value

</td><td>

Display value of the characteristic sys\_id. Matches **sys\_id.value**.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.sys\_id.label

</td><td>

Label of the characteristic sys\_id.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.sys\_id.name

</td><td>

Name of the characteristic sys\_id.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.sys\_id.type

</td><td>

Type of the characteristic sys\_id. Value is always `string`.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.sys\_id.id

</td><td>

Value of the characteristic sys\_id.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.sys\_updated\_by

</td><td>

Name of the user who last updated the sales agreement line characteristic.Table: User \[user\]

Data type: Object

```
"sys_updated_by": {
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String"
}
```

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.sys\_updated\_by.display\_value

</td><td>

Display value of the user who updated the characteristic of the sales agreement line item. Matches **sys\_created\_by.value**.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.sys\_updated\_by.label

</td><td>

Label of the user who updated the characteristic.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.sys\_updated\_by.name

</td><td>

Name of the user who updated the characteristic.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.sys\_updated\_by.type

</td><td>

Type of the user who updated the characteristic. Value is always `string`.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.sys\_updated\_by.value

</td><td>

Value of user who updated the characteristic.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.sys\_updated\_on

</td><td>

Date and time the sales agreement line characteristic was last updated.Data type: Object

```
"sys_updated_on": {
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String"
}
```

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.sys\_updated\_on.display\_value

</td><td>

Display value of the updated date. Matches **updated\_on.value**.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.sys\_updated\_on.label

</td><td>

Label of the updated date.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.sys\_updated\_on.name

</td><td>

Name of the updated date.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.sys\_updated\_on.type

</td><td>

Type of the updated date. Value is always `glide_date_time`.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.sys\_updated\_on.value

</td><td>

Value of the updated date.Format: YYYY-DD-MM HH:mm:ss

Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.type

</td><td>

Type of characteristic in the sales agreement line characteristic.Table: Sales Agreement Line Characteristics \[sn\_sales\_agmt\_core\_sales\_agreement\_line\_characteristic\]

Data type: Object

```
"type": {
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String"
}
```

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.type.display\_value

</td><td>

Display value of the characteristic type. Matches **type.value**.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.type.label

</td><td>

Label of the characteristic type.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.type.name

</td><td>

Name of the characteristic type.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.type.type

</td><td>

Type of the characteristic type. Value is always `string`.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.type.value

</td><td>

Value of the characteristic type.Possible values:

-   coverage
-   coverage and usage

Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.value

</td><td>

Value of the characteristic on the sales agreement line.Table: Sales Agreement Line Characteristics \[sn\_sales\_agmt\_core\_sales\_agreement\_line\_characteristic\]

Data type: Object

```
"type": {
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String"
}
```

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.value.display\_value

</td><td>

Display value of the characteristic. Matches **type.value**.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.value.label

</td><td>

Label of the characteristic value.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.value.name

</td><td>

Name of the characteristic value.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.value.type

</td><td>

Type of the characteristic value. Value is always `string`.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.value.value

</td><td>

Value of the characteristic.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.short\_description

</td><td>

Brief details describing the sales agreement line.Table: Sales Agreement Line  \[sn\_sales\_agmt\_core\_sales\_agreement\_line\]

Data type: Object

```
"short_description": { 
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String" 
}
```

</td></tr><tr><td>

sales\_agreement\_lines.short\_description.display\_value

</td><td>

Display value of the short description. Matches **short\_description.value**.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.short\_description.label

</td><td>

Label of the short description.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.short\_description.name

</td><td>

Name of the short description.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.short\_description.type

</td><td>

Type of short description. Always of type `string`.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.short\_description.value

</td><td>

Value of the short description.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.start\_date

</td><td>

Start date of the sales agreement line.Data type: Object

```
"start_date": {
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String"
}
```

</td></tr><tr><td>

sales\_agreement\_lines.start\_date.display\_value

</td><td>

Display value of the sales agreement line's start date. Matches **start\_date.value**.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.start\_date.label

</td><td>

Label of the sales agreement line's start date.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.start\_date.name

</td><td>

Name of the sales agreement line's start date.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.start\_date.type

</td><td>

Type of sales agreement line's start date. Value is always `glide_date_time`.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.start\_date.value

</td><td>

Value of the sales agreement line's start date.Format: YYYY-MM-DD

Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.state

</td><td>

Valid state of the sales agreement line.Table: Sales Agreement Line  \[sn\_sales\_agmt\_core\_sales\_agreement\_line\]

Data type: Object

```
"state": { 
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String" 
}
```

</td></tr><tr><td>

sales\_agreement\_lines.state.display\_value

</td><td>

Display value of the state. Matches **state.value**.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.state.label

</td><td>

Label of the state.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.state.name

</td><td>

Name of the state.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.state.type

</td><td>

Type of state. Value is always `string`.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.state.value

</td><td>

Value of the state.Possible values:

-   pending\_activation
-   suspended
-   active
-   expired
-   cancelled

Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sys\_created\_by

</td><td>

Name of the user who created the sales agreement line.Table: User \[user\]

Data type: Object

```
"sys_created_by": {
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String"
}
```

</td></tr><tr><td>

sales\_agreement\_lines.sys\_created\_by.display\_value

</td><td>

Display value of the user who created the sales agreement line. Matches **sys\_created\_by.value**.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sys\_created\_by.label

</td><td>

Label of the user who created the sales agreement line.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sys\_created\_by.name

</td><td>

Name of the user who created the sales agreement line.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sys\_created\_by.type

</td><td>

Type of the Created by field. Value is always `string`.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sys\_created\_by.value

</td><td>

Value of the user who created the sales agreement line.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sys\_created\_on

</td><td>

Date and time the sales agreement line record was created.Data type: Object

```
"sys_created_on": { 
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String"
}
```

</td></tr><tr><td>

sales\_agreement\_lines.sys\_created\_on.display\_value

</td><td>

Display value of the creation date of the sales agreement line record. Matches **sys\_created\_on.value**.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sys\_created\_on.label

</td><td>

Label of the creation date of the sales agreement line record.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sys\_created\_on.name

</td><td>

Name of the creation date of the sales agreement line record.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sys\_created\_on.type

</td><td>

Type of the creation date of the sales agreement line record. Value is always `glide_date_time`.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sys\_created\_on.value

</td><td>

Value of the creation date of the sales agreement line record.Format: YYYY-MM-DD HH:mm:ss

Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sys\_id

</td><td>

Sys\_id of the sales agreement line record .Table: Sales Agreement Line  \[sn\_sales\_agmt\_core\_sales\_agreement\_line\]

Data type: Object

```
"sys_id": { 
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String" 
}
```

</td></tr><tr><td>

sales\_agreement\_lines.sys\_id.displayValue

</td><td>

Display value of the sys\_id of the sales agreement line record . Matches **sys\_id.value**.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sys\_id.label

</td><td>

Automatically-generated name or label of the sales agreement line record  sys\_id.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sys\_id.type

</td><td>

Type of sys\_id of the sales agreement line record . Value is always `string`.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sys\_id.value

</td><td>

Sys\_id number assigned to the sales agreement line record .Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sys\_updated\_by

</td><td>

Name of the user who last updated the sales agreement line.Table: User \[user\]

Data type: Object

```
"sys_updated_by": { 
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String"
}
```

</td></tr><tr><td>

sales\_agreement\_lines.sys\_updated\_by.display\_value

</td><td>

Display value of the user who updated the sales agreement line. Matches **sys\_updated\_by.value**.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sys\_updated\_by.label

</td><td>

Label of the user who updated the sales agreement line.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sys\_updated\_by.name

</td><td>

Name of the user who updated the sales agreement line.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sys\_updated\_by.type

</td><td>

Type of the user who updated the sales agreement line. Value is always `string`.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sys\_updated\_by.value

</td><td>

Value of the user who updated the sales agreement line.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sys\_updated\_on

</td><td>

Date and time the sales agreement line record was last updated.Data type: Object

```
"sys_updated_on": { 
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String"
}
```

</td></tr><tr><td>

sales\_agreement\_lines.sys\_updated\_on.display\_value

</td><td>

The display value of the updated date and time on the sales agreement line. Matches **sys\_updated\_on.value**.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sys\_updated\_on.label

</td><td>

Label of the updated date and time on the sales agreement lineData type: String

</td></tr><tr><td>

sales\_agreement\_lines.sys\_updated\_on.name

</td><td>

Name of the updated date and time on the sales agreement lineData type: String

</td></tr><tr><td>

sales\_agreement\_lines.sys\_updated\_on.type

</td><td>

Type of the updated date and time on the sales agreement line. Value is always `glide_date_time`.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sys\_updated\_on.value

</td><td>

Value of the updated date and time on the sales agreement lineFormat: YYYY-MM-DD HH:mm:ss

Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.top\_sales\_agreement\_line

</td><td>

Information about the top sales agreement line.Table: Sales Agreement Line  \[sn\_sales\_agmt\_core\_sales\_agreement\_line\]

Data type: Object

```
"top_sales_agreement_line": { 
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String"
}
```

</td></tr><tr><td>

sales\_agreement\_lines.top\_sales\_agreement\_line.display\_value

</td><td>

Display value of the top sales agreement line. Matches **top\_sales\_agreement\_line.value**.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.top\_sales\_agreement\_line.label

</td><td>

Label of the top sales agreement line.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.top\_sales\_agreement\_line.name

</td><td>

Name the top sales agreement line.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.top\_sales\_agreement\_line.type

</td><td>

Type of the top sales agreement line. Value is always `reference`.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.top\_sales\_agreement\_line.value

</td><td>

Value of the top sales agreement line.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.total\_one\_time\_price

</td><td>

Total one-time charges to be paid for the product or service.Table: Sales Agreement Line  \[sn\_sales\_agmt\_core\_sales\_agreement\_line\]

Data type: Object

```
"total_one_time_price": { 
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String"
}
```

</td></tr><tr><td>

sales\_agreement\_lines.total\_one\_time\_price.display\_value

</td><td>

Display value of the total one time price. Matches **total\_one\_time\_price.value**.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.total\_one\_time\_price.label

</td><td>

Label of the total one time price.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.total\_one\_time\_price.name

</td><td>

Name of the total one time price.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.total\_one\_time\_price.type

</td><td>

Type of the total one time price. Value is always `decimal`.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.total\_one\_time\_price.value

</td><td>

Value of the total one time price.Data type: String represented as a number \(currency\)

</td></tr><tr><td>

sales\_agreement\_lines.total\_recurring\_price

</td><td>

Total recurring price for the product associated with the sales agreement line.Table: Sales Agreement Line  \[sn\_sales\_agmt\_core\_sales\_agreement\_line\]

Data type: Object

```
"total_recurring_price": { 
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String"
}
```

</td></tr><tr><td>

sales\_agreement\_lines.total\_recurring\_price.display\_value

</td><td>

Display value of the total one time price. Matches **total\_recurring\_price.value**.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.total\_recurring\_price.label

</td><td>

Label of the total recurring price.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.total\_recurring\_price.name

</td><td>

Name of the total recurring price.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.total\_recurring\_price.type

</td><td>

Type of the total recurring price. Value is always `decimal`.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.total\_recurring\_price.value

</td><td>

Value of the total recurring price.Data type: String represented as a number \(currency\)

</td></tr><tr><td>

sales\_agreement\_lines.unit\_net\_price

</td><td>

The price for each unit within the sales agreement line.Table: Sales Agreement Line  \[sn\_sales\_agmt\_core\_sales\_agreement\_line\]

Data type: Object

```
"unit_net_price": { 
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String"
}
```

</td></tr><tr><td>

sales\_agreement\_lines.unit\_net\_price

</td><td>

Display value of the unit net price. Matches **unit\_net\_price.value**.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.unit\_net\_price

</td><td>

Label of the unit net price.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.unit\_net\_price

</td><td>

Name of the unit net price.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.unit\_net\_price

</td><td>

Type of the unit net price. Value is always `decimal`.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.unit\_net\_price

</td><td>

Value of the unit net price.Data type: String represented as a number \(currency\)

</td></tr><tr><td>

sales\_agreement\_lines.unit\_of\_measurement

</td><td>

Unit of measurement of the sales agreement line.Table: Unit of measures \[sn\_prd\_pm\_uom\_list\]

Data type: Object

```
"unit_of_measurement": { 
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String"
}
```

</td></tr><tr><td>

sales\_agreement\_lines.unit\_of\_measurement.display\_value

</td><td>

Display value of the unit of measurement. Matches **unit\_of\_measurement.value**.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.unit\_of\_measurement.label

</td><td>

Label of the unit of measurement.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.unit\_of\_measurement.name

</td><td>

Name of the unit of measurement.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.unit\_of\_measurement.type

</td><td>

Type of the unit of measurement. Value is always `reference`.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.unit\_of\_measurement.value

</td><td>

Value of the unit of measurement. For example, `bundle` or `each`.Data type: String

</td></tr><tr><td>

shipping\_location

</td><td>

Shipping address details on the sales agreement.Table: Location \[location\]

Data type: Object

```
"unit_of_measure": { 
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String"
}
```

</td></tr><tr><td>

shipping\_location.display\_value

</td><td>

Display value of the shipping location.Data type: String

</td></tr><tr><td>

shipping\_location.label

</td><td>

Label of the shipping location.Data type: String

</td></tr><tr><td>

shipping\_location.name

</td><td>

Name of the shipping location.Data type: String

</td></tr><tr><td>

shipping\_location.type

</td><td>

Type of shipping location. Value is always `reference`.Data type: String

</td></tr><tr><td>

shipping\_location.value

</td><td>

Value of the shipping location. For example, an address.Data type: String

</td></tr><tr><td>

short\_description

</td><td>

Brief details describing the sales agreement.Table: Sales Agreement  \[sn\_sales\_agmt\_core\_sales\_agreement\]

Data type: Object

```
"short_description": { 
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String" 
}
```

</td></tr><tr><td>

short\_description.display\_value

</td><td>

Display value of the short description. Matches **short\_description.value**.Data type: String

</td></tr><tr><td>

short\_description.label

</td><td>

Label of the short description.Data type: String

</td></tr><tr><td>

short\_description.name

</td><td>

Name of the short description.Data type: String

</td></tr><tr><td>

short\_description.type

</td><td>

Type of short description. Always of type `string`.Data type: String

</td></tr><tr><td>

short\_description.value

</td><td>

Value of the short description.Data type: String

</td></tr><tr><td>

starts

</td><td>

Start date of the sales agreement.Data type: Object

```
"starts": { 
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String"
}
```

</td></tr><tr><td>

starts.display\_value

</td><td>

Display value of the start date. Matches **start.value**.Data type: String

</td></tr><tr><td>

starts.label

</td><td>

Label of the start date.Data type: String

</td></tr><tr><td>

starts.name

</td><td>

Name of the start date.Data type: String

</td></tr><tr><td>

starts.type

</td><td>

Type of start date. Value is always `glide_date_time`Data type: String

</td></tr><tr><td>

starts.value

</td><td>

Value of the start date.Format: YYYY-MM-DD HH:mm:ss

Data type: String

</td></tr><tr><td>

state

</td><td>

State of the sales agreement.Table: Sales Agreement  \[sn\_sales\_agmt\_core\_sales\_agreement\]

Data type: Object

```
"state": { 
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String" 
}
```

</td></tr><tr><td>

state.display\_value

</td><td>

Display value of the state. Matches **state.value**.Data type: String

</td></tr><tr><td>

state.lable

</td><td>

Label of the state.Data type: String

</td></tr><tr><td>

state.name

</td><td>

Name of the state.Data type: String

</td></tr><tr><td>

state.type

</td><td>

Type of state. Value is always `string`.Data type: String

</td></tr><tr><td>

state.value

</td><td>

Value of the state.Possible values:

-   active
-   cancelled
-   draft
-   expired

Data type: String

</td></tr><tr><td>

sys\_created\_by

</td><td>

Name of the user who created the sales agreement.Table: User \[user\]

Data type: Object

```
"sys_created_by": {
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String"
}
```

</td></tr><tr><td>

sys\_created\_by.display\_value

</td><td>

Display value of the user who created the sales agreement. Matches **sys\_created\_by.value**.Data type: String

</td></tr><tr><td>

sys\_created\_by.label

</td><td>

Label of the user who created the sales agreement.Data type: String

</td></tr><tr><td>

sys\_created\_by.name

</td><td>

Name of the user who created the sales agreement.Data type: String

</td></tr><tr><td>

sys\_created\_by.type

</td><td>

Type of the user who created the sales agreement. Value is always `string`.Data type: String

</td></tr><tr><td>

sys\_created\_by.value

</td><td>

Value of the user who created the sales agreement.Data type: String

</td></tr><tr><td>

sys\_created\_on

</td><td>

Details about the date and time that the sales agreement was created.Data type: Object

```
"sys_created_on": { 
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String"
}
```

</td></tr><tr><td>

sys\_created\_on.display\_value

</td><td>

Display value of the creation date and time. Matches **sys\_created\_on.value**.Data type: String

</td></tr><tr><td>

sys\_created\_on.label

</td><td>

Label of the creation date and time.Data type: String

</td></tr><tr><td>

sys\_created\_on.name

</td><td>

Name of the creation date and time.Data type: String

</td></tr><tr><td>

sys\_created\_on.type

</td><td>

Type of the creation date and time. Value is always `string`.Data type: String

</td></tr><tr><td>

sys\_created\_on.value

</td><td>

Value of the creation date and time.Data type: String

</td></tr><tr><td>

sys\_id

</td><td>

Sys\_id   of the newly created sales agreement.Table: Sales Agreement  \[sn\_sales\_agmt\_core\_sales\_agreement\]

Data type: Object

```
"sys_id": { 
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String" 
}
```

</td></tr><tr><td>

sys\_id.displayValue

</td><td>

Display value of the unique sys\_id value. Matches **sys\_id.value**.Data type: String

</td></tr><tr><td>

sys\_id.label

</td><td>

Automatically generated name or label of the sys\_id.Data type: String

</td></tr><tr><td>

sys\_id.type

</td><td>

Type of sys\_id given to the sales agreement. Value is always `GUID`.Data type: String

</td></tr><tr><td>

sys\_id.value

</td><td>

Sys\_id number assigned to the new sales agreement.Data type: String

</td></tr><tr><td>

sys\_updated\_by

</td><td>

Name of the user who last updated the sales agreement.Table: User \[user\]

Data type: Object

```
"sys_updated_by": { 
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String"
}
```

</td></tr><tr><td>

sys\_updated\_by.display\_value

</td><td>

Display value of the user who updated the sales agreement. Matches **sys\_updated\_by.value**.Data type: String

</td></tr><tr><td>

sys\_updated\_by.label

</td><td>

Label of the user who updated the sales agreement.Data type: String

</td></tr><tr><td>

sys\_updated\_by.name

</td><td>

Name of the user who updated the sales agreement.Data type: String

</td></tr><tr><td>

sys\_updated\_by.type

</td><td>

Type of the user who updated the sales agreement. Value is always `string`.Data type: String

</td></tr><tr><td>

sys\_updated\_by.value

</td><td>

Value of the user who updated the sales agreement.Data type: String

</td></tr><tr><td>

sys\_updated\_on

</td><td>

Details about the date and time that the sales agreement was updated.Data type: Object

```
"sys_updated_on": { 
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String"
}
```

</td></tr><tr><td>

sys\_updated\_on.display\_value

</td><td>

Date and time value of the updated sales agreement. Matches **sys\_updated\_on.value**.Format: YYYY-MM-DD HH:mm:ss

Data type: String

</td></tr><tr><td>

sys\_updated\_on.label

</td><td>

Label of the updated sales agreement.Data type: String

</td></tr><tr><td>

sys\_updated\_on.name

</td><td>

Name of the updated sales agreement.Data type: String

</td></tr><tr><td>

sys\_updated\_on.type

</td><td>

Type of the updated sales agreement. Value is always `glide_date_time`.Data type: String

</td></tr><tr><td>

sys\_updated\_on.value

</td><td>

Date and time value of the updated sales agreement.Format: YYYY-MM-DD HH:mm:ss

Data type: String

</td></tr></tbody>
</table>### cURL request

The following example returns the sales agreement information associated with the given sys\_id and the optional **display\_value** parameter set to `true` so that display values are provided in the response body.

```

curl "https://instance.service-now.com/api/sn_sales_agmt_core/v1/salesagreement/eb853fe5b5165610f87786d3c2884335?display_value=true" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
```

Response body. The response shows the display\_values for every parameter of the given sales agreement.

```
{
  "result": {
    "sys_id": {
      "display_value": "eb853fe5b5165610f87786d3c2884335"
    },
    "sys_created_by": {
      "display_value": "maint"
    },
    "sys_updated_by": {
      "display_value": "maint"
    },
    "sys_created_on": {
      "display_value": "2024-12-05 22:43:51"
    },
    "sys_updated_on": {
      "display_value": "2024-12-05 22:43:51"
    },
    "account": {
      "display_value": "Boxeo"
    },
    "consumer": {
      "display_value": ""
    },
    "number": {
      "display_value": "SA0010004"
    },
    "state": {
      "display_value": "Active"
    },
    "starts": {
      "display_value": "2024-01-01"
    },
    "ends": {
      "display_value": "2024-12-31"
    },
    "short_description": {
      "display_value": "This is a Sa created by API"
    },
    "currency": {
      "display_value": "USD"
    },
    "default_price_list": {
      "display_value": "SA Price List"
    },
    "billing_location": {
      "display_value": "100 South Charles Street, Baltimore,MD"
    },
    "contact": {
      "display_value": "Alex Linde"
    },
    "shipping_location": {
      "display_value": "100 South Charles Street, Baltimore,MD"
    },
    "quote": {
      "display_value": "QT0000001"
    },
    "sales_agreement_lines": [
      {
        "sys_id": {
          "display_value": "af853fe5b5165610f87786d3c2884339"
        },
        "sys_created_by": {
          "display_value": "maint"
        },
        "sys_updated_by": {
          "display_value": "maint"
        },
        "sys_created_on": {
          "display_value": "2024-12-05 22:43:51"
        },
        "sys_updated_on": {
          "display_value": "2024-12-05 22:43:51"
        },
        "number": {
          "display_value": "SAL0010003"
        },
        "sales_agreement": {
          "display_value": "SA0010004"
        },
        "short_description": {
          "display_value": "this is sample sa line 1"
        },
        "start_date": {
          "display_value": "2024-11-10"
        },
        "end_date": {
          "display_value": "2024-12-31"
        },
        "state": {
          "display_value": "Active"
        },
        "product_offering": {
          "display_value": "Home Automation Bundle"
        },
        "product_specification": {
          "display_value": ""
        },
        "product_model": {
          "display_value": ""
        },
        "price_list": {
          "display_value": "SA Price List"
        },
        "parent_line": {
          "display_value": ""
        },
        "unit_net_price": {
          "display_value": "£314.2315"
        },
        "quantity": {
          "display_value": "2"
        },
        "unit_of_measurement": {
          "display_value": "Each"
        },
        "shipping_location": {
          "display_value": "100 South Charles Street, Baltimore,MD"
        },
        "total_one_time_price": {
          "display_value": "£314.2315"
        },
        "total_recurring_price": {
          "display_value": "£0.00"
        },
        "top_sales_agreement_line": {
          "display_value": "SAL0010003"
        },
        "quote_line": {
          "display_value": ""
        },
        "child_sales_agreement_lines": [
          {
            "sys_id": {
              "display_value": "eb85f329b5165610f87786d3c2884318"
            },
            "sys_created_by": {
              "display_value": "maint"
            },
            "sys_updated_by": {
              "display_value": "maint"
            },
            "sys_created_on": {
              "display_value": "2024-12-05 22:43:51"
            },
            "sys_updated_on": {
              "display_value": "2024-12-05 22:43:51"
            },
            "number": {
              "display_value": "SAL0010004"
            },
            "sales_agreement": {
              "display_value": "SA0010004"
            },
            "short_description": {
              "display_value": "this is sample child sa line 1"
            },
            "start_date": {
              "display_value": "2024-11-11"
            },
            "end_date": {
              "display_value": "2024-12-31"
            },
            "state": {
              "display_value": "Active"
            },
            "product_offering": {
              "display_value": "Home Automation Hub"
            },
            "product_specification": {
              "display_value": ""
            },
            "product_model": {
              "display_value": ""
            },
            "price_list": {
              "display_value": "SA Price List"
            },
            "parent_line": {
              "display_value": "SAL0010003"
            },
            "unit_net_price": {
              "display_value": "£94.2694"
            },
            "quantity": {
              "display_value": "2"
            },
            "unit_of_measurement": {
              "display_value": "Each"
            },
            "shipping_location": {
              "display_value": "100 South Charles Street, Baltimore,MD"
            },
            "total_one_time_price": {
              "display_value": "£94.2694"
            },
            "total_recurring_price": {
              "display_value": "£0.00"
            },
            "top_sales_agreement_line": {
              "display_value": "SAL0010003"
            },
            "quote_line": {
              "display_value": ""
            },
            "child_sales_agreement_lines": [],
            "sales_agreement_line_characteristics": [
              {
                "sys_id": {
                  "display_value": "e385f329b5165610f87786d3c288431a"
                },
                "sys_created_by": {
                  "display_value": "maint"
                },
                "sys_updated_by": {
                  "display_value": "maint"
                },
                "sys_created_on": {
                  "display_value": "2024-12-05 22:43:51"
                },
                "sys_updated_on": {
                  "display_value": "2024-12-05 22:43:51"
                },
                "sales_agreement": {
                  "display_value": "SA0010004"
                },
                "sales_agreement_line": {
                  "display_value": "SAL0010004"
                },
                "characteristic": {
                  "display_value": "Connectivity Tech"
                },
                "type": {
                  "display_value": null
                },
                "characteristic_option": {
                  "display_value": "3G"
                },
                "value": {
                  "display_value": "3G"
                }
              }
            ],
            "sales_agreement_line_adjustments": [
              {
                "sys_id": {
                  "display_value": "2385f329b5165610f87786d3c288431b"
                },
                "sys_created_by": {
                  "display_value": "maint"
                },
                "sys_updated_by": {
                  "display_value": "maint"
                },
                "sys_created_on": {
                  "display_value": "2024-12-05 22:43:51"
                },
                "sys_updated_on": {
                  "display_value": "2024-12-05 22:43:51"
                },
                "sales_agreement": {
                  "display_value": "SA0010004"
                },
                "sales_agreement_line": {
                  "display_value": "SAL0010004"
                },
                "adjustment_type": {
                  "display_value": "Markdown %"
                },
                "adjustment_source": {
                  "display_value": "Manual"
                },
                "adjustment_value": {
                  "display_value": "20"
                },
                "applicable_to": {
                  "display_value": "Unit Quantity"
                },
                "short_description": {
                  "display_value": "Price adjustment"
                },
                "number": {
                  "display_value": "SALA0010004"
                },
                "quantity": {
                  "display_value": "1"
                },
                "total_amount": {
                  "display_value": "£28.00"
                },
                "amount": {
                  "display_value": "£28.00"
                }
              }
            ]
          }
        ],
        "sales_agreement_line_characteristics": [
          {
            "sys_id": {
              "display_value": "a785f329b5165610f87786d3c2884315"
            },
            "sys_created_by": {
              "display_value": "maint"
            },
            "sys_updated_by": {
              "display_value": "maint"
            },
            "sys_created_on": {
              "display_value": "2024-12-05 22:43:51"
            },
            "sys_updated_on": {
              "display_value": "2024-12-05 22:43:51"
            },
            "sales_agreement": {
              "display_value": "SA0010004"
            },
            "sales_agreement_line": {
              "display_value": "SAL0010003"
            },
            "characteristic": {
              "display_value": "Connectivity Tech"
            },
            "type": {
              "display_value": null
            },
            "characteristic_option": {
              "display_value": "3G"
            },
            "value": {
              "display_value": "3G"
            }
          }
        ],
        "sales_agreement_line_adjustments": [
          {
            "sys_id": {
              "display_value": "2b85f329b5165610f87786d3c2884316"
            },
            "sys_created_by": {
              "display_value": "maint"
            },
            "sys_updated_by": {
              "display_value": "maint"
            },
            "sys_created_on": {
              "display_value": "2024-12-05 22:43:51"
            },
            "sys_updated_on": {
              "display_value": "2024-12-05 22:43:51"
            },
            "sales_agreement": {
              "display_value": "SA0010004"
            },
            "sales_agreement_line": {
              "display_value": "SAL0010003"
            },
            "adjustment_type": {
              "display_value": "Markdown %"
            },
            "adjustment_source": {
              "display_value": "Auto"
            },
            "adjustment_value": {
              "display_value": "10"
            },
            "applicable_to": {
              "display_value": "Unit Quantity"
            },
            "short_description": {
              "display_value": "Price adjustment"
            },
            "number": {
              "display_value": "SALA0010003"
            },
            "quantity": {
              "display_value": "3"
            },
            "total_amount": {
              "display_value": "£120.00"
            },
            "amount": {
              "display_value": "£40.00"
            }
          }
        ]
      }
    ]
  }
}
```

### cURL request

The following example returns the sales agreement information associated with the given sys\_id and the optional **display\_value** parameter set to `all` so that all parameter values are provided in the response body.

```

curl "https://instance.service-now.com/api/sn_sales_agmt_core/v1/salesagreement/eb853fe5b5165610f87786d3c2884335?display_value=true" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
  "state": "active",
  "account": "86837a386f0331003b3c498f5d3ee4ca",
  "starts": "2024-01-01",
  "ends": "2024-12-31",
  "short_description": "this is a sample sales agreement",
  "quote": "04ba9004f11f3110f8777d7194f166f6",
  "default_price_list": "19d29513d0e63110f8770dbf976be122",
  "contact": "",
  "name": "",
  "description": "",
  "currency": "",
  "sales_agreement_lines": [
    {
      "start_date": "2024-02-01",
      "end_date": "2024-11-30",
      "short_description": "this is sample sa line 1",
      "state": "active",
      "quantity": "",
      "price_list": "19d29513d0e63110f8770dbf976be122",
      "product_offering": "",
      "product_specification": "",
      "product_model": "",
      "unit_net_price": "",
      "unit_of_measure": "",
      "shipping_location": "",
      "billing_location": "",
      "total_one_time_price": "",
      "total_recurring_price": "",
      "quote_line": "",
      "child_sales_agreement_lines": [
        {
          "start_date": "2024-02-01",
          "end_date": "2024-11-30",
          "short_description": "this is sample sa line 1",
          "state": "active",
          "quantity": "",
          "price_list": "19d29513d0e63110f8770dbf976be122",
          "product_offering": "",
          "product_specification": "",
          "product_model": "",
          "unit_net_price": "",
          "unit_of_measure": "",
          "shipping_location": "",
          "billing_location": "",
          "total_one_time_price": "",
          "total_recurring_price": "",
          "quote_line": "",
          "sales_agreement_line_characteristics": [
            {
              "characteristic": "4d289f1a775131108e191e599a5a99c7",
              "type": "coverage",
              "characteristic_option": "",
              "value": ""
            }
          ]
        },
        {
          "start_date": "2024-02-01",
          "end_date": "2024-11-30",
          "short_description": "this is sample sa line 1",
          "state": "active",
          "quantity": "",
          "price_list": "19d29513d0e63110f8770dbf976be122",
          "product_offering": "",
          "product_specification": "",
          "product_model": "",
          "unit_net_price": "",
          "unit_of_measure": "",
          "shipping_location": "",
          "billing_location": "",
          "total_one_time_price": "",
          "total_recurring_price": "",
          "quote_line": "",
          "sales_agreement_line_characteristics": [
            {
              "characteristic": "4d289f1a775131108e191e599a5a99c7",
              "type": "coverage",
              "characteristic_option": "",
              "value": ""
            }
          ]
        }
      ],
      "sales_agreement_line_characteristics": [
        {
          "characteristic": "4d289f1a775131108e191e599a5a99c7",
          "type": "coverage",
          "characteristic_option": "",
          "value": ""
        }
      ],
      "sales_agreement_line_adjustments": [
        {
          "total_amount": "",
          "quantity": 3,
          "amount": "",
          "short_description": "line adjustment",
          "adjustment_value": "123",
          "adjustment_source": "",
          "adjustment_type": "d88bc79653dd91105c0eddeeff7b12c1",
          "applicable_to": ""
        }
      ]
    }
  ]
}"
```

Response body. The response shows all parameters of the given sales agreement.

```
{
  "result": {
    "sys_id": {
      "label": "Sys ID",
      "value": "bc93e08a78755a10f8777f88938ba1d8",
      "displayValue": "bc93e08a78755a10f8777f88938ba1d8",
      "type": "GUID"
    },
    "sys_created_by": {
      "name": "sys_created_by",
      "label": "Created by",
      "value": "maint",
      "display_value": "maint",
      "type": "string"
    },
    "sys_updated_by": {
      "name": "sys_updated_by",
      "label": "Updated by",
      "value": "maint",
      "display_value": "maint",
      "type": "string"
    },
    "sys_created_on": {
      "name": "sys_created_on",
      "label": "Created",
      "value": "2024-11-12 08:11:59",
      "display_value": "2024-11-12 00:11:59",
      "type": "glide_date_time"
    },
    "sys_updated_on": {
      "name": "sys_updated_on",
      "label": "Updated",
      "value": "2024-11-12 08:11:59",
      "display_value": "2024-11-12 00:11:59",
      "type": "glide_date_time"
    },
    "name": null,
    "account": {
      "name": "account",
      "label": "Account",
      "value": "86837a386f0331003b3c498f5d3ee4ca",
      "display_value": "Boxeo",
      "type": "reference"
    },
    "consumer": {
      "name": "consumer",
      "label": "Consumer",
      "value": null,
      "display_value": "",
      "type": "reference"
    },
    "number": {
      "name": "number",
      "label": "Number",
      "value": "SA0010106",
      "display_value": "SA0010106",
      "type": "string"
    },
    "state": {
      "name": "state",
      "label": "State",
      "value": "active",
      "display_value": "Active",
      "type": "string"
    },
    "starts": {
      "name": "starts",
      "label": "Start date",
      "value": "2024-01-01",
      "display_value": "2024-01-01",
      "type": "glide_date"
    },
    "ends": {
      "name": "ends",
      "label": "End date",
      "value": "2024-12-31",
      "display_value": "2024-12-31",
      "type": "glide_date"
    },
    "short_description": {
      "name": "short_description",
      "label": "Short description",
      "value": "this is a sample sales agreement",
      "display_value": "this is a sample sales agreement",
      "type": "string"
    },
    "description": {
      "name": "description",
      "label": "Description",
      "value": null,
      "display_value": "",
      "type": "string"
    },
    "currency": {
      "name": "currency",
      "label": "Currency",
      "value": null,
      "display_value": "",
      "type": "reference"
    },
    "default_price_list": {
      "name": "default_price_list",
      "label": "Default price list",
      "value": "19d29513d0e63110f8770dbf976be122",
      "display_value": "Standard Price List",
      "type": "reference"
    },
    "billing_location": {
      "name": "billing_location",
      "label": "Billing location",
      "value": null,
      "display_value": "",
      "type": "reference"
    },
    "contact": {
      "name": "contact",
      "label": "Contact",
      "value": null,
      "display_value": "",
      "type": "reference"
    },
    "shipping_location": {
      "name": "shipping_location",
      "label": "Shipping location",
      "value": null,
      "display_value": "",
      "type": "reference"
    },
    "quote": {
      "name": "quote",
      "label": "Quote",
      "value": "04ba9004f11f3110f8777d7194f166f6",
      "display_value": "QT0000001",
      "type": "reference"
    },
    "service_contract_lines": [
      {
        "sys_id": {
          "label": "Sys ID",
          "value": "3c93e08a78755a10f8777f88938ba1dd",
          "displayValue": "3c93e08a78755a10f8777f88938ba1dd",
          "type": "GUID"
        },
        "sys_created_by": {
          "name": "sys_created_by",
          "label": "Created by",
          "value": "maint",
          "display_value": "maint",
          "type": "string"
        },
        "sys_updated_by": {
          "name": "sys_updated_by",
          "label": "Updated by",
          "value": "maint",
          "display_value": "maint",
          "type": "string"
        },
        "sys_created_on": {
          "name": "sys_created_on",
          "label": "Created",
          "value": "2024-11-12 08:11:59",
          "display_value": "2024-11-12 00:11:59",
          "type": "glide_date_time"
        },
        "sys_updated_on": {
          "name": "sys_updated_on",
          "label": "Updated",
          "value": "2024-11-12 08:11:59",
          "display_value": "2024-11-12 00:11:59",
          "type": "glide_date_time"
        },
        "number": {
          "name": "number",
          "label": "Number",
          "value": "SAL0010126",
          "display_value": "SAL0010126",
          "type": "string"
        },
        "sales_agreement": {
          "name": "sales_agreement",
          "label": "Sales agreement",
          "value": "bc93e08a78755a10f8777f88938ba1d8",
          "display_value": "SA0010106",
          "type": "reference"
        },
        "short_description": {
          "name": "short_description",
          "label": "Short description",
          "value": "this is sample sa line 1",
          "display_value": "this is sample sa line 1",
          "type": "string"
        },
        "start_date": {
          "name": "start_date",
          "label": "Start date",
          "value": "2024-02-01",
          "display_value": "2024-02-01",
          "type": "glide_date"
        },
        "end_date": {
          "name": "end_date",
          "label": "End date",
          "value": "2024-11-30",
          "display_value": "2024-11-30",
          "type": "glide_date"
        },
        "state": {
          "name": "state",
          "label": "State",
          "value": "active",
          "display_value": "Active",
          "type": "string"
        },
        "product_offering": {
          "name": "product_offering",
          "label": "Product offering",
          "value": null,
          "display_value": "",
          "type": "reference"
        },
        "product_specification": {
          "name": "product_specification",
          "label": "Product specification",
          "value": null,
          "display_value": "",
          "type": "reference"
        },
        "product_model": {
          "name": "product_model",
          "label": "Product model",
          "value": null,
          "display_value": "",
          "type": "reference"
        },
        "price_list": {
          "label": "Price list",
          "value": "19d29513d0e63110f8770dbf976be122",
          "display_value": "Standard Price List",
          "type": "reference"
        },
        "parent_line": {
          "name": "parent_line",
          "label": "Parent line",
          "value": null,
          "display_value": "",
          "type": "reference"
        },
        "unit_net_price": {
          "name": "unit_net_price",
          "label": "Unit net price",
          "value": "0",
          "display_value": "£0.00",
          "type": "currency"
        },
        "quantity": {
          "name": "quantity",
          "label": "Quantity",
          "value": "2",
          "display_value": "2",
          "type": "decimal"
        },
        "unit_of_measure": null,
        "shipping_location": {
          "name": "shipping_location",
          "label": "Shipping location",
          "value": null,
          "display_value": "",
          "type": "reference"
        },
        "total_one_time_price": {
          "name": "total_one_time_price",
          "label": "Total one-time price",
          "value": "0",
          "display_value": "£0.00",
          "type": "currency"
        },
        "total_recurring_price": {
          "name": "total_recurring_price",
          "label": "Total recurring price",
          "value": "0",
          "display_value": "£0.00",
          "type": "currency"
        },
        "top_agreement_line": null,
        "quote_line": {
          "name": "quote_line",
          "label": "Quote line",
          "value": null,
          "display_value": "",
          "type": "reference"
        },
        "sales_agreement_line_characteristics": [
          {
            "sys_id": {
              "label": "Sys ID",
              "value": "b093e08a78755a10f8777f88938ba1e0",
              "displayValue": "b093e08a78755a10f8777f88938ba1e0",
              "type": "GUID"
            },
            "sys_created_by": {
              "name": "sys_created_by",
              "label": "Created by",
              "value": "maint",
              "display_value": "maint",
              "type": "string"
            },
            "sys_updated_by": {
              "name": "sys_updated_by",
              "label": "Updated by",
              "value": "maint",
              "display_value": "maint",
              "type": "string"
            },
            "sys_created_on": {
              "name": "sys_created_on",
              "label": "Created",
              "value": "2024-11-12 08:11:59",
              "display_value": "2024-11-12 00:11:59",
              "type": "glide_date_time"
            },
            "sys_updated_on": {
              "name": "sys_updated_on",
              "label": "Updated",
              "value": "2024-11-12 08:11:59",
              "display_value": "2024-11-12 00:11:59",
              "type": "glide_date_time"
            },
            "sales_agreement": {
              "name": "sales_agreement",
              "label": "Sales agreement",
              "value": "bc93e08a78755a10f8777f88938ba1d8",
              "display_value": "SA0010106",
              "type": "reference"
            },
            "sales_agreement_line": {
              "name": "sales_agreement_line",
              "label": "Sales agreement line",
              "value": "3c93e08a78755a10f8777f88938ba1dd",
              "display_value": "SAL0010126",
              "type": "reference"
            },
            "characteristic": {
              "name": "characteristic",
              "label": "Characteristic",
              "value": "4d289f1a775131108e191e599a5a99c7",
              "display_value": "AC",
              "type": "reference"
            },
            "type": {
              "name": "type",
              "label": "Type",
              "value": "coverage",
              "display_value": "Coverage",
              "type": "string"
            },
            "characteristic_option": {
              "name": "characteristic_option",
              "label": "Characteristic option",
              "value": null,
              "display_value": "",
              "type": "reference"
            },
            "value": {
              "name": "value",
              "label": "Value",
              "value": null,
              "display_value": "",
              "type": "string"
            }
          }
        ],
        "sales_agreement_line_adjustments": [
          {
            "sys_id": {
              "label": "Sys ID",
              "value": "7093e08a78755a10f8777f88938ba1e1",
              "displayValue": "7093e08a78755a10f8777f88938ba1e1",
              "type": "GUID"
            },
            "sys_created_by": {
              "name": "sys_created_by",
              "label": "Created by",
              "value": "maint",
              "display_value": "maint",
              "type": "string"
            },
            "sys_updated_by": {
              "name": "sys_updated_by",
              "label": "Updated by",
              "value": "maint",
              "display_value": "maint",
              "type": "string"
            },
            "sys_created_on": {
              "name": "sys_created_on",
              "label": "Created",
              "value": "2024-11-12 08:11:59",
              "display_value": "2024-11-12 00:11:59",
              "type": "glide_date_time"
            },
            "sys_updated_on": {
              "name": "sys_updated_on",
              "label": "Updated",
              "value": "2024-11-12 08:11:59",
              "display_value": "2024-11-12 00:11:59",
              "type": "glide_date_time"
            },
            "sales_agreement": {
              "name": "sales_agreement",
              "label": "Sales agreement",
              "value": "bc93e08a78755a10f8777f88938ba1d8",
              "display_value": "SA0010106",
              "type": "reference"
            },
            "sales_agreement_line": {
              "name": "sales_agreement_line",
              "label": "Sales Agreement Line",
              "value": "3c93e08a78755a10f8777f88938ba1dd",
              "display_value": "SAL0010126",
              "type": "reference"
            },
            "adjustment_type": {
              "name": "adjustment_type",
              "label": "Adjustment type",
              "value": "d88bc79653dd91105c0eddeeff7b12c1",
              "display_value": "Markup amount",
              "type": "reference"
            },
            "adjustment_source": {
              "name": "adjustment_source",
              "label": "Adjustment source",
              "value": "MANUAL",
              "display_value": "Manual",
              "type": "string"
            },
            "adjustment_value": {
              "name": "adjustment_value",
              "label": "Adjustment value",
              "value": "123",
              "display_value": "123",
              "type": "decimal"
            },
            "applicable_to": {
              "name": "applicable_to",
              "label": "Applicable to",
              "value": "UNIT_QTY",
              "display_value": "Unit Quantity",
              "type": "string"
            },
            "short_description": {
              "name": "short_description",
              "label": "Short description",
              "value": "line adjustment",
              "display_value": "line adjustment",
              "type": "string"
            },
            "number": {
              "name": "number",
              "label": "Number",
              "value": "SALA0010031",
              "display_value": "SALA0010031",
              "type": "string"
            },
            "quantity": {
              "name": "quantity",
              "label": "Quantity",
              "value": "3",
              "display_value": "3",
              "type": "integer"
            },
            "total_amount": {
              "name": "total_amount",
              "label": "Total amount",
              "value": "0",
              "display_value": "£0.00",
              "type": "currency"
            },
            "amount": {
              "name": "amount",
              "label": "Amount",
              "value": "0",
              "display_value": "£0.00",
              "type": "currency"
            }
          }
        ],
        "child_sales_agreement_lines": [
          {
            "sys_id": {
              "label": "Sys ID",
              "value": "7893e08a78755a10f8777f88938ba1e2",
              "displayValue": "7893e08a78755a10f8777f88938ba1e2",
              "type": "GUID"
            },
            "sys_created_by": {
              "name": "sys_created_by",
              "label": "Created by",
              "value": "maint",
              "display_value": "maint",
              "type": "string"
            },
            "sys_updated_by": {
              "name": "sys_updated_by",
              "label": "Updated by",
              "value": "maint",
              "display_value": "maint",
              "type": "string"
            },
            "sys_created_on": {
              "name": "sys_created_on",
              "label": "Created",
              "value": "2024-11-12 08:11:59",
              "display_value": "2024-11-12 00:11:59",
              "type": "glide_date_time"
            },
            "sys_updated_on": {
              "name": "sys_updated_on",
              "label": "Updated",
              "value": "2024-11-12 08:11:59",
              "display_value": "2024-11-12 00:11:59",
              "type": "glide_date_time"
            },
            "number": {
              "name": "number",
              "label": "Number",
              "value": "SAL0010127",
              "display_value": "SAL0010127",
              "type": "string"
            },
            "sales_agreement": {
              "name": "sales_agreement",
              "label": "Sales agreement",
              "value": "bc93e08a78755a10f8777f88938ba1d8",
              "display_value": "SA0010106",
              "type": "reference"
            },
            "short_description": {
              "name": "short_description",
              "label": "Short description",
              "value": "this is sample sa line 1",
              "display_value": "this is sample sa line 1",
              "type": "string"
            },
            "start_date": {
              "name": "start_date",
              "label": "Start date",
              "value": "2024-02-01",
              "display_value": "2024-02-01",
              "type": "glide_date"
            },
            "end_date": {
              "name": "end_date",
              "label": "End date",
              "value": "2024-11-30",
              "display_value": "2024-11-30",
              "type": "glide_date"
            },
            "state": {
              "name": "state",
              "label": "State",
              "value": "active",
              "display_value": "Active",
              "type": "string"
            },
            "product_offering": {
              "name": "product_offering",
              "label": "Product offering",
              "value": null,
              "display_value": "",
              "type": "reference"
            },
            "product_specification": {
              "name": "product_specification",
              "label": "Product specification",
              "value": null,
              "display_value": "",
              "type": "reference"
            },
            "product_model": {
              "name": "product_model",
              "label": "Product model",
              "value": null,
              "display_value": "",
              "type": "reference"
            },
            "price_list": {
              "name": "price_list",
              "label": "Price list",
              "value": "19d29513d0e63110f8770dbf976be122",
              "display_value": "Standard Price List",
              "type": "reference"
            },
            "parent_line": {
              "name": "parent_line",
              "label": "Parent line",
              "value": "3c93e08a78755a10f8777f88938ba1dd",
              "display_value": "SAL0010126",
              "type": "reference"
            },
            "unit_net_price": {
              "name": "unit_net_price",
              "label": "Unit net price",
              "value": "0",
              "display_value": "£0.00",
              "type": "currency"
            },
            "quantity": {
              "name": "quantity",
              "label": "q",
              "value": "2",
              "display_value": "2",
              "type": "decimal"
            },
            "unit_of_measure": null,
            "shipping_location": {
              "name": "shipping_location",
              "label": "Shipping location",
              "value": null,
              "display_value": "",
              "type": "reference"
            },
            "total_one_time_price": {
              "name": "total_one_time_price",
              "label": "Total one-time price",
              "value": "0",
              "display_value": "£0.00",
              "type": "currency"
            },
            "total_recurring_price": {
              "name": "total_recurring_price",
              "label": "Total recurring price",
              "value": "0",
              "display_value": "£0.00",
              "type": "currency"
            },
            "top_agreement_line": null,
            "quote_line": {
              "name": "quote_line",
              "label": "Quote line",
              "value": null,
              "display_value": "",
              "type": "reference"
            },
            "sales_agreement_line_characteristics": [
              {
                "sys_id": {
                  "label": "Sys ID",
                  "value": "74932c8a78755a10f8777f88938ba132",
                  "displayValue": "74932c8a78755a10f8777f88938ba132",
                  "type": "GUID"
                },
                "sys_created_by": {
                  "name": "sys_created_by",
                  "label": "Created by",
                  "display_value": "maint",
                  "type": "string"
                },
                "sys_updated_by": {
                  "name": "sys_updated_by",
                  "label": "Updated by",
                  "value": "maint",
                  "display_value": "maint",
                  "type": "string"
                },
                "sys_created_on": {
                  "name": "sys_created_on",
                  "label": "Created",
                  "value": "2024-11-12 08:11:59",
                  "display_value": "2024-11-12 00:11:59",
                  "type": "glide_date_time"
                },
                "sys_updated_on": {
                  "name": "sys_updated_on",
                  "label": "Updated",
                  "value": "2024-11-12 08:11:59",
                  "display_value": "2024-11-12 00:11:59",
                  "type": "glide_date_time"
                },
                "sales_agreement": {
                  "name": "sales_agreement",
                  "label": "Sales agreement",
                  "value": "bc93e08a78755a10f8777f88938ba1d8",
                  "display_value": "SA0010106",
                  "type": "reference"
                },
                "sales_agreement_line": {
                  "name": "sales_agreement_line",
                  "label": "Sales agreement line",
                  "value": "7893e08a78755a10f8777f88938ba1e2",
                  "display_value": "SAL0010127",
                  "type": "reference"
                },
                "characteristic": {
                  "name": "characteristic",
                  "label": "Characteristic",
                  "value": "4d289f1a775131108e191e599a5a99c7",
                  "display_value": "AC",
                  "type": "reference"
                },
                "type": {
                  "name": "type",
                  "label": "Type",
                  "value": "coverage",
                  "display_value": "Coverage",
                  "type": "string"
                },
                "characteristic_option": {
                  "name": "characteristic_option",
                  "label": "Characteristic option",
                  "value": null,
                  "display_value": "",
                  "type": "reference"
                },
                "value": {
                  "name": "value",
                  "label": "Value",
                  "value": null,
                  "display_value": "",
                  "type": "string"
                }
              }
            ],
            "sales_agreement_line_adjustments": [],
            "child_sales_agreement_lines": []
          },
          {
            "sys_id": {
              "label": "Sys ID",
              "value": "78932c8a78755a10f8777f88938ba133",
              "displayValue": "78932c8a78755a10f8777f88938ba133",
              "type": "GUID"
            },
            "sys_created_by": {
              "name": "sys_created_by",
              "label": "Created by",
              "value": "maint",
              "display_value": "maint",
              "type": "string"
            },
            "sys_updated_by": {
              "name": "sys_updated_by",
              "label": "Updated by",
              "value": "maint",
              "display_value": "maint",
              "type": "string"
            },
            "sys_created_on": {
              "name": "sys_created_on",
              "label": "Created",
              "value": "2024-11-12 08:11:59",
              "display_value": "2024-11-12 00:11:59",
              "type": "glide_date_time"
            },
            "sys_updated_on": {
              "name": "sys_updated_on",
              "label": "Updated",
              "value": "2024-11-12 08:11:59",
              "display_value": "2024-11-12 00:11:59",
              "type": "glide_date_time"
            },
            "number": {
              "name": "number",
              "label": "Number",
              "value": "SAL0010128",
              "display_value": "SAL0010128",
              "type": "string"
            },
            "sales_agreement": {
              "name": "sales_agreement",
              "label": "Sales agreement",
              "value": "bc93e08a78755a10f8777f88938ba1d8",
              "display_value": "SA0010106",
              "type": "reference"
            },
            "short_description": {
              "name": "short_description",
              "label": "Short description",
              "value": "this is sample sa line 1",
              "display_value": "this is sample sa line 1",
              "type": "string"
            },
            "start_date": {
              "name": "start_date",
              "label": "Start date",
              "value": "2024-02-01",
              "display_value": "2024-02-01",
              "type": "glide_date"
            },
            "end_date": {
              "name": "end_date",
              "label": "End date",
              "value": "2024-11-30",
              "display_value": "2024-11-30",
              "type": "glide_date"
            },
            "state": {
              "name": "state",
              "label": "State",
              "value": "active",
              "display_value": "Active",
              "type": "string"
            },
            "product_offering": {
              "name": "product_offering",
              "label": "Product offering",
              "value": null,
              "display_value": "",
              "type": "reference"
            },
            "product_specification": {
              "name": "product_specification",
              "label": "Product specification",
              "value": null,
              "display_value": "",
              "type": "reference"
            },
            "product_model": {
              "name": "product_model",
              "label": "Product model",
              "value": null,
              "display_value": "",
              "type": "reference"
            },
            "price_list": {
              "name": "price_list",
              "label": "Price list",
              "value": "19d29513d0e63110f8770dbf976be122",
              "display_value": "Standard Price List",
              "type": "reference"
            },
            "parent_line": {
              "name": "parent_line",
              "label": "Parent line",
              "value": "3c93e08a78755a10f8777f88938ba1dd",
              "display_value": "SAL0010126",
              "type": "reference"
            },
            "unit_net_price": {
              "name": "unit_net_price",
              "label": "Unit net price",
              "value": "0",
              "display_value": "£0.00",
              "type": "currency"
            },
            "quantity": {
              "name": "quantity",
              "label": "Quantity",
              "value": "2",
              "display_value": "2",
              "type": "decimal"
            },
            "unit_of_measure": null,
            "shipping_location": {
              "name": "shipping_location",
              "label": "Shipping location",
              "value": null,
              "display_value": "",
              "type": "reference"
            },
            "total_one_time_price": {
              "name": "total_one_time_price",
              "label": "Total one-time price",
              "value": "0",
              "display_value": "£0.00",
              "type": "currency"
            },
            "total_recurring_price": {
              "name": "total_recurring_price",
              "label": "Total recurring price",
              "value": "0",
              "display_value": "£0.00",
              "type": "currency"
            },
            "top_agreement_line": null,
            "quote_line": {
              "name": "quote_line",
              "label": "Quote line",
              "value": null,
              "display_value": "",
              "type": "reference"
            },
            "sales_agreement_line_characteristics": [
              {
                "sys_id": {
                  "label": "Sys ID",
                  "value": "38932c8a78755a10f8777f88938ba134",
                  "displayValue": "38932c8a78755a10f8777f88938ba134",
                  "type": "GUID"
                },
                "sys_created_by": {
                  "name": "sys_created_by",
                  "label": "Created by",
                  "value": "maint",
                  "display_value": "maint",
                  "type": "string"
                },
                "sys_updated_by": {
                  "name": "sys_updated_by",
                  "label": "Updated by",
                  "value": "maint",
                  "display_value": "maint",
                  "type": "string"
                },
                "sys_created_on": {
                  "name": "sys_created_on",
                  "label": "Created",
                  "value": "2024-11-12 08:11:59",
                  "display_value": "2024-11-12 00:11:59",
                  "type": "glide_date_time"
                },
                "sys_updated_on": {
                  "name": "sys_updated_on",
                  "label": "Updated",
                  "value": "2024-11-12 08:11:59",
                  "display_value": "2024-11-12 00:11:59",
                  "type": "glide_date_time"
                },
                "sales_agreement": {
                  "name": "sales_agreement",
                  "label": "Sales agreement",
                  "value": "bc93e08a78755a10f8777f88938ba1d8",
                  "display_value": "SA0010106",
                  "type": "reference"
                },
                "sales_agreement_line": {
                  "name": "sales_agreement_line",
                  "label": "Sales agreement line",
                  "value": "78932c8a78755a10f8777f88938ba133",
                  "display_value": "SAL0010128",
                  "type": "reference"
                },
                "characteristic": {
                  "name": "characteristic",
                  "label": "Characteristic",
                  "value": "4d289f1a775131108e191e599a5a99c7",
                  "display_value": "AC",
                  "type": "reference"
                },
                "type": {
                  "name": "type",
                  "label": "Type",
                  "value": "coverage",
                  "display_value": "Coverage",
                  "type": "string"
                },
                "characteristic_option": {
                  "name": "characteristic_option",
                  "label": "Characteristic option",
                  "value": null,
                  "display_value": "",
                  "type": "reference"
                },
                "value":
                  "name": "value",
                  "label": "Value",
                  "value": null,
                  "display_value": "",
                  "type": "string"
                }
              }
            ],
            "sales_agreement_line_adjustments": [],
            "child_sales_agreement_lines": []
          }
        ]
      }
    ]
  }
}
```

### cURL request

The following example returns the sales agreement information associated with the given sys\_id and the optional **display\_value** parameter set to `true` so that display values are provided in the response body.

```

curl "https://instance.service-now.com/api/sn_sales_agmt_core/v1/salesagreement/eb853fe5b5165610f87786d3c2884335?display_value=true" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
```

Response body. The response shows the display\_values for every parameter of the given sales agreement.

```
{
  "result": {
    "sys_id": {
      "display_value": "eb853fe5b5165610f87786d3c2884335"
    },
    "sys_created_by": {
      "display_value": "maint"
    },
    "sys_updated_by": {
      "display_value": "maint"
    },
    "sys_created_on": {
      "display_value": "2024-12-05 22:43:51"
    },
    "sys_updated_on": {
      "display_value": "2024-12-05 22:43:51"
    },
    "account": {
      "display_value": "Boxeo"
    },
    "consumer": {
      "display_value": ""
    },
    "number": {
      "display_value": "SA0010004"
    },
    "state": {
      "display_value": "Active"
    },
    "starts": {
      "display_value": "2024-01-01"
    },
    "ends": {
      "display_value": "2024-12-31"
    },
    "short_description": {
      "display_value": "This is a Sa created by API"
    },
    "currency": {
      "display_value": "USD"
    },
    "default_price_list": {
      "display_value": "SA Price List"
    },
    "billing_location": {
      "display_value": "100 South Charles Street, Baltimore,MD"
    },
    "contact": {
      "display_value": "Alex Linde"
    },
    "shipping_location": {
      "display_value": "100 South Charles Street, Baltimore,MD"
    },
    "quote": {
      "display_value": "QT0000001"
    },
    "sales_agreement_lines": [
      {
        "sys_id": {
          "display_value": "af853fe5b5165610f87786d3c2884339"
        },
        "sys_created_by": {
          "display_value": "maint"
        },
        "sys_updated_by": {
          "display_value": "maint"
        },
        "sys_created_on": {
          "display_value": "2024-12-05 22:43:51"
        },
        "sys_updated_on": {
          "display_value": "2024-12-05 22:43:51"
        },
        "number": {
          "display_value": "SAL0010003"
        },
        "sales_agreement": {
          "display_value": "SA0010004"
        },
        "short_description": {
          "display_value": "this is sample sa line 1"
        },
        "start_date": {
          "display_value": "2024-11-10"
        },
        "end_date": {
          "display_value": "2024-12-31"
        },
        "state": {
          "display_value": "Active"
        },
        "product_offering": {
          "display_value": "Home Automation Bundle"
        },
        "product_specification": {
          "display_value": ""
        },
        "product_model": {
          "display_value": ""
        },
        "price_list": {
          "display_value": "SA Price List"
        },
        "parent_line": {
          "display_value": ""
        },
        "unit_net_price": {
          "display_value": "£314.2315"
        },
        "quantity": {
          "display_value": "2"
        },
        "unit_of_measurement": {
          "display_value": "Each"
        },
        "shipping_location": {
          "display_value": "100 South Charles Street, Baltimore,MD"
        },
        "total_one_time_price": {
          "display_value": "£314.2315"
        },
        "total_recurring_price": {
          "display_value": "£0.00"
        },
        "top_sales_agreement_line": {
          "display_value": "SAL0010003"
        },
        "quote_line": {
          "display_value": ""
        },
        "child_sales_agreement_lines": [
          {
            "sys_id": {
              "display_value": "eb85f329b5165610f87786d3c2884318"
            },
            "sys_created_by": {
              "display_value": "maint"
            },
            "sys_updated_by": {
              "display_value": "maint"
            },
            "sys_created_on": {
              "display_value": "2024-12-05 22:43:51"
            },
            "sys_updated_on": {
              "display_value": "2024-12-05 22:43:51"
            },
            "number": {
              "display_value": "SAL0010004"
            },
            "sales_agreement": {
              "display_value": "SA0010004"
            },
            "short_description": {
              "display_value": "this is sample child sa line 1"
            },
            "start_date": {
              "display_value": "2024-11-11"
            },
            "end_date": {
              "display_value": "2024-12-31"
            },
            "state": {
              "display_value": "Active"
            },
            "product_offering": {
              "display_value": "Home Automation Hub"
            },
            "product_specification": {
              "display_value": ""
            },
            "product_model": {
              "display_value": ""
            },
            "price_list": {
              "display_value": "SA Price List"
            },
            "parent_line": {
              "display_value": "SAL0010003"
            },
            "unit_net_price": {
              "display_value": "£94.2694"
            },
            "quantity": {
              "display_value": "2"
            },
            "unit_of_measurement": {
              "display_value": "Each"
            },
            "shipping_location": {
              "display_value": "100 South Charles Street, Baltimore,MD"
            },
            "total_one_time_price": {
              "display_value": "£94.2694"
            },
            "total_recurring_price": {
              "display_value": "£0.00"
            },
            "top_sales_agreement_line": {
              "display_value": "SAL0010003"
            },
            "quote_line": {
              "display_value": ""
            },
            "child_sales_agreement_lines": [],
            "sales_agreement_line_characteristics": [
              {
                "sys_id": {
                  "display_value": "e385f329b5165610f87786d3c288431a"
                },
                "sys_created_by": {
                  "display_value": "maint"
                },
                "sys_updated_by": {
                  "display_value": "maint"
                },
                "sys_created_on": {
                  "display_value": "2024-12-05 22:43:51"
                },
                "sys_updated_on": {
                  "display_value": "2024-12-05 22:43:51"
                },
                "sales_agreement": {
                  "display_value": "SA0010004"
                },
                "sales_agreement_line": {
                  "display_value": "SAL0010004"
                },
                "characteristic": {
                  "display_value": "Connectivity Tech"
                },
                "type": {
                  "display_value": null
                },
                "characteristic_option": {
                  "display_value": "3G"
                },
                "value": {
                  "display_value": "3G"
                }
              }
            ],
            "sales_agreement_line_adjustments": [
              {
                "sys_id": {
                  "display_value": "2385f329b5165610f87786d3c288431b"
                },
                "sys_created_by": {
                  "display_value": "maint"
                },
                "sys_updated_by": {
                  "display_value": "maint"
                },
                "sys_created_on": {
                  "display_value": "2024-12-05 22:43:51"
                },
                "sys_updated_on": {
                  "display_value": "2024-12-05 22:43:51"
                },
                "sales_agreement": {
                  "display_value": "SA0010004"
                },
                "sales_agreement_line": {
                  "display_value": "SAL0010004"
                },
                "adjustment_type": {
                  "display_value": "Markdown %"
                },
                "adjustment_source": {
                  "display_value": "Manual"
                },
                "adjustment_value": {
                  "display_value": "20"
                },
                "applicable_to": {
                  "display_value": "Unit Quantity"
                },
                "short_description": {
                  "display_value": "Price adjustment"
                },
                "number": {
                  "display_value": "SALA0010004"
                },
                "quantity": {
                  "display_value": "1"
                },
                "total_amount": {
                  "display_value": "£28.00"
                },
                "amount": {
                  "display_value": "£28.00"
                }
              }
            ]
          }
        ],
        "sales_agreement_line_characteristics": [
          {
            "sys_id": {
              "display_value": "a785f329b5165610f87786d3c2884315"
            },
            "sys_created_by": {
              "display_value": "maint"
            },
            "sys_updated_by": {
              "display_value": "maint"
            },
            "sys_created_on": {
              "display_value": "2024-12-05 22:43:51"
            },
            "sys_updated_on": {
              "display_value": "2024-12-05 22:43:51"
            },
            "sales_agreement": {
              "display_value": "SA0010004"
            },
            "sales_agreement_line": {
              "display_value": "SAL0010003"
            },
            "characteristic": {
              "display_value": "Connectivity Tech"
            },
            "type": {
              "display_value": null
            },
            "characteristic_option": {
              "display_value": "3G"
            },
            "value": {
              "display_value": "3G"
            }
          }
        ],
        "sales_agreement_line_adjustments": [
          {
            "sys_id": {
              "display_value": "2b85f329b5165610f87786d3c2884316"
            },
            "sys_created_by": {
              "display_value": "maint"
            },
            "sys_updated_by": {
              "display_value": "maint"
            },
            "sys_created_on": {
              "display_value": "2024-12-05 22:43:51"
            },
            "sys_updated_on": {
              "display_value": "2024-12-05 22:43:51"
            },
            "sales_agreement": {
              "display_value": "SA0010004"
            },
            "sales_agreement_line": {
              "display_value": "SAL0010003"
            },
            "adjustment_type": {
              "display_value": "Markdown %"
            },
            "adjustment_source": {
              "display_value": "Auto"
            },
            "adjustment_value": {
              "display_value": "10"
            },
            "applicable_to": {
              "display_value": "Unit Quantity"
            },
            "short_description": {
              "display_value": "Price adjustment"
            },
            "number": {
              "display_value": "SALA0010003"
            },
            "quantity": {
              "display_value": "3"
            },
            "total_amount": {
              "display_value": "£120.00"
            },
            "amount": {
              "display_value": "£40.00"
            }
          }
        ]
      }
    ]
  }
}
```

## Sales Agreement - POST /api/sn\_sales\_agmt\_core/salesagreement

Creates a new sales agreement  according to details provided in the request body.

### URL format

Versioned URL: `/api/sn_sales_agmt_core/v1/salesagreement`

Default URL: `/api/sn_sales_agmt_core/salesagreement`

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

### Supported request parameters

<table id="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`. Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

account

</td><td>

Required. Sys\_id of the account.Table: Account \[customer\_account\]

Data type: String

</td></tr><tr><td>

billing\_location

</td><td>

Billing address of the new sales agreement.Table: Location \[location\]

Data type: String

Default: empty string

</td></tr><tr><td>

contact

</td><td>

Sys\_id the contact.Table: Contact \[customer\_contact\]

Data type: String

Default: null

</td></tr><tr><td>

currency

</td><td>

Country currency code to use in the new sales agreement. For example, `USD` or `EUR`.Table: Currency \[fx\_currency\]

Data type: Number \(decimal\)

Default: 0

</td></tr><tr><td>

default\_price\_list

</td><td>

Required. Sys\_id of the price list.Table: Price List \[sn\_csm\_pricing\_price\_list\]

Data type: String

</td></tr><tr><td>

ends

</td><td>

Required. End date of the sales agreement.Format: YYYY-MM-DD

Data type: String

</td></tr><tr><td>

quote

</td><td>

Sys\_id of the quote.Table: Quote \[sn\_quote\_mgmt\_core\_quote\]

Data type: String

</td></tr><tr><td>

sales\_agreement\_lines

</td><td>

List of sales agreement lines under the sales agreement.Table: Sales Agreement Line  \[sn\_sales\_agmt\_core\_sales\_agreement\_line\]

Data type: Array of objects

```
"sales_agreement_lines": [ 
  {
  "child_sales_agreement_lines": [Array],
  "end_date": "String",
  "price_list": "String",
  "product_model": "String", 
  "product_offering": "String", 
  "product_specification": "String",
  "quantity": Number,
  "quote_line": "String",
  "sales_agreement_line_adjustments": [Array], 
  "sales_agreement_line_characteristics": [Array]
  "shipping_location": "String",
  "short_description": "String",
  "start_date": "String",
  "state": "String",
  "total_one_time_price": "String",
  "unit_net_price": "String"
  "unit_of_measurement": "String",
  }
]
```

</td></tr><tr><td>

sales\_agreement\_lines.child\_sales\_agreement\_lines

</td><td>

List of child sales agreement lines to associate with the parent sales agreement. Follows the same object structure as the **sales\_agreement\_lines** object parameter.Table: Sales Agreement Line  \[sn\_sales\_agmt\_core\_sales\_agreement\_line\]

Data type: Array of objects  

```
"child_sales_agreement_lines": [ 
  {
  "end_date": "String",
  "price_list": "String",
  "product_model": "String",
  "product_offering": "String", 
  "product_specification": "String", 
  "quantity": Number, 
  "quote_line": "String",
  "sales_agreement_line_adjustments": [Array], 
  "sales_agreement_line_characteristics": [Array],
  "shipping_location": "String",
  "short_description": "String",
  "start_date": "String",
  "state": "String",
  "total_one_time_price": "String", 
  "total_recurring_price": "String", 
  "unit_net_price": "String",
  "unit_of_measurement": "String"
  } 
]
```

</td></tr><tr><td>

sales\_agreement\_lines.child\_sales\_agreement\_lines.end\_date

</td><td>

Start date of the sales agreement line.Format: YYYY-MM-DD

Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.child\_sales\_agreement\_lines.price\_list

</td><td>

Sys\_id of the price list.Table: Price List \[sn\_csm\_pricing\_price\_list\]

Data type: String

Default: null

</td></tr><tr><td>

sales\_agreement\_lines.child\_sales\_agreement\_lines.product\_model

</td><td>

Sys\_id of the product model.Table: Product Model \[cmdb\_model\]

Data type: String

Default: null

</td></tr><tr><td>

sales\_agreement\_lines.child\_sales\_agreement\_lines.product\_offering

</td><td>

Sys\_id of the product offering.Table: Product Offering \[sn\_prd\_pm\_product\_offering\]

Data type: String

Default: null

</td></tr><tr><td>

sales\_agreement\_lines.child\_sales\_agreement\_lines.product\_specification

</td><td>

Sys\_id of the product specification.Table: Product Specification \[sn\_prd\_pm\_product\_specification\]

Data type: String

Default: null

</td></tr><tr><td>

sales\_agreement\_lines.child\_sales\_agreement\_lines.quantity

</td><td>

Number of products to add to the sales agreement line .Table: Product Model \[cmdb\_model\]

Data type: Number \(decimal\)

Default: 0

</td></tr><tr><td>

sales\_agreement\_lines.child\_sales\_agreement\_lines.quote\_line

</td><td>

Sys\_id of the quote line item.Table: Quote Line \[sn\_quote\_mgmt\_core\_quote\_line\_item\]

Data type: String

Default: null

</td></tr><tr><td>

sales\_agreement\_lines.child\_sales\_agreement\_lines.sales\_agreement\_line\_adjustments 

</td><td>

List of price adjustments under the child sales agreement line.  Price adjustment data is inserted in the child sales agreement.Table: Sales Agreement Line Adjustments  \[sn\_sales\_agmt\_core\_sales\_agreement\_line\_adjustment\]

Data type: Array of objects  

```
 "sales_agreement_line_adjustments": [ 
  {
  "adjustment_source": "String", 
  "adjustment_type": "String",
  "adjustment_value": "String", 
  "amount": "String",
  "applicable_to": "String", 
  "quantity": Number, 
  "short_description": "String",
  "total_amount": "String"
  } 
]
```

</td></tr><tr><td>

sales\_agreement\_lines.child\_sales\_agreement\_lines.sales\_agreement\_line\_adjustments.adjustment\_source

</td><td>

Source type of the adjustment.Accepted values:

-   manual
-   auto

Data type: String

Default: manual

</td></tr><tr><td>

sales\_agreement\_lines.child\_sales\_agreement\_lines.sales\_agreement\_line\_adjustments.adjustment\_type

</td><td>

Required. Sys\_id of the adjustment type.Table: Sales Agreement Line Adjustments  \[sn\_sales\_agmt\_core\_sales\_agreement\_line\_adjustment\]

Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.child\_sales\_agreement\_lines.sales\_agreement\_line\_adjustments.adjustment\_value

</td><td>

Required. Value of the price modification.Data type: Number

Table: Sales Agreement Line Adjustments  \[sn\_sales\_agmt\_core\_sales\_agreement\_line\_adjustment\]

Default: 0

</td></tr><tr><td>

sales\_agreement\_lines.child\_sales\_agreement\_lines.sales\_agreement\_line\_adjustments.amount

</td><td>

Amount of the line adjustment.Data type: Number \(decimal\)

Table: Sales Agreement Line Adjustments  \[sn\_sales\_agmt\_core\_sales\_agreement\_line\_adjustment\]

Default: null

</td></tr><tr><td>

sales\_agreement\_lines.child\_sales\_agreement\_lines.sales\_agreement\_line\_adjustments.applicable\_to

</td><td>

Sys\_id of the line adjustment record that this adjustment is applicable to.Data type: String

Table: Sales Agreement Line Adjustments  \[sn\_sales\_agmt\_core\_sales\_agreement\_line\_adjustment\]

Default: null

</td></tr><tr><td>

sales\_agreement\_lines.child\_sales\_agreement\_lines.sales\_agreement\_line\_adjustments.quantity

</td><td>

Number of products to add to the child sales agreement line.Data type: Number

Default: 0

</td></tr><tr><td>

sales\_agreement\_lines.child\_sales\_agreement\_lines.sales\_agreement\_line\_adjustments.short\_description

</td><td>

Brief description of the sales agreement adjustment. Data type: String

Default: Empty string

</td></tr><tr><td>

sales\_agreement\_lines.child\_sales\_agreement\_lines.sales\_agreement\_line\_adjustments.total\_amount

</td><td>

Total amount of the line adjustment. The sum of both the **sales\_agreement\_line\_adjustments.amount** and **sales\_agreement\_line\_adjustments.adjustment\_value** values.Data type: Number \(decimal\)

Default: 0

</td></tr><tr><td>

sales\_agreement\_lines.child\_sales\_agreement\_lines.sales\_agreement\_line\_characteristics 

</td><td>

List of characteristic data to insert in the  child sales agreement line.Table: Sales Agreement Line Characteristics  \[sn\_sales\_agmt\_core\_sales\_agreement\_line\_characteristic\]

Data type: Array of objects  

```
"sales_agreement_line_characteristics": [ 
  { 
  "characteristic": "String",
  "characteristic_option": "String",
  "type": "String", 
  "value": "String" 
  }
]
```

</td></tr><tr><td>

sales\_agreement\_lines.child\_sales\_agreement\_lines.sales\_agreement\_line\_characteristics .characteristic

</td><td>

Required. Sys\_id of a characteristic record. Table: Sales Agreement Line Characteristics  \[sn\_sales\_agmt\_core\_sales\_agreement\_line\_characteristic\]

Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.child\_sales\_agreement\_lines.sales\_agreement\_line\_characteristics .characteristic\_option

</td><td>

Sys\_id of the characteristic option. Table: Sales Agreement Line Characteristics  \[sn\_sales\_agmt\_core\_sales\_agreement\_line\_characteristic\]

Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.child\_sales\_agreement\_lines.sales\_agreement\_line\_characteristics .type

</td><td>

Type of the sales agreement characteristic.Accepted values:

-   coverage
-   coverage and usage

Table: Sales Agreement Line Characteristics  \[sn\_sales\_agmt\_core\_sales\_agreement\_line\_characteristic\]

Data type: String

Default: coverage

</td></tr><tr><td>

sales\_agreement\_lines.child\_sales\_agreement\_lines.sales\_agreement\_line\_characteristics .value

</td><td>

Value of the characteristic.Default: null

Data type: String

Table: Sales Agreement Line Characteristics  \[sn\_sales\_agmt\_core\_sales\_agreement\_line\_characteristic\]

</td></tr><tr><td>

sales\_agreement\_lines.child\_sales\_agreement\_lines.shipping\_location

</td><td>

Reference to the shipping location  of the child sales agreement line.Table: Location \[location\]

Data type: String

Default:

</td></tr><tr><td>

sales\_agreement\_lines.child\_sales\_agreement\_lines.short\_description

</td><td>

Brief details describing the child sales agreement line.Data type: String

Default: Empty string

</td></tr><tr><td>

sales\_agreement\_lines.child\_sales\_agreement\_lines.start\_date

</td><td>

Required. Start date of the child sales agreement line.Format: YYYY-MM-DD

Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.child\_sales\_agreement\_lines.state

</td><td>

Required. Activity state in which to set the new sales agreement line. Accepted values:

-   pending\_activation: Sets the sales agreement line to a pending state.
-   suspended: Sets the sales agreement line to a suspended state.
-   active: Sets the sales agreement line to an active state.
-   expired: Sets the sales agreement in a expired state.
-   cancelled: Sets the sales agreement to a cancelled state.

Data type: String

Default: pending\_activation

</td></tr><tr><td>

sales\_agreement\_lines.child\_sales\_agreement\_lines.total\_one\_time\_price

</td><td>

Total one-time charges to be paid for the product or service.Data type: Number \(decimal\)

Table: Sales Agreement Line  \[sn\_sales\_agmt\_core\_sales\_agreement\_line\]

Default: 0

</td></tr><tr><td>

sales\_agreement\_lines.child\_sales\_agreement\_lines.total\_recurring\_price

</td><td>

Annual price for the product associated with the child line item.Data type: Number \(decimal\)

Table: Sales Agreement Line  \[sn\_sales\_agmt\_core\_sales\_agreement\_line\]

Default: 0

</td></tr><tr><td>

sales\_agreement\_lines.child\_sales\_agreement\_lines.unit\_net\_price

</td><td>

Price per each unit for the product associated with the sales agreement line.Table: Sales Agreement Line  \[sn\_sales\_agmt\_core\_sales\_agreement\_line\]

Data type: String

Default value: 0

</td></tr><tr><td>

sales\_agreement\_lines.end\_date

</td><td>

End date of the sales agreement line.Format: YYYY-MM-DD

Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.price\_list

</td><td>

Sys\_id of the price list associated with the sales agreement line.Table: Price List \[sn\_csm\_pricing\_price\_list\]

Data type: String

Default value: null

</td></tr><tr><td>

sales\_agreement\_lines.product\_model

</td><td>

Sys\_id of the product model associated with the sales agreement line.Table: Product Model \[cmdb\_model\]

Data type: String

Default value: null

</td></tr><tr><td>

sales\_agreement\_lines.product\_offering

</td><td>

Sys\_id  of the product offering associated with the sales agreement line.Table: Product Offering \[sn\_prd\_pm\_product\_offering\]

Data type: String

Default value: null

</td></tr><tr><td>

sales\_agreement\_lines.product\_specification

</td><td>

Sys\_id  of the product specification associated with the sales agreement line.Table: Product Specification \[sn\_prd\_pm\_product\_specification\]

Data type: String

Default value: null

</td></tr><tr><td>

sales\_agreement\_lines.quantity

</td><td>

Number of products to add to the sales agreement line.Data type: Number \(decimal\)

Default: 0

</td></tr><tr><td>

sales\_agreement\_lines.quote\_line

</td><td>

Sys\_id of the quote line item associated with the sales agreement line.Data type: String

Table: Quote Line \[sn\_quote\_mgmt\_core\_quote\_line\_item\]

Default value: null

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments

</td><td>

List of price adjustments to insert under the sales agreement line. Table: Sales Agreement Line Adjustments  \[sn\_sales\_agmt\_core\_sales\_agreement\_line\_adjustment\]

Data type: Array of objects  

```
 "sales_agreement_line_adjustments": [ 
  {
  "adjustment_source": "String", 
  "adjustment_type": "String",
  "adjustment_value": "String", 
  "amount": "String",
  "applicable_to": "String", 
  "quantity": Number, 
  "short_description": "String",
  "total_amount": "String"
  } 
]
```

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.adjustment\_source

</td><td>

Source type of the adjustment.Accepted values:

-   manual
-   auto

Data type: String

Default: manual

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.adjustment\_type

</td><td>

Required. Sys\_id of the adjustment type.Table: Sales Agreement Line Adjustments  \[sn\_sales\_agmt\_core\_sales\_agreement\_line\_adjustment\]

Data type: String

Default: null

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.adjustment\_value

</td><td>

Required. Value of the price adjustment.Data type: Number \(decimal\)

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.amount

</td><td>

Price amount of the line adjustment.Data type: Number \(decimal\)

Default: 0

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.applicable\_to

</td><td>

Quantity type that the sales adjustment is applicable to.Valid values:

-   LUMPSUM\_QTY: lipsum quantity
-   UNIT\_QTY: unit quantity

Data type: String

Default: null

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.quantity

</td><td>

Number of products to add to the sales agreement line adjustment.Table: Sales Agreement Line Adjustments  \[sn\_sales\_agmt\_core\_sales\_agreement\_line\_adjustment\]

Data type: Number \(decimal\)

Default: 0

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.short\_description

</td><td>

Brief description of the sales agreement adjustment. Data type: String

Default: Empty string

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.total\_amount

</td><td>

Total amount of the line adjustment. The sum of both the **sales\_agreement\_line\_adjustments.amount** and **sales\_agreement\_line\_adjustments.adjustment\_value** values.Data type: String

Default: manual

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics

</td><td>

List of characteristics under the  sales agreement line. The data in this parameter   will be inserted in  Sales Agreement Characteristics  record.  Table: Sales Agreement Line Characteristics  \[sn\_sales\_agmt\_core\_sales\_agreement\_line\_characteristic\]

Data type: Array of objects  

```
"sales_agreement_line_characteristics": [ 
  { 
  "characteristic": "String",
  "characteristic_option": "String",
  "type": "String", 
  "value": "String" 
  }
]
```

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics .characteristic

</td><td>

Required. Sys\_id of the sales agreement line characteristic. Table: Sales Agreement Line Characteristics  \[sn\_sales\_agmt\_core\_sales\_agreement\_line\_characteristic\]

Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics .characteristic\_option

</td><td>

The characteristic option associated with the sales agreement line. Table: Product Characteristic Option \[sn\_prd\_pm\_characteristic\_option\]

Data type: String

Default: null

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics .type

</td><td>

Type of the sales agreement characteristic.Accepted values:

-   coverage
-   coverage and usage

Table: Sales Agreement Line Characteristics  \[sn\_sales\_agmt\_core\_sales\_agreement\_line\_characteristic\]

Data type: String

Default: coverage

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics .value

</td><td>

Value of the characteristic.Table: Sales Agreement Line Characteristics  \[sn\_sales\_agmt\_core\_sales\_agreement\_line\_characteristic\]

Data type: String

Default: null

</td></tr><tr><td>

sales\_agreement\_lines.shipping\_location

</td><td>

Reference to the shipping location  of the sales agreement line.Table: Sales Agreement Line  \[sn\_sales\_agmt\_core\_sales\_agreement\_line\]

Data type: String

Default: null

</td></tr><tr><td>

sales\_agreement\_lines.short\_description

</td><td>

Brief details describing the sales agreement line.Data type: String

Default: Empty string

</td></tr><tr><td>

sales\_agreement\_lines.start\_date

</td><td>

Start date of the sales agreement line.Format: YYYY-MM-DD

Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.state

</td><td>

Required. Activity state in which to set the new sales agreement line. Accepted values:

-   pending\_activation: Sets the sales agreement line to a pending state.
-   suspended: Sets the sales agreement line to a suspended state.
-   active: Sets the sales agreement line to an active state.
-   expired: Sets the sales agreement in a expired state.
-   cancelled: Sets the sales agreement to a cancelled state.

Data type: String

Table: Sales Agreement Line  \[sn\_sales\_agmt\_core\_sales\_agreement\_line\]

Default: pending\_activation

</td></tr><tr><td>

sales\_agreement\_lines.total\_one\_time\_price

</td><td>

Total one-time price to be paid for the product or service associated with the sales agreement line.Data type: Number \(decimal\)

Default: 0

</td></tr><tr><td>

sales\_agreement\_lines.unit\_net\_price

</td><td>

The price for each unit within the sales agreement line.Data type: Number \(decimal\)

Default value: 0

</td></tr><tr><td>

sales\_agreement\_lines.unit\_of\_measurement

</td><td>

The unit of measurement. For example, `bundle` or `each`.Table: Unit of measures \[sn\_prd\_pm\_uom\_list\]

Data type: String

Default value: null

</td></tr><tr><td>

shipping\_location

</td><td>

Shipping location of the sales agreement.Table: Location \[location\]

Data type: String

Default: null

</td></tr><tr><td>

short\_description

</td><td>

Brief details describing the sales agreement.Table: Sales Agreement Line  \[sn\_sales\_agmt\_core\_sales\_agreement\_line\]

Data type: String

Default: Empty string

</td></tr><tr><td>

starts

</td><td>

Required. Start date of the sales agreement.Format: YYYY-MM-DD

Data type: String

</td></tr><tr><td>

state

</td><td>

Activity state in which to set the new sales agreement. Accepted values:

-   draft: Sets the sales agreement in a draft state.
-   active: Sets the sales agreement to an active state.
-   expired: Sets the sales agreement in a expired state.
-   cancelled: Sets the sales agreement to a cancelled state.

Table: Sales Agreement Line  \[sn\_sales\_agmt\_core\_sales\_agreement\_line\]

Data type: String

Default: draft

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Only supports **application/json**.|
|Content-Type|Data format of the request body. Only supports **application/json**.|

|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|201|Record is successfully created.|
|400|Bad Request. A bad request type or malformed request was detected.|
|403|Forbidden. The user doesn't have access rights to the specified record.|

### Response body parameters \(JSON or XML\)

<table id="id_axq_ryw_c2c"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

Results of the sales agreement with all its associated information.Data type: Object

```
"result": {
    "account": {Object},
    "billing_location": {Object},
    "consumer": {Object},
    "contact": {Object},
    "currency": {Object},
    "default_price_list": {Object},
    "ends": {Object},
    "number": {Object},
    "quote": {Object},
    "sales_agreement_lines": [Array]
    "shipping_location": {Object},
    "short_description": {Object},
    "starts": {Object},
    "state": {Object},
    "sys_id": {Object},
    "sys_created_by": {Object},
    "sys_created_on": {Object},
    "sys_updated_by": {Object},
    "sys_updated_on": {Object}
}
```

</td></tr><tr><td>

account

</td><td>

Account information associated with the sales agreement.Table: Account \[customer\_account\]

Data type: Object

```
"account": {
 "display_value": "String",
 "label": "String",
 "name": "String",
 "type": "String",
 "value": "String"
}
```

</td></tr><tr><td>

account.display\_value

</td><td>

Display value of the account. Matches **account.value**.Data type: String

</td></tr><tr><td>

account.label

</td><td>

Label of the account.Data type: String

</td></tr><tr><td>

account.name

</td><td>

Name of the account.Data type: String

</td></tr><tr><td>

account.type

</td><td>

Type of account. Value is always `reference`.Data type: String

</td></tr><tr><td>

account.value

</td><td>

Sys\_id of the account.Table: Account \[customer\_account\]

Data type: String

</td></tr><tr><td>

billing\_location

</td><td>

Billing address of the sales agreement.Updated table: Location \[cmn\_location\]

Data type: Object

```
"billing_location": { 
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String"
}
```

</td></tr><tr><td>

billing\_location.display\_value

</td><td>

Display value of the billing location. Matches **billing\_location.value**.Data type: String

</td></tr><tr><td>

billing\_location.label

</td><td>

Label of the billing location.Data type: String

</td></tr><tr><td>

billing\_location.name

</td><td>

Name of the billing location.Data type: String

</td></tr><tr><td>

billing\_location.type

</td><td>

Type of billing location. Value is always `reference`.Data type: String

</td></tr><tr><td>

billing\_location.value

</td><td>

Value of the billing location.Data type: String

</td></tr><tr><td>

consumer

</td><td>

Consumer details of the sales agreement.Table: Consumer \[csm\_consumer\]

Data type: Object

```
"consumer": { 
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String"
}
```

</td></tr><tr><td>

consumer.display\_value

</td><td>

Display value of the consumer. Matches **consumer.value**.Data type: String

</td></tr><tr><td>

consumer.label

</td><td>

Label of the consumer.Data type: String

</td></tr><tr><td>

consumer.name

</td><td>

Name of the consumer.Data type: String

</td></tr><tr><td>

consumer.type

</td><td>

Type of consumer. Value is always `reference`.Data type: String

</td></tr><tr><td>

consumer.value

</td><td>

Value of the consumer.Data type: String

</td></tr><tr><td>

contact

</td><td>

Contact information associated with the sales agreement.Table: Contact \[customer\_contact\]

Data type: Object

```
"contact": { 
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String"
}
```

</td></tr><tr><td>

contact.display\_value

</td><td>

Display value of the contact. Matches **contact.value**.Data type: String

</td></tr><tr><td>

contact.label

</td><td>

Label of the contact.Data type: String

</td></tr><tr><td>

contact.name

</td><td>

Name of the contact. Data type: String

</td></tr><tr><td>

contact.type

</td><td>

Type of contact. Value is always `reference`.Data type: String

</td></tr><tr><td>

contact.value

</td><td>

Value of the contact.Data type: String

</td></tr><tr><td>

currency

</td><td>

Currency code associated with the sales agreement.Table: Currency \[fx\_currency\]

Data type: Object

```
"currency": { 
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String"
}
```

</td></tr><tr><td>

currency.display\_value

</td><td>

Display value of the currency. Matches **currency.value**. For example, `USD`.Data type: String

</td></tr><tr><td>

currency.label

</td><td>

Label of the currency.Data type: String

</td></tr><tr><td>

currency.name

</td><td>

Name of the currency.Data type: String

</td></tr><tr><td>

currency.type

</td><td>

Type of currency. Value is always `reference`.Data type: String

</td></tr><tr><td>

currency.value

</td><td>

Country currency code of the currency. For example, `USD`.Data type: String

</td></tr><tr><td>

default\_price\_list

</td><td>

Details about the default price list of the sales agreement.Table: Price List \[sn\_csm\_pricing\_price\_list\]

Data type: Object

```
"default_price_list": {
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String" 
}
```

</td></tr><tr><td>

default\_price\_list.display\_value

</td><td>

Display value of the default price list.Data type: String

</td></tr><tr><td>

default\_price\_list.label

</td><td>

Label of the default price list.Data type: String

</td></tr><tr><td>

default\_price\_list.name

</td><td>

Name of the default price list.Data type: String

</td></tr><tr><td>

default\_price\_list.type

</td><td>

Type of default price list. Value is always `reference`.Data type: String

</td></tr><tr><td>

default\_price\_list.value

</td><td>

Sys\_id of the default price list.Data type: String

</td></tr><tr><td>

ends

</td><td>

End date of the sales agreement.Data type: Object

```
"ends": {
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String" 
}
```

</td></tr><tr><td>

ends.display\_value

</td><td>

Display value of the end date. Matches **end.value**.Data type: String

</td></tr><tr><td>

ends.label

</td><td>

Label of the end date.Data type: String

</td></tr><tr><td>

ends.label

</td><td>

Name of the end date.Data type: String

</td></tr><tr><td>

ends.type

</td><td>

Type of end date. Value is always `glide_date`.Data type: String

</td></tr><tr><td>

ends.value

</td><td>

Value of the end date.Format: YYYY-MM-DD

Data type: String

</td></tr><tr><td>

number

</td><td>

Automatically generated sales agreement number or the number posted .Table: Sales Agreement  \[sn\_sales\_agmt\_core\_sales\_agreement\]

Data type: Object

```
"number": { 
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String"
}
```

</td></tr><tr><td>

number.display\_value

</td><td>

Display value of the sales agreement number. Matches **number.value**.Data type: String

</td></tr><tr><td>

number.label

</td><td>

Label of the sales agreement number.Data type: String

</td></tr><tr><td>

number.name

</td><td>

Name of the sales agreement number.Data type: String

</td></tr><tr><td>

number.type

</td><td>

Type of sales agreement number. Value is always `String`.Data type: String

</td></tr><tr><td>

number.value

</td><td>

Value of the sales agreement number. For example, `SA0010106`.Data type: String

</td></tr><tr><td>

quote

</td><td>

Information about the sales agreement quote.Table: Quote \[sn\_quote\_mgmt\_core\_quote\]

Data type: Object

```
"quote": { 
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String"
}
```

</td></tr><tr><td>

quote.display\_value

</td><td>

Display value of the quote.Data type: String

</td></tr><tr><td>

quote.label

</td><td>

Label of the quote.Data type: String

</td></tr><tr><td>

quote.name

</td><td>

Name of the quote.Data type: String

</td></tr><tr><td>

quote.type

</td><td>

Type of quote. Value is always `reference`.Data type: String

</td></tr><tr><td>

quote.value

</td><td>

Sys\_id of the quote.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines

</td><td>

List of sales agreement lines under the  sales agreement. Table: Sales Agreement Line  \[sn\_sales\_agmt\_core\_sales\_agreement\_line\]

Data type: Array of objects

```
sales_agreement_lines": [
  {
  "child_sales_agreement_lines": [Array]
  "end_date": {Object},
  "number": {Object},
  "parent_line": {Object},
  "price_list": {Object},
  "product_model": {Object},
  "product_offering": {Object},
  "product_specification": {Object},
  "quantity": {Object},
  "quote_line": {Object},
  "sales_agreement": {Object},
  "sales_agreement_line_characteristics": [Array],
  "sales_agreement_line_adjustments": [Array],
  "shipping_location": {Object},
  "short_description": {Object},
  "start_date": {Object},
  "state": {Object},
  "sys_id": {Object},
  "sys_created_by": {Object},
  "sys_created_on": {Object},
  "sys_updated_by": {Object},
  "sys_updated_on": {Object},
  "top_sales_agreement_line": {Object},
  "total_one_time_price": {Object},
  "total_recurring_price": {Object},
  "unit_net_price": {Object},
  "unit_of_measure": {Object},
  }
]
```

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments

</td><td>

List of sales agreement line adjustments.Table: Sales Agreement Line Adjustments  \[sn\_sales\_agmt\_core\_sales\_agreement\_line\_adjustment\]

Data type: Array of objects

```
"sales_agreement_line_adjustments": [
  {
  "adjustment_source": {Object},
  "adjustment_type": {Object},
  "adjustment_value": {Object},
  "amount": {Object},
  "applicable_to": {Object},
  "number": {Object},
  "quantity": {Object},
  "sales_agreement": {Object},
  "sales_agreement_line": {Object},
  "short_description": {Object},
  "sys_id": {Object},
  "sys_created_by": {Object},
  "sys_updated_by": {Object},
  "sys_created_on": {Object},
  "sys_updated_on": {Object},
  "total_amount": {Object}
  }
]
```

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.adjustment\_source

</td><td>

Source information of the sales agreement line adjustment.Table: Sales Agreement Line Adjustments  \[sn\_sales\_agmt\_core\_sales\_agreement\_line\_adjustment\]

Data type: Object

```
"adjustment_source": { 
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String"
}
```

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.adjustment\_source.display\_value

</td><td>

Source display value of the sales agreement line adjustment. Matches **sales agreement line adjustment.value**.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.adjustment\_source.label

</td><td>

Source label of the sales agreement line adjustment.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.adjustment\_source.name

</td><td>

Source name of the sales agreement line adjustment.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.adjustment\_source.type

</td><td>

Source type of sales agreement line adjustment. Value is always `string`.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.adjustment\_source.value

</td><td>

Source value of the sales agreement line adjustment.Possible values:

-   auto
-   manual

Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.adjustment\_type

</td><td>

Information about the sales agreement line adjustment type.Data type: Object

```
"adjustment_type": { 
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String"
}
```

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.adjustment\_type.display\_value

</td><td>

Display value of the adjustment type.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.adjustment\_type.label

</td><td>

Label of the adjustment type.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.adjustment\_type.name

</td><td>

Name of the adjustment type.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.adjustment\_type.type

</td><td>

Type of adjustment type. Value is always `reference`.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.adjustment\_type.value

</td><td>

Sys\_id of the adjustment type.Table: Sales Agreement Line Adjustments  \[sn\_sales\_agmt\_core\_sales\_agreement\_line\_adjustment\]

Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.adjustment\_value

</td><td>

Information about the adjustment value.Table: Sales Agreement Line Adjustments  \[sn\_sales\_agmt\_core\_sales\_agreement\_line\_adjustment\]

Data type: Object

```
"adjustment_type": { 
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String"
}
```

</td></tr><tr><td>

sales\_agreement\_lines.agreement\_line\_adjustments.adjustment\_value.display\_value

</td><td>

Display value of the adjustment value. Matches **adjustment\_value.value**.Data type: Number \(decimal\)

</td></tr><tr><td>

sales\_agreement\_lines.agreement\_line\_adjustments.adjustment\_value.label

</td><td>

Label of the adjustment value.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.agreement\_line\_adjustments.adjustment\_value.name

</td><td>

Name of the adjustment value.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.agreement\_line\_adjustments.adjustment\_value.type

</td><td>

Type of adjustment. Value is always `decimal`.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.agreement\_line\_adjustments.adjustment\_value.value

</td><td>

Number value of the adjustment.Data type: Number \(decimal\)

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.amount

</td><td>

Information about the amount of the sales agreement line adjustment.Table: Sales Agreement Line Adjustments  \[sn\_sales\_agmt\_core\_sales\_agreement\_line\_adjustment\]

Data type: Object

```
"amount": { 
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String"
}
```

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.amount.display\_value

</td><td>

Display value of the adjustment amount. Matches **amount.value**. Automatically includes the dollar sign of the associated currency \(for example, `$0.00` when **currency** is set to `USD`\).Data type: Number \(decimal\)

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.amount.label

</td><td>

Label of the adjustment amount.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.amount.name

</td><td>

Name of the adjustment amount.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.amount.type

</td><td>

Type of the adjustment amount. Value is always `currency`.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.amount.value

</td><td>

Dollar value of the adjustment amount.Data type: Number

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.applicable\_to

</td><td>

Reference of the entity that the adjustment is applicable to.Table: Sales Agreement Line Adjustments  \[sn\_sales\_agmt\_core\_sales\_agreement\_line\_adjustment\]

Data type: Object

```
"applicable_to": { 
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String"
}
```

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.applicable\_to.display\_value

</td><td>

Display value of the entity that the adjustment is applicable to. Matches **applicable\_to.value**.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.applicable\_to.label

</td><td>

Label of the entity that the adjustment is applicable to.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.applicable\_to.name

</td><td>

Name of the entity that the adjustment is applicable to.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.applicable\_to.type

</td><td>

Type of the entity that the adjustment is applicable to. Value is always `String`.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.applicable\_to.value

</td><td>

Quantity type that the line adjustment is applicable to.Possible values:

-   LUMPSUM\_QTY: lipsum quantity
-   UNIT\_QTY: unit quantity

Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.number

</td><td>

Automatically generated sales agreement line adjustments number or the number posted.Table: Sales Agreement Line Adjustments  \[sn\_sales\_agmt\_core\_sales\_agreement\_line\_adjustment\]

Data type: Object

```
"number": { 
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String"
}
```

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.number.display\_value

</td><td>

Display value of the adjustments number. Matches **number.value**.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.number.label

</td><td>

Label of the adjustment number.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.number.name

</td><td>

Name of the adjustment number.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.number.type

</td><td>

Type of the adjustment number. Value is always `string`.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.number.value

</td><td>

Value of the adjustment number. For example, `SALA0010004`.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.quantity

</td><td>

Quantity of product adjusted on the sales agreement line.Table: Sales Agreement Line Adjustments  \[sn\_sales\_agmt\_core\_sales\_agreement\_line\_adjustment\]

Data type: Object

```
"quantity": { 
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String"
}
```

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.quantity.display\_value

</td><td>

Display value of the adjustment quantity. Matches **quantity.value**.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.quantity.label

</td><td>

Label of the adjustment quantity.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.quantity.name

</td><td>

Name of the adjustment quantity.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.quantity.type

</td><td>

Type of the adjustment quantity. Value is always `decimal`.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.quantity.value

</td><td>

Value of the adjustment quantity.Data type: Number

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.sales\_agreement

</td><td>

Reference to the sales agreement associated with the sales agreement line adjustment.Table: Sales Agreement Line Adjustments  \[sn\_sales\_agmt\_core\_sales\_agreement\_line\_adjustment\]

Data type: Object

```
"quantity": { 
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String"
}
```

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.sales\_agreement.display\_value

</td><td>

Display value of the sales agreement associated with the sales agreement line adjustment. For example, `SA0010106`.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.sales\_agreement.label

</td><td>

Label of the sales agreement associated with the sales agreement line adjustment.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.sales\_agreement.name

</td><td>

Name of the sales agreement associated with the sales agreement line adjustment.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.sales\_agreement.type

</td><td>

Type of the sales agreement associated with the sales agreement line adjustment. Value is always `reference`.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.sales\_agreement.value

</td><td>

Sys\_id of the sales agreement associated with the sales agreement line adjustment.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.sales\_agreement\_line

</td><td>

Reference to sales agreement line associated with the sales agreement line adjustment.Table: Sales Agreement Line Adjustments  \[sn\_sales\_agmt\_core\_sales\_agreement\_line\_adjustment\]

Data type: Object

```
"sales_agreement_line": { 
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String"
}
```

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.sales\_agreement\_line.display\_value

</td><td>

Number of the sales agreement associated with the sales agreement line adjustment. For example, `SAL0010126`.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.sales\_agreement\_line.label

</td><td>

Label of the sales agreement associated with the sales agreement line adjustment.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.sales\_agreement\_line.name

</td><td>

Name of the sales agreement associated with the sales agreement line adjustment.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.sales\_agreement\_line.type

</td><td>

Type of the sales agreement associated with the sales agreement line adjustment. Value is always `String`.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.sales\_agreement\_line.value

</td><td>

Sys\_id of the sales agreement associated with the sales agreement line adjustment.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.short\_description

</td><td>

Brief description detailing the sales agreement line adjustment.Table: Sales Agreement Line Adjustments  \[sn\_sales\_agmt\_core\_sales\_agreement\_line\_adjustment\]

Data type: Object

```
"short_description": { 
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String"
}
```

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.short\_description.display\_value

</td><td>

Display value of the short description detailing the particular line adjustment. Matches **short\_description.value**.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.short\_description.label

</td><td>

Label of the short description detailing the particular line adjustment.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.short\_description.name

</td><td>

Name of the short description detailing the particular line adjustment.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.short\_description.type

</td><td>

Type of the short description detailing the particular line adjustment. Value is always `string`.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.short\_description.value

</td><td>

Value of the short description detailing the particular line adjustment.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.sys\_created\_by

</td><td>

Name of the user who created the sales agreement line adjustment.Table: Sales Agreement Line Adjustments  \[sn\_sales\_agmt\_core\_sales\_agreement\_line\_adjustment\]

Data type: Object

```
"created_by": { 
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String"
}
```

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.sys\_created\_by.display\_value

</td><td>

Display value of the user who created the sales agreement line adjustment. Matches **created\_by.value**.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.sys\_created\_by.label

</td><td>

Label of the user who created the sales agreement line adjustment.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.sys\_created\_by.name

</td><td>

Name of the user who created the sales agreement line adjustment.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.sys\_created\_by.type

</td><td>

Type of the user who created the sales agreement line adjustment. Value is always `string`.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.sys\_created\_by.value

</td><td>

Value of the user who created the sales agreement line adjustment.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.sys\_created\_on

</td><td>

Date and time of when the sales agreement line adjustment was created.Data type: Object

```
"created_on": { 
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String"
}
```

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.sys\_created\_on.display\_value

</td><td>

Display value of the date and time that the line adjustment was created. Matches **created\_on.value**.Format: YYYY-MM-DD HH:mm:ss

Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.sys\_created\_on.label

</td><td>

Label of the date and time that the line adjustment was created.Format: YYYY-MM-DD HH:mm:ss

Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.sys\_created\_on.name

</td><td>

Name of the date and time that the line adjustment was created.Format: YYYY-MM-DD HH:mm:ss

Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.sys\_created\_on.type

</td><td>

Type of the date and time that the line adjustment was created. Value is always `glide_date_time`.Format: YYYY-MM-DD HH:mm:ss

Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.sys\_created\_on.value

</td><td>

Value of the date and time that the line adjustment was created.Format: YYYY-MM-DD HH:mm:ss

Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.sys\_id

</td><td>

Sys\_id of the sales agreement line adjustment.Table: Sales Agreement Line Adjustments  \[sn\_sales\_agmt\_core\_sales\_agreement\_line\_adjustment\]

Data type: Object

```
"sys_id": { 
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String"
}
```

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.sys\_id.display\_value

</td><td>

Display value of the line adjustment sys\_id. Matches **sys\_id.value**.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.sys\_id.label

</td><td>

Label of the line adjustment sys\_id.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.sys\_id.name

</td><td>

Name of the line adjustment sys\_id.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.sys\_id.type

</td><td>

Type of the line adjustment sys\_id. Value is always `string`.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.sys\_id.value

</td><td>

Value of the line adjustment sys\_id.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.sys\_updated\_by

</td><td>

Name of the user who last updated the sales agreement line adjustment.Table: Sales Agreement Line Adjustments  \[sn\_sales\_agmt\_core\_sales\_agreement\_line\_adjustment\]

Data type: Object

```
"updated_by": { 
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String"
}
```

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.sys\_updated\_by.display\_value

</td><td>

Display value of the user who last updated the sales agreement line adjustment. Matches **updated\_by.value**.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.sys\_updated\_by.label

</td><td>

Label of the user who last updated the sales agreement line adjustment.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.sys\_updated\_by.name

</td><td>

Name of the user who last updated the sales agreement line adjustment.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.sys\_updated\_by.type

</td><td>

Type of user who last updated the sales agreement line adjustment. Value is always `String`.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.sys\_updated\_by.value

</td><td>

Value of the user who last updated the sales agreement line adjustment.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.sys\_updated\_on

</td><td>

Date and time when the sales agreement line adjustment was updated.Data type: Object

```
"updated_on": { 
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String"
}
```

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.sys\_updated\_on.display\_value

</td><td>

Display value of the date and time that the line adjustment was last updated. Matches **updated\_on.value**.Format: YYYY-MM-DD HH:mm:ss

Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.sys\_updated\_on.label

</td><td>

Label of the date and time that the line adjustment was last updated.Format: YYYY-MM-DD HH:mm:ss

Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.sys\_updated\_on.name

</td><td>

Name of the date and time that the line adjustment was last updated.Format: YYYY-MM-DD HH:mm:ss

Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.sys\_updated\_on.type

</td><td>

Type of date and time that the line adjustment was last updated. Value is always `glide_date_time`.Format: YYYY-MM-DD HH:mm:ss

Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.sys\_updated\_on.value

</td><td>

Value of the date and time that the line adjustment was last updated.Format: YYYY-MM-DD HH:mm:ss

Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.total\_amount

</td><td>

Total amount of the sales agreement line adjustment.Table: Sales Agreement Line Adjustments  \[sn\_sales\_agmt\_core\_sales\_agreement\_line\_adjustment\]

Data type: Object

```
"total_amount": { 
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String"
}
```

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.total\_amount.display\_value

</td><td>

Display value of the total adjustment amount. Matches **total\_amount.value**.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.total\_amount.label

</td><td>

Label of the total adjustment amount.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.total\_amount.name

</td><td>

Name of the total adjustment amount.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.total\_amount.type

</td><td>

Type of the total adjustment amount. Value is always `currency`.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_adjustments.total\_amount.value

</td><td>

Value of the total adjustment amount.Data type: String represented by a number \(float\)

</td></tr><tr><td>

sales\_agreement\_lines.child\_sales\_agreement\_lines

</td><td>

List of sales agreement lines. Follows the same object structure as the **sales\_agreement\_lines** object parameter.Table: Sales Agreement Line  \[sn\_sales\_agmt\_core\_sales\_agreement\_line\]

Data type: Array of objects

```
"child_sales_agreement_lines": [
  {
  "end_date": {Object},
  "number": {Object},
  "parent_line": {Object},
  "price_list": {Object},
  "product_model": {Object},
  "product_offering": {Object},
  "product_specification": {Object},
  "quantity": {Object},
  "quote_line": {Object},
  "sales_agreement": {Object},
  "sales_agreement_line_adjustments": [Array],
  "sales_agreement_line_characteristics": [Array],
  "shipping_location": {Object},
  "short_description": {Object},
  "start_date": {Object},
  "state": {Object},
  "sys_id": {Object},
  "sys_created_by": {Object},
  "sys_created_on": {Object},
  "sys_updated_by": {Object},
  "sys_updated_on": {Object},
  "top_sales_agreement_line": {Object},
  "total_one_time_price": {Object},
  "total_recurring_price": {Object},
  "unit_net_price": {Object},
  "unit_of_measure": {Object}
  }
]
```

</td></tr><tr><td>

sales\_agreement\_lines.end\_date

</td><td>

End date of the sales agreement line.Data type: Object

```
"end_date": {
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String" 
}
```

</td></tr><tr><td>

sales\_agreement\_lines.end\_date.display\_value

</td><td>

Display value of the end date for the sales agreement line. Matches **end.value**.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.end\_date.label

</td><td>

Label of the end date for the sales agreement line.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.end\_date.name

</td><td>

Name of the end date for the sales agreement line.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.end\_date.type

</td><td>

Type of end date for the sales agreement line. Value is always `glide_date_time`.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.end\_date.value

</td><td>

End date and time value of the sales agreement line.Format: YYYY-MM-DD HH:mm:ss

Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.number

</td><td>

Automatically generated sales agreement line number or the number posted .Table: Sales Agreement Line  \[sn\_sales\_agmt\_core\_sales\_agreement\_line\]

Data type: Object

```
"number": { 
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String"
}
```

</td></tr><tr><td>

sales\_agreement\_lines.number.display\_value

</td><td>

Display value of the sales agreement line number. For example, `SAL0010128`. Matches **number.value**.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.number.label

</td><td>

Label of the number.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.number.name

</td><td>

Name of the number.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.number.type

</td><td>

Type of number. Value is always `string`.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.number.value

</td><td>

Value of the sales agreement line number. For example, `SAL0010128`.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.parent\_line

</td><td>

Information about the parent sales agreement line.Table: Sales Agreement Line  \[sn\_sales\_agmt\_core\_sales\_agreement\_line\]

Data type: Object

```
"parent_line": { 
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String"
}
```

</td></tr><tr><td>

sales\_agreement\_lines.parent\_line.display\_value

</td><td>

Display number of the parent sales agreement line. For example, `SAL0010126`.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.parent\_line.label

</td><td>

Label of the parent sales agreement line.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.parent\_line.name

</td><td>

Name of the parent sales agreement line.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.parent\_line.type

</td><td>

Type of parent sales agreement line. Value is always `reference`.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.parent\_line.value

</td><td>

Sys\_id of the parent sales agreement line.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.price\_list

</td><td>

Price list details of the sales agreement line.Table: Sales Agreement Line  \[sn\_sales\_agmt\_core\_sales\_agreement\_line\]

Data type: Object

```
"price_list": {
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String" 
}
```

</td></tr><tr><td>

sales\_agreement\_lines.price\_list.display\_value

</td><td>

Display value of the sales agreement line's price list.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.price\_list.label

</td><td>

Label of the sales agreement line's price list.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.price\_list.name

</td><td>

Name of the sales agreement line's price list.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.price\_list.type

</td><td>

Type of sales agreement line's price list. Value is always `reference`.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.price\_list.value

</td><td>

Sys\_id of the price list associated with the sales agreement line.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.product\_model

</td><td>

Details about the product model on the sales agreement line.Table: Product Model \[cmdb\_model\]

Data type: Object

```
"product_model": {
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String" 
}
```

</td></tr><tr><td>

sales\_agreement\_lines.product\_model.display\_value

</td><td>

Display value of the product model on the sales agreement line. Matches **product\_model.value**.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.product\_model.label

</td><td>

Label of the product model on the sales agreement line.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.product\_model.name

</td><td>

Name of the product model on the sales agreement line.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.product\_model.type

</td><td>

Type of product model on the sales agreement line. Value is always `reference`.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.product\_model.value

</td><td>

Value of the product model on the sales agreement line.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.product\_offering

</td><td>

Details about the product offering on the sales agreement line.Table: Product Offering \[sn\_prd\_pm\_product\_offering\]

Data type: Object

```
"product_offering": {
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String" 
}
```

</td></tr><tr><td>

sales\_agreement\_lines.product\_offering.display\_value

</td><td>

Display value of the product offering on the sales agreement line.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.product\_offering.label

</td><td>

Label of the product offering on the sales agreement line.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.product\_offering.name

</td><td>

Name of the product offering on the sales agreement line.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.product\_offering.type

</td><td>

Type of product offering on the sales agreement line. Value is always `reference`.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.product\_offering.value

</td><td>

Value of the product offering on the sales agreement line.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.product\_specification

</td><td>

Reference to product specification of the sales agreement line.Table: Sales Agreement Line  \[sn\_sales\_agmt\_core\_sales\_agreement\_line\]

Data type: Object

```
"product_offering": {
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String" 
}
```

</td></tr><tr><td>

sales\_agreement\_lines.product\_specification.display\_value

</td><td>

Display value of the product offering on the sales agreement line. Matches **product\_specification.value**.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.product\_specification.label

</td><td>

Label of the product specification on the sales agreement line.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.product\_specification.name

</td><td>

Name of the product specification on the sales agreement line.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.product\_specification.type

</td><td>

Type of product specification on the sales agreement line. Value is always `reference`.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.product\_specification.value

</td><td>

Value of the product specification on the sales agreement line.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.quantity

</td><td>

Number of products to add to the sales agreement line.Table: Sales Agreement Line  \[sn\_sales\_agmt\_core\_sales\_agreement\_line\]

Data type: Object

```
"quantity": {
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String" 
}
```

</td></tr><tr><td>

sales\_agreement\_lines.quantity.display\_value

</td><td>

Display value of the product quantity on the sales agreement line. Matches **quantity.value**.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.quantity.label

</td><td>

Label of the product quantity on the sales agreement line.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.quantity.name

</td><td>

Name of the product quantity on the sales agreement line.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.quantity.type

</td><td>

Type of product quantity on the sales agreement line. Value is always `decimal`.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.quantity.value

</td><td>

Number of products on the sales agreement line. Data type: Number

</td></tr><tr><td>

sales\_agreement\_lines.quote\_line

</td><td>

Reference of the quote line item on the sales agreement line.Table: Quote Line \[sn\_quote\_mgmt\_core\_quote\_line\_item\]

Data type: Object

```
"quote_line": {
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String" 
}
```

</td></tr><tr><td>

sales\_agreement\_lines.quote\_line.display\_value

</td><td>

Display value of the quote line item on the sales agreement line.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.quote\_line.label

</td><td>

Label of the quote line item on the sales agreement line.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.quote\_line.name

</td><td>

Name of the quote line item on the sales agreement line.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.quote\_line.type

</td><td>

Type of quote line item on the sales agreement line. Value is always `reference`.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.quote\_line.value

</td><td>

Value of the quote line item on the sales agreement line.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement

</td><td>

Reference to the sales agreement of the sales agreement line.Table: Sales Agreement Line  \[sn\_sales\_agmt\_core\_sales\_agreement\_line\]

Data type: Object

```
"sales_agreement": {
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String" 
}
```

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement.display\_value

</td><td>

Display value of the sales agreement of the sales agreement line. For example, `SA0010106`.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement.label

</td><td>

Label of the sales agreement of the sales agreement line.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement.name

</td><td>

Name of the sales agreement of the sales agreement line.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement.type

</td><td>

Type of sales agreement of the sales agreement line. Value is always `reference`.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement.value

</td><td>

Sys\_id of the sales agreement of the sales agreement line.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics

</td><td>

List of sales agreement line characteristics.Table: Sales Agreement Line Characteristics \[sn\_sales\_agmt\_core\_sales\_agreement\_line\_characteristic\]

Data type: Array of objects

```
"sales_agreement_line_characteristics": [
 {
   "characteristic": {Object},
   "characteristic_option": {Object},
   "sales_agreement": {Object},
   "sales_agreement_line": {Object},
   "sys_id": {Object},
   "sys_created_by": {Object},
   "sys_updated_by": {Object},
   "sys_created_on": {Object},
   "sys_updated_on": {Object},
   "type": {Object},
   "value": {Object}
  }
]
```

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.characteristic

</td><td>

Characteristic associated with the sales agreement line.Table: sn\_prd\_pm\_characteristic

Data type: Object

```
"characteristic": {
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String" 
}
```

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.characteristic.display\_value

</td><td>

Display value of the characteristic on the sales agreement line.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.characteristic.label

</td><td>

Label of the characteristic on the sales agreement line.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.characteristic.name

</td><td>

Name of the characteristic on the sales agreement line.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.characteristic.type

</td><td>

Type of characteristic on the sales agreement line. Value is always `reference`.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.characteristic.value

</td><td>

Value of the characteristic on the sales agreement line.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.characteristic\_option

</td><td>

Information about the characteristic option on the sales agreement line.Table: Sales Agreement Line Characteristics \[sn\_sales\_agmt\_core\_sales\_agreement\_line\_characteristic\]

Data type: Object

```
"characteristic_option": {
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String" 
}
```

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.characteristic\_option.display\_value

</td><td>

Display value of the characteristic on the sales agreement line. Matches **characteristic\_option.value**. Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.characteristic\_option.label

</td><td>

Label of the characteristic option on the sales agreement line.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.characteristic\_option.name

</td><td>

Name of the characteristic option on the sales agreement line.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.characteristic\_option.type

</td><td>

Type of characteristic option on the sales agreement line. Value is always `reference`.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.characteristic\_option.value

</td><td>

Value of the characteristic option on the sales agreement line.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.sales\_agreement

</td><td>

Details of the sales agreement characteristic on the sales agreement line.Table: Sales Agreement Line Characteristics \[sn\_sales\_agmt\_core\_sales\_agreement\_line\_characteristic\]

Data type: Object

```
"sales_agreement": {
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String" 
}
```

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.sales\_agreement.display\_value

</td><td>

Display value of the sales agreement characteristic. Matches **sales\_agreement.value**. Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.sales\_agreement.label

</td><td>

Label of the sales agreement characteristic.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.sales\_agreement.name

</td><td>

Name of the sales agreement characteristic.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.sales\_agreement.type

</td><td>

Type of sales agreement characteristic. Value is always `reference`.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.sales\_agreement.value

</td><td>

Value of the sales agreement characteristic.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.sales\_agreement\_line

</td><td>

Details about the characteristic of the sales agreement line.Table: Sales Agreement Line Characteristics \[sn\_sales\_agmt\_core\_sales\_agreement\_line\_characteristic\]

Data type: Object

```
"sales_agreement_line": {
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String" 
}
```

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.sales\_agreement\_line.display\_value

</td><td>

Display value of the characteristic of the sales agreement line. Matches **sales\_agreement\_line.value**. Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.sales\_agreement\_line.label

</td><td>

Characteristic label of the sales agreement line.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.sales\_agreement\_line.name

</td><td>

Characteristic name of the sales agreement line.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.sales\_agreement\_line.type

</td><td>

Characteristic type of the sales agreement line. Value is always `reference`.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.sales\_agreement\_line.value

</td><td>

Characteristic value of the sales agreement line.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.sys\_created\_by

</td><td>

Name of the user who created the sales agreement line characteristic.Table: User \[user\]

Data type: Object

```
"sys_created_by": {
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String"
}
```

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.sys\_created\_by.display\_value

</td><td>

Display value of the Created by field. Matches **sys\_created\_by.value**.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.sys\_created\_by.label

</td><td>

Label of the Created by field.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.sys\_created\_by.name

</td><td>

Name of the Created by field.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.sys\_created\_by.type

</td><td>

Type of the Created by field. Value is always `string`.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.sys\_created\_by.value

</td><td>

Value of the Created by field.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.sys\_created\_on

</td><td>

Date and time the sales agreement line characteristic was created.Data type: Object

```
"sys_created_on": {
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String"
}
```

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.sys\_created\_on.display\_value

</td><td>

Display value of the Created on field. Matches **sys\_created\_on.value**.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.sys\_created\_on.label

</td><td>

Label of the Created on field.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.sys\_created\_on.name

</td><td>

Name of the Created on field.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.sys\_created\_on.type

</td><td>

Type of the Created on field. Value is always `glide_date_time`.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.sys\_created\_on.value

</td><td>

Value of the Created on field.Format: YYYY-DD-MM HH:mm:ss

Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.sys\_id

</td><td>

Sys\_id of the sales agreement line characteristic.Table: Sales Agreement Line Characteristics \[sn\_sales\_agmt\_core\_sales\_agreement\_line\_characteristic\]

Data type: Object

```
"sys_id": {
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String"
}
```

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.sys\_id.display\_value

</td><td>

Display value of the characteristic sys\_id. Matches **sys\_id.value**.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.sys\_id.label

</td><td>

Label of the characteristic sys\_id.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.sys\_id.name

</td><td>

Name of the characteristic sys\_id.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.sys\_id.type

</td><td>

Type of the characteristic sys\_id. Value is always `string`.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.sys\_id.id

</td><td>

Value of the characteristic sys\_id.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.sys\_updated\_by

</td><td>

Name of the user who last updated the sales agreement line characteristic.Table: User \[user\]

Data type: Object

```
"sys_updated_by": {
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String"
}
```

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.sys\_updated\_by.display\_value

</td><td>

Display value of the user who updated the characteristic of the sales agreement line item. Matches **sys\_created\_by.value**.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.sys\_updated\_by.label

</td><td>

Label of the user who updated the characteristic.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.sys\_updated\_by.name

</td><td>

Name of the user who updated the characteristic.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.sys\_updated\_by.type

</td><td>

Type of the user who updated the characteristic. Value is always `string`.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.sys\_updated\_by.value

</td><td>

Value of user who updated the characteristic.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.sys\_updated\_on

</td><td>

Date and time the sales agreement line characteristic was last updated.Data type: Object

```
"sys_updated_on": {
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String"
}
```

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.sys\_updated\_on.display\_value

</td><td>

Display value of the updated date. Matches **updated\_on.value**.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.sys\_updated\_on.label

</td><td>

Label of the updated date.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.sys\_updated\_on.name

</td><td>

Name of the updated date.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.sys\_updated\_on.type

</td><td>

Type of the updated date. Value is always `glide_date_time`.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.sys\_updated\_on.value

</td><td>

Value of the updated date.Format: YYYY-DD-MM HH:mm:ss

Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.type

</td><td>

Type of characteristic in the sales agreement line characteristic.Table: Sales Agreement Line Characteristics \[sn\_sales\_agmt\_core\_sales\_agreement\_line\_characteristic\]

Data type: Object

```
"type": {
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String"
}
```

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.type.display\_value

</td><td>

Display value of the characteristic type. Matches **type.value**.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.type.label

</td><td>

Label of the characteristic type.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.type.name

</td><td>

Name of the characteristic type.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.type.type

</td><td>

Type of the characteristic type. Value is always `string`.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.type.value

</td><td>

Value of the characteristic type.Possible values:

-   coverage
-   coverage and usage

Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.value

</td><td>

Value of the characteristic on the sales agreement line.Table: Sales Agreement Line Characteristics \[sn\_sales\_agmt\_core\_sales\_agreement\_line\_characteristic\]

Data type: Object

```
"type": {
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String"
}
```

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.value.display\_value

</td><td>

Display value of the characteristic. Matches **type.value**.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.value.label

</td><td>

Label of the characteristic value.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.value.name

</td><td>

Name of the characteristic value.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.value.type

</td><td>

Type of the characteristic value. Value is always `string`.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sales\_agreement\_line\_characteristics.value.value

</td><td>

Value of the characteristic.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.short\_description

</td><td>

Brief details describing the sales agreement line.Table: Sales Agreement Line  \[sn\_sales\_agmt\_core\_sales\_agreement\_line\]

Data type: Object

```
"short_description": { 
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String" 
}
```

</td></tr><tr><td>

sales\_agreement\_lines.short\_description.display\_value

</td><td>

Display value of the short description. Matches **short\_description.value**.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.short\_description.label

</td><td>

Label of the short description.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.short\_description.name

</td><td>

Name of the short description.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.short\_description.type

</td><td>

Type of short description. Always of type `string`.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.short\_description.value

</td><td>

Value of the short description.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.start\_date

</td><td>

Start date of the sales agreement line.Data type: Object

```
"start_date": {
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String"
}
```

</td></tr><tr><td>

sales\_agreement\_lines.start\_date.display\_value

</td><td>

Display value of the sales agreement line's start date. Matches **start\_date.value**.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.start\_date.label

</td><td>

Label of the sales agreement line's start date.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.start\_date.name

</td><td>

Name of the sales agreement line's start date.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.start\_date.type

</td><td>

Type of sales agreement line's start date. Value is always `glide_date_time`.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.start\_date.value

</td><td>

Value of the sales agreement line's start date.Format: YYYY-MM-DD

Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.state

</td><td>

Valid state of the sales agreement line.Table: Sales Agreement Line  \[sn\_sales\_agmt\_core\_sales\_agreement\_line\]

Data type: Object

```
"state": { 
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String" 
}
```

</td></tr><tr><td>

sales\_agreement\_lines.state.display\_value

</td><td>

Display value of the state. Matches **state.value**.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.state.label

</td><td>

Label of the state.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.state.name

</td><td>

Name of the state.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.state.type

</td><td>

Type of state. Value is always `string`.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.state.value

</td><td>

Value of the state.Possible values:

-   pending\_activation
-   suspended
-   active
-   expired
-   cancelled

Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sys\_created\_by

</td><td>

Name of the user who created the sales agreement line.Table: User \[user\]

Data type: Object

```
"sys_created_by": {
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String"
}
```

</td></tr><tr><td>

sales\_agreement\_lines.sys\_created\_by.display\_value

</td><td>

Display value of the user who created the sales agreement line. Matches **sys\_created\_by.value**.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sys\_created\_by.label

</td><td>

Label of the user who created the sales agreement line.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sys\_created\_by.name

</td><td>

Name of the user who created the sales agreement line.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sys\_created\_by.type

</td><td>

Type of the Created by field. Value is always `string`.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sys\_created\_by.value

</td><td>

Value of the user who created the sales agreement line.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sys\_created\_on

</td><td>

Date and time the sales agreement line record was created.Data type: Object

```
"sys_created_on": { 
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String"
}
```

</td></tr><tr><td>

sales\_agreement\_lines.sys\_created\_on.display\_value

</td><td>

Display value of the creation date of the sales agreement line record. Matches **sys\_created\_on.value**.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sys\_created\_on.label

</td><td>

Label of the creation date of the sales agreement line record.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sys\_created\_on.name

</td><td>

Name of the creation date of the sales agreement line record.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sys\_created\_on.type

</td><td>

Type of the creation date of the sales agreement line record. Value is always `glide_date_time`.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sys\_created\_on.value

</td><td>

Value of the creation date of the sales agreement line record.Format: YYYY-MM-DD HH:mm:ss

Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sys\_id

</td><td>

Sys\_id of the sales agreement line record .Table: Sales Agreement Line  \[sn\_sales\_agmt\_core\_sales\_agreement\_line\]

Data type: Object

```
"sys_id": { 
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String" 
}
```

</td></tr><tr><td>

sales\_agreement\_lines.sys\_id.displayValue

</td><td>

Display value of the sys\_id of the sales agreement line record . Matches **sys\_id.value**.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sys\_id.label

</td><td>

Automatically-generated name or label of the sales agreement line record  sys\_id.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sys\_id.type

</td><td>

Type of sys\_id of the sales agreement line record . Value is always `string`.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sys\_id.value

</td><td>

Sys\_id number assigned to the sales agreement line record .Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sys\_updated\_by

</td><td>

Name of the user who last updated the sales agreement line.Table: User \[user\]

Data type: Object

```
"sys_updated_by": { 
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String"
}
```

</td></tr><tr><td>

sales\_agreement\_lines.sys\_updated\_by.display\_value

</td><td>

Display value of the user who updated the sales agreement line. Matches **sys\_updated\_by.value**.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sys\_updated\_by.label

</td><td>

Label of the user who updated the sales agreement line.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sys\_updated\_by.name

</td><td>

Name of the user who updated the sales agreement line.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sys\_updated\_by.type

</td><td>

Type of the user who updated the sales agreement line. Value is always `string`.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sys\_updated\_by.value

</td><td>

Value of the user who updated the sales agreement line.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sys\_updated\_on

</td><td>

Date and time the sales agreement line record was last updated.Data type: Object

```
"sys_updated_on": { 
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String"
}
```

</td></tr><tr><td>

sales\_agreement\_lines.sys\_updated\_on.display\_value

</td><td>

The display value of the updated date and time on the sales agreement line. Matches **sys\_updated\_on.value**.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sys\_updated\_on.label

</td><td>

Label of the updated date and time on the sales agreement lineData type: String

</td></tr><tr><td>

sales\_agreement\_lines.sys\_updated\_on.name

</td><td>

Name of the updated date and time on the sales agreement lineData type: String

</td></tr><tr><td>

sales\_agreement\_lines.sys\_updated\_on.type

</td><td>

Type of the updated date and time on the sales agreement line. Value is always `glide_date_time`.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.sys\_updated\_on.value

</td><td>

Value of the updated date and time on the sales agreement lineFormat: YYYY-MM-DD HH:mm:ss

Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.top\_sales\_agreement\_line

</td><td>

Information about the top sales agreement line.Table: Sales Agreement Line  \[sn\_sales\_agmt\_core\_sales\_agreement\_line\]

Data type: Object

```
"top_sales_agreement_line": { 
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String"
}
```

</td></tr><tr><td>

sales\_agreement\_lines.top\_sales\_agreement\_line.display\_value

</td><td>

Display value of the top sales agreement line. Matches **top\_sales\_agreement\_line.value**.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.top\_sales\_agreement\_line.label

</td><td>

Label of the top sales agreement line.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.top\_sales\_agreement\_line.name

</td><td>

Name the top sales agreement line.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.top\_sales\_agreement\_line.type

</td><td>

Type of the top sales agreement line. Value is always `reference`.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.top\_sales\_agreement\_line.value

</td><td>

Value of the top sales agreement line.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.total\_one\_time\_price

</td><td>

Total one-time charges to be paid for the product or service.Table: Sales Agreement Line  \[sn\_sales\_agmt\_core\_sales\_agreement\_line\]

Data type: Object

```
"total_one_time_price": { 
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String"
}
```

</td></tr><tr><td>

sales\_agreement\_lines.total\_one\_time\_price.display\_value

</td><td>

Display value of the total one time price. Matches **total\_one\_time\_price.value**.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.total\_one\_time\_price.label

</td><td>

Label of the total one time price.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.total\_one\_time\_price.name

</td><td>

Name of the total one time price.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.total\_one\_time\_price.type

</td><td>

Type of the total one time price. Value is always `decimal`.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.total\_one\_time\_price.value

</td><td>

Value of the total one time price.Data type: String represented as a number \(currency\)

</td></tr><tr><td>

sales\_agreement\_lines.total\_recurring\_price

</td><td>

Total recurring price for the product associated with the sales agreement line.Table: Sales Agreement Line  \[sn\_sales\_agmt\_core\_sales\_agreement\_line\]

Data type: Object

```
"total_recurring_price": { 
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String"
}
```

</td></tr><tr><td>

sales\_agreement\_lines.total\_recurring\_price.display\_value

</td><td>

Display value of the total one time price. Matches **total\_recurring\_price.value**.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.total\_recurring\_price.label

</td><td>

Label of the total recurring price.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.total\_recurring\_price.name

</td><td>

Name of the total recurring price.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.total\_recurring\_price.type

</td><td>

Type of the total recurring price. Value is always `decimal`.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.total\_recurring\_price.value

</td><td>

Value of the total recurring price.Data type: String represented as a number \(currency\)

</td></tr><tr><td>

sales\_agreement\_lines.unit\_net\_price

</td><td>

The price for each unit within the sales agreement line.Table: Sales Agreement Line  \[sn\_sales\_agmt\_core\_sales\_agreement\_line\]

Data type: Object

```
"unit_net_price": { 
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String"
}
```

</td></tr><tr><td>

sales\_agreement\_lines.unit\_net\_price

</td><td>

Display value of the unit net price. Matches **unit\_net\_price.value**.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.unit\_net\_price

</td><td>

Label of the unit net price.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.unit\_net\_price

</td><td>

Name of the unit net price.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.unit\_net\_price

</td><td>

Type of the unit net price. Value is always `decimal`.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.unit\_net\_price

</td><td>

Value of the unit net price.Data type: String represented as a number \(currency\)

</td></tr><tr><td>

sales\_agreement\_lines.unit\_of\_measurement

</td><td>

Unit of measurement of the sales agreement line.Table: Unit of measures \[sn\_prd\_pm\_uom\_list\]

Data type: Object

```
"unit_of_measurement": { 
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String"
}
```

</td></tr><tr><td>

sales\_agreement\_lines.unit\_of\_measurement.display\_value

</td><td>

Display value of the unit of measurement. Matches **unit\_of\_measurement.value**.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.unit\_of\_measurement.label

</td><td>

Label of the unit of measurement.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.unit\_of\_measurement.name

</td><td>

Name of the unit of measurement.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.unit\_of\_measurement.type

</td><td>

Type of the unit of measurement. Value is always `reference`.Data type: String

</td></tr><tr><td>

sales\_agreement\_lines.unit\_of\_measurement.value

</td><td>

Value of the unit of measurement. For example, `bundle` or `each`.Data type: String

</td></tr><tr><td>

shipping\_location

</td><td>

Shipping address details on the sales agreement.Table: Location \[location\]

Data type: Object

```
"unit_of_measure": { 
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String"
}
```

</td></tr><tr><td>

shipping\_location.display\_value

</td><td>

Display value of the shipping location.Data type: String

</td></tr><tr><td>

shipping\_location.label

</td><td>

Label of the shipping location.Data type: String

</td></tr><tr><td>

shipping\_location.name

</td><td>

Name of the shipping location.Data type: String

</td></tr><tr><td>

shipping\_location.type

</td><td>

Type of shipping location. Value is always `reference`.Data type: String

</td></tr><tr><td>

shipping\_location.value

</td><td>

Value of the shipping location. For example, an address.Data type: String

</td></tr><tr><td>

short\_description

</td><td>

Brief details describing the sales agreement.Table: Sales Agreement  \[sn\_sales\_agmt\_core\_sales\_agreement\]

Data type: Object

```
"short_description": { 
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String" 
}
```

</td></tr><tr><td>

short\_description.display\_value

</td><td>

Display value of the short description. Matches **short\_description.value**.Data type: String

</td></tr><tr><td>

short\_description.label

</td><td>

Label of the short description.Data type: String

</td></tr><tr><td>

short\_description.name

</td><td>

Name of the short description.Data type: String

</td></tr><tr><td>

short\_description.type

</td><td>

Type of short description. Always of type `string`.Data type: String

</td></tr><tr><td>

short\_description.value

</td><td>

Value of the short description.Data type: String

</td></tr><tr><td>

starts

</td><td>

Start date of the sales agreement.Data type: Object

```
"starts": { 
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String"
}
```

</td></tr><tr><td>

starts.display\_value

</td><td>

Display value of the start date. Matches **start.value**.Data type: String

</td></tr><tr><td>

starts.label

</td><td>

Label of the start date.Data type: String

</td></tr><tr><td>

starts.name

</td><td>

Name of the start date.Data type: String

</td></tr><tr><td>

starts.type

</td><td>

Type of start date. Value is always `glide_date_time`Data type: String

</td></tr><tr><td>

starts.value

</td><td>

Value of the start date.Format: YYYY-MM-DD HH:mm:ss

Data type: String

</td></tr><tr><td>

state

</td><td>

State of the sales agreement.Table: Sales Agreement  \[sn\_sales\_agmt\_core\_sales\_agreement\]

Data type: Object

```
"state": { 
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String" 
}
```

</td></tr><tr><td>

state.display\_value

</td><td>

Display value of the state. Matches **state.value**.Data type: String

</td></tr><tr><td>

state.lable

</td><td>

Label of the state.Data type: String

</td></tr><tr><td>

state.name

</td><td>

Name of the state.Data type: String

</td></tr><tr><td>

state.type

</td><td>

Type of state. Value is always `string`.Data type: String

</td></tr><tr><td>

state.value

</td><td>

Value of the state.Possible values:

-   active
-   cancelled
-   draft
-   expired

Data type: String

</td></tr><tr><td>

sys\_created\_by

</td><td>

Name of the user who created the sales agreement.Table: User \[user\]

Data type: Object

```
"sys_created_by": {
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String"
}
```

</td></tr><tr><td>

sys\_created\_by.display\_value

</td><td>

Display value of the user who created the sales agreement. Matches **sys\_created\_by.value**.Data type: String

</td></tr><tr><td>

sys\_created\_by.label

</td><td>

Label of the user who created the sales agreement.Data type: String

</td></tr><tr><td>

sys\_created\_by.name

</td><td>

Name of the user who created the sales agreement.Data type: String

</td></tr><tr><td>

sys\_created\_by.type

</td><td>

Type of the user who created the sales agreement. Value is always `string`.Data type: String

</td></tr><tr><td>

sys\_created\_by.value

</td><td>

Value of the user who created the sales agreement.Data type: String

</td></tr><tr><td>

sys\_created\_on

</td><td>

Details about the date and time that the sales agreement was created.Data type: Object

```
"sys_created_on": { 
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String"
}
```

</td></tr><tr><td>

sys\_created\_on.display\_value

</td><td>

Display value of the creation date and time. Matches **sys\_created\_on.value**.Data type: String

</td></tr><tr><td>

sys\_created\_on.label

</td><td>

Label of the creation date and time.Data type: String

</td></tr><tr><td>

sys\_created\_on.name

</td><td>

Name of the creation date and time.Data type: String

</td></tr><tr><td>

sys\_created\_on.type

</td><td>

Type of the creation date and time. Value is always `string`.Data type: String

</td></tr><tr><td>

sys\_created\_on.value

</td><td>

Value of the creation date and time.Data type: String

</td></tr><tr><td>

sys\_id

</td><td>

Sys\_id   of the newly created sales agreement.Table: Sales Agreement  \[sn\_sales\_agmt\_core\_sales\_agreement\]

Data type: Object

```
"sys_id": { 
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String" 
}
```

</td></tr><tr><td>

sys\_id.displayValue

</td><td>

Display value of the unique sys\_id value. Matches **sys\_id.value**.Data type: String

</td></tr><tr><td>

sys\_id.label

</td><td>

Automatically generated name or label of the sys\_id.Data type: String

</td></tr><tr><td>

sys\_id.type

</td><td>

Type of sys\_id given to the sales agreement. Value is always `GUID`.Data type: String

</td></tr><tr><td>

sys\_id.value

</td><td>

Sys\_id number assigned to the new sales agreement.Data type: String

</td></tr><tr><td>

sys\_updated\_by

</td><td>

Name of the user who last updated the sales agreement.Table: User \[user\]

Data type: Object

```
"sys_updated_by": { 
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String"
}
```

</td></tr><tr><td>

sys\_updated\_by.display\_value

</td><td>

Display value of the user who updated the sales agreement. Matches **sys\_updated\_by.value**.Data type: String

</td></tr><tr><td>

sys\_updated\_by.label

</td><td>

Label of the user who updated the sales agreement.Data type: String

</td></tr><tr><td>

sys\_updated\_by.name

</td><td>

Name of the user who updated the sales agreement.Data type: String

</td></tr><tr><td>

sys\_updated\_by.type

</td><td>

Type of the user who updated the sales agreement. Value is always `string`.Data type: String

</td></tr><tr><td>

sys\_updated\_by.value

</td><td>

Value of the user who updated the sales agreement.Data type: String

</td></tr><tr><td>

sys\_updated\_on

</td><td>

Details about the date and time that the sales agreement was updated.Data type: Object

```
"sys_updated_on": { 
  "display_value": "String",
  "label": "String",
  "name": "String",
  "type": "String",
  "value": "String"
}
```

</td></tr><tr><td>

sys\_updated\_on.display\_value

</td><td>

Date and time value of the updated sales agreement. Matches **sys\_updated\_on.value**.Format: YYYY-MM-DD HH:mm:ss

Data type: String

</td></tr><tr><td>

sys\_updated\_on.label

</td><td>

Label of the updated sales agreement.Data type: String

</td></tr><tr><td>

sys\_updated\_on.name

</td><td>

Name of the updated sales agreement.Data type: String

</td></tr><tr><td>

sys\_updated\_on.type

</td><td>

Type of the updated sales agreement. Value is always `glide_date_time`.Data type: String

</td></tr><tr><td>

sys\_updated\_on.value

</td><td>

Date and time value of the updated sales agreement.Format: YYYY-MM-DD HH:mm:ss

Data type: String

</td></tr></tbody>
</table>### cURL request

The following example creates a new sales agreement with details such as sales agreement characteristics and price adjustments. As a result, the new sales agreement is returned and added as a new record in Sales Agreement  \[sn\_sales\_agmt\_core\_sales\_agreement\] table.

```
curl "https://instance.service-now.com//api/sn_sales_agmt_core/salesagreement" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{ 
    "state": "active", 
    "account": "86837a386f0331003b3c498f5d3ee4ca", 
    "starts": "2024-01-01", 
    "ends": "2024-12-31", 
    "short_description": "This is a Sa created by API", 
    "quote": "04ba9004f11f3110f8777d7194f166f6", 
    "default_price_list": "96257fe1b5165610f87786d3c28843e9", 
    "contact": "60beb5e7d7600200e5982cf65e6103ad", 
    "currency": "USD", 
    "billing_location": "25ab9c4d0a0a0bb300f7dabdc0ca7c1c", 
    "shipping_location": "25ab9c4d0a0a0bb300f7dabdc0ca7c1c", 
    "sales_agreement_lines": [ 
        { 
            "state": "active", 
            "start_date": "2024-11-10", 
            "end_date": "2024-12-31", 
            "short_description": "this is sample sa line 1", 
            "quantity": 2, 
            "quote_line": "", 
            "price_list": "96257fe1b5165610f87786d3c28843e9", 
            "product_offering": "26d07c3211707110f877366201dea60c", 
            "product_specification": "", 
            "product_model": "", 
            "unit_of_measurement": "cb2795d553020110286eddeeff7b12ff", 
            "unit_net_price": "USD;400.00", 
            "total_one_time_price": "USD;400.00", 
            "shipping_location": "25ab9c4d0a0a0bb300f7dabdc0ca7c1c", 
            "child_sales_agreement_lines": [ 
                { 
                    "state": "active", 
                    "start_date": "2024-11-11", 
                    "end_date": "2024-12-31", 
                    "short_description": "this is sample child sa line 1", 
                    "quantity": 2, 
                    "quote_line": "", 
                    "price_list": "96257fe1b5165610f87786d3c28843e9", 
                    "product_offering": "3f6111dfd0a63110f8770dbf976be149", 
                    "product_specification": "", 
                    "product_model": "", 
                    "unit_of_measurement": "cb2795d553020110286eddeeff7b12ff", 
                    "unit_net_price": "USD;120.00", 
                    "total_one_time_price": "USD;120.00", 
                    "total_recurring_price": "", 
                    "shipping_location": "25ab9c4d0a0a0bb300f7dabdc0ca7c1c", 
                    "sales_agreement_line_characteristics": [ 
                        { 
                            "characteristic": "4f31999fd0a63110f8770dbf976be178", 
                            "type": "", 
                            "characteristic_option": "0b31999fd0a63110f8770dbf976be179", 
                            "value": "3G" 
                        } 
                    ], 
                    "sales_agreement_line_adjustments": [ 
                        { 
                            "amount": "28", 
                            "total_amount": "28", 
                            "quantity": 1, 
                            "short_description": "Price adjustment", 
                            "adjustment_value": "20", 
                            "adjustment_source": "", 
                            "adjustment_type": "a96c83d653dd91105c0eddeeff7b12d8", 
                            "applicable_to": "UNIT_QTY" 
                        } 
                    ] 
                } 
            ], 
            "sales_agreement_line_characteristics": [ 
                { 
                    "characteristic": "4f31999fd0a63110f8770dbf976be178", 
                    "type": "", 
                    "characteristic_option": "0b31999fd0a63110f8770dbf976be179", 
                    "value": "3G" 
                } 
            ], 
            "sales_agreement_line_adjustments": [ 
                { 
                    "amount": "40", 
                    "total_amount": "120", 
                    "quantity": 3, 
                    "short_description": "Price adjustment", 
                    "adjustment_value": "10", 
                    "adjustment_source": "AUTO", 
                    "adjustment_type": "a96c83d653dd91105c0eddeeff7b12d8", 
                    "applicable_to": "UNIT_QTY" 
                } 
            ] 
        } 
    ] 
}
```

Response body.

```
{
  "result": {
    "sys_id": {
      "label": "Sys ID",
      "value": "bc93e08a78755a10f8777f88938ba1d8",
      "displayValue": "bc93e08a78755a10f8777f88938ba1d8",
      "type": "GUID"
    },
    "sys_created_by": {
      "name": "sys_created_by",
      "label": "Created by",
      "value": "maint",
      "display_value": "maint",
      "type": "string"
    },
    "sys_updated_by": {
      "name": "sys_updated_by",
      "label": "Updated by",
      "value": "maint",
      "display_value": "maint",
      "type": "string"
    },
    "sys_created_on": {
      "name": "sys_created_on",
      "label": "Created",
      "value": "2024-11-12 08:11:59",
      "display_value": "2024-11-12 00:11:59",
      "type": "glide_date_time"
    },
    "sys_updated_on": {
      "name": "sys_updated_on",
      "label": "Updated",
      "value": "2024-11-12 08:11:59",
      "display_value": "2024-11-12 00:11:59",
      "type": "glide_date_time"
    },
    "name": null,
    "account": {
      "name": "account",
      "label": "Account",
      "value": "86837a386f0331003b3c498f5d3ee4ca",
      "display_value": "Boxeo",
      "type": "reference"
    },
    "consumer": {
      "name": "consumer",
      "label": "Consumer",
      "value": null,
      "display_value": "",
      "type": "reference"
    },
    "number": {
      "name": "number",
      "label": "Number",
      "value": "SA0010106",
      "display_value": "SA0010106",
      "type": "string"
    },
    "state": {
      "name": "state",
      "label": "State",
      "value": "active",
      "display_value": "Active",
      "type": "string"
    },
    "starts": {
      "name": "starts",
      "label": "Start date",
      "value": "2024-01-01",
      "display_value": "2024-01-01",
      "type": "glide_date"
    },
    "ends": {
      "name": "ends",
      "label": "End date",
      "value": "2024-12-31",
      "display_value": "2024-12-31",
      "type": "glide_date"
    },
    "short_description": {
      "name": "short_description",
      "label": "Short description",
      "value": "this is a sample sales agreement",
      "display_value": "this is a sample sales agreement",
      "type": "string"
    },
    "description": {
      "name": "description",
      "label": "Description",
      "value": null,
      "display_value": "",
      "type": "string"
    },
    "currency": {
      "name": "currency",
      "label": "Currency",
      "value": null,
      "display_value": "",
      "type": "reference"
    },
    "default_price_list": {
      "name": "default_price_list",
      "label": "Default price list",
      "value": "19d29513d0e63110f8770dbf976be122",
      "display_value": "Standard Price List",
      "type": "reference"
    },
    "billing_location": {
      "name": "billing_location",
      "label": "Billing location",
      "value": null,
      "display_value": "",
      "type": "reference"
    },
    "contact": {
      "name": "contact",
      "label": "Contact",
      "value": null,
      "display_value": "",
      "type": "reference"
    },
    "shipping_location": {
      "name": "shipping_location",
      "label": "Shipping location",
      "value": null,
      "display_value": "",
      "type": "reference"
    },
    "quote": {
      "name": "quote",
      "label": "Quote",
      "value": "04ba9004f11f3110f8777d7194f166f6",
      "display_value": "QT0000001",
      "type": "reference"
    },
    "service_contract_lines": [
      {
        "sys_id": {
          "label": "Sys ID",
          "value": "3c93e08a78755a10f8777f88938ba1dd",
          "displayValue": "3c93e08a78755a10f8777f88938ba1dd",
          "type": "GUID"
        },
        "sys_created_by": {
          "name": "sys_created_by",
          "label": "Created by",
          "value": "maint",
          "display_value": "maint",
          "type": "string"
        },
        "sys_updated_by": {
          "name": "sys_updated_by",
          "label": "Updated by",
          "value": "maint",
          "display_value": "maint",
          "type": "string"
        },
        "sys_created_on": {
          "name": "sys_created_on",
          "label": "Created",
          "value": "2024-11-12 08:11:59",
          "display_value": "2024-11-12 00:11:59",
          "type": "glide_date_time"
        },
        "sys_updated_on": {
          "name": "sys_updated_on",
          "label": "Updated",
          "value": "2024-11-12 08:11:59",
          "display_value": "2024-11-12 00:11:59",
          "type": "glide_date_time"
        },
        "number": {
          "name": "number",
          "label": "Number",
          "value": "SAL0010126",
          "display_value": "SAL0010126",
          "type": "string"
        },
        "sales_agreement": {
          "name": "sales_agreement",
          "label": "Sales agreement",
          "value": "bc93e08a78755a10f8777f88938ba1d8",
          "display_value": "SA0010106",
          "type": "reference"
        },
        "short_description": {
          "name": "short_description",
          "label": "Short description",
          "value": "this is sample sa line 1",
          "display_value": "this is sample sa line 1",
          "type": "string"
        },
        "start_date": {
          "name": "start_date",
          "label": "Start date",
          "value": "2024-02-01",
          "display_value": "2024-02-01",
          "type": "glide_date"
        },
        "end_date": {
          "name": "end_date",
          "label": "End date",
          "value": "2024-11-30",
          "display_value": "2024-11-30",
          "type": "glide_date"
        },
        "state": {
          "name": "state",
          "label": "State",
          "value": "active",
          "display_value": "Active",
          "type": "string"
        },
        "product_offering": {
          "name": "product_offering",
          "label": "Product offering",
          "value": null,
          "display_value": "",
          "type": "reference"
        },
        "product_specification": {
          "name": "product_specification",
          "label": "Product specification",
          "value": null,
          "display_value": "",
          "type": "reference"
        },
        "product_model": {
          "name": "product_model",
          "label": "Product model",
          "value": null,
          "display_value": "",
          "type": "reference"
        },
        "price_list": {
          "name": "price_list",
          "label": "Price list",
          "value": "19d29513d0e63110f8770dbf976be122",
          "display_value": "Standard Price List",
          "type": "reference"
        },
        "parent_line": {
          "name": "parent_line",
          "label": "Parent line",
          "value": null,
          "display_value": "",
          "type": "reference"
        },
        "unit_net_price": {
          "name": "unit_net_price",
          "label": "Unit net price",
          "value": "0",
          "display_value": "£0.00",
          "type": "currency"
        },
        "quantity": {
          "name": "quantity",
          "label": "Quantity",
          "value": "2",
          "display_value": "2",
          "type": "decimal"
        },
        "unit_of_measure": null,
        "shipping_location": {
          "name": "shipping_location",
          "label": "Shipping location",
          "value": null,
          "display_value": "",
          "type": "reference"
        },
        "total_one_time_price": {
          "name": "total_one_time_price",
          "label": "Total one-time price",
          "value": "0",
          "display_value": "£0.00",
          "type": "currency"
        },
        "total_recurring_price": {
          "name": "total_recurring_price",
          "label": "Total recurring price",
          "value": "0",
          "display_value": "£0.00",
          "type": "currency"
        },
        "top_agreement_line": null,
        "quote_line": {
          "name": "quote_line",
          "label": "Quote line",
          "value": null,
          "display_value": "",
          "type": "reference"
        },
        "sales_agreement_line_characteristics": [
          {
            "sys_id": {
              "label": "Sys ID",
              "value": "b093e08a78755a10f8777f88938ba1e0",
              "displayValue": "b093e08a78755a10f8777f88938ba1e0",
              "type": "GUID"
            },
            "sys_created_by": {
              "name": "sys_created_by",
              "label": "Created by",
              "value": "maint",
              "display_value": "maint",
              "type": "string"
            },
            "sys_updated_by": {
              "name": "sys_updated_by",
              "label": "Updated by",
              "value": "maint",
              "display_value": "maint",
              "type": "string"
            },
            "sys_created_on": {
              "name": "sys_created_on",
              "label": "Created",
              "value": "2024-11-12 08:11:59",
              "display_value": "2024-11-12 00:11:59",
              "type": "glide_date_time"
            },
            "sys_updated_on": {
              "name": "sys_updated_on",
              "label": "Updated",
              "value": "2024-11-12 08:11:59",
              "display_value": "2024-11-12 00:11:59",
              "type": "glide_date_time"
            },
            "sales_agreement": {
              "name": "sales_agreement",
              "label": "Sales agreement",
              "value": "bc93e08a78755a10f8777f88938ba1d8",
              "display_value": "SA0010106",
              "type": "reference"
            },
            "sales_agreement_line": {
              "name": "sales_agreement_line",
              "label": "Sales agreement line",
              "value": "3c93e08a78755a10f8777f88938ba1dd",
              "display_value": "SAL0010126",
              "type": "reference"
            },
            "characteristic": {
              "name": "characteristic",
              "label": "Characteristic",
              "value": "4d289f1a775131108e191e599a5a99c7",
              "display_value": "AC",
              "type": "reference"
            },
            "type": {
              "name": "type",
              "label": "Type",
              "value": "coverage",
              "display_value": "Coverage",
              "type": "string"
            },
            "characteristic_option": {
              "name": "characteristic_option",
              "label": "Characteristic option",
              "value": null,
              "display_value": "",
              "type": "reference"
            },
            "value": {
              "name": "value",
              "label": "Value",
              "value": null,
              "display_value": "",
              "type": "string"
            }
          }
        ],
        "sales_agreement_line_adjustments": [
          {
            "sys_id": {
              "label": "Sys ID",
              "value": "7093e08a78755a10f8777f88938ba1e1",
              "displayValue": "7093e08a78755a10f8777f88938ba1e1",
              "type": "GUID"
            },
            "sys_created_by": {
              "name": "sys_created_by",
              "label": "Created by",
              "value": "maint",
              "display_value": "maint",
              "type": "string"
            },
            "sys_updated_by": {
              "name": "sys_updated_by",
              "label": "Updated by",
              "value": "maint",
              "display_value": "maint",
              "type": "string"
            },
            "sys_created_on": {
              "name": "sys_created_on",
              "label": "Created",
              "value": "2024-11-12 08:11:59",
              "display_value": "2024-11-12 00:11:59",
              "type": "glide_date_time"
            },
            "sys_updated_on": {
              "name": "sys_updated_on",
              "label": "Updated",
              "value": "2024-11-12 08:11:59",
              "display_value": "2024-11-12 00:11:59",
              "type": "glide_date_time"
            },
            "sales_agreement": {
              "name": "sales_agreement",
              "label": "Sales agreement",
              "value": "bc93e08a78755a10f8777f88938ba1d8",
              "display_value": "SA0010106",
              "type": "reference"
            },
            "sales_agreement_line": {
              "name": "sales_agreement_line",
              "label": "Sales Agreement Line",
              "value": "3c93e08a78755a10f8777f88938ba1dd",
              "display_value": "SAL0010126",
              "type": "reference"
            },
            "adjustment_type": {
              "name": "adjustment_type",
              "label": "Adjustment type",
              "value": "d88bc79653dd91105c0eddeeff7b12c1",
              "display_value": "Markup amount",
              "type": "reference"
            },
            "adjustment_source": {
              "name": "adjustment_source",
              "label": "Adjustment source",
              "value": "MANUAL",
              "display_value": "Manual",
              "type": "string"
            },
            "adjustment_value": {
              "name": "adjustment_value",
              "label": "Adjustment value",
              "value": "123",
              "display_value": "123",
              "type": "decimal"
            },
            "applicable_to": {
              "name": "applicable_to",
              "label": "Applicable to",
              "value": "UNIT_QTY",
              "display_value": "Unit Quantity",
              "type": "string"
            },
            "short_description": {
              "name": "short_description",
              "label": "Short description",
              "value": "line adjustment",
              "display_value": "line adjustment",
              "type": "string"
            },
            "number": {
              "name": "number",
              "label": "Number",
              "value": "SALA0010031",
              "display_value": "SALA0010031",
              "type": "string"
            },
            "quantity": {
              "name": "quantity",
              "label": "Quantity",
              "value": "3",
              "display_value": "3",
              "type": "integer"
            },
            "total_amount": {
              "name": "total_amount",
              "label": "Total amount",
              "value": "0",
              "display_value": "£0.00",
              "type": "currency"
            },
            "amount": {
              "name": "amount",
              "label": "Amount",
              "value": "0",
              "display_value": "£0.00",
              "type": "currency"
            }
          }
        ],
        "child_sales_agreement_lines": [
          {
            "sys_id": {
              "label": "Sys ID",
              "value": "7893e08a78755a10f8777f88938ba1e2",
              "displayValue": "7893e08a78755a10f8777f88938ba1e2",
              "type": "GUID"
            },
            "sys_created_by": {
              "name": "sys_created_by",
              "label": "Created by",
              "value": "maint",
              "display_value": "maint",
              "type": "string"
            },
            "sys_updated_by": {
              "name": "sys_updated_by",
              "label": "Updated by",
              "value": "maint",
              "display_value": "maint",
              "type": "string"
            },
            "sys_created_on": {
              "name": "sys_created_on",
              "label": "Created",
              "value": "2024-11-12 08:11:59",
              "display_value": "2024-11-12 00:11:59",
              "type": "glide_date_time"
            },
            "sys_updated_on": {
              "name": "sys_updated_on",
              "label": "Updated",
              "value": "2024-11-12 08:11:59",
              "display_value": "2024-11-12 00:11:59",
              "type": "glide_date_time"
            },
            "number": {
              "name": "number",
              "label": "Number",
              "value": "SAL0010127",
              "display_value": "SAL0010127",
              "type": "string"
            },
            "sales_agreement": {
              "name": "sales_agreement",
              "label": "Sales agreement",
              "value": "bc93e08a78755a10f8777f88938ba1d8",
              "display_value": "SA0010106",
              "type": "reference"
            },
            "short_description": {
              "name": "short_description",
              "label": "Short description",
              "value": "this is sample sa line 1",
              "display_value": "this is sample sa line 1",
              "type": "string"
            },
            "start_date": {
              "name": "start_date",
              "label": "Start date",
              "value": "2024-02-01",
              "display_value": "2024-02-01",
              "type": "glide_date"
            },
            "end_date": {
              "name": "end_date",
              "label": "End date",
              "value": "2024-11-30",
              "display_value": "2024-11-30",
              "type": "glide_date"
            },
            "state": {
              "name": "state",
              "label": "State",
              "value": "active",
              "display_value": "Active",
              "type": "string"
            },
            "product_offering": {
              "name": "product_offering",
              "label": "Product offering",
              "value": null,
              "display_value": "",
              "type": "reference"
            },
            "product_specification": {
              "name": "product_specification",
              "label": "Product specification",
              "value": null,
              "display_value": "",
              "type": "reference"
            },
            "product_model": {
              "name": "product_model",
              "label": "Product model",
              "value": null,
              "display_value": "",
              "type": "reference"
            },
            "price_list": {
              "name": "price_list",
              "label": "Price list",
              "value": "19d29513d0e63110f8770dbf976be122",
              "display_value": "Standard Price List",
              "type": "reference"
            },
            "parent_line": {
              "name": "parent_line",
              "label": "Parent line",
              "value": "3c93e08a78755a10f8777f88938ba1dd",
              "display_value": "SAL0010126",
              "type": "reference"
            },
            "unit_net_price": {
              "name": "unit_net_price",
              "label": "Unit net price",
              "value": "0",
              "display_value": "£0.00",
              "type": "currency"
            },
            "quantity": {
              "name": "quantity",
              "label": "Quantity",
              "value": "2",
              "display_value": "2",
              "type": "decimal"
            },
            "unit_of_measure": null,
            "shipping_location": {
              "name": "shipping_location",
              "label": "Shipping location",
              "value": null,
              "display_value": "",
              "type": "reference"
            },
            "total_one_time_price": {
              "name": "total_one_time_price",
              "label": "Total one-time price",
              "value": "0",
              "display_value": "£0.00",
              "type": "currency"
            },
            "total_recurring_price": {
              "name": "total_recurring_price",
              "label": "Total recurring price",
              "value": "0",
              "display_value": "£0.00",
              "type": "currency"
            },
            "top_agreement_line": null,
            "quote_line": {
              "name": "quote_line",
              "label": "Quote line",
              "value": null,
              "display_value": "",
              "type": "reference"
            },
            "sales_agreement_line_characteristics": [
              {
                "sys_id": {
                  "label": "Sys ID",
                  "value": "74932c8a78755a10f8777f88938ba132",
                  "displayValue": "74932c8a78755a10f8777f88938ba132",
                  "type": "GUID"
                },
                "sys_created_by": {
                  "name": "sys_created_by",
                  "label": "Created by",
                  "value": "maint",
                  "display_value": "maint",
                  "type": "string"
                },
                "sys_updated_by": {
                  "name": "sys_updated_by",
                  "label": "Updated by",
                  "value": "maint",
                  "display_value": "maint",
                  "type": "string"
                },
                "sys_created_on": {
                  "name": "sys_created_on",
                  "label": "Created",
                  "value": "2024-11-12 08:11:59",
                  "display_value": "2024-11-12 00:11:59",
                  "type": "glide_date_time"
                },
                "sys_updated_on": {
                  "name": "sys_updated_on",
                  "label": "Updated",
                  "value": "2024-11-12 08:11:59",
                  "display_value": "2024-11-12 00:11:59",
                  "type": "glide_date_time"
                },
                "sales_agreement": {
                  "name": "sales_agreement",
                  "label": "Sales agreement",
                  "value": "bc93e08a78755a10f8777f88938ba1d8",
                  "display_value": "SA0010106",
                  "type": "reference"
                },
                "sales_agreement_line": {
                  "name": "sales_agreement_line",
                  "label": "Sales agreement line",
                  "value": "7893e08a78755a10f8777f88938ba1e2",
                  "display_value": "SAL0010127",
                  "type": "reference"
                },
                "characteristic": {
                  "name": "characteristic",
                  "label": "Characteristic",
                  "value": "4d289f1a775131108e191e599a5a99c7",
                  "display_value": "AC",
                  "type": "reference"
                },
                "type": {
                  "name": "type",
                  "label": "Type",
                  "value": "coverage",
                  "display_value": "Coverage",
                  "type": "string"
                },
                "characteristic_option": {
                  "name": "characteristic_option",
                  "label": "Characteristic option",
                  "value": null,
                  "display_value": "",
                  "type": "reference"
                },
                "value": {
                  "name": "value",
                  "label": "Value",
                  "value": null,
                  "display_value": "",
                  "type": "string"
                }
              }
            ],
            "sales_agreement_line_adjustments": [],
            "child_sales_agreement_lines": []
          },
          {
            "sys_id": {
              "label": "Sys ID",
              "value": "78932c8a78755a10f8777f88938ba133",
              "displayValue": "78932c8a78755a10f8777f88938ba133",
              "type": "GUID"
            },
            "sys_created_by": {
              "name": "sys_created_by",
              "label": "Created by",
              "value": "maint",
              "display_value": "maint",
              "type": "string"
            },
            "sys_updated_by": {
              "name": "sys_updated_by",
              "label": "Updated by",
              "value": "maint",
              "display_value": "maint",
              "type": "string"
            },
            "sys_created_on": {
              "name": "sys_created_on",
              "label": "Created",
              "value": "2024-11-12 08:11:59",
              "display_value": "2024-11-12 00:11:59",
              "type": "glide_date_time"
            },
            "sys_updated_on": {
              "name": "sys_updated_on",
              "label": "Updated",
              "value": "2024-11-12 08:11:59",
              "display_value": "2024-11-12 00:11:59",
              "type": "glide_date_time"
            },
            "number": {
              "name": "number",
              "label": "Number",
              "value": "SAL0010128",
              "display_value": "SAL0010128",
              "type": "string"
            },
            "sales_agreement": {
              "name": "sales_agreement",
              "label": "Sales agreement",
              "value": "bc93e08a78755a10f8777f88938ba1d8",
              "display_value": "SA0010106",
              "type": "reference"
            },
            "short_description": {
              "name": "short_description",
              "label": "Short description",
              "value": "this is sample sa line 1",
              "display_value": "this is sample sa line 1",
              "type": "string"
            },
            "start_date": {
              "name": "start_date",
              "label": "Start date",
              "value": "2024-02-01",
              "display_value": "2024-02-01",
              "type": "glide_date"
            },
            "end_date": {
              "name": "end_date",
              "label": "End date",
              "value": "2024-11-30",
              "display_value": "2024-11-30",
              "type": "glide_date"
            },
            "state": {
              "name": "state",
              "label": "State",
              "value": "active",
              "display_value": "Active",
              "type": "string"
            },
            "product_offering": {
              "name": "product_offering",
              "label": "Product offering",
              "value": null,
              "display_value": "",
              "type": "reference"
            },
            "product_specification": {
              "name": "product_specification",
              "label": "Product specification",
              "value": null,
              "display_value": "",
              "type": "reference"
            },
            "product_model": {
              "name": "product_model",
              "label": "Product model",
              "value": null,
              "display_value": "",
              "type": "reference"
            },
            "price_list": {
              "name": "price_list",
              "label": "Price list",
              "value": "19d29513d0e63110f8770dbf976be122",
              "display_value": "Standard Price List",
              "type": "reference"
            },
            "parent_line": {
              "name": "parent_line",
              "label": "Parent line",
              "value": "3c93e08a78755a10f8777f88938ba1dd",
              "display_value": "SAL0010126",
              "type": "reference"
            },
            "unit_net_price": {
              "name": "unit_net_price",
              "label": "Unit net price",
              "value": "0",
              "display_value": "£0.00",
              "type": "currency"
            },
            "quantity": {
              "name": "quantity",
              "label": "Quantity",
              "value": "2",
              "display_value": "2",
              "type": "decimal"
            },
            "unit_of_measure": null,
            "shipping_location": {
              "name": "shipping_location",
              "label": "Shipping location",
              "value": null,
              "display_value": "",
              "type": "reference"
            },
            "total_one_time_price": {
              "name": "total_one_time_price",
              "label": "Total one-time price",
              "value": "0",
              "display_value": "£0.00",
              "type": "currency"
            },
            "total_recurring_price": {
              "name": "total_recurring_price",
              "label": "Total recurring price",
              "value": "0",
              "display_value": "£0.00",
              "type": "currency"
            },
            "top_agreement_line": null,
            "quote_line": {
              "name": "quote_line",
              "label": "Quote line",
              "value": null,
              "display_value": "",
              "type": "reference"
            },
            "sales_agreement_line_characteristics": [
              {
                "sys_id": {
                  "label": "Sys ID",
                  "value": "38932c8a78755a10f8777f88938ba134",
                  "displayValue": "38932c8a78755a10f8777f88938ba134",
                  "type": "GUID"
                },
                "sys_created_by": {
                  "name": "sys_created_by",
                  "label": "Created by",
                  "value": "maint",
                  "display_value": "maint",
                  "type": "string"
                },
                "sys_updated_by": {
                  "name": "sys_updated_by",
                  "label": "Updated by",
                  "value": "maint",
                  "display_value": "maint",
                  "type": "string"
                },
                "sys_created_on": {
                  "name": "sys_created_on",
                  "label": "Created",
                  "value": "2024-11-12 08:11:59",
                  "display_value": "2024-11-12 00:11:59",
                  "type": "glide_date_time"
                },
                "sys_updated_on": {
                  "name": "sys_updated_on",
                  "label": "Updated",
                  "value": "2024-11-12 08:11:59",
                  "display_value": "2024-11-12 00:11:59",
                  "type": "glide_date_time"
                },
                "sales_agreement": {
                  "name": "sales_agreement",
                  "label": "Sales agreement",
                  "value": "bc93e08a78755a10f8777f88938ba1d8",
                  "display_value": "SA0010106",
                  "type": "reference"
                },
                "sales_agreement_line": {
                  "name": "sales_agreement_line",
                  "label": "Sales agreement line",
                  "value": "78932c8a78755a10f8777f88938ba133",
                  "display_value": "SAL0010128",
                  "type": "reference"
                },
                "characteristic": {
                  "name": "characteristic",
                  "label": "Characteristic",
                  "value": "4d289f1a775131108e191e599a5a99c7",
                  "display_value": "AC",
                  "type": "reference"
                },
                "type": {
                  "name": "type",
                  "label": "Type",
                  "value": "coverage",
                  "display_value": "Coverage",
                  "type": "string"
                },
                "characteristic_option": {
                  "name": "characteristic_option",
                  "label": "Characteristic option",
                  "value": null,
                  "display_value": "",
                  "type": "reference"
                },
                "value": {
                  "name": "value",
                  "label": "Value",
                  "value": null,
                  "display_value": "",
                  "type": "string"
                }
              }
            ],
            "sales_agreement_line_adjustments": [],
            "child_sales_agreement_lines": []
          }
        ]
      }
    ]
  }
}

```

