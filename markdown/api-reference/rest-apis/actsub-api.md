---
title: ActivitySubscriptions API
description: The ActivitySubscriptions API provides endpoints to retrieve Activity entities from the Subscriptions and Activity Feed Framework.Retrieves activity records from the Subscriptions and Activity Feed Framework.Retrieves facets configured for an activity context from the Subscriptions and Activity Feed Framework. Displays activity counts and data for each facet as determined by activity type, group, and context settings.
locale: en-US
release: australia
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 18
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# ActivitySubscriptions API

The ActivitySubscriptions API provides endpoints to retrieve Activity entities from the Subscriptions and Activity Feed Framework.

This API requires activation of the Subscriptions and Activity Feed Framework \(com.snc.activity\_subscriptions\) plugin. Activate the Customer Central \(com.sn\_csm\_customer\_central\) plugin to seed configuration in all required tables. For more information on customer central configuration settings, see Configure customer central.

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## ActivitySubscriptions - GET /now/actsub/activities

Retrieves activity records from the Subscriptions and Activity Feed Framework.

No role is required to access this endpoint, but data returned is limited by user access settings.

### URL format

Versioned URL: `/api/now/{api_version}/actsub/activities`

Default URL: `/api/now/actsub/activities`

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

before

</td><td>

Date/time value. The request returns only records created prior to this date and time.Data type: String

Format: YYYY-MM-DD hh:mm:ss or YYYY-MM-DD

</td></tr><tr><td>

context

</td><td>

Required. Sys\_id of an activity context.Predefined activity contexts include Consumer and Contact.

Data type: String

Table: Activity Context \[sn\_actsub\_activity\_context\]

</td></tr><tr><td>

context\_instance

</td><td>

Required. Sys\_id of an instance of the specified activity context, representing the initiator of the activities you want to retrieve. Located in the appropriate table for the activity context.As an example, if you set **context** to the sys\_id of the Consumer activity context, set this parameter to the sys\_id of the Consumer \[csm\_consumer\] table record for the consumer whose activities you want to retrieve.

Data type: String

</td></tr><tr><td>

end\_date

</td><td id="end-date-query-param-entry">

Date/time value. The request returns only records created during the time period defined by **start\_date** and this parameter. Must be set along with **start\_date**.Data type: String

 Format: YYYY-MM-DD hh:mm:ss or YYYY-MM-DD

</td></tr><tr><td>

facets

</td><td>

Comma-separated list of sys\_ids of activity facet types to retrieve for the specified activity context.For more details on activity facets, see Create facets for activity contexts.

Data type: String

Default: Return all activity facet types configured for the activity context.

Table: Activity Facet \[sn\_actsub\_facet\]

</td></tr><tr><td>

last

</td><td>

Index value of the first result row omitted from the response body. The result row index starts at 0, so the last row included in the response body is the one with the index **last**-1.For example, setting `last=5` omits rows with index 5 and above and returns at most only the first five result rows \(with index values 0 through 4\). Setting `stFrom=1` and `last=5` skips the first result row and returns the second through fifth result rows \(with index values 1 through 4\).

Data type: Number \(integer\)

Default: The value of the **com.snc.actsub.activities.api.fetch.limit** system property \(10 by default\).

</td></tr><tr><td>

record\_id

</td><td>

Sys\_id of a record to use when rendering dynamic facets. Located in the appropriate table for the activity type you want to retrieve.For example, if you want to fetch activities for a Case record, set this parameter to the sys\_id of the Case record in question.

For more details on dynamic facets, see Create facets for activity contexts.

Data type: String

</td></tr><tr><td>

start\_date

</td><td id="start-date-query-param-entry">

Date/time value. The request returns only records created during the time period defined by this parameter and **end\_date**. Must be set along with **end\_date**.Data type: String

 Format: YYYY-MM-DD hh:mm:ss or YYYY-MM-DD

</td></tr><tr><td>

stFrom

</td><td>

Index value of the first result row to include in the response body. The result row index starts at 0.For example, `stFrom=2` skips the first two result rows and returns results from the third row onward.

Data type: Number \(integer\)

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

400

</td><td id="entry-400-status-code">

Bad Request. A bad request type or malformed request was detected. The response body **result.message** parameter describes the nature of the error.Example error messages:

-   `Make sure a valid context and context_instance are passed` or `Make sure a valid stream and user are passed` indicates that the request lacks one or both of the **context** and **context\_instance** query parameters. These parameters are required.
-   `stFrom can not be greater than last` indicates that the **stFrom** query parameter value exceeds the **last** query parameter value.
-   `Please provide start_date and end_date` indicates that the request includes only one of the **start\_date** and **end\_date** query parameters, which cannot be used separately.
-   `start_date can not be ahead of end_date` indicates that the specified **start\_date** query parameter value occurs after the specified **end\_date** query parameter value.
-   `Provided context is not configured in the system` indicates that the **context** query parameter value does not represent a valid activity context.
-   `Make sure a valid context_instance is passed` indicates that the **context\_instance** query parameter value does not represent a valid instance of the specified activity context.

</td></tr><tr><td>

401

</td><td id="entry-401-status-code">

Unauthorized. The user credentials are incorrect or have not been passed.

</td></tr><tr><td>

500

</td><td id="entry-500-status-code">

Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.

</td></tr></tbody>
</table>### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

Result object.Data type: Object

```

"result": {
  "activities": [Array],
  "message": "String",
  "status": Number,
  "stream": "String",
  "user": "String"
}
```

</td></tr><tr><td>

result.activities

</td><td>

Array of objects in which each object represents an activity record from the specified activity context and context instance.Data type: Array of Objects

```
"activities": [
  {
    "activity_type_id": "String",
    "content_fields": [Array],
    "created": "String",
    "icon": "String",
    "source_table_name": "String",
    "subheader_fields": [Array],
    "subobject_sys_id": "String",
    "subobject_table_name": "String",
    "sys_id": "String",
    "title": "String"
  }
]
```

</td></tr><tr><td>

result.activities.activity\_type\_id

</td><td>

Sys\_id of the record from the Activity Types \[sn\_actsub\_activity\_type\] table that corresponds to the type of this activity record.Data type: String

</td></tr><tr><td>

result.activities.content\_fields

</td><td>

Array of objects in which each object represents a field to display as content in the tile for the activity record.Data type: Array of Objects

```
"content_fields": [
  {
    "deeplink_to_subobject": "String",
    "display_as_timeago": "String",
    "label": "String",
    "show_label": "String",
    "type": "String",
    "value": "String"
  }
]
```

</td></tr><tr><td>

result.activities.content\_fields.deeplink\_to\_subobject

</td><td>

Flag indicating whether or not the content field displays as a hyperlink to the record for the object on which this activity was performed.Valid values:

-   true: The content field displays as a hyperlink to the record for the object on which this activity was performed.
-   false: The content field displays as a hyperlink to the record for the object on which this activity was performed.

Data type: String

</td></tr><tr><td>

result.activities.content\_fields.display\_as\_timeago

</td><td>

Flag indicating whether or not the content field displays in time ago format.Valid values:

-   true: The content field displays in time ago format.
-   false: The content field does not display in time ago format.

Data type: String

</td></tr><tr><td>

result.activities.content\_fields.label

</td><td>

Label for the content field.Data type: String

</td></tr><tr><td>

result.activities.content\_fields.show\_label

</td><td>

Flag indicating whether or not the content field label displays for content field values in the tile for this activity record.Valid values:

-   true: The content field label displays for content field values in the tile for this activity record.
-   false: The content field label doesn't display for content field values in the tile for this activity record.

Data type: String

</td></tr><tr><td>

result.activities.content\_fields.type

</td><td>

Type of the content field.Data type: String

</td></tr><tr><td>

result.activities.content\_fields.value

</td><td>

Value of the content field.Data type: String

</td></tr><tr><td>

result.activities.created

</td><td>

Creation date/time for this activity record.Data type: String

Format: YYYY-DD-MM hh:mm:ss

</td></tr><tr><td>

result.activities.icon

</td><td>

Name of the icon displayed on the tile for this activity record.Data type: String

</td></tr><tr><td>

result.activities.source\_table\_name

</td><td>

Name of the table in which this activity record is located. Determined by the Activity Source defined in the Activity Types \[sn\_actsub\_activity\_type\] table for the type associated with this activity record.

Data type: String

</td></tr><tr><td>

result.activities.subheader\_fields

</td><td>

Array of objects in which each object represents a field displayed in the subheader of the tile for this activity record.Data type: Array of Objects

```
"subheader_fields": [
  {
    "deeplink_to_subobject": "String",
    "display_as_timeago": "String",
    "label": "String",
    "show_label": "String",
    "type": "String",
    "value": "String"
  }
]
```

</td></tr><tr><td>

result.activities.subheader\_fields.deeplink\_to\_subobject

</td><td>

Flag indicating whether or not the subheader field displays as a hyperlink to the record for the object on which this activity was performed.Valid values:

-   true: The subheader field displays as a hyperlink to the record for the object on which this activity was performed.
-   false: The subheader field doesn't display as a hyperlink to the record for the object on which this activity was performed.

Data type: String

</td></tr><tr><td>

result.activities.subheader\_fields.display\_as\_timeago

</td><td>

Flag indicating whether or not the subheader field displays in time ago format.Valid values:

-   true: The subheader field displays in time ago format.
-   false: The subheader field doesn't display in time ago format.

Data type: String

</td></tr><tr><td>

result.activities.subheader\_fields.label

</td><td>

Label for the subheader field.Data type: String

</td></tr><tr><td>

result.activities.subheader\_fields.show\_label

</td><td>

Flag indicating whether or not the subheader field label displays for subheader field values in the tile for this activity record.Valid values:

-   true: The subheader field label displays for subheader field values in the tile for this activity record.
-   false: The subheader field label doesn't display for subheader field values in the tile for this activity record.

Data type: String

</td></tr><tr><td>

result.activities.subheader\_fields.type

</td><td>

Type of the subheader field.Data type: String

</td></tr><tr><td>

result.activities.subheader\_fields.value

</td><td>

Value of the subheader field.Data type: String

</td></tr><tr><td>

result.activities.subobject\_sys\_id

</td><td>

Sys\_id of the record for the object on which this activity was performed. Located in the table specified in the **subobject\_table\_name** parameter value.Data type: String

</td></tr><tr><td>

result.activities.subobject\_table\_name

</td><td>

Name of the table containing the record for the object on which this activity was performed. Determined by the Table Name defined in the Activity Group \[sn\_actsub\_subscribable\_object\] table for the group containing the activity type associated with this activity record.

Data type: String

</td></tr><tr><td>

result.activities.sys\_id

</td><td>

Sys\_id of this activity record. Located in the table specified as the **source\_table\_name** response body parameter value.Data type: String

</td></tr><tr><td>

result.activities.title

</td><td>

Title that displays on the tile for this activity record.Data type: String

</td></tr><tr><td>

result.hasMoreRecords

</td><td>

Flag indicating whether or not the list of activities in the response body is truncated by the **last** query parameter value.Valid values:

-   true: The list of activities in the response body is truncated by the **last** query parameter value. Repeating the request with a higher **last** query parameter value will return additional activities for this context and context instance.
-   false: The list of activities in the response body isn't truncated by the **last** query parameter value. No further activities are available for this context and context instance.

Data type: String

</td></tr><tr><td>

result.message

</td><td>

Error message describing the problem encountered during request processing.Data type: String

</td></tr><tr><td>

result.status

</td><td>

HTTP status code returned for request.Valid values: Refer to Status Codes.

Data type: Number

</td></tr><tr><td>

result.stream

</td><td>

Sys\_id specified in request **context** query parameter.Data type: String

Table: Activity Context \[sn\_actsub\_activity\_context\]

</td></tr><tr><td>

result.user

</td><td>

Sys\_id specified in request **context\_instance** query parameter. Located in the appropriate table for the activity context.Data type: String

</td></tr></tbody>
</table>### cURL request

Request the second and third activity records for a specific Contact, limiting to data from 2020:

```
curl "https://instance.servicenow.com/api/now/actsub/activities\
?context=4a6a035a73d30010e37d71ef64f6a714\
&context_instance=ddce70866f9331003b3c498f5d3ee417\
&stFrom=1&last=3\
&start_date=2020-01-01%2000:00:00&end_date=2020-12-31%2023:59:59" \
--request GET \
--header "Accept: application/json" \
--user "username:password"
```

The response body includes the two requested activity records for the specified Contact:

```
{
  "result": {
    "hasMoreRecords": true,
    "activities": [
      {
        "subobject_table_name": "sn_customerservice_case",
        "source_table_name": "sn_customerservice_case",
        "content_fields": [
          {
            "value": "Test",
            "show_label": "false",
            "type": "string",
            "label": "Short description",
            "display_as_timeago": "false",
            "deeplink_to_subobject": "false"
          }
        ],
        "created": "2020-05-29 18:42:16",
        "activity_type_id": "baf0aace73530010e37d71ef64f6a748",
        "title": "Lamar Wilson created case",
        "subobject_sys_id": "1687360e8d819010f87705a074e52ac9",
        "icon": "clipboard_outline",
        "sys_id": "1687360e8d819010f87705a074e52ac9",
        "subheader_fields": [
          {
            "value": "CS0001007",
            "show_label": "false",
            "type": "string",
            "label": "Number",
            "display_as_timeago": "false",
            "deeplink_to_subobject": "true"
          },
          {
            "value": "2020-05-29 18:42:16",
            "show_label": "false",
            "type": "glide_date_time",
            "label": "Created",
            "display_as_timeago": "true",
            "deeplink_to_subobject": "false"
          },
          {
            "value": "",
            "show_label": "false",
            "type": "reference",
            "label": "Assigned to",
            "display_as_timeago": "false",
            "deeplink_to_subobject": "false"
          },
          {
            "value": "Lamar Wilson",
            "show_label": "false",
            "type": "reference",
            "label": "Contact",
            "display_as_timeago": "false",
            "deeplink_to_subobject": "false"
          }
        ]
      },
      {
        "subobject_table_name": "kb_knowledge",
        "source_table_name": "kb_use",
        "content_fields": [
          {
            "value": "How to Set Up a Broadband Router",
            "show_label": "false",
            "type": "string",
            "label": "Short description",
            "display_as_timeago": "false",
            "deeplink_to_subobject": "false"
          }
        ],
        "created": "2020-05-26 10:00:00",
        "activity_type_id": "4a8c329273d30010e37d71ef64f6a7c1",
        "title": "Lamar Wilson viewed knowledge article",
        "subobject_sys_id": "f855a0a89f011200550bf7b6077fcf4f",
        "icon": "document_outline",
        "sys_id": "b929dd5873941010e37d71ef64f6a719",
        "subheader_fields": [
          {
            "value": "KB0000110",
            "show_label": "false",
            "type": "string",
            "label": "Number",
            "display_as_timeago": "false",
            "deeplink_to_subobject": "true"
          },
          {
            "value": "2020-05-26 10:00:00",
            "show_label": "false",
            "type": "glide_date_time",
            "label": "Created",
            "display_as_timeago": "true",
            "deeplink_to_subobject": "false"
          }
        ]
      }
    ]
  }
}
```

## ActivitySubscriptions - GET /now/actsub/facets/\{activity\_context\}/\{context\_instance\}

Retrieves facets configured for an activity context from the Subscriptions and Activity Feed Framework. Displays activity counts and data for each facet as determined by activity type, group, and context settings.

Users must have the actsub\_user or admin role to access this endpoint. Data returned is limited by user access settings.

For more details on activity context facets, see Create facets for activity contexts.

### URL format

Versioned URL: `/api/now/{api_version}/actsub/facets/{activity_context}/{context_instance}`

Default URL: `/api/now/actsub/facets/{activity_context}/{context_instance}`

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

activity\_context

</td><td>

Sys\_id of an activity context.Predefined activity contexts include Consumer and Contact. Navigate to **Customer Central** &gt; **Customer Activity** &gt; **Activity Contexts** to view the full list of activity contexts defined for your instance.

Data type: String

Table: Activity Contexts \[sn\_actsub\_activity\_context\]

</td></tr><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`. Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr><tr><td>

context\_instance

</td><td>

Sys\_id of an instance of the specified activity context, representing the initiator of the activities you want to retrieve facets for.As an example, if you set **activity\_context** to the sys\_id of the Contact activity context, you should set this parameter to the sys\_id of the Contact \[customer\_contact\] record for the contact whose activity facets you want to retrieve.

Data type: String

Table: In the context table specified for the activity context record in the Activity Contexts \[sn\_actsub\_activity\_context\] table.

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

end\_date

</td><td id="end-date-query-param-entry">

Date/time value. The request returns only records created during the time period defined by **start\_date** and this parameter. Must be set along with **start\_date**.Data type: String

 Format: YYYY-MM-DD hh:mm:ss or YYYY-MM-DD

</td></tr><tr><td>

facets

</td><td>

Comma-separated list of sys\_ids of activity facets to retrieve for the specified activity context.To see the activity facet types defined for an activity context, navigate to **Customer Central** &gt; **Customer Activity** &gt; **Activity Contexts** and examine the **Facets** related list.

Data type: String

Default: Return all activity facets configured for the activity context.

</td></tr><tr><td>

get\_activity\_count

</td><td>

Flag indicating whether or not to include activity counts for each facet in the response body.Valid values:

-   true: Include facet activity counts.
-   false: Omit facet activity counts.

Data type: Boolean

Default: false

</td></tr><tr><td>

lazy\_load

</td><td>

Flag indicating whether or not to improve performance by omitting facet activity data and activity counts from the response body. This parameter takes precedence over **get\_activity\_count**.Valid values:

-   true: Omit facet activity data and activity counts.
-   false: Retrieve facet activity data and activity counts.

Data type: Boolean

Default: false

</td></tr><tr><td>

start\_date

</td><td id="start-date-query-param-entry">

Date/time value. The request returns only records created during the time period defined by this parameter and **end\_date**. Must be set along with **end\_date**.Data type: String

 Format: YYYY-MM-DD hh:mm:ss or YYYY-MM-DD

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

400

</td><td id="entry-400-status-code">

Bad Request. A bad request type or malformed request was detected. The response body **result.message** parameter describes the nature of the error.Example error messages:

-   `Make sure a valid activity context details are passed` indicates that the **activity\_context** path parameter value does not represent a valid activity context, the **context\_instance** path parameter value does not represent a valid instance of the specified activity context, or both.
-   `Please provide start_date and end_date` indicates that the request includes only one of the **start\_date** and **end\_date** query parameters, which cannot be used separately.
-   `start_date can not be ahead of end_date` indicates that the specified **start\_date** query parameter value occurs after the specified **end\_date** query parameter value.

</td></tr><tr><td>

401

</td><td id="entry-401-status-code">

Unauthorized. The user credentials are incorrect or have not been passed.

</td></tr><tr><td>

500

</td><td id="entry-500-status-code">

Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.

</td></tr></tbody>
</table>### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

List of activity facets.Data type: Array of Objects

```
"result": [
  {
    "activity_count": Number,
    "children": [Array],
    "facets": [Array],
    "icon": "String",
    "is_dynamic": "String",
    "message": "String",
    "name": "String",
    "status": Number
  }
]
```

</td></tr><tr><td>

result.activity\_count

</td><td>

Number of activity records included in this facet \(and its children, if any. Only displayed when **lazy\_load** query parameter is false and **get\_activity\_count** query parameter is true.Data type: Number

</td></tr><tr><td>

result.children

</td><td>

Array of objects in which each object represents an activity record \(if this is a dynamic facet\) or a child facet \(if this is a static facet\).Data type: Array of Objects

```

"children": [
  {
    "activity_count": Number
    "facet": "String",
    "icon": "String",
    "title": "String"
  }
]
```

</td></tr><tr><td>

result.children.activity\_count

</td><td>

Number of activity records included in this child facet \(and its children, if any\). Only displayed when the **lazy\_load** query parameter is false and the **get\_activity\_count** query parameter is true.Data type: Number

</td></tr><tr><td>

result.children.created

</td><td>

Creation date/time for this activity record.Data type: String

Format: YYYY-MM-DD hh:mm:ss

</td></tr><tr><td>

result.children.facet

</td><td>

Sys\_id of this child facet record.Data type: String

Table: Activity Facet \[sn\_actsub\_facet\]

</td></tr><tr><td>

result.children.icon

</td><td>

Name of the icon associated with this child facet.Data type: String

</td></tr><tr><td>

result.children.sys\_id

</td><td>

Sys\_id of this activity record. Located in the appropriate table for the parent facet type.As an example, an activity record included in the Cases facet has a sys\_id located in the Case \[sn\_customerservice\_case\] table.

Data type: String

</td></tr><tr><td>

result.children.metadata

</td><td>

Array of objects in which each object includes activity record data for a facet field configured in the Activity Facet \[sn\_actsub\_facet\] table record for this facet type.Data type: Array of Objects

```

"metadata": [
  {
    "key": "String",
    "label": "String",
    "type": "String",
    "value": "String"
  }
]
```

</td></tr><tr><td>

result.children.metadata.key

</td><td>

Name of this facet field.Data type: String

</td></tr><tr><td>

result.children.metadata.label

</td><td>

Label of this facet field.Data type: String

</td></tr><tr><td>

result.children.metadata.type

</td><td>

Type of this facet field.Data type: String

</td></tr><tr><td>

result.children.metadata.value

</td><td>

Value of this facet field.Data type: String

</td></tr><tr><td>

result.children.title

</td><td>

Name of this activity record or child facet.Data type: String

</td></tr><tr><td>

result.facets

</td><td>

List of sys\_ids associated with this facet record. For a dynamic facet, this array contains the sys\_id of the facet itself. For a static facet, it instead contains the sys\_ids of all facets which are children of the facet.Data type: Array

```

"facets": [
  "510d7e2e73570010e37d71ef64f6a70d",
  "bc9bfaaa73570010e37d71ef64f6a771"
]
```

Table: Activity Facet \[sn\_actsub\_facet\]

</td></tr><tr><td>

result.icon

</td><td>

Name of the icon associated with this facet.Data type: String

</td></tr><tr><td>

result.is\_dynamic

</td><td>

Flag indicating whether or not this facet is a dynamic facet. This value determines the type of information included in the **children** response body parameter.Possible values:

-   true: This is a dynamic facet. The **children** response body parameter value contains activity record details, and the **facets** parameter contains the dynamic facet sys\_id.
-   false: This is a static facet \(a facet group\). The **children** response body parameter value contains child facets, and the **facets** parameter contains the sys\_ids of these child facets.

Data type: Boolean

</td></tr><tr><td>

result.message

</td><td>

Error message describing problem encountered during request processing.Data type: String

</td></tr><tr><td>

result.name

</td><td>

Name of the facet or facet group.Data type: String

</td></tr><tr><td>

result.status

</td><td>

HTTP status code returned for request.Possible values: See the Status Code table.

Data type: Number

</td></tr></tbody>
</table>### cURL request

Retrieve Chat, Phone, and Knowledge articles facets and activity counts for a Contact:

```
curl "https://instance.servicenow.com/api/now/actsub/facets/4a6a035a73d30010e37d71ef64f6a714/ddce70866f9331003b3c498f5d3ee417\
?get_activity_count=true\
&facets=510d7e2e73570010e37d71ef64f6a70d,bc9bfaaa73570010e37d71ef64f6a771,c72d7e2e73570010e37d71ef64f6a7b8" \
--request GET \
--header "Accept: application/json" \
--user "username:password"
```

The response body includes the three requested facets as children of their facet groups, with activity counts displayed:

```
{
  "result": [
    {
      "is_dynamic": false,
      "name": "Interactions",
      "activity_count": 4.0,
      "facets": [
        "510d7e2e73570010e37d71ef64f6a70d",
        "bc9bfaaa73570010e37d71ef64f6a771"
      ],
      "children": [
        {
          "facet": "510d7e2e73570010e37d71ef64f6a70d",
          "icon": "chat_outline",
          "activity_count": 2.0,
          "title": "Chat"
        },
        {
          "facet": "bc9bfaaa73570010e37d71ef64f6a771",
          "icon": "phone_outline",
          "activity_count": 2.0,
          "title": "Phone"
        }
      ]
    },
    {
      "is_dynamic": false,
      "name": "Portal Activity",
      "activity_count": 5.0,
      "facets": [
        "c72d7e2e73570010e37d71ef64f6a7b8"
      ],
      "children": [
        {
          "facet": "c72d7e2e73570010e37d71ef64f6a7b8",
          "icon": "document_outline",
          "activity_count": 5.0,
          "title": "Knowledge articles"
        }
      ]
    }
  ]
}
```

