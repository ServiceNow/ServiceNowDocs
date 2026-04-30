---
title: Case API
description: The Case API provides endpoints that enable you to retrieve and update Customer Service Management \(CSM\) case records.Retrieves the activity stream for a specified Customer Service Management \(CSM\) case.Retrieves the list of possible field values for a choice or reference field in the Case \[sn\_customerservice\_case\] table.Retrieves the list of possible field values for a choice or reference field for a specified record in the Case \[sn\_customerservice\_case\] table.Retrieves the specified Customer Service Management \(CSM\) case.Retrieves a specified set of Customer Service Management \(CSM\) cases.Creates a new Customer Service Management \(CSM\) case.Updates the specified existing Customer Service Management \(CSM\) case with the passed-in parameters.
locale: en-US
release: yokohama
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 163
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# Case API

The Case API provides endpoints that enable you to retrieve and update Customer Service Management \(CSM\) case records.

In addition, you can generate new social media profile records when creating a case.

The Case API requires the Customer Service plugin \(com.sn\_customerservice\) and is provided within the sn\_customerservice namespace.

Users must have the csm\_ws\_integration role for full API access. External users with the sn\_customerservice.customer or sn\_customerservice.consumer roles can also access the endpoints.

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## Case - GET /sn\_customerservice/case/\{id\}/activities

Retrieves the activity stream for a specified Customer Service Management \(CSM\) case.

Use this endpoint to retrieve all entries from the activity stream for a specified record from the Case \[sn\_customerservice\_case\] table.

To use this endpoint, users must have the csm\_ws\_integration, sn\_customerservice.customer, or sn\_customerservice.consumer role.

**Note:** You can reference all sysparm query parameters using either their full name or their shortened name \(without the **sysparm\_** prefix\). For example, for **sysparm\_limit** you can also use **limit**.

### URL format

Versioned URL: `/api/sn_customerservice/{api_version}/case/{id}/activities`

Default URL: `/api/sn_customerservice/case/{id}/activities`

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

Sys\_id or case number of the case to retrieve. Results will be unpredictable if a specified case number is shared by two or more cases.Data type: String

Table: Case \[sn\_customerservice\_case\]

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sysparm\_activity\_type

</td><td id="sysparm_activity_type-entry-case">

Filters the type of activities to return from the activity stream. The **entries.element** parameter contains the activity type for each activity. For example:

-   `sysparm_activity_type=attachment`
-   `sysparm_activity_type=work_notes`
-   `sysparm_activity_type=attachment,work_notes`
-   `sysparm_ activity_type=attachment,work_notes,comments`

Data type: String

Default: Returns all types of activity.

</td></tr><tr><td>

sysparm\_limit

</td><td>

Maximum number of records to return. Unusually large **sysparm\_limit** values can impact system performance. For requests that exceed this number of records, use the **sysparm\_offset** parameter to paginate record retrieval. Data type: Number

</td></tr><tr><td>

sysparm\_offset

</td><td>

Starting record index for which to begin retrieving records. Use this value to paginate record retrieval. This functionality enables the retrieval of all records, regardless of the number of records, in small manageable chunks. For example, the first time you call this endpoint, **sysparm\_offset** is set to "0". To simply page through all available records, use `sysparm_offset=sysparm_offset+sysparm_limit`, until you reach the end of all records.

Do not pass a negative number in the **sysparm\_offset** parameter.Data type: Number

Default: 0

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
</table><table class="rest_api_response_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Link

</td><td>

REST response data can be split into multiple result sets. Where applicable, the response header contains different links for the first set, previous set, next set, and the last set of records.For example:

`https://<instance name>.service-now.com/api/now/table/cmdb_ci?sysparm_offset=40&sysparm_limit=1000>;rel="next"`,

`https://<instance name>.service-now.com/api/now/table/cmdb_ci?sysparm_offset=40&sysparm_limit=1000>;rel="prev"`,

`https://<instance name>.service-now.com/api/now/table/cmdb_ci?sysparm_offset=0&sysparm_limit=1000>;rel="first"`,

`https://<instance name>.service-now.com/api/now/table/cmdb_ci?sysparm_offset=2780&sysparm_limit=1000>;rel="last"`

</td></tr><tr><td id="x-total-count-response-entry-RESTAPI">

X-Total-Count

</td><td>

Response header showing the total number of records matching the request when the **sysparm\_limit** or **sysparm\_offset** query parameters are specified.

</td></tr></tbody>
</table>### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|404|Not found. The requested item wasn't found.|
|500|Internal Server Error. A logic error on the server-side code occurred.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

display\_value

</td><td>

Case number for the CSM case.Data type: String

</td></tr><tr><td>

entries

</td><td>

List that represents activity stream entries from the CSM case.Data type: Array of Objects

```
"entries": [
  {
    "attachment": {Object},
    "contains_code": Boolean,
    "element": "String",
    "field_label": "String",
    "initials": "String",
    "login_name": "String",
    "name": "String",
    "sys_created_on": "String",
    "sys_created_on_adjusted": "String",
    "sys_id": "String",
    "user_sys_id": "String",
    "value": "String"
  }
]
```

</td></tr><tr><td>

entries.attachment

</td><td>

Description of a file attached to the CSM case in the activity stream entry.Data type: Object

```
"attachment": {
  "average_image_color": "String",
  "content_type": "String",
  "file_name": "String",
  "image_height": Number,
  "image_path": "String",
  "image_width": Number,
  "path": "String",
  "size": "String",
  "size_bytes": Number,
  "state": "String",
  "sys_id": "String",
  "thumbnail_path": "String"
}
```

</td></tr><tr><td>

entries.attachment.average\_image\_color

</td><td>

Hexadecimal representation of average color for image attachment.Data type: String

</td></tr><tr><td>

entries.attachment.content\_type

</td><td>

MIME type for the attachment.Examples include:

-   application/pdf
-   image/jpeg
-   message/rfc822

Data type: String

</td></tr><tr><td>

entries.attachment.file\_name

</td><td>

File name for the attachment.Data type: String

</td></tr><tr><td>

entries.attachment.image\_height

</td><td>

Height of image attachment in pixels.Data type: Number

</td></tr><tr><td>

entries.attachment.image\_path

</td><td>

Direct download link for image attachment.Data type: String

</td></tr><tr><td>

entries.attachment.image\_width

</td><td>

Width of image attachment in pixels.Data type: Number

</td></tr><tr><td>

entries.attachment.path

</td><td>

Direct link to the attachment.Data type: String

</td></tr><tr><td>

entries.attachment.size

</td><td>

Size of the attachment.Examples:

-   157.7 KB
-   2.2 MB

Data type: String

</td></tr><tr><td>

entries.attachment.size\_bytes

</td><td>

Size of the attachment.Data type: Number

Unit: Bytes

</td></tr><tr><td>

entries.attachment.state

</td><td>

State of the attachment record.Possible values:

-   Available
-   Available Conditionally
-   Not available
-   Pending

Data type: String

Table: Attachment \[sys\_attachment\]

</td></tr><tr><td>

entries.attachment.sys\_id

</td><td>

Sys\_id for the attachment.Data type: String

Table: Attachment \[sys\_attachment\]

</td></tr><tr><td>

entries.attachment.thumbnail\_path

</td><td>

Direct download link for thumbnail of image attachment.Data type: String

</td></tr><tr><td>

entries.contains\_code

</td><td>

Flag that indicates whether the activity stream entry contains code or not.Possible values:

-   true: The activity stream entry contains code.
-   false: The activity stream entry doesn't contain code.

Data type: Boolean

</td></tr><tr><td>

entries.element

</td><td>

Name for the journal field associated with the activity stream entry.Data type: String

Table: Dictionary Entries \[sys\_dictionary\]

</td></tr><tr><td>

entries.field\_label

</td><td>

Display name for the journal field associated with the activity stream entry.Data type: String

</td></tr><tr><td>

entries.initials

</td><td>

Initials of the user who created the activity stream entry.Data type: String

</td></tr><tr><td>

entries.login\_name

</td><td>

Full user name for the user who created the activity stream entry.Data type: String

</td></tr><tr><td>

entries.name

</td><td>

Full user name for the user who created the activity stream entry.Data type: String

</td></tr><tr><td>

entries.sys\_created\_on

</td><td>

Date and time of creation for the activity stream entry, expressed in GMT timezone.Data type: String

Format: YYYY-MM-DD hh:mm:ss

</td></tr><tr><td>

entries.sys\_created\_on\_adjusted

</td><td>

Date and time of creation for the activity stream entry, expressed in logged-in user timezone.Data type: String

Format: YYYY-MM-DD hh:mm:ss

</td></tr><tr><td>

entries.sys\_id

</td><td>

Sys\_id for the activity stream entry.Data type: String

</td></tr><tr><td>

entries.user\_sys\_id

</td><td>

Sys\_id for user who created the activity stream entry. Data type: String

Table: User \[sys\_user\]

</td></tr><tr><td>

entries.value

</td><td>

Value for this journal entry.Data type: String

</td></tr><tr><td>

journal\_fields

</td><td>

List of journal fields present in the Case table from which activity entries are drawn.Data type: Array of Objects

```
"journal_fields": [
  {
    "can read": Boolean,
    "can_write": Boolean,
    "color": "String",
    "label": "String",
    "name": "String"
  }
]
```

</td></tr><tr><td>

journal\_fields.can\_read

</td><td>

Flag that indicates whether the logged-in user can read this journal field or not.Possible values:

-   true: The logged-in user can read this journal field.
-   false: The logged-in user can't read this journal field.

Data type: Boolean

</td></tr><tr><td>

journal\_fields.can\_write

</td><td>

Flag that indicates whether the logged-in user can write to the journal field or not.Possible values:

-   true: The logged-in user can write to this journal field.
-   false: The logged-in user can't write to this journal field.

Data type: Boolean

</td></tr><tr><td>

journal\_fields.color

</td><td>

Color that represents the journal field in case activity stream on ServiceNow AI Platform.Data type: String

</td></tr><tr><td>

journal\_fields.label

</td><td>

Display name for the journal field.Data type: String

</td></tr><tr><td>

journal\_fields.name

</td><td>

Name for the journal field.Data type: String

Table: Dictionary Entries \[sys\_dictionary\]

</td></tr><tr><td>

label

</td><td>

Display label for the table in which the CSM case record appears.Possible value: Case

Data type: String

</td></tr><tr><td>

number

</td><td>

Case number for the CSM case.Data type: String

</td></tr><tr><td>

short\_description

</td><td>

Short description for the CSM case.Data type: String

</td></tr><tr><td>

sys\_created\_on

</td><td>

Date and time of case creation, expressed in GMT timezone.Data type: String

Format: YYYY-MM-DD hh:mm:ss

</td></tr><tr><td>

sys\_created\_on\_adjusted

</td><td>

Date and time of case creation, expressed in logged-in user timezone.Data type: String

Format: YYYY-MM-DD hh:mm:ss

</td></tr><tr><td>

sys\_id

</td><td>

Sys\_id for the CSM case.Data type: String

Table: Case \[sn\_customerservice\_case\]

</td></tr><tr><td>

table

</td><td>

Name of the table in which the CSM case appears.Possible value: sn\_customerservice\_case

Data type: String

</td></tr><tr><td>

thumbnail\_path

</td><td>

Direct link to get thumbnail for attachment \(only for attachment of type images.\)Data type: String

</td></tr><tr><td>

user\_full\_name

</td><td>

Full name for logged-in user.Data type: String

</td></tr><tr><td>

user\_login

</td><td>

User ID for logged-in user.Data type: String

</td></tr><tr><td>

user\_sys\_id

</td><td>

Sys\_id for logged-in user.Data type: String

Table: User \[sys\_user\]

</td></tr></tbody>
</table>### cURL request

Retrieve the complete activity stream for a CSM case by sys\_id.

```
curl --request GET 'https://instance.servicenow.com/api/sn_customerservice/case/f352dc9387632300d6b0a7da0acb0b60/activities'  \
--request GET \
--header 'Accept: application/json' \
--user 'username':'password'
```

The response shows a single activity stream entry for the specified case, an **Additional comments** journal entry submitted by the agent.

```
{
  "result": {
    "display_value": "CS0001401",
    "sys_id": "f352dc9387632300d6b0a7da0acb0b60",
    "short_description": "Laptop is not working properly",
    "number": "CS0001401",
    "entries": [
      {
        "sys_created_on_adjusted": "2020-05-04 14:15:44",
        "sys_id": "600b6e4adb241010d045232d1396196a",
        "login_name": "John Jason",
        "user_sys_id": "da419c1fc312310015519f2974d3ae15",
        "initials": "JJ",
        "sys_created_on": "2020-05-04 21:15:44",
        "contains_code": "false",
        "field_label": "Additional comments",
        "name": "John Jason",
        "value": "Hi, Alex. Can you please send me a photo of the label on your laptop so we can send you the correct replacement?",
        "element": "comments"
      }
    ],
    "user_sys_id": "b1e0989f87232300d6b0a7da0acb0beb",
    "user_full_name": "Mark Johnson",
    "user_login": "admin",
    "label": "Case",
    "table": "sn_customerservice_case",
    "journal_fields": [
      {
        "can_read": true,
        "color": "transparent",
        "can_write": true,
        "name": "comments",
        "label": "Additional comments"
      },
      {
        "can_read": true,
        "color": "gold",
        "can_write": true,
        "name": "work_notes",
        "label": "Work notes"
      }
    ],
    "sys_created_on": "2019-02-15 21:57:04",
    "sys_created_on_adjusted": "2019-02-15 13:57:04"
  }
}

```

## Case - GET /sn\_customerservice/case/field\_values/\{field\_name\}

Retrieves the list of possible field values for a choice or reference field in the Case \[sn\_customerservice\_case\] table.

To use this endpoint, users must have the csm\_ws\_integration, sn\_customerservice.customer, or sn\_customerservice.consumer role.

Use this endpoint to populate field value lists in case creation forms.

When you request values for a reference field, any reference qualifiers defined for the requested field in the Dictionary Entry \[sys\_dictionary\] table are applied. For more information on reference qualifiers, see [Reference qualifiers](https://www.servicenow.com/docs/access?context=c_ReferenceQualifiers&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

You can use the **sysparm\_ref\_qual\_input** query parameter to specify field values to use when evaluating JavaScript reference qualifiers. For an example, see the query parameter listing below.

When you request values for a choice field that is dependent on another field, you can use the **sysparm\_dependent\_value** query parameter to specify a value for the dependency parent field and restrict the returned field values accordingly. For more details on dependent fields, see [Make a field dependent](https://www.servicenow.com/docs/access?context=t_MakingAFieldDependent&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

**Note:** You can reference all sysparm query parameters using either their full name or their shortened name \(without the **sysparm\_** prefix\). For example, for **sysparm\_limit** you can also use **limit**.

### URL format

Versioned URL: `/api/sn_customerservice/{api_version}/case/field_values/{field_name}`

Default URL: `/api/sn_customerservice/case/field_values/{field_name}`

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

field\_name

</td><td>

Name of a choice or reference field.Data type: String

Table: Case \[sn\_customerservice\_case\]

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sysparm\_dependent\_value

</td><td id="case-sysparm-dependent-value-entry">

Value to select in the Case \[sn\_customerservice\_case\] table choice field that the requested field is dependent on. Use only when requesting a choice field that is dependent on another field.As an example, suppose you create a custom **Channel Instance** choice field in the Case table which is dependent on the default **Channel** choice field. When **sysparm\_dependent\_value** is not specified, this endpoint returns the full set of values for your custom field. To instead return only the subset of custom field values that are available when the Phone CSM channel is chosen from the **Channel** field, specify:

`sysparm_dependent_value=Phone`

Data type: String

</td></tr><tr><td>

sysparm\_limit

</td><td>

Maximum number of records to return. Unusually large **sysparm\_limit** values can impact system performance. For requests that exceed this number of records, use the **sysparm\_offset** parameter to paginate record retrieval. Data type: Number

</td></tr><tr><td>

sysparm\_offset

</td><td>

Starting record index for which to begin retrieving records. Use this value to paginate record retrieval. This functionality enables the retrieval of all records, regardless of the number of records, in small manageable chunks. For example, the first time you call this endpoint, **sysparm\_offset** is set to "0". To simply page through all available records, use `sysparm_offset=sysparm_offset+sysparm_limit`, until you reach the end of all records.

Do not pass a negative number in the **sysparm\_offset** parameter.Data type: Number

Default: 0

</td></tr><tr><td>

sysparm\_reference\_field\_columns

</td><td id="sysparm_reference_field_columns-entry-case">

Comma-separated list of column names, from the table of the specified reference field, to return in the response. For example, if Contact is the specified reference field, you would include a list of all the fields in the Contact table to return.Data type: String

</td></tr><tr><td>

sysparm\_query

</td><td>

Encoded query used to filter the result set. Queries defined using this parameter are appended to any encoded queries produced by reference qualifiers.For example:

`(sysparm_query=caller_id=javascript:gs.getUserID()^active=true)`

The encoded query supports order by. To sort responses based on certain fields, use the ORDERBY and ORDERBYDESC clauses in **sysparm\_query**. For example, `sysparm_query=active=true^ORDERBYnumber^ORDERBYDESCcategory` filters all active records and orders the results in ascending order by number first, and then in descending order by category.

If part of the query is invalid, such as by specifying an invalid field name, the instance ignores the invalid part. It then returns rows using only the valid portion of the query. You can control this behavior using the property **glide.invalid\_query.returns\_no\_rows**. Set this property to true to return no rows on an invalid query.

**Note:** The **glide.invalid\_query.returns\_no\_rows** property controls the behavior of all queries across the instance, such as in lists, scripts \(GlideRecord.query\(\)\), and web service APIs.

Data type: String

</td></tr><tr><td>

sysparm\_ref\_qual\_input

</td><td id="case-sysparm-ref-qual-input-entry">

Encoded set of field values representing a current object to pass to reference qualifiers that use JavaScript functions. Use only when requesting a reference field.For example, when requesting values from the **Asset** field, you can set this query parameter value to return only assets belonging to the specified product instead of assets belonging to the product associated with the specified case:

`sysparm_ref_qual_input=product=5d1b7bb053401010dc25ddeeff7b129d`

Data type: String

Syntax: `{field1}={value1}^{field2}={value2}[…]`

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
</table><table class="rest_api_response_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Link

</td><td>

REST response data can be split into multiple result sets. Where applicable, the response header contains different links for the first set, previous set, next set, and the last set of records.For example:

`https://<instance name>.service-now.com/api/now/table/cmdb_ci?sysparm_offset=40&sysparm_limit=1000>;rel="next"`,

`https://<instance name>.service-now.com/api/now/table/cmdb_ci?sysparm_offset=40&sysparm_limit=1000>;rel="prev"`,

`https://<instance name>.service-now.com/api/now/table/cmdb_ci?sysparm_offset=0&sysparm_limit=1000>;rel="first"`,

`https://<instance name>.service-now.com/api/now/table/cmdb_ci?sysparm_offset=2780&sysparm_limit=1000>;rel="last"`

</td></tr></tbody>
</table>### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|400|Bad Request. A bad request type or malformed request was detected.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table id="table_m3x_ym1_bmb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

List of values for the requested field.Data type: Array of Objects

```
"result": [
  {
    "label": "String",
    "value": "String"
  }
]
```

</td></tr><tr><td>

result.label

</td><td>

Display value for the field value.Data type: String

</td></tr><tr><td>

result.value

</td><td>

Field value.Data type: String

</td></tr></tbody>
</table>### cURL request

Retrieve values for the contact reference field from all cases:

```
curl 'https://instance.servicenow.com/api/sn_customerservice/case/field_values/contact' \
--request GET \
--header 'Accept: application/json' \
--user 'username':'password'
```

The response displays labels and values for matching contacts:

```
{
  "result": [
    {
      "label": "Amy Pascal",
      "value": "268e22b0d7300200e5982cf65e6103d3"
    },
    {
      "label": "Marta Hoch",
      "value": "8c974d254fb81200025ba3618110c707"
    },
    {
      "label": "Charlie Brown",
      "value": "078d399dd7600200e5982cf65e6103a2"
    },
    {
      "label": "Alex Linde",
      "value": "60beb5e7d7600200e5982cf65e6103ad"
    },
    {
      "label": "Crissy Stark",
      "value": "00189b324f1e0200c0adfe618110c76d"
    },
    {
      "label": "Denis Koch",
      "value": "07e6fa386f0331003b3c498f5d3ee4a1"
    }
  ]
}
```

## Case - GET /sn\_customerservice/case/\{id\}/field\_values/\{field\_name\}

Retrieves the list of possible field values for a choice or reference field for a specified record in the Case \[sn\_customerservice\_case\] table.

To use this endpoint, users must have the csm\_ws\_integration, sn\_customerservice.customer, or sn\_customerservice.consumer role.

Use this endpoint to populate field value lists in case update forms.

When you request values for a reference field, any reference qualifiers defined for the requested field in the Dictionary Entry \[sys\_dictionary\] table are applied, using values from the specified case record. For more information on reference qualifiers, see [Reference qualifiers](https://www.servicenow.com/docs/access?context=c_ReferenceQualifiers&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

You can use the **sysparm\_ref\_qual\_input** query parameter to override values from the specified case when evaluating JavaScript reference qualifiers. For an example, see the query parameter listing below.

When you request values for a choice field that is dependent on another field, this endpoint limits returned field values based on the dependency parent field value selected in the specified case record. For more details on dependent fields, see [Make a field dependent](https://www.servicenow.com/docs/access?context=t_MakingAFieldDependent&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

You can use the **sysparm\_dependent\_value** query parameter to override the selection from the dependency parent field. For an example, see the query parameter listing below.

**Note:** You can reference all sysparm query parameters using either their full name or their shortened name \(without the **sysparm\_** prefix\). For example, for **sysparm\_limit** you can also use **limit**.

### URL format

Versioned URL: `/api/sn_customerservice/{api_version}/case/{id}/field_values/{field_name}`

Default URL: `/api/sn_customerservice/case/{id}/field_values/{field_name}`

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

field\_name

</td><td>

Name of a choice or reference field.Data type: String

Table: Case \[sn\_customerservice\_case\]

</td></tr><tr><td>

id

</td><td>

Sys\_id of a record to use when evaluating reference qualifiers.Data type: String

Table: Case \[sn\_customerservice\_case\]

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sysparm\_dependent\_value

</td><td id="case-sysparm-dependent-value-entry">

Value to select in the Case \[sn\_customerservice\_case\] table choice field that the requested field is dependent on. Use only when requesting a choice field that is dependent on another field.As an example, suppose you create a custom **Channel Instance** choice field in the Case table which is dependent on the default **Channel** choice field. When **sysparm\_dependent\_value** is not specified, this endpoint returns the full set of values for your custom field. To instead return only the subset of custom field values that are available when the Phone CSM channel is chosen from the **Channel** field, specify:

`sysparm_dependent_value=Phone`

Data type: String

</td></tr><tr><td>

sysparm\_limit

</td><td>

Maximum number of records to return. Unusually large **sysparm\_limit** values can impact system performance. For requests that exceed this number of records, use the **sysparm\_offset** parameter to paginate record retrieval. Data type: Number

</td></tr><tr><td>

sysparm\_offset

</td><td>

Starting record index for which to begin retrieving records. Use this value to paginate record retrieval. This functionality enables the retrieval of all records, regardless of the number of records, in small manageable chunks. For example, the first time you call this endpoint, **sysparm\_offset** is set to "0". To simply page through all available records, use `sysparm_offset=sysparm_offset+sysparm_limit`, until you reach the end of all records.

Do not pass a negative number in the **sysparm\_offset** parameter.Data type: Number

Default: 0

</td></tr><tr><td>

sysparm\_query

</td><td>

Encoded query used to filter the result set. Queries defined using this parameter are appended to any encoded queries produced by reference qualifiers.For example:

`(sysparm_query=caller_id=javascript:gs.getUserID()^active=true)`

The encoded query supports order by. To sort responses based on certain fields, use the ORDERBY and ORDERBYDESC clauses in **sysparm\_query**. For example, `sysparm_query=active=true^ORDERBYnumber^ORDERBYDESCcategory` filters all active records and orders the results in ascending order by number first, and then in descending order by category.

If part of the query is invalid, such as by specifying an invalid field name, the instance ignores the invalid part. It then returns rows using only the valid portion of the query. You can control this behavior using the property **glide.invalid\_query.returns\_no\_rows**. Set this property to true to return no rows on an invalid query.

**Note:** The **glide.invalid\_query.returns\_no\_rows** property controls the behavior of all queries across the instance, such as in lists, scripts \(GlideRecord.query\(\)\), and web service APIs.

Data type: String

</td></tr><tr><td>

sysparm\_reference\_field\_columns

</td><td id="sysparm_reference_field_columns-entry-case">

Comma-separated list of column names, from the table of the specified reference field, to return in the response. For example, if Contact is the specified reference field, you would include a list of all the fields in the Contact table to return.Data type: String

</td></tr><tr><td>

sysparm\_ref\_qual\_input

</td><td id="case-sysparm-ref-qual-input-entry">

Encoded set of field values representing a current object to pass to reference qualifiers that use JavaScript functions. Use only when requesting a reference field.For example, when requesting values from the **Asset** field, you can set this query parameter value to return only assets belonging to the specified product instead of assets belonging to the product associated with the specified case:

`sysparm_ref_qual_input=product=5d1b7bb053401010dc25ddeeff7b129d`

Data type: String

Syntax: `{field1}={value1}^{field2}={value2}[…]`

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
</table><table class="rest_api_response_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Link

</td><td>

REST response data can be split into multiple result sets. Where applicable, the response header contains different links for the first set, previous set, next set, and the last set of records.For example:

`https://<instance name>.service-now.com/api/now/table/cmdb_ci?sysparm_offset=40&sysparm_limit=1000>;rel="next"`,

`https://<instance name>.service-now.com/api/now/table/cmdb_ci?sysparm_offset=40&sysparm_limit=1000>;rel="prev"`,

`https://<instance name>.service-now.com/api/now/table/cmdb_ci?sysparm_offset=0&sysparm_limit=1000>;rel="first"`,

`https://<instance name>.service-now.com/api/now/table/cmdb_ci?sysparm_offset=2780&sysparm_limit=1000>;rel="last"`

</td></tr></tbody>
</table>### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|400|Bad Request. A bad request type or malformed request was detected.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

List of values for the requested field.Data type: Array of Objects

```
"result": [
  {
    "label": "String",
    "value": "String"
  }
]
```

</td></tr><tr><td>

result.label

</td><td>

Display value for the field value.Data type: String

</td></tr><tr><td>

result.value

</td><td>

Field value.Data type: String

</td></tr></tbody>
</table>### cURL request

Retrieve the contact reference field value for an existing case:

```
curl 'https://instance.servicenow.com/api/sn_customerservice/case/f352dc9387632300d6b0a7da0acb0b60/field_values/contact' \
--request GET \
--header 'Accept: application/json' \
--user 'username':'password'
```

The response displays the label and value for the contact assigned to the specified case:

```
{
  "result": [
    {
      "label": "Alex Linde",
      "value": "60beb5e7d7600200e5982cf65e6103ad"
    }
  ]
}
```

## Case - GET /sn\_customerservice/case/\{id\}

Retrieves the specified Customer Service Management \(CSM\) case.

To use this endpoint, users must have the csm\_ws\_integration, sn\_customerservice.customer, or sn\_customerservice.consumer role.

**Note:** You can reference all sysparm query parameters using either their full name or their shortened name \(without the **sysparm\_** prefix\). For example, for **sysparm\_limit** you can also use **limit**.

### URL format

Versioned URL: `/api/sn_customerservice/{api_version}/case/{id}`

Default URL: `/api/sn_customerservice/case/{id}`

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

Sys\_id or case number for the case to retrieve. Results will be unpredictable if a specified case number is shared by two or more cases.Data type: String

Table: Case \[sn\_customerservice\_case\]

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sysparm\_display\_value

</td><td id="entry-sysparm_display_value-REST_API">

Determines the type of data returned, either the actual values from the database or the display values of the fields. Display values are manipulated based on the actual value in the database and user or system settings and preferences.If returning display values, the value that is returned is dependent on the field type.

-   Choice fields: The database value may be a number, but the display value will be more descriptive.
-   Date fields: The database value is in UTC format, while the display value is based on the user's time zone.
-   Encrypted text: The database value is encrypted, while the displayed value is unencrypted based on the user's encryption context.
-   Reference fields: The database value is sys\_id, but the display value is a display field of the referenced record.

Data type: String

Valid values:

-   true: Returns the display values for all fields.
-   false: Returns the actual values from the database.
-   all: Returns both actual and display values.

Default: false

**Note:** There is no preferred method for setting this parameter. However, specifying the display value may cause performance issues since it is not reading directly from the database and may include referencing other fields and records. For more information on display values and actual values, see [Table API FAQs \(KB0534905\).](https://support.servicenow.com/kb_view.do?sysparm_article=KB0534905)

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

Indicates that the request is invalid. Could be due to one of the following reasons:-   Requested case does not exist.
-   User does not have access to the case.

</td></tr></tbody>
</table>### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Element

</th><th>

Description

</th></tr></thead><tbody><tr><td>

account

</td><td id="casetable-account-entry">

Sys\_id of the account record associated with the case.

Data type: String

Table: Account \[customer\_account\]

</td></tr><tr><td>

account

</td><td>

Account details.Data type: Object

```
"account": {
  "account_code": "String",
  "account_parent": "String",
  "account_path": "String",
  "active_escalation": "String",
  "apple_icon": Image,
  "banner_image": Image,
  "banner_image_light": Image,
  "banner_text": "String",
  "city": "String",
  "contact": "String",
  "country": "String",
  "customer": "String",
  "discount": "String",
  "fax_phone": "String",
  "fiscal_year": "String",
  "lat_long_error": "String",
  "latitude": "String",
  "longitude": "String",
  "market_cap": "String",
  "name": "String",
  "notes": "String",
  "num_employees": Number,
  "number": "String",
  "parent": "String",
  "partner": "String",
  "phone": "String",
  "primary": Boolean,
  "primary_contact": "String",
  "profits": Number,
  "publicly_traded": Boolean,
  "rank_tier": "String",
  "registration_code": "String",
  "revenue_per_year": Number,
  "state": "String",
  "stock_price": "String",
  "stock_symbol": "String",
  "street": "String",
  "sys_class_name": "String",
  "sys_created_by": "String",
  "sys_created_on": "String",
  "sys_id": "String",
  "sys_mod_count": Number,
  "sys_updated_by": "String",
  "sys_updated_on": "String",
  "theme": "String",
  "vendor": Boolean,
  "vendor_manager": "String",
  "vendor_type": "String",
  "website": "String",
  "zip": "String
}
```

</td></tr><tr><td>

account.account\_code

</td><td>

Unique combination of values that an application uses to identify budget forecasts and budget plans.Data type: String

Maximum length: 255

</td></tr><tr><td>

account.account\_parent

</td><td>

Sys\_id of the parent account of this account. Located in the Account \[customer\_account\] table.Data type: String

</td></tr><tr><td>

account.account\_path

</td><td>

Path from the parent to the child accounts in the account hierarchy.Data type: String

Maximum length: 255

</td></tr><tr><td>

account.active\_escalation

</td><td>

Sys\_id of the active escalation associated with the account.Data type: String

Table: Escalation \[sn\_customerservice\_escalation\]

</td></tr><tr><td>

account.apple\_icon

</td><td>

Icon for iPhone home page bookmarks.Data type: Image

</td></tr><tr><td>

account.banner\_image

</td><td>

Banner image that appears on the customer portal.Data type: Image

</td></tr><tr><td>

account.banner\_image\_light

</td><td>

Small banner image.Data type: Image

</td></tr><tr><td>

account.banner\_text

</td><td>

Banner text that appears on the customer portal.Data type: String

Maximum length: 4,000

</td></tr><tr><td>

account.city

</td><td>

City in which the company that is associated with this account resides.Data type: String

Maximum length: 50

</td></tr><tr><td>

account.contact

</td><td>

Sys\_id of a contact record associated with this account.Data type: String

Table: User \[sys\_user\]

</td></tr><tr><td>

account.country

</td><td>

Country in which the company that is associated with this account resides.Data type: String

Maximum length: 40

Default: USA

</td></tr><tr><td>

account.customer

</td><td>

Flag that indicates whether the account is a customer account, as opposed to a partner account.Possible values:

-   true: Customer account
-   false: Partner account

Data type: Boolean

Default: false

</td></tr><tr><td>

account.discount

</td><td>

Discount given to the account on purchases.Data type: Number

Maximum length: 15

</td></tr><tr><td>

account.fax\_phone

</td><td>

Primary fax phone number for the company associated with this account.Data type: String

Maximum length: 40

</td></tr><tr><td>

account.fiscal\_year

</td><td>

Fiscal year for the company associated with the account.Data type: String

</td></tr><tr><td>

account.lat\_long\_error

</td><td>

Difference in the actual location as compared to latitude and longitude information.Data type: String

Maximum length: 1,000

</td></tr><tr><td>

account.latitude

</td><td>

Latitude of the company associated with this account.Data type: Number \(floating point number\)

Maximum length: 40

</td></tr><tr><td>

account.longitude

</td><td>

Longitude of the company associated with this account.Data type: Number \(floating point number\)

Maximum length: 40

</td></tr><tr><td>

account.manufacturer

</td><td>

Flag that indicates whether the company associated with this account manufactures goods.Possible values:

-   true: Manufactures goods
-   false: Does not manufacture goods

Data type: Boolean

Default: false

</td></tr><tr><td>

account.market\_cap

</td><td>

Market value of the associated company's publicly traded stock shares.Data type: Number \(currency\)

Maximum length: 20

</td></tr><tr><td>

account.name

</td><td>

Name of the company associated with this account.Data type: String

Maximum length: 80

</td></tr><tr><td>

account.notes

</td><td>

Additional information about the company.Data type: String

Maximum length: 4,000

</td></tr><tr><td>

account.num\_employees

</td><td>

Number of people employed by the company.Data type: Number \(Integer\)

Maximum length: 40

</td></tr><tr><td>

account.number

</td><td>

Number that identifies this account.Data type: String

Maximum length: 40

</td></tr><tr><td>

account.parent

</td><td>

Sys\_id of the parent account of this account.Data type: String

Table: Company \[core\_company\]

</td></tr><tr><td>

account.partner

</td><td>

Flag that indicates whether the account is a partner account or a customer account.Possible values:

-   true: Partner account
-   false: Customer account

Data type: Boolean

Default: false

</td></tr><tr><td>

account.phone

</td><td>

Primary phone number for the company.Data type: String

</td></tr><tr><td>

account.primary

</td><td>

Flag that indicates whether this is a primary account.Possible values:

-   true: Primary account
-   false: Secondary account

Data type: Boolean

Default: false

</td></tr><tr><td>

account.primary\_contact

</td><td>

Sys\_id of the primary contact for the account.Data type: String

Table: Contact \[customer\_contact\]

</td></tr><tr><td>

account.profits

</td><td>

Profit information entered for this account.Data type: Number \(Currency\)

Maximum length: 40

</td></tr><tr><td>

account.publicly\_traded

</td><td>

Flag that indicates whether the company associated with this account is publicly traded on the stock exchange.Possible values:

-   true: Publicly traded
-   false: Private company

Data type: Boolean

</td></tr><tr><td>

account.rank\_tier

</td><td>

Type of account.Possible values:

-   blacklist
-   other
-   strategic
-   tactical
-   valued

Data type: String

Maximum length: 40

</td></tr><tr><td>

account.registration\_code

</td><td>

Unique code that customers use when requesting a login on the customer portal. This code provides a method for validating the customer on the company before granting access.Data type: String

Maximum length: 40

</td></tr><tr><td>

account.revenue\_per\_year

</td><td>

Revenue produced by the company associated with this account.Data type: Number \(Currency\)

Maximum length: 20

</td></tr><tr><td>

account.state

</td><td>

State in which the company resides.Data type: String

Maximum length: 40

</td></tr><tr><td>

account.stock\_price

</td><td>

Price of the company stock.Data type: String

Maximum length: 40

</td></tr><tr><td>

account.stock\_symbol

</td><td>

Stock symbol of the company.Data type: String

Maximum length: 40

</td></tr><tr><td>

account.street

</td><td>

Street address of the company.Data type: String

Maximum length: 255

</td></tr><tr><td>

account.sys\_class\_name

</td><td>

Table that contains the associated account record.Data type: String

</td></tr><tr><td>

account.sys\_created\_by

</td><td>

User that originally created the account.Data type: String

Maximum length: 40

</td></tr><tr><td>

account.sys\_created\_on

</td><td>

Date and time that the account was originally created.Data type: String

</td></tr><tr><td>

account.sys\_id

</td><td>

Sys\_id for the account record.Data type: String

</td></tr><tr><td>

account.sys\_mod\_count

</td><td>

Number of times the account information has been updated.Data type: Number \(Integer\)

</td></tr><tr><td>

account.sys\_updated\_by

</td><td>

User that last modified the account information.Data type: String

Maximum length: 40

</td></tr><tr><td>

account.sys\_updated\_on

</td><td>

Date and time the account information was last updated.Data type: String

</td></tr><tr><td>

account.theme

</td><td>

Sys\_id of the customer portal theme used by this account.Data type: String

Table: Theme \[sys\_ui\_theme\]

</td></tr><tr><td>

account.vendor

</td><td>

Flag that indicates whether the company associated with this account is a vendor.Possible values:

-   true: Vendor
-   false: Not a vendor

Data type: Boolean

Default: false

</td></tr><tr><td>

account.vendor\_manager

</td><td>

List of sys\_ids of the vendor managers for the account.Data type: String

Table: User \[sys\_user\]

</td></tr><tr><td>

account.vendor\_type

</td><td>

List of sys\_ids of the type of vendor such as, applications, hardware, services, or software.Data type: String

Table: Vendor Type \[vendor\_type\]

</td></tr><tr><td>

account.website

</td><td>

URL of the website for the company.Data type: String

Maximum length: 1,024

</td></tr><tr><td>

account.zip

</td><td>

Zip code of the company.Data type: String

Maximum length: 40

</td></tr><tr><td>

active

</td><td id="casetable-active-entry">

Flag that indicates whether the case is open and active.Possible values:

-   true: Case is active
-   false: Case is closed

Data type: Boolean

Default: true

</td></tr><tr><td>

active\_account\_escalation

</td><td id="casetable-active_account_escalation-entry">

Sys\_id of the active account escalation record associated with the case.Data type: String

Table: Escalation \[sn\_customerservice\_escalation\]

</td></tr><tr><td>

active\_escalation

</td><td id="casetable-active_escalation-entry">

Sys\_id of the active escalation record associated with the case.Data type: String

Table: Escalation \[sn\_customerservice\_escalation\]

</td></tr><tr><td>

activity\_due

</td><td id="casetable-activity_due-entry">

Date for which the associated case is expected to be completed.Data type: String

</td></tr><tr><td>

additional\_assignee\_list

</td><td id="casetable-additional_assignee_list-entry">

List of the sys\_ids of the additional persons \(other than the primary assignee\) that have been assigned to the account.Data type: Array

Maximum: 4,000

Table: User \[sys\_user\]

</td></tr><tr><td>

approval

</td><td id="casetable-approval-entry">

String that describes the type of approval required.Possible values:

-   approved
-   cancelled
-   duplicate
-   not\_required
-   not requested
-   rejected
-   requested

Data type: String

Maximum characters: 40

Default: not requested

</td></tr><tr><td>

approval\_history

</td><td id="casetable-approval_history-entry">

List of all approvals associated with the case.Data type: String

Maximum characters: 4,000

</td></tr><tr><td>

approval\_set

</td><td id="casetable-approval_set-entry">

Date and time that the associated action was approved.Data type: String

</td></tr><tr><td>

asset

</td><td id="casetable-asset-entry">

Sys\_id of the asset record associated with the case.Data type: String

Table: Asset \[alm\_asset\]

</td></tr><tr><td>

assigned\_to

</td><td id="casetable-assigned_to-entry">

Sys\_id of the person assigned to the case.

Table: User \[sys\_user\]

 Data type: String

</td></tr><tr><td>

assignment\_group

</td><td id="casetable-aassignment_group-entry">

Sys\_id of the customer service agent group assigned to the case.Data type: String

Table: Group \[sys\_user\_group\]

</td></tr><tr><td>

business\_duration

</td><td id="casetable-business_duration-entry">

Length in calendar work hours, work days, and work weeks that it took to complete the case.Data type: String

</td></tr><tr><td>

business\_impact

</td><td id="casetable-business_impact-entry">

Impact of the issue on the associated customer.Data type: String

Maximum characters: 4,000

</td></tr><tr><td>

business\_service

</td><td id="casetable-business_service-entry">

Sys\_id of the service record associated with the case.Data type: String

Table: Service \[cmdb\_ci\_service\]

</td></tr><tr><td>

case

</td><td id="casetable-case-entry">

Case short description and case number.Data type: String

Maximum length: 300

</td></tr><tr><td>

case\_report

</td><td id="casetable-case_report-entry">

Sys\_id of the associated case report.Data type: String

Table: Case Report \[sn\_customerservice\_case\_report\]

</td></tr><tr><td>

category

</td><td id="casetable-category-entry">

Case category.Possible values:

-   0: Question
-   1: Issue
-   2: Feature

Data type: Number \(Integer\)

Default: 1

</td></tr><tr><td>

cause

</td><td id="casetable-cause-entry">

Details about the cause of the problem.Data type: String

Maximum length: 4,000

</td></tr><tr><td>

caused\_by

</td><td id="casetable-caused_by-entry">

Sys\_id of the change request that caused the case to be created.Data type: String

Table: Change Request \[change\_request\]

</td></tr><tr><td>

change

</td><td id="casetable-change-entry">

Sys\_id of the change request that caused the case to be created.Data type: String

Table: Change Request \[change\_request\]

</td></tr><tr><td>

child\_case\_creation\_progress

</td><td id="casetable-child_case_creation_progress-entry">

Flag that indicates whether the case is a child case that was created from a major case.Possible values:

-   true: Child case created from a major case
-   false: Not a child case

Data type: Boolean

</td></tr><tr><td>

closed\_at

</td><td id="casetable-closed_at-entry">

Date and time that the case was closed.Data type: String

</td></tr><tr><td>

closed\_by

</td><td id="casetable-closed_by-entry">

Sys\_id of the user that closed the case.Data type: String

Table: User \[sys\_user\]

</td></tr><tr><td>

close\_notes

</td><td id="casetable-close_notes-entry">

Notes made when the case was closed.Data type: String

Maximum length: 4,000

</td></tr><tr><td>

cmdb\_ci

</td><td id="casetable-cmdb_ci-entry">

Sys\_id of the configuration item associated with the case.Data type: String

Table: Configuration Item \[cmdb\_ci\]

</td></tr><tr><td>

comments

</td><td id="casetable-comments-entry">

Additional comments about the case.Data type: String

Maximum length: 4,000

</td></tr><tr><td>

comments\_and\_work\_notes

</td><td id="casetable-comments_and_work_notes-entry">

Comments and work notes entered for the case.Data type: String

Maximum length: 4,000

</td></tr><tr><td>

company

</td><td id="casetable-company-entry">

Sys\_id of the company associated with the case.Data type: String

Table: Company \[core\_company\]

</td></tr><tr><td>

consumer

</td><td id="casetable-consumer-entry">

Business-to-consumer cases only. Sys\_id of the person to contact with regard to this case.Data type: String

Table: Consumer \[csm\_consumer\]

</td></tr><tr><td>

consumer

</td><td>

Array of parameters for business-to-consumer cases.

</td></tr><tr><td>

consumer.active

</td><td>

Flag that indicates whether the consumer is active.Possible values:

-   true: Consumer active
-   false: Consumer de-activated

Data type: Boolean

Default: true

</td></tr><tr><td>

consumer.business\_phone

</td><td>

Business phone number of the consumer.Data type: String

Maximum length: 40

</td></tr><tr><td>

consumer.city

</td><td>

City in which the consumer resides.Data type: String

Maximum length: 100

</td></tr><tr><td>

consumer.country

</td><td>

Country in which the consumer resides.Data type: String

Maximum length: 40

</td></tr><tr><td>

consumer.date\_format

</td><td>

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

consumer.email

</td><td>

Email address of the consumer.Data type: String

Maximum length: 100

</td></tr><tr><td>

consumer.fax

</td><td>

Fax number of the consumer.Data type: String

Maximum length: 40

</td></tr><tr><td>

consumer.first\_name

</td><td>

Consumer first name.Data type: String

Maximum length: 50

</td></tr><tr><td>

consumer.gender

</td><td>

Gender of the consumer.Data type: String

Maximum length: 40

</td></tr><tr><td>

consumer.home\_phone

</td><td>

Home phone number of the consumer.Data type: String

Maximum length: 40

</td></tr><tr><td>

consumer.household

</td><td>

Sys\_id of the record that describes the household characteristics.Data type: String

Table: Household \[csm\_household\]

</td></tr><tr><td>

consumer.last\_name

</td><td>

Consumer last name.Data type: String

Maximum length: 50

</td></tr><tr><td>

consumer.middle\_name

</td><td>

Consumer middle name.Data type: String

Maximum length: 50

</td></tr><tr><td>

consumer.mobile\_phone

</td><td>

Consumer mobile phone number.Data type: String

Maximum length: 40

</td></tr><tr><td>

consumer.name

</td><td>

Consumer full name; first\_name+middle\_name+last\_name.Data type: String

Maximum length: 152

</td></tr><tr><td>

consumer.notes

</td><td>

Notes on consumer.Data type: String

Maximum length: 4,000

</td></tr><tr><td>

consumer.notification

</td><td>

Indicates whether the consumer should receive notifications.Valid values:

-   1: Disabled
-   2: Enabled

Data type: Number \(Integer\)

Maximum length: 40

Default: 2

</td></tr><tr><td>

consumer.number

</td><td>

Unique number associated with the consumer.Data type: String

Maximum length: 40

</td></tr><tr><td>

consumer.photo

</td><td>

Photo of the consumer.Data type: Image

</td></tr><tr><td>

consumer.preferred\_language

</td><td>

Consumer primary language.Data type: String

Maximum length: 3

</td></tr><tr><td>

consumer.prefix

</td><td>

Consumer name prefix such as, Dr., Mr., Mrs., or Ms.Data type: String

Maximum length: 40

</td></tr><tr><td>

consumer.primary

</td><td>

Flag that indicates whether this is the primary consumer.Possible values:

-   true: Primary consumer
-   false: Not primary consumer

Data type: Boolean

Default: false

</td></tr><tr><td>

consumer.state

</td><td>

State in which the consumer resides.Data type: String

Maximum length: 100

</td></tr><tr><td>

consumer.street

</td><td>

Consumer street address.Data type: String

Maximum length: 255

</td></tr><tr><td>

consumer.suffix

</td><td>

Consumer name suffix such as Jr., Sr., or II.Data type: String

</td></tr><tr><td>

consumer.sys\_created\_by

</td><td>

User that created the consumer record.Data type: String

Maximum length: 40

</td></tr><tr><td>

consumer.sys\_created\_on

</td><td>

Date and time the consumer record was originally created.Data type: String

</td></tr><tr><td>

consumer.sys\_domain

</td><td>

ServiceNow domain in which the consumer information resides.Data type: String

</td></tr><tr><td>

consumer.sys\_id

</td><td>

Unique identifier for the consumer.Data type: String

</td></tr><tr><td>

consumer.sys\_mod\_count

</td><td>

Number of times that the associated consumer information has been modified.Data type: Number \(Integer\)

</td></tr><tr><td>

consumer.sys\_updated\_by

</td><td>

User that last updated the consumer information.Data type: String

Maximum length: 40

</td></tr><tr><td>

consumer.sys\_updated\_on

</td><td>

Date and time when the consumer information was last updated.Data type: String

</td></tr><tr><td>

consumer.time\_format

</td><td>

Format in which to display time.Valid values:

-   hh.mm.ss a: hh.mm.ss \(12 hour\)
-   hh:mm:ss a: hh:mm:ss \(12 hour\)
-   HH.mm.ss: hh.mm.ss \(24 hour\)
-   HH:mm:ss: hh:mm:ss \(24 hour\)

Data type: String

Maximum length: 40

Default: blank \(system time format\)

</td></tr><tr><td>

consumer.time\_zone

</td><td>

Consumer time zone, such as Canada/Central or US/Eastern.Data type: String

Maximum length: 40

</td></tr><tr><td>

consumer.title

</td><td>

Consumer business title such as Manager, Software Developer, or Contractor.Data type: String

Maximum length: 60

</td></tr><tr><td>

consumer.user

</td><td>

Sys\_id of the consumer user. Data type: String

Table: Consumer User \[csm\_consumer\_user\]

</td></tr><tr><td>

consumer.zip

</td><td>

Consumer zip code. Data type: String

Maximum length: 40

</td></tr><tr><td>

contact

</td><td id="casetable-contact-entry">

Business-to-business based cases only. Sys\_id of the person to contact regarding this case.Data type: String

Table: Contact \[customer\_contact\]

</td></tr><tr><td>

contact

</td><td>

Array of contact parameters for business-to-business cases.

</td></tr><tr><td>

contact.account

</td><td>

Sys\_id of the account record to which the contact is associated.Data type: String

Table: Account \[customer\_account\]

</td></tr><tr><td>

contact.active

</td><td>

Flag that indicates whether the contact is active within the system.Possible values:

-   true: Contact is active
-   false: Contact is inactive

Data type: Boolean

Default: true

</td></tr><tr><td>

contact.agent\_status

</td><td>

Status of the agent.Possible values:

-   Off work
-   On break
-   On route
-   On site

Data type: String

Maximum length: 40

</td></tr><tr><td>

contact.building

</td><td>

Sys\_id of the record that describes the building in which the contact resides.Data type: String

Table: Building \[cmn\_building\]

</td></tr><tr><td>

contact.calendar\_integration

</td><td>

Calendar application that the contact uses.1: Outlook

Data type: Number \(Integer\)

Default: 1

</td></tr><tr><td>

contact.city

</td><td>

City in which the contact resides.Data type: String

Maximum length: 40

</td></tr><tr><td>

contact.company

</td><td>

Sys\_id of the company record to which the contact is associated.Data type: String

Table: Company \[core\_company\]

</td></tr><tr><td>

contact.cost\_center

</td><td>

Sys\_id of the cost center associated with the contact.Data type: String

Table: Cost Center \[cmn\_cost\_center\]

</td></tr><tr><td>

contact.country

</td><td>

Country code of the country in which the contact resides.Data type: String

Maximum length: 3

</td></tr><tr><td>

contact.date\_format

</td><td>

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

contact.default\_perspective

</td><td>

Sys\_id of the default perspective for the contact.Data type: String

Table: Menu List \[sys\_perspective\]

</td></tr><tr><td>

contact.department

</td><td>

Sys\_id of the department associated with the contact.Data type: String

Table: Department \[cmn\_department\]

</td></tr><tr><td>

contact.edu\_status

</td><td>

Education status of the associated contact.Data type: String

Maximum length: 40

Default: faculty

</td></tr><tr><td>

contact.email

</td><td>

Contact email address.Data type: String

</td></tr><tr><td>

contact.employee\_number

</td><td>

Contact employee number.Data type: String

</td></tr><tr><td>

contact.enable\_multifactor\_authn

</td><td>

Flag that indicates whether multifactor authorization is required for the contact to log in to the service portal.Possible values:

-   true: Multifactor authorization enabled
-   false: Multifactor authorization disabled

Data type: Boolean

Default: false

</td></tr><tr><td>

contact.failed\_attempts

</td><td>

Number of failed log in attempts.Data type: Number \(Integer\)

</td></tr><tr><td>

contact.first\_name

</td><td>

Contact first name.Data type: String

Maximum length: 50

</td></tr><tr><td>

contact.gender

</td><td>

Contact gender.Data type: String

Maximum length: 40

</td></tr><tr><td>

contact.geolocation\_tracked

</td><td>

Flag that indicates whether the contact location is obtained through geotracking.Possible values:

-   true: Contact location obtained through geotracking
-   false: Contact location not obtained through geotracking

Data type: Boolean

Default value: false

</td></tr><tr><td>

contact.home\_phone

</td><td>

Contact home phone number.Data type: String

Maximum length: 40

</td></tr><tr><td>

contact.internal\_integration\_user

</td><td>

Flag that indicates whether the contact is an internal integration user.Possible values:

-   true: Internal integration user
-   false: Other type of user

Data type: Boolean

Default: false

</td></tr><tr><td>

contact.introduction

</td><td>

IntroductionData type: String

Maximum length: 40

</td></tr><tr><td>

contact.last\_login

</td><td>

Date on which the contact last logged into the system.Data type: String \(Date\)

</td></tr><tr><td>

contact.last\_login\_device

</td><td>

Device the consumer used the last time they logged in to the system.Data type: String

Maximum length: 40

</td></tr><tr><td>

contact.last\_login\_time

</td><td>

Date and time the contact logged in to the system.Data type: String \(Date/time\)

</td></tr><tr><td>

contact.last\_name

</td><td>

Contact last name.Data type: String

Maximum length: 50

</td></tr><tr><td>

contact.last\_position\_update

</td><td>

Date and time the last position was updated.Data type: String \(Date/time\)

</td></tr><tr><td>

contact.latitude

</td><td>

Latitude coordinate of the contact.Data type: Number \(Floating point\)

Maximum length: 40

</td></tr><tr><td>

contact.ldap\_server

</td><td>

Sys\_id of the LDAP server used by the contact to last log in to the system. Data type: String

Table: LDAP Server \[ldap\_server\_config\]

</td></tr><tr><td>

contact.location

</td><td>

Sys\_id of the record that describes the location of the contactData type: String

Table: Location \[cmn\_location\]

</td></tr><tr><td>

contact.locked\_out

</td><td>

Flag that indicates if the contact is locked-out.Possible values:

-   true: Contact locked-out
-   false: Contact not locked-out

Data type: Boolean

Default: false

</td></tr><tr><td>

contact.longitude

</td><td>

Longitude coordinate of the contact.Data type: Number \(Floating point\)

Maximum length: 40

</td></tr><tr><td>

contact.manager

</td><td>

Sys\_id of the record that describes the direct supervisor of the contact.Data type: String

Table: User \[sys\_user\]

</td></tr><tr><td>

contact.middle\_name

</td><td>

Contact middle name.Data type: Number \(Floating point\)

Maximum length: 50

</td></tr><tr><td>

contact.mobile\_phone

</td><td>

Contact mobile phone number.Data type: String

 Maximum length: 40

</td></tr><tr><td>

contact.name

</td><td>

Contact full name.Data type: String

Maximum length: 151

</td></tr><tr><td>

contact.notification

</td><td>

Indicates whether the contact should receive notifications.Valid values:

-   1: Disabled
-   2: Enabled

Data type: Number \(Integer\)

Default: 2

</td></tr><tr><td>

contact.on\_schedule

</td><td>

Indicates the timeliness of dispatched service personnel.Valid values:

-   Ahead: Ahead of schedule.
-   behind\_less30: Behind schedule, but less than 30 minutes.
-   behind\_30to60: Behind schedule between 30 and 60 minutes.
-   behind\_more60: Behind schedule more than 60 minutes.
-   on\_time: On schedule.

Data type: String

Maximum length: 40

</td></tr><tr><td>

contact.phone

</td><td>

Contact business phone number.Data type: String

Maximum length: 40

</td></tr><tr><td>

contact.photo

</td><td>

Photo image of the contact. Data type: String

</td></tr><tr><td>

contact.preferred\_language

</td><td>

Country code of the contact primary language.Data type: String

Maximum length: 3

</td></tr><tr><td>

contact.roles

</td><td>

List of user roles associated with the contact.Data type: String

Maximum length: 40

</td></tr><tr><td>

contact.schedule

</td><td>

Sys\_id of the record that describes the work schedule for the associated contact.Data type: String

Table: Schedule \[cmn\_schedule\]

</td></tr><tr><td>

contact.source

</td><td>

Source of the contact.Data type: String

Maximum length: 255

</td></tr><tr><td>

contact.state

</td><td>

State in which the contact resides.Data type: String

Maximum length: 40

</td></tr><tr><td>

contact.street

</td><td>

Contact street address.Data type: String

Maximum length: 255

</td></tr><tr><td>

contact.sys\_class\_name

</td><td>

Table that contains the contact record. Data type: String

Maximum length: 80

</td></tr><tr><td>

contact.sys\_created\_by

</td><td>

User that originally created the associated contact record.Data type: String

Maximum length: 40

</td></tr><tr><td>

contact.sys\_created\_on

</td><td>

Data and time the associated contact was originally created.Data type: String \(Date/time\)

</td></tr><tr><td>

contact.sys\_domain

</td><td>

ServiceNow instance domain of the associated contact record.Data type: String

</td></tr><tr><td>

contact.sys\_domain\_path

</td><td>

Contact record domain path.Data type: String

Maximum length: 255

Default: / \(global\)

</td></tr><tr><td>

contact.sys\_id

</td><td>

Unique identifier for the associated contact record.Data type: String

</td></tr><tr><td>

contact.sys\_mod\_count

</td><td>

Number of times that the associated contact record has been modified.Data type: Number \(Integer\)

</td></tr><tr><td>

contact.sys\_tags

</td><td>

System tags for the content.Data type: String

</td></tr><tr><td>

contact.sys\_updated\_by

</td><td>

User that last updated the associated contact information.Data type: String

Maximum length: 40

</td></tr><tr><td>

contact.sys\_updated\_on

</td><td>

Data and time the associated contact information was updated.Data type: String \(Date/time\)

</td></tr><tr><td>

contact.time\_format

</td><td>

Format in which to display time.Valid values:

-   hh.mm.ss a: hh.mm.ss \(12 hour\)
-   hh:mm:ss a: hh:mm:ss \(12 hour\)
-   HH.mm.ss: hh.mm.ss \(24 hour\)
-   HH:mm:ss: hh:mm:ss \(24 hour\)

Data type: String

Maximum length: 40

Default: Blank \(system time format\)

</td></tr><tr><td>

contact.time\_sheet\_policy

</td><td>

Sys\_id of the record that contains the time sheet policy for the associated contact.Data type: String

Table: Time Sheet Policy \[time\_sheet\_policy\]

</td></tr><tr><td>

contact.time\_zone

</td><td>

Time zone in which the contact resides, such as Canada/Central or US/Eastern.Data type: String

Maximum length: 40

</td></tr><tr><td>

contact.title

</td><td>

Contact business title such as Manager, Software Developer, or Contractor.Data type: String

Maximum length: 60

</td></tr><tr><td>

contact.user\_name

</td><td>

Contact user ID.Data type: String

Maximum length: 40

</td></tr><tr><td>

contact.vip

</td><td>

Flag that indicates whether the associated contact has VIP status.Possible values:

-   true: VIP
-   false: Not VIP

Data type: Boolean

Default: false

</td></tr><tr><td>

contact.web\_service\_access\_only

</td><td>

Flag that indicates whether the contact can only access services through the web.Possible values:

-   true: Web access only
-   false: Access through all available methods

Data type: Boolean

Default: false

</td></tr><tr><td>

contact.zip

</td><td>

Contact zip code.Data type: String

Maximum length: 40

</td></tr><tr><td>

contact\_local\_time

</td><td id="casetable-contact_local_time-entry">

Contact local time.Data type: String

Maximum length: 70

</td></tr><tr><td>

contact\_time\_zone

</td><td id="casetable-contact_time_zone-entry">

Time zone of the contact associated with the case.Data type: String

Maximum length: 40

</td></tr><tr><td>

contact\_type

</td><td id="casetable-contact_type-entry">

Method in which the case was initially reported.Possible values:

-   chat
-   email
-   phone
-   social
-   web

Data type: String

Maximum length: 40

</td></tr><tr><td>

contract

</td><td id="casetable-contract-entry">

Sys\_id of the contract associated with the case. This contract contains information about the type of support that is provided to the company associated to the case. A contract can include a company and contact and the specific assets that are covered. A contract can also include multiple service entitlements and SLAs.Data type: String

Table: Contract \[ast\_contract\]

</td></tr><tr><td>

correlation\_display

</td><td id="casetable-correlation_display-entry">

Correlation display.Data type: String

Maximum length: 100

</td></tr><tr><td>

correlation\_id

</td><td id="casetable-correlation_id-entry">

Correlation identifier.Data type: String

Maximum length: 100

</td></tr><tr><td>

delivery\_plan

</td><td id="casetable-delivery_plan-entry">

Sys\_id of the parent execution plan for this case.Data type: String

Table: Execution Plan \[sc\_cat\_item\_delivery\_plan\]

</td></tr><tr><td>

delivery\_task

</td><td id="casetable-delivery_task-entry">

Sys\_id of the execution plan task.Data type: String

Table: Execution Plan Task \[sc\_cat\_item\_delivery\_task\]

</td></tr><tr><td>

description

</td><td id="casetable-description-entry">

Detailed description of the problem associated with the case. Data type: String

Maximum length: 4,000

</td></tr><tr><td>

due\_date

</td><td id="casetable-due_date-entry">

Date that the case is due to be closed.Data type: String

</td></tr><tr><td>

entitlement

</td><td id="casetable-entitlement-entry">

Sys\_id of the entitlement record associated with the case. Entitlements define the type of support that a customer receives as well as the supported communication channels. An entitlement can be associated with a product, an asset, an account, or a contract.Data type: String

Table: Entitlement \[service\_entitlement\]

</td></tr><tr><td>

escalation

</td><td id="casetable-escalation-entry">

Current escalation level.Possible values:

-   0: Normal
-   1: Moderate
-   2: High
-   3: Overdue

Data type: Number \(Integer\)

Default: 0

</td></tr><tr><td>

expected\_start

</td><td id="casetable-expected_start-entry">

Date and time when work is scheduled to begin on the case.Data type: String

</td></tr><tr><td>

first\_response\_time

</td><td id="casetable-first_response_time-entry">

Date and time when the first action was taken on the case.Data type: String

</td></tr><tr><td>

follow\_the\_sun

</td><td id="casetable-follow_the_sun-entry">

Flag that indicates whether the case should be handed-off for global follow-up.If a customer enters additional comments on a Priority 1 - Critical or a Priority 2 - High case, or if the case is escalated, the flag is automatically set to true.

Possible values:

-   true: Case should be handed-off for global follow-up
-   false: Case shouldn't be handed-off for global follow-up

Data type: Boolean

Default: false

</td></tr><tr><td>

follow\_up

</td><td id="casetable-follow_up-entry">

Date and time of the next follow-up action.Data type: String

</td></tr><tr><td>

group\_list

</td><td id="casetable-group_list-entry">

List of sys\_ids of the group records associated with the case.Data type: Array

Table: Group \[sys\_user\_group\]

</td></tr><tr><td>

impact

</td><td id="casetable-impact-entry">

Impact on customer.Possible values:

-   1: High
-   2: Medium
-   3: Low

Data type: Number \(Integer\)

Default: 3

</td></tr><tr><td>

knowledge

</td><td id="casetable-knowledge-entry">

Flag that indicates if there is a knowledge base article available for the specified issue.Possible values:

-   true: Knowledge base article is available for this issue
-   false: Knowledge base article is not available for this issue

Data type: Boolean

Default: false

</td></tr><tr><td>

location

</td><td id="casetable-location-entry">

Sys\_id of the record describing the company location.Data type: String

Table: Location \[cmn\_location\]

</td></tr><tr><td>

made\_sla

</td><td id="casetable-made_sla-entry">

Flag that indicates whether the case was resolved in alignment with the associated service level agreement.Possible values:

-   true: Case was resolved in alignment with SLA
-   false: Case wasn't resolved according to the SLA

Data type: Boolean

Default: true

</td></tr><tr><td>

major\_case\_state

</td><td id="casetable-major_case_state-entry">

Current state of the major case.Possible values:

-   accepted: Initial state when a manager creates a major case or when a manager promotes a candidate case.
-   canceled: Case is canceled.
-   proposed: Initial state when an agent or manager creates or proposes a candidate case.
-   rejected: Manager rejected candidate case.

Data type: String

Maximum length: 40

</td></tr><tr><td>

needs\_attention

</td><td id="casetable-needs_attention-entry">

Flag that indicates whether the case needs attention.Possible values:

-   true: Case needs additional attention
-   false: Case doesn't need additional attention

Data type: Boolean

Default: false

</td></tr><tr><td>

notes\_to\_comments

</td><td id="casetable-notes_to_comments-entry">

Flag that indicates whether to add the resolution notes to the comments.Possible values:

-   true: Resolutions notes, when added, are also added to the comments
-   false: Resolution notes in comments aren't required

Data type: Boolean

</td></tr><tr><td>

notify

</td><td id="casetable-notify-entry">

Method to use to notify contact/consumer.Possible values:

-   1: Do not notify
-   2: Send email
-   3: Telephone

Data type: Number \(Integer\)

Default: 1

</td></tr><tr><td>

number

</td><td id="casetable-number-entry">

Case number.Data type: String

Maximum length: 40

</td></tr><tr><td>

opened\_at

</td><td id="casetable-opened_at-entry">

Date and time that the case was opened.Data type: String

</td></tr><tr><td>

opened\_by

</td><td id="casetable-opened_by-entry">

Sys\_id of the person that initially opened the case.Data type: String

Table: User \[sys\_user\]

</td></tr><tr><td>

order

</td><td id="casetable-order-entry">

Order of the case.Data type: Number \(Integer\)

</td></tr><tr><td>

parent

</td><td id="casetable-parent-entry">

Sys\_id of the parent case to which this case \(child\) is associated.Data type: String

Table: Task \[task\]

</td></tr><tr><td>

partner

</td><td id="casetable-partner-entry">

Sys\_id of the partner associated with the case.Data type: String

Table: Account \[customer\_account\]

</td></tr><tr><td>

partner\_contact

</td><td id="casetable-partner_contact-entry">

Sys\_id of the partner contact associated with the case.Data type: String

Table: Contact \[customer\_contact\]

</td></tr><tr><td>

priority

</td><td id="casetable-priority-entry">

Priority of the case. Possible values:

-   1: Critical
-   2: High
-   3: Moderate
-   4: Low

Data type: Number \(Integer\)

Default: 4

</td></tr><tr><td>

probable\_cause

</td><td id="casetable-probable_cause-entry">

Possible cause of the issue associated with the case.Data type: String

Maximum length: 4,000

</td></tr><tr><td>

problem

</td><td id="casetable-problem-entry">

Sys\_id of the issue that the customer is encountering.Data type: String

Table: Problem \[problem\]

</td></tr><tr><td>

product

</td><td id="casetable-product-entry">

Sys\_id of the product model of the asset associated to the case. A model is a specific version or configuration of an asset \(for example, Apple Mac Book Pro\).Data type: String

Table: Product Model \[cmdb\_model\]

</td></tr><tr><td>

reassignment\_count

</td><td id="casetable-reassignment_count-entry">

Number of times that the case was reassigned to a person that is responsible for moving the case forward.Data type: Number \(Integer\)

Default: 0

</td></tr><tr><td>

recipient\_list

</td><td id="casetable-recipient_list-entry">

Sys\_id of the record that contains the list of recipients for communications about this case.Data type: String

Table: Recipients List \[sn\_publications\_recipients\_list\]

</td></tr><tr><td>

rejection\_goto

</td><td id="casetable-rejection_goto-entry">

Sys\_id of the task to execute if the case is rejected.Data type: String

Table: Task \[task\]

</td></tr><tr><td>

resolution\_code

</td><td id="casetable-resolution_code-entry">

Resolution state for the case, such as "Solved - Fixed by Support/Guidance provided". Data type: String

Maximum length: 40

</td></tr><tr><td>

resolved\_at

</td><td id="casetable-resolved_at-entry">

Date and time that the case was resolved.Data type: String

</td></tr><tr><td>

resolved\_by

</td><td id="casetable-resolved_by-entry">

Sys\_id of the person that resolved the case.Data type: String

Table: User \[sys\_user\]

</td></tr><tr id="case-result-response-row"><td>

result

</td><td>

List of values for the requested field.Data type: Array of Objects

```
"result": [
  {
    "label": "String",
    "value": "String"
  }
]
```

</td></tr><tr id="case-result-label-response-row"><td>

result.label

</td><td>

Display value for the field value.Data type: String

</td></tr><tr id="case-result-value-response-row"><td>

result.value

</td><td>

Field value.Data type: String

</td></tr><tr><td>

short\_description

</td><td id="casetable-short_description-entry">

Concise description of the case. Data type: String

Maximum length: 160

</td></tr><tr><td>

skills

</td><td id="casetable-skills-entry">

List of the unique identifiers \(sys\_id\) of the skills needed to complete the case.Data type: String

Table: Skill \[cmn\_skill\]

</td></tr><tr><td>

sla\_due

</td><td id="casetable-sla_due-entry">

Date/time at which the case must be closed based on the associated service level agreement.Data type: String

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile

</td><td>

Details for a specific social media profile, such as Facebook, Twitter, or YouTube.Data type: Array of Objects

```
"sn_app_cs_social_social_profile": [
  {
    "account": "String",
    "channel": [Array],
    "contact": {Object},
    "consumer": {Object},
    "created_on": "String",
    "profile": "String",
    "profile_url": "String",
    "social_id": "String",
    "source": "String",
    "sys_created_by": "String",
    "sys_created_on": "String",
    "sys_id": "String",
    "sys_mod_count": Number,
    "sys_tags": "String",
    "sys_updated_by": "String",
    "sys_updated_on": "String"
  }
]
```

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.account

</td><td>

Unique identifier of the record containing account information for the social media profile. Located in the Account \[customer\_account\] table.Data type: String

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.channel

</td><td>

Details on the associated social media profile channel.Data type: Object

```
"channel": {
  "name": "String",
  "sys_class_name": "String",
  "sys_created_by": "String",
  "sys_created_on": "String",
  "sys_mod_count": Number,
  "sys_package": "String",
  "sys_policy": "String",
  "sys_scope": "String",
  "sys_tags": "String",
  "sys_update_name": "String",
  "sys_updated_by": "String",
  "sys_updated_on": "String"
}
```

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.channel.name

</td><td>

Name of the social media channel.Data type: String

Maximum length: 100

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.channel.sys\_class\_name

</td><td>

Table that contains the social media channel record.Data type: String

Maximum length: 80

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.channel.sys\_created\_by

</td><td>

Person that created the social media channel.Data type: String

Maximum length: 40

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.channel.sys\_created\_on

</td><td>

Date and time the social media profile was created.Data type: Date/time

Maximum length: 40

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.channel.sys\_id

</td><td>

Unique identifier of the associated social media profile channel.Data type: String

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.channel.sys\_mod\_count

</td><td>

Number of times that information was modified for the associated social media profile channel.Data type: Integer

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.channel.sys\_name

</td><td>

System name of channel.Data type: String

Maximum length: 255

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.channel.sys\_package

</td><td>

Unique identifier of the record that contains information about the package associated with the profile; Package \[sys\_package\] table.Data type: Reference

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.channel.sys\_policy

</td><td>

System protection policy.Possible values:

-   protected
-   read

Data type: String

Maximum length: 40

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.channel.sys\_scope

</td><td>

Unique identifier of the record that contains information about the scope of the social profile; Application \[sys\_scope\] table.Data type: Reference

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.channel.sys\_tags

</td><td>

System tags associated with the channel.Data type: String

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.channel.sys\_update\_name

</td><td>

Name of the person that last updated the social media profile channel.Data type: String

Maximum length: 250

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.channel.sys\_updated\_by

</td><td>

User that last updated the social media profile channel.Data type: String

Maximum length: 40

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.channel.sys\_updated\_on

</td><td>

Date and time the social media profile channel was last updated.Data type: Date/time

Maximum length: 40

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.consumer

</td><td>

For business-to-consumer cases. Details about the consumer associated with the case.Data type: Object

```
"consumer": {
  "active": Boolean,
  "business_phone": "String",
  "city": "String",
  "country": "String",
  "date_format": "String",
  "email": "String",
  "fax": "String",
  "first_name": "String",
  "gender": "String",
  "home_phone": "String",
  "household": "String",
  "last_name": "String",
  "middle_name": "String",
  "mobile_phone": "String",
  "name": "String",
  "notes": "String",
  "notification": Number,
  "number": "String",
  "photo": Image,
  "preferred_language": "String",
  "prefix": "String",
  "primary": Boolean,
  "state": "String",
  "street": "String",
  "suffix": "String",
  "sys_created_by": "String",
  "sys_created_on": "String",
  "sys_domain": "String",
  "sys_id": "String",
  "sys_mod_count": Number,
  "sys_tags": "String",
  "sys_updated_by": "String",
  "sys_updated_on": "String",
  "time_format": "String",
  "time_zone": "String",
  "title": "String",
  "user": "String",
  "zip": "String"
}
```

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.consumer.active

</td><td>

Flag that indicates whether the consumer is active.Possible values:

-   true: Consumer active
-   false: Consumer de-activated

Data type: Boolean

Default: true

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.consumer.business\_phone

</td><td>

Business phone number of the consumer.Data type: String

Maximum length: 40

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.consumer.city

</td><td>

City in which the consumer resides.Data type: String

Maximum length: 100

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.consumer.country

</td><td>

Country in which the consumer resides.Data type: String

Maximum length: 40

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.consumer.date\_format

</td><td>

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

sn\_app\_cs\_social\_social\_profile.consumer.email

</td><td>

Email address of the consumer.Data type: String

Maximum length: 100

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.consumer.fax

</td><td>

Fax number of the consumer.Data type: String

Maximum length: 40

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.consumer.first\_name

</td><td>

Consumer first name.Data type: String

Maximum length: 50

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.consumer.gender

</td><td>

Gender of the consumer.Data type: String

Maximum length: 40

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.consumer.home\_phone

</td><td>

Home phone number of the consumer.Data type: String

Maximum length: 40

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.consumer.household

</td><td>

Sys\_id of the record that describes the household characteristics.Data type: String

Table: Household \[csm\_household\]

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.consumer.last\_name

</td><td>

Consumer last name.Data type: String

Maximum length: 50

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.consumer.middle\_name

</td><td>

Consumer middle name.Data type: String

Maximum length: 50

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.consumer.mobile\_phone

</td><td>

Consumer mobile phone number.Data type: String

Maximum length: 40

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.consumer.name

</td><td>

Consumer full name; first\_name+middle\_name+last\_name.Data type: String

Maximum length: 152

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.consumer.notes

</td><td>

Notes on consumer.Data type: String

Maximum length: 4,000

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.consumer.notification

</td><td>

Indicates whether the consumer should receive notifications.Valid values:

-   1: Disabled
-   2: Enabled

Data type: Number \(Integer\)

Maximum length: 40

Default: 2

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.consumer.number

</td><td>

Unique number associated with the consumer.Data type: String

Maximum length: 40

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.consumer.photo

</td><td>

Photo of the consumer.Data type: Image

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.consumer.preferred\_language

</td><td>

Consumer primary language.Data type: String

Maximum length: 3

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.consumer.prefix

</td><td>

Consumer name prefix such as, Dr., Mr., Mrs., or Ms.Data type: String

Maximum length: 40

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.consumer.primary

</td><td>

Flag that indicates whether this is the primary consumer.Possible values:

-   true: Primary consumer
-   false: Not primary consumer

Data type: Boolean

Default: false

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.consumer.state

</td><td>

State in which the consumer resides.Data type: String

Maximum length: 100

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.consumer.street

</td><td>

Consumer street address.Data type: String

Maximum length: 255

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.consumer.suffix

</td><td>

Consumer name suffix such as Jr., Sr., or II.Data type: String

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.consumer.sys\_created\_by

</td><td>

User that created the consumer record.Data type: String

Maximum length: 40

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.consumer.sys\_created\_on

</td><td>

Date and time the consumer record was originally created.Data type: String

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.consumer.sys\_domain

</td><td>

ServiceNow domain in which the consumer information resides.Data type: String

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.consumer.sys\_id

</td><td>

Unique identifier for the consumer.Data type: String

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.consumer.sys\_mod\_count

</td><td>

Number of times that the associated consumer information has been modified.Data type: Number \(Integer\)

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.consumer.sys\_tags

</td><td>

Consumer system tags.

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.consumer.sys\_updated\_by

</td><td>

User that last updated the consumer information.Data type: String

Maximum length: 40

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.consumer.sys\_updated\_on

</td><td>

Date and time when the consumer information was last updated.Data type: String

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.consumer.time\_format

</td><td>

Format in which to display time.Valid values:

-   hh.mm.ss a: hh.mm.ss \(12 hour\)
-   hh:mm:ss a: hh:mm:ss \(12 hour\)
-   HH.mm.ss: hh.mm.ss \(24 hour\)
-   HH:mm:ss: hh:mm:ss \(24 hour\)

Data type: String

Maximum length: 40

Default: blank \(system time format\)

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.consumer.time\_zone

</td><td>

Consumer time zone, such as Canada/Central or US/Eastern.Data type: String

Maximum length: 40

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.consumer.title

</td><td>

Consumer business title such as Manager, Software Developer, or Contractor.Data type: String

Maximum length: 60

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.consumer.user

</td><td>

Sys\_id of the consumer user. Data type: String

Table: Consumer User \[csm\_consumer\_user\]

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.consumer.zip

</td><td>

Consumer zip code. Data type: String

Maximum length: 40

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact

</td><td>

For business-to-business cases. Unique identifier of the record containing details about the social media profile that belongs to the contact associated with the case. Located in the Contact \[customer\_contact\] table.Data type: String

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.account

</td><td>

Sys\_id of the account record to which the contact is associated.Data type: String

Table: Account \[customer\_account\]

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.active

</td><td>

Flag that indicates whether the contact is active within the system.Possible values:

-   true: Contact is active
-   false: Contact is inactive

Data type: Boolean

Default: true

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.agent\_status

</td><td>

Status of the agent.Possible values:

-   Off work
-   On break
-   On route
-   On site

Data type: String

Maximum length: 40

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.building

</td><td>

Sys\_id of the record that describes the building in which the contact resides.Data type: String

Table: Building \[cmn\_building\]

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.calendar\_integration

</td><td>

Calendar application that the contact uses.1: Outlook

Data type: Number \(Integer\)

Default: 1

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.city

</td><td>

City in which the contact resides.Data type: String

Maximum length: 40

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.company

</td><td>

Sys\_id of the company record to which the contact is associated.Data type: String

Table: Company \[core\_company\]

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.cost\_center

</td><td>

Sys\_id of the cost center associated with the contact.Data type: String

Table: Cost Center \[cmn\_cost\_center\]

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.country

</td><td>

Country code of the country in which the contact resides.Data type: String

Maximum length: 3

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.date\_format

</td><td>

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

sn\_app\_cs\_social\_social\_profile.contact.default\_perspective

</td><td>

Sys\_id of the default perspective for the contact.Data type: String

Table: Menu List \[sys\_perspective\]

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.department

</td><td>

Sys\_id of the department associated with the contact.Data type: String

Table: Department \[cmn\_department\]

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.edu\_status

</td><td>

Education status of the associated contact.Data type: String

Maximum length: 40

Default: faculty

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.email

</td><td>

Contact email address.Data type: String

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.employee\_number

</td><td>

Contact employee number.Data type: String

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.enable\_multifactor\_authn

</td><td>

Flag that indicates whether multifactor authorization is required for the contact to log in to the service portal.Possible values:

-   true: Multifactor authorization enabled
-   false: Multifactor authorization disabled

Data type: Boolean

Default: false

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.failed\_attempts

</td><td>

Number of failed log in attempts.Data type: Number \(Integer\)

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.first\_name

</td><td>

Contact first name.Data type: String

Maximum length: 50

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.gender

</td><td>

Contact gender.Data type: String

Maximum length: 40

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.geolocation\_tracked

</td><td>

Flag that indicates whether the contact location is obtained through geotracking.Possible values:

-   true: Contact location obtained through geotracking
-   false: Contact location not obtained through geotracking

Data type: Boolean

Default value: false

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.home\_phone

</td><td>

Contact home phone number.Data type: String

Maximum length: 40

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.internal\_itegration\_user

</td><td>

Flag that indicates whether the contact is an internal integration user.Possible values:

-   true: Internal integration user
-   false: Other type of user

Data type: Boolean

Default: false

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.introduction

</td><td>

IntroductionData type: String

Maximum length: 40

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.last\_login

</td><td>

Date on which the contact last logged into the system.Data type: String \(Date\)

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.last\_login\_device

</td><td>

Device the consumer used the last time they logged in to the system.Data type: String

Maximum length: 40

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.last\_login\_time

</td><td>

Date and time the contact logged in to the system.Data type: String \(Date/time\)

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.last\_name

</td><td>

Contact last name.Data type: String

Maximum length: 50

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.last\_position\_update

</td><td>

Date and time the last position was updated.Data type: String \(Date/time\)

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.latitude

</td><td>

Latitude coordinate of the contact.Data type: Number \(Floating point\)

Maximum length: 40

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.ldap\_server

</td><td>

Sys\_id of the LDAP server used by the contact to last log in to the system. Data type: String

Table: LDAP Server \[ldap\_server\_config\]

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.location

</td><td>

Sys\_id of the record that describes the location of the contactData type: String

Table: Location \[cmn\_location\]

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.locked\_out

</td><td>

Flag that indicates if the contact is locked-out.Possible values:

-   true: Contact locked-out
-   false: Contact not locked-out

Data type: Boolean

Default: false

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.longitude

</td><td>

Longitude coordinate of the contact.Data type: Number \(Floating point\)

Maximum length: 40

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.manager

</td><td>

Sys\_id of the record that describes the direct supervisor of the contact.Data type: String

Table: User \[sys\_user\]

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.middle\_name

</td><td>

Contact middle name.Data type: Number \(Floating point\)

Maximum length: 50

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.mobile\_phone

</td><td>

Contact mobile phone number.Data type: String

 Maximum length: 40

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.name

</td><td>

Contact full name.Data type: String

Maximum length: 151

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.notification

</td><td>

Indicates whether the contact should receive notifications.Valid values:

-   1: Disabled
-   2: Enabled

Data type: Number \(Integer\)

Default: 2

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.on\_schedule

</td><td>

Indicates the timeliness of dispatched service personnel.Valid values:

-   Ahead: Ahead of schedule.
-   behind\_less30: Behind schedule, but less than 30 minutes.
-   behind\_30to60: Behind schedule between 30 and 60 minutes.
-   behind\_more60: Behind schedule more than 60 minutes.
-   on\_time: On schedule.

Data type: String

Maximum length: 40

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.phone

</td><td>

Contact business phone number.Data type: String

Maximum length: 40

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.photo

</td><td>

Photo image of the contact. Data type: String

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.preferred\_language

</td><td>

Country code of the contact primary language.Data type: String

Maximum length: 3

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.roles

</td><td>

List of user roles associated with the contact.Data type: String

Maximum length: 40

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.schedule

</td><td>

Sys\_id of the record that describes the work schedule for the associated contact.Data type: String

Table: Schedule \[cmn\_schedule\]

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.source

</td><td>

Source of the contact.Data type: String

Maximum length: 255

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.state

</td><td>

State in which the contact resides.Data type: String

Maximum length: 40

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.street

</td><td>

Contact street address.Data type: String

Maximum length: 255

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.sys\_class\_name

</td><td>

Table that contains the contact record. Data type: String

Maximum length: 80

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.sys\_created\_by

</td><td>

User that originally created the associated contact record.Data type: String

Maximum length: 40

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.sys\_created\_on

</td><td>

Data and time the associated contact was originally created.Data type: String \(Date/time\)

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.sys\_domain

</td><td>

ServiceNow instance domain of the associated contact record.Data type: String

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.sys\_domain\_path

</td><td>

Contact record domain path.Data type: String

Maximum length: 255

Default: / \(global\)

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.sys\_id

</td><td>

Unique identifier for the associated contact record.Data type: String

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.sys\_mod\_count

</td><td>

Number of times that the associated contact record has been modified.Data type: Number \(Integer\)

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.sys\_tags

</td><td>

Contact system tags.

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.sys\_updated\_by

</td><td>

User that last updated the associated contact information.Data type: String

Maximum length: 40

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.sys\_updated\_on

</td><td>

Data and time the associated contact information was updated.Data type: String \(Date/time\)

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.time\_format

</td><td>

Format in which to display time.Valid values:

-   hh.mm.ss a: hh.mm.ss \(12 hour\)
-   hh:mm:ss a: hh:mm:ss \(12 hour\)
-   HH.mm.ss: hh.mm.ss \(24 hour\)
-   HH:mm:ss: hh:mm:ss \(24 hour\)

Data type: String

Maximum length: 40

Default: Blank \(system time format\)

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.time\_sheet\_policy

</td><td>

Sys\_id of the record that contains the time sheet policy for the associated contact.Data type: String

Table: Time Sheet Policy \[time\_sheet\_policy\]

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.time\_zone

</td><td>

Time zone in which the contact resides, such as Canada/Central or US/Eastern.Data type: String

Maximum length: 40

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.title

</td><td>

Contact business title such as Manager, Software Developer, or Contractor.Data type: String

Maximum length: 60

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.user\_name

</td><td>

Contact user ID.Data type: String

Maximum length: 40

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.vip

</td><td>

Flag that indicates whether the associated contact has VIP status.Possible values:

-   true: VIP
-   false: Not VIP

Data type: Boolean

Default: false

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.web\_service\_access\_only

</td><td>

Flag that indicates whether the contact can only access services through the web.Possible values:

-   true: Web access only
-   false: Access through all available methods

Data type: Boolean

Default: false

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.zip

</td><td>

Contact zip code.Data type: String

Maximum length: 40

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.created\_on

</td><td>

Date and time the associated social media profile was initially created.

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.profile

</td><td>

Social profile.Data type: String

 Maximum length: 255

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.profile\_url

</td><td>

URL to use to access the social media profile.Data type: String

 Maximum length: 1,024

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.social\_id

</td><td>

Unique social media account provider identifier for the associated social media account.Data type: String

 Maximum length: 100

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.source

</td><td>

Source of the social profile.Data type: String

 Maximum length: 255

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.sys\_created\_by

</td><td>

User that initially created the social media profile.Data type: String

 Maximum length: 40

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.sys\_created\_on

</td><td>

Date and time the social media profile was initially created.Data type: String \(Date/time\)

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.sys\_id

</td><td>

Unique identifier for the social media profile.Data type: String

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.sys\_mod\_count

</td><td>

Number of times that information was modified for the associated social media profile.Data type: Number \(Integer\)

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.sys\_tags

</td><td>

Profile system tags.

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.sys\_updated\_by

</td><td>

User that initially created the social media profile.Data type: String

 Maximum length: 40

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.sys\_updated\_on

</td><td>

User that initially created the social media profile.Data type: String

 Maximum length: 40

</td></tr><tr><td>

state

</td><td id="casetable-state-entry">

Current state of the case.Possible values:

-   1: New
-   3: Closed
-   6: Resolved
-   10: Open
-   18: Awaiting Info

Data type: Number \(Integer\)

Default: 1

</td></tr><tr><td>

subcategory

</td><td id="casetable-subcategory-entry">

Case subcategory.Possible values:

0: QuestionData type: Number \(Integer\)

Default: 0

</td></tr><tr><td>

support\_manager

</td><td id="casetable-support_manager-entry">

Sys\_id of the CSM manager assigned to the case.Data type: String

Table: User \[sys\_user\]

</td></tr><tr><td>

sync\_driver

</td><td id="casetable-sync_driver-entry">

Flag that indicates whether there's driver synchronization.Possible values:

-   true: Driver is synchronized
-   false: Driver isn't synchronized

Data type: Boolean

</td></tr><tr><td>

sys\_class\_name

</td><td id="casetable-sys_class_name-entry">

Table that contains the case record.Data type: String

Maximum length: 80

</td></tr><tr><td>

sys\_created\_by

</td><td id="casetable-sys_created_by-entry">

Person that initially opened the case.Data type: String

Maximum length: 40

</td></tr><tr><td>

sys\_created\_on

</td><td id="casetable-sys_created_on-entry">

Date and time when the case was initially created.Data type: String

</td></tr><tr><td>

sys\_domain

</td><td id="casetable-sys_domain-entry">

Domain associated with the case.Data type: String

Maximum length: 32

Default: global

</td></tr><tr><td>

sys\_domain\_path

</td><td id="casetable-sys_domain_path-entry">

Domain path.Data type: String

Maximum length: 255

Default: /

</td></tr><tr><td>

sys\_id

</td><td id="casetable-sys_sys_id-entry">

Unique identifier for the case.Data type: String

Maximum length: 32

</td></tr><tr><td>

sys\_mod\_count

</td><td id="casetable-sys_mod_count-entry">

Number of updates to the case since it was initially created.Data type: Number \(Integer\)

</td></tr><tr><td>

sys\_tags

</td><td>

System tags.

</td></tr><tr><td>

sys\_updated\_by

</td><td id="casetable-sys_updated_by-entry">

Person that last updated the case.Data type: String

Maximum length: 40

</td></tr><tr><td>

sys\_updated\_on

</td><td id="casetable-sys_updated_on-entry">

Date and time when the case was last updated.Data type: String

</td></tr><tr><td>

time\_worked

</td><td id="casetable-time_worked-entry">

Total amount of time worked on the case.Data type: String

</td></tr><tr><td>

upon\_approval

</td><td id="casetable-upon_approval-entry">

Action to take if the case is approved.Possible values:

-   do\_nothing
-   proceed

Data type: String

Maximum length: 40

Default: proceed

</td></tr><tr><td>

upon\_reject

</td><td id="casetable-upon_reject-entry">

Action to take if the case is rejected.Possible values:

-   cancel
-   goto

Data type: String

Maximum length: 40

Default: cancel

</td></tr><tr><td>

urgency

</td><td id="casetable-urgency-entry">

Urgency of the case.Possible values:

-   1: High
-   2: Medium
-   3: Low

Data type: Number \(Integer\)

Default: 3

</td></tr><tr><td>

user\_input

</td><td id="casetable-user_input-entry">

Additional user input.Data type: String

Maximum length: 4,000

</td></tr><tr><td>

variable\_pool

</td><td>

Grouping of variables.

</td></tr><tr><td>

variables

</td><td id="casetable-variables-entry">

Name-value pairs of variables associated with the case.Data type: String

Maximum length: 40

</td></tr><tr><td>

watch\_list

</td><td id="casetable-watch_list-entry">

List of sys\_ids of the users who receive notifications about this case when additional comments are added or if the state of a case is changed to Resolved or Closed.Data type: Array

Table: User \[sys\_user\]

</td></tr><tr><td>

wf\_activity

</td><td id="casetable-wf_activity-entry">

Sys\_id of the workflow activity record associated with the case.Data type: String

Table: Workflow Activity \[wf\_activity\]

</td></tr><tr><td>

work\_end

</td><td id="casetable-work_end-entry">

Date and time work ended on the case.Data type: String

</td></tr><tr><td>

work\_notes

</td><td id="casetable-work_notes-entry">

Information about how to resolve the case, or steps taken to resolve it.Data type: String

Maximum length: 4,000

</td></tr><tr><td>

work\_notes\_list

</td><td id="casetable-work_notes_list-entry">

List of sys\_ids of the internal users who receive notifications about this case when work notes are added.Data type: Array

Table: User \[sys\_user\]

</td></tr><tr><td>

work\_start

</td><td id="casetable-work_start-entry">

Date and time that work started on the case.Data type: String

</td></tr></tbody>
</table>### cURL request

```
curl "https://instance.servicenow.com/api/sn_customerservice/case/ba325dbe64f01300964fae39b050e9a6" \
--request GET \
--header "Accept:application/json" \
--user "username":"password"

```

```
{
  "result": {
    "parent": "",
    "caused_by": "",
    "watch_list": "",
    "active_escalation": "",
    "upon_reject": "cancel",
    "sys_updated_on": "2018-06-18 00:14:43",
    "support_manager": "",
    "approval_history": "",
    "skills": "",
    "number": "CS0000871",
    "problem": "",
    "state": "10",
    "case": "Acme Analytics performance degradation​CS0000871",
    "sys_created_by": "john.jason",
    "knowledge": "false",
    "order": "",
    "cmdb_ci": "",
    "delivery_plan": "",
    "impact": "3",
    "contract": "",
    "active": "true",
    "work_notes_list": "",
    "auto_created_case": "false",
    "priority": "1",
    "sys_domain_path": "/",
    "rejection_goto": "",
    "first_response_time": "",
    "business_duration": "",
    "group_list": "",
    "child_case_creation_progress": "false",
    "sync_driver": "false",
    "approval_set": "",
    "wf_activity": "",
    "short_description": "Acme Analytics performance degradation",
    "correlation_display": "",
    "delivery_task": "",
    "work_start": "",
    "recipient_list": "",
    "additional_assignee_list": "",
    "notify": "1",
    "sys_class_name": "sn_customerservice_case",
    "closed_by": "",
    "follow_up": "",
    "contact_local_time": "",
    "sn_app_cs_social_social_profile": "",
    "reassignment_count": "0",
    "contact_time_zone": "",
    "notes_to_comments": "false",
    "assigned_to": "da419c1fc312310015519f2974d3ae15",
    "product": "4c84a024c3211200bb779f2974d3aef6",
    "variables": "",
    "variable_pool": "",
    "hierarchical_variables": "variable_pool",
    "sla_due": "",
    "change": "",
    "comments_and_work_notes": "",
    "partner": "",
    "escalation": "0",
    "upon_approval": "proceed",
    "partner_contact": "",
    "correlation_id": "",
    "asset": "",
    "made_sla": "true",
    "resolved_by": "",
    "sys_updated_by": "john.jason",
    "opened_by": "da419c1fc312310015519f2974d3ae15",
    "user_input": "",
    "sys_created_on": "2018-06-18 00:14:39",
    "contact": "",
    "sys_domain": "global",
    "closed_at": "",
    "follow_the_sun": "false",
    "entitlement": "",
    "business_service": "",
    "business_impact": "Acme Anaytics performance is extremely slow. Customers are not able to use it. ",
    "time_worked": "",
    "expected_start": "",
    "opened_at": "2018-06-18 00:14:39",
    "work_end": "",
    "resolved_at": "",
    "case_report": "27329dbe64f01300964fae39b050e93c",
    "subcategory": "0",
    "work_notes": "",
    "assignment_group": "",
    "cause": "",
    "description": "",
    "calendar_duration": "",
    "close_notes": "",
    "sys_id": "ba325dbe64f01300964fae39b050e9a6",
    "contact_type": "web",
    "resolution_code": "",
    "probable_cause": "",
    "urgency": "3",
    "company": "",
    "major_case_state": "accepted",
    "consumer": "",
    "activity_due": "",
    "comments": "",
    "approval": "not requested",
    "due_date": "",
    "sys_mod_count": "2",
    "sys_tags": "",
    "active_account_escalation": "",
    "location": "",
    "category": "1",
    "account": ""
  }
}
```

## Case - GET /sn\_customerservice/case

Retrieves a specified set of Customer Service Management \(CSM\) cases.

To use this endpoint, users must have the csm\_ws\_integration, sn\_customerservice.customer, or sn\_customerservice.consumer role.

**Note:** You can reference all sysparm query parameters using either their full name or their shortened name \(without the **sysparm\_** prefix\). For example, for **sysparm\_limit** you can also use **limit**.

### URL format

Versioned URL: `/api/sn_customerservice/{api_version}/case`

Default URL: `/api/sn_customerservice/case`

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td>

Optional. Version of the endpoint to access. For example, `v1` or `v2`. Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sysparm\_display\_value

</td><td>

Data retrieval operation for reference and choice fields.Based on this value, retrieves the display value and/or the actual value from the database.

Data type: String

Valid values:

-   true: Returns the display values for all fields
-   false: Returns the actual values from the database
-   all: Returns both actual and display values

Default: false

**Note:** There is no preferred method for setting this parameter. However, specifying the display value may cause performance issues since it is not reading directly from the database and may include referencing other fields and records. For more information on display values and actual values, see [Table API FAQs \(KB0534905\).](https://support.servicenow.com/kb_view.do?sysparm_article=KB0534905)

</td></tr><tr><td>

sysparm\_fields

</td><td id="sysparm_fields_entry-RESTAPI">

Comma-separated list of fields to return in the response. Invalid fields are ignored.Data type: String

Default: Return all fields.

</td></tr><tr><td>

sysparm\_limit

</td><td>

Maximum number of records to return. Unusually large **sysparm\_limit** values can impact system performance. For requests that exceed this number of records, use the **sysparm\_offset** parameter to paginate record retrieval. Data type: Number

</td></tr><tr><td>

sysparm\_offset

</td><td>

Starting record index for which to begin retrieving records. Use this value to paginate record retrieval. This functionality enables the retrieval of all records, regardless of the number of records, in small manageable chunks. For example, the first time you call this endpoint, **sysparm\_offset** is set to "0". To simply page through all available records, use `sysparm_offset=sysparm_offset+sysparm_limit`, until you reach the end of all records.

Do not pass a negative number in the **sysparm\_offset** parameter.Data type: Number

Default: 0

</td></tr><tr><td>

sysparm\_query

</td><td>

Encoded query used to filter the result set.For example:

`(sysparm_query=caller_id=javascript:gs.getUserID()^active=true)`

The encoded query supports order by. To sort responses based on certain fields, use the ORDERBY and ORDERBYDESC clauses in **sysparm\_query**. For example, `sysparm_query=active=true^ORDERBYnumber^ORDERBYDESCcategory` filters all active records and orders the results in ascending order by number first, and then in descending order by category.

If part of the query is invalid, such as by specifying an invalid field name, the instance ignores the invalid part. It then returns rows using only the valid portion of the query. You can control this behavior using the property **glide.invalid\_query.returns\_no\_rows**. Set this property to true to return no rows on an invalid query.

**Note:** The **glide.invalid\_query.returns\_no\_rows** property controls the behavior of all queries across the instance, such as in lists, scripts \(GlideRecord.query\(\)\), and web service APIs.

Data type: String

</td></tr><tr><td>

sysparm\_reference\_fields

</td><td>

Whether or not to retrieve fields from reference tables such as account, contact, consumer, and sn\_app\_cs\_social\_social\_profile. By default, these fields are returned if the user has read access to them, but this adds performance overhead. When retrieving a large number of case records, this overhead can be eliminated by setting `sysparm_reference_fields=false`.Data type: Boolean

 Default: true

 **Note:** When using this endpoint, you can omit the **sysparm\_** prefix for this query parameter and specify it as **reference\_fields**.

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
</table><table class="rest_api_response_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Link

</td><td>

REST response data can be split into multiple result sets. Where applicable, the response header contains different links for the first set, previous set, next set, and the last set of records.For example:

`https://<instance name>.service-now.com/api/now/table/cmdb_ci?sysparm_offset=40&sysparm_limit=1000>;rel="next"`,

`https://<instance name>.service-now.com/api/now/table/cmdb_ci?sysparm_offset=40&sysparm_limit=1000>;rel="prev"`,

`https://<instance name>.service-now.com/api/now/table/cmdb_ci?sysparm_offset=0&sysparm_limit=1000>;rel="first"`,

`https://<instance name>.service-now.com/api/now/table/cmdb_ci?sysparm_offset=2780&sysparm_limit=1000>;rel="last"`

</td></tr><tr><td id="x-total-count-response-entry-RESTAPI">

X-Total-Count

</td><td>

Response header showing the total number of records matching the request when the **sysparm\_limit** or **sysparm\_offset** query parameters are specified.

</td></tr></tbody>
</table>### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|500|Internal Server Error. A logic error on the server-side code occurred.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Element

</th><th>

Description

</th></tr></thead><tbody><tr><td>

account

</td><td id="casetable-account-entry">

Sys\_id of the account record associated with the case.

Data type: String

Table: Account \[customer\_account\]

</td></tr><tr><td>

account

</td><td>

Account details.Data type: Object

```
"account": {
  "account_code": "String",
  "account_parent": "String",
  "account_path": "String",
  "active_escalation": "String",
  "apple_icon": Image,
  "banner_image": Image,
  "banner_image_light": Image,
  "banner_text": "String",
  "city": "String",
  "contact": "String",
  "country": "String",
  "customer": "String",
  "discount": "String",
  "fax_phone": "String",
  "fiscal_year": "String",
  "lat_long_error": "String",
  "latitude": "String",
  "longitude": "String",
  "market_cap": "String",
  "name": "String",
  "notes": "String",
  "num_employees": Number,
  "number": "String",
  "parent": "String",
  "partner": "String",
  "phone": "String",
  "primary": Boolean,
  "primary_contact": "String",
  "profits": Number,
  "publicly_traded": Boolean,
  "rank_tier": "String",
  "registration_code": "String",
  "revenue_per_year": Number,
  "state": "String",
  "stock_price": "String",
  "stock_symbol": "String",
  "street": "String",
  "sys_class_name": "String",
  "sys_created_by": "String",
  "sys_created_on": "String",
  "sys_id": "String",
  "sys_mod_count": Number,
  "sys_updated_by": "String",
  "sys_updated_on": "String",
  "theme": "String",
  "vendor": Boolean,
  "vendor_manager": "String",
  "vendor_type": "String",
  "website": "String",
  "zip": "String
}
```

</td></tr><tr><td>

account.account\_code

</td><td>

Unique combination of values that an application uses to identify budget forecasts and budget plans.Data type: String

Maximum length: 255

</td></tr><tr><td>

account.account\_parent

</td><td>

Sys\_id of the parent account of this account. Located in the Account \[customer\_account\] table.Data type: String

</td></tr><tr><td>

account.account\_path

</td><td>

Path from the parent to the child accounts in the account hierarchy.Data type: String

Maximum length: 255

</td></tr><tr><td>

account.active\_escalation

</td><td>

Sys\_id of the active escalation associated with the account.Data type: String

Table: Escalation \[sn\_customerservice\_escalation\]

</td></tr><tr><td>

account.apple\_icon

</td><td>

Icon for iPhone home page bookmarks.Data type: Image

</td></tr><tr><td>

account.banner\_image

</td><td>

Banner image that appears on the customer portal.Data type: Image

</td></tr><tr><td>

account.banner\_image\_light

</td><td>

Small banner image.Data type: Image

</td></tr><tr><td>

account.banner\_text

</td><td>

Banner text that appears on the customer portal.Data type: String

Maximum length: 4,000

</td></tr><tr><td>

account.city

</td><td>

City in which the company that is associated with this account resides.Data type: String

Maximum length: 50

</td></tr><tr><td>

account.contact

</td><td>

Sys\_id of a contact record associated with this account.Data type: String

Table: User \[sys\_user\]

</td></tr><tr><td>

account.country

</td><td>

Country in which the company that is associated with this account resides.Data type: String

Maximum length: 40

Default: USA

</td></tr><tr><td>

account.customer

</td><td>

Flag that indicates whether the account is a customer account, as opposed to a partner account.Possible values:

-   true: Customer account
-   false: Partner account

Data type: Boolean

Default: false

</td></tr><tr><td>

account.discount

</td><td>

Discount given to the account on purchases.Data type: Number

Maximum length: 15

</td></tr><tr><td>

account.fax\_phone

</td><td>

Primary fax phone number for the company associated with this account.Data type: String

Maximum length: 40

</td></tr><tr><td>

account.fiscal\_year

</td><td>

Fiscal year for the company associated with the account.Data type: String

</td></tr><tr><td>

account.lat\_long\_error

</td><td>

Difference in the actual location as compared to latitude and longitude information.Data type: String

Maximum length: 1,000

</td></tr><tr><td>

account.latitude

</td><td>

Latitude of the company associated with this account.Data type: Number \(floating point number\)

Maximum length: 40

</td></tr><tr><td>

account.longitude

</td><td>

Longitude of the company associated with this account.Data type: Number \(floating point number\)

Maximum length: 40

</td></tr><tr><td>

account.manufacturer

</td><td>

Flag that indicates whether the company associated with this account manufactures goods.Possible values:

-   true: Manufactures goods
-   false: Does not manufacture goods

Data type: Boolean

Default: false

</td></tr><tr><td>

account.market\_cap

</td><td>

Market value of the associated company's publicly traded stock shares.Data type: Number \(currency\)

Maximum length: 20

</td></tr><tr><td>

account.name

</td><td>

Name of the company associated with this account.Data type: String

Maximum length: 80

</td></tr><tr><td>

account.notes

</td><td>

Additional information about the company.Data type: String

Maximum length: 4,000

</td></tr><tr><td>

account.num\_employees

</td><td>

Number of people employed by the company.Data type: Number \(Integer\)

Maximum length: 40

</td></tr><tr><td>

account.number

</td><td>

Number that identifies this account.Data type: String

Maximum length: 40

</td></tr><tr><td>

account.parent

</td><td>

Sys\_id of the parent account of this account.Data type: String

Table: Company \[core\_company\]

</td></tr><tr><td>

account.partner

</td><td>

Flag that indicates whether the account is a partner account or a customer account.Possible values:

-   true: Partner account
-   false: Customer account

Data type: Boolean

Default: false

</td></tr><tr><td>

account.phone

</td><td>

Primary phone number for the company.Data type: String

</td></tr><tr><td>

account.primary

</td><td>

Flag that indicates whether this is a primary account.Possible values:

-   true: Primary account
-   false: Secondary account

Data type: Boolean

Default: false

</td></tr><tr><td>

account.primary\_contact

</td><td>

Sys\_id of the primary contact for the account.Data type: String

Table: Contact \[customer\_contact\]

</td></tr><tr><td>

account.profits

</td><td>

Profit information entered for this account.Data type: Number \(Currency\)

Maximum length: 40

</td></tr><tr><td>

account.publicly\_traded

</td><td>

Flag that indicates whether the company associated with this account is publicly traded on the stock exchange.Possible values:

-   true: Publicly traded
-   false: Private company

Data type: Boolean

</td></tr><tr><td>

account.rank\_tier

</td><td>

Type of account.Possible values:

-   blacklist
-   other
-   strategic
-   tactical
-   valued

Data type: String

Maximum length: 40

</td></tr><tr><td>

account.registration\_code

</td><td>

Unique code that customers use when requesting a login on the customer portal. This code provides a method for validating the customer on the company before granting access.Data type: String

Maximum length: 40

</td></tr><tr><td>

account.revenue\_per\_year

</td><td>

Revenue produced by the company associated with this account.Data type: Number \(Currency\)

Maximum length: 20

</td></tr><tr><td>

account.state

</td><td>

State in which the company resides.Data type: String

Maximum length: 40

</td></tr><tr><td>

account.stock\_price

</td><td>

Price of the company stock.Data type: String

Maximum length: 40

</td></tr><tr><td>

account.stock\_symbol

</td><td>

Stock symbol of the company.Data type: String

Maximum length: 40

</td></tr><tr><td>

account.street

</td><td>

Street address of the company.Data type: String

Maximum length: 255

</td></tr><tr><td>

account.sys\_class\_name

</td><td>

Table that contains the associated account record.Data type: String

</td></tr><tr><td>

account.sys\_created\_by

</td><td>

User that originally created the account.Data type: String

Maximum length: 40

</td></tr><tr><td>

account.sys\_created\_on

</td><td>

Date and time that the account was originally created.Data type: String

</td></tr><tr><td>

account.sys\_id

</td><td>

Sys\_id for the account record.Data type: String

</td></tr><tr><td>

account.sys\_mod\_count

</td><td>

Number of times the account information has been updated.Data type: Number \(Integer\)

</td></tr><tr><td>

account.sys\_updated\_by

</td><td>

User that last modified the account information.Data type: String

Maximum length: 40

</td></tr><tr><td>

account.sys\_updated\_on

</td><td>

Date and time the account information was last updated.Data type: String

</td></tr><tr><td>

account.theme

</td><td>

Sys\_id of the customer portal theme used by this account.Data type: String

Table: Theme \[sys\_ui\_theme\]

</td></tr><tr><td>

account.vendor

</td><td>

Flag that indicates whether the company associated with this account is a vendor.Possible values:

-   true: Vendor
-   false: Not a vendor

Data type: Boolean

Default: false

</td></tr><tr><td>

account.vendor\_manager

</td><td>

List of sys\_ids of the vendor managers for the account.Data type: String

Table: User \[sys\_user\]

</td></tr><tr><td>

account.vendor\_type

</td><td>

List of sys\_ids of the type of vendor such as, applications, hardware, services, or software.Data type: String

Table: Vendor Type \[vendor\_type\]

</td></tr><tr><td>

account.website

</td><td>

URL of the website for the company.Data type: String

Maximum length: 1,024

</td></tr><tr><td>

account.zip

</td><td>

Zip code of the company.Data type: String

Maximum length: 40

</td></tr><tr><td>

active

</td><td id="casetable-active-entry">

Flag that indicates whether the case is open and active.Possible values:

-   true: Case is active
-   false: Case is closed

Data type: Boolean

Default: true

</td></tr><tr><td>

active\_account\_escalation

</td><td id="casetable-active_account_escalation-entry">

Sys\_id of the active account escalation record associated with the case.Data type: String

Table: Escalation \[sn\_customerservice\_escalation\]

</td></tr><tr><td>

active\_escalation

</td><td id="casetable-active_escalation-entry">

Sys\_id of the active escalation record associated with the case.Data type: String

Table: Escalation \[sn\_customerservice\_escalation\]

</td></tr><tr><td>

activity\_due

</td><td id="casetable-activity_due-entry">

Date for which the associated case is expected to be completed.Data type: String

</td></tr><tr><td>

additional\_assignee\_list

</td><td id="casetable-additional_assignee_list-entry">

List of the sys\_ids of the additional persons \(other than the primary assignee\) that have been assigned to the account.Data type: Array

Maximum: 4,000

Table: User \[sys\_user\]

</td></tr><tr><td>

approval

</td><td id="casetable-approval-entry">

String that describes the type of approval required.Possible values:

-   approved
-   cancelled
-   duplicate
-   not\_required
-   not requested
-   rejected
-   requested

Data type: String

Maximum characters: 40

Default: not requested

</td></tr><tr><td>

approval\_history

</td><td id="casetable-approval_history-entry">

List of all approvals associated with the case.Data type: String

Maximum characters: 4,000

</td></tr><tr><td>

approval\_set

</td><td id="casetable-approval_set-entry">

Date and time that the associated action was approved.Data type: String

</td></tr><tr><td>

asset

</td><td id="casetable-asset-entry">

Sys\_id of the asset record associated with the case.Data type: String

Table: Asset \[alm\_asset\]

</td></tr><tr><td>

assigned\_to

</td><td id="casetable-assigned_to-entry">

Sys\_id of the person assigned to the case.

Table: User \[sys\_user\]

 Data type: String

</td></tr><tr><td>

assignment\_group

</td><td id="casetable-aassignment_group-entry">

Sys\_id of the customer service agent group assigned to the case.Data type: String

Table: Group \[sys\_user\_group\]

</td></tr><tr><td>

business\_duration

</td><td id="casetable-business_duration-entry">

Length in calendar work hours, work days, and work weeks that it took to complete the case.Data type: String

</td></tr><tr><td>

business\_impact

</td><td id="casetable-business_impact-entry">

Impact of the issue on the associated customer.Data type: String

Maximum characters: 4,000

</td></tr><tr><td>

business\_service

</td><td id="casetable-business_service-entry">

Sys\_id of the service record associated with the case.Data type: String

Table: Service \[cmdb\_ci\_service\]

</td></tr><tr><td>

case

</td><td id="casetable-case-entry">

Case short description and case number.Data type: String

Maximum length: 300

</td></tr><tr><td>

case\_report

</td><td id="casetable-case_report-entry">

Sys\_id of the associated case report.Data type: String

Table: Case Report \[sn\_customerservice\_case\_report\]

</td></tr><tr><td>

category

</td><td id="casetable-category-entry">

Case category.Possible values:

-   0: Question
-   1: Issue
-   2: Feature

Data type: Number \(Integer\)

Default: 1

</td></tr><tr><td>

cause

</td><td id="casetable-cause-entry">

Details about the cause of the problem.Data type: String

Maximum length: 4,000

</td></tr><tr><td>

caused\_by

</td><td id="casetable-caused_by-entry">

Sys\_id of the change request that caused the case to be created.Data type: String

Table: Change Request \[change\_request\]

</td></tr><tr><td>

change

</td><td id="casetable-change-entry">

Sys\_id of the change request that caused the case to be created.Data type: String

Table: Change Request \[change\_request\]

</td></tr><tr><td>

child\_case\_creation\_progress

</td><td id="casetable-child_case_creation_progress-entry">

Flag that indicates whether the case is a child case that was created from a major case.Possible values:

-   true: Child case created from a major case
-   false: Not a child case

Data type: Boolean

</td></tr><tr><td>

closed\_at

</td><td id="casetable-closed_at-entry">

Date and time that the case was closed.Data type: String

</td></tr><tr><td>

closed\_by

</td><td id="casetable-closed_by-entry">

Sys\_id of the user that closed the case.Data type: String

Table: User \[sys\_user\]

</td></tr><tr><td>

close\_notes

</td><td id="casetable-close_notes-entry">

Notes made when the case was closed.Data type: String

Maximum length: 4,000

</td></tr><tr><td>

cmdb\_ci

</td><td id="casetable-cmdb_ci-entry">

Sys\_id of the configuration item associated with the case.Data type: String

Table: Configuration Item \[cmdb\_ci\]

</td></tr><tr><td>

comments

</td><td id="casetable-comments-entry">

Additional comments about the case.Data type: String

Maximum length: 4,000

</td></tr><tr><td>

comments\_and\_work\_notes

</td><td id="casetable-comments_and_work_notes-entry">

Comments and work notes entered for the case.Data type: String

Maximum length: 4,000

</td></tr><tr><td>

company

</td><td id="casetable-company-entry">

Sys\_id of the company associated with the case.Data type: String

Table: Company \[core\_company\]

</td></tr><tr><td>

consumer

</td><td id="casetable-consumer-entry">

Business-to-consumer cases only. Sys\_id of the person to contact with regard to this case.Data type: String

Table: Consumer \[csm\_consumer\]

</td></tr><tr><td>

consumer

</td><td>

Array of parameters for business-to-consumer cases.

</td></tr><tr><td>

consumer.active

</td><td>

Flag that indicates whether the consumer is active.Possible values:

-   true: Consumer active
-   false: Consumer de-activated

Data type: Boolean

Default: true

</td></tr><tr><td>

consumer.business\_phone

</td><td>

Business phone number of the consumer.Data type: String

Maximum length: 40

</td></tr><tr><td>

consumer.city

</td><td>

City in which the consumer resides.Data type: String

Maximum length: 100

</td></tr><tr><td>

consumer.country

</td><td>

Country in which the consumer resides.Data type: String

Maximum length: 40

</td></tr><tr><td>

consumer.date\_format

</td><td>

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

consumer.email

</td><td>

Email address of the consumer.Data type: String

Maximum length: 100

</td></tr><tr><td>

consumer.fax

</td><td>

Fax number of the consumer.Data type: String

Maximum length: 40

</td></tr><tr><td>

consumer.first\_name

</td><td>

Consumer first name.Data type: String

Maximum length: 50

</td></tr><tr><td>

consumer.gender

</td><td>

Gender of the consumer.Data type: String

Maximum length: 40

</td></tr><tr><td>

consumer.home\_phone

</td><td>

Home phone number of the consumer.Data type: String

Maximum length: 40

</td></tr><tr><td>

consumer.household

</td><td>

Sys\_id of the record that describes the household characteristics.Data type: String

Table: Household \[csm\_household\]

</td></tr><tr><td>

consumer.last\_name

</td><td>

Consumer last name.Data type: String

Maximum length: 50

</td></tr><tr><td>

consumer.middle\_name

</td><td>

Consumer middle name.Data type: String

Maximum length: 50

</td></tr><tr><td>

consumer.mobile\_phone

</td><td>

Consumer mobile phone number.Data type: String

Maximum length: 40

</td></tr><tr><td>

consumer.name

</td><td>

Consumer full name; first\_name+middle\_name+last\_name.Data type: String

Maximum length: 152

</td></tr><tr><td>

consumer.notes

</td><td>

Notes on consumer.Data type: String

Maximum length: 4,000

</td></tr><tr><td>

consumer.notification

</td><td>

Indicates whether the consumer should receive notifications.Valid values:

-   1: Disabled
-   2: Enabled

Data type: Number \(Integer\)

Maximum length: 40

Default: 2

</td></tr><tr><td>

consumer.number

</td><td>

Unique number associated with the consumer.Data type: String

Maximum length: 40

</td></tr><tr><td>

consumer.photo

</td><td>

Photo of the consumer.Data type: Image

</td></tr><tr><td>

consumer.preferred\_language

</td><td>

Consumer primary language.Data type: String

Maximum length: 3

</td></tr><tr><td>

consumer.prefix

</td><td>

Consumer name prefix such as, Dr., Mr., Mrs., or Ms.Data type: String

Maximum length: 40

</td></tr><tr><td>

consumer.primary

</td><td>

Flag that indicates whether this is the primary consumer.Possible values:

-   true: Primary consumer
-   false: Not primary consumer

Data type: Boolean

Default: false

</td></tr><tr><td>

consumer.state

</td><td>

State in which the consumer resides.Data type: String

Maximum length: 100

</td></tr><tr><td>

consumer.street

</td><td>

Consumer street address.Data type: String

Maximum length: 255

</td></tr><tr><td>

consumer.suffix

</td><td>

Consumer name suffix such as Jr., Sr., or II.Data type: String

</td></tr><tr><td>

consumer.sys\_created\_by

</td><td>

User that created the consumer record.Data type: String

Maximum length: 40

</td></tr><tr><td>

consumer.sys\_created\_on

</td><td>

Date and time the consumer record was originally created.Data type: String

</td></tr><tr><td>

consumer.sys\_domain

</td><td>

ServiceNow domain in which the consumer information resides.Data type: String

</td></tr><tr><td>

consumer.sys\_id

</td><td>

Unique identifier for the consumer.Data type: String

</td></tr><tr><td>

consumer.sys\_mod\_count

</td><td>

Number of times that the associated consumer information has been modified.Data type: Number \(Integer\)

</td></tr><tr><td>

consumer.sys\_updated\_by

</td><td>

User that last updated the consumer information.Data type: String

Maximum length: 40

</td></tr><tr><td>

consumer.sys\_updated\_on

</td><td>

Date and time when the consumer information was last updated.Data type: String

</td></tr><tr><td>

consumer.time\_format

</td><td>

Format in which to display time.Valid values:

-   hh.mm.ss a: hh.mm.ss \(12 hour\)
-   hh:mm:ss a: hh:mm:ss \(12 hour\)
-   HH.mm.ss: hh.mm.ss \(24 hour\)
-   HH:mm:ss: hh:mm:ss \(24 hour\)

Data type: String

Maximum length: 40

Default: blank \(system time format\)

</td></tr><tr><td>

consumer.time\_zone

</td><td>

Consumer time zone, such as Canada/Central or US/Eastern.Data type: String

Maximum length: 40

</td></tr><tr><td>

consumer.title

</td><td>

Consumer business title such as Manager, Software Developer, or Contractor.Data type: String

Maximum length: 60

</td></tr><tr><td>

consumer.user

</td><td>

Sys\_id of the consumer user. Data type: String

Table: Consumer User \[csm\_consumer\_user\]

</td></tr><tr><td>

consumer.zip

</td><td>

Consumer zip code. Data type: String

Maximum length: 40

</td></tr><tr><td>

contact

</td><td id="casetable-contact-entry">

Business-to-business based cases only. Sys\_id of the person to contact regarding this case.Data type: String

Table: Contact \[customer\_contact\]

</td></tr><tr><td>

contact

</td><td>

Array of contact parameters for business-to-business cases.

</td></tr><tr><td>

contact.account

</td><td>

Sys\_id of the account record to which the contact is associated.Data type: String

Table: Account \[customer\_account\]

</td></tr><tr><td>

contact.active

</td><td>

Flag that indicates whether the contact is active within the system.Possible values:

-   true: Contact is active
-   false: Contact is inactive

Data type: Boolean

Default: true

</td></tr><tr><td>

contact.agent\_status

</td><td>

Status of the agent.Possible values:

-   Off work
-   On break
-   On route
-   On site

Data type: String

Maximum length: 40

</td></tr><tr><td>

contact.building

</td><td>

Sys\_id of the record that describes the building in which the contact resides.Data type: String

Table: Building \[cmn\_building\]

</td></tr><tr><td>

contact.calendar\_integration

</td><td>

Calendar application that the contact uses.1: Outlook

Data type: Number \(Integer\)

Default: 1

</td></tr><tr><td>

contact.city

</td><td>

City in which the contact resides.Data type: String

Maximum length: 40

</td></tr><tr><td>

contact.company

</td><td>

Sys\_id of the company record to which the contact is associated.Data type: String

Table: Company \[core\_company\]

</td></tr><tr><td>

contact.cost\_center

</td><td>

Sys\_id of the cost center associated with the contact.Data type: String

Table: Cost Center \[cmn\_cost\_center\]

</td></tr><tr><td>

contact.country

</td><td>

Country code of the country in which the contact resides.Data type: String

Maximum length: 3

</td></tr><tr><td>

contact.date\_format

</td><td>

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

contact.default\_perspective

</td><td>

Sys\_id of the default perspective for the contact.Data type: String

Table: Menu List \[sys\_perspective\]

</td></tr><tr><td>

contact.department

</td><td>

Sys\_id of the department associated with the contact.Data type: String

Table: Department \[cmn\_department\]

</td></tr><tr><td>

contact.edu\_status

</td><td>

Education status of the associated contact.Data type: String

Maximum length: 40

Default: faculty

</td></tr><tr><td>

contact.email

</td><td>

Contact email address.Data type: String

</td></tr><tr><td>

contact.employee\_number

</td><td>

Contact employee number.Data type: String

</td></tr><tr><td>

contact.enable\_multifactor\_authn

</td><td>

Flag that indicates whether multifactor authorization is required for the contact to log in to the service portal.Possible values:

-   true: Multifactor authorization enabled
-   false: Multifactor authorization disabled

Data type: Boolean

Default: false

</td></tr><tr><td>

contact.failed\_attempts

</td><td>

Number of failed log in attempts.Data type: Number \(Integer\)

</td></tr><tr><td>

contact.first\_name

</td><td>

Contact first name.Data type: String

Maximum length: 50

</td></tr><tr><td>

contact.gender

</td><td>

Contact gender.Data type: String

Maximum length: 40

</td></tr><tr><td>

contact.geolocation\_tracked

</td><td>

Flag that indicates whether the contact location is obtained through geotracking.Possible values:

-   true: Contact location obtained through geotracking
-   false: Contact location not obtained through geotracking

Data type: Boolean

Default value: false

</td></tr><tr><td>

contact.home\_phone

</td><td>

Contact home phone number.Data type: String

Maximum length: 40

</td></tr><tr><td>

contact.internal\_integration\_user

</td><td>

Flag that indicates whether the contact is an internal integration user.Possible values:

-   true: Internal integration user
-   false: Other type of user

Data type: Boolean

Default: false

</td></tr><tr><td>

contact.introduction

</td><td>

IntroductionData type: String

Maximum length: 40

</td></tr><tr><td>

contact.last\_login

</td><td>

Date on which the contact last logged into the system.Data type: String \(Date\)

</td></tr><tr><td>

contact.last\_login\_device

</td><td>

Device the consumer used the last time they logged in to the system.Data type: String

Maximum length: 40

</td></tr><tr><td>

contact.last\_login\_time

</td><td>

Date and time the contact logged in to the system.Data type: String \(Date/time\)

</td></tr><tr><td>

contact.last\_name

</td><td>

Contact last name.Data type: String

Maximum length: 50

</td></tr><tr><td>

contact.last\_position\_update

</td><td>

Date and time the last position was updated.Data type: String \(Date/time\)

</td></tr><tr><td>

contact.latitude

</td><td>

Latitude coordinate of the contact.Data type: Number \(Floating point\)

Maximum length: 40

</td></tr><tr><td>

contact.ldap\_server

</td><td>

Sys\_id of the LDAP server used by the contact to last log in to the system. Data type: String

Table: LDAP Server \[ldap\_server\_config\]

</td></tr><tr><td>

contact.location

</td><td>

Sys\_id of the record that describes the location of the contactData type: String

Table: Location \[cmn\_location\]

</td></tr><tr><td>

contact.locked\_out

</td><td>

Flag that indicates if the contact is locked-out.Possible values:

-   true: Contact locked-out
-   false: Contact not locked-out

Data type: Boolean

Default: false

</td></tr><tr><td>

contact.longitude

</td><td>

Longitude coordinate of the contact.Data type: Number \(Floating point\)

Maximum length: 40

</td></tr><tr><td>

contact.manager

</td><td>

Sys\_id of the record that describes the direct supervisor of the contact.Data type: String

Table: User \[sys\_user\]

</td></tr><tr><td>

contact.middle\_name

</td><td>

Contact middle name.Data type: Number \(Floating point\)

Maximum length: 50

</td></tr><tr><td>

contact.mobile\_phone

</td><td>

Contact mobile phone number.Data type: String

 Maximum length: 40

</td></tr><tr><td>

contact.name

</td><td>

Contact full name.Data type: String

Maximum length: 151

</td></tr><tr><td>

contact.notification

</td><td>

Indicates whether the contact should receive notifications.Valid values:

-   1: Disabled
-   2: Enabled

Data type: Number \(Integer\)

Default: 2

</td></tr><tr><td>

contact.on\_schedule

</td><td>

Indicates the timeliness of dispatched service personnel.Valid values:

-   Ahead: Ahead of schedule.
-   behind\_less30: Behind schedule, but less than 30 minutes.
-   behind\_30to60: Behind schedule between 30 and 60 minutes.
-   behind\_more60: Behind schedule more than 60 minutes.
-   on\_time: On schedule.

Data type: String

Maximum length: 40

</td></tr><tr><td>

contact.phone

</td><td>

Contact business phone number.Data type: String

Maximum length: 40

</td></tr><tr><td>

contact.photo

</td><td>

Photo image of the contact. Data type: String

</td></tr><tr><td>

contact.preferred\_language

</td><td>

Country code of the contact primary language.Data type: String

Maximum length: 3

</td></tr><tr><td>

contact.roles

</td><td>

List of user roles associated with the contact.Data type: String

Maximum length: 40

</td></tr><tr><td>

contact.schedule

</td><td>

Sys\_id of the record that describes the work schedule for the associated contact.Data type: String

Table: Schedule \[cmn\_schedule\]

</td></tr><tr><td>

contact.source

</td><td>

Source of the contact.Data type: String

Maximum length: 255

</td></tr><tr><td>

contact.state

</td><td>

State in which the contact resides.Data type: String

Maximum length: 40

</td></tr><tr><td>

contact.street

</td><td>

Contact street address.Data type: String

Maximum length: 255

</td></tr><tr><td>

contact.sys\_class\_name

</td><td>

Table that contains the contact record. Data type: String

Maximum length: 80

</td></tr><tr><td>

contact.sys\_created\_by

</td><td>

User that originally created the associated contact record.Data type: String

Maximum length: 40

</td></tr><tr><td>

contact.sys\_created\_on

</td><td>

Data and time the associated contact was originally created.Data type: String \(Date/time\)

</td></tr><tr><td>

contact.sys\_domain

</td><td>

ServiceNow instance domain of the associated contact record.Data type: String

</td></tr><tr><td>

contact.sys\_domain\_path

</td><td>

Contact record domain path.Data type: String

Maximum length: 255

Default: / \(global\)

</td></tr><tr><td>

contact.sys\_id

</td><td>

Unique identifier for the associated contact record.Data type: String

</td></tr><tr><td>

contact.sys\_mod\_count

</td><td>

Number of times that the associated contact record has been modified.Data type: Number \(Integer\)

</td></tr><tr><td>

contact.sys\_tags

</td><td>

System tags for the content.Data type: String

</td></tr><tr><td>

contact.sys\_updated\_by

</td><td>

User that last updated the associated contact information.Data type: String

Maximum length: 40

</td></tr><tr><td>

contact.sys\_updated\_on

</td><td>

Data and time the associated contact information was updated.Data type: String \(Date/time\)

</td></tr><tr><td>

contact.time\_format

</td><td>

Format in which to display time.Valid values:

-   hh.mm.ss a: hh.mm.ss \(12 hour\)
-   hh:mm:ss a: hh:mm:ss \(12 hour\)
-   HH.mm.ss: hh.mm.ss \(24 hour\)
-   HH:mm:ss: hh:mm:ss \(24 hour\)

Data type: String

Maximum length: 40

Default: Blank \(system time format\)

</td></tr><tr><td>

contact.time\_sheet\_policy

</td><td>

Sys\_id of the record that contains the time sheet policy for the associated contact.Data type: String

Table: Time Sheet Policy \[time\_sheet\_policy\]

</td></tr><tr><td>

contact.time\_zone

</td><td>

Time zone in which the contact resides, such as Canada/Central or US/Eastern.Data type: String

Maximum length: 40

</td></tr><tr><td>

contact.title

</td><td>

Contact business title such as Manager, Software Developer, or Contractor.Data type: String

Maximum length: 60

</td></tr><tr><td>

contact.user\_name

</td><td>

Contact user ID.Data type: String

Maximum length: 40

</td></tr><tr><td>

contact.vip

</td><td>

Flag that indicates whether the associated contact has VIP status.Possible values:

-   true: VIP
-   false: Not VIP

Data type: Boolean

Default: false

</td></tr><tr><td>

contact.web\_service\_access\_only

</td><td>

Flag that indicates whether the contact can only access services through the web.Possible values:

-   true: Web access only
-   false: Access through all available methods

Data type: Boolean

Default: false

</td></tr><tr><td>

contact.zip

</td><td>

Contact zip code.Data type: String

Maximum length: 40

</td></tr><tr><td>

contact\_local\_time

</td><td id="casetable-contact_local_time-entry">

Contact local time.Data type: String

Maximum length: 70

</td></tr><tr><td>

contact\_time\_zone

</td><td id="casetable-contact_time_zone-entry">

Time zone of the contact associated with the case.Data type: String

Maximum length: 40

</td></tr><tr><td>

contact\_type

</td><td id="casetable-contact_type-entry">

Method in which the case was initially reported.Possible values:

-   chat
-   email
-   phone
-   social
-   web

Data type: String

Maximum length: 40

</td></tr><tr><td>

contract

</td><td id="casetable-contract-entry">

Sys\_id of the contract associated with the case. This contract contains information about the type of support that is provided to the company associated to the case. A contract can include a company and contact and the specific assets that are covered. A contract can also include multiple service entitlements and SLAs.Data type: String

Table: Contract \[ast\_contract\]

</td></tr><tr><td>

correlation\_display

</td><td id="casetable-correlation_display-entry">

Correlation display.Data type: String

Maximum length: 100

</td></tr><tr><td>

correlation\_id

</td><td id="casetable-correlation_id-entry">

Correlation identifier.Data type: String

Maximum length: 100

</td></tr><tr><td>

delivery\_plan

</td><td id="casetable-delivery_plan-entry">

Sys\_id of the parent execution plan for this case.Data type: String

Table: Execution Plan \[sc\_cat\_item\_delivery\_plan\]

</td></tr><tr><td>

delivery\_task

</td><td id="casetable-delivery_task-entry">

Sys\_id of the execution plan task.Data type: String

Table: Execution Plan Task \[sc\_cat\_item\_delivery\_task\]

</td></tr><tr><td>

description

</td><td id="casetable-description-entry">

Detailed description of the problem associated with the case. Data type: String

Maximum length: 4,000

</td></tr><tr><td>

due\_date

</td><td id="casetable-due_date-entry">

Date that the case is due to be closed.Data type: String

</td></tr><tr><td>

entitlement

</td><td id="casetable-entitlement-entry">

Sys\_id of the entitlement record associated with the case. Entitlements define the type of support that a customer receives as well as the supported communication channels. An entitlement can be associated with a product, an asset, an account, or a contract.Data type: String

Table: Entitlement \[service\_entitlement\]

</td></tr><tr><td>

escalation

</td><td id="casetable-escalation-entry">

Current escalation level.Possible values:

-   0: Normal
-   1: Moderate
-   2: High
-   3: Overdue

Data type: Number \(Integer\)

Default: 0

</td></tr><tr><td>

expected\_start

</td><td id="casetable-expected_start-entry">

Date and time when work is scheduled to begin on the case.Data type: String

</td></tr><tr><td>

first\_response\_time

</td><td id="casetable-first_response_time-entry">

Date and time when the first action was taken on the case.Data type: String

</td></tr><tr><td>

follow\_the\_sun

</td><td id="casetable-follow_the_sun-entry">

Flag that indicates whether the case should be handed-off for global follow-up.If a customer enters additional comments on a Priority 1 - Critical or a Priority 2 - High case, or if the case is escalated, the flag is automatically set to true.

Possible values:

-   true: Case should be handed-off for global follow-up
-   false: Case shouldn't be handed-off for global follow-up

Data type: Boolean

Default: false

</td></tr><tr><td>

follow\_up

</td><td id="casetable-follow_up-entry">

Date and time of the next follow-up action.Data type: String

</td></tr><tr><td>

group\_list

</td><td id="casetable-group_list-entry">

List of sys\_ids of the group records associated with the case.Data type: Array

Table: Group \[sys\_user\_group\]

</td></tr><tr><td>

impact

</td><td id="casetable-impact-entry">

Impact on customer.Possible values:

-   1: High
-   2: Medium
-   3: Low

Data type: Number \(Integer\)

Default: 3

</td></tr><tr><td>

knowledge

</td><td id="casetable-knowledge-entry">

Flag that indicates if there is a knowledge base article available for the specified issue.Possible values:

-   true: Knowledge base article is available for this issue
-   false: Knowledge base article is not available for this issue

Data type: Boolean

Default: false

</td></tr><tr><td>

location

</td><td id="casetable-location-entry">

Sys\_id of the record describing the company location.Data type: String

Table: Location \[cmn\_location\]

</td></tr><tr><td>

made\_sla

</td><td id="casetable-made_sla-entry">

Flag that indicates whether the case was resolved in alignment with the associated service level agreement.Possible values:

-   true: Case was resolved in alignment with SLA
-   false: Case wasn't resolved according to the SLA

Data type: Boolean

Default: true

</td></tr><tr><td>

major\_case\_state

</td><td id="casetable-major_case_state-entry">

Current state of the major case.Possible values:

-   accepted: Initial state when a manager creates a major case or when a manager promotes a candidate case.
-   canceled: Case is canceled.
-   proposed: Initial state when an agent or manager creates or proposes a candidate case.
-   rejected: Manager rejected candidate case.

Data type: String

Maximum length: 40

</td></tr><tr><td>

needs\_attention

</td><td id="casetable-needs_attention-entry">

Flag that indicates whether the case needs attention.Possible values:

-   true: Case needs additional attention
-   false: Case doesn't need additional attention

Data type: Boolean

Default: false

</td></tr><tr><td>

notes\_to\_comments

</td><td id="casetable-notes_to_comments-entry">

Flag that indicates whether to add the resolution notes to the comments.Possible values:

-   true: Resolutions notes, when added, are also added to the comments
-   false: Resolution notes in comments aren't required

Data type: Boolean

</td></tr><tr><td>

notify

</td><td id="casetable-notify-entry">

Method to use to notify contact/consumer.Possible values:

-   1: Do not notify
-   2: Send email
-   3: Telephone

Data type: Number \(Integer\)

Default: 1

</td></tr><tr><td>

number

</td><td id="casetable-number-entry">

Case number.Data type: String

Maximum length: 40

</td></tr><tr><td>

opened\_at

</td><td id="casetable-opened_at-entry">

Date and time that the case was opened.Data type: String

</td></tr><tr><td>

opened\_by

</td><td id="casetable-opened_by-entry">

Sys\_id of the person that initially opened the case.Data type: String

Table: User \[sys\_user\]

</td></tr><tr><td>

order

</td><td id="casetable-order-entry">

Order of the case.Data type: Number \(Integer\)

</td></tr><tr><td>

parent

</td><td id="casetable-parent-entry">

Sys\_id of the parent case to which this case \(child\) is associated.Data type: String

Table: Task \[task\]

</td></tr><tr><td>

partner

</td><td id="casetable-partner-entry">

Sys\_id of the partner associated with the case.Data type: String

Table: Account \[customer\_account\]

</td></tr><tr><td>

partner\_contact

</td><td id="casetable-partner_contact-entry">

Sys\_id of the partner contact associated with the case.Data type: String

Table: Contact \[customer\_contact\]

</td></tr><tr><td>

priority

</td><td id="casetable-priority-entry">

Priority of the case. Possible values:

-   1: Critical
-   2: High
-   3: Moderate
-   4: Low

Data type: Number \(Integer\)

Default: 4

</td></tr><tr><td>

probable\_cause

</td><td id="casetable-probable_cause-entry">

Possible cause of the issue associated with the case.Data type: String

Maximum length: 4,000

</td></tr><tr><td>

problem

</td><td id="casetable-problem-entry">

Sys\_id of the issue that the customer is encountering.Data type: String

Table: Problem \[problem\]

</td></tr><tr><td>

product

</td><td id="casetable-product-entry">

Sys\_id of the product model of the asset associated to the case. A model is a specific version or configuration of an asset \(for example, Apple Mac Book Pro\).Data type: String

Table: Product Model \[cmdb\_model\]

</td></tr><tr><td>

reassignment\_count

</td><td id="casetable-reassignment_count-entry">

Number of times that the case was reassigned to a person that is responsible for moving the case forward.Data type: Number \(Integer\)

Default: 0

</td></tr><tr><td>

recipient\_list

</td><td id="casetable-recipient_list-entry">

Sys\_id of the record that contains the list of recipients for communications about this case.Data type: String

Table: Recipients List \[sn\_publications\_recipients\_list\]

</td></tr><tr><td>

rejection\_goto

</td><td id="casetable-rejection_goto-entry">

Sys\_id of the task to execute if the case is rejected.Data type: String

Table: Task \[task\]

</td></tr><tr><td>

resolution\_code

</td><td id="casetable-resolution_code-entry">

Resolution state for the case, such as "Solved - Fixed by Support/Guidance provided". Data type: String

Maximum length: 40

</td></tr><tr><td>

resolved\_at

</td><td id="casetable-resolved_at-entry">

Date and time that the case was resolved.Data type: String

</td></tr><tr><td>

resolved\_by

</td><td id="casetable-resolved_by-entry">

Sys\_id of the person that resolved the case.Data type: String

Table: User \[sys\_user\]

</td></tr><tr id="case-result-response-row"><td>

result

</td><td>

List of values for the requested field.Data type: Array of Objects

```
"result": [
  {
    "label": "String",
    "value": "String"
  }
]
```

</td></tr><tr id="case-result-label-response-row"><td>

result.label

</td><td>

Display value for the field value.Data type: String

</td></tr><tr id="case-result-value-response-row"><td>

result.value

</td><td>

Field value.Data type: String

</td></tr><tr><td>

short\_description

</td><td id="casetable-short_description-entry">

Concise description of the case. Data type: String

Maximum length: 160

</td></tr><tr><td>

skills

</td><td id="casetable-skills-entry">

List of the unique identifiers \(sys\_id\) of the skills needed to complete the case.Data type: String

Table: Skill \[cmn\_skill\]

</td></tr><tr><td>

sla\_due

</td><td id="casetable-sla_due-entry">

Date/time at which the case must be closed based on the associated service level agreement.Data type: String

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile

</td><td>

Details for a specific social media profile, such as Facebook, Twitter, or YouTube.Data type: Array of Objects

```
"sn_app_cs_social_social_profile": [
  {
    "account": "String",
    "channel": [Array],
    "contact": {Object},
    "consumer": {Object},
    "created_on": "String",
    "profile": "String",
    "profile_url": "String",
    "social_id": "String",
    "source": "String",
    "sys_created_by": "String",
    "sys_created_on": "String",
    "sys_id": "String",
    "sys_mod_count": Number,
    "sys_tags": "String",
    "sys_updated_by": "String",
    "sys_updated_on": "String"
  }
]
```

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.account

</td><td>

Unique identifier of the record containing account information for the social media profile. Located in the Account \[customer\_account\] table.Data type: String

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.channel

</td><td>

Details on the associated social media profile channel.Data type: Object

```
"channel": {
  "name": "String",
  "sys_class_name": "String",
  "sys_created_by": "String",
  "sys_created_on": "String",
  "sys_mod_count": Number,
  "sys_package": "String",
  "sys_policy": "String",
  "sys_scope": "String",
  "sys_tags": "String",
  "sys_update_name": "String",
  "sys_updated_by": "String",
  "sys_updated_on": "String"
}
```

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.channel.name

</td><td>

Name of the social media channel.Data type: String

Maximum length: 100

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.channel.sys\_class\_name

</td><td>

Table that contains the social media channel record.Data type: String

Maximum length: 80

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.channel.sys\_created\_by

</td><td>

Person that created the social media channel.Data type: String

Maximum length: 40

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.channel.sys\_created\_on

</td><td>

Date and time the social media profile was created.Data type: Date/time

Maximum length: 40

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.channel.sys\_id

</td><td>

Unique identifier of the associated social media profile channel.Data type: String

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.channel.sys\_mod\_count

</td><td>

Number of times that information was modified for the associated social media profile channel.Data type: Integer

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.channel.sys\_name

</td><td>

System name of channel.Data type: String

Maximum length: 255

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.channel.sys\_package

</td><td>

Unique identifier of the record that contains information about the package associated with the profile; Package \[sys\_package\] table.Data type: Reference

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.channel.sys\_policy

</td><td>

System protection policy.Possible values:

-   protected
-   read

Data type: String

Maximum length: 40

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.channel.sys\_scope

</td><td>

Unique identifier of the record that contains information about the scope of the social profile; Application \[sys\_scope\] table.Data type: Reference

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.channel.sys\_tags

</td><td>

System tags associated with the channel.Data type: String

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.channel.sys\_update\_name

</td><td>

Name of the person that last updated the social media profile channel.Data type: String

Maximum length: 250

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.channel.sys\_updated\_by

</td><td>

User that last updated the social media profile channel.Data type: String

Maximum length: 40

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.channel.sys\_updated\_on

</td><td>

Date and time the social media profile channel was last updated.Data type: Date/time

Maximum length: 40

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.consumer

</td><td>

For business-to-consumer cases. Details about the consumer associated with the case.Data type: Object

```
"consumer": {
  "active": Boolean,
  "business_phone": "String",
  "city": "String",
  "country": "String",
  "date_format": "String",
  "email": "String",
  "fax": "String",
  "first_name": "String",
  "gender": "String",
  "home_phone": "String",
  "household": "String",
  "last_name": "String",
  "middle_name": "String",
  "mobile_phone": "String",
  "name": "String",
  "notes": "String",
  "notification": Number,
  "number": "String",
  "photo": Image,
  "preferred_language": "String",
  "prefix": "String",
  "primary": Boolean,
  "state": "String",
  "street": "String",
  "suffix": "String",
  "sys_created_by": "String",
  "sys_created_on": "String",
  "sys_domain": "String",
  "sys_id": "String",
  "sys_mod_count": Number,
  "sys_tags": "String",
  "sys_updated_by": "String",
  "sys_updated_on": "String",
  "time_format": "String",
  "time_zone": "String",
  "title": "String",
  "user": "String",
  "zip": "String"
}
```

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.consumer.active

</td><td>

Flag that indicates whether the consumer is active.Possible values:

-   true: Consumer active
-   false: Consumer de-activated

Data type: Boolean

Default: true

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.consumer.business\_phone

</td><td>

Business phone number of the consumer.Data type: String

Maximum length: 40

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.consumer.city

</td><td>

City in which the consumer resides.Data type: String

Maximum length: 100

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.consumer.country

</td><td>

Country in which the consumer resides.Data type: String

Maximum length: 40

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.consumer.date\_format

</td><td>

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

sn\_app\_cs\_social\_social\_profile.consumer.email

</td><td>

Email address of the consumer.Data type: String

Maximum length: 100

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.consumer.fax

</td><td>

Fax number of the consumer.Data type: String

Maximum length: 40

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.consumer.first\_name

</td><td>

Consumer first name.Data type: String

Maximum length: 50

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.consumer.gender

</td><td>

Gender of the consumer.Data type: String

Maximum length: 40

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.consumer.home\_phone

</td><td>

Home phone number of the consumer.Data type: String

Maximum length: 40

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.consumer.household

</td><td>

Sys\_id of the record that describes the household characteristics.Data type: String

Table: Household \[csm\_household\]

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.consumer.last\_name

</td><td>

Consumer last name.Data type: String

Maximum length: 50

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.consumer.middle\_name

</td><td>

Consumer middle name.Data type: String

Maximum length: 50

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.consumer.mobile\_phone

</td><td>

Consumer mobile phone number.Data type: String

Maximum length: 40

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.consumer.name

</td><td>

Consumer full name; first\_name+middle\_name+last\_name.Data type: String

Maximum length: 152

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.consumer.notes

</td><td>

Notes on consumer.Data type: String

Maximum length: 4,000

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.consumer.notification

</td><td>

Indicates whether the consumer should receive notifications.Valid values:

-   1: Disabled
-   2: Enabled

Data type: Number \(Integer\)

Maximum length: 40

Default: 2

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.consumer.number

</td><td>

Unique number associated with the consumer.Data type: String

Maximum length: 40

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.consumer.photo

</td><td>

Photo of the consumer.Data type: Image

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.consumer.preferred\_language

</td><td>

Consumer primary language.Data type: String

Maximum length: 3

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.consumer.prefix

</td><td>

Consumer name prefix such as, Dr., Mr., Mrs., or Ms.Data type: String

Maximum length: 40

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.consumer.primary

</td><td>

Flag that indicates whether this is the primary consumer.Possible values:

-   true: Primary consumer
-   false: Not primary consumer

Data type: Boolean

Default: false

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.consumer.state

</td><td>

State in which the consumer resides.Data type: String

Maximum length: 100

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.consumer.street

</td><td>

Consumer street address.Data type: String

Maximum length: 255

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.consumer.suffix

</td><td>

Consumer name suffix such as Jr., Sr., or II.Data type: String

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.consumer.sys\_created\_by

</td><td>

User that created the consumer record.Data type: String

Maximum length: 40

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.consumer.sys\_created\_on

</td><td>

Date and time the consumer record was originally created.Data type: String

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.consumer.sys\_domain

</td><td>

ServiceNow domain in which the consumer information resides.Data type: String

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.consumer.sys\_id

</td><td>

Unique identifier for the consumer.Data type: String

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.consumer.sys\_mod\_count

</td><td>

Number of times that the associated consumer information has been modified.Data type: Number \(Integer\)

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.consumer.sys\_tags

</td><td>

Consumer system tags.

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.consumer.sys\_updated\_by

</td><td>

User that last updated the consumer information.Data type: String

Maximum length: 40

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.consumer.sys\_updated\_on

</td><td>

Date and time when the consumer information was last updated.Data type: String

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.consumer.time\_format

</td><td>

Format in which to display time.Valid values:

-   hh.mm.ss a: hh.mm.ss \(12 hour\)
-   hh:mm:ss a: hh:mm:ss \(12 hour\)
-   HH.mm.ss: hh.mm.ss \(24 hour\)
-   HH:mm:ss: hh:mm:ss \(24 hour\)

Data type: String

Maximum length: 40

Default: blank \(system time format\)

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.consumer.time\_zone

</td><td>

Consumer time zone, such as Canada/Central or US/Eastern.Data type: String

Maximum length: 40

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.consumer.title

</td><td>

Consumer business title such as Manager, Software Developer, or Contractor.Data type: String

Maximum length: 60

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.consumer.user

</td><td>

Sys\_id of the consumer user. Data type: String

Table: Consumer User \[csm\_consumer\_user\]

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.consumer.zip

</td><td>

Consumer zip code. Data type: String

Maximum length: 40

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact

</td><td>

For business-to-business cases. Unique identifier of the record containing details about the social media profile that belongs to the contact associated with the case. Located in the Contact \[customer\_contact\] table.Data type: String

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.account

</td><td>

Sys\_id of the account record to which the contact is associated.Data type: String

Table: Account \[customer\_account\]

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.active

</td><td>

Flag that indicates whether the contact is active within the system.Possible values:

-   true: Contact is active
-   false: Contact is inactive

Data type: Boolean

Default: true

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.agent\_status

</td><td>

Status of the agent.Possible values:

-   Off work
-   On break
-   On route
-   On site

Data type: String

Maximum length: 40

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.building

</td><td>

Sys\_id of the record that describes the building in which the contact resides.Data type: String

Table: Building \[cmn\_building\]

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.calendar\_integration

</td><td>

Calendar application that the contact uses.1: Outlook

Data type: Number \(Integer\)

Default: 1

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.city

</td><td>

City in which the contact resides.Data type: String

Maximum length: 40

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.company

</td><td>

Sys\_id of the company record to which the contact is associated.Data type: String

Table: Company \[core\_company\]

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.cost\_center

</td><td>

Sys\_id of the cost center associated with the contact.Data type: String

Table: Cost Center \[cmn\_cost\_center\]

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.country

</td><td>

Country code of the country in which the contact resides.Data type: String

Maximum length: 3

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.date\_format

</td><td>

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

sn\_app\_cs\_social\_social\_profile.contact.default\_perspective

</td><td>

Sys\_id of the default perspective for the contact.Data type: String

Table: Menu List \[sys\_perspective\]

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.department

</td><td>

Sys\_id of the department associated with the contact.Data type: String

Table: Department \[cmn\_department\]

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.edu\_status

</td><td>

Education status of the associated contact.Data type: String

Maximum length: 40

Default: faculty

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.email

</td><td>

Contact email address.Data type: String

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.employee\_number

</td><td>

Contact employee number.Data type: String

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.enable\_multifactor\_authn

</td><td>

Flag that indicates whether multifactor authorization is required for the contact to log in to the service portal.Possible values:

-   true: Multifactor authorization enabled
-   false: Multifactor authorization disabled

Data type: Boolean

Default: false

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.failed\_attempts

</td><td>

Number of failed log in attempts.Data type: Number \(Integer\)

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.first\_name

</td><td>

Contact first name.Data type: String

Maximum length: 50

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.gender

</td><td>

Contact gender.Data type: String

Maximum length: 40

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.geolocation\_tracked

</td><td>

Flag that indicates whether the contact location is obtained through geotracking.Possible values:

-   true: Contact location obtained through geotracking
-   false: Contact location not obtained through geotracking

Data type: Boolean

Default value: false

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.home\_phone

</td><td>

Contact home phone number.Data type: String

Maximum length: 40

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.internal\_itegration\_user

</td><td>

Flag that indicates whether the contact is an internal integration user.Possible values:

-   true: Internal integration user
-   false: Other type of user

Data type: Boolean

Default: false

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.introduction

</td><td>

IntroductionData type: String

Maximum length: 40

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.last\_login

</td><td>

Date on which the contact last logged into the system.Data type: String \(Date\)

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.last\_login\_device

</td><td>

Device the consumer used the last time they logged in to the system.Data type: String

Maximum length: 40

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.last\_login\_time

</td><td>

Date and time the contact logged in to the system.Data type: String \(Date/time\)

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.last\_name

</td><td>

Contact last name.Data type: String

Maximum length: 50

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.last\_position\_update

</td><td>

Date and time the last position was updated.Data type: String \(Date/time\)

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.latitude

</td><td>

Latitude coordinate of the contact.Data type: Number \(Floating point\)

Maximum length: 40

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.ldap\_server

</td><td>

Sys\_id of the LDAP server used by the contact to last log in to the system. Data type: String

Table: LDAP Server \[ldap\_server\_config\]

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.location

</td><td>

Sys\_id of the record that describes the location of the contactData type: String

Table: Location \[cmn\_location\]

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.locked\_out

</td><td>

Flag that indicates if the contact is locked-out.Possible values:

-   true: Contact locked-out
-   false: Contact not locked-out

Data type: Boolean

Default: false

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.longitude

</td><td>

Longitude coordinate of the contact.Data type: Number \(Floating point\)

Maximum length: 40

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.manager

</td><td>

Sys\_id of the record that describes the direct supervisor of the contact.Data type: String

Table: User \[sys\_user\]

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.middle\_name

</td><td>

Contact middle name.Data type: Number \(Floating point\)

Maximum length: 50

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.mobile\_phone

</td><td>

Contact mobile phone number.Data type: String

 Maximum length: 40

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.name

</td><td>

Contact full name.Data type: String

Maximum length: 151

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.notification

</td><td>

Indicates whether the contact should receive notifications.Valid values:

-   1: Disabled
-   2: Enabled

Data type: Number \(Integer\)

Default: 2

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.on\_schedule

</td><td>

Indicates the timeliness of dispatched service personnel.Valid values:

-   Ahead: Ahead of schedule.
-   behind\_less30: Behind schedule, but less than 30 minutes.
-   behind\_30to60: Behind schedule between 30 and 60 minutes.
-   behind\_more60: Behind schedule more than 60 minutes.
-   on\_time: On schedule.

Data type: String

Maximum length: 40

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.phone

</td><td>

Contact business phone number.Data type: String

Maximum length: 40

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.photo

</td><td>

Photo image of the contact. Data type: String

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.preferred\_language

</td><td>

Country code of the contact primary language.Data type: String

Maximum length: 3

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.roles

</td><td>

List of user roles associated with the contact.Data type: String

Maximum length: 40

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.schedule

</td><td>

Sys\_id of the record that describes the work schedule for the associated contact.Data type: String

Table: Schedule \[cmn\_schedule\]

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.source

</td><td>

Source of the contact.Data type: String

Maximum length: 255

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.state

</td><td>

State in which the contact resides.Data type: String

Maximum length: 40

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.street

</td><td>

Contact street address.Data type: String

Maximum length: 255

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.sys\_class\_name

</td><td>

Table that contains the contact record. Data type: String

Maximum length: 80

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.sys\_created\_by

</td><td>

User that originally created the associated contact record.Data type: String

Maximum length: 40

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.sys\_created\_on

</td><td>

Data and time the associated contact was originally created.Data type: String \(Date/time\)

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.sys\_domain

</td><td>

ServiceNow instance domain of the associated contact record.Data type: String

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.sys\_domain\_path

</td><td>

Contact record domain path.Data type: String

Maximum length: 255

Default: / \(global\)

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.sys\_id

</td><td>

Unique identifier for the associated contact record.Data type: String

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.sys\_mod\_count

</td><td>

Number of times that the associated contact record has been modified.Data type: Number \(Integer\)

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.sys\_tags

</td><td>

Contact system tags.

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.sys\_updated\_by

</td><td>

User that last updated the associated contact information.Data type: String

Maximum length: 40

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.sys\_updated\_on

</td><td>

Data and time the associated contact information was updated.Data type: String \(Date/time\)

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.time\_format

</td><td>

Format in which to display time.Valid values:

-   hh.mm.ss a: hh.mm.ss \(12 hour\)
-   hh:mm:ss a: hh:mm:ss \(12 hour\)
-   HH.mm.ss: hh.mm.ss \(24 hour\)
-   HH:mm:ss: hh:mm:ss \(24 hour\)

Data type: String

Maximum length: 40

Default: Blank \(system time format\)

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.time\_sheet\_policy

</td><td>

Sys\_id of the record that contains the time sheet policy for the associated contact.Data type: String

Table: Time Sheet Policy \[time\_sheet\_policy\]

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.time\_zone

</td><td>

Time zone in which the contact resides, such as Canada/Central or US/Eastern.Data type: String

Maximum length: 40

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.title

</td><td>

Contact business title such as Manager, Software Developer, or Contractor.Data type: String

Maximum length: 60

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.user\_name

</td><td>

Contact user ID.Data type: String

Maximum length: 40

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.vip

</td><td>

Flag that indicates whether the associated contact has VIP status.Possible values:

-   true: VIP
-   false: Not VIP

Data type: Boolean

Default: false

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.web\_service\_access\_only

</td><td>

Flag that indicates whether the contact can only access services through the web.Possible values:

-   true: Web access only
-   false: Access through all available methods

Data type: Boolean

Default: false

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.zip

</td><td>

Contact zip code.Data type: String

Maximum length: 40

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.created\_on

</td><td>

Date and time the associated social media profile was initially created.

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.profile

</td><td>

Social profile.Data type: String

 Maximum length: 255

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.profile\_url

</td><td>

URL to use to access the social media profile.Data type: String

 Maximum length: 1,024

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.social\_id

</td><td>

Unique social media account provider identifier for the associated social media account.Data type: String

 Maximum length: 100

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.source

</td><td>

Source of the social profile.Data type: String

 Maximum length: 255

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.sys\_created\_by

</td><td>

User that initially created the social media profile.Data type: String

 Maximum length: 40

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.sys\_created\_on

</td><td>

Date and time the social media profile was initially created.Data type: String \(Date/time\)

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.sys\_id

</td><td>

Unique identifier for the social media profile.Data type: String

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.sys\_mod\_count

</td><td>

Number of times that information was modified for the associated social media profile.Data type: Number \(Integer\)

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.sys\_tags

</td><td>

Profile system tags.

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.sys\_updated\_by

</td><td>

User that initially created the social media profile.Data type: String

 Maximum length: 40

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.sys\_updated\_on

</td><td>

User that initially created the social media profile.Data type: String

 Maximum length: 40

</td></tr><tr><td>

state

</td><td id="casetable-state-entry">

Current state of the case.Possible values:

-   1: New
-   3: Closed
-   6: Resolved
-   10: Open
-   18: Awaiting Info

Data type: Number \(Integer\)

Default: 1

</td></tr><tr><td>

subcategory

</td><td id="casetable-subcategory-entry">

Case subcategory.Possible values:

0: QuestionData type: Number \(Integer\)

Default: 0

</td></tr><tr><td>

support\_manager

</td><td id="casetable-support_manager-entry">

Sys\_id of the CSM manager assigned to the case.Data type: String

Table: User \[sys\_user\]

</td></tr><tr><td>

sync\_driver

</td><td id="casetable-sync_driver-entry">

Flag that indicates whether there's driver synchronization.Possible values:

-   true: Driver is synchronized
-   false: Driver isn't synchronized

Data type: Boolean

</td></tr><tr><td>

sys\_class\_name

</td><td id="casetable-sys_class_name-entry">

Table that contains the case record.Data type: String

Maximum length: 80

</td></tr><tr><td>

sys\_created\_by

</td><td id="casetable-sys_created_by-entry">

Person that initially opened the case.Data type: String

Maximum length: 40

</td></tr><tr><td>

sys\_created\_on

</td><td id="casetable-sys_created_on-entry">

Date and time when the case was initially created.Data type: String

</td></tr><tr><td>

sys\_domain

</td><td id="casetable-sys_domain-entry">

Domain associated with the case.Data type: String

Maximum length: 32

Default: global

</td></tr><tr><td>

sys\_domain\_path

</td><td id="casetable-sys_domain_path-entry">

Domain path.Data type: String

Maximum length: 255

Default: /

</td></tr><tr><td>

sys\_id

</td><td id="casetable-sys_sys_id-entry">

Unique identifier for the case.Data type: String

Maximum length: 32

</td></tr><tr><td>

sys\_mod\_count

</td><td id="casetable-sys_mod_count-entry">

Number of updates to the case since it was initially created.Data type: Number \(Integer\)

</td></tr><tr><td>

sys\_tags

</td><td>

System tags.

</td></tr><tr><td>

sys\_updated\_by

</td><td id="casetable-sys_updated_by-entry">

Person that last updated the case.Data type: String

Maximum length: 40

</td></tr><tr><td>

sys\_updated\_on

</td><td id="casetable-sys_updated_on-entry">

Date and time when the case was last updated.Data type: String

</td></tr><tr><td>

time\_worked

</td><td id="casetable-time_worked-entry">

Total amount of time worked on the case.Data type: String

</td></tr><tr><td>

upon\_approval

</td><td id="casetable-upon_approval-entry">

Action to take if the case is approved.Possible values:

-   do\_nothing
-   proceed

Data type: String

Maximum length: 40

Default: proceed

</td></tr><tr><td>

upon\_reject

</td><td id="casetable-upon_reject-entry">

Action to take if the case is rejected.Possible values:

-   cancel
-   goto

Data type: String

Maximum length: 40

Default: cancel

</td></tr><tr><td>

urgency

</td><td id="casetable-urgency-entry">

Urgency of the case.Possible values:

-   1: High
-   2: Medium
-   3: Low

Data type: Number \(Integer\)

Default: 3

</td></tr><tr><td>

user\_input

</td><td id="casetable-user_input-entry">

Additional user input.Data type: String

Maximum length: 4,000

</td></tr><tr><td>

variable\_pool

</td><td>

Grouping of variables.

</td></tr><tr><td>

variables

</td><td id="casetable-variables-entry">

Name-value pairs of variables associated with the case.Data type: String

Maximum length: 40

</td></tr><tr><td>

watch\_list

</td><td id="casetable-watch_list-entry">

List of sys\_ids of the users who receive notifications about this case when additional comments are added or if the state of a case is changed to Resolved or Closed.Data type: Array

Table: User \[sys\_user\]

</td></tr><tr><td>

wf\_activity

</td><td id="casetable-wf_activity-entry">

Sys\_id of the workflow activity record associated with the case.Data type: String

Table: Workflow Activity \[wf\_activity\]

</td></tr><tr><td>

work\_end

</td><td id="casetable-work_end-entry">

Date and time work ended on the case.Data type: String

</td></tr><tr><td>

work\_notes

</td><td id="casetable-work_notes-entry">

Information about how to resolve the case, or steps taken to resolve it.Data type: String

Maximum length: 4,000

</td></tr><tr><td>

work\_notes\_list

</td><td id="casetable-work_notes_list-entry">

List of sys\_ids of the internal users who receive notifications about this case when work notes are added.Data type: Array

Table: User \[sys\_user\]

</td></tr><tr><td>

work\_start

</td><td id="casetable-work_start-entry">

Date and time that work started on the case.Data type: String

</td></tr></tbody>
</table>### cURL request

Retrieve the third and fourth CSM cases listed for a specific account.

```
curl "https://instance.servicenow.com/api/sn_customerservice/case?sysparm_query=account=86837a386f0331003b3c498f5d3ee4ca&sysparm_limit=2&sysparm_offset=2" \
--request GET \
--header "Accept:application/json" \
--user "username":"password"

```

The response shows the two cases.

```
{
  "result": [{
    "parent": "",
    "caused_by": "",
    "watch_list": "",
    "active_escalation": "",
    "upon_reject": "cancel",
    "sys_updated_on": "2017-06-17 16:37:13",
    "support_manager": "",
    "approval_history": "",
    "skills": "a6d64b11d772120058c92cf65e610357,9b178b11d772120058c92cf65e610382,1c76ec15d703120058c92cf65e61034a",
    "number": "CS0000009",
    "problem": "",
    "state": "18",
    "case": "Advanced and large routers making noise​CS0000009",
    "sys_created_by": "alex linde",
    "knowledge": "false",
    "order": "",
    "cmdb_ci": "",
    "delivery_plan": "",
    "impact": "3",
    "contract": "",
    "active": "true",
    "work_notes_list": "",
    "auto_created_case": "false",
    "priority": "3",
    "sys_domain_path": "/",
    "rejection_goto": "",
    "first_response_time": "",
    "business_duration": "",
    "group_list": "",
    "child_case_creation_progress": "false",
    "sync_driver": "false",
    "approval_set": "",
    "wf_activity": "",
    "short_description": "Advanced and large routers making noise",
    "correlation_display": "",
    "delivery_task": "",
    "work_start": "",
    "recipient_list": "",
    "additional_assignee_list": "",
    "notify": "1",
    "sys_class_name": "sn_customerservice_case",
    "closed_by": "",
    "follow_up": "",
    "contact_local_time": "",
    "sn_app_cs_social_social_profile": "",
    "reassignment_count": "1",
    "contact_time_zone": "",
    "notes_to_comments": "false",
    "assigned_to": "85453c616fc331003b3c498f5d3ee4fa",
    "product": "5f5fbcc3c0a8010e00f3b27814f3b96b",
    "variables": "",
    "variable_pool": "",
    "hierarchical_variables": "variable_pool",
    "sla_due": "",
    "change": "",
    "comments_and_work_notes": "",
    "partner": "",
    "escalation": "0",
    "upon_approval": "proceed",
    "partner_contact": "",
    "correlation_id": "",
    "asset": "a8fb6024d7700200e5982cf65e61034d",
    "made_sla": "true",
    "resolved_by": "",
    "sys_updated_by": "admin",
    "opened_by": "60beb5e7d7600200e5982cf65e6103ad",
    "user_input": "",
    "sys_created_on": "2016-09-19 16:49:18",
    "contact": {
      "country": "",
      "calendar_integration": "1",
      "last_position_update": "",
      "last_login_time": "2018-05-10 19:50:26",
      "last_login_device": "0:0:0:0:0:0:0:1%0",
      "source": "",
      "sys_updated_on": "2018-02-16 21:30:03",
      "building": "",
      "web_service_access_only": "false",
      "notification": "1",
      "sys_updated_by": "venki",
      "enable_multifactor_authn": "false",
      "sys_created_on": "2018-02-16 21:29:11",
      "sys_domain": "global",
      "agent_status": "",
      "state": "",
      "vip": "false",
      "sys_created_by": "venki",
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
      "phone": "(626) 722-6969",
      "cost_center": "",
      "name": "Julie Lewis",
      "employee_number": "",
      "gender": "",
      "city": "",
      "user_name": "julie.lewis",
      "failed_attempts": "",
      "edu_status": "faculty",
      "latitude": "",
      "roles": "",
      "title": "Operations Manager",
      "sys_class_name": "customer_contact",
      "sys_id": "4d147a386f0331003b3c498f5d3ee437",
      "internal_integration_user": "false",
      "ldap_server": "",
      "mobile_phone": "",
      "street": "",
      "company": "86837a386f0331003b3c498f5d3ee4ca",
      "department": "",
      "first_name": "Julie",
      "preferred_language": "en",
      "introduction": "",
      "email": "julie.lewis@mailinator.com",
      "manager": "",
      "locked_out": "false",
      "sys_mod_count": "1",
      "last_name": "Lewis",
      "photo": "",
      "sys_tags": "",
      "middle_name": "",
      "time_zone": "",
      "schedule": "",
      "on_schedule": "",
      "date_format": "",
      "location": "",
      "account": "86837a386f0331003b3c498f5d3ee4ca"
    },
    "sys_domain": "global",
    "closed_at": "",
    "follow_the_sun": "false",
    "entitlement": "",
    "business_service": "",
    "business_impact": "",
    "time_worked": "",
    "expected_start": "",
    "opened_at": "2016-09-19 16:49:18",
    "work_end": "",
    "resolved_at": "",
    "case_report": "",
    "subcategory": "0",
    "work_notes": "",
    "assignment_group": "6a42f4616fc331003b3c498f5d3ee46f",
    "cause": "",
    "description": "",
    "calendar_duration": "",
    "close_notes": "",
    "sys_id": "dccc6024d7700200e5982cf65e6103e5",
    "contact_type": "web",
    "resolution_code": "",
    "probable_cause": "",
    "urgency": "3",
    "company": "",
    "major_case_state": "",
    "consumer": "",
    "activity_due": "",
    "comments": "",
    "approval": "not requested",
    "due_date": "",
    "sys_mod_count": "5",
    "sys_tags": "",
    "active_account_escalation": "",
    "location": "",
    "category": "1",
    "account": {
      "banner_image_light": "",
      "country": "USA",
      "parent": "",
      "notes": "",
      "stock_symbol": "",
      "discount": "",
      "active_escalation": "",
      "sys_updated_on": "2019-01-03 19:37:35",
      "apple_icon": "",
      "number": "ACCT0000001",
      "sys_updated_by": "admin",
      "fiscal_year": "",
      "sys_created_on": "2018-02-20 21:29:16",
      "contact": "4d147a386f0331003b3c498f5d3ee437",
      "stock_price": "",
      "state": "",
      "banner_image": "",
      "sys_created_by": "venki",
      "longitude": "-122.4005464",
      "zip": "94103",
      "profits": "0",
      "phone": "(626) 722-6999",
      "fax_phone": "",
      "name": "Boxeo",
      "banner_text": "",
      "account_code": "~~~~1",
      "primary": "false",
      "city": "San Francisco",
      "latitude": "37.7838391",
      "sys_class_name": "customer_account",
      "manufacturer": "false",
      "account_parent": "",
      "sys_id": "86837a386f0331003b3c498f5d3ee4ca",
      "market_cap": "0",
      "num_employees": "",
      "rank_tier": "",
      "street": "747 Howard St",
      "vendor": "false",
      "lat_long_error": "",
      "theme": "",
      "vendor_type": "",
      "website": "www.boxeo.com",
      "revenue_per_year": "0",
      "publicly_traded": "false",
      "sys_mod_count": "9",
      "sys_tags": "",
      "partner": "false",
      "registration_code": "BOXEO",
      "vendor_manager": "",
      "account_path": "~~~~1",
      "primary_contact": "4d147a386f0331003b3c498f5d3ee437",
      "customer": "true"
    }
  }, {
    "parent": "",
    "caused_by": "",
    "watch_list": "",
    "active_escalation": "",
    "upon_reject": "cancel",
    "sys_updated_on": "2019-01-15 23:28:00",
    "support_manager": "",
    "approval_history": "",
    "skills": "a6d64b11d772120058c92cf65e610357,9b178b11d772120058c92cf65e610382,1c76ec15d703120058c92cf65e61034a",
    "number": "CS0000005",
    "problem": "",
    "state": "6",
    "case": "Urgent issue, need help ...​CS0000005",
    "sys_created_by": "admin",
    "knowledge": "false",
    "order": "",
    "cmdb_ci": "",
    "delivery_plan": "",
    "impact": "",
    "contract": "495e16b96f0731003b3c498f5d3ee4af",
    "active": "true",
    "work_notes_list": "",
    "auto_created_case": "false",
    "priority": "1",
    "sys_domain_path": "/",
    "rejection_goto": "",
    "first_response_time": "",
    "business_duration": "",
    "group_list": "",
    "child_case_creation_progress": "false",
    "sync_driver": "false",
    "approval_set": "",
    "wf_activity": "",
    "short_description": "Urgent issue, need help ...",
    "correlation_display": "",
    "delivery_task": "",
    "work_start": "",
    "recipient_list": "",
    "additional_assignee_list": "",
    "notify": "",
    "sys_class_name": "sn_customerservice_case",
    "closed_by": "",
    "follow_up": "",
    "contact_local_time": "",
    "sn_app_cs_social_social_profile": "",
    "reassignment_count": "",
    "contact_time_zone": "",
    "notes_to_comments": "false",
    "assigned_to": "85453c616fc331003b3c498f5d3ee4fa",
    "product": "9068b0a16fc331003b3c498f5d3ee438",
    "variables": "",
    "variable_pool": "",
    "hierarchical_variables": "variable_pool",
    "sla_due": "",
    "change": "",
    "comments_and_work_notes": "",
    "partner": "",
    "escalation": "",
    "upon_approval": "proceed",
    "partner_contact": "",
    "correlation_id": "",
    "asset": "b8defca16fc331003b3c498f5d3ee4e7",
    "made_sla": "false",
    "resolved_by": "",
    "sys_updated_by": "jodi.seals",
    "opened_by": "ddce70866f9331003b3c498f5d3ee417",
    "user_input": "",
    "sys_created_on": "2019-01-02 20:00:00",
    "contact": {
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
    "sys_domain": "global",
    "closed_at": "",
    "follow_the_sun": "false",
    "entitlement": "1eb7893a6f1b31003b3c498f5d3ee4dd",
    "business_service": "",
    "business_impact": "",
    "time_worked": "",
    "expected_start": "",
    "opened_at": "2019-01-02 20:00:00",
    "work_end": "",
    "resolved_at": "",
    "case_report": "",
    "subcategory": "0",
    "work_notes": "",
    "assignment_group": "0df0c400c322310015519f2974d3ae23",
    "cause": "",
    "description": "",
    "calendar_duration": "",
    "close_notes": "",
    "sys_id": "cf866683c3033100b12d9f2974d3ae1f",
    "contact_type": "web",
    "resolution_code": "",
    "probable_cause": "",
    "urgency": "3",
    "company": "",
    "major_case_state": "",
    "consumer": "",
    "activity_due": "",
    "comments": "",
    "approval": "",
    "due_date": "2016-08-04 20:36:23",
    "sys_mod_count": "0",
    "sys_tags": "",
    "active_account_escalation": "",
    "location": "",
    "category": "1",
    "account": {
      "banner_image_light": "",
      "country": "USA",
      "parent": "",
      "notes": "",
      "stock_symbol": "",
      "discount": "",
      "active_escalation": "",
      "sys_updated_on": "2019-01-03 19:37:35",
      "apple_icon": "",
      "number": "ACCT0000001",
      "sys_updated_by": "admin",
      "fiscal_year": "",
      "sys_created_on": "2018-02-20 21:29:16",
      "contact": "4d147a386f0331003b3c498f5d3ee437",
      "stock_price": "",
      "state": "",
      "banner_image": "",
      "sys_created_by": "venki",
      "longitude": "-122.4005464",
      "zip": "94103",
      "profits": "0",
      "phone": "(626) 722-6999",
      "fax_phone": "",
      "name": "Boxeo",
      "banner_text": "",
      "account_code": "~~~~1",
      "primary": "false",
      "city": "San Francisco",
      "latitude": "37.7838391",
      "sys_class_name": "customer_account",
      "manufacturer": "false",
      "account_parent": "",
      "sys_id": "86837a386f0331003b3c498f5d3ee4ca",
      "market_cap": "0",
      "num_employees": "",
      "rank_tier": "",
      "street": "747 Howard St",
      "vendor": "false",
      "lat_long_error": "",
      "theme": "",
      "vendor_type": "",
      "website": "www.boxeo.com",
      "revenue_per_year": "0",
      "publicly_traded": "false",
      "sys_mod_count": "9",
      "sys_tags": "",
      "partner": "false",
      "registration_code": "BOXEO",
      "vendor_manager": "",
      "account_path": "~~~~1",
      "primary_contact": "4d147a386f0331003b3c498f5d3ee437",
      "customer": "true"
    }
  }]
}
```

## Case - POST /sn\_customerservice/case

Creates a new Customer Service Management \(CSM\) case.

To use this endpoint, users must have the csm\_ws\_integration, sn\_customerservice.customer, or sn\_customerservice.consumer role.

You can create different types of cases depending on whether you are working in a business-to-business \(B2B\) or business-to-consumer \(B2C\) environment, or creating a case for an order or product.

In addition, you can create a social media profile for a contact, consumer, or account using this endpoint. To create a social media profile, you must specify the following parameters in the request body:

-   **social\_channel**
-   **social\_handle**
-   **social\_handle\_type**
-   **social\_handle\_url**
-   **social\_post\_url**

All request body parameters are optional. Some parameters are only valid in one environment or the other \(B2B or B2C\), and are noted as such in the request body parameter descriptions. If you specify a contact, the account, case report, contract, and entitlement parameters are defaulted to the values defined in the contact/account records. If you specify an account, the case report, contract, and entitlement parameters are defaulted to the values defined in the account record \(unless overridden by passed in parameters.\) If you do not pass any parameters to the endpoint, the case record is created with only default information \(defined in the table below\) and instance generated values \(**sys\_\***\). All other parameters are set with their equivalent of a null value. In addition to the list of parameters defined below, which define the parameters found in a base system, the endpoint also accepts custom case fields and any additional case fields configured in your instance. For additional information on these elements, refer to your specific table definitions \[**System Definition** &gt; **Tables**\].

**Warning:** This endpoint does not perform parameter validation as doing so can create excessive overhead. If a request parameter is misspelled, is not valid for the type of case, or is not supported by the endpoint, it is either ignored without warning or can cause unexpected results. For example, if you create a consumer or contact for the wrong type of case or mismatch a contact with an account.

**Warning:** By default, external users who have the sn\_customerservice.customer or sn\_customerservice.consumer role can only set the account, asset, comments, consumer, contact, contact\_type, partner, partner\_contact, priority, product, short\_description, and state fields using this endpoint.

**Note:** You can reference all sysparm query parameters using either their full name or their shortened name \(without the **sysparm\_** prefix\). For example, for **sysparm\_limit** you can also use **limit**.

### URL format

Versioned URL: `/api/sn_customerservice/{api_version}/case`

Default URL: `/api/sn_customerservice/case`

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

</td><td>

Sys\_id of the account associated with the case. Data type: String

Default: If **contact** specified, defaults to account specified in contact record.

Table: Account \[customer\_account\]

</td></tr><tr><td>

active

</td><td id="casetable-active-entry">

Flag that indicates whether the case is open and active.Possible values:

-   true: Case is active
-   false: Case is closed

Data type: Boolean

Default: true

</td></tr><tr><td>

active\_account\_escalation

</td><td id="casetable-active_account_escalation-entry">

Sys\_id of the active account escalation record associated with the case.Data type: String

Table: Escalation \[sn\_customerservice\_escalation\]

</td></tr><tr><td>

active\_escalation

</td><td id="casetable-active_escalation-entry">

Sys\_id of the active escalation record associated with the case.Data type: String

Table: Escalation \[sn\_customerservice\_escalation\]

</td></tr><tr><td>

activity\_due

</td><td id="casetable-activity_due-entry">

Date for which the associated case is expected to be completed.Data type: String

</td></tr><tr><td>

additional\_assignee\_list

</td><td id="casetable-additional_assignee_list-entry">

List of the sys\_ids of the additional persons \(other than the primary assignee\) that have been assigned to the account.Data type: Array

Maximum: 4,000

Table: User \[sys\_user\]

</td></tr><tr><td>

approval

</td><td id="casetable-approval-entry">

String that describes the type of approval required.Possible values:

-   approved
-   cancelled
-   duplicate
-   not\_required
-   not requested
-   rejected
-   requested

Data type: String

Maximum characters: 40

Default: not requested

</td></tr><tr><td>

assigned\_to

</td><td id="casetable-assigned_to-entry">

Sys\_id of the person assigned to the case.

Table: User \[sys\_user\]

 Data type: String

</td></tr><tr><td>

assignment\_group

</td><td id="casetable-aassignment_group-entry">

Sys\_id of the customer service agent group assigned to the case.Data type: String

Table: Group \[sys\_user\_group\]

</td></tr><tr><td>

business\_duration

</td><td id="casetable-business_duration-entry">

Length in calendar work hours, work days, and work weeks that it took to complete the case.Data type: String

</td></tr><tr><td>

business\_impact

</td><td id="casetable-business_impact-entry">

Impact of the issue on the associated customer.Data type: String

Maximum characters: 4,000

</td></tr><tr><td>

business\_service

</td><td id="casetable-business_service-entry">

Sys\_id of the service record associated with the case.Data type: String

Table: Service \[cmdb\_ci\_service\]

</td></tr><tr><td>

category

</td><td id="casetable-category-entry">

Case category.Possible values:

-   0: Question
-   1: Issue
-   2: Feature

Data type: Number \(Integer\)

Default: 1

</td></tr><tr><td>

cause

</td><td id="casetable-cause-entry">

Details about the cause of the problem.Data type: String

Maximum length: 4,000

</td></tr><tr><td>

caused\_by

</td><td id="casetable-caused_by-entry">

Sys\_id of the change request that caused the case to be created.Data type: String

Table: Change Request \[change\_request\]

</td></tr><tr><td>

change

</td><td id="casetable-change-entry">

Sys\_id of the change request that caused the case to be created.Data type: String

Table: Change Request \[change\_request\]

</td></tr><tr><td>

child\_case\_creation\_progress

</td><td id="casetable-child_case_creation_progress-entry">

Flag that indicates whether the case is a child case that was created from a major case.Possible values:

-   true: Child case created from a major case
-   false: Not a child case

Data type: Boolean

</td></tr><tr><td>

close\_notes

</td><td id="casetable-close_notes-entry">

Notes made when the case was closed.Data type: String

Maximum length: 4,000

</td></tr><tr><td>

closed\_at

</td><td id="casetable-closed_at-entry">

Date and time that the case was closed.Data type: String

</td></tr><tr><td>

closed\_by

</td><td id="casetable-closed_by-entry">

Sys\_id of the user that closed the case.Data type: String

Table: User \[sys\_user\]

</td></tr><tr><td>

cmdb\_ci

</td><td id="casetable-cmdb_ci-entry">

Sys\_id of the configuration item associated with the case.Data type: String

Table: Configuration Item \[cmdb\_ci\]

</td></tr><tr><td>

comments

</td><td id="casetable-comments-entry">

Additional comments about the case.Data type: String

Maximum length: 4,000

</td></tr><tr><td>

company

</td><td id="casetable-company-entry">

Sys\_id of the company associated with the case.Data type: String

Table: Company \[core\_company\]

</td></tr><tr><td>

consumer

</td><td id="casetable-consumer-entry">

Business-to-consumer cases only. Sys\_id of the person to contact with regard to this case.Data type: String

Table: Consumer \[csm\_consumer\]

</td></tr><tr><td>

contact

</td><td id="casetable-contact-entry">

Business-to-business based cases only. Sys\_id of the person to contact regarding this case.Data type: String

Table: Contact \[customer\_contact\]

</td></tr><tr><td>

contact\_time\_zone

</td><td id="casetable-contact_time_zone-entry">

Time zone of the contact associated with the case.Data type: String

Maximum length: 40

</td></tr><tr><td>

contact\_type

</td><td id="casetable-contact_type-entry">

Method in which the case was initially reported.Possible values:

-   chat
-   email
-   phone
-   social
-   web

Data type: String

Maximum length: 40

</td></tr><tr><td>

contract

</td><td id="casetable-contract-entry">

Sys\_id of the contract associated with the case. This contract contains information about the type of support that is provided to the company associated to the case. A contract can include a company and contact and the specific assets that are covered. A contract can also include multiple service entitlements and SLAs.Data type: String

Table: Contract \[ast\_contract\]

</td></tr><tr><td>

correlation\_display

</td><td id="casetable-correlation_display-entry">

Correlation display.Data type: String

Maximum length: 100

</td></tr><tr><td>

correlation\_id

</td><td id="casetable-correlation_id-entry">

Correlation identifier.Data type: String

Maximum length: 100

</td></tr><tr><td>

delivery\_plan

</td><td id="casetable-delivery_plan-entry">

Sys\_id of the parent execution plan for this case.Data type: String

Table: Execution Plan \[sc\_cat\_item\_delivery\_plan\]

</td></tr><tr><td>

delivery\_task

</td><td id="casetable-delivery_task-entry">

Sys\_id of the execution plan task.Data type: String

Table: Execution Plan Task \[sc\_cat\_item\_delivery\_task\]

</td></tr><tr><td>

description

</td><td id="casetable-description-entry">

Detailed description of the problem associated with the case. Data type: String

Maximum length: 4,000

</td></tr><tr><td>

due\_date

</td><td id="casetable-due_date-entry">

Date that the case is due to be closed.Data type: String

</td></tr><tr><td>

entitlement

</td><td id="casetable-entitlement-entry">

Sys\_id of the entitlement record associated with the case. Entitlements define the type of support that a customer receives as well as the supported communication channels. An entitlement can be associated with a product, an asset, an account, or a contract.Data type: String

Table: Entitlement \[service\_entitlement\]

</td></tr><tr><td>

escalation

</td><td id="casetable-escalation-entry">

Current escalation level.Possible values:

-   0: Normal
-   1: Moderate
-   2: High
-   3: Overdue

Data type: Number \(Integer\)

Default: 0

</td></tr><tr><td>

expected\_start

</td><td id="casetable-expected_start-entry">

Date and time when work is scheduled to begin on the case.Data type: String

</td></tr><tr><td>

first\_response\_time

</td><td id="casetable-first_response_time-entry">

Date and time when the first action was taken on the case.Data type: String

</td></tr><tr><td>

follow\_the\_sun

</td><td id="casetable-follow_the_sun-entry">

Flag that indicates whether the case should be handed-off for global follow-up.If a customer enters additional comments on a Priority 1 - Critical or a Priority 2 - High case, or if the case is escalated, the flag is automatically set to true.

Possible values:

-   true: Case should be handed-off for global follow-up
-   false: Case shouldn't be handed-off for global follow-up

Data type: Boolean

Default: false

</td></tr><tr><td>

group\_list

</td><td id="casetable-group_list-entry">

List of sys\_ids of the group records associated with the case.Data type: Array

Table: Group \[sys\_user\_group\]

</td></tr><tr><td>

impact

</td><td id="casetable-impact-entry">

Impact on customer.Possible values:

-   1: High
-   2: Medium
-   3: Low

Data type: Number \(Integer\)

Default: 3

</td></tr><tr><td>

knowledge

</td><td id="casetable-knowledge-entry">

Flag that indicates if there is a knowledge base article available for the specified issue.Possible values:

-   true: Knowledge base article is available for this issue
-   false: Knowledge base article is not available for this issue

Data type: Boolean

Default: false

</td></tr><tr><td>

location

</td><td id="casetable-location-entry">

Sys\_id of the record describing the company location.Data type: String

Table: Location \[cmn\_location\]

</td></tr><tr><td>

made\_sla

</td><td id="casetable-made_sla-entry">

Flag that indicates whether the case was resolved in alignment with the associated service level agreement.Possible values:

-   true: Case was resolved in alignment with SLA
-   false: Case wasn't resolved according to the SLA

Data type: Boolean

Default: true

</td></tr><tr><td>

major\_case\_state

</td><td id="casetable-major_case_state-entry">

Current state of the major case.Possible values:

-   accepted: Initial state when a manager creates a major case or when a manager promotes a candidate case.
-   canceled: Case is canceled.
-   proposed: Initial state when an agent or manager creates or proposes a candidate case.
-   rejected: Manager rejected candidate case.

Data type: String

Maximum length: 40

</td></tr><tr><td>

notes\_to\_comments

</td><td id="casetable-notes_to_comments-entry">

Flag that indicates whether to add the resolution notes to the comments.Possible values:

-   true: Resolutions notes, when added, are also added to the comments
-   false: Resolution notes in comments aren't required

Data type: Boolean

</td></tr><tr><td>

notify

</td><td id="casetable-notify-entry">

Method to use to notify contact/consumer.Possible values:

-   1: Do not notify
-   2: Send email
-   3: Telephone

Data type: Number \(Integer\)

Default: 1

</td></tr><tr><td>

number

</td><td id="casetable-number-entry">

Case number.Data type: String

Maximum length: 40

</td></tr><tr><td>

opened\_at

</td><td id="casetable-opened_at-entry">

Date and time that the case was opened.Data type: String

</td></tr><tr><td>

opened\_by

</td><td id="casetable-opened_by-entry">

Sys\_id of the person that initially opened the case.Data type: String

Table: User \[sys\_user\]

</td></tr><tr><td>

order

</td><td id="casetable-order-entry">

Order of the case.Data type: Number \(Integer\)

</td></tr><tr><td>

parent

</td><td id="casetable-parent-entry">

Sys\_id of the parent case to which this case \(child\) is associated.Data type: String

Table: Task \[task\]

</td></tr><tr><td>

partner

</td><td id="casetable-partner-entry">

Sys\_id of the partner associated with the case.Data type: String

Table: Account \[customer\_account\]

</td></tr><tr><td>

partner\_contact

</td><td id="casetable-partner_contact-entry">

Sys\_id of the partner contact associated with the case.Data type: String

Table: Contact \[customer\_contact\]

</td></tr><tr><td>

priority

</td><td id="casetable-priority-entry">

Priority of the case. Possible values:

-   1: Critical
-   2: High
-   3: Moderate
-   4: Low

Data type: Number \(Integer\)

Default: 4

</td></tr><tr><td>

probable\_cause

</td><td id="casetable-probable_cause-entry">

Possible cause of the issue associated with the case.Data type: String

Maximum length: 4,000

</td></tr><tr><td>

problem

</td><td id="casetable-problem-entry">

Sys\_id of the issue that the customer is encountering.Data type: String

Table: Problem \[problem\]

</td></tr><tr><td>

product

</td><td id="casetable-product-entry">

Sys\_id of the product model of the asset associated to the case. A model is a specific version or configuration of an asset \(for example, Apple Mac Book Pro\).Data type: String

Table: Product Model \[cmdb\_model\]

</td></tr><tr><td>

reassignment\_count

</td><td id="casetable-reassignment_count-entry">

Number of times that the case was reassigned to a person that is responsible for moving the case forward.Data type: Number \(Integer\)

Default: 0

</td></tr><tr><td>

recipient\_list

</td><td id="casetable-recipient_list-entry">

Sys\_id of the record that contains the list of recipients for communications about this case.Data type: String

Table: Recipients List \[sn\_publications\_recipients\_list\]

</td></tr><tr><td>

rejection\_goto

</td><td id="casetable-rejection_goto-entry">

Sys\_id of the task to execute if the case is rejected.Data type: String

Table: Task \[task\]

</td></tr><tr><td>

resolution\_code

</td><td id="casetable-resolution_code-entry">

Resolution state for the case, such as "Solved - Fixed by Support/Guidance provided". Data type: String

Maximum length: 40

</td></tr><tr><td>

resolved\_at

</td><td id="casetable-resolved_at-entry">

Date and time that the case was resolved.Data type: String

</td></tr><tr><td>

resolved\_by

</td><td id="casetable-resolved_by-entry">

Sys\_id of the person that resolved the case.Data type: String

Table: User \[sys\_user\]

</td></tr><tr><td>

short\_description

</td><td id="casetable-short_description-entry">

Concise description of the case. Data type: String

Maximum length: 160

</td></tr><tr><td>

skills

</td><td id="casetable-skills-entry">

List of the unique identifiers \(sys\_id\) of the skills needed to complete the case.Data type: String

Table: Skill \[cmn\_skill\]

</td></tr><tr><td>

sla\_due

</td><td id="casetable-sla_due-entry">

Date/time at which the case must be closed based on the associated service level agreement.Data type: String

</td></tr><tr><td>

social\_channel

</td><td>

Type of social media channel such as Twitter, Facebook, or Instagram.Data type: String

</td></tr><tr><td>

social\_handle

</td><td>

User handle on the channel.Data type: String

</td></tr><tr><td>

social\_handle\_type

</td><td>

Type of case to associate the social media profile.Valid values:

 -   account
-   consumer
-   contact

 Data type: String

</td></tr><tr><td>

social\_handle\_url

</td><td>

URL of the user's social media handle.Data type: String

</td></tr><tr><td>

social\_post\_url

</td><td>

URL of the social message from which the case is being generated.Data type: String

</td></tr><tr><td>

state

</td><td id="casetable-state-entry">

Current state of the case.Possible values:

-   1: New
-   3: Closed
-   6: Resolved
-   10: Open
-   18: Awaiting Info

Data type: Number \(Integer\)

Default: 1

</td></tr><tr><td>

subcategory

</td><td id="casetable-subcategory-entry">

Case subcategory.Possible values:

0: QuestionData type: Number \(Integer\)

Default: 0

</td></tr><tr><td>

support\_manager

</td><td id="casetable-support_manager-entry">

Sys\_id of the CSM manager assigned to the case.Data type: String

Table: User \[sys\_user\]

</td></tr><tr><td>

sync\_driver

</td><td id="casetable-sync_driver-entry">

Flag that indicates whether there's driver synchronization.Possible values:

-   true: Driver is synchronized
-   false: Driver isn't synchronized

Data type: Boolean

</td></tr><tr><td>

sys\_domain\_path

</td><td id="casetable-sys_domain_path-entry">

Domain path.Data type: String

Maximum length: 255

Default: /

</td></tr><tr><td>

time\_worked

</td><td id="casetable-time_worked-entry">

Total amount of time worked on the case.Data type: String

</td></tr><tr><td>

upon\_approval

</td><td id="casetable-upon_approval-entry">

Action to take if the case is approved.Possible values:

-   do\_nothing
-   proceed

Data type: String

Maximum length: 40

Default: proceed

</td></tr><tr><td>

upon\_reject

</td><td id="casetable-upon_reject-entry">

Action to take if the case is rejected.Possible values:

-   cancel
-   goto

Data type: String

Maximum length: 40

Default: cancel

</td></tr><tr><td>

urgency

</td><td id="casetable-urgency-entry">

Urgency of the case.Possible values:

-   1: High
-   2: Medium
-   3: Low

Data type: Number \(Integer\)

Default: 3

</td></tr><tr><td>

user\_input

</td><td id="casetable-user_input-entry">

Additional user input.Data type: String

Maximum length: 4,000

</td></tr><tr><td>

variables

</td><td id="casetable-variables-entry">

Name-value pairs of variables associated with the case.Data type: String

Maximum length: 40

</td></tr><tr><td>

watch\_list

</td><td id="casetable-watch_list-entry">

List of sys\_ids of the users who receive notifications about this case when additional comments are added or if the state of a case is changed to Resolved or Closed.Data type: Array

Table: User \[sys\_user\]

</td></tr><tr><td>

wf\_activity

</td><td id="casetable-wf_activity-entry">

Sys\_id of the workflow activity record associated with the case.Data type: String

Table: Workflow Activity \[wf\_activity\]

</td></tr><tr><td>

work\_end

</td><td id="casetable-work_end-entry">

Date and time work ended on the case.Data type: String

</td></tr><tr><td>

work\_notes\_list

</td><td id="casetable-work_notes_list-entry">

List of sys\_ids of the internal users who receive notifications about this case when work notes are added.Data type: Array

Table: User \[sys\_user\]

</td></tr><tr><td>

work\_start

</td><td id="casetable-work_start-entry">

Date and time that work started on the case.Data type: String

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
|201|New case record was successfully created.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|500|Internal Server Error. A logic error on the server-side code occurred.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Element

</th><th>

Description

</th></tr></thead><tbody><tr><td>

number

</td><td>

Associated case number.Data type: String

</td></tr><tr><td>

sys\_id

</td><td>

Sys\_id of the new case record created in the Case \[sn\_customerservice\_case\] table.Data type: String

</td></tr></tbody>
</table>### cURL request

The following example illustrates how to create a case based on a consumer and also create a new social media account that is associated with the case.

```
curl "https://instance.servicenow.com/api/sn_customerservice/case" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{ \
    consumer: \"cd97ef1ddb8bc7006b7a9646db9619ac\", \
    contact_type: \"social\", \
    priority: \"4\", \
    short_description: \"Consumer Test Case\", \
    social_channel: \"TWITTER\", \
    social_handle: \"consumertwo\", \
    social_handle_type: \"Consumer\", \
    social_handle_url: \"https://www.twitter.com/consumertwo\", \
    social_post_url: \"https://twitter.com/MuleSoft/status/829092185022750720\"}" \
--user "username":"password"

```

```
{
  "result": {
    "sys_id": "0397c743db436f0057c3fd441d96197f",
    "number": "CS0001005"
  }
}
```

### cURL request

The following example illustrates how to create a case for an account.

```
curl "https://instance.servicenow.com/api/sn_customerservice/case" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{ \
    account: \"051f62b0d7300200e5982cf65e610333\", \
    contact_type: \"phone\", \
    priority: \"1\", \
    short_description: \"Power Outage\"}" \
--user "username":"password"

```

```
{
  "result": {
    "sys_id": "b88366ffdb1b0b00216e9ee6db96190b",
    "number": "CS0001021"
  }
}
```

### cURL request

The following example illustrates how to create a case for a specific contact. Note that if an account is specified within the contact record, that account is automatically assigned to the case.

```
curl "https://instance.servicenow.com/api/sn_customerservice/case" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{ \
    contact: \"62fe1c97db76c3006b7a9646db961999\", \
    contact_type: \"phone\", \
    priority: \"3\", \
    short_description: \"Power Outage\"}" \
--user "username":"password"

```

```
{
  "result": {
    "sys_id": "bf916affdb1b0b00216e9ee6db961937",
    "number": "CS0001013"
  }
}
```

## Case - PUT /sn\_customerservice/case/\{id\}

Updates the specified existing Customer Service Management \(CSM\) case with the passed-in parameters.

**Warning:** This endpoint does not perform parameter validation as doing so can create excessive overhead. If a request parameter is misspelled, is not valid for the type of case, or is not supported by the endpoint, it is either ignored without warning or can cause unexpected results. For example, if you create a consumer or contact for the wrong type of case or mismatch a contact with an account.

**Warning:** By default, external users who have the sn\_customerservice.customer or sn\_customerservice.consumer role can only set the comments and state fields using this endpoint. Admins can enable external users to set additional fields by specifying the field names in the UPDATE\_ALLOWED\_FIELDS array defined in the CaseRESTAPIValidatorForExternalUser script include. Exercise caution when adding new fields to this array, as there may not be existing validators for input into those fields. For more information on script includes, see [Script includes](../../../script/server-scripting/concept/c_ScriptIncludes.md#).

**Note:** You can reference all sysparm query parameters using either their full name or their shortened name \(without the **sysparm\_** prefix\). For example, for **sysparm\_limit** you can also use **limit**.

### URL format

Versioned URL: `/api/sn_customerservice/{api_version}/case/{id}`

Default URL: `/api/sn_customerservice/case/{id}`

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

Sys\_id of the case to update.Table: Case \[sn\_customerservice\_case\]

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sysparm\_display\_value

</td><td id="entry-sysparm_display_value-REST_API">

Determines the type of data returned, either the actual values from the database or the display values of the fields. Display values are manipulated based on the actual value in the database and user or system settings and preferences.If returning display values, the value that is returned is dependent on the field type.

-   Choice fields: The database value may be a number, but the display value will be more descriptive.
-   Date fields: The database value is in UTC format, while the display value is based on the user's time zone.
-   Encrypted text: The database value is encrypted, while the displayed value is unencrypted based on the user's encryption context.
-   Reference fields: The database value is sys\_id, but the display value is a display field of the referenced record.

Data type: String

Valid values:

-   true: Returns the display values for all fields.
-   false: Returns the actual values from the database.
-   all: Returns both actual and display values.

Default: false

**Note:** There is no preferred method for setting this parameter. However, specifying the display value may cause performance issues since it is not reading directly from the database and may include referencing other fields and records. For more information on display values and actual values, see [Table API FAQs \(KB0534905\).](https://support.servicenow.com/kb_view.do?sysparm_article=KB0534905)

</td></tr><tr><td>

sysparm\_fields

</td><td id="sysparm_fields_entry-RESTAPI">

Comma-separated list of fields to return in the response. Invalid fields are ignored.Data type: String

Default: Return all fields.

</td></tr><tr><td>

sysparm\_get\_case\_details

</td><td id="sysparm_get_case_details-entry-RESTAPI">

Flag that indicates whether to return the updated case record.Valid values:

-   true: Return updated case record.
-   false: Do not return the updated case record.

Data type: Boolean

Default: false

</td></tr></tbody>
</table><table class="rest_api_request_body"><thead><tr><th>

Element

</th><th>

Description

</th></tr></thead><tbody><tr><td>

account

</td><td>

Sys\_id of the account associated with the case.Data type: String

Default: If **contact** specified, defaults to account specified in contact record.

Table: Account \[customer\_account\]

</td></tr><tr><td>

active

</td><td id="casetable-active-entry">

Flag that indicates whether the case is open and active.Possible values:

-   true: Case is active
-   false: Case is closed

Data type: Boolean

Default: true

</td></tr><tr><td>

active\_account\_escalation

</td><td id="casetable-active_account_escalation-entry">

Sys\_id of the active account escalation record associated with the case.Data type: String

Table: Escalation \[sn\_customerservice\_escalation\]

</td></tr><tr><td>

active\_escalation

</td><td id="casetable-active_escalation-entry">

Sys\_id of the active escalation record associated with the case.Data type: String

Table: Escalation \[sn\_customerservice\_escalation\]

</td></tr><tr><td>

activity\_due

</td><td id="casetable-activity_due-entry">

Date for which the associated case is expected to be completed.Data type: String

</td></tr><tr><td>

additional\_assignee\_list

</td><td id="casetable-additional_assignee_list-entry">

List of the sys\_ids of the additional persons \(other than the primary assignee\) that have been assigned to the account.Data type: Array

Maximum: 4,000

Table: User \[sys\_user\]

</td></tr><tr><td>

approval

</td><td id="casetable-approval-entry">

String that describes the type of approval required.Possible values:

-   approved
-   cancelled
-   duplicate
-   not\_required
-   not requested
-   rejected
-   requested

Data type: String

Maximum characters: 40

Default: not requested

</td></tr><tr><td>

assigned\_to

</td><td id="casetable-assigned_to-entry">

Sys\_id of the person assigned to the case.

Table: User \[sys\_user\]

 Data type: String

</td></tr><tr><td>

assignment\_group

</td><td id="casetable-aassignment_group-entry">

Sys\_id of the customer service agent group assigned to the case.Data type: String

Table: Group \[sys\_user\_group\]

</td></tr><tr><td>

business\_duration

</td><td id="casetable-business_duration-entry">

Length in calendar work hours, work days, and work weeks that it took to complete the case.Data type: String

</td></tr><tr><td>

business\_impact

</td><td id="casetable-business_impact-entry">

Impact of the issue on the associated customer.Data type: String

Maximum characters: 4,000

</td></tr><tr><td>

business\_service

</td><td id="casetable-business_service-entry">

Sys\_id of the service record associated with the case.Data type: String

Table: Service \[cmdb\_ci\_service\]

</td></tr><tr><td>

category

</td><td id="casetable-category-entry">

Case category.Possible values:

-   0: Question
-   1: Issue
-   2: Feature

Data type: Number \(Integer\)

Default: 1

</td></tr><tr><td>

cause

</td><td id="casetable-cause-entry">

Details about the cause of the problem.Data type: String

Maximum length: 4,000

</td></tr><tr><td>

caused\_by

</td><td id="casetable-caused_by-entry">

Sys\_id of the change request that caused the case to be created.Data type: String

Table: Change Request \[change\_request\]

</td></tr><tr><td>

change

</td><td id="casetable-change-entry">

Sys\_id of the change request that caused the case to be created.Data type: String

Table: Change Request \[change\_request\]

</td></tr><tr><td>

child\_case\_creation\_progress

</td><td id="casetable-child_case_creation_progress-entry">

Flag that indicates whether the case is a child case that was created from a major case.Possible values:

-   true: Child case created from a major case
-   false: Not a child case

Data type: Boolean

</td></tr><tr><td>

close\_notes

</td><td id="casetable-close_notes-entry">

Notes made when the case was closed.Data type: String

Maximum length: 4,000

</td></tr><tr><td>

closed\_at

</td><td id="casetable-closed_at-entry">

Date and time that the case was closed.Data type: String

</td></tr><tr><td>

closed\_by

</td><td id="casetable-closed_by-entry">

Sys\_id of the user that closed the case.Data type: String

Table: User \[sys\_user\]

</td></tr><tr><td>

cmdb\_ci

</td><td id="casetable-cmdb_ci-entry">

Sys\_id of the configuration item associated with the case.Data type: String

Table: Configuration Item \[cmdb\_ci\]

</td></tr><tr><td>

comments

</td><td id="casetable-comments-entry">

Additional comments about the case.Data type: String

Maximum length: 4,000

</td></tr><tr><td>

company

</td><td id="casetable-company-entry">

Sys\_id of the company associated with the case.Data type: String

Table: Company \[core\_company\]

</td></tr><tr><td>

consumer

</td><td id="casetable-consumer-entry">

Business-to-consumer cases only. Sys\_id of the person to contact with regard to this case.Data type: String

Table: Consumer \[csm\_consumer\]

</td></tr><tr><td>

contact

</td><td id="casetable-contact-entry">

Business-to-business based cases only. Sys\_id of the person to contact regarding this case.Data type: String

Table: Contact \[customer\_contact\]

</td></tr><tr><td>

contact\_time\_zone

</td><td id="casetable-contact_time_zone-entry">

Time zone of the contact associated with the case.Data type: String

Maximum length: 40

</td></tr><tr><td>

contact\_type

</td><td id="casetable-contact_type-entry">

Method in which the case was initially reported.Possible values:

-   chat
-   email
-   phone
-   social
-   web

Data type: String

Maximum length: 40

</td></tr><tr><td>

contract

</td><td id="casetable-contract-entry">

Sys\_id of the contract associated with the case. This contract contains information about the type of support that is provided to the company associated to the case. A contract can include a company and contact and the specific assets that are covered. A contract can also include multiple service entitlements and SLAs.Data type: String

Table: Contract \[ast\_contract\]

</td></tr><tr><td>

correlation\_display

</td><td id="casetable-correlation_display-entry">

Correlation display.Data type: String

Maximum length: 100

</td></tr><tr><td>

correlation\_id

</td><td id="casetable-correlation_id-entry">

Correlation identifier.Data type: String

Maximum length: 100

</td></tr><tr><td>

delivery\_plan

</td><td id="casetable-delivery_plan-entry">

Sys\_id of the parent execution plan for this case.Data type: String

Table: Execution Plan \[sc\_cat\_item\_delivery\_plan\]

</td></tr><tr><td>

delivery\_task

</td><td id="casetable-delivery_task-entry">

Sys\_id of the execution plan task.Data type: String

Table: Execution Plan Task \[sc\_cat\_item\_delivery\_task\]

</td></tr><tr><td>

description

</td><td id="casetable-description-entry">

Detailed description of the problem associated with the case. Data type: String

Maximum length: 4,000

</td></tr><tr><td>

due\_date

</td><td id="casetable-due_date-entry">

Date that the case is due to be closed.Data type: String

</td></tr><tr><td>

entitlement

</td><td id="casetable-entitlement-entry">

Sys\_id of the entitlement record associated with the case. Entitlements define the type of support that a customer receives as well as the supported communication channels. An entitlement can be associated with a product, an asset, an account, or a contract.Data type: String

Table: Entitlement \[service\_entitlement\]

</td></tr><tr><td>

escalation

</td><td id="casetable-escalation-entry">

Current escalation level.Possible values:

-   0: Normal
-   1: Moderate
-   2: High
-   3: Overdue

Data type: Number \(Integer\)

Default: 0

</td></tr><tr><td>

expected\_start

</td><td id="casetable-expected_start-entry">

Date and time when work is scheduled to begin on the case.Data type: String

</td></tr><tr><td>

first\_response\_time

</td><td id="casetable-first_response_time-entry">

Date and time when the first action was taken on the case.Data type: String

</td></tr><tr><td>

follow\_the\_sun

</td><td id="casetable-follow_the_sun-entry">

Flag that indicates whether the case should be handed-off for global follow-up.If a customer enters additional comments on a Priority 1 - Critical or a Priority 2 - High case, or if the case is escalated, the flag is automatically set to true.

Possible values:

-   true: Case should be handed-off for global follow-up
-   false: Case shouldn't be handed-off for global follow-up

Data type: Boolean

Default: false

</td></tr><tr><td>

group\_list

</td><td id="casetable-group_list-entry">

List of sys\_ids of the group records associated with the case.Data type: Array

Table: Group \[sys\_user\_group\]

</td></tr><tr><td>

impact

</td><td id="casetable-impact-entry">

Impact on customer.Possible values:

-   1: High
-   2: Medium
-   3: Low

Data type: Number \(Integer\)

Default: 3

</td></tr><tr><td>

knowledge

</td><td id="casetable-knowledge-entry">

Flag that indicates if there is a knowledge base article available for the specified issue.Possible values:

-   true: Knowledge base article is available for this issue
-   false: Knowledge base article is not available for this issue

Data type: Boolean

Default: false

</td></tr><tr><td>

location

</td><td id="casetable-location-entry">

Sys\_id of the record describing the company location.Data type: String

Table: Location \[cmn\_location\]

</td></tr><tr><td>

made\_sla

</td><td id="casetable-made_sla-entry">

Flag that indicates whether the case was resolved in alignment with the associated service level agreement.Possible values:

-   true: Case was resolved in alignment with SLA
-   false: Case wasn't resolved according to the SLA

Data type: Boolean

Default: true

</td></tr><tr><td>

major\_case\_state

</td><td id="casetable-major_case_state-entry">

Current state of the major case.Possible values:

-   accepted: Initial state when a manager creates a major case or when a manager promotes a candidate case.
-   canceled: Case is canceled.
-   proposed: Initial state when an agent or manager creates or proposes a candidate case.
-   rejected: Manager rejected candidate case.

Data type: String

Maximum length: 40

</td></tr><tr><td>

notes\_to\_comments

</td><td id="casetable-notes_to_comments-entry">

Flag that indicates whether to add the resolution notes to the comments.Possible values:

-   true: Resolutions notes, when added, are also added to the comments
-   false: Resolution notes in comments aren't required

Data type: Boolean

</td></tr><tr><td>

notify

</td><td id="casetable-notify-entry">

Method to use to notify contact/consumer.Possible values:

-   1: Do not notify
-   2: Send email
-   3: Telephone

Data type: Number \(Integer\)

Default: 1

</td></tr><tr><td>

number

</td><td id="casetable-number-entry">

Case number.Data type: String

Maximum length: 40

</td></tr><tr><td>

opened\_at

</td><td id="casetable-opened_at-entry">

Date and time that the case was opened.Data type: String

</td></tr><tr><td>

opened\_by

</td><td id="casetable-opened_by-entry">

Sys\_id of the person that initially opened the case.Data type: String

Table: User \[sys\_user\]

</td></tr><tr><td>

order

</td><td id="casetable-order-entry">

Order of the case.Data type: Number \(Integer\)

</td></tr><tr><td>

parent

</td><td id="casetable-parent-entry">

Sys\_id of the parent case to which this case \(child\) is associated.Data type: String

Table: Task \[task\]

</td></tr><tr><td>

partner

</td><td id="casetable-partner-entry">

Sys\_id of the partner associated with the case.Data type: String

Table: Account \[customer\_account\]

</td></tr><tr><td>

partner\_contact

</td><td id="casetable-partner_contact-entry">

Sys\_id of the partner contact associated with the case.Data type: String

Table: Contact \[customer\_contact\]

</td></tr><tr><td>

priority

</td><td id="casetable-priority-entry">

Priority of the case. Possible values:

-   1: Critical
-   2: High
-   3: Moderate
-   4: Low

Data type: Number \(Integer\)

Default: 4

</td></tr><tr><td>

probable\_cause

</td><td id="casetable-probable_cause-entry">

Possible cause of the issue associated with the case.Data type: String

Maximum length: 4,000

</td></tr><tr><td>

problem

</td><td id="casetable-problem-entry">

Sys\_id of the issue that the customer is encountering.Data type: String

Table: Problem \[problem\]

</td></tr><tr><td>

product

</td><td id="casetable-product-entry">

Sys\_id of the product model of the asset associated to the case. A model is a specific version or configuration of an asset \(for example, Apple Mac Book Pro\).Data type: String

Table: Product Model \[cmdb\_model\]

</td></tr><tr><td>

reassignment\_count

</td><td id="casetable-reassignment_count-entry">

Number of times that the case was reassigned to a person that is responsible for moving the case forward.Data type: Number \(Integer\)

Default: 0

</td></tr><tr><td>

recipient\_list

</td><td id="casetable-recipient_list-entry">

Sys\_id of the record that contains the list of recipients for communications about this case.Data type: String

Table: Recipients List \[sn\_publications\_recipients\_list\]

</td></tr><tr><td>

rejection\_goto

</td><td id="casetable-rejection_goto-entry">

Sys\_id of the task to execute if the case is rejected.Data type: String

Table: Task \[task\]

</td></tr><tr><td>

resolution\_code

</td><td id="casetable-resolution_code-entry">

Resolution state for the case, such as "Solved - Fixed by Support/Guidance provided". Data type: String

Maximum length: 40

</td></tr><tr><td>

resolved\_at

</td><td id="casetable-resolved_at-entry">

Date and time that the case was resolved.Data type: String

</td></tr><tr><td>

resolved\_by

</td><td id="casetable-resolved_by-entry">

Sys\_id of the person that resolved the case.Data type: String

Table: User \[sys\_user\]

</td></tr><tr><td>

short\_description

</td><td id="casetable-short_description-entry">

Concise description of the case. Data type: String

Maximum length: 160

</td></tr><tr><td>

skills

</td><td id="casetable-skills-entry">

List of the unique identifiers \(sys\_id\) of the skills needed to complete the case.Data type: String

Table: Skill \[cmn\_skill\]

</td></tr><tr><td>

sla\_due

</td><td id="casetable-sla_due-entry">

Date/time at which the case must be closed based on the associated service level agreement.Data type: String

</td></tr><tr><td>

social\_channel

</td><td>

Type of social media channel such as Twitter, Facebook, or Instagram.Data type: String

</td></tr><tr><td>

social\_handle

</td><td>

User handle on the channel.Data type: String

</td></tr><tr><td>

social\_handle\_type

</td><td>

Type of case to associate the social media profile.Valid values:

 -   account
-   contact
-   consumer

 Data type: String

</td></tr><tr><td>

social\_handle\_url

</td><td>

URL of the user's social media handle.Data type: String

</td></tr><tr><td>

social\_post\_url

</td><td>

URL of the social message from which the case is being generated.Data type: String

</td></tr><tr><td>

state

</td><td id="casetable-state-entry">

Current state of the case.Possible values:

-   1: New
-   3: Closed
-   6: Resolved
-   10: Open
-   18: Awaiting Info

Data type: Number \(Integer\)

Default: 1

</td></tr><tr><td>

subcategory

</td><td id="casetable-subcategory-entry">

Case subcategory.Possible values:

0: QuestionData type: Number \(Integer\)

Default: 0

</td></tr><tr><td>

support\_manager

</td><td id="casetable-support_manager-entry">

Sys\_id of the CSM manager assigned to the case.Data type: String

Table: User \[sys\_user\]

</td></tr><tr><td>

sync\_driver

</td><td id="casetable-sync_driver-entry">

Flag that indicates whether there's driver synchronization.Possible values:

-   true: Driver is synchronized
-   false: Driver isn't synchronized

Data type: Boolean

</td></tr><tr><td>

sys\_domain\_path

</td><td id="casetable-sys_domain_path-entry">

Domain path.Data type: String

Maximum length: 255

Default: /

</td></tr><tr><td>

time\_worked

</td><td id="casetable-time_worked-entry">

Total amount of time worked on the case.Data type: String

</td></tr><tr><td>

upon\_approval

</td><td id="casetable-upon_approval-entry">

Action to take if the case is approved.Possible values:

-   do\_nothing
-   proceed

Data type: String

Maximum length: 40

Default: proceed

</td></tr><tr><td>

upon\_reject

</td><td id="casetable-upon_reject-entry">

Action to take if the case is rejected.Possible values:

-   cancel
-   goto

Data type: String

Maximum length: 40

Default: cancel

</td></tr><tr><td>

urgency

</td><td id="casetable-urgency-entry">

Urgency of the case.Possible values:

-   1: High
-   2: Medium
-   3: Low

Data type: Number \(Integer\)

Default: 3

</td></tr><tr><td>

user\_input

</td><td id="casetable-user_input-entry">

Additional user input.Data type: String

Maximum length: 4,000

</td></tr><tr><td>

variables

</td><td id="casetable-variables-entry">

Name-value pairs of variables associated with the case.Data type: String

Maximum length: 40

</td></tr><tr><td>

watch\_list

</td><td id="casetable-watch_list-entry">

List of sys\_ids of the users who receive notifications about this case when additional comments are added or if the state of a case is changed to Resolved or Closed.Data type: Array

Table: User \[sys\_user\]

</td></tr><tr><td>

wf\_activity

</td><td id="casetable-wf_activity-entry">

Sys\_id of the workflow activity record associated with the case.Data type: String

Table: Workflow Activity \[wf\_activity\]

</td></tr><tr><td>

work\_end

</td><td id="casetable-work_end-entry">

Date and time work ended on the case.Data type: String

</td></tr><tr><td>

work\_notes\_list

</td><td id="casetable-work_notes_list-entry">

List of sys\_ids of the internal users who receive notifications about this case when work notes are added.Data type: Array

Table: User \[sys\_user\]

</td></tr><tr><td>

work\_start

</td><td id="casetable-work_start-entry">

Date and time that work started on the case.Data type: String

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
|201|Successful.|
|400|Bad Request. A bad request type or malformed request was detected.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|500|Internal Server Error. A logic error on the server-side code occurred.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Element

</th><th>

Description

</th></tr></thead><tbody><tr><td>

account

</td><td id="casetable-account-entry">

Sys\_id of the account record associated with the case.

Data type: String

Table: Account \[customer\_account\]

</td></tr><tr><td>

account

</td><td>

Account details.Data type: Object

```
"account": {
  "account_code": "String",
  "account_parent": "String",
  "account_path": "String",
  "active_escalation": "String",
  "apple_icon": Image,
  "banner_image": Image,
  "banner_image_light": Image,
  "banner_text": "String",
  "city": "String",
  "contact": "String",
  "country": "String",
  "customer": "String",
  "discount": "String",
  "fax_phone": "String",
  "fiscal_year": "String",
  "lat_long_error": "String",
  "latitude": "String",
  "longitude": "String",
  "market_cap": "String",
  "name": "String",
  "notes": "String",
  "num_employees": Number,
  "number": "String",
  "parent": "String",
  "partner": "String",
  "phone": "String",
  "primary": Boolean,
  "primary_contact": "String",
  "profits": Number,
  "publicly_traded": Boolean,
  "rank_tier": "String",
  "registration_code": "String",
  "revenue_per_year": Number,
  "state": "String",
  "stock_price": "String",
  "stock_symbol": "String",
  "street": "String",
  "sys_class_name": "String",
  "sys_created_by": "String",
  "sys_created_on": "String",
  "sys_id": "String",
  "sys_mod_count": Number,
  "sys_updated_by": "String",
  "sys_updated_on": "String",
  "theme": "String",
  "vendor": Boolean,
  "vendor_manager": "String",
  "vendor_type": "String",
  "website": "String",
  "zip": "String
}
```

</td></tr><tr><td>

account.account\_code

</td><td>

Unique combination of values that an application uses to identify budget forecasts and budget plans.Data type: String

Maximum length: 255

</td></tr><tr><td>

account.account\_parent

</td><td>

Sys\_id of the parent account of this account. Located in the Account \[customer\_account\] table.Data type: String

</td></tr><tr><td>

account.account\_path

</td><td>

Path from the parent to the child accounts in the account hierarchy.Data type: String

Maximum length: 255

</td></tr><tr><td>

account.active\_escalation

</td><td>

Sys\_id of the active escalation associated with the account.Data type: String

Table: Escalation \[sn\_customerservice\_escalation\]

</td></tr><tr><td>

account.apple\_icon

</td><td>

Icon for iPhone home page bookmarks.Data type: Image

</td></tr><tr><td>

account.banner\_image

</td><td>

Banner image that appears on the customer portal.Data type: Image

</td></tr><tr><td>

account.banner\_image\_light

</td><td>

Small banner image.Data type: Image

</td></tr><tr><td>

account.banner\_text

</td><td>

Banner text that appears on the customer portal.Data type: String

Maximum length: 4,000

</td></tr><tr><td>

account.city

</td><td>

City in which the company that is associated with this account resides.Data type: String

Maximum length: 50

</td></tr><tr><td>

account.contact

</td><td>

Sys\_id of a contact record associated with this account.Data type: String

Table: User \[sys\_user\]

</td></tr><tr><td>

account.country

</td><td>

Country in which the company that is associated with this account resides.Data type: String

Maximum length: 40

Default: USA

</td></tr><tr><td>

account.customer

</td><td>

Flag that indicates whether the account is a customer account, as opposed to a partner account.Possible values:

-   true: Customer account
-   false: Partner account

Data type: Boolean

Default: false

</td></tr><tr><td>

account.discount

</td><td>

Discount given to the account on purchases.Data type: Number

Maximum length: 15

</td></tr><tr><td>

account.fax\_phone

</td><td>

Primary fax phone number for the company associated with this account.Data type: String

Maximum length: 40

</td></tr><tr><td>

account.fiscal\_year

</td><td>

Fiscal year for the company associated with the account.Data type: String

</td></tr><tr><td>

account.lat\_long\_error

</td><td>

Difference in the actual location as compared to latitude and longitude information.Data type: String

Maximum length: 1,000

</td></tr><tr><td>

account.latitude

</td><td>

Latitude of the company associated with this account.Data type: Number \(floating point number\)

Maximum length: 40

</td></tr><tr><td>

account.longitude

</td><td>

Longitude of the company associated with this account.Data type: Number \(floating point number\)

Maximum length: 40

</td></tr><tr><td>

account.manufacturer

</td><td>

Flag that indicates whether the company associated with this account manufactures goods.Possible values:

-   true: Manufactures goods
-   false: Does not manufacture goods

Data type: Boolean

Default: false

</td></tr><tr><td>

account.market\_cap

</td><td>

Market value of the associated company's publicly traded stock shares.Data type: Number \(currency\)

Maximum length: 20

</td></tr><tr><td>

account.name

</td><td>

Name of the company associated with this account.Data type: String

Maximum length: 80

</td></tr><tr><td>

account.notes

</td><td>

Additional information about the company.Data type: String

Maximum length: 4,000

</td></tr><tr><td>

account.num\_employees

</td><td>

Number of people employed by the company.Data type: Number \(Integer\)

Maximum length: 40

</td></tr><tr><td>

account.number

</td><td>

Number that identifies this account.Data type: String

Maximum length: 40

</td></tr><tr><td>

account.parent

</td><td>

Sys\_id of the parent account of this account.Data type: String

Table: Company \[core\_company\]

</td></tr><tr><td>

account.partner

</td><td>

Flag that indicates whether the account is a partner account or a customer account.Possible values:

-   true: Partner account
-   false: Customer account

Data type: Boolean

Default: false

</td></tr><tr><td>

account.phone

</td><td>

Primary phone number for the company.Data type: String

</td></tr><tr><td>

account.primary

</td><td>

Flag that indicates whether this is a primary account.Possible values:

-   true: Primary account
-   false: Secondary account

Data type: Boolean

Default: false

</td></tr><tr><td>

account.primary\_contact

</td><td>

Sys\_id of the primary contact for the account.Data type: String

Table: Contact \[customer\_contact\]

</td></tr><tr><td>

account.profits

</td><td>

Profit information entered for this account.Data type: Number \(Currency\)

Maximum length: 40

</td></tr><tr><td>

account.publicly\_traded

</td><td>

Flag that indicates whether the company associated with this account is publicly traded on the stock exchange.Possible values:

-   true: Publicly traded
-   false: Private company

Data type: Boolean

</td></tr><tr><td>

account.rank\_tier

</td><td>

Type of account.Possible values:

-   blacklist
-   other
-   strategic
-   tactical
-   valued

Data type: String

Maximum length: 40

</td></tr><tr><td>

account.registration\_code

</td><td>

Unique code that customers use when requesting a login on the customer portal. This code provides a method for validating the customer on the company before granting access.Data type: String

Maximum length: 40

</td></tr><tr><td>

account.revenue\_per\_year

</td><td>

Revenue produced by the company associated with this account.Data type: Number \(Currency\)

Maximum length: 20

</td></tr><tr><td>

account.state

</td><td>

State in which the company resides.Data type: String

Maximum length: 40

</td></tr><tr><td>

account.stock\_price

</td><td>

Price of the company stock.Data type: String

Maximum length: 40

</td></tr><tr><td>

account.stock\_symbol

</td><td>

Stock symbol of the company.Data type: String

Maximum length: 40

</td></tr><tr><td>

account.street

</td><td>

Street address of the company.Data type: String

Maximum length: 255

</td></tr><tr><td>

account.sys\_class\_name

</td><td>

Table that contains the associated account record.Data type: String

</td></tr><tr><td>

account.sys\_created\_by

</td><td>

User that originally created the account.Data type: String

Maximum length: 40

</td></tr><tr><td>

account.sys\_created\_on

</td><td>

Date and time that the account was originally created.Data type: String

</td></tr><tr><td>

account.sys\_id

</td><td>

Sys\_id for the account record.Data type: String

</td></tr><tr><td>

account.sys\_mod\_count

</td><td>

Number of times the account information has been updated.Data type: Number \(Integer\)

</td></tr><tr><td>

account.sys\_updated\_by

</td><td>

User that last modified the account information.Data type: String

Maximum length: 40

</td></tr><tr><td>

account.sys\_updated\_on

</td><td>

Date and time the account information was last updated.Data type: String

</td></tr><tr><td>

account.theme

</td><td>

Sys\_id of the customer portal theme used by this account.Data type: String

Table: Theme \[sys\_ui\_theme\]

</td></tr><tr><td>

account.vendor

</td><td>

Flag that indicates whether the company associated with this account is a vendor.Possible values:

-   true: Vendor
-   false: Not a vendor

Data type: Boolean

Default: false

</td></tr><tr><td>

account.vendor\_manager

</td><td>

List of sys\_ids of the vendor managers for the account.Data type: String

Table: User \[sys\_user\]

</td></tr><tr><td>

account.vendor\_type

</td><td>

List of sys\_ids of the type of vendor such as, applications, hardware, services, or software.Data type: String

Table: Vendor Type \[vendor\_type\]

</td></tr><tr><td>

account.website

</td><td>

URL of the website for the company.Data type: String

Maximum length: 1,024

</td></tr><tr><td>

account.zip

</td><td>

Zip code of the company.Data type: String

Maximum length: 40

</td></tr><tr><td>

active

</td><td id="d4583e83">

Flag that indicates whether the case is open and active.Possible values:

-   true: Case is active
-   false: Case is closed

Data type: Boolean

Default: true

</td></tr><tr><td>

active\_account\_escalation

</td><td id="d4583e106">

Sys\_id of the active account escalation record associated with the case.Data type: String

Table: Escalation \[sn\_customerservice\_escalation\]

</td></tr><tr><td>

active\_escalation

</td><td id="d4583e119">

Sys\_id of the active escalation record associated with the case.Data type: String

Table: Escalation \[sn\_customerservice\_escalation\]

</td></tr><tr><td>

activity\_due

</td><td id="d4583e132">

Date for which the associated case is expected to be completed.Data type: String

</td></tr><tr><td>

additional\_assignee\_list

</td><td id="d4583e144">

List of the sys\_ids of the additional persons \(other than the primary assignee\) that have been assigned to the account.Data type: Array

Maximum: 4,000

Table: User \[sys\_user\]

</td></tr><tr><td>

approval

</td><td id="d4583e159">

String that describes the type of approval required.Possible values:

-   approved
-   cancelled
-   duplicate
-   not\_required
-   not requested
-   rejected
-   requested

Data type: String

Maximum characters: 40

Default: not requested

</td></tr><tr><td>

approval\_history

</td><td id="casetable-approval_history-entry">

List of all approvals associated with the case.Data type: String

Maximum characters: 4,000

</td></tr><tr><td>

approval\_set

</td><td id="casetable-approval_set-entry">

Date and time that the associated action was approved.Data type: String

</td></tr><tr><td>

asset

</td><td id="casetable-asset-entry">

Sys\_id of the asset record associated with the case.Data type: String

Table: Asset \[alm\_asset\]

</td></tr><tr><td>

assigned\_to

</td><td id="d4583e254">

Sys\_id of the person assigned to the case.

Table: User \[sys\_user\]

 Data type: String

</td></tr><tr><td>

assignment\_group

</td><td id="d4583e271">

Sys\_id of the customer service agent group assigned to the case.Data type: String

Table: Group \[sys\_user\_group\]

</td></tr><tr><td>

business\_duration

</td><td id="d4583e307">

Length in calendar work hours, work days, and work weeks that it took to complete the case.Data type: String

</td></tr><tr><td>

business\_impact

</td><td id="d4583e318">

Impact of the issue on the associated customer.Data type: String

Maximum characters: 4,000

</td></tr><tr><td>

business\_service

</td><td id="d4583e331">

Sys\_id of the service record associated with the case.Data type: String

Table: Service \[cmdb\_ci\_service\]

</td></tr><tr><td>

case

</td><td id="casetable-case-entry">

Case short description and case number.Data type: String

Maximum length: 300

</td></tr><tr><td>

case\_report

</td><td id="casetable-case_report-entry">

Sys\_id of the associated case report.Data type: String

Table: Case Report \[sn\_customerservice\_case\_report\]

</td></tr><tr><td>

category

</td><td id="d4583e384">

Case category.Possible values:

-   0: Question
-   1: Issue
-   2: Feature

Data type: Number \(Integer\)

Default: 1

</td></tr><tr><td>

cause

</td><td id="d4583e410">

Details about the cause of the problem.Data type: String

Maximum length: 4,000

</td></tr><tr><td>

caused\_by

</td><td id="d4583e423">

Sys\_id of the change request that caused the case to be created.Data type: String

Table: Change Request \[change\_request\]

</td></tr><tr><td>

change

</td><td id="d4583e437">

Sys\_id of the change request that caused the case to be created.Data type: String

Table: Change Request \[change\_request\]

</td></tr><tr><td>

child\_case\_creation\_progress

</td><td id="d4583e450">

Flag that indicates whether the case is a child case that was created from a major case.Possible values:

-   true: Child case created from a major case
-   false: Not a child case

Data type: Boolean

</td></tr><tr><td>

closed\_at

</td><td id="d4583e471">

Date and time that the case was closed.Data type: String

</td></tr><tr><td>

closed\_by

</td><td id="d4583e482">

Sys\_id of the user that closed the case.Data type: String

Table: User \[sys\_user\]

</td></tr><tr><td>

close\_notes

</td><td id="d4583e495">

Notes made when the case was closed.Data type: String

Maximum length: 4,000

</td></tr><tr><td>

cmdb\_ci

</td><td id="d4583e508">

Sys\_id of the configuration item associated with the case.Data type: String

Table: Configuration Item \[cmdb\_ci\]

</td></tr><tr><td>

comments

</td><td id="d4583e522">

Additional comments about the case.Data type: String

Maximum length: 4,000

</td></tr><tr><td>

comments\_and\_work\_notes

</td><td id="casetable-comments_and_work_notes-entry">

Comments and work notes entered for the case.Data type: String

Maximum length: 4,000

</td></tr><tr><td>

company

</td><td id="d4583e548">

Sys\_id of the company associated with the case.Data type: String

Table: Company \[core\_company\]

</td></tr><tr><td>

consumer

</td><td id="d4583e561">

Business-to-consumer cases only. Sys\_id of the person to contact with regard to this case.Data type: String

Table: Consumer \[csm\_consumer\]

</td></tr><tr><td>

consumer

</td><td>

Array of parameters for business-to-consumer cases.

</td></tr><tr><td>

consumer.active

</td><td>

Flag that indicates whether the consumer is active.Possible values:

-   true: Consumer active
-   false: Consumer de-activated

Data type: Boolean

Default: true

</td></tr><tr><td>

consumer.business\_phone

</td><td>

Business phone number of the consumer.Data type: String

Maximum length: 40

</td></tr><tr><td>

consumer.city

</td><td>

City in which the consumer resides.Data type: String

Maximum length: 100

</td></tr><tr><td>

consumer.country

</td><td>

Country in which the consumer resides.Data type: String

Maximum length: 40

</td></tr><tr><td>

consumer.date\_format

</td><td>

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

consumer.email

</td><td>

Email address of the consumer.Data type: String

Maximum length: 100

</td></tr><tr><td>

consumer.fax

</td><td>

Fax number of the consumer.Data type: String

Maximum length: 40

</td></tr><tr><td>

consumer.first\_name

</td><td>

Consumer first name.Data type: String

Maximum length: 50

</td></tr><tr><td>

consumer.gender

</td><td>

Gender of the consumer.Data type: String

Maximum length: 40

</td></tr><tr><td>

consumer.home\_phone

</td><td>

Home phone number of the consumer.Data type: String

Maximum length: 40

</td></tr><tr><td>

consumer.household

</td><td>

Sys\_id of the record that describes the household characteristics.Data type: String

Table: Household \[csm\_household\]

</td></tr><tr><td>

consumer.last\_name

</td><td>

Consumer last name.Data type: String

Maximum length: 50

</td></tr><tr><td>

consumer.middle\_name

</td><td>

Consumer middle name.Data type: String

Maximum length: 50

</td></tr><tr><td>

consumer.mobile\_phone

</td><td>

Consumer mobile phone number.Data type: String

Maximum length: 40

</td></tr><tr><td>

consumer.name

</td><td>

Consumer full name; first\_name+middle\_name+last\_name.Data type: String

Maximum length: 152

</td></tr><tr><td>

consumer.notes

</td><td>

Notes on consumer.Data type: String

Maximum length: 4,000

</td></tr><tr><td>

consumer.notification

</td><td>

Indicates whether the consumer should receive notifications.Valid values:

-   1: Disabled
-   2: Enabled

Data type: Number \(Integer\)

Maximum length: 40

Default: 2

</td></tr><tr><td>

consumer.number

</td><td>

Unique number associated with the consumer.Data type: String

Maximum length: 40

</td></tr><tr><td>

consumer.photo

</td><td>

Photo of the consumer.Data type: Image

</td></tr><tr><td>

consumer.preferred\_language

</td><td>

Consumer primary language.Data type: String

Maximum length: 3

</td></tr><tr><td>

consumer.prefix

</td><td>

Consumer name prefix such as, Dr., Mr., Mrs., or Ms.Data type: String

Maximum length: 40

</td></tr><tr><td>

consumer.primary

</td><td>

Flag that indicates whether this is the primary consumer.Possible values:

-   true: Primary consumer
-   false: Not primary consumer

Data type: Boolean

Default: false

</td></tr><tr><td>

consumer.state

</td><td>

State in which the consumer resides.Data type: String

Maximum length: 100

</td></tr><tr><td>

consumer.street

</td><td>

Consumer street address.Data type: String

Maximum length: 255

</td></tr><tr><td>

consumer.suffix

</td><td>

Consumer name suffix such as Jr., Sr., or II.Data type: String

</td></tr><tr><td>

consumer.sys\_created\_by

</td><td>

User that created the consumer record.Data type: String

Maximum length: 40

</td></tr><tr><td>

consumer.sys\_created\_on

</td><td>

Date and time the consumer record was originally created.Data type: String

</td></tr><tr><td>

consumer.sys\_domain

</td><td>

ServiceNow domain in which the consumer information resides.Data type: String

</td></tr><tr><td>

consumer.sys\_id

</td><td>

Unique identifier for the consumer.Data type: String

</td></tr><tr><td>

consumer.sys\_mod\_count

</td><td>

Number of times that the associated consumer information has been modified.Data type: Number \(Integer\)

</td></tr><tr><td>

consumer.sys\_updated\_by

</td><td>

User that last updated the consumer information.Data type: String

Maximum length: 40

</td></tr><tr><td>

consumer.sys\_updated\_on

</td><td>

Date and time when the consumer information was last updated.Data type: String

</td></tr><tr><td>

consumer.time\_format

</td><td>

Format in which to display time.Valid values:

-   hh.mm.ss a: hh.mm.ss \(12 hour\)
-   hh:mm:ss a: hh:mm:ss \(12 hour\)
-   HH.mm.ss: hh.mm.ss \(24 hour\)
-   HH:mm:ss: hh:mm:ss \(24 hour\)

Data type: String

Maximum length: 40

Default: blank \(system time format\)

</td></tr><tr><td>

consumer.time\_zone

</td><td>

Consumer time zone, such as Canada/Central or US/Eastern.Data type: String

Maximum length: 40

</td></tr><tr><td>

consumer.title

</td><td>

Consumer business title such as Manager, Software Developer, or Contractor.Data type: String

Maximum length: 60

</td></tr><tr><td>

consumer.user

</td><td>

Sys\_id of the consumer user. Data type: String

Table: Consumer User \[csm\_consumer\_user\]

</td></tr><tr><td>

consumer.zip

</td><td>

Consumer zip code. Data type: String

Maximum length: 40

</td></tr><tr><td>

contact

</td><td id="d4583e574">

Business-to-business based cases only. Sys\_id of the person to contact regarding this case.Data type: String

Table: Contact \[customer\_contact\]

</td></tr><tr><td>

contact

</td><td>

Array of contact parameters for business-to-business cases.

</td></tr><tr><td>

contact.account

</td><td>

Sys\_id of the account record to which the contact is associated.Data type: String

Table: Account \[customer\_account\]

</td></tr><tr><td>

contact.active

</td><td>

Flag that indicates whether the contact is active within the system.Possible values:

-   true: Contact is active
-   false: Contact is inactive

Data type: Boolean

Default: true

</td></tr><tr><td>

contact.agent\_status

</td><td>

Status of the agent.Possible values:

-   Off work
-   On break
-   On route
-   On site

Data type: String

Maximum length: 40

</td></tr><tr><td>

contact.building

</td><td>

Sys\_id of the record that describes the building in which the contact resides.Data type: String

Table: Building \[cmn\_building\]

</td></tr><tr><td>

contact.calendar\_integration

</td><td>

Calendar application that the contact uses.1: Outlook

Data type: Number \(Integer\)

Default: 1

</td></tr><tr><td>

contact.city

</td><td>

City in which the contact resides.Data type: String

Maximum length: 40

</td></tr><tr><td>

contact.company

</td><td>

Sys\_id of the company record to which the contact is associated.Data type: String

Table: Company \[core\_company\]

</td></tr><tr><td>

contact.cost\_center

</td><td>

Sys\_id of the cost center associated with the contact.Data type: String

Table: Cost Center \[cmn\_cost\_center\]

</td></tr><tr><td>

contact.country

</td><td>

Country code of the country in which the contact resides.Data type: String

Maximum length: 3

</td></tr><tr><td>

contact.date\_format

</td><td>

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

contact.default\_perspective

</td><td>

Sys\_id of the default perspective for the contact.Data type: String

Table: Menu List \[sys\_perspective\]

</td></tr><tr><td>

contact.department

</td><td>

Sys\_id of the department associated with the contact.Data type: String

Table: Department \[cmn\_department\]

</td></tr><tr><td>

contact.edu\_status

</td><td>

Education status of the associated contact.Data type: String

Maximum length: 40

Default: faculty

</td></tr><tr><td>

contact.email

</td><td>

Contact email address.Data type: String

</td></tr><tr><td>

contact.employee\_number

</td><td>

Contact employee number.Data type: String

</td></tr><tr><td>

contact.enable\_multifactor\_authn

</td><td>

Flag that indicates whether multifactor authorization is required for the contact to log in to the service portal.Possible values:

-   true: Multifactor authorization enabled
-   false: Multifactor authorization disabled

Data type: Boolean

Default: false

</td></tr><tr><td>

contact.failed\_attempts

</td><td>

Number of failed log in attempts.Data type: Number \(Integer\)

</td></tr><tr><td>

contact.first\_name

</td><td>

Contact first name.Data type: String

Maximum length: 50

</td></tr><tr><td>

contact.gender

</td><td>

Contact gender.Data type: String

Maximum length: 40

</td></tr><tr><td>

contact.geolocation\_tracked

</td><td>

Flag that indicates whether the contact location is obtained through geotracking.Possible values:

-   true: Contact location obtained through geotracking
-   false: Contact location not obtained through geotracking

Data type: Boolean

Default value: false

</td></tr><tr><td>

contact.home\_phone

</td><td>

Contact home phone number.Data type: String

Maximum length: 40

</td></tr><tr><td>

contact.internal\_integration\_user

</td><td>

Flag that indicates whether the contact is an internal integration user.Possible values:

-   true: Internal integration user
-   false: Other type of user

Data type: Boolean

Default: false

</td></tr><tr><td>

contact.introduction

</td><td>

IntroductionData type: String

Maximum length: 40

</td></tr><tr><td>

contact.last\_login

</td><td>

Date on which the contact last logged into the system.Data type: String \(Date\)

</td></tr><tr><td>

contact.last\_login\_device

</td><td>

Device the consumer used the last time they logged in to the system.Data type: String

Maximum length: 40

</td></tr><tr><td>

contact.last\_login\_time

</td><td>

Date and time the contact logged in to the system.Data type: String \(Date/time\)

</td></tr><tr><td>

contact.last\_name

</td><td>

Contact last name.Data type: String

Maximum length: 50

</td></tr><tr><td>

contact.last\_position\_update

</td><td>

Date and time the last position was updated.Data type: String \(Date/time\)

</td></tr><tr><td>

contact.latitude

</td><td>

Latitude coordinate of the contact.Data type: Number \(Floating point\)

Maximum length: 40

</td></tr><tr><td>

contact.ldap\_server

</td><td>

Sys\_id of the LDAP server used by the contact to last log in to the system. Data type: String

Table: LDAP Server \[ldap\_server\_config\]

</td></tr><tr><td>

contact.location

</td><td>

Sys\_id of the record that describes the location of the contactData type: String

Table: Location \[cmn\_location\]

</td></tr><tr><td>

contact.locked\_out

</td><td>

Flag that indicates if the contact is locked-out.Possible values:

-   true: Contact locked-out
-   false: Contact not locked-out

Data type: Boolean

Default: false

</td></tr><tr><td>

contact.longitude

</td><td>

Longitude coordinate of the contact.Data type: Number \(Floating point\)

Maximum length: 40

</td></tr><tr><td>

contact.manager

</td><td>

Sys\_id of the record that describes the direct supervisor of the contact.Data type: String

Table: User \[sys\_user\]

</td></tr><tr><td>

contact.middle\_name

</td><td>

Contact middle name.Data type: Number \(Floating point\)

Maximum length: 50

</td></tr><tr><td>

contact.mobile\_phone

</td><td>

Contact mobile phone number.Data type: String

 Maximum length: 40

</td></tr><tr><td>

contact.name

</td><td>

Contact full name.Data type: String

Maximum length: 151

</td></tr><tr><td>

contact.notification

</td><td>

Indicates whether the contact should receive notifications.Valid values:

-   1: Disabled
-   2: Enabled

Data type: Number \(Integer\)

Default: 2

</td></tr><tr><td>

contact.on\_schedule

</td><td>

Indicates the timeliness of dispatched service personnel.Valid values:

-   Ahead: Ahead of schedule.
-   behind\_less30: Behind schedule, but less than 30 minutes.
-   behind\_30to60: Behind schedule between 30 and 60 minutes.
-   behind\_more60: Behind schedule more than 60 minutes.
-   on\_time: On schedule.

Data type: String

Maximum length: 40

</td></tr><tr><td>

contact.phone

</td><td>

Contact business phone number.Data type: String

Maximum length: 40

</td></tr><tr><td>

contact.photo

</td><td>

Photo image of the contact. Data type: String

</td></tr><tr><td>

contact.preferred\_language

</td><td>

Country code of the contact primary language.Data type: String

Maximum length: 3

</td></tr><tr><td>

contact.roles

</td><td>

List of user roles associated with the contact.Data type: String

Maximum length: 40

</td></tr><tr><td>

contact.schedule

</td><td>

Sys\_id of the record that describes the work schedule for the associated contact.Data type: String

Table: Schedule \[cmn\_schedule\]

</td></tr><tr><td>

contact.source

</td><td>

Source of the contact.Data type: String

Maximum length: 255

</td></tr><tr><td>

contact.state

</td><td>

State in which the contact resides.Data type: String

Maximum length: 40

</td></tr><tr><td>

contact.street

</td><td>

Contact street address.Data type: String

Maximum length: 255

</td></tr><tr><td>

contact.sys\_class\_name

</td><td>

Table that contains the contact record. Data type: String

Maximum length: 80

</td></tr><tr><td>

contact.sys\_created\_by

</td><td>

User that originally created the associated contact record.Data type: String

Maximum length: 40

</td></tr><tr><td>

contact.sys\_created\_on

</td><td>

Data and time the associated contact was originally created.Data type: String \(Date/time\)

</td></tr><tr><td>

contact.sys\_domain

</td><td>

ServiceNow instance domain of the associated contact record.Data type: String

</td></tr><tr><td>

contact.sys\_domain\_path

</td><td>

Contact record domain path.Data type: String

Maximum length: 255

Default: / \(global\)

</td></tr><tr><td>

contact.sys\_id

</td><td>

Unique identifier for the associated contact record.Data type: String

</td></tr><tr><td>

contact.sys\_mod\_count

</td><td>

Number of times that the associated contact record has been modified.Data type: Number \(Integer\)

</td></tr><tr><td>

contact.sys\_tags

</td><td>

System tags for the content.Data type: String

</td></tr><tr><td>

contact.sys\_updated\_by

</td><td>

User that last updated the associated contact information.Data type: String

Maximum length: 40

</td></tr><tr><td>

contact.sys\_updated\_on

</td><td>

Data and time the associated contact information was updated.Data type: String \(Date/time\)

</td></tr><tr><td>

contact.time\_format

</td><td>

Format in which to display time.Valid values:

-   hh.mm.ss a: hh.mm.ss \(12 hour\)
-   hh:mm:ss a: hh:mm:ss \(12 hour\)
-   HH.mm.ss: hh.mm.ss \(24 hour\)
-   HH:mm:ss: hh:mm:ss \(24 hour\)

Data type: String

Maximum length: 40

Default: Blank \(system time format\)

</td></tr><tr><td>

contact.time\_sheet\_policy

</td><td>

Sys\_id of the record that contains the time sheet policy for the associated contact.Data type: String

Table: Time Sheet Policy \[time\_sheet\_policy\]

</td></tr><tr><td>

contact.time\_zone

</td><td>

Time zone in which the contact resides, such as Canada/Central or US/Eastern.Data type: String

Maximum length: 40

</td></tr><tr><td>

contact.title

</td><td>

Contact business title such as Manager, Software Developer, or Contractor.Data type: String

Maximum length: 60

</td></tr><tr><td>

contact.user\_name

</td><td>

Contact user ID.Data type: String

Maximum length: 40

</td></tr><tr><td>

contact.vip

</td><td>

Flag that indicates whether the associated contact has VIP status.Possible values:

-   true: VIP
-   false: Not VIP

Data type: Boolean

Default: false

</td></tr><tr><td>

contact.web\_service\_access\_only

</td><td>

Flag that indicates whether the contact can only access services through the web.Possible values:

-   true: Web access only
-   false: Access through all available methods

Data type: Boolean

Default: false

</td></tr><tr><td>

contact.zip

</td><td>

Contact zip code.Data type: String

Maximum length: 40

</td></tr><tr><td>

contact\_local\_time

</td><td id="casetable-contact_local_time-entry">

Contact local time.Data type: String

Maximum length: 70

</td></tr><tr><td>

contact\_time\_zone

</td><td id="d4583e601">

Time zone of the contact associated with the case.Data type: String

Maximum length: 40

</td></tr><tr><td>

contact\_type

</td><td id="d4583e614">

Method in which the case was initially reported.Possible values:

-   chat
-   email
-   phone
-   social
-   web

Data type: String

Maximum length: 40

</td></tr><tr><td>

contract

</td><td id="d4583e646">

Sys\_id of the contract associated with the case. This contract contains information about the type of support that is provided to the company associated to the case. A contract can include a company and contact and the specific assets that are covered. A contract can also include multiple service entitlements and SLAs.Data type: String

Table: Contract \[ast\_contract\]

</td></tr><tr><td>

correlation\_display

</td><td id="d4583e685">

Correlation display.Data type: String

Maximum length: 100

</td></tr><tr><td>

correlation\_id

</td><td id="d4583e699">

Correlation identifier.Data type: String

Maximum length: 100

</td></tr><tr><td>

delivery\_plan

</td><td id="d4583e712">

Sys\_id of the parent execution plan for this case.Data type: String

Table: Execution Plan \[sc\_cat\_item\_delivery\_plan\]

</td></tr><tr><td>

delivery\_task

</td><td id="d4583e725">

Sys\_id of the execution plan task.Data type: String

Table: Execution Plan Task \[sc\_cat\_item\_delivery\_task\]

</td></tr><tr><td>

description

</td><td id="d4583e738">

Detailed description of the problem associated with the case. Data type: String

Maximum length: 4,000

</td></tr><tr><td>

due\_date

</td><td id="d4583e753">

Date that the case is due to be closed.Data type: String

</td></tr><tr><td>

entitlement

</td><td id="d4583e764">

Sys\_id of the entitlement record associated with the case. Entitlements define the type of support that a customer receives as well as the supported communication channels. An entitlement can be associated with a product, an asset, an account, or a contract.Data type: String

Table: Entitlement \[service\_entitlement\]

</td></tr><tr><td>

escalation

</td><td id="d4583e778">

Current escalation level.Possible values:

-   0: Normal
-   1: Moderate
-   2: High
-   3: Overdue

Data type: Number \(Integer\)

Default: 0

</td></tr><tr><td>

expected\_start

</td><td id="d4583e807">

Date and time when work is scheduled to begin on the case.Data type: String

</td></tr><tr><td>

first\_response\_time

</td><td id="d4583e818">

Date and time when the first action was taken on the case.Data type: String

</td></tr><tr><td>

follow\_the\_sun

</td><td id="d4583e829">

Flag that indicates whether the case should be handed-off for global follow-up.If a customer enters additional comments on a Priority 1 - Critical or a Priority 2 - High case, or if the case is escalated, the flag is automatically set to true.

Possible values:

-   true: Case should be handed-off for global follow-up
-   false: Case shouldn't be handed-off for global follow-up

Data type: Boolean

Default: false

</td></tr><tr><td>

follow\_up

</td><td id="casetable-follow_up-entry">

Date and time of the next follow-up action.Data type: String

</td></tr><tr><td>

group\_list

</td><td id="d4583e865">

List of sys\_ids of the group records associated with the case.Data type: Array

Table: Group \[sys\_user\_group\]

</td></tr><tr><td>

impact

</td><td id="d4583e879">

Impact on customer.Possible values:

-   1: High
-   2: Medium
-   3: Low

Data type: Number \(Integer\)

Default: 3

</td></tr><tr><td>

knowledge

</td><td id="d4583e941">

Flag that indicates if there is a knowledge base article available for the specified issue.Possible values:

-   true: Knowledge base article is available for this issue
-   false: Knowledge base article is not available for this issue

Data type: Boolean

Default: false

</td></tr><tr><td>

location

</td><td id="d4583e964">

Sys\_id of the record describing the company location.Data type: String

Table: Location \[cmn\_location\]

</td></tr><tr><td>

made\_sla

</td><td id="d4583e977">

Flag that indicates whether the case was resolved in alignment with the associated service level agreement.Possible values:

-   true: Case was resolved in alignment with SLA
-   false: Case wasn't resolved according to the SLA

Data type: Boolean

Default: true

</td></tr><tr><td>

major\_case\_state

</td><td id="d4583e1001">

Current state of the major case.Possible values:

-   accepted: Initial state when a manager creates a major case or when a manager promotes a candidate case.
-   canceled: Case is canceled.
-   proposed: Initial state when an agent or manager creates or proposes a candidate case.
-   rejected: Manager rejected candidate case.

Data type: String

Maximum length: 40

</td></tr><tr><td>

needs\_attention

</td><td id="casetable-needs_attention-entry">

Flag that indicates whether the case needs attention.Possible values:

-   true: Case needs additional attention
-   false: Case doesn't need additional attention

Data type: Boolean

Default: false

</td></tr><tr><td>

notes\_to\_comments

</td><td id="d4583e1053">

Flag that indicates whether to add the resolution notes to the comments.Possible values:

-   true: Resolutions notes, when added, are also added to the comments
-   false: Resolution notes in comments aren't required

Data type: Boolean

</td></tr><tr><td>

notify

</td><td id="d4583e1074">

Method to use to notify contact/consumer.Possible values:

-   1: Do not notify
-   2: Send email
-   3: Telephone

Data type: Number \(Integer\)

Default: 1

</td></tr><tr><td>

number

</td><td id="d4583e1100">

Case number.Data type: String

Maximum length: 40

</td></tr><tr><td>

opened\_at

</td><td id="d4583e1113">

Date and time that the case was opened.Data type: String

</td></tr><tr><td>

opened\_by

</td><td id="d4583e1125">

Sys\_id of the person that initially opened the case.Data type: String

Table: User \[sys\_user\]

</td></tr><tr><td>

order

</td><td id="d4583e1138">

Order of the case.Data type: Number \(Integer\)

</td></tr><tr><td>

parent

</td><td id="d4583e1149">

Sys\_id of the parent case to which this case \(child\) is associated.Data type: String

Table: Task \[task\]

</td></tr><tr><td>

partner

</td><td id="d4583e1162">

Sys\_id of the partner associated with the case.Data type: String

Table: Account \[customer\_account\]

</td></tr><tr><td>

partner\_contact

</td><td id="d4583e1175">

Sys\_id of the partner contact associated with the case.Data type: String

Table: Contact \[customer\_contact\]

</td></tr><tr><td>

priority

</td><td id="d4583e1188">

Priority of the case. Possible values:

-   1: Critical
-   2: High
-   3: Moderate
-   4: Low

Data type: Number \(Integer\)

Default: 4

</td></tr><tr><td>

probable\_cause

</td><td id="d4583e1243">

Possible cause of the issue associated with the case.Data type: String

Maximum length: 4,000

</td></tr><tr><td>

problem

</td><td id="d4583e1256">

Sys\_id of the issue that the customer is encountering.Data type: String

Table: Problem \[problem\]

</td></tr><tr><td>

product

</td><td id="d4583e1269">

Sys\_id of the product model of the asset associated to the case. A model is a specific version or configuration of an asset \(for example, Apple Mac Book Pro\).Data type: String

Table: Product Model \[cmdb\_model\]

</td></tr><tr><td>

reassignment\_count

</td><td id="d4583e1282">

Number of times that the case was reassigned to a person that is responsible for moving the case forward.Data type: Number \(Integer\)

Default: 0

</td></tr><tr><td>

recipient\_list

</td><td id="d4583e1295">

Sys\_id of the record that contains the list of recipients for communications about this case.Data type: String

Table: Recipients List \[sn\_publications\_recipients\_list\]

</td></tr><tr><td>

rejection\_goto

</td><td id="d4583e1309">

Sys\_id of the task to execute if the case is rejected.Data type: String

Table: Task \[task\]

</td></tr><tr><td>

resolution\_code

</td><td id="d4583e1322">

Resolution state for the case, such as "Solved - Fixed by Support/Guidance provided". Data type: String

Maximum length: 40

</td></tr><tr><td>

resolved\_at

</td><td id="d4583e1335">

Date and time that the case was resolved.Data type: String

</td></tr><tr><td>

resolved\_by

</td><td id="d4583e1346">

Sys\_id of the person that resolved the case.Data type: String

Table: User \[sys\_user\]

</td></tr><tr id="case-result-response-row"><td>

result

</td><td>

List of values for the requested field.Data type: Array of Objects

```
"result": [
  {
    "label": "String",
    "value": "String"
  }
]
```

</td></tr><tr id="case-result-label-response-row"><td>

result.label

</td><td>

Display value for the field value.Data type: String

</td></tr><tr id="case-result-value-response-row"><td>

result.value

</td><td>

Field value.Data type: String

</td></tr><tr><td>

short\_description

</td><td id="d4583e1378">

Concise description of the case. Data type: String

Maximum length: 160

</td></tr><tr><td>

skills

</td><td id="d4583e1393">

List of the unique identifiers \(sys\_id\) of the skills needed to complete the case.Data type: String

Table: Skill \[cmn\_skill\]

</td></tr><tr><td>

sla\_due

</td><td id="d4583e1406">

Date/time at which the case must be closed based on the associated service level agreement.Data type: String

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile

</td><td>

Details for a specific social media profile, such as Facebook, Twitter, or YouTube.Data type: Array of Objects

```
"sn_app_cs_social_social_profile": [
  {
    "account": "String",
    "channel": [Array],
    "contact": {Object},
    "consumer": {Object},
    "created_on": "String",
    "profile": "String",
    "profile_url": "String",
    "social_id": "String",
    "source": "String",
    "sys_created_by": "String",
    "sys_created_on": "String",
    "sys_id": "String",
    "sys_mod_count": Number,
    "sys_tags": "String",
    "sys_updated_by": "String",
    "sys_updated_on": "String"
  }
]
```

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.account

</td><td>

Unique identifier of the record containing account information for the social media profile. Located in the Account \[customer\_account\] table.Data type: String

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.channel

</td><td>

Details on the associated social media profile channel.Data type: Object

```
"channel": {
  "name": "String",
  "sys_class_name": "String",
  "sys_created_by": "String",
  "sys_created_on": "String",
  "sys_mod_count": Number,
  "sys_package": "String",
  "sys_policy": "String",
  "sys_scope": "String",
  "sys_tags": "String",
  "sys_update_name": "String",
  "sys_updated_by": "String",
  "sys_updated_on": "String"
}
```

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.channel.name

</td><td>

Name of the social media channel.Data type: String

Maximum length: 100

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.channel.sys\_class\_name

</td><td>

Table that contains the social media channel record.Data type: String

Maximum length: 80

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.channel.sys\_created\_by

</td><td>

Person that created the social media channel.Data type: String

Maximum length: 40

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.channel.sys\_created\_on

</td><td>

Date and time the social media profile was created.Data type: Date/time

Maximum length: 40

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.channel.sys\_id

</td><td>

Unique identifier of the associated social media profile channel.Data type: String

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.channel.sys\_mod\_count

</td><td>

Number of times that information was modified for the associated social media profile channel.Data type: Integer

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.channel.sys\_name

</td><td>

System name of channel.Data type: String

Maximum length: 255

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.channel.sys\_package

</td><td>

Unique identifier of the record that contains information about the package associated with the profile; Package \[sys\_package\] table.Data type: Reference

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.channel.sys\_policy

</td><td>

System protection policy.Possible values:

-   protected
-   read

Data type: String

Maximum length: 40

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.channel.sys\_scope

</td><td>

Unique identifier of the record that contains information about the scope of the social profile; Application \[sys\_scope\] table.Data type: Reference

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.channel.sys\_tags

</td><td>

System tags associated with the channel.Data type: String

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.channel.sys\_update\_name

</td><td>

Name of the person that last updated the social media profile channel.Data type: String

Maximum length: 250

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.channel.sys\_updated\_by

</td><td>

User that last updated the social media profile channel.Data type: String

Maximum length: 40

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.channel.sys\_updated\_on

</td><td>

Date and time the social media profile channel was last updated.Data type: Date/time

Maximum length: 40

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.consumer

</td><td>

For business-to-consumer cases. Details about the consumer associated with the case.Data type: Object

```
"consumer": {
  "active": Boolean,
  "business_phone": "String",
  "city": "String",
  "country": "String",
  "date_format": "String",
  "email": "String",
  "fax": "String",
  "first_name": "String",
  "gender": "String",
  "home_phone": "String",
  "household": "String",
  "last_name": "String",
  "middle_name": "String",
  "mobile_phone": "String",
  "name": "String",
  "notes": "String",
  "notification": Number,
  "number": "String",
  "photo": Image,
  "preferred_language": "String",
  "prefix": "String",
  "primary": Boolean,
  "state": "String",
  "street": "String",
  "suffix": "String",
  "sys_created_by": "String",
  "sys_created_on": "String",
  "sys_domain": "String",
  "sys_id": "String",
  "sys_mod_count": Number,
  "sys_tags": "String",
  "sys_updated_by": "String",
  "sys_updated_on": "String",
  "time_format": "String",
  "time_zone": "String",
  "title": "String",
  "user": "String",
  "zip": "String"
}
```

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.consumer.active

</td><td>

Flag that indicates whether the consumer is active.Possible values:

-   true: Consumer active
-   false: Consumer de-activated

Data type: Boolean

Default: true

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.consumer.business\_phone

</td><td>

Business phone number of the consumer.Data type: String

Maximum length: 40

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.consumer.city

</td><td>

City in which the consumer resides.Data type: String

Maximum length: 100

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.consumer.country

</td><td>

Country in which the consumer resides.Data type: String

Maximum length: 40

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.consumer.date\_format

</td><td>

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

sn\_app\_cs\_social\_social\_profile.consumer.email

</td><td>

Email address of the consumer.Data type: String

Maximum length: 100

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.consumer.fax

</td><td>

Fax number of the consumer.Data type: String

Maximum length: 40

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.consumer.first\_name

</td><td>

Consumer first name.Data type: String

Maximum length: 50

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.consumer.gender

</td><td>

Gender of the consumer.Data type: String

Maximum length: 40

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.consumer.home\_phone

</td><td>

Home phone number of the consumer.Data type: String

Maximum length: 40

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.consumer.household

</td><td>

Sys\_id of the record that describes the household characteristics.Data type: String

Table: Household \[csm\_household\]

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.consumer.last\_name

</td><td>

Consumer last name.Data type: String

Maximum length: 50

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.consumer.middle\_name

</td><td>

Consumer middle name.Data type: String

Maximum length: 50

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.consumer.mobile\_phone

</td><td>

Consumer mobile phone number.Data type: String

Maximum length: 40

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.consumer.name

</td><td>

Consumer full name; first\_name+middle\_name+last\_name.Data type: String

Maximum length: 152

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.consumer.notes

</td><td>

Notes on consumer.Data type: String

Maximum length: 4,000

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.consumer.notification

</td><td>

Indicates whether the consumer should receive notifications.Valid values:

-   1: Disabled
-   2: Enabled

Data type: Number \(Integer\)

Maximum length: 40

Default: 2

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.consumer.number

</td><td>

Unique number associated with the consumer.Data type: String

Maximum length: 40

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.consumer.photo

</td><td>

Photo of the consumer.Data type: Image

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.consumer.preferred\_language

</td><td>

Consumer primary language.Data type: String

Maximum length: 3

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.consumer.prefix

</td><td>

Consumer name prefix such as, Dr., Mr., Mrs., or Ms.Data type: String

Maximum length: 40

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.consumer.primary

</td><td>

Flag that indicates whether this is the primary consumer.Possible values:

-   true: Primary consumer
-   false: Not primary consumer

Data type: Boolean

Default: false

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.consumer.state

</td><td>

State in which the consumer resides.Data type: String

Maximum length: 100

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.consumer.street

</td><td>

Consumer street address.Data type: String

Maximum length: 255

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.consumer.suffix

</td><td>

Consumer name suffix such as Jr., Sr., or II.Data type: String

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.consumer.sys\_created\_by

</td><td>

User that created the consumer record.Data type: String

Maximum length: 40

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.consumer.sys\_created\_on

</td><td>

Date and time the consumer record was originally created.Data type: String

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.consumer.sys\_domain

</td><td>

ServiceNow domain in which the consumer information resides.Data type: String

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.consumer.sys\_id

</td><td>

Unique identifier for the consumer.Data type: String

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.consumer.sys\_mod\_count

</td><td>

Number of times that the associated consumer information has been modified.Data type: Number \(Integer\)

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.consumer.sys\_tags

</td><td>

Consumer system tags.

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.consumer.sys\_updated\_by

</td><td>

User that last updated the consumer information.Data type: String

Maximum length: 40

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.consumer.sys\_updated\_on

</td><td>

Date and time when the consumer information was last updated.Data type: String

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.consumer.time\_format

</td><td>

Format in which to display time.Valid values:

-   hh.mm.ss a: hh.mm.ss \(12 hour\)
-   hh:mm:ss a: hh:mm:ss \(12 hour\)
-   HH.mm.ss: hh.mm.ss \(24 hour\)
-   HH:mm:ss: hh:mm:ss \(24 hour\)

Data type: String

Maximum length: 40

Default: blank \(system time format\)

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.consumer.time\_zone

</td><td>

Consumer time zone, such as Canada/Central or US/Eastern.Data type: String

Maximum length: 40

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.consumer.title

</td><td>

Consumer business title such as Manager, Software Developer, or Contractor.Data type: String

Maximum length: 60

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.consumer.user

</td><td>

Sys\_id of the consumer user. Data type: String

Table: Consumer User \[csm\_consumer\_user\]

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.consumer.zip

</td><td>

Consumer zip code. Data type: String

Maximum length: 40

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact

</td><td>

For business-to-business cases. Unique identifier of the record containing details about the social media profile that belongs to the contact associated with the case. Located in the Contact \[customer\_contact\] table.Data type: String

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.account

</td><td>

Sys\_id of the account record to which the contact is associated.Data type: String

Table: Account \[customer\_account\]

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.active

</td><td>

Flag that indicates whether the contact is active within the system.Possible values:

-   true: Contact is active
-   false: Contact is inactive

Data type: Boolean

Default: true

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.agent\_status

</td><td>

Status of the agent.Possible values:

-   Off work
-   On break
-   On route
-   On site

Data type: String

Maximum length: 40

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.building

</td><td>

Sys\_id of the record that describes the building in which the contact resides.Data type: String

Table: Building \[cmn\_building\]

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.calendar\_integration

</td><td>

Calendar application that the contact uses.1: Outlook

Data type: Number \(Integer\)

Default: 1

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.city

</td><td>

City in which the contact resides.Data type: String

Maximum length: 40

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.company

</td><td>

Sys\_id of the company record to which the contact is associated.Data type: String

Table: Company \[core\_company\]

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.cost\_center

</td><td>

Sys\_id of the cost center associated with the contact.Data type: String

Table: Cost Center \[cmn\_cost\_center\]

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.country

</td><td>

Country code of the country in which the contact resides.Data type: String

Maximum length: 3

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.date\_format

</td><td>

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

sn\_app\_cs\_social\_social\_profile.contact.default\_perspective

</td><td>

Sys\_id of the default perspective for the contact.Data type: String

Table: Menu List \[sys\_perspective\]

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.department

</td><td>

Sys\_id of the department associated with the contact.Data type: String

Table: Department \[cmn\_department\]

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.edu\_status

</td><td>

Education status of the associated contact.Data type: String

Maximum length: 40

Default: faculty

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.email

</td><td>

Contact email address.Data type: String

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.employee\_number

</td><td>

Contact employee number.Data type: String

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.enable\_multifactor\_authn

</td><td>

Flag that indicates whether multifactor authorization is required for the contact to log in to the service portal.Possible values:

-   true: Multifactor authorization enabled
-   false: Multifactor authorization disabled

Data type: Boolean

Default: false

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.failed\_attempts

</td><td>

Number of failed log in attempts.Data type: Number \(Integer\)

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.first\_name

</td><td>

Contact first name.Data type: String

Maximum length: 50

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.gender

</td><td>

Contact gender.Data type: String

Maximum length: 40

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.geolocation\_tracked

</td><td>

Flag that indicates whether the contact location is obtained through geotracking.Possible values:

-   true: Contact location obtained through geotracking
-   false: Contact location not obtained through geotracking

Data type: Boolean

Default value: false

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.home\_phone

</td><td>

Contact home phone number.Data type: String

Maximum length: 40

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.internal\_itegration\_user

</td><td>

Flag that indicates whether the contact is an internal integration user.Possible values:

-   true: Internal integration user
-   false: Other type of user

Data type: Boolean

Default: false

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.introduction

</td><td>

IntroductionData type: String

Maximum length: 40

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.last\_login

</td><td>

Date on which the contact last logged into the system.Data type: String \(Date\)

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.last\_login\_device

</td><td>

Device the consumer used the last time they logged in to the system.Data type: String

Maximum length: 40

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.last\_login\_time

</td><td>

Date and time the contact logged in to the system.Data type: String \(Date/time\)

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.last\_name

</td><td>

Contact last name.Data type: String

Maximum length: 50

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.last\_position\_update

</td><td>

Date and time the last position was updated.Data type: String \(Date/time\)

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.latitude

</td><td>

Latitude coordinate of the contact.Data type: Number \(Floating point\)

Maximum length: 40

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.ldap\_server

</td><td>

Sys\_id of the LDAP server used by the contact to last log in to the system. Data type: String

Table: LDAP Server \[ldap\_server\_config\]

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.location

</td><td>

Sys\_id of the record that describes the location of the contactData type: String

Table: Location \[cmn\_location\]

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.locked\_out

</td><td>

Flag that indicates if the contact is locked-out.Possible values:

-   true: Contact locked-out
-   false: Contact not locked-out

Data type: Boolean

Default: false

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.longitude

</td><td>

Longitude coordinate of the contact.Data type: Number \(Floating point\)

Maximum length: 40

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.manager

</td><td>

Sys\_id of the record that describes the direct supervisor of the contact.Data type: String

Table: User \[sys\_user\]

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.middle\_name

</td><td>

Contact middle name.Data type: Number \(Floating point\)

Maximum length: 50

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.mobile\_phone

</td><td>

Contact mobile phone number.Data type: String

 Maximum length: 40

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.name

</td><td>

Contact full name.Data type: String

Maximum length: 151

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.notification

</td><td>

Indicates whether the contact should receive notifications.Valid values:

-   1: Disabled
-   2: Enabled

Data type: Number \(Integer\)

Default: 2

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.on\_schedule

</td><td>

Indicates the timeliness of dispatched service personnel.Valid values:

-   Ahead: Ahead of schedule.
-   behind\_less30: Behind schedule, but less than 30 minutes.
-   behind\_30to60: Behind schedule between 30 and 60 minutes.
-   behind\_more60: Behind schedule more than 60 minutes.
-   on\_time: On schedule.

Data type: String

Maximum length: 40

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.phone

</td><td>

Contact business phone number.Data type: String

Maximum length: 40

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.photo

</td><td>

Photo image of the contact. Data type: String

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.preferred\_language

</td><td>

Country code of the contact primary language.Data type: String

Maximum length: 3

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.roles

</td><td>

List of user roles associated with the contact.Data type: String

Maximum length: 40

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.schedule

</td><td>

Sys\_id of the record that describes the work schedule for the associated contact.Data type: String

Table: Schedule \[cmn\_schedule\]

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.source

</td><td>

Source of the contact.Data type: String

Maximum length: 255

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.state

</td><td>

State in which the contact resides.Data type: String

Maximum length: 40

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.street

</td><td>

Contact street address.Data type: String

Maximum length: 255

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.sys\_class\_name

</td><td>

Table that contains the contact record. Data type: String

Maximum length: 80

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.sys\_created\_by

</td><td>

User that originally created the associated contact record.Data type: String

Maximum length: 40

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.sys\_created\_on

</td><td>

Data and time the associated contact was originally created.Data type: String \(Date/time\)

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.sys\_domain

</td><td>

ServiceNow instance domain of the associated contact record.Data type: String

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.sys\_domain\_path

</td><td>

Contact record domain path.Data type: String

Maximum length: 255

Default: / \(global\)

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.sys\_id

</td><td>

Unique identifier for the associated contact record.Data type: String

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.sys\_mod\_count

</td><td>

Number of times that the associated contact record has been modified.Data type: Number \(Integer\)

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.sys\_tags

</td><td>

Contact system tags.

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.sys\_updated\_by

</td><td>

User that last updated the associated contact information.Data type: String

Maximum length: 40

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.sys\_updated\_on

</td><td>

Data and time the associated contact information was updated.Data type: String \(Date/time\)

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.time\_format

</td><td>

Format in which to display time.Valid values:

-   hh.mm.ss a: hh.mm.ss \(12 hour\)
-   hh:mm:ss a: hh:mm:ss \(12 hour\)
-   HH.mm.ss: hh.mm.ss \(24 hour\)
-   HH:mm:ss: hh:mm:ss \(24 hour\)

Data type: String

Maximum length: 40

Default: Blank \(system time format\)

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.time\_sheet\_policy

</td><td>

Sys\_id of the record that contains the time sheet policy for the associated contact.Data type: String

Table: Time Sheet Policy \[time\_sheet\_policy\]

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.time\_zone

</td><td>

Time zone in which the contact resides, such as Canada/Central or US/Eastern.Data type: String

Maximum length: 40

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.title

</td><td>

Contact business title such as Manager, Software Developer, or Contractor.Data type: String

Maximum length: 60

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.user\_name

</td><td>

Contact user ID.Data type: String

Maximum length: 40

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.vip

</td><td>

Flag that indicates whether the associated contact has VIP status.Possible values:

-   true: VIP
-   false: Not VIP

Data type: Boolean

Default: false

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.web\_service\_access\_only

</td><td>

Flag that indicates whether the contact can only access services through the web.Possible values:

-   true: Web access only
-   false: Access through all available methods

Data type: Boolean

Default: false

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.contact.zip

</td><td>

Contact zip code.Data type: String

Maximum length: 40

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.created\_on

</td><td>

Date and time the associated social media profile was initially created.

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.profile

</td><td>

Social profile.Data type: String

 Maximum length: 255

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.profile\_url

</td><td>

URL to use to access the social media profile.Data type: String

 Maximum length: 1,024

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.social\_id

</td><td>

Unique social media account provider identifier for the associated social media account.Data type: String

 Maximum length: 100

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.source

</td><td>

Source of the social profile.Data type: String

 Maximum length: 255

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.sys\_created\_by

</td><td>

User that initially created the social media profile.Data type: String

 Maximum length: 40

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.sys\_created\_on

</td><td>

Date and time the social media profile was initially created.Data type: String \(Date/time\)

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.sys\_id

</td><td>

Unique identifier for the social media profile.Data type: String

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.sys\_mod\_count

</td><td>

Number of times that information was modified for the associated social media profile.Data type: Number \(Integer\)

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.sys\_tags

</td><td>

Profile system tags.

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.sys\_updated\_by

</td><td>

User that initially created the social media profile.Data type: String

 Maximum length: 40

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile.sys\_updated\_on

</td><td>

User that initially created the social media profile.Data type: String

 Maximum length: 40

</td></tr><tr><td>

state

</td><td id="d4583e1457">

Current state of the case.Possible values:

-   1: New
-   3: Closed
-   6: Resolved
-   10: Open
-   18: Awaiting Info

Data type: Number \(Integer\)

Default: 1

</td></tr><tr><td>

subcategory

</td><td id="d4583e1489">

Case subcategory.Possible values:

0: QuestionData type: Number \(Integer\)

Default: 0

</td></tr><tr><td>

support\_manager

</td><td id="d4583e1505">

Sys\_id of the CSM manager assigned to the case.Data type: String

Table: User \[sys\_user\]

</td></tr><tr><td>

sync\_driver

</td><td id="d4583e1518">

Flag that indicates whether there's driver synchronization.Possible values:

-   true: Driver is synchronized
-   false: Driver isn't synchronized

Data type: Boolean

</td></tr><tr><td>

sys\_class\_name

</td><td id="casetable-sys_class_name-entry">

Table that contains the case record.Data type: String

Maximum length: 80

</td></tr><tr><td>

sys\_created\_by

</td><td id="casetable-sys_created_by-entry">

Person that initially opened the case.Data type: String

Maximum length: 40

</td></tr><tr><td>

sys\_created\_on

</td><td id="casetable-sys_created_on-entry">

Date and time when the case was initially created.Data type: String

</td></tr><tr><td>

sys\_domain

</td><td id="casetable-sys_domain-entry">

Domain associated with the case.Data type: String

Maximum length: 32

Default: global

</td></tr><tr><td>

sys\_domain\_path

</td><td id="d4583e1592">

Domain path.Data type: String

Maximum length: 255

Default: /

</td></tr><tr><td>

sys\_id

</td><td id="casetable-sys_sys_id-entry">

Unique identifier for the case.Data type: String

Maximum length: 32

</td></tr><tr><td>

sys\_mod\_count

</td><td id="casetable-sys_mod_count-entry">

Number of updates to the case since it was initially created.Data type: Number \(Integer\)

</td></tr><tr><td>

sys\_tags

</td><td>

System tags.

</td></tr><tr><td>

sys\_updated\_by

</td><td id="casetable-sys_updated_by-entry">

Person that last updated the case.Data type: String

Maximum length: 40

</td></tr><tr><td>

sys\_updated\_on

</td><td id="casetable-sys_updated_on-entry">

Date and time when the case was last updated.Data type: String

</td></tr><tr><td>

time\_worked

</td><td id="d4583e1661">

Total amount of time worked on the case.Data type: String

</td></tr><tr><td>

upon\_approval

</td><td id="d4583e1677">

Action to take if the case is approved.Possible values:

-   do\_nothing
-   proceed

Data type: String

Maximum length: 40

Default: proceed

</td></tr><tr><td>

upon\_reject

</td><td id="d4583e1702">

Action to take if the case is rejected.Possible values:

-   cancel
-   goto

Data type: String

Maximum length: 40

Default: cancel

</td></tr><tr><td>

urgency

</td><td id="d4583e1728">

Urgency of the case.Possible values:

-   1: High
-   2: Medium
-   3: Low

Data type: Number \(Integer\)

Default: 3

</td></tr><tr><td>

user\_input

</td><td id="d4583e1754">

Additional user input.Data type: String

Maximum length: 4,000

</td></tr><tr><td>

variable\_pool

</td><td>

Grouping of variables.

</td></tr><tr><td>

variables

</td><td id="d4583e1767">

Name-value pairs of variables associated with the case.Data type: String

Maximum length: 40

</td></tr><tr><td>

watch\_list

</td><td id="d4583e1780">

List of sys\_ids of the users who receive notifications about this case when additional comments are added or if the state of a case is changed to Resolved or Closed.Data type: Array

Table: User \[sys\_user\]

</td></tr><tr><td>

wf\_activity

</td><td id="d4583e1793">

Sys\_id of the workflow activity record associated with the case.Data type: String

Table: Workflow Activity \[wf\_activity\]

</td></tr><tr><td>

work\_end

</td><td id="d4583e1806">

Date and time work ended on the case.Data type: String

</td></tr><tr><td>

work\_notes

</td><td id="casetable-work_notes-entry">

Information about how to resolve the case, or steps taken to resolve it.Data type: String

Maximum length: 4,000

</td></tr><tr><td>

work\_notes\_list

</td><td id="d4583e1831">

List of sys\_ids of the internal users who receive notifications about this case when work notes are added.Data type: Array

Table: User \[sys\_user\]

</td></tr><tr><td>

work\_start

</td><td id="d4583e1844">

Date and time that work started on the case.Data type: String

</td></tr></tbody>
</table>### Notes on request body parameters

All request body parameters are optional. Not all parameters apply to all case types \(B2B vs B2C and order vs product.\) Ensure that the parameters that you set do not conflict, such as a mismatch between the account and contact or consumer. In addition to the list of elements defined below \(which define the elements found in a base system\), the endpoint also accepts custom case fields and any additional case fields configured in your instance. For additional information on these elements, refer to your specific table definitions \[**System Definition** &gt; **Tables**\].

### cURL request

The following example illustrates how to update a consumer-based case.

```
curl "https://instance.servicenow.com/api/sn_cusomerservice/case/0397c743db436f0057c3fd441d96197f" \
--request PUT \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{ \
  consumer: \"cd97ef1ddb8bc7006b7a9646db9619ac\", \
  contact_type: \"phone\", \
  priority: \"4\", \
  short_description: \"Consumer Test Case\"}" \
--user "username":"password"

```

```
{
  "result": {
    "sys_id": "0397c743db436f0057c3fd441d96197f",
    "number": "CS0001005"
  }
}
```

