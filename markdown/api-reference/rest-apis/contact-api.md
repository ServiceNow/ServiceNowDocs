---
title: Contact API
description: The Contact API provides endpoints that enable you to retrieve and update Customer Service Management \(CSM\) contact records.Retrieves a specified set of Customer Service Management \(CSM\) contacts.Retrieves the specified Customer Service Management \(CSM\) contact.Creates a new Customer Service Management \(CSM\) contact.
locale: en-US
release: yokohama
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 26
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# Contact API

The Contact API provides endpoints that enable you to retrieve and update Customer Service Management \(CSM\) contact records.

In addition, you can generate new social media profile records when creating a contact.

The Contact API requires the Customer Service plugin \(com.sn\_customerservice\) and is provided within the `now` namespace.

Users need the csm\_ws\_integration role for full API access.

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## Contact - GET /now/contact

Retrieves a specified set of Customer Service Management \(CSM\) contacts.

### URL format

Versioned URL: `/api/now/{api_version}/contact`

Default URL: `/api/now/contact`

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
</table>|Name|Description|
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

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

The endpoint may return the following JSON or XML elements in the response body. In addition to the list of elements defined below \(which define the elements in a base system\), the endpoint also returns any custom fields added to the Contact \[customer\_contact\] table. For additional information on these elements, refer to your specific table definition \[**System Definition** &gt; **Tables**\].

<table><thead><tr><th>

Element

</th><th>

Description

</th></tr></thead><tbody><tr><td>

account

</td><td id="contacttable-account-enrty">

Sys\_id of the account record to which the contact is associated.Data type: String

Table: Account \[customer\_account\]

</td></tr><tr><td>

active

</td><td id="contacttable-active-entry">

Flag that indicates whether the contact is active within the system.Possible values:

-   true: Contact is active
-   false: Contact is inactive

Data type: Boolean

Default: true

</td></tr><tr><td>

agent\_status

</td><td id="contacttable-agent_status-entry">

Status of the agent.Possible values:

-   Off work
-   On break
-   On route
-   On site

Data type: String

Maximum length: 40

</td></tr><tr><td>

building

</td><td id="contacttable-building-entry">

Sys\_id of the record that describes the building in which the contact resides.Data type: String

Table: Building \[cmn\_building\]

</td></tr><tr><td>

calendar\_integration

</td><td id="contacttable-calendar_integration-entry">

Calendar application that the contact uses.1: Outlook

Data type: Number \(Integer\)

Default: 1

</td></tr><tr><td>

city

</td><td id="contacttable-city-entry">

City in which the contact resides.Data type: String

Maximum length: 40

</td></tr><tr><td>

company

</td><td id="contacttable-company-entry">

Sys\_id of the company record to which the contact is associated.Data type: String

Table: Company \[core\_company\]

</td></tr><tr><td>

cost\_center

</td><td id="contacttable-cost_center-entry">

Sys\_id of the cost center associated with the contact.Data type: String

Table: Cost Center \[cmn\_cost\_center\]

</td></tr><tr><td>

country

</td><td id="contacttable-country-entry">

Country code of the country in which the contact resides.Data type: String

Maximum length: 3

</td></tr><tr><td>

date\_format

</td><td id="contacttable-date_format-entry">

Format in which to display dates to contacts.Valid values:

-   dd/mm/yyyy
-   dd-mm-yyyy
-   dd.mm.yyyy
-   mm-dd-yyyy
-   yyyy-mm-dd

Data type: String

Maximum length: 40

Default: blank \(system date format\)

</td></tr><tr><td>

default\_perspective

</td><td id="contacttable-default_perspective-entry">

Sys\_id of the default perspective for the contact.Data type: String

Table: Menu List \[sys\_perspective\]

</td></tr><tr><td>

department

</td><td id="contacttable-department-entry">

Sys\_id of the department associated with the contact.Data type: String

Table: Department \[cmn\_department\]

</td></tr><tr><td>

edu\_status

</td><td id="contacttable-edu_status-entry">

Education status of the associated contact.Data type: String

Maximum length: 40

Default: faculty

</td></tr><tr><td>

email

</td><td id="contacttable-email-entry">

Contact email address.Data type: String

</td></tr><tr><td>

employee\_number

</td><td id="contacttable-employee_number-entry">

Contact employee number.Data type: String

</td></tr><tr><td>

enable\_multifactor\_authn

</td><td id="contacttable-enable_multifactor_authn-entry">

Flag that indicates whether multifactor authorization is required for the contact to log in to the service portal.Possible values:

-   true: Multifactor authorization enabled
-   false: Multifactor authorization disabled

Data type: Boolean

Default: false

</td></tr><tr><td>

failed\_attempts

</td><td id="contacttable-failed_attempts-entry">

Number of failed log in attempts.Data type: Number \(Integer\)

</td></tr><tr><td>

first\_name

</td><td id="contacttable-first_name-entry">

Contact first name.Data type: String

Maximum length: 50

</td></tr><tr><td>

gender

</td><td id="contacttable-gender-entry">

Contact gender.Data type: String

Maximum length: 40

</td></tr><tr><td>

geolocation\_tracked

</td><td id="contacttable-geolocation_tracked-entry">

Flag that indicates whether the contact location is obtained through geotracking.Possible values:

-   true: Contact location obtained through geotracking
-   false: Contact location not obtained through geotracking

Data type: Boolean

Default value: false

</td></tr><tr><td>

home\_phone

</td><td id="contacttable-home_phone-entry">

Contact home phone number.Data type: String

Maximum length: 40

</td></tr><tr><td>

internal\_integration\_user

</td><td id="contacttable-internal_integration_user-entry">

Flag that indicates whether the contact is an internal integration user.Possible values:

-   true: Internal integration user
-   false: Other type of user

Data type: Boolean

Default: false

</td></tr><tr><td>

introduction

</td><td id="contacttable-introduction-entry">

IntroductionData type: String

Maximum length: 40

</td></tr><tr><td>

last\_login

</td><td id="contacttable-last_login-entry">

Date on which the contact last logged into the system.Data type: String \(Date\)

</td></tr><tr><td>

last\_login\_device

</td><td id="contacttable-last_login_device-entry">

Device the consumer used the last time they logged in to the system.Data type: String

Maximum length: 40

</td></tr><tr><td>

last\_login\_time

</td><td id="contacttable-last_login_time-entry">

Date and time the contact logged in to the system.Data type: String \(Date/time\)

</td></tr><tr><td>

last\_name

</td><td id="contacttable-last_name-entry">

Contact last name.Data type: String

Maximum length: 50

</td></tr><tr><td>

last\_position\_update

</td><td id="contacttable-last_position_update-entry">

Date and time the last position was updated.Data type: String \(Date/time\)

</td></tr><tr><td>

latitude

</td><td id="contacttable-latitude-entry">

Latitude coordinate of the contact.Data type: Number \(Floating point\)

Maximum length: 40

</td></tr><tr><td>

ldap\_server

</td><td id="contacttable-ldap_server-entry">

Sys\_id of the LDAP server used by the contact to last log in to the system. Data type: String

Table: LDAP Server \[ldap\_server\_config\]

</td></tr><tr><td>

location

</td><td id="contacttable-location-entry">

Sys\_id of the record that describes the location of the contactData type: String

Table: Location \[cmn\_location\]

</td></tr><tr><td>

locked\_out

</td><td id="contacttable-locked_out-entry">

Flag that indicates if the contact is locked-out.Possible values:

-   true: Contact locked-out
-   false: Contact not locked-out

Data type: Boolean

Default: false

</td></tr><tr><td>

longitude

</td><td id="contacttable-longitude-entry">

Longitude coordinate of the contact.Data type: Number \(Floating point\)

Maximum length: 40

</td></tr><tr><td>

manager

</td><td id="contacttable-manager-entry">

Sys\_id of the record that describes the direct supervisor of the contact.Data type: String

Table: User \[sys\_user\]

</td></tr><tr><td>

middle\_name

</td><td id="contacttable-middle_name-entry">

Contact middle name.Data type: Number \(Floating point\)

Maximum length: 50

</td></tr><tr><td>

mobile\_phone

</td><td id="contacttable-mobile_phone-entry">

Contact mobile phone number.Data type: String

 Maximum length: 40

</td></tr><tr><td>

name

</td><td id="contacttable-name-entry">

Contact full name.Data type: String

Maximum length: 151

</td></tr><tr><td>

notification

</td><td id="contacttable-notification-entry">

Indicates whether the contact should receive notifications.Valid values:

-   1: Disabled
-   2: Enabled

Data type: Number \(Integer\)

Default: 2

</td></tr><tr><td>

on\_schedule

</td><td id="contacttable-on_schedule-entry">

Indicates the timeliness of dispatched service personnel.Valid values:

-   Ahead: Ahead of schedule.
-   behind\_less30: Behind schedule, but less than 30 minutes.
-   behind\_30to60: Behind schedule between 30 and 60 minutes.
-   behind\_more60: Behind schedule more than 60 minutes.
-   on\_time: On schedule.

Data type: String

Maximum length: 40

</td></tr><tr><td>

phone

</td><td id="contacttable-phone-entry">

Contact business phone number.Data type: String

Maximum length: 40

</td></tr><tr><td>

photo

</td><td id="contacttable-photo-entry">

Photo image of the contact. Data type: String

</td></tr><tr><td>

preferred\_language

</td><td id="contacttable-preferred_language-entry">

Country code of the contact primary language.Data type: String

Maximum length: 3

</td></tr><tr><td>

roles

</td><td id="contacttable-roles-entry">

List of user roles associated with the contact.Data type: String

Maximum length: 40

</td></tr><tr><td>

schedule

</td><td id="contacttable-schedule-entry">

Sys\_id of the record that describes the work schedule for the associated contact.Data type: String

Table: Schedule \[cmn\_schedule\]

</td></tr><tr><td>

source

</td><td id="contacttable-source-entry">

Source of the contact.Data type: String

Maximum length: 255

</td></tr><tr><td>

state

</td><td id="contacttable-state-entry">

State in which the contact resides.Data type: String

Maximum length: 40

</td></tr><tr><td>

street

</td><td id="contacttable-street-entry">

Contact street address.Data type: String

Maximum length: 255

</td></tr><tr><td>

sys\_class\_name

</td><td id="contacttable-sys_class_name-entry">

Table that contains the contact record. Data type: String

Maximum length: 80

</td></tr><tr><td>

sys\_created\_by

</td><td id="contacttable-sys_created_by-entry">

User that originally created the associated contact record.Data type: String

Maximum length: 40

</td></tr><tr><td>

sys\_created\_on

</td><td id="contacttable-sys_created_on-entry">

Data and time the associated contact was originally created.Data type: String \(Date/time\)

</td></tr><tr><td>

sys\_domain

</td><td id="contacttable-sys_domain-entry">

ServiceNow instance domain of the associated contact record.Data type: String

</td></tr><tr><td>

sys\_domain\_path

</td><td id="contacttable-sys_domain_path-entry">

Contact record domain path.Data type: String

Maximum length: 255

Default: / \(global\)

</td></tr><tr><td>

sys\_id

</td><td id="contacttable-sys_id-entry">

Unique identifier for the associated contact record.Data type: String

</td></tr><tr><td>

sys\_mod\_count

</td><td id="contacttable-sys_mod_count-entry">

Number of times that the associated contact record has been modified.Data type: Number \(Integer\)

</td></tr><tr><td>

sys\_tags

</td><td>

System tags.Data type: String

</td></tr><tr><td>

sys\_updated\_by

</td><td id="contacttable-sys_updated_by-entry">

User that last updated the associated contact information.Data type: String

Maximum length: 40

</td></tr><tr><td>

sys\_updated\_on

</td><td id="contacttable-sys_updated_on-entry">

Data and time the associated contact information was updated.Data type: String \(Date/time\)

</td></tr><tr><td>

time\_format

</td><td id="contacttable-time_format-entry">

Format in which to display time.Valid values:

-   hh.mm.ss a: hh.mm.ss \(12 hour\)
-   hh:mm:ss a: hh:mm:ss \(12 hour\)
-   HH.mm.ss: hh.mm.ss \(24 hour\)
-   HH:mm:ss: hh:mm:ss \(24 hour\)

Data type: String

Maximum length: 40

Default: Blank \(system time format\)

</td></tr><tr><td>

time\_sheet\_policy

</td><td id="contacttable-time_sheet_policy-entry">

Sys\_id of the record that contains the time sheet policy for the associated contact.Data type: String

Table: Time Sheet Policy \[time\_sheet\_policy\]

</td></tr><tr><td>

time\_zone

</td><td id="contacttable-time_zone-entry">

Time zone in which the contact resides, such as Canada/Central or US/Eastern.Data type: String

Maximum length: 40

</td></tr><tr><td>

title

</td><td id="contacttable-title-entry">

Contact business title such as Manager, Software Developer, or Contractor.Data type: String

Maximum length: 60

</td></tr><tr><td>

user\_name

</td><td id="contacttable-user_name-entry">

Contact user ID.Data type: String

Maximum length: 40

</td></tr><tr><td>

vip

</td><td id="contacttable-vip-entry">

Flag that indicates whether the associated contact has VIP status.Possible values:

-   true: VIP
-   false: Not VIP

Data type: Boolean

Default: false

</td></tr><tr><td>

web\_service\_access\_only

</td><td id="contacttable-web_service_access_only-entry">

Flag that indicates whether the contact can only access services through the web.Possible values:

-   true: Web access only
-   false: Access through all available methods

Data type: Boolean

Default: false

</td></tr><tr><td>

zip

</td><td id="contacttable-zip-entry">

Contact zip code.Data type: String

Maximum length: 40

</td></tr></tbody>
</table>### cURL request

```
curl "https://instance.servicenow.com/api/now/contact?sysparm_query=account=86837a386f0331003b3c498f5d3ee4ca&sysparm_limit=2&sysparm_offset=2>;rel="next" \
--request GET \
--header "Accept:application/json" \
--user "username":"password"

```

```
{
  "result": [
    {
      "country": "",
      "calendar_integration": "1",
      "last_position_update": "",
      "last_login_time": "2018-03-10 21:48:11",
      "last_login_device": "",
      "source": "",
      "sys_updated_on": "2019-01-03 05:49:34",
      "building": "",
      "web_service_access_only": "false",
      "notification": "2",
      "sys_updated_by": "system",
      "enable_multifactor_authn": "false",
      "sys_created_on": "2018-03-04 20:26:32",
      "sys_domain": "global",
      "agent_status": "",
      "state": "",
      "vip": "false",
      "sys_created_by": "admin",
      "longitude": "",
      "zip": "",
      "home_phone": "",
      "time_format": "",
      "last_login": "",
      "default_perspective": "",
      "geolocation_tracked": "false",
      "active": "true",
      "time_sheet_policy": "",
      "sys_domain_path": "/",
      "phone": "+1 858 287 7834",
      "cost_center": "",
      "name": "George Warren",
      "employee_number": "",
      "gender": "",
      "city": "",
      "user_name": "george.warren",
      "failed_attempts": "",
      "edu_status": "",
      "latitude": "",
      "roles": "",
      "title": "Network Administrator",
      "sys_class_name": "customer_contact",
      "sys_id": "ddce70866f9331003b3c498f5d3ee417",
      "internal_integration_user": "false",
      "ldap_server": "",
      "mobile_phone": "+1 858 867 7857",
      "street": "",
      "company": "86837a386f0331003b3c498f5d3ee4ca",
      "department": "",
      "first_name": "George",
      "preferred_language": "",
      "introduction": "",
      "email": "geo.warren@mailinator.com",
      "manager": "",
      "locked_out": "false",
      "sys_mod_count": "3",
      "last_name": "Warren",
      "photo": "",
      "sys_tags": "",
      "middle_name": "",
      "time_zone": "",
      "schedule": "",
      "on_schedule": "",
      "date_format": "",
      "location": "25ab8e460a0a0bb300857304ff811af5",
      "account": "86837a386f0331003b3c498f5d3ee4ca"
    },
    {
      "country": "",
      "calendar_integration": "1",
      "last_position_update": "",
      "last_login_time": "2019-01-03 15:08:57",
      "last_login_device": "73.71.157.241",
      "source": "",
      "sys_updated_on": "2019-01-03 23:26:12",
      "building": "",
      "web_service_access_only": "false",
      "notification": "2",
      "sys_updated_by": "admin",
      "enable_multifactor_authn": "false",
      "sys_created_on": "2019-01-03 15:07:25",
      "sys_domain": "global",
      "agent_status": "",
      "state": "",
      "vip": "false",
      "sys_created_by": "carl.customer",
      "longitude": "",
      "zip": "",
      "home_phone": "",
      "time_format": "",
      "last_login": "",
      "default_perspective": "",
      "geolocation_tracked": "false",
      "active": "true",
      "time_sheet_policy": "",
      "sys_domain_path": "/",
      "phone": "+16692627777",
      "cost_center": "",
      "name": "Jane Contact",
      "employee_number": "",
      "gender": "",
      "city": "",
      "user_name": "Jane.Contact",
      "failed_attempts": "",
      "edu_status": "faculty",
      "latitude": "",
      "roles": "",
      "title": "",
      "sys_class_name": "customer_contact",
      "sys_id": "0a232a0013691200042ab3173244b075",
      "internal_integration_user": "false",
      "ldap_server": "",
      "mobile_phone": "",
      "street": "",
      "company": "86837a386f0331003b3c498f5d3ee4ca",
      "department": "",
      "first_name": "Jane",
      "preferred_language": "",
      "introduction": "",
      "email": "jane.contact@mailinator.com",
      "manager": "",
      "locked_out": "false",
      "sys_mod_count": "3",
      "last_name": "Contact",
      "photo": "",
      "sys_tags": "",
      "middle_name": "",
      "time_zone": "",
      "schedule": "",
      "on_schedule": "",
      "date_format": "",
      "location": "",
      "account": "86837a386f0331003b3c498f5d3ee4ca"
    }
  ]
}
```

## Contact - GET /now/contact/\{id\}

Retrieves the specified Customer Service Management \(CSM\) contact.

### URL format

Versioned URL: `/api/now/{api_version}/contact/{id}`

Default URL: `/api/now/contact/{id}`

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

Sys\_id of the contact to retrieve.Data type: String

Table: Contact \[customer\_contact\]

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
-   User doesn't have access to the case.

</td></tr><tr><td>

500

</td><td id="entry-500-status-code">

Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.

</td></tr></tbody>
</table>### Response body parameters \(JSON or XML\)

The endpoint may return the following JSON or XML elements in the response body. In addition to the list of elements defined below \(which define the elements in a base system\), the endpoint also returns any custom fields added to the Contact \[customer\_contact\] table. For additional information on these elements, refer to your specific table definition \[**System Definition** &gt; **Tables**\].

<table><thead><tr><th>

Element

</th><th>

Description

</th></tr></thead><tbody><tr><td>

account

</td><td id="contacttable-account-enrty">

Sys\_id of the account record to which the contact is associated.Data type: String

Table: Account \[customer\_account\]

</td></tr><tr><td>

active

</td><td id="contacttable-active-entry">

Flag that indicates whether the contact is active within the system.Possible values:

-   true: Contact is active
-   false: Contact is inactive

Data type: Boolean

Default: true

</td></tr><tr><td>

agent\_status

</td><td id="contacttable-agent_status-entry">

Status of the agent.Possible values:

-   Off work
-   On break
-   On route
-   On site

Data type: String

Maximum length: 40

</td></tr><tr><td>

building

</td><td id="contacttable-building-entry">

Sys\_id of the record that describes the building in which the contact resides.Data type: String

Table: Building \[cmn\_building\]

</td></tr><tr><td>

calendar\_integration

</td><td id="contacttable-calendar_integration-entry">

Calendar application that the contact uses.1: Outlook

Data type: Number \(Integer\)

Default: 1

</td></tr><tr><td>

city

</td><td id="contacttable-city-entry">

City in which the contact resides.Data type: String

Maximum length: 40

</td></tr><tr><td>

company

</td><td id="contacttable-company-entry">

Sys\_id of the company record to which the contact is associated.Data type: String

Table: Company \[core\_company\]

</td></tr><tr><td>

cost\_center

</td><td id="contacttable-cost_center-entry">

Sys\_id of the cost center associated with the contact.Data type: String

Table: Cost Center \[cmn\_cost\_center\]

</td></tr><tr><td>

country

</td><td id="contacttable-country-entry">

Country code of the country in which the contact resides.Data type: String

Maximum length: 3

</td></tr><tr><td>

date\_format

</td><td id="contacttable-date_format-entry">

Format in which to display dates to contacts.Valid values:

-   dd/mm/yyyy
-   dd-mm-yyyy
-   dd.mm.yyyy
-   mm-dd-yyyy
-   yyyy-mm-dd

Data type: String

Maximum length: 40

Default: blank \(system date format\)

</td></tr><tr><td>

default\_perspective

</td><td id="contacttable-default_perspective-entry">

Sys\_id of the default perspective for the contact.Data type: String

Table: Menu List \[sys\_perspective\]

</td></tr><tr><td>

department

</td><td id="contacttable-department-entry">

Sys\_id of the department associated with the contact.Data type: String

Table: Department \[cmn\_department\]

</td></tr><tr><td>

edu\_status

</td><td id="contacttable-edu_status-entry">

Education status of the associated contact.Data type: String

Maximum length: 40

Default: faculty

</td></tr><tr><td>

email

</td><td id="contacttable-email-entry">

Contact email address.Data type: String

</td></tr><tr><td>

employee\_number

</td><td id="contacttable-employee_number-entry">

Contact employee number.Data type: String

</td></tr><tr><td>

enable\_multifactor\_authn

</td><td id="contacttable-enable_multifactor_authn-entry">

Flag that indicates whether multifactor authorization is required for the contact to log in to the service portal.Possible values:

-   true: Multifactor authorization enabled
-   false: Multifactor authorization disabled

Data type: Boolean

Default: false

</td></tr><tr><td>

failed\_attempts

</td><td id="contacttable-failed_attempts-entry">

Number of failed log in attempts.Data type: Number \(Integer\)

</td></tr><tr><td>

first\_name

</td><td id="contacttable-first_name-entry">

Contact first name.Data type: String

Maximum length: 50

</td></tr><tr><td>

gender

</td><td id="contacttable-gender-entry">

Contact gender.Data type: String

Maximum length: 40

</td></tr><tr><td>

geolocation\_tracked

</td><td id="contacttable-geolocation_tracked-entry">

Flag that indicates whether the contact location is obtained through geotracking.Possible values:

-   true: Contact location obtained through geotracking
-   false: Contact location not obtained through geotracking

Data type: Boolean

Default value: false

</td></tr><tr><td>

home\_phone

</td><td id="contacttable-home_phone-entry">

Contact home phone number.Data type: String

Maximum length: 40

</td></tr><tr><td>

internal\_integration\_user

</td><td id="contacttable-internal_integration_user-entry">

Flag that indicates whether the contact is an internal integration user.Possible values:

-   true: Internal integration user
-   false: Other type of user

Data type: Boolean

Default: false

</td></tr><tr><td>

introduction

</td><td id="contacttable-introduction-entry">

IntroductionData type: String

Maximum length: 40

</td></tr><tr><td>

last\_login

</td><td id="contacttable-last_login-entry">

Date on which the contact last logged into the system.Data type: String \(Date\)

</td></tr><tr><td>

last\_login\_device

</td><td id="contacttable-last_login_device-entry">

Device the consumer used the last time they logged in to the system.Data type: String

Maximum length: 40

</td></tr><tr><td>

last\_login\_time

</td><td id="contacttable-last_login_time-entry">

Date and time the contact logged in to the system.Data type: String \(Date/time\)

</td></tr><tr><td>

last\_name

</td><td id="contacttable-last_name-entry">

Contact last name.Data type: String

Maximum length: 50

</td></tr><tr><td>

last\_position\_update

</td><td id="contacttable-last_position_update-entry">

Date and time the last position was updated.Data type: String \(Date/time\)

</td></tr><tr><td>

latitude

</td><td id="contacttable-latitude-entry">

Latitude coordinate of the contact.Data type: Number \(Floating point\)

Maximum length: 40

</td></tr><tr><td>

ldap\_server

</td><td id="contacttable-ldap_server-entry">

Sys\_id of the LDAP server used by the contact to last log in to the system. Data type: String

Table: LDAP Server \[ldap\_server\_config\]

</td></tr><tr><td>

location

</td><td id="contacttable-location-entry">

Sys\_id of the record that describes the location of the contactData type: String

Table: Location \[cmn\_location\]

</td></tr><tr><td>

locked\_out

</td><td id="contacttable-locked_out-entry">

Flag that indicates if the contact is locked-out.Possible values:

-   true: Contact locked-out
-   false: Contact not locked-out

Data type: Boolean

Default: false

</td></tr><tr><td>

longitude

</td><td id="contacttable-longitude-entry">

Longitude coordinate of the contact.Data type: Number \(Floating point\)

Maximum length: 40

</td></tr><tr><td>

manager

</td><td id="contacttable-manager-entry">

Sys\_id of the record that describes the direct supervisor of the contact.Data type: String

Table: User \[sys\_user\]

</td></tr><tr><td>

middle\_name

</td><td id="contacttable-middle_name-entry">

Contact middle name.Data type: Number \(Floating point\)

Maximum length: 50

</td></tr><tr><td>

mobile\_phone

</td><td id="contacttable-mobile_phone-entry">

Contact mobile phone number.Data type: String

 Maximum length: 40

</td></tr><tr><td>

name

</td><td id="contacttable-name-entry">

Contact full name.Data type: String

Maximum length: 151

</td></tr><tr><td>

notification

</td><td id="contacttable-notification-entry">

Indicates whether the contact should receive notifications.Valid values:

-   1: Disabled
-   2: Enabled

Data type: Number \(Integer\)

Default: 2

</td></tr><tr><td>

on\_schedule

</td><td id="contacttable-on_schedule-entry">

Indicates the timeliness of dispatched service personnel.Valid values:

-   Ahead: Ahead of schedule.
-   behind\_less30: Behind schedule, but less than 30 minutes.
-   behind\_30to60: Behind schedule between 30 and 60 minutes.
-   behind\_more60: Behind schedule more than 60 minutes.
-   on\_time: On schedule.

Data type: String

Maximum length: 40

</td></tr><tr><td>

phone

</td><td id="contacttable-phone-entry">

Contact business phone number.Data type: String

Maximum length: 40

</td></tr><tr><td>

photo

</td><td id="contacttable-photo-entry">

Photo image of the contact. Data type: String

</td></tr><tr><td>

preferred\_language

</td><td id="contacttable-preferred_language-entry">

Country code of the contact primary language.Data type: String

Maximum length: 3

</td></tr><tr><td>

roles

</td><td id="contacttable-roles-entry">

List of user roles associated with the contact.Data type: String

Maximum length: 40

</td></tr><tr><td>

schedule

</td><td id="contacttable-schedule-entry">

Sys\_id of the record that describes the work schedule for the associated contact.Data type: String

Table: Schedule \[cmn\_schedule\]

</td></tr><tr><td>

source

</td><td id="contacttable-source-entry">

Source of the contact.Data type: String

Maximum length: 255

</td></tr><tr><td>

state

</td><td id="contacttable-state-entry">

State in which the contact resides.Data type: String

Maximum length: 40

</td></tr><tr><td>

street

</td><td id="contacttable-street-entry">

Contact street address.Data type: String

Maximum length: 255

</td></tr><tr><td>

sys\_class\_name

</td><td id="contacttable-sys_class_name-entry">

Table that contains the contact record. Data type: String

Maximum length: 80

</td></tr><tr><td>

sys\_created\_by

</td><td id="contacttable-sys_created_by-entry">

User that originally created the associated contact record.Data type: String

Maximum length: 40

</td></tr><tr><td>

sys\_created\_on

</td><td id="contacttable-sys_created_on-entry">

Data and time the associated contact was originally created.Data type: String \(Date/time\)

</td></tr><tr><td>

sys\_domain

</td><td id="contacttable-sys_domain-entry">

ServiceNow instance domain of the associated contact record.Data type: String

</td></tr><tr><td>

sys\_domain\_path

</td><td id="contacttable-sys_domain_path-entry">

Contact record domain path.Data type: String

Maximum length: 255

Default: / \(global\)

</td></tr><tr><td>

sys\_id

</td><td id="contacttable-sys_id-entry">

Unique identifier for the associated contact record.Data type: String

</td></tr><tr><td>

sys\_mod\_count

</td><td id="contacttable-sys_mod_count-entry">

Number of times that the associated contact record has been modified.Data type: Number \(Integer\)

</td></tr><tr><td>

sys\_updated\_by

</td><td id="contacttable-sys_updated_by-entry">

User that last updated the associated contact information.Data type: String

Maximum length: 40

</td></tr><tr><td>

sys\_updated\_on

</td><td id="contacttable-sys_updated_on-entry">

Data and time the associated contact information was updated.Data type: String \(Date/time\)

</td></tr><tr><td>

time\_format

</td><td id="contacttable-time_format-entry">

Format in which to display time.Valid values:

-   hh.mm.ss a: hh.mm.ss \(12 hour\)
-   hh:mm:ss a: hh:mm:ss \(12 hour\)
-   HH.mm.ss: hh.mm.ss \(24 hour\)
-   HH:mm:ss: hh:mm:ss \(24 hour\)

Data type: String

Maximum length: 40

Default: Blank \(system time format\)

</td></tr><tr><td>

time\_sheet\_policy

</td><td id="contacttable-time_sheet_policy-entry">

Sys\_id of the record that contains the time sheet policy for the associated contact.Data type: String

Table: Time Sheet Policy \[time\_sheet\_policy\]

</td></tr><tr><td>

time\_zone

</td><td id="contacttable-time_zone-entry">

Time zone in which the contact resides, such as Canada/Central or US/Eastern.Data type: String

Maximum length: 40

</td></tr><tr><td>

title

</td><td id="contacttable-title-entry">

Contact business title such as Manager, Software Developer, or Contractor.Data type: String

Maximum length: 60

</td></tr><tr><td>

user\_name

</td><td id="contacttable-user_name-entry">

Contact user ID.Data type: String

Maximum length: 40

</td></tr><tr><td>

vip

</td><td id="contacttable-vip-entry">

Flag that indicates whether the associated contact has VIP status.Possible values:

-   true: VIP
-   false: Not VIP

Data type: Boolean

Default: false

</td></tr><tr><td>

web\_service\_access\_only

</td><td id="contacttable-web_service_access_only-entry">

Flag that indicates whether the contact can only access services through the web.Possible values:

-   true: Web access only
-   false: Access through all available methods

Data type: Boolean

Default: false

</td></tr><tr><td>

zip

</td><td id="contacttable-zip-entry">

Contact zip code.Data type: String

Maximum length: 40

</td></tr></tbody>
</table>### cURL request

```
curl "https://instance.servicenow.com/api/now/contact/ddce70866f9331003b3c498f5d3ee417 \
--request GET \
--header "Accept:application/json" \
--user "username":"password"

```

```
{
  "result": {
    "country": "",
    "calendar_integration": "1",
    "last_position_update": "",
    "last_login_time": "2018-03-10 21:48:11",
    "last_login_device": "",
    "source": "",
    "sys_updated_on": "2019-01-03 05:49:34",
    "building": "",
    "web_service_access_only": "false",
    "notification": "2",
    "sys_updated_by": "system",
    "enable_multifactor_authn": "false",
    "sys_created_on": "2018-03-04 20:26:32",
    "sys_domain": "global",
    "agent_status": "",
    "state": "",
    "vip": "false",
    "sys_created_by": "admin",
    "longitude": "",
    "zip": "",
    "home_phone": "",
    "time_format": "",
    "last_login": "",
    "default_perspective": "",
    "geolocation_tracked": "false",
    "active": "true",
    "time_sheet_policy": "",
    "sys_domain_path": "/",
    "phone": "+1 858 287 7834",
    "cost_center": "",
    "name": "George Warren",
    "employee_number": "",
    "gender": "",
    "city": "",
    "user_name": "george.warren",
    "failed_attempts": "",
    "edu_status": "",
    "latitude": "",
    "roles": "",
    "title": "Network Administrator",
    "sys_class_name": "customer_contact",
    "sys_id": "ddce70866f9331003b3c498f5d3ee417",
    "internal_integration_user": "false",
    "ldap_server": "",
    "mobile_phone": "+1 858 867 7857",
    "street": "",
    "company": "86837a386f0331003b3c498f5d3ee4ca",
    "department": "",
    "first_name": "George",
    "preferred_language": "",
    "introduction": "",
    "email": "geo.warren@mailinator.com",
    "manager": "",
    "locked_out": "false",
    "sys_mod_count": "3",
    "last_name": "Warren",
    "photo": "",
    "sys_tags": "",
    "middle_name": "",
    "time_zone": "",
    "schedule": "",
    "on_schedule": "",
    "date_format": "",
    "location": "25ab8e460a0a0bb300857304ff811af5",
    "account": "86837a386f0331003b3c498f5d3ee4ca"
  }
}

```

## Contact - POST /now/contact

Creates a new Customer Service Management \(CSM\) contact.

In addition, you can create a social media profile for the contact using this endpoint. To create the profile, you must specify the following parameters in the request body:

-   **social\_channel**
-   **social\_handle**
-   **social\_handle\_url**

**Warning:** This endpoint does not perform parameter validation as doing so can create excessive overhead. If a request parameter is misspelled, is not valid, or is not supported by the endpoint, it is ignored without warning.

### URL format

Versioned URL: `/api/now/{api_version}/contact`

Default URL: `/api/now/contact`

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

account

</td><td id="contacttable-account-enrty">

Sys\_id of the account record to which the contact is associated.Data type: String

Table: Account \[customer\_account\]

</td></tr><tr><td>

active

</td><td id="contacttable-active-entry">

Flag that indicates whether the contact is active within the system.Possible values:

-   true: Contact is active
-   false: Contact is inactive

Data type: Boolean

Default: true

</td></tr><tr><td>

agent\_status

</td><td id="contacttable-agent_status-entry">

Status of the agent.Possible values:

-   Off work
-   On break
-   On route
-   On site

Data type: String

Maximum length: 40

</td></tr><tr><td>

building

</td><td id="contacttable-building-entry">

Sys\_id of the record that describes the building in which the contact resides.Data type: String

Table: Building \[cmn\_building\]

</td></tr><tr><td>

calendar\_integration

</td><td id="contacttable-calendar_integration-entry">

Calendar application that the contact uses.1: Outlook

Data type: Number \(Integer\)

Default: 1

</td></tr><tr><td>

city

</td><td id="contacttable-city-entry">

City in which the contact resides.Data type: String

Maximum length: 40

</td></tr><tr><td>

company

</td><td id="contacttable-company-entry">

Sys\_id of the company record to which the contact is associated.Data type: String

Table: Company \[core\_company\]

</td></tr><tr><td>

cost\_center

</td><td id="contacttable-cost_center-entry">

Sys\_id of the cost center associated with the contact.Data type: String

Table: Cost Center \[cmn\_cost\_center\]

</td></tr><tr><td>

country

</td><td id="contacttable-country-entry">

Country code of the country in which the contact resides.Data type: String

Maximum length: 3

</td></tr><tr><td>

date\_format

</td><td id="contacttable-date_format-entry">

Format in which to display dates to contacts.Valid values:

-   dd/mm/yyyy
-   dd-mm-yyyy
-   dd.mm.yyyy
-   mm-dd-yyyy
-   yyyy-mm-dd

Data type: String

Maximum length: 40

Default: blank \(system date format\)

</td></tr><tr><td>

default\_perspective

</td><td id="contacttable-default_perspective-entry">

Sys\_id of the default perspective for the contact.Data type: String

Table: Menu List \[sys\_perspective\]

</td></tr><tr><td>

department

</td><td id="contacttable-department-entry">

Sys\_id of the department associated with the contact.Data type: String

Table: Department \[cmn\_department\]

</td></tr><tr><td>

edu\_status

</td><td id="contacttable-edu_status-entry">

Education status of the associated contact.Data type: String

Maximum length: 40

Default: faculty

</td></tr><tr><td>

email

</td><td id="contacttable-email-entry">

Contact email address.Data type: String

</td></tr><tr><td>

employee\_number

</td><td id="contacttable-employee_number-entry">

Contact employee number.Data type: String

</td></tr><tr><td>

enable\_multifactor\_authn

</td><td id="contacttable-enable_multifactor_authn-entry">

Flag that indicates whether multifactor authorization is required for the contact to log in to the service portal.Possible values:

-   true: Multifactor authorization enabled
-   false: Multifactor authorization disabled

Data type: Boolean

Default: false

</td></tr><tr><td>

failed\_attempts

</td><td id="contacttable-failed_attempts-entry">

Number of failed log in attempts.Data type: Number \(Integer\)

</td></tr><tr><td>

first\_name

</td><td id="contacttable-first_name-entry">

Contact first name.Data type: String

Maximum length: 50

</td></tr><tr><td>

gender

</td><td id="contacttable-gender-entry">

Contact gender.Data type: String

Maximum length: 40

</td></tr><tr><td>

geolocation\_tracked

</td><td id="contacttable-geolocation_tracked-entry">

Flag that indicates whether the contact location is obtained through geotracking.Possible values:

-   true: Contact location obtained through geotracking
-   false: Contact location not obtained through geotracking

Data type: Boolean

Default value: false

</td></tr><tr><td>

home\_phone

</td><td id="contacttable-home_phone-entry">

Contact home phone number.Data type: String

Maximum length: 40

</td></tr><tr><td>

internal\_integration\_user

</td><td id="contacttable-internal_integration_user-entry">

Flag that indicates whether the contact is an internal integration user.Possible values:

-   true: Internal integration user
-   false: Other type of user

Data type: Boolean

Default: false

</td></tr><tr><td>

introduction

</td><td id="contacttable-introduction-entry">

IntroductionData type: String

Maximum length: 40

</td></tr><tr><td>

last\_login\_device

</td><td id="contacttable-last_login_device-entry">

Device the consumer used the last time they logged in to the system.Data type: String

Maximum length: 40

</td></tr><tr><td>

last\_login\_time

</td><td id="contacttable-last_login_time-entry">

Date and time the contact logged in to the system.Data type: String \(Date/time\)

</td></tr><tr><td>

last\_name

</td><td id="contacttable-last_name-entry">

Contact last name.Data type: String

Maximum length: 50

</td></tr><tr><td>

latitude

</td><td id="contacttable-latitude-entry">

Latitude coordinate of the contact.Data type: Number \(Floating point\)

Maximum length: 40

</td></tr><tr><td>

ldap\_server

</td><td id="contacttable-ldap_server-entry">

Sys\_id of the LDAP server used by the contact to last log in to the system. Data type: String

Table: LDAP Server \[ldap\_server\_config\]

</td></tr><tr><td>

location

</td><td id="contacttable-location-entry">

Sys\_id of the record that describes the location of the contactData type: String

Table: Location \[cmn\_location\]

</td></tr><tr><td>

locked\_out

</td><td id="contacttable-locked_out-entry">

Flag that indicates if the contact is locked-out.Possible values:

-   true: Contact locked-out
-   false: Contact not locked-out

Data type: Boolean

Default: false

</td></tr><tr><td>

longitude

</td><td id="contacttable-longitude-entry">

Longitude coordinate of the contact.Data type: Number \(Floating point\)

Maximum length: 40

</td></tr><tr><td>

manager

</td><td id="contacttable-manager-entry">

Sys\_id of the record that describes the direct supervisor of the contact.Data type: String

Table: User \[sys\_user\]

</td></tr><tr><td>

middle\_name

</td><td id="contacttable-middle_name-entry">

Contact middle name.Data type: Number \(Floating point\)

Maximum length: 50

</td></tr><tr><td>

mobile\_phone

</td><td id="contacttable-mobile_phone-entry">

Contact mobile phone number.Data type: String

 Maximum length: 40

</td></tr><tr><td>

name

</td><td id="contacttable-name-entry">

Contact full name.Data type: String

Maximum length: 151

</td></tr><tr><td>

notification

</td><td id="contacttable-notification-entry">

Indicates whether the contact should receive notifications.Valid values:

-   1: Disabled
-   2: Enabled

Data type: Number \(Integer\)

Default: 2

</td></tr><tr><td>

on\_schedule

</td><td id="contacttable-on_schedule-entry">

Indicates the timeliness of dispatched service personnel.Valid values:

-   Ahead: Ahead of schedule.
-   behind\_less30: Behind schedule, but less than 30 minutes.
-   behind\_30to60: Behind schedule between 30 and 60 minutes.
-   behind\_more60: Behind schedule more than 60 minutes.
-   on\_time: On schedule.

Data type: String

Maximum length: 40

</td></tr><tr><td>

phone

</td><td id="contacttable-phone-entry">

Contact business phone number.Data type: String

Maximum length: 40

</td></tr><tr><td>

photo

</td><td id="contacttable-photo-entry">

Photo image of the contact. Data type: String

</td></tr><tr><td>

preferred\_language

</td><td id="contacttable-preferred_language-entry">

Country code of the contact primary language.Data type: String

Maximum length: 3

</td></tr><tr><td>

roles

</td><td id="contacttable-roles-entry">

List of user roles associated with the contact.Data type: String

Maximum length: 40

</td></tr><tr><td>

schedule

</td><td id="contacttable-schedule-entry">

Sys\_id of the record that describes the work schedule for the associated contact.Data type: String

Table: Schedule \[cmn\_schedule\]

</td></tr><tr><td>

social\_channel

</td><td>

Social media channel to which the contact is associated such as Twitter, Facebook, or Instagram.Data type: String

</td></tr><tr><td>

social\_handle

</td><td>

User handle on the social media channel.Data type: String

</td></tr><tr><td>

social\_handle\_url

</td><td>

URL to the contact's social channel profile.Data type: String

</td></tr><tr><td>

source

</td><td id="contacttable-source-entry">

Source of the contact.Data type: String

Maximum length: 255

</td></tr><tr><td>

state

</td><td id="contacttable-state-entry">

State in which the contact resides.Data type: String

Maximum length: 40

</td></tr><tr><td>

street

</td><td id="contacttable-street-entry">

Contact street address.Data type: String

Maximum length: 255

</td></tr><tr><td>

time\_format

</td><td id="contacttable-time_format-entry">

Format in which to display time.Valid values:

-   hh.mm.ss a: hh.mm.ss \(12 hour\)
-   hh:mm:ss a: hh:mm:ss \(12 hour\)
-   HH.mm.ss: hh.mm.ss \(24 hour\)
-   HH:mm:ss: hh:mm:ss \(24 hour\)

Data type: String

Maximum length: 40

Default: Blank \(system time format\)

</td></tr><tr><td>

time\_sheet\_policy

</td><td id="contacttable-time_sheet_policy-entry">

Sys\_id of the record that contains the time sheet policy for the associated contact.Data type: String

Table: Time Sheet Policy \[time\_sheet\_policy\]

</td></tr><tr><td>

time\_zone

</td><td id="contacttable-time_zone-entry">

Time zone in which the contact resides, such as Canada/Central or US/Eastern.Data type: String

Maximum length: 40

</td></tr><tr><td>

title

</td><td id="contacttable-title-entry">

Contact business title such as Manager, Software Developer, or Contractor.Data type: String

Maximum length: 60

</td></tr><tr><td>

user\_name

</td><td id="contacttable-user_name-entry">

Contact user ID.Data type: String

Maximum length: 40

</td></tr><tr><td>

vip

</td><td id="contacttable-vip-entry">

Flag that indicates whether the associated contact has VIP status.Possible values:

-   true: VIP
-   false: Not VIP

Data type: Boolean

Default: false

</td></tr><tr><td>

web\_service\_access\_only

</td><td id="contacttable-web_service_access_only-entry">

Flag that indicates whether the contact can only access services through the web.Possible values:

-   true: Web access only
-   false: Access through all available methods

Data type: Boolean

Default: false

</td></tr><tr><td>

zip

</td><td id="contacttable-zip-entry">

Contact zip code.Data type: String

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
|201|New contact record was successfully created.|
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

Sys\_id of the newly created contact record.Data type: String

</td></tr></tbody>
</table>### cURL request

```
curl -X POST "https://instance.servicenow.com/api/now/contact" \
-H 'Accept: application/json' \
-H 'Content-Type: application/json' \
-d '{ \
  "country": "USA", \
  "calendar_integration": "1", \
  "last_login_time": "2018-03-10 21:48:11", \
  "last_login_device": "tablet", \
  "building": "Cardinal West", \
  "web_service_access_only": "false", \
  "notification": "1", \
  "enable_multifactor_authn": "true", \
  "agent_status": "Travelling", \
  "state": "CA", \
  "vip": "false", \
  "longitude": "123.76", \
  "zip": "92069", \
  "home_phone": "(555)555-1234", \
  "time_format": "hh:mm:ss", \
  "geolocation_tracked": "false", \
  "active": "true", \
  "phone": "+1 858 287 7834", \
  "cost_center": "1345", \
  "name": "Dora Warren", \
  "employee_number": "546", \
  "gender": "Female", \
  "city": "Orlando", \
  "user_name": "dora.warren", \
  "failed_attempts": "2", \
  "edu_status": "current", \
  "latitude": "57.6", \
  "title": "Network Administrator", \
  "internal_integration_user": "false", \
  "ldap_server": "10.24.23.123", \
  "mobile_phone": "+1 858 867 7857", \
  "street": "123 Lagume", \
  "company": "86837a386f0331003b3c498f5d3ee4ca", \
  "department": "IT", \
  "first_name": "Dora", \
  "preferred_language": "Spanish", \
  "email": "dora.warren@mailinator.com", \
  "manager": "ddce70866f9331003b3c498f5d3ee417", \
  "locked_out": "false", \
  "last_name": "Warren", \
  "middle_name": "Dell", \
  "time_zone": "PST", \
  "schedule": "9-5", \
  "date_format": "MM/DD/YY", \
  "location": "25ab8e460a0a0bb300857304ff811af5", \
  "account": "86837a386f0331003b3c498f5d3ee4ca" \
}'
--user 'username':'password'
```

```
"result": "62fe1c97db76c3006b7a9646db961999"
```

