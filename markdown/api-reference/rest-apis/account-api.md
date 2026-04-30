---
title: Account API
description: The Account API provides endpoints to retrieve Customer Service Management \(CSM\) account records.Retrieves a specified set of Customer Service Management \(CSM\) accounts.Retrieves the specified Customer Service Management \(CSM\) account.
locale: en-US
release: zurich
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 14
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# Account API

The Account API provides endpoints to retrieve Customer Service Management \(CSM\) account records.

This API requires the Customer Service plugin \(com.sn\_customerservice\) and is provided within the `now` namespace.

Users require the csm\_ws\_integration role for full API access.

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## Account - GET /now/account

Retrieves a specified set of Customer Service Management \(CSM\) accounts.

### URL format

Versioned URL: `/api/now/{api_version}/account`

Default URL: `/api/now/account`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`. Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sysparm\_limit

</td><td id="sysparm-limit-entry">

Maximum number of records to return. For requests that exceed this number of records, use the **sysparm\_offset** parameter to paginate record retrieval.

In the response, the boolean parameter **hasMore** is returned. It indicates whether there are more records to return that meet the filter criteria.

Data type: Number

Default: 10

</td></tr><tr><td>

sysparm\_offset

</td><td id="sysparm-offset-entry">

Starting record index for which to begin retrieving records. Use this value to paginate record retrieval. This functionality enables the retrieval of all records, regardless of the number of records, in small manageable chunks.

For example, the first time you call this endpoint, **sysparm\_offset** is set to "0". To simply page through all available records, use `sysparm_offset=sysparm_offset+sysparm_limit`, until you reach the end of all records.

Do not pass a negative number in the **sysparm\_offset** parameter.

Data type: Number

Default: 0

</td></tr><tr><td>

sysparm\_query

</td><td id="sysparm-query-entry">

Encoded query used to filter the result set.For example:

`sysparm_query=caller_id=javascript:gs.getUserID()^active=true`

The encoded query supports order by. To sort responses based on certain fields, use the ORDERBY and ORDERBYDESC clauses in **sysparm\_query**. For example, `sysparm_query=active=true^ORDERBYnumber^ORDERBYDESCcategory` filters all active records and orders the results in ascending order by number first, and then in descending order by category.

If part of the query is invalid, such as by specifying an invalid field name, the instance ignores the invalid part. It then returns rows using only the valid portion of the query. You can control this behavior using the property **glide.invalid\_query.returns\_no\_rows**. Set this property to true to return no rows on an invalid query.

**Note:** The **glide.invalid\_query.returns\_no\_rows** property controls the behavior of all queries across the instance, such as in lists, scripts \(GlideRecord.query\(\)\), and web service APIs.

Data type: String

</td></tr></tbody>
</table>|Element|Description|
|-------|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

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

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table id="table_pgg_h4b_1dc"><thead><tr><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr id="accounttable-account_code-row"><td>

account\_code

</td><td id="accounttable-account_code-entry">

Unique combination of values that an application uses to identify budget forecasts and budget plans.Data type: String

Maximum length: 255

</td></tr><tr id="accounttable-account_parent-row"><td>

account\_parent

</td><td id="accounttable-account_parent-entry">

Sys\_id of the parent account of this account. Located in the Account \[customer\_account\] table.Data type: String

</td></tr><tr id="accounttable-account_path-row"><td>

account\_path

</td><td id="accounttable-account_path-entry">

Path from the parent to the child accounts in the account hierarchy.Data type: String

Maximum length: 255

</td></tr><tr id="accounttable-active_escalation-row"><td>

active\_escalation

</td><td id="accounttable-active_escalation-entry">

Sys\_id of the active escalation associated with the account.Data type: String

Table: Escalation \[sn\_customerservice\_escalation\]

</td></tr><tr id="accounttable-apple_icon-row"><td>

apple\_icon

</td><td id="accounttable-apple_icon-entry">

Icon for iPhone home page bookmarks.Data type: Image

</td></tr><tr id="accounttable-banner_image-row"><td>

banner\_image

</td><td id="accounttable-banner_image-entry">

Banner image that appears on the customer portal.Data type: Image

</td></tr><tr id="accounttable-banner_image_light-row"><td>

banner\_image\_light

</td><td id="accounttable-banner_image_light-entry">

Small banner image.Data type: Image

</td></tr><tr id="accounttable-banner_text-row"><td>

banner\_text

</td><td id="accounttable-banner_text-entry">

Banner text that appears on the customer portal.Data type: String

Maximum length: 4,000

</td></tr><tr id="accounttable-city-row"><td>

city

</td><td id="accounttable-city-entry">

City in which the company that is associated with this account resides.Data type: String

Maximum length: 50

</td></tr><tr id="accounttable-contact-row"><td>

contact

</td><td id="accounttable-contact-entry">

Sys\_id of a contact record associated with this account.Data type: String

Table: User \[sys\_user\]

</td></tr><tr id="accounttable-country-row"><td>

country

</td><td id="accounttable-country-entry">

Country in which the company that is associated with this account resides.Data type: String

Maximum length: 40

Default: USA

</td></tr><tr id="accounttable-customer-row"><td>

customer

</td><td id="accounttable-customer-entry">

Flag that indicates whether the account is a customer account, as opposed to a partner account.Possible values:

-   true: Customer account
-   false: Partner account

Data type: Boolean

Default: false

</td></tr><tr id="accounttable-discount-row"><td>

discount

</td><td id="accounttable-discount-entry">

Discount given to the account on purchases.Data type: Number

Maximum length: 15

</td></tr><tr id="accounttable-fax_phone-row"><td>

fax\_phone

</td><td id="accounttable-fax_phone-entry">

Primary fax phone number for the company associated with this account.Data type: String

Maximum length: 40

</td></tr><tr id="accounttable-fiscal_year-row"><td>

fiscal\_year

</td><td id="accounttable-fiscal_year-entry">

Fiscal year for the company associated with the account.Data type: String

</td></tr><tr id="accounttable-lat_long_error-row"><td>

lat\_long\_error

</td><td id="accounttable-lat_long_error-entry">

Difference in the actual location as compared to latitude and longitude information.Data type: String

Maximum length: 1,000

</td></tr><tr id="accounttable-latitude-row"><td>

latitude

</td><td id="accounttable-latitude-entry">

Latitude of the company associated with this account.Data type: Number \(floating point number\)

Maximum length: 40

</td></tr><tr id="accounttable-longitude-row"><td>

longitude

</td><td id="accounttable-longitude-entry">

Longitude of the company associated with this account.Data type: Number \(floating point number\)

Maximum length: 40

</td></tr><tr id="accounttable-manufactuer-row"><td>

manufacturer

</td><td id="accounttable-manufactuer-entry">

Flag that indicates whether the company associated with this account manufactures goods.Possible values:

-   true: Manufactures goods
-   false: Does not manufacture goods

Data type: Boolean

Default: false

</td></tr><tr id="accounttable-market_cap-row"><td>

market\_cap

</td><td id="accounttable-market_cap-entry">

Market value of the associated company's publicly traded stock shares.Data type: Number \(currency\)

Maximum length: 20

</td></tr><tr id="accounttable-name-row"><td>

name

</td><td id="accounttable-name-entry">

Name of the company associated with this account.Data type: String

Maximum length: 80

</td></tr><tr id="accounttable-notes-row"><td>

notes

</td><td id="accounttable-notes-entry">

Additional information about the company.Data type: String

Maximum length: 4,000

</td></tr><tr id="accounttable-num_employees-row"><td>

num\_employees

</td><td id="accounttable-num_employees-entry">

Number of people employed by the company.Data type: Number \(Integer\)

Maximum length: 40

</td></tr><tr id="accounttable-number-row"><td>

number

</td><td id="accounttable-number-entry">

Number that identifies this account.Data type: String

Maximum length: 40

</td></tr><tr id="accounttable-parent-row"><td>

parent

</td><td id="accounttable-parent-entry">

Sys\_id of the parent account of this account.Data type: String

Table: Company \[core\_company\]

</td></tr><tr id="accounttable-partner-row"><td>

partner

</td><td id="accounttable-partner-entry">

Flag that indicates whether the account is a partner account or a customer account.Possible values:

-   true: Partner account
-   false: Customer account

Data type: Boolean

Default: false

</td></tr><tr id="accounttable-phone-row"><td>

phone

</td><td id="accounttable-phone-entry">

Primary phone number for the company.Data type: String

</td></tr><tr id="accounttable-primary-row"><td>

primary

</td><td id="accounttable-primary-entry">

Flag that indicates whether this is a primary account.Possible values:

-   true: Primary account
-   false: Secondary account

Data type: Boolean

Default: false

</td></tr><tr id="accounttable-primary_contact-row"><td>

primary\_contact

</td><td id="accounttable-primary_contact-entry">

Sys\_id of the primary contact for the account.Data type: String

Table: Contact \[customer\_contact\]

</td></tr><tr id="accounttable-profits-row"><td>

profits

</td><td id="accounttable-profits-entry">

Profit information entered for this account.Data type: Number \(Currency\)

Maximum length: 40

</td></tr><tr id="accounttable-publicly_traded-row"><td>

publicly\_traded

</td><td id="accounttable-publicly_traded-entry">

Flag that indicates whether the company associated with this account is publicly traded on the stock exchange.Possible values:

-   true: Publicly traded
-   false: Private company

Data type: Boolean

</td></tr><tr id="accounttable-rank_tier-row"><td>

rank\_tier

</td><td id="accounttable-rank_tier-entry">

Type of account.Possible values:

-   blacklist
-   other
-   strategic
-   tactical
-   valued

Data type: String

Maximum length: 40

</td></tr><tr id="accounttable-registration_code-row"><td>

registration\_code

</td><td id="accounttable-registration_code-entry">

Unique code that customers use when requesting a login on the customer portal. This code provides a method for validating the customer on the company before granting access.Data type: String

Maximum length: 40

</td></tr><tr id="accounttable-revenue_per_year-row"><td>

revenue\_per\_year

</td><td id="accounttable-revenue_per_year-entry">

Revenue produced by the company associated with this account.Data type: Number \(Currency\)

Maximum length: 20

</td></tr><tr id="accounttable-state-row"><td>

state

</td><td id="accounttable-state-entry">

State in which the company resides.Data type: String

Maximum length: 40

</td></tr><tr id="accounttable-stock_price-row"><td>

stock\_price

</td><td id="accounttable-stock_price-entry">

Price of the company stock.Data type: String

Maximum length: 40

</td></tr><tr id="accounttable-stock_symbol-row"><td>

stock\_symbol

</td><td id="accounttable-stock_symbol-entry">

Stock symbol of the company.Data type: String

Maximum length: 40

</td></tr><tr id="accounttable-street-row"><td>

street

</td><td id="accounttable-street-entry">

Street address of the company.Data type: String

Maximum length: 255

</td></tr><tr id="accounttable-sys_class_name-row"><td>

sys\_class\_name

</td><td id="accounttable-sys_class_name-entry">

Table that contains the associated account record.Data type: String

</td></tr><tr id="accounttable-sys_created_by-row"><td>

sys\_created\_by

</td><td id="accounttable-sys_created_by-entry">

User that originally created the account.Data type: String

Maximum length: 40

</td></tr><tr id="accounttable-sys_created_on-row"><td>

sys\_created\_on

</td><td id="accounttable-sys_created_on-entry">

Date and time that the account was originally created.Data type: String

</td></tr><tr id="accounttable-sys_id-row"><td>

sys\_id

</td><td id="accounttable-sys_id-entry">

Sys\_id for the account record.Data type: String

</td></tr><tr id="accounttable-sys_mod_count-row"><td>

sys\_mod\_count

</td><td id="accounttable-sys_mod_count-entry">

Number of times the account information has been updated.Data type: Number \(Integer\)

</td></tr><tr id="accounttable-sys_updated_by-row"><td>

sys\_updated\_by

</td><td id="accounttable-sys_updated_by-entry">

User that last modified the account information.Data type: String

Maximum length: 40

</td></tr><tr id="accounttable-sys_updated_on-row"><td>

sys\_updated\_on

</td><td id="accounttable-sys_updated_on-entry">

Date and time the account information was last updated.Data type: String

</td></tr><tr id="accounttable-theme-row"><td>

theme

</td><td id="accounttable-theme-entry">

Sys\_id of the customer portal theme used by this account.Data type: String

Table: Theme \[sys\_ui\_theme\]

</td></tr><tr id="accounttable-vendor-row"><td>

vendor

</td><td id="accounttable-vendor-entry">

Flag that indicates whether the company associated with this account is a vendor.Possible values:

-   true: Vendor
-   false: Not a vendor

Data type: Boolean

Default: false

</td></tr><tr id="accounttable-vendor_manager-row"><td>

vendor\_manager

</td><td id="accounttable-vendor_manager-entry">

List of sys\_ids of the vendor managers for the account.Data type: String

Table: User \[sys\_user\]

</td></tr><tr id="accounttable-vendor_type-row"><td>

vendor\_type

</td><td id="accounttable-vendor_type-entry">

List of sys\_ids of the type of vendor such as, applications, hardware, services, or software.Data type: String

Table: Vendor Type \[vendor\_type\]

</td></tr><tr id="accounttable-website-row"><td>

website

</td><td id="accounttable-website-entry">

URL of the website for the company.Data type: String

Maximum length: 1,024

</td></tr><tr id="accounttable-zip-row"><td>

zip

</td><td id="accounttable-zip-entry">

Zip code of the company.Data type: String

Maximum length: 40

</td></tr></tbody>
</table>### cURL request

```
curl "https://instance.servicenow.com/api/now/account?sysparm_limit=2&sysparm_offset=2>;rel="next" \
--request GET \
--header "Accept:application/json" \
--user 'username':'password'

```

```
{
"result": [
  {
   "banner_image_light": "",
   "country": "USA",
   "parent": "",
   "notes": "",
   "stock_symbol": "",
   "discount": "",
   "active_escalation": "",
   "sys_updated_on": "2019-01-03 19:37:55",
   "apple_icon": "",
   "number": "ACCT0000003",
    "sys_updated_by": "admin",
    "fiscal_year": "",
    "sys_created_on": "2018-12-23 05:25:17",
    "contact": "",
    "stock_price": "",
    "state": "",
    "banner_image": "",
    "sys_created_by": "admin",
    "longitude": "",
    "zip": "BR1 3QR",
    "profits": "0",
    "phone": "+44 20 8466 9992",
    "fax_phone": "",
    "name": "Boxeo EMEA",
    "banner_text": "",
    "account_code": "~~~~3",
    "primary": "false",
    "city": "Bromley",
    "latitude": "",
    "sys_class_name": "customer_account",
    "manufacturer": "false",
    "account_parent": "86837a386f0331003b3c498f5d3ee4ca",
    "sys_id": "3eedd08413651200042ab3173244b088",
    "market_cap": "0",
    "num_employees": "",
    "rank_tier": "",
    "street": "18 London Rd",
    "vendor": "false",
    "lat_long_error": "",
    "theme": "",
    "vendor_type": "",
    "website": "",
    "revenue_per_year": "0",
    "publicly_traded": "false",
    "sys_mod_count": "5",
    "sys_tags": "",
    "partner": "false",
    "registration_code": "BOXEO-EMEA",
    "vendor_manager": "",
    "account_path": "~~~~1/~~~~3",
    "primary_contact": "ff66c1254fb81200025ba3618110c76e",
    "customer": "true"
  },
  {
    "banner_image_light": "",
    "country": "USA",
    "parent": "",
    "notes": "",
    "stock_symbol": "",
    "discount": "",
    "active_escalation": "",
    "sys_updated_on": "2019-01-03 19:38:04",
    "apple_icon": "",
    "number": "ACCT0000004",
    "sys_updated_by": "admin",
    "fiscal_year": "",
    "sys_created_on": "2018-12-23 05:19:24",
    "contact": "",
    "stock_price": "",
    "state": "",
    "banner_image": "",
    "sys_created_by": "admin",
    "longitude": "",
    "zip": "V5L 2G4",
    "profits": "0",
    "phone": "+1 604-255-9797",
    "fax_phone": "",
    "name": "Boxeo Canada",
    "banner_text": "",
    "account_code": "~~~~4",
    "primary": "false",
    "city": "Vancouver",
    "latitude": "",
    "sys_class_name": "customer_account",
    "manufacturer": "false",
    "account_parent": "86837a386f0331003b3c498f5d3ee4ca",
    "sys_id": "609cd80413651200042ab3173244b03e",
    "market_cap": "0",
    "num_employees": "",
    "rank_tier": "",
    "street": "1362 Venables St,, BC V5L 2G4, Canada",
    "vendor": "false",
    "lat_long_error": "",
    "theme": "",
    "vendor_type": "",
    "website": "",
    "revenue_per_year": "0",
    "publicly_traded": "false",
    "sys_mod_count": "5",
    "sys_tags": "",
    "partner": "false",
    "registration_code": "BOXEO-CANADA",
    "vendor_manager": "",
    "account_path": "~~~~1/~~~~4",
    "primary_contact": "c07424a54f781200025ba3618110c746",
    "customer": "true"
  }
 ]
}
```

## Account - GET /now/account/\{id\}

Retrieves the specified Customer Service Management \(CSM\) account.

### URL format

Versioned URL: `/api/now/{api_version}/account/{id}`

Default URL: `/api/now/account/{id}`

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

Sys\_id of the account to retrieve. Located in the Customer \[customer\_account\] table.Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

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

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

<table><thead><tr><th>

Status code

</th><th>

Description

</th></tr></thead><tbody><tr><td>

200

</td><td id="entry-200-status-code">

Successful. The request was successfully processed.

</td></tr><tr><td>

404

</td><td>

Indicates that the request is invalid.i89Possible cause:

-   Requested case doesn’t exist.
-   User doesn’t have access to the account record.

</td></tr></tbody>
</table>### Response body parameters \(JSON or XML\)

<table id="table_pgg_h4b_1dc"><thead><tr><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr id="accounttable-account_code-row"><td>

account\_code

</td><td id="accounttable-account_code-entry">

Unique combination of values that an application uses to identify budget forecasts and budget plans.Data type: String

Maximum length: 255

</td></tr><tr id="accounttable-account_parent-row"><td>

account\_parent

</td><td id="accounttable-account_parent-entry">

Sys\_id of the parent account of this account. Located in the Account \[customer\_account\] table.Data type: String

</td></tr><tr id="accounttable-account_path-row"><td>

account\_path

</td><td id="accounttable-account_path-entry">

Path from the parent to the child accounts in the account hierarchy.Data type: String

Maximum length: 255

</td></tr><tr id="accounttable-active_escalation-row"><td>

active\_escalation

</td><td id="accounttable-active_escalation-entry">

Sys\_id of the active escalation associated with the account.Data type: String

Table: Escalation \[sn\_customerservice\_escalation\]

</td></tr><tr id="accounttable-apple_icon-row"><td>

apple\_icon

</td><td id="accounttable-apple_icon-entry">

Icon for iPhone home page bookmarks.Data type: Image

</td></tr><tr id="accounttable-banner_image-row"><td>

banner\_image

</td><td id="accounttable-banner_image-entry">

Banner image that appears on the customer portal.Data type: Image

</td></tr><tr id="accounttable-banner_image_light-row"><td>

banner\_image\_light

</td><td id="accounttable-banner_image_light-entry">

Small banner image.Data type: Image

</td></tr><tr id="accounttable-banner_text-row"><td>

banner\_text

</td><td id="accounttable-banner_text-entry">

Banner text that appears on the customer portal.Data type: String

Maximum length: 4,000

</td></tr><tr id="accounttable-city-row"><td>

city

</td><td id="accounttable-city-entry">

City in which the company that is associated with this account resides.Data type: String

Maximum length: 50

</td></tr><tr id="accounttable-contact-row"><td>

contact

</td><td id="accounttable-contact-entry">

Sys\_id of a contact record associated with this account.Data type: String

Table: User \[sys\_user\]

</td></tr><tr id="accounttable-country-row"><td>

country

</td><td id="accounttable-country-entry">

Country in which the company that is associated with this account resides.Data type: String

Maximum length: 40

Default: USA

</td></tr><tr id="accounttable-customer-row"><td>

customer

</td><td id="accounttable-customer-entry">

Flag that indicates whether the account is a customer account, as opposed to a partner account.Possible values:

-   true: Customer account
-   false: Partner account

Data type: Boolean

Default: false

</td></tr><tr id="accounttable-discount-row"><td>

discount

</td><td id="accounttable-discount-entry">

Discount given to the account on purchases.Data type: Number

Maximum length: 15

</td></tr><tr id="accounttable-fax_phone-row"><td>

fax\_phone

</td><td id="accounttable-fax_phone-entry">

Primary fax phone number for the company associated with this account.Data type: String

Maximum length: 40

</td></tr><tr id="accounttable-fiscal_year-row"><td>

fiscal\_year

</td><td id="accounttable-fiscal_year-entry">

Fiscal year for the company associated with the account.Data type: String

</td></tr><tr id="accounttable-lat_long_error-row"><td>

lat\_long\_error

</td><td id="accounttable-lat_long_error-entry">

Difference in the actual location as compared to latitude and longitude information.Data type: String

Maximum length: 1,000

</td></tr><tr id="accounttable-latitude-row"><td>

latitude

</td><td id="accounttable-latitude-entry">

Latitude of the company associated with this account.Data type: Number \(floating point number\)

Maximum length: 40

</td></tr><tr id="accounttable-longitude-row"><td>

longitude

</td><td id="accounttable-longitude-entry">

Longitude of the company associated with this account.Data type: Number \(floating point number\)

Maximum length: 40

</td></tr><tr id="accounttable-manufactuer-row"><td>

manufacturer

</td><td id="accounttable-manufactuer-entry">

Flag that indicates whether the company associated with this account manufactures goods.Possible values:

-   true: Manufactures goods
-   false: Does not manufacture goods

Data type: Boolean

Default: false

</td></tr><tr id="accounttable-market_cap-row"><td>

market\_cap

</td><td id="accounttable-market_cap-entry">

Market value of the associated company's publicly traded stock shares.Data type: Number \(currency\)

Maximum length: 20

</td></tr><tr id="accounttable-name-row"><td>

name

</td><td id="accounttable-name-entry">

Name of the company associated with this account.Data type: String

Maximum length: 80

</td></tr><tr id="accounttable-notes-row"><td>

notes

</td><td id="accounttable-notes-entry">

Additional information about the company.Data type: String

Maximum length: 4,000

</td></tr><tr id="accounttable-num_employees-row"><td>

num\_employees

</td><td id="accounttable-num_employees-entry">

Number of people employed by the company.Data type: Number \(Integer\)

Maximum length: 40

</td></tr><tr id="accounttable-number-row"><td>

number

</td><td id="accounttable-number-entry">

Number that identifies this account.Data type: String

Maximum length: 40

</td></tr><tr id="accounttable-parent-row"><td>

parent

</td><td id="accounttable-parent-entry">

Sys\_id of the parent account of this account.Data type: String

Table: Company \[core\_company\]

</td></tr><tr id="accounttable-partner-row"><td>

partner

</td><td id="accounttable-partner-entry">

Flag that indicates whether the account is a partner account or a customer account.Possible values:

-   true: Partner account
-   false: Customer account

Data type: Boolean

Default: false

</td></tr><tr id="accounttable-phone-row"><td>

phone

</td><td id="accounttable-phone-entry">

Primary phone number for the company.Data type: String

</td></tr><tr id="accounttable-primary-row"><td>

primary

</td><td id="accounttable-primary-entry">

Flag that indicates whether this is a primary account.Possible values:

-   true: Primary account
-   false: Secondary account

Data type: Boolean

Default: false

</td></tr><tr id="accounttable-primary_contact-row"><td>

primary\_contact

</td><td id="accounttable-primary_contact-entry">

Sys\_id of the primary contact for the account.Data type: String

Table: Contact \[customer\_contact\]

</td></tr><tr id="accounttable-profits-row"><td>

profits

</td><td id="accounttable-profits-entry">

Profit information entered for this account.Data type: Number \(Currency\)

Maximum length: 40

</td></tr><tr id="accounttable-publicly_traded-row"><td>

publicly\_traded

</td><td id="accounttable-publicly_traded-entry">

Flag that indicates whether the company associated with this account is publicly traded on the stock exchange.Possible values:

-   true: Publicly traded
-   false: Private company

Data type: Boolean

</td></tr><tr id="accounttable-rank_tier-row"><td>

rank\_tier

</td><td id="accounttable-rank_tier-entry">

Type of account.Possible values:

-   blacklist
-   other
-   strategic
-   tactical
-   valued

Data type: String

Maximum length: 40

</td></tr><tr id="accounttable-registration_code-row"><td>

registration\_code

</td><td id="accounttable-registration_code-entry">

Unique code that customers use when requesting a login on the customer portal. This code provides a method for validating the customer on the company before granting access.Data type: String

Maximum length: 40

</td></tr><tr id="accounttable-revenue_per_year-row"><td>

revenue\_per\_year

</td><td id="accounttable-revenue_per_year-entry">

Revenue produced by the company associated with this account.Data type: Number \(Currency\)

Maximum length: 20

</td></tr><tr id="accounttable-state-row"><td>

state

</td><td id="accounttable-state-entry">

State in which the company resides.Data type: String

Maximum length: 40

</td></tr><tr id="accounttable-stock_price-row"><td>

stock\_price

</td><td id="accounttable-stock_price-entry">

Price of the company stock.Data type: String

Maximum length: 40

</td></tr><tr id="accounttable-stock_symbol-row"><td>

stock\_symbol

</td><td id="accounttable-stock_symbol-entry">

Stock symbol of the company.Data type: String

Maximum length: 40

</td></tr><tr id="accounttable-street-row"><td>

street

</td><td id="accounttable-street-entry">

Street address of the company.Data type: String

Maximum length: 255

</td></tr><tr id="accounttable-sys_class_name-row"><td>

sys\_class\_name

</td><td id="accounttable-sys_class_name-entry">

Table that contains the associated account record.Data type: String

</td></tr><tr id="accounttable-sys_created_by-row"><td>

sys\_created\_by

</td><td id="accounttable-sys_created_by-entry">

User that originally created the account.Data type: String

Maximum length: 40

</td></tr><tr id="accounttable-sys_created_on-row"><td>

sys\_created\_on

</td><td id="accounttable-sys_created_on-entry">

Date and time that the account was originally created.Data type: String

</td></tr><tr id="accounttable-sys_id-row"><td>

sys\_id

</td><td id="accounttable-sys_id-entry">

Sys\_id for the account record.Data type: String

</td></tr><tr id="accounttable-sys_mod_count-row"><td>

sys\_mod\_count

</td><td id="accounttable-sys_mod_count-entry">

Number of times the account information has been updated.Data type: Number \(Integer\)

</td></tr><tr id="accounttable-sys_updated_by-row"><td>

sys\_updated\_by

</td><td id="accounttable-sys_updated_by-entry">

User that last modified the account information.Data type: String

Maximum length: 40

</td></tr><tr id="accounttable-sys_updated_on-row"><td>

sys\_updated\_on

</td><td id="accounttable-sys_updated_on-entry">

Date and time the account information was last updated.Data type: String

</td></tr><tr id="accounttable-theme-row"><td>

theme

</td><td id="accounttable-theme-entry">

Sys\_id of the customer portal theme used by this account.Data type: String

Table: Theme \[sys\_ui\_theme\]

</td></tr><tr id="accounttable-vendor-row"><td>

vendor

</td><td id="accounttable-vendor-entry">

Flag that indicates whether the company associated with this account is a vendor.Possible values:

-   true: Vendor
-   false: Not a vendor

Data type: Boolean

Default: false

</td></tr><tr id="accounttable-vendor_manager-row"><td>

vendor\_manager

</td><td id="accounttable-vendor_manager-entry">

List of sys\_ids of the vendor managers for the account.Data type: String

Table: User \[sys\_user\]

</td></tr><tr id="accounttable-vendor_type-row"><td>

vendor\_type

</td><td id="accounttable-vendor_type-entry">

List of sys\_ids of the type of vendor such as, applications, hardware, services, or software.Data type: String

Table: Vendor Type \[vendor\_type\]

</td></tr><tr id="accounttable-website-row"><td>

website

</td><td id="accounttable-website-entry">

URL of the website for the company.Data type: String

Maximum length: 1,024

</td></tr><tr id="accounttable-zip-row"><td>

zip

</td><td id="accounttable-zip-entry">

Zip code of the company.Data type: String

Maximum length: 40

</td></tr></tbody>
</table>### cURL request

```
curl "https://instance.servicenow.com/api/now/account/bf60bef46f0331003b3c498f5d3ee41a" \
--request GET \
--header "Accept:application/json" \
--user "username":"password"

```

```
{
"result": {
  "banner_image_light": "",
  "country": "USA",
  "parent": "",
  "notes": "",
  "stock_symbol": "",
  "discount": "",
  "active_escalation": "e4fa242887150300fe4433d4c6cb0b5f",
  "sys_updated_on": "2020-07-30 21:57:54",
  "apple_icon": "",
  "number": "ACCT0000009",
  "sys_updated_by": "admin",
  "fiscal_year": "",
  "sys_created_on": "2019-09-16 21:19:27",
  "contact": "bea1fef46f0331003b3c498f5d3ee4c5",
  "stock_price": "",
  "state": "California",
  "banner_image": "",
  "sys_created_by": "venki",
  "longitude": "-122.116445",
  "zip": "94022",
  "profits": "0",
  "phone": "(877) 729-4269",
  "fax_phone": "",
  "name": "Avid Corporation",
  "banner_text": "",
  "account_code": "~~~~9",
  "primary": "false",
  "city": "Los Altos",
  "latitude": "37.402666",
  "sys_class_name": "customer_account",
  "manufacturer": "false",
  "account_parent": "",
  "sys_id": "bf60bef46f0331003b3c498f5d3ee41a",
  "market_cap": "0",
  "num_employees": "",
  "rank_tier": "",
  "street": "4440 El Camino Real",
  "vendor": "false",
  "lat_long_error": "",
  "theme": "",
  "vendor_type": "",
  "website": "http://www.avidcorp.com",
  "revenue_per_year": "0",
  "publicly_traded": "false",
  "sys_mod_count": "10",
  "sys_tags": "",
  "partner": "false",
  "registration_code": "AVID",
  "vendor_manager": "",
  "account_path": "~~~~9",
  "primary_contact": "bea1fef46f0331003b3c498f5d3ee4c5",
  "customer": "true"
 }
}
```

