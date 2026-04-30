---
title: Consumer API
description: The Consumer API provides endpoints to retrieve and update Customer Service Management \(CSM\) consumer records.Retrieves a specified set of Customer Service Management \(CSM\) consumer records.Retrieves the specified Customer Service Management \(CSM\) consumer record.Creates a new Customer Service Management \(CSM\) consumer.
locale: en-US
release: yokohama
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 17
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# Consumer API

The Consumer API provides endpoints to retrieve and update Customer Service Management \(CSM\) consumer records.

In addition, you can generate new social media profile records when creating a consumer.

The Consumer API requires the Customer Service plugin \(com.sn\_customerservice\) and is provided within the `now` namespace.

Users require the csm\_ws\_integration role for full API access.

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## Consumer - GET /now/consumer

Retrieves a specified set of Customer Service Management \(CSM\) consumer records.

### URL format

Versioned URL: `/api/now/{api_version}/consumer`

Default URL: `/api/now/consumer`

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

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
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|404|Not found. The requested item wasn't found.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

The endpoint may return the following JSON or XML elements in the response body. In addition to the list of elements defined below \(which define the elements in a base system\), the endpoint also returns any custom fields added to the Consumer \[csm\_consumer\] table. For additional information on these elements, refer to your specific table definition \[**System Definition** &gt; **Tables**\].

<table><thead><tr><th>

Element

</th><th>

Description

</th></tr></thead><tbody><tr><td>

active

</td><td id="consumertable-active-entry">

Flag that indicates whether the consumer is active.Possible values:

-   true: Consumer active
-   false: Consumer de-activated

Data type: Boolean

Default: true

</td></tr><tr><td>

business\_phone

</td><td id="consumertable-business_phone-entry">

Business phone number of the consumer.Data type: String

Maximum length: 40

</td></tr><tr><td>

city

</td><td id="consumertable-city-entry">

City in which the consumer resides.Data type: String

Maximum length: 100

</td></tr><tr><td>

country

</td><td id="consumertable-country-entry">

Country in which the consumer resides.Data type: String

Maximum length: 40

</td></tr><tr><td>

date\_format

</td><td id="consumertable-date_format-entry">

Format in which to display dates.Valid values:

-   dd-mm-yyyy
-   dd/mm/yyyy
-   dd.mm.yyyy
-   mm-dd-yyyy
-   yyyy-mm-dd

Data type: String

Maximum length: 40

Default: blank \(system date format\)

</td></tr><tr><td>

email

</td><td id="consumertable-email-entry">

Email address of the consumer.Data type: String

Maximum length: 100

</td></tr><tr><td>

fax

</td><td id="consumertable-fax-entry">

Fax number of the consumer.Data type: String

Maximum length: 40

</td></tr><tr><td>

first\_name

</td><td id="consumertable-first_name-entry">

Consumer first name.Data type: String

Maximum length: 50

</td></tr><tr><td>

gender

</td><td id="consumertable-gender-entry">

Gender of the consumer.Data type: String

Maximum length: 40

</td></tr><tr><td>

home\_phone

</td><td id="consumertable-home_phone-entry">

Home phone number of the consumer.Data type: String

Maximum length: 40

</td></tr><tr><td>

household

</td><td id="consumertable-household-entry">

Sys\_id of the record that describes the household characteristics.Data type: String

Table: Household \[csm\_household\]

</td></tr><tr><td>

last\_name

</td><td id="consumertable-last_name-entry">

Consumer last name.Data type: String

Maximum length: 50

</td></tr><tr><td>

middle\_name

</td><td id="consumertable-middle_name-entry">

Consumer middle name.Data type: String

Maximum length: 50

</td></tr><tr><td>

mobile\_phone

</td><td id="consumertable-mobile_phone-entry">

Consumer mobile phone number.Data type: String

Maximum length: 40

</td></tr><tr><td>

name

</td><td id="consumertable-name-entry">

Consumer full name; first\_name+middle\_name+last\_name.Data type: String

Maximum length: 152

</td></tr><tr><td>

notes

</td><td id="consumertable-notes-entry">

Notes on consumer.Data type: String

Maximum length: 4,000

</td></tr><tr><td>

notification

</td><td id="consumertable-notification-entry">

Indicates whether the consumer should receive notifications.Valid values:

-   1: Disabled
-   2: Enabled

Data type: Number \(Integer\)

Maximum length: 40

Default: 2

</td></tr><tr><td>

number

</td><td id="consumertable-number-entry">

Unique number associated with the consumer.Data type: String

Maximum length: 40

</td></tr><tr><td>

photo

</td><td id="consumertable-photo-entry">

Photo of the consumer.Data type: Image

</td></tr><tr><td>

preferred\_language

</td><td id="consumertable-preferred_language-entry">

Consumer primary language.Data type: String

Maximum length: 3

</td></tr><tr><td>

prefix

</td><td id="consumertable-prefix-entry">

Consumer name prefix such as, Dr., Mr., Mrs., or Ms.Data type: String

Maximum length: 40

</td></tr><tr><td>

primary

</td><td id="consumertable-primary-entry">

Flag that indicates whether this is the primary consumer.Possible values:

-   true: Primary consumer
-   false: Not primary consumer

Data type: Boolean

Default: false

</td></tr><tr><td>

state

</td><td id="consumertable-state-entry">

State in which the consumer resides.Data type: String

Maximum length: 100

</td></tr><tr><td>

street

</td><td id="consumertable-street-entry">

Consumer street address.Data type: String

Maximum length: 255

</td></tr><tr><td>

suffix

</td><td id="consumertable-suffix-entry">

Consumer name suffix such as Jr., Sr., or II.Data type: String

</td></tr><tr><td>

sys\_created\_by

</td><td id="consumertable-sys_created_by-entry">

User that created the consumer record.Data type: String

Maximum length: 40

</td></tr><tr><td>

sys\_created\_on

</td><td id="consumertable-sys_created_on-entry">

Date and time the consumer record was originally created.Data type: String

</td></tr><tr><td>

sys\_domain

</td><td id="consumertable-sys_domain-entry">

ServiceNow domain in which the consumer information resides.Data type: String

</td></tr><tr><td>

sys\_id

</td><td id="consumertable-sys_id-entry">

Unique identifier for the consumer.Data type: String

</td></tr><tr><td>

sys\_mod\_count

</td><td id="consumertable-sys_mod_count-entry">

Number of times that the associated consumer information has been modified.Data type: Number \(Integer\)

</td></tr><tr><td>

sys\_tags

</td><td>

System tags.Data type: String

</td></tr><tr><td>

sys\_updated\_by

</td><td id="consumertable-sys_updated_by-entry">

User that last updated the consumer information.Data type: String

Maximum length: 40

</td></tr><tr><td>

sys\_updated\_on

</td><td id="consumertable-sys_updated_on-entry">

Date and time when the consumer information was last updated.Data type: String

</td></tr><tr><td>

time\_format

</td><td id="consumertable-time_format-entry">

Format in which to display time.Valid values:

-   hh.mm.ss a: hh.mm.ss \(12 hour\)
-   hh:mm:ss a: hh:mm:ss \(12 hour\)
-   HH.mm.ss: hh.mm.ss \(24 hour\)
-   HH:mm:ss: hh:mm:ss \(24 hour\)

Data type: String

Maximum length: 40

Default: blank \(system time format\)

</td></tr><tr><td>

time\_zone

</td><td id="consumertable-time_zone-entry">

Consumer time zone, such as Canada/Central or US/Eastern.Data type: String

Maximum length: 40

</td></tr><tr><td>

title

</td><td id="consumertable-title-entry">

Consumer business title such as Manager, Software Developer, or Contractor.Data type: String

Maximum length: 60

</td></tr><tr><td>

user

</td><td id="consumertable-user-entry">

Sys\_id of the consumer user. Data type: String

Table: Consumer User \[csm\_consumer\_user\]

</td></tr><tr><td>

zip

</td><td id="consumertable-zip-entry">

Consumer zip code. Data type: String

Maximum length: 40

</td></tr></tbody>
</table>### cURL request

```
curl "https://instance.servicenow.com/api/now/consumer?sysparm_query=account=86837a386f0331003b3c498f5d3ee4ca&sysparm_limit=2&sysparm_offset=2>;rel="next" \
--request GET \
--header "Accept:application/json" \
--user "username":"password"
```

```
{
  "result": [
    {
      "country": "USA",
      "notes": "",
      "gender": "Male",
      "city": "Plano",
      "prefix": "",
      "sys_updated_on": "2016-08-12 00:19:12",
      "suffix": "",
      "title": "",
      "number": "CSMR0000004",
      "notification": "2",
      "sys_id": "01d8403fdb1b1200b6075200cf961941",
      "business_phone": "",
      "sys_updated_by": "prithvi",
      "mobile_phone": "",
      "street": "6900 Dallas Pkwy",
      "sys_created_on": "2016-06-16 19:20:13",
      "sys_domain": "global",
      "state": "TX",
      "fax": "",
      "first_name": "Harding",
      "email": "harding.asher@mailinator.com",
      "preferred_language": "",
      "sys_created_by": "guest",
      "zip": "75024",
      "home_phone": "",
      "time_format": "",
      "sys_mod_count": "8",
      "last_name": "Asher",
      "photo": "",
      "active": "true",
      "middle_name": "",
      "time_zone": "",
      "sys_tags": "",
      "name": "Harding Asher",
      "household": "",
      "date_format": "",
      "user": "c3d35d82c37122005871d44d81d3ae91",
      "primary": "false"
    },
    {
      "country": "USA",
      "notes": "",
      "gender": "Male",
      "city": "San Francisco",
      "prefix": "",
      "sys_updated_on": "2016-08-12 00:20:27",
      "suffix": "",
      "title": "",
      "number": "CSMR0000002",
      "notification": "2",
      "sys_id": "a0488cfbdb1b1200b6075200cf9619db",
      "business_phone": "",
      "sys_updated_by": "prithvi",
      "mobile_phone": "",
      "street": "144 2nd St",
      "sys_created_on": "2016-06-16 19:17:44",
      "sys_domain": "global",
      "state": "CA",
      "fax": "",
      "first_name": "Sam",
      "email": "sam.collins@mailinator.com",
      "preferred_language": "",
      "sys_created_by": "guest",
      "zip": "94105",
      "home_phone": "",
      "time_format": "",
      "sys_mod_count": "13",
      "last_name": "Collins",
      "photo": "",
      "active": "true",
      "middle_name": "",
      "time_zone": "",
      "sys_tags": "",
      "name": "Sam Collins",
      "household": "",
      "date_format": "",
      "user": "64488cfbdb1b1200b6075200cf9619db",
      "primary": "false"
    }
  ]
}

```

## Consumer - GET /now/consumer/\{id\}

Retrieves the specified Customer Service Management \(CSM\) consumer record.

### URL format

Versioned URL: `/api/now/{api_version}/consumer/{id}`

Default URL: `/api/now/consumer/{id}`

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

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

Sys\_id of the consumer record to return.Data type: String

Table: Consumer \[csm\_consumer\]

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

401

</td><td id="entry-401-status-code">

Unauthorized. The user credentials are incorrect or have not been passed.

</td></tr><tr><td>

404

</td><td>

Indicates that the request is invalid. Could be due to one of the following reasons:-   Requested case doesn't exist.
-   User doesn't have access to the consumer record.

</td></tr><tr><td>

500

</td><td id="entry-500-status-code">

Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.

</td></tr></tbody>
</table>### Response body parameters \(JSON or XML\)

The endpoint may return the following JSON or XML elements in the response body. In addition to the list of elements defined below \(which define the elements in a base system\), the endpoint also returns any custom fields added to the Consumer \[csm\_consumer\] table. For additional information on these elements, refer to your specific table definition \[**System Definition** &gt; **Tables**\].

<table><thead><tr><th>

Element

</th><th>

Description

</th></tr></thead><tbody><tr><td>

active

</td><td id="consumertable-active-entry">

Flag that indicates whether the consumer is active.Possible values:

-   true: Consumer active
-   false: Consumer de-activated

Data type: Boolean

Default: true

</td></tr><tr><td>

business\_phone

</td><td id="consumertable-business_phone-entry">

Business phone number of the consumer.Data type: String

Maximum length: 40

</td></tr><tr><td>

city

</td><td id="consumertable-city-entry">

City in which the consumer resides.Data type: String

Maximum length: 100

</td></tr><tr><td>

country

</td><td id="consumertable-country-entry">

Country in which the consumer resides.Data type: String

Maximum length: 40

</td></tr><tr><td>

date\_format

</td><td id="consumertable-date_format-entry">

Format in which to display dates.Valid values:

-   dd-mm-yyyy
-   dd/mm/yyyy
-   dd.mm.yyyy
-   mm-dd-yyyy
-   yyyy-mm-dd

Data type: String

Maximum length: 40

Default: blank \(system date format\)

</td></tr><tr><td>

email

</td><td id="consumertable-email-entry">

Email address of the consumer.Data type: String

Maximum length: 100

</td></tr><tr><td>

fax

</td><td id="consumertable-fax-entry">

Fax number of the consumer.Data type: String

Maximum length: 40

</td></tr><tr><td>

first\_name

</td><td id="consumertable-first_name-entry">

Consumer first name.Data type: String

Maximum length: 50

</td></tr><tr><td>

gender

</td><td id="consumertable-gender-entry">

Gender of the consumer.Data type: String

Maximum length: 40

</td></tr><tr><td>

home\_phone

</td><td id="consumertable-home_phone-entry">

Home phone number of the consumer.Data type: String

Maximum length: 40

</td></tr><tr><td>

household

</td><td id="consumertable-household-entry">

Sys\_id of the record that describes the household characteristics.Data type: String

Table: Household \[csm\_household\]

</td></tr><tr><td>

last\_name

</td><td id="consumertable-last_name-entry">

Consumer last name.Data type: String

Maximum length: 50

</td></tr><tr><td>

middle\_name

</td><td id="consumertable-middle_name-entry">

Consumer middle name.Data type: String

Maximum length: 50

</td></tr><tr><td>

mobile\_phone

</td><td id="consumertable-mobile_phone-entry">

Consumer mobile phone number.Data type: String

Maximum length: 40

</td></tr><tr><td>

name

</td><td id="consumertable-name-entry">

Consumer full name; first\_name+middle\_name+last\_name.Data type: String

Maximum length: 152

</td></tr><tr><td>

notes

</td><td id="consumertable-notes-entry">

Notes on consumer.Data type: String

Maximum length: 4,000

</td></tr><tr><td>

notification

</td><td id="consumertable-notification-entry">

Indicates whether the consumer should receive notifications.Valid values:

-   1: Disabled
-   2: Enabled

Data type: Number \(Integer\)

Maximum length: 40

Default: 2

</td></tr><tr><td>

number

</td><td id="consumertable-number-entry">

Unique number associated with the consumer.Data type: String

Maximum length: 40

</td></tr><tr><td>

photo

</td><td id="consumertable-photo-entry">

Photo of the consumer.Data type: Image

</td></tr><tr><td>

preferred\_language

</td><td id="consumertable-preferred_language-entry">

Consumer primary language.Data type: String

Maximum length: 3

</td></tr><tr><td>

prefix

</td><td id="consumertable-prefix-entry">

Consumer name prefix such as, Dr., Mr., Mrs., or Ms.Data type: String

Maximum length: 40

</td></tr><tr><td>

primary

</td><td id="consumertable-primary-entry">

Flag that indicates whether this is the primary consumer.Possible values:

-   true: Primary consumer
-   false: Not primary consumer

Data type: Boolean

Default: false

</td></tr><tr><td>

state

</td><td id="consumertable-state-entry">

State in which the consumer resides.Data type: String

Maximum length: 100

</td></tr><tr><td>

street

</td><td id="consumertable-street-entry">

Consumer street address.Data type: String

Maximum length: 255

</td></tr><tr><td>

suffix

</td><td id="consumertable-suffix-entry">

Consumer name suffix such as Jr., Sr., or II.Data type: String

</td></tr><tr><td>

sys\_created\_by

</td><td id="consumertable-sys_created_by-entry">

User that created the consumer record.Data type: String

Maximum length: 40

</td></tr><tr><td>

sys\_created\_on

</td><td id="consumertable-sys_created_on-entry">

Date and time the consumer record was originally created.Data type: String

</td></tr><tr><td>

sys\_domain

</td><td id="consumertable-sys_domain-entry">

ServiceNow domain in which the consumer information resides.Data type: String

</td></tr><tr><td>

sys\_id

</td><td id="consumertable-sys_id-entry">

Unique identifier for the consumer.Data type: String

</td></tr><tr><td>

sys\_mod\_count

</td><td id="consumertable-sys_mod_count-entry">

Number of times that the associated consumer information has been modified.Data type: Number \(Integer\)

</td></tr><tr><td>

sys\_updated\_by

</td><td id="consumertable-sys_updated_by-entry">

User that last updated the consumer information.Data type: String

Maximum length: 40

</td></tr><tr><td>

sys\_updated\_on

</td><td id="consumertable-sys_updated_on-entry">

Date and time when the consumer information was last updated.Data type: String

</td></tr><tr><td>

time\_format

</td><td id="consumertable-time_format-entry">

Format in which to display time.Valid values:

-   hh.mm.ss a: hh.mm.ss \(12 hour\)
-   hh:mm:ss a: hh:mm:ss \(12 hour\)
-   HH.mm.ss: hh.mm.ss \(24 hour\)
-   HH:mm:ss: hh:mm:ss \(24 hour\)

Data type: String

Maximum length: 40

Default: blank \(system time format\)

</td></tr><tr><td>

time\_zone

</td><td id="consumertable-time_zone-entry">

Consumer time zone, such as Canada/Central or US/Eastern.Data type: String

Maximum length: 40

</td></tr><tr><td>

title

</td><td id="consumertable-title-entry">

Consumer business title such as Manager, Software Developer, or Contractor.Data type: String

Maximum length: 60

</td></tr><tr><td>

user

</td><td id="consumertable-user-entry">

Sys\_id of the consumer user. Data type: String

Table: Consumer User \[csm\_consumer\_user\]

</td></tr><tr><td>

zip

</td><td id="consumertable-zip-entry">

Consumer zip code. Data type: String

Maximum length: 40

</td></tr></tbody>
</table>### cURL request

```
curl "https://instance.servicenow.com/api/now/consumer/01d8403fdb1b1200b6075200cf961941 \
--request GET \
--header "Accept:application/json" \
--user "username":"password"

```

```
{
  "result": {
    "country": "USA",
    "notes": "",
    "gender": "Male",
    "city": "Plano",
    "prefix": "",
    "sys_updated_on": "2016-08-12 00:19:12",
    "suffix": "",
    "title": "",
    "number": "CSMR0000004",
    "notification": "2",
    "sys_id": "01d8403fdb1b1200b6075200cf961941",
    "business_phone": "",
    "sys_updated_by": "prithvi",
    "mobile_phone": "",
    "street": "6900 Dallas Pkwy",
    "sys_created_on": "2016-06-16 19:20:13",
    "sys_domain": "global",
    "state": "TX",
    "fax": "",
    "first_name": "Harding",
    "email": "harding.asher@mailinator.com",
    "preferred_language": "",
    "sys_created_by": "guest",
    "zip": "75024",
    "home_phone": "",
    "time_format": "",
    "sys_mod_count": "8",
    "last_name": "Asher",
    "photo": "",
    "active": "true",
    "middle_name": "",
    "time_zone": "",
    "sys_tags": "",
    "name": "Harding Asher",
    "household": "",
    "date_format": "",
    "user": "c3d35d82c37122005871d44d81d3ae91",
    "primary": "false"
  }
}

```

## Consumer - POST /now/consumer

Creates a new Customer Service Management \(CSM\) consumer.

In addition, you can create a social media profile for the consumer using this endpoint. To create the profile, you must specify the following parameters in the request body:

-   **social\_channel**
-   **social\_handle**
-   **social\_handle\_url**

**Warning:** This endpoint does not perform parameter validation as doing so can create excessive overhead. If a request parameter is misspelled, is not valid, or is not supported by the endpoint, it is ignored without warning.

### URL format

Versioned URL: `/api/now/{api_version}/consumer`

Default URL: `/api/now/consumer`

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

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
</table>|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_request_body"><thead><tr><th>

Element

</th><th>

Description

</th></tr></thead><tbody><tr><td>

active

</td><td id="consumertable-active-entry">

Flag that indicates whether the consumer is active.Possible values:

-   true: Consumer active
-   false: Consumer de-activated

Data type: Boolean

Default: true

</td></tr><tr><td>

business\_phone

</td><td id="consumertable-business_phone-entry">

Business phone number of the consumer.Data type: String

Maximum length: 40

</td></tr><tr><td>

city

</td><td id="consumertable-city-entry">

City in which the consumer resides.Data type: String

Maximum length: 100

</td></tr><tr><td>

country

</td><td id="consumertable-country-entry">

Country in which the consumer resides.Data type: String

Maximum length: 40

</td></tr><tr><td>

date\_format

</td><td id="consumertable-date_format-entry">

Format in which to display dates.Valid values:

-   dd-mm-yyyy
-   dd/mm/yyyy
-   dd.mm.yyyy
-   mm-dd-yyyy
-   yyyy-mm-dd

Data type: String

Maximum length: 40

Default: blank \(system date format\)

</td></tr><tr><td>

email

</td><td id="consumertable-email-entry">

Email address of the consumer.Data type: String

Maximum length: 100

</td></tr><tr><td>

fax

</td><td id="consumertable-fax-entry">

Fax number of the consumer.Data type: String

Maximum length: 40

</td></tr><tr><td>

first\_name

</td><td id="consumertable-first_name-entry">

Consumer first name.Data type: String

Maximum length: 50

</td></tr><tr><td>

gender

</td><td id="consumertable-gender-entry">

Gender of the consumer.Data type: String

Maximum length: 40

</td></tr><tr><td>

home\_phone

</td><td id="consumertable-home_phone-entry">

Home phone number of the consumer.Data type: String

Maximum length: 40

</td></tr><tr><td>

household

</td><td id="consumertable-household-entry">

Sys\_id of the record that describes the household characteristics.Data type: String

Table: Household \[csm\_household\]

</td></tr><tr><td>

last\_name

</td><td id="consumertable-last_name-entry">

Consumer last name.Data type: String

Maximum length: 50

</td></tr><tr><td>

middle\_name

</td><td id="consumertable-middle_name-entry">

Consumer middle name.Data type: String

Maximum length: 50

</td></tr><tr><td>

mobile\_phone

</td><td id="consumertable-mobile_phone-entry">

Consumer mobile phone number.Data type: String

Maximum length: 40

</td></tr><tr><td>

name

</td><td id="consumertable-name-entry">

Consumer full name; first\_name+middle\_name+last\_name.Data type: String

Maximum length: 152

</td></tr><tr><td>

notes

</td><td id="consumertable-notes-entry">

Notes on consumer.Data type: String

Maximum length: 4,000

</td></tr><tr><td>

notification

</td><td id="consumertable-notification-entry">

Indicates whether the consumer should receive notifications.Valid values:

-   1: Disabled
-   2: Enabled

Data type: Number \(Integer\)

Maximum length: 40

Default: 2

</td></tr><tr><td>

photo

</td><td id="consumertable-photo-entry">

Photo of the consumer.Data type: Image

</td></tr><tr><td>

preferred\_language

</td><td id="consumertable-preferred_language-entry">

Consumer primary language.Data type: String

Maximum length: 3

</td></tr><tr><td>

prefix

</td><td id="consumertable-prefix-entry">

Consumer name prefix such as, Dr., Mr., Mrs., or Ms.Data type: String

Maximum length: 40

</td></tr><tr><td>

primary

</td><td id="consumertable-primary-entry">

Flag that indicates whether this is the primary consumer.Possible values:

-   true: Primary consumer
-   false: Not primary consumer

Data type: Boolean

Default: false

</td></tr><tr><td>

social\_channel

</td><td>

Social media channel to which the consumer is associated such as Twitter, Facebook, or Instagram.Data type: String

</td></tr><tr><td>

social\_handle

</td><td>

User handle on the social media channel.Data type: String

</td></tr><tr><td>

social\_handle\_url

</td><td>

URL to the consumer's social channel handle.Data type: String

</td></tr><tr><td>

state

</td><td id="consumertable-state-entry">

State in which the consumer resides.Data type: String

Maximum length: 100

</td></tr><tr><td>

street

</td><td id="consumertable-street-entry">

Consumer street address.Data type: String

Maximum length: 255

</td></tr><tr><td>

suffix

</td><td id="consumertable-suffix-entry">

Consumer name suffix such as Jr., Sr., or II.Data type: String

</td></tr><tr><td>

time\_format

</td><td id="consumertable-time_format-entry">

Format in which to display time.Valid values:

-   hh.mm.ss a: hh.mm.ss \(12 hour\)
-   hh:mm:ss a: hh:mm:ss \(12 hour\)
-   HH.mm.ss: hh.mm.ss \(24 hour\)
-   HH:mm:ss: hh:mm:ss \(24 hour\)

Data type: String

Maximum length: 40

Default: blank \(system time format\)

</td></tr><tr><td>

time\_zone

</td><td id="consumertable-time_zone-entry">

Consumer time zone, such as Canada/Central or US/Eastern.Data type: String

Maximum length: 40

</td></tr><tr><td>

title

</td><td id="consumertable-title-entry">

Consumer business title such as Manager, Software Developer, or Contractor.Data type: String

Maximum length: 60

</td></tr><tr><td>

user

</td><td id="consumertable-user-entry">

Sys\_id of the consumer user. Data type: String

Table: Consumer User \[csm\_consumer\_user\]

</td></tr><tr><td>

zip

</td><td id="consumertable-zip-entry">

Consumer zip code. Data type: String

Maximum length: 40

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
|201|New consumer record was successfully created.|
|400|Bad Request. A bad request type or malformed request was detected.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|500|Internal Server Error. A logic error on the server-side code occurred.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Element

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

Sys\_id of the newly created consumer record.Data type: String

</td></tr></tbody>
</table>### cURL request

```
curl -X POST "https://instance.servicenow.com/api/now/consumer" \
-H "Accept: application/json" \
-H "Content-Type: application/json" \
-d " { \
  "country": "USA", \
  "notes": "Never comes in before 10am", \
  "gender": "Female", \
  "city": "San Marcos", \
  "prefix": "Ms", \
  "title": "Director", \
  "notification": "1", \
  "business_phone": "(555)555-1234", \
  "mobile_phone": "(555)555-1235", \
  "street": "123 Sesame St", \
  "state": "CA", \
  "fax": "(555)555-1236", \
  "first_name": "Jane", \
  "zip": "92001", \
  "home_phone": "(555)555-1234", \
  "last_name": "Brown", \
  "active": "true", \
  "middle_name": "Dell", \
  "time_zone": "PST", \
  "name": "Jane Brown", \
  "household": "4", \
  "user": "c3d35d82c37122005871d44d81d3ae91", \
  "primary": "false" \
}"
--user "username":"password"
```

```
{
    "result": "0f5c13addb93230057c3fd441d9619b8"
}
```

