---
title: Customer Central API
description: The Customer Central API provides endpoints to access customer information and configuration details.Returns customer information and configuration details for a specific customer context.
locale: en-US
release: zurich
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 13
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# Customer Central API

The Customer Central API provides endpoints to access customer information and configuration details.

Use this API to obtain information records \(cards\) that were previously generated through the Customer Central interface.

You must have the admin or sn\_esm\_agent role to access this API. In addition, before this API is available in your instance you must activate the **com.sn\_csm\_customer\_central** plugin.

For additional information, see [Customer Central](https://www.servicenow.com/docs/access?context=customer-central&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US).

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## Customer Central - GET /cust\_central/custinfo/\{context\}/\{context\_instance\}/\{target\}

Returns customer information and configuration details for a specific customer context.

Customer context is determined by the customer content table that you specify, either the Consumer \[csm\_consumer\] or Contact \[customer\_contact\] table, and its associated target table. This information is located in the Customer Information Context \[sn\_customercentral\_cust\_info\_config\] table.

This endpoint returns all active records \(cards\) within the following Customer Central configuration tables for the specified customer context:

-   List Configuration \[sn\_customercentral\_list\_config\]
-   Record Configuration \[sn\_customercentral\_record\_config\]
-   Report Configuration \[sn\_customercentral\_report\_config\]
-   Report Group Configuration \[sn\_customercentral\_report\_group\_config\]

You must define any additional configuration records that you need through the Customer Central interface. For details, see [Configure customer central](https://www.servicenow.com/docs/access?context=configure-customer-central&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US).

### URL format

Versioned URL: `/api/sn_customercentral/{api_version}/cust_central/custinfo/{context}/{context_instance}/{target}`

Default URL: `/api/sn_customercentral/cust_central/custinfo/{context}/{context_instance}/{target}`

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

context

</td><td>

Name of the customer context table to use.Valid values:

-   csm\_consumer
-   customer\_contact

Data type: String

</td></tr><tr><td>

context\_instance

</td><td>

Sys\_id of the record in the table specified in the **context** parameter to return. Data type: String

</td></tr><tr><td>

target

</td><td>

Target table associated with the customer context table specified in the **context** parameter. The combination of the **context** parameter and**target** parameter define a unique customer information context. Data type: String

Table: Customer Information Context \[sn\_customercentral\_cust\_info\_config\]

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

before

</td><td>

Return all configuration records created before the specified date and time.Date type: String

Format: YYYY-MM-DD or the format defined in the **glide.sys.date\_format** system property

Default: Return all configuration records created before current session time.

</td></tr><tr><td>

end

</td><td>

Last record to return. Use this value to paginate record retrieval or use with the **start** parameter to select a specific set of records to return.Data type: Number

Default: Last record in file

</td></tr><tr><td>

start

</td><td>

Starting record index for which to begin retrieving records. Use this value to paginate record retrieval. This functionality enables the retrieval of all records, regardless of the number of records, in small manageable chunks. Don't pass a negative number.

Data type: Number

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

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|400|Bad Request. A bad request type or malformed request was detected. Ensure that the path parameters contain valid values.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

cards\_info

</td><td>

List of contact cards associated with the specified customer.Data type: Array \(content depends on selected customer\)

</td></tr><tr><td>

cards\_info.data\_configurations

</td><td>

Configuration information.Data type: Object

```
"data_configurations": {
  "aggregate_field": "String",
  "aggregate_function": "String",
  "chart_settings": "String"
  "decimal_precision": Number,
  "filter_query": "String",
  "group_by": "String",
  "number_of_groups": "String",
  "show_other": Boolean,
  "source_id": "String",
  "source_type": "String",
  "stack_by_field": "String",
  "sys_id": "String",
  "trend_field": "String",
  "trend_interval": "String",
  "type": "String"
}
```

</td></tr><tr><td>

cards\_info.data\_configurations.aggregate\_field

</td><td>

Column name to aggregate. Data type: String

</td></tr><tr><td>

cards\_info.data\_configurations.aggregate\_function

</td><td>

Function to use to aggregate the specified table column.Possible values:

-   AVG
-   COUNT
-   COUNT\(DISTINCT\)
-   SUM

Data type: String

</td></tr><tr><td>

cards\_info.data\_configurations.decimal\_precision

</td><td>

Number of digits to the right of the decimal point to return.Data type: Number

</td></tr><tr><td>

cards\_info.data\_configurations.filter\_query

</td><td>

Query string to use to refine the data used in the report.Data type: String

</td></tr><tr><td>

cards\_info.data\_configurations.group\_by

</td><td>

Name of the column to use to group the report data.Data type: String

</td></tr><tr><td>

cards\_info.data\_configurations.number\_of\_groups

</td><td>

Maximum number of groups to display in the report.Possible values:

-   `all`: Show all groups.
-   0: Uses the value in the **glide.ui.chart.generate\_other** system property.

**Note:** It is not recommended to change the value of the **glide.ui.chart.generate\_other** system property, as it applies to all reports in the instance.

-   Greater than 0: Number of groups to display. The groups that appear are the ones with the highest values for whatever is being tracked.

Data type: String

</td></tr><tr><td>

cards\_info.data\_configurations.show\_other

</td><td>

Flag that indicates whether the group "Other" appears within the report. If not all groups are to display, as defined by the **number\_of\_groups** parameter, the values of the non-display groups are combined and displayed under a single heading of "Other".Possible values:

-   true: Include the "Other" group.
-   false: Don't include the "Other" group.

Data type: Boolean

</td></tr><tr><td>

cards\_info.data\_configurations.source\_id

</td><td>

Table name or sys\_id of the report source information. This correlates to the information in the **cards\_info.reportGroupConfigurations.data\_configurations.source\_type** parameter.Data type: String

</td></tr><tr><td>

cards\_info.data\_configurations.source\_type

</td><td>

Type of information in the **cards\_info.reportGroupConfigurations.data\_configurations.source\_id** parameter used to identify the source table.Possible values:

-   source: Sys\_id of the source table.
-   table: Table name of the source table.

Data type: String

</td></tr><tr><td>

cards\_info.data\_configurations.stack\_by\_field

</td><td>

Name of the table column to use when implementing "stack by" in the report.Data type: String

</td></tr><tr><td>

cards\_info.data\_configurations.sys\_id

</td><td>

Sys\_id of the report used in the report configuration.Data type: String

</td></tr><tr><td>

cards\_info.data\_configurations.trend\_field

</td><td>

Name of table column to use in trend analysis.Data type: String

</td></tr><tr><td>

cards\_info.data\_configurations.trend\_interval

</td><td>

Time interval for the trend information. For example, week, month, year, etc.Data type: String

</td></tr><tr><td>

cards\_info.data\_configurations.type

</td><td>

Type of report, such as single score, donut, vertical, line, stacked bar, etc.Data type: String

</td></tr><tr><td>

cards\_info.encodedQuery

</td><td>

Encoded query string to use to refine the data that appears in the report.Data type: String

</td></tr><tr><td>

cards\_info.fields

</td><td>

List of name-value pairs that define the fields within the associated record.Data type: Array of Objects

```
"fields": [
  {
    "label": "String",
    "value": "String"
  }
]
```

</td></tr><tr><td>

cards\_info.fields.label

</td><td>

Field label.Data type: String

</td></tr><tr><td>

cards\_info.fields.value

</td><td>

Field value.Data type: String

</td></tr><tr><td>

cards\_info.listLimit

</td><td>

Pagination limit. Number of records to show on a list card.Data type: String

</td></tr><tr><td>

cards\_info.reportGroupConfigurations

</td><td>

List of objects that define the report groups.Data type: Array of Objects

```
"reportGroupConfigurations": [
  {
    "data_configurations": {Object},
    "style_configurations": {Object},
    "title": "String",
    "type": "String"
  }
]
```

</td></tr><tr><td>

cards\_info.reportGroupConfigurations.data\_configurations

</td><td>

Configuration information.Data type: Object

```
"data_configurations": {
  "aggregate_field": "String",
  "aggregate_function": "String",
  "chart_settings": "String"
  "decimal_precision": Number,
  "filter_query": "String",
  "group_by": "String",
  "number_of_groups": "String",
  "show_other": Boolean,
  "source_id": "String",
  "source_type": "String",
  "stack_by_field": "String",
  "sys_id": "String",
  "trend_field": "String",
  "trend_interval": "String",
  "type": "String"
}
```

</td></tr><tr><td>

cards\_info.reportGroupConfigurations.data\_configurations.aggregate\_field

</td><td>

Column name to aggregate. Data type: String

</td></tr><tr><td>

cards\_info.reportGroupConfigurations.data\_configurations.aggregate\_function

</td><td>

Function to use to aggregate the specified table column.Possible values:

-   AVG
-   COUNT
-   COUNT\(DISTINCT\)
-   SUM

Data type: String

</td></tr><tr><td>

cards\_info.reportGroupConfigurations.data\_configurations.decimal\_precision

</td><td>

Number of digits to the right of the decimal point to return.Data type: Number

</td></tr><tr><td>

cards\_info.reportGroupConfigurations.data\_configurations.filter\_query

</td><td>

Query string to use to refine the data used in the report.Data type: String

</td></tr><tr><td>

cards\_info.reportGroupConfigurations.data\_configurations.group\_by

</td><td>

Name of the column to use to group the report data.Data type: String

</td></tr><tr><td>

cards\_info.reportGroupConfigurations.data\_configurations.number\_of\_groups

</td><td>

Maximum number of groups to display in the report.Possible values:

-   `all`: Show all groups.
-   0: Uses the value in the **glide.ui.chart.generate\_other** system property.

**Note:** It is not recommended to change the value of the **glide.ui.chart.generate\_other** system property, as it applies to all reports in the instance.

-   Greater than 0: Number of groups to display. The groups that appear are the ones with the highest values for whatever is being tracked.

Data type: String

</td></tr><tr><td>

cards\_info.reportGroupConfigurations.data\_configurations.show\_other

</td><td>

Flag that indicates whether the group "Other" appears within the report. If not all groups are to display, as defined by the **number\_of\_groups** parameter, the values of the non-display groups are combined and displayed under a single heading of "Other".Possible values:

-   true: Include the "Other" group.
-   false: Don't include the "Other" group.

Data type: Boolean

</td></tr><tr><td>

cards\_info.reportGroupConfigurations.data\_configurations.source\_id

</td><td>

Table name or sys\_id of the report source information. This correlates to the information in the **cards\_info.reportGroupConfigurations.data\_configurations.source\_type** parameter.Data type: String

</td></tr><tr><td>

cards\_info.reportGroupConfigurations.data\_configurations.source\_type

</td><td>

Type of information in the **cards\_info.reportGroupConfigurations.data\_configurations.source\_id** parameter used to identify the source table.Possible values:

-   source: Sys\_id of the source table.
-   table: Table name of the source table.

Data type: String

</td></tr><tr><td>

cards\_info.reportGroupConfigurations.data\_configurations.stack\_by\_field

</td><td>

Name of the table column to use when implementing "stack by" in the report.Data type: String

</td></tr><tr><td>

cards\_info.reportGroupConfigurations.data\_configurations.sys\_id

</td><td>

Sys\_id of the report used in the report configuration.Data type: String

</td></tr><tr><td>

cards\_info.reportGroupConfigurations.data\_configurations.trend\_field

</td><td>

Name of table column to use in trend analysis.Data type: String

</td></tr><tr><td>

cards\_info.reportGroupConfigurations.data\_configurations.trend\_interval

</td><td>

Time interval for the trend information. For example, week, month, year, etc.Data type: String

</td></tr><tr><td>

cards\_info.reportGroupConfigurations.data\_configurations.type

</td><td>

Type of report associated with the report group, such as donut or single\_core.Data type: String

</td></tr><tr><td>

cards\_info.reportGroupConfigurations.style\_configurations

</td><td>

Styles to use within the associated report group.Data type: Object

```
"style_configurations": {
  "colorPalette": "String",
  "scoreColor": "String",
  "show_zero": Boolean
}
```

</td></tr><tr><td>

cards\_info.reportGroupConfigurations.style\_configurations.colorPalette

</td><td>

Colors used in the report.Data type: String

</td></tr><tr><td>

cards\_info.reportGroupConfigurations.style\_configurations.scoreColor

</td><td>

Color of the score value within the report.Data type: String

</td></tr><tr><td>

cards\_info.reportGroupConfigurations.style\_configurations.show\_zero

</td><td>

Flag that indicates whether data points equal to zero are shown in the report.Possible values:

-   true: Zero values are shown.
-   false: Zero values aren't shown.

Data type: Boolean

</td></tr><tr><td>

cards\_info.reportGroupConfigurations.title

</td><td>

Title of the report group.Data type: String

</td></tr><tr><td>

cards\_info.reportGroupConfigurations.type

</td><td>

File type for which the information is being returned.Always sn\_customercentral\_report\_config.

Data type: String

</td></tr><tr><td>

cards\_info.sourceTableName

</td><td>

Name of the table used for the associated list card.Data type: String

</td></tr><tr><td>

cards\_info.style\_configurations

</td><td>

Styles to use within the associated report.Data type: Object

```
"style_configurations": {
  "colorPalette": "String",
  "dataLabelConfig": {Object},
  "height": "String",
  "hideRegister": Boolean,
  "registerConfig": {Object},
  "registerPosition": "String",
  "scoreColor": "String",
  "showDataLabels": Boolean,
  "showTooltip": Boolean,
  "show_zero": Boolean,
  "width": "String"
}
```

</td></tr><tr><td>

cards\_info.style\_configurations.colorPalette

</td><td>

Colors used in the report.Data type: String

</td></tr><tr><td>

cards\_info.style\_configurations.dataLabelConfig

</td><td>

Configuration parameters that control how data labels appear in the report.Data type: Object

```
"dataLabelConfig": [
  {
    "showTotal": Boolean
  }
]
```

</td></tr><tr><td>

cards\_info.style\_configurations.dataLabelConfig.showTotal

</td><td>

Flag that indicates whether to display the total in the report.Possible values:

-   true: Show totals.
-   false: Don't show totals.

Data type: Boolean

</td></tr><tr><td>

cards\_info.style\_configurations.height

</td><td>

Height of the associated report.Data type: String

Unit: Pixels or "auto"

</td></tr><tr><td>

cards\_info.style\_configurations.hideRegister

</td><td>

Flag that indicates whether to display the register in the card.Possible values:

-   true: Show the register.
-   false: Don't show the register.

Data type: Boolean

</td></tr><tr><td>

cards\_info.style\_configurations.registerConfig

</td><td>

Configuration values that control how the register appears in the report.Data type: Object

```
"registerConfig": {
  "hideBorder": Boolean,
  "showPercentages": Boolean
}
```

</td></tr><tr><td>

cards\_info.style\_configurations.registerConfig.hideBorder

</td><td>

Flag that indicates whether to hide the border around the register.Possible values:

-   true: Hide the register border.
-   false: Show the register border.

Data type: Boolean

</td></tr><tr><td>

cards\_info.style\_configurations.registerConfig.showPercentages

</td><td>

Flag that indicates whether to show register percentages.Possible values:

-   true: Show register percentages.
-   false: Hide register percentages.

Data type: Boolean

</td></tr><tr><td>

cards\_info.style\_configurations.registerPosition

</td><td>

Position of the register within a card.Data type: String

</td></tr><tr><td>

cards\_info.style\_configurations.scoreColor

</td><td>

Color of the score value within the report.Data type: String

</td></tr><tr><td>

cards\_info.style\_configurations.showDataLabels

</td><td>

Flag that indicates whether to show the data labels within the report.Possible values:

-   true: Show the data labels.
-   false: Hide the data labels.

Data type: Boolean

</td></tr><tr><td>

cards\_info.style\_configurations.showTooltip

</td><td>

Flag that indicates whether to show tool tips within the report.Possible values:

-   true: Show tool tips.
-   false: Hide tool tips.

Data type: Boolean

</td></tr><tr><td>

cards\_info.style\_configurations.show\_zero

</td><td>

Flag that indicates whether data points equal to zero are shown in the report.Possible values:

-   true: Zero values are shown.
-   false: Zero values aren't shown.

Data type: Boolean

</td></tr><tr><td>

cards\_info.style\_configurations.width

</td><td>

Width of the associated report.Data type: String

Unit: Pixels or "auto"

</td></tr><tr><td>

cards\_info.subheader\_fields

</td><td>

Details to show on the sub-header of the associated card.Data type: Object

```
"subheader_fields": {
  "avatar": "String",
  "subheader_tags": [Array],
  "sys_id": "String",
  "title": "String"
}
```

</td></tr><tr><td>

cards\_info.subheader\_fields.avatar

</td><td>

File name of the avatar associated with the specified**context\_instance**, such as the contact's avatar.![Avatar placement](../image/cust-central_avatar.png)

Data type: String

</td></tr><tr><td>

cards\_info.subheader\_fields.subheader\_tags

</td><td>

List of tags associated with the record sub-header, such as escalation tags.![Sub-header tag placement](../image/cust-central_sub-header_tags.png)

Data type: Array \(content varies\)

</td></tr><tr><td>

cards\_info.subheader\_fields.sys\_id

</td><td>

Sys\_id of the associated customer.Data type: String

Table: Users \[sys\_user\]

</td></tr><tr><td>

cards\_info.subheader\_fields.title

</td><td>

Title to display on the sub-header.![Sub-header title placement](../image/cust-central_sub-header-title.png)

Data type: String

</td></tr><tr><td>

cards\_info.title

</td><td>

Title on the card \(record\).Data type: String

</td></tr><tr><td>

cards\_info.type

</td><td>

File type for which the information is being returned.Possible values:

-   sn\_customercentral\_list\_config: List Configuration
-   sn\_customercentral\_record\_config: Record Configuration
-   sn\_customercentral\_report\_config: Report Configuration
-   sn\_customercentral\_report\_group\_config: Report Group Configuration

Data type: String

</td></tr><tr><td>

cards\_info.viewName

</td><td>

Name of the view configured for the table specified in **cards\_info.sourceTableName**.Data type: String

</td></tr><tr><td>

has\_more\_records

</td><td>

Flag that indicates whether there are more records to retrieve.Possible values:

-   true: More records to retrieve.
-   false: No more records.

Data type: Boolean

</td></tr><tr><td>

layout

</td><td>

Number of columns per row. Each comma separated value defines the width of a column on the report display. For example "6,6" denotes two columns, each being six units wide, for a total of 12 units per row \(maximum\). A value of "3,6,3" denotes a row with three columns.Data type: String

</td></tr><tr><td>

status

</td><td>

HTTP status of the request.Data type: String

</td></tr></tbody>
</table>### cURL request

```
curl "https://instance.servicenow/api/sn_customercentral/cust_central/custinfo/csm_consumer/a0488cfbdb1b1200b6075200cf9619db/interaction" \
--request GET \
--header "Accept:application/json" \
--user "username":"password"
```

```
{
  "result": {
    "layout": "6,6",
    "cards_info": [
      {
        "title": "Consumer",
        "type": "sn_customercentral_record_config",
        "subheader_fields": {
          "title": "Sam Collins",
          "subheader_tags": [],
          "avatar": "",
          "sys_id": "64488cfbdb1b1200b6075200cf9619db"
        },
        "fields": [
          {
            "label": "Mobile phone",
            "value": ""
          },
          {
            "label": "Business phone",
            "value": ""
          },
          {
            "label": "Email",
            "value": "sam.collins@mailinator.com"
          },
          {
            "label": "Street",
            "value": "144 2nd St"
          },
          {
            "label": "City",
            "value": "San Francisco"
          },
          {
            "label": "State / Province",
            "value": "CA"
          }
        ]
      },
      {
        "title": "High priority cases",
        "type": "sn_customercentral_report_group_config",
        "reportGroupConfigurations": [
          {
            "title": "Escalated",
            "type": "sn_customercentral_report_config",
            "data_configurations": {
              "type": "single_score",
              "source_type": "table",
              "source_id": "sn_customerservice_case",
              "group_by": "",
              "trend_interval": "year",
              "trend_field": "",
              "stack_by_field": "",
              "aggregate_function": "COUNT",
              "aggregate_field": "",
              "filter_query": "active=true^active_escalationISNOTEMPTY^EQ^consumer=a0488cfbdb1b1200b6075200cf9619db^ORDERBYDESCsys_created_on^sys_created_on>=2020-04-07 13:40:48",
              "decimal_precision": 2,
              "number_of_groups": 0,
              "show_other": true,
              "sys_id": "c169a0f50f3b0010e6d4fd820b767e2e"
            },
            "style_configurations": {
              "scoreColor": "#000000",
              "show_zero": true
            }
          },
          {
            "title": "P1",
            "type": "sn_customercentral_report_config",
            "data_configurations": {
              "type": "single_score",
              "source_type": "table",
              "source_id": "sn_customerservice_case",
              "group_by": "",
              "trend_interval": "year",
              "trend_field": "",
              "stack_by_field": "",
              "aggregate_function": "COUNT",
              "aggregate_field": "",
              "filter_query": "active=true^priority=1^EQ^consumer=a0488cfbdb1b1200b6075200cf9619db^ORDERBYDESCsys_created_on^sys_created_on>=2020-04-07 13:40:48",
              "decimal_precision": 2,
              "number_of_groups": 0,
              "show_other": true,
              "sys_id": "cce86cb50f3b0010e6d4fd820b767eba"
            },
            "style_configurations": {
              "scoreColor": "#000000",
              "show_zero": true
            }
          },
          {
            "title": "SLA breached",
            "type": "sn_customercentral_report_config",
            "data_configurations": {
              "type": "single_score",
              "source_type": "table",
              "source_id": "task_sla",
              "group_by": "",
              "trend_interval": "year",
              "trend_field": "",
              "stack_by_field": "",
              "aggregate_function": "COUNT",
              "aggregate_field": "",
              "filter_query": "task.active=true^task.sys_class_name=sn_customerservice_case^stage!=cancelled^task.closed_atISEMPTY^sla.type=SLA^has_breached=true^EQ^taskIN59b65dc4db952200d75270f5bf96193eccc8cf82db912200d75270f5bf9619de^ORDERBYDESCsys_created_on^sys_created_on>=2020-04-07 13:40:48",
              "decimal_precision": 2,
              "number_of_groups": 0,
              "show_other": true,
              "sys_id": "e739a0f50f3b0010e6d4fd820b767e22"
            },
            "style_configurations": {
              "scoreColor": "#000000",
              "show_zero": true
            }
          }
        ]
      },
      {
        "title": "Case overview",
        "type": "sn_customercentral_report_config",
        "data_configurations": {
          "type": "donut",
          "source_type": "table",
          "source_id": "sn_customerservice_case",
          "group_by": "state",
          "trend_interval": "year",
          "trend_field": "",
          "stack_by_field": "",
          "aggregate_function": "COUNT",
          "aggregate_field": "",
          "filter_query": "^consumer=a0488cfbdb1b1200b6075200cf9619db^ORDERBYDESCsys_created_on^sys_created_on>=2020-04-07 13:40:48",
          "decimal_precision": 2,
          "number_of_groups": 0,
          "show_other": true,
          "sys_id": "d169216c0f770010e6d4fd820b767ea8"
        },
        "style_configurations": {
          "width": "auto",
          "height": "auto",
          "colorPalette": [
            "#278ecf",
            "#4bd762",
            "#ffca1f",
            "#ff9416",
            "#d42ae8"
          ],
          "hideRegister": false,
          "registerConfig": {
            "hideBorder": true,
            "showPercentages": false
          },
          "registerPosition": "right",
          "showDataLabels": false,
          "dataLabelConfig": {
            "showTotal": false
          },
          "showTooltip": true
        }
      },
      {
        "title": "Recent cases",
        "type": "sn_customercentral_list_config",
        "listLimit": "3",
        "viewName": "customer_central",
        "encodedQuery": "active=true^consumer=a0488cfbdb1b1200b6075200cf9619db^ORDERBYDESCsys_created_on^sys_created_on>=2020-04-07 13:40:48",
        "sourceTableName": "sn_customerservice_case"
      },
      {
        "title": "Recent chat interactions",
        "type": "sn_customercentral_list_config",
        "listLimit": "3",
        "viewName": "customer_central",
        "encodedQuery": "active=false^type=chat^consumer=a0488cfbdb1b1200b6075200cf9619db^ORDERBYDESCsys_created_on^sys_created_on>=2020-04-07 13:40:48",
        "sourceTableName": "interaction"
      },
      {
        "title": "Recent phone calls",
        "type": "sn_customercentral_list_config",
        "listLimit": "3",
        "viewName": "customer_central",
        "encodedQuery": "active=false^type=phone^consumer=a0488cfbdb1b1200b6075200cf9619db^ORDERBYDESCsys_created_on^sys_created_on>=2020-04-07 13:40:48",
        "sourceTableName": "interaction"
      },
      {
        "title": "Recent viewed articles",
        "type": "sn_customercentral_list_config",
        "listLimit": "3",
        "viewName": "customer_central",
        "encodedQuery": "user=64488cfbdb1b1200b6075200cf9619db^viewed=true^ORDERBYDESCsys_created_on^sys_created_on>=2020-04-07 13:40:48",
        "sourceTableName": "kb_use"
      },
      {
        "title": "Contracts",
        "type": "sn_customercentral_list_config",
        "listLimit": "3",
        "viewName": "customer_central",
        "encodedQuery": "active=true^state=Active^consumer=a0488cfbdb1b1200b6075200cf9619db^ORDERBYDESCsys_created_on^sys_created_on>=2020-04-07 13:40:48",
        "sourceTableName": "ast_contract"
      },
      {
        "title": "Entitlements",
        "type": "sn_customercentral_list_config",
        "listLimit": "3",
        "viewName": "customer_central",
        "encodedQuery": "active=true^end_date=NULL^ORend_date>=2020-05-07 07:00:00^consumer=a0488cfbdb1b1200b6075200cf9619db^ORDERBYDESCsys_created_on^sys_created_on>=2020-04-07 13:40:48",
        "sourceTableName": "service_entitlement"
      }
    ],
    "has_more_records": false,
    "status": "200"
  }
}
```

