---
title: Response Templates API
description: The Response Templates API provides endpoints to handle records in the Response Templates \[sn\_templated\_snip\_note\_template\] table.Returns records from the Response Templates \[sn\_templated\_snip\_note\_template\] table.
locale: en-US
release: zurich
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# Response Templates API

The Response Templates API provides endpoints to handle records in the Response Templates \[sn\_templated\_snip\_note\_template\] table.

This script include requires the Templated Responses plugin \(com.sn\_templated\_snip\), which is activated by default, and runs within the `sn_templated_snip` namespace.

For additional information on response templates, see [Response templates](https://www.servicenow.com/docs/access?context=response-templates-templated-snippets&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## Response Templates - POST /response\_templates/get\_templates

Returns records from the Response Templates \[sn\_templated\_snip\_note\_template\] table.

### URL format

Default URL: `/api/sn_templated_snip/response_templates/get_templates`

### Supported request parameters

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

errorFormat

</td><td>

HTML formatting to use for errors. Data type: String

 Default: `"<span style='color:#ff0000'>${%s}</span>"`

</td></tr><tr><td>

includeEvaluatedBody

</td><td>

Flag that indicates whether to render the template variables.Valid values:

 -   false: Do not render the template variables. The response contains the message variables.

For example:

    ```
Please note that your case ${number} has been escalated to ${assignment_group}.
    ```

-   true: Renders the template variables and returns **evaluated\_response** in the return results.

For example:

    ```
Please note that your case INC100001 has been escalated to Facilities.
    ```


 Data type: Boolean

 Default: false

</td></tr><tr><td>

limit

</td><td>

Maximum number of response templates to return.Data type: Number

 Default: 50

</td></tr><tr><td>

offset

</td><td>

For pagination, the index at which to start the search.Data type: Number

 Default: 0

</td></tr><tr><td>

opts

</td><td>

Parameters to pass to the sn\_templated\_snip.response\_template extension point. The format and content of these parameters are dependent on the implementation of the extension point. For additional information on extension points, see [Using extension points to extend application functionality](../../../build/applications/concept/extension-points.md).Data type: Object

</td></tr><tr><td>

recordId

</td><td>

Required. Sys\_id of the record to use to render the variables in the response template.Data type: String

</td></tr><tr><td>

searchTerm

</td><td>

Text to use to filter the list of matching response templates.The endpoint performs a CONTAINS search of this text on the name and body fields and a STARTS WITH search on the short name field. For example, if the search term is "crash", the endpoint returns any response template that matches the query criteria and has crash in the name or body or the short name starts with crash.

 Response templates with exact matches on short name appear first in the return results. All other returned response templates are sorted by name.

 Data type: String

 Default: Return all matching response templates.

</td></tr><tr><td>

tableName

</td><td>

Required. Name of the table to use to search the Response Templates table to locate corresponding response templates. For example, "incident" or "sn\_hr\_core\_case".Data type: String

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
|200|Successful. The request was successfully processed.|
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

Array of objects that list all of the templates that match the specified search criteria.

 Data type: Array

 ```
"result": [
  {Object}
]
```

</td></tr><tr><td>

result.&lt;object&gt;

</td><td>

Response templates with exact matches on short name appear first in the return results. All other returned response templates are sorted by name.

 Data type: Object

 ```
{
  "evaluated_response": [Array],
  "name": "String",
  "short_name": "String",
  "short_name_match": Boolean,
  "sys_id": "String",
  "template_body": "String"
}
```

</td></tr><tr><td>

result.&lt;object&gt;.evaluated\_response

</td><td>

Array that lists the results of the template evaluation.

 Data type: Array

 ```
"elevated_response":[
  "error": [Array],
  "evaluated_body": "String",
  "success": Boolean
]
```

</td></tr><tr><td>

result.&lt;object&gt;.evaluated\_response.error

</td><td>

List of entries for each evaluation error that occurred.

 Data type: Array

 ```
"error":[
  "inAccessibleVariables": "String",
  "message": "String",
  "unEvaluatedVariables": "String"
]
```

</td></tr><tr><td>

result.&lt;object&gt;.evaluated\_response.error.inAccessibleVariables

</td><td>

Variables in the response template body that could not be resolved.Data type: String

</td></tr><tr><td>

result.&lt;object&gt;.evaluated\_response.error.message

</td><td>

Error message.Data type: String

</td></tr><tr><td>

result.&lt;object&gt;.evaluated\_response.error.unEvaluatedVariables

</td><td>

Variables in the response template body that were not evaluated.Data type: String

</td></tr><tr><td>

result.&lt;object&gt;.evaluated\_response.evaluated\_body

</td><td>

Evaluated response template body in HTML.Data type: String

</td></tr><tr><td>

result.&lt;object&gt;.evaluated\_response.success

</td><td>

Flag that indicates whether all of the variables rendered properly.

 Possible values:

-   true: All variables rendered properly.
-   false: Variables did not render properly.

 Data type: Boolean

</td></tr><tr><td>

result.&lt;object&gt;.name

</td><td>

Name of the response template.Data type: String

</td></tr><tr><td>

result.&lt;object&gt;.short\_name

</td><td>

Short name of the response template.Data type: String

</td></tr><tr><td>

result.&lt;object&gt;.short\_name\_match

</td><td>

Flag that indicates whether an exact match occurred on the short name of the response template.

 Possible values:

-   true: Search term is an exact match.
-   false: Search term is not an exact match.

 Data type: Boolean

</td></tr><tr><td>

result.&lt;object&gt;.sys\_id

</td><td>

Sys\_id of the response template.Data type: String

</td></tr><tr><td>

result.&lt;object&gt;.template\_body

</td><td>

Response template body in HTML.Data type: String

</td></tr></tbody>
</table>### Sample cURL request

```
curl "https://instance.service-now.com/api/sn_templated_snip/response_templates/get_templates" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
  \"tableName\": \"sn_hr_core_case_total_rewards\",
  \"recordId\": \"2c9e43320b30220097432da0d5673a9c\"
}" \
--user "username":"password"
```

```
{
   "result": [
      {
         "sys_id": "2552c4ec0b03320036e62c7885673a5a",
         "name": "Escalation Notes - Total Rewards",
         "short_name": "Escalation Notes - Total Rewards",
         "template_body": "<p>Dear ${subject_person},<\/p>\n<p>Please note that your case ${number} has been escalated to ${assignment_group}. An agent will be assigned on your case and will keep you updated. If you have more questions please reach out to our team.<\/p>\n<p>Regards,<\/p>\n<p>${sys_updated_by}<\/p>"
      },
      {
         "sys_id": "698388ec0b03320036e62c7885673ab5",
         "name": "Resolution Notes - Phone Inquiry",
         "short_name": "Resolution Notes - Phone Inquiry",
         "template_body": "<p>Thank you ${subject_person} for reaching out to the Global HR Services Team for your inquiry. As discussed over the phone, we have resolved your case ${number}.<\/p>\n<p>We are happy to help if you have more questions for our team. Please reach out and mention the case number ${number} on the call.<\/p>\n<p>Regards,<\/p>\n<p>${assigned_to}<\/p>"
      }
   ]
}
```

