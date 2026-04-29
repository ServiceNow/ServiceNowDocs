---
title: ATF Code Coverage API
description: The ATF Code Coverage API provides endpoints to compute code coverage from Automated Test Framework \(ATF\) runs. Coverage can be retrieved by filtered line numbers, for specific script IDs, or for all scripts covered by a set of test suite/test runs.Aggregates coverage across all scripts covered by the provided ATF runs. Supports combining test suite runs and individual test runs.Computes coverage for specific script records.Computes code coverage using a set of filtered line numbers per metadata record.
locale: en-US
release: australia
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 15
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# ATF Code Coverage API

The ATF Code Coverage API provides endpoints to compute code coverage from Automated Test Framework \(ATF\) runs. Coverage can be retrieved by filtered line numbers, for specific script IDs, or for all scripts covered by a set of test suite/test runs.

ATF code coverage is a tool that enables you to determine what percentage of code in a deployment request is covered by ATF test suites.

By default, if ATF test suites cover less than 70% of the code in a deployment request, ReleaseOps transitions the deployment request to the Reconciling state and a test failure task is automatically created. You can adjust the ATF code coverage threshold in the deployment request assessment playbook. For more information, see [Set Automated Test Framework \(ATF\) code coverage](https://www.servicenow.com/docs/access?context=set-atf-code-coverage-threshold&version=australia&pubname=australia-application-development&ft:locale=en-US).

For information on ATF and Performance Analyzer, see [Testing and debugging applications](https://www.servicenow.com/docs/access?context=testing-and-debugging-applications&version=australia&pubname=australia-application-development&ft:locale=en-US)

[Deployment analyzer in ReleaseOps](https://www.servicenow.com/docs/access?context=deployment-analyzer&version=australia&pubname=australia-application-development&ft:locale=en-US)

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## ATF Code Coverage - POST /now/atf/code\_coverage/all

Aggregates coverage across all scripts covered by the provided ATF runs. Supports combining test suite runs and individual test runs.

### URL format

Versioned URL: `/api/now/v1/atf/code_coverage/all`

Default URL: `/api/now/atf/code_coverage/all`

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

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

test\_suite\_result\_ids

</td><td>

Required unless `test_result_ids` are provided. List of test suite result sys\_ids.Table: Test Suite Results \[sys\_atf\_test\_suite\_result\]

Data type: Array of strings

</td></tr><tr><td>

test\_result\_ids

</td><td>

Required unless `test_suite_result_ids` are provided. List of test result sys\_ids to include \(can be combined with suites\). Table: Test Results \[sys\_atf\_test\_result\]

Data type: Array of strings

</td></tr><tr><td>

verbose

</td><td>

Flag that indicates level of detail to provide in the response for each custom test script.Valid values:

-   true: Include detailed per-item coverage in the response body **details** object.
-   false: The response body **details** object will return empty or not at all.

Default: false

Data type: Boolean

</td></tr><tr><td>

sys\_scopes

</td><td>

Filter results to specified application scopes \(e.g., `["x_my_app", "global"]`\). Multiple scopes use OR logic, so any matching scope is included. No filtering occurs if any empty or NULL array is provided.Data type: Array of strings

</td></tr></tbody>
</table>### Headers

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
|400|Bad Request. A bad request type or malformed request was detected.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON\)

<table id="table_10z_n1c_i8e"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

link

</td><td>

Link to the request record.Data type: String

</td></tr><tr><td>

details.&lt;scriptId&gt;

</td><td>

Lists the ATF aggregation coverage percent of each custom test script by script sys\_id.Data type: Number

</td></tr><tr><td>

api\_request\_sys\_id

</td><td>

The sys\_id of the request.Table: ATF code coverage API requests \[sys\_atf\_code\_coverage\_request\]

Data type: String

</td></tr><tr><td>

result

</td><td>

Success or error message.Error response formats:

-   400 Bad Request

`{ "result": "Validation error: <specific_error_message>" }`

-   500 Internal Server Error

`{ "result": "Internal server error: <error_message>" }`


Possible errors:

-   Request body validation - `Request body is required and cannot be empty`
-   Test ID validation - `At least one valid (non-empty) ID must be provided in either test_result_ids or test_suite_result_ids`
-   Type mismatch - `Invalid data type in request parameters`

Data type: String

</td></tr><tr><td>

total

</td><td>

Overall code coverage percentage reflecting the combined ATF code coverage of the scripts listed in the **details** property. The value is zero if no custom scripts are associated with the tests provided or no percentage of code coverage has been provided.Possible values: 0-100

Data type: Number

</td></tr><tr><td>

truncation\_message

</td><td>

If request data was truncated during persistence, provides details about what scripts have truncated information.Example message:

`truncation_message: "Field atf_code_coverage_request.metadata_info truncated from 5000 to 4000 characters (max: 4000). Consider increasing column length to prevent data loss"`

Data type: String

</td></tr><tr><td>

was\_truncated

</td><td>

Flag that indicates whether request data was truncated during persistence. To reduce truncation, you can change the default number of characters supported.For example, `request_data_truncated: true`.

Valid values:

-   true: Request data was truncated during persistence.
-   false: Request data was not truncated during persistence.

Data type: Boolean

Default number of characters: 4000

</td></tr></tbody>
</table>### cURL request

The following example shows how to retrieve all of the code coverage for a selected test result suite and test result.

```
curl "https://instance.service-now.com/api/now/atf/code_coverage/all" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
  \"test_suite_result_ids\": [\"5f81c7c4ff943210b88affffffffffc5\"],
  \"test_result_ids\": [\"bb8daec1ff103210b88affffffffff1c\"],
  \"verbose\": true,
  \"sys_scopes\": [\"x_my_app\", \"global\"]
}" \
--user 'username':'password'
```

Output:

```
{
  "result": "success",
  "total": 73,
  "details": {
    "sys_script_include_a1b2c3d4e5f6a7b8c9d0e1f2a3b4c5d6": 85,
    "sys_script_include_b2c3d4e5f6a7b8c9d0e1f2a3b4c5d6e7": 92,
    "sys_ui_script_c3d4e5f6a7b8c9d0e1f2a3b4c5d6e7f8": 45,
    "sys_script_d4e5f6a7b8c9d0e1f2a3b4c5d6e7f8a9": 68,
    "sys_script_include_e5f6a7b8c9d0e1f2a3b4c5d6e7f8a9b0": 100
  },
  "api_request_sys_id": "f6a7b8c9d0e1f2a3b4c5d6e7f8a9b0c1",
  "link": "https://instance.service-now.com/sys_atf_code_coverage_request.do?sys_id=f6a7b8c9d0e1f2a3b4c5d6e7f8a9b0c1"
}
```

## ATF Code Coverage - POST /now/atf/code\_coverage/by\_script\_id

Computes coverage for specific script records.

To compute code coverage for all scripts covered by specified ATF runs, use the endpoint /now/atf/code\_coverage/all.

### URL format

Versioned URL: `/api/now/v1/atf/code_coverage/by_script_id`

Default URL: `/api/now/atf/code_coverage/by_script_id`

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

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

test\_suite\_result\_ids

</td><td>

Required unless `test_result_ids` are provided. List of test suite result sys\_ids.Table: Test Suite Results \[sys\_atf\_test\_suite\_result\]

Data type: Array of strings

</td></tr><tr><td>

test\_result\_ids

</td><td>

Required unless `test_suite_result_ids` are provided. List of test result sys\_ids to include \(can be combined with suites\). Table: Test Results \[sys\_atf\_test\_result\]

Data type: Array of strings

</td></tr><tr><td>

script\_array

</td><td>

Required. One or more valid script sys\_ids to evaluate for code coverage. Must contain at least one valid \(non-empty\) script identifier. Null, empty, or whitespace-only entries are filtered out.Table: Metadata Tracing \[sys\_traced\_metadata\]

Data type: Array

</td></tr><tr><td>

verbose

</td><td>

Flag that indicates level of detail to provide in the response for each custom test script.Valid values:

-   true: Include detailed per-item coverage in the response body **details** object.
-   false: The response body **details** object will return empty or not at all.

Default: false

Data type: Boolean

</td></tr><tr><td>

sys\_scopes

</td><td>

Filter results to specified application scopes \(e.g., `["x_my_app", "global"]`\). Multiple scopes use OR logic, so any matching scope is included. No filtering occurs if any empty or NULL array is provided.Data type: Array of strings

</td></tr></tbody>
</table>### Headers

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
|400|Bad Request. A bad request type or malformed request was detected.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON\)

<table id="table_10z_n1c_i8e"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

link

</td><td>

Link to the request record.Data type: String

</td></tr><tr><td>

details.&lt;scriptId&gt;

</td><td>

Lists the ATF aggregation coverage percent of each custom test script by script sys\_id.Data type: Number

</td></tr><tr><td>

api\_request\_sys\_id

</td><td>

The sys\_id of the request.Table: ATF code coverage API requests \[sys\_atf\_code\_coverage\_request\]

Data type: String

</td></tr><tr><td>

result

</td><td>

Success or error message.Error response formats:

-   400 Bad Request

`{ "result": "Validation error: <specific_error_message>" }`

-   500 Internal Server Error

`{ "result": "Internal server error: <error_message>" }`


Possible errors:

-   Request body validation - `Request body is required and cannot be empty`
-   Script array validation results if the **script\_array** request entries provided are null, empty, or whitespace - `"script_array is required and cannot be empty - script_array must contain at least one valid script identifier"`
-   Test ID validation - `At least one valid (non-empty) ID must be provided in either test_result_ids or test_suite_result_ids`
-   Type mismatch - `Invalid data type in request parameters`

Data type: String

</td></tr><tr><td>

total

</td><td>

Overall code coverage percentage reflecting the combined ATF code coverage of the scripts listed in the **details** property. The value is zero if no custom scripts are associated with the tests provided or no percentage of code coverage has been provided.Possible values: 0-100

Data type: Number

</td></tr><tr><td>

truncation\_message

</td><td>

If request data was truncated during persistence, provides details about what scripts have truncated information.Example message:

`truncation_message: "Field atf_code_coverage_request.metadata_info truncated from 5000 to 4000 characters (max: 4000). Consider increasing column length to prevent data loss"`

Data type: String

</td></tr><tr><td>

was\_truncated

</td><td>

Flag that indicates whether request data was truncated during persistence. To reduce truncation, you can change the default number of characters supported.For example, `request_data_truncated: true`.

Valid values:

-   true: Request data was truncated during persistence.
-   false: Request data was not truncated during persistence.

Data type: Boolean

Default number of characters: 4000

</td></tr></tbody>
</table>### Additional information

Large request payloads may be truncated when persisted if the request data exceeds database field limits.

The following fields in the ATF code coverage API requests \[sys\_atf\_code\_coverage\_request\] table are subject to truncation:

-   test\_suite\_results - JSON array of test suite result IDs.
-   test\_results - JSON array of test result IDs.
-   metadata\_info - JSON object containing filtered lines or a script array.

If the **was\_truncated** property is true, details are provided in the **truncation\_message** property of the response body. Additionally, the system logs the following message:

`Field <table_name>.<field_name> truncated from <original_length> to <truncated_length> characters (max: <max_field_length>). Consider increasing column length to prevent data loss"`

The **glide.db.truncate\_utf8** system property truncation behavior:

-   If **glide.db.truncate\_utf8** is true, the information truncates at UTF-8 byte boundaries. This setting is safer for multi-byte characters.
-   If **glide.db.truncate\_utf8** is false \(default\), the information truncates at character boundaries. The default boundary is 4000 characters.

### cURL request

The following example shows how to retrieve the code coverage for a selected test result suite filtered by a specific test script. When **verbose** is `false` or omitted, the **details** object is empty. Only the overall **total** percentage is returned.

```
curl "https://instance.service-now.com/api/now/atf/code_coverage/by_script_id" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
  \"test_suite_result_ids\": [\"5f81c7c4ff943210b88affffffffffc5\"],
  \"script_array\": [
    \"sys_script_include_db95cb370a0a0b2b00244880b5cacda7\",
    \"sys_script_include_a1b2c3d4e5f6a7b8c9d0e1f2a3b4c5d6\"
  ]
}" \
--user 'username':'password'
```

Output:

```
{
  "result": "success",
  "total": 78,
  "details": {},
  "api_request_sys_id": "a7b8c9d0e1f2a3b4c5d6e7f8a9b0c1d2",
  "link": "https://instance.service-now.com/sys_atf_code_coverage_request.do?sys_id=a7b8c9d0e1f2a3b4c5d6e7f8a9b0c1d2"
}
```

## ATF Code Coverage - POST /now/atf/code\_coverage/by\_line\_number

Computes code coverage using a set of filtered line numbers per metadata record.

### URL format

Versioned URL: `/api/now/v1/atf/code_coverage/by_line_number`

Default URL: `/api/now/atf/code_coverage/by_line_number`

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

<table id="table_fyr_lf4_k3c" class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

test\_suite\_result\_ids

</td><td>

Required unless `test_result_ids` are provided. List of test suite result sys\_ids.Table: Test Suite Results \[sys\_atf\_test\_suite\_result\]

Data type: Array of strings

</td></tr><tr><td>

test\_result\_ids

</td><td>

Required unless `test_suite_result_ids` are provided. List of test result sys\_ids to include \(can be combined with suites\). Table: Test Results \[sys\_atf\_test\_result\]

Data type: Array of strings

</td></tr><tr id="atfCC-reqParms-filtered_lines"><td>

filtered\_lines

</td><td>

Required. Map of metadata sys\_ids and corresponding code lines to designate for code coverage \(e.g., `{ "<metadata_sys_id>": { "script": [...] } }`\).Data type: Object

</td></tr><tr id="atfCC-reqParms-filtered_linesID"><td>

filtered\_lines.&lt;sys\_id&gt;

</td><td>

Required, must not be empty. One or more script sys\_ids to evaluate for code coverage. Must contain at least one valid \(non-empty\) script identifier. Null, empty, or whitespace-only entries are filtered out.Table: Metadata Tracing \[sys\_traced\_metadata\]

Data type: Object

</td></tr><tr id="atfCC-reqParms-filtered_linesScrpt"><td>

filtered\_lines.&lt;sys\_id&gt;.script

</td><td>

Required. List of line numbers and strings of ranges of lines numbers. All values provided must be positive integers greater than or equal to 1.Valid line number formats:

-   Individual lines: \[1, 7, 10\]
-   Ranges: For example, \["1-7"\] expands to \[1, 2, 3, 4, 5, 6, 7\].
    -   The format is start-end, where the value of start is less than or equal to end.
    -   The maximum range is 10000 lines.
-   Mixed formats. For example, \[1, "3-6", 7\] expands to \[1, 3, 4, 5, 6, 7\].

Example:

```
{
  "filtered_lines": {
    "sys_script_include_db95cb370a0a0b2b00244880b5cacda7": {
      "script": [1, "3-6", 7, "10-12"]
    }
  }
}
```

Data type: Array

</td></tr><tr><td>

verbose

</td><td>

Flag that indicates level of detail to provide in the response for each custom test script.Valid values:

-   true: Include detailed per-item coverage in the response body **details** object.
-   false: The response body **details** object will return empty or not at all.

Default: false

Data type: Boolean

</td></tr><tr><td>

sys\_scopes

</td><td>

Filter results to specified application scopes \(e.g., `["x_my_app", "global"]`\). Multiple scopes use OR logic, so any matching scope is included. No filtering occurs if any empty or NULL array is provided.Data type: Array of strings

</td></tr></tbody>
</table>### Headers

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
|400|Bad Request. A bad request type or malformed request was detected.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON\)

<table id="table_10z_n1c_i8e"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

link

</td><td>

Link to the request record.Data type: String

</td></tr><tr><td>

details.&lt;scriptId&gt;

</td><td>

Lists the ATF aggregation coverage percent of each custom test script by script sys\_id.Data type: Number

</td></tr><tr><td>

api\_request\_sys\_id

</td><td>

The sys\_id of the request.Table: ATF code coverage API requests \[sys\_atf\_code\_coverage\_request\]

Data type: String

</td></tr><tr><td>

result

</td><td>

Success or error message.Error response formats:

-   400 Bad Request

`{ "result": "Validation error: <specific_error_message>" }`

-   500 Internal Server Error

`{ "result": "Internal server error: <error_message>" }`


Possible errors:

-   Filtered lines validation - `"filtered_lines is required and cannot be empty" - "filtered_lines must contain at least one metadata entry with valid line numbers"`
-   Filtered lines structure errors:
    -   `"Invalid line number format in filtered_lines: <details>"`
    -   `"Invalid data type in filtered_lines: Ensure line numbers are integers or valid range strings (e.g., '1-7')"`
    -   `"Null value found in filtered_lines structure. All metadata IDs, field names, and line number lists must be non-null"`
    -   `"Unexpected error processing filtered_lines: <exception_type>: <message>"`
-   Line number format errors:
    -   Generic parsing failure - `"Invalid line number format: <item>"` -
    -   Line number &lt; 1 - `"Line number must be positive: <line_number>"`
    -   Line range selection error, such as "a-b" - `"Invalid range format: <range>. Both start and end must be valid integers"`
    -   Line range selection error, such as "10-5" - `"Invalid range: <range>. Start value (<start>) must be less than or equal to end value (<end>)"`
    -   Line range selection error, such as "-5-10" - `"Invalid range: <range>. Line numbers must be positive (start: <start>)"`
    -   Line range selection error, such as "1-50000" - `"Range too large: <range>. Maximum range size is 10000 lines (requested: <size>)"`
-   Request body validation - `Request body is required and cannot be empty`
-   Test ID validation - `At least one valid (non-empty) ID must be provided in either test_result_ids or test_suite_result_ids`
-   Type mismatch - `Invalid data type in request parameters`

Data type: String

</td></tr><tr><td>

total

</td><td>

Overall code coverage percentage reflecting the combined ATF code coverage of the scripts listed in the **details** property. The value is zero if no custom scripts are associated with the tests provided or no percentage of code coverage has been provided.Possible values: 0-100

Data type: Number

</td></tr><tr><td>

truncation\_message

</td><td>

If request data was truncated during persistence, provides details about what scripts have truncated information.Example message:

`truncation_message: "Field atf_code_coverage_request.metadata_info truncated from 5000 to 4000 characters (max: 4000). Consider increasing column length to prevent data loss"`

Data type: String

</td></tr><tr><td>

was\_truncated

</td><td>

Flag that indicates whether request data was truncated during persistence. To reduce truncation, you can change the default number of characters supported.For example, `request_data_truncated: true`.

Valid values:

-   true: Request data was truncated during persistence.
-   false: Request data was not truncated during persistence.

Data type: Boolean

Default number of characters: 4000

</td></tr></tbody>
</table>### Additional information

Large request payloads may be truncated when persisted if the request data exceeds database field limits.

The following fields in the ATF code coverage API requests \[sys\_atf\_code\_coverage\_request\] table are subject to truncation:

-   test\_suite\_results - JSON array of test suite result IDs.
-   test\_results - JSON array of test result IDs.
-   metadata\_info - JSON object containing filtered lines or a script array.

If the **was\_truncated** property is true, details are provided in the **truncation\_message** property of the response body. Additionally, the system logs the following message:

`Field <table_name>.<field_name> truncated from <original_length> to <truncated_length> characters (max: <max_field_length>). Consider increasing column length to prevent data loss"`

The **glide.db.truncate\_utf8** system property truncation behavior:

-   If **glide.db.truncate\_utf8** is true, the information truncates at UTF-8 byte boundaries. This setting is safer for multi-byte characters.
-   If **glide.db.truncate\_utf8** is false \(default\), the information truncates at character boundaries. The default boundary is 4000 characters.

### cURL request

The following example shows how to retrieve all code coverage for a selected test result suite and test result.

```
curl "https://instance.service-now.com/api/now/atf/code_coverage/by_line_number" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
  \"test_suite_result_ids\": [\"5f81c7c4ff943210b88affffffffffc5\"],
  \"test_result_ids\": [\"bb8daec1ff103210b88affffffffff1c\"],
  \"filtered_lines\": {
    \"sys_script_include_db95cb370a0a0b2b00244880b5cacda7\": {
      \"script\": [1, \"3-6\", 7, \"10-12\"]
    }
  },
  \"verbose\": true,
  \"sys_scopes\": [\"x_my_app\", \"global\"]
}" \
--user 'username':'password'
```

Output:

```
{
  "result": "success",z
  "total": 64,
  "details": {
    "sys_script_include_db95cb370a0a0b2b00244880b5cacda7": 80,
    "sys_ui_script_c3d4e5f6a7b8c9d0e1f2a3b4c5d6e7f8": 50
  },
  "api_request_sys_id": "b8c9d0e1f2a3b4c5d6e7f8a9b0c1d2e3",
  "link": "https://instance.service-now.com/sys_atf_code_coverage_request.do?sys_id=b8c9d0e1f2a3b4c5d6e7f8a9b0c1d2e3",
  "was_truncated": false
}
```

