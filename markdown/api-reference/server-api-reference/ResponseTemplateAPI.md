---
title: ResponseTemplate - Scoped, Global
description: The ResponseTemplate script include provides methods for managing response templates.Instantiates a new ResponseTemplate object.Returns all response templates from a specified table that match the passed in query criteria.Renders the HTML body of a specified response template.
locale: en-US
release: xanadu
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 6
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# ResponseTemplate - Scoped, Global

The ResponseTemplate script include provides methods for managing response templates.

Response templates are reusable messages that agents can copy to case or task forms. They provide quick and consistent messages to users and display standard chat response messages to requesters in Agent Chat. This script include requires the Templated Responses plugin \(com.sn\_templated\_snip\), which is activated by default, and runs within the `sn_templated_snip` namespace.

For additional information on response templates, see [Response templates](https://www.servicenow.com/docs/access?context=response-templates-templated-snippets&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## ResponseTemplate - ResponseTemplate\(\)

Instantiates a new ResponseTemplate object.

|Name|Type|Description|
|----|----|-----------|
|None| | |

```
new sn_templated_snip.ResponseTemplate().query("incident","ef4225a40a0a0b5700d0b8a790747812", "", 0, 0, true, ""); 
```

## ResponseTemplate - query\(String tableName, String recordId, String searchTerm, Number limit, Number offset, Boolean includeEvaluatedBody, String errorFormat, Object opts\)

Returns all response templates from a specified table that match the passed in query criteria.

<table id="table_bq2_kgr_vhb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

tableName

</td><td>

String

</td><td>

Name of the table to use to search the sn\_templated\_snip\_note\_template table to locate corresponding response templates. For example, incident or sn\_hr\_core\_case.

</td></tr><tr><td>

recordId

</td><td>

String

</td><td>

Sys ID of the record to use to render the variables in the response template.

</td></tr><tr><td>

searchTerm

</td><td>

String

</td><td>

Optional. Text to use to filter the list of matching response templates. The method performs a CONTAINS search of this text on the name and body fields and a STARTS WITH search on the short name field. For example, if the search term is "crash", the method returns any response template that matches the query criteria and has crash in the name or body or the short name starts with crash.

 Response templates with exact matches on short name appear first in the return results. All other returned response templates are sorted by name.

 Default: Return all matching response templates.

</td></tr><tr><td>

limit

</td><td>

Number

</td><td>

Optional. Maximum number of response templates to return.Default: 50

</td></tr><tr><td>

offset

</td><td>

Number

</td><td>

Optional. For pagination, the index at which to start the search.Default: 0

</td></tr><tr><td>

includeEvaluatedBody

</td><td>

Boolean

</td><td>

Optional. Flag that indicates whether to render the template variables.Valid values:

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


 Default: false

</td></tr><tr><td>

errorFormat

</td><td>

String

</td><td>

Optional. HTML formatting to use for errors. For example:

 `"<span style='color:#ffff00'>${%s}</span>"`

 Default: `"<span style='color:#ff0000'>${%s}</span>"`

</td></tr><tr><td>

opts

</td><td>

Object

</td><td>

Optional. Parameters to pass to the sn\_templated\_snip.response\_template extension point. The format and content of these parameters are dependent on the implementation of the extension point. For additional information on extension points, see [Using extension points to extend application functionality](../../../../../build/applications/concept/extension-points.md).

</td></tr></tbody>
</table><table id="table_cq2_kgr_vhb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Array of all templates that match the specified search criteria. Response templates with exact matches on short name appear first in the return results. All other returned response templates are sorted by name.Each node in the Array may contain the following parameters:

 -   **sys\_id**: String. Unique identifier of the response template.
-   **name**: String. Name of the response template.
-   **short\_name**: String. Short name of the response template.
-   **body**: HTML. Body of the response template.
-   **short\_name\_match**: Boolean. Flag that indicates whether an exact match occurred on the short name of the response template.
-   **evaluated\_response**: Array. Results of the template evaluation.
    -   **success**: Boolean. Flag that indicates whether all variables rendered properly.
    -   **evaluated\_body**: HTML. Rendered response template body.
    -   **error**: Array. Entry for each evaluation error that occurred.
        -   **inAccessibleVariables**: String. Variables in the response template body that could not be resolved.
        -   **unEvaluatedVariables**: String. Variablesin the response template body that were not evaluated.
        -   **message**: String. Error message.

</td></tr></tbody>
</table>This example shows how to query for response templates associated with the incident table.

```
query("incident","ef4225a40a0a0b5700d0b8a790747812", "", 0, 0, false, "");
```

Successful response:

```
[
  {
    "sys_id": "5fc1d65993003300a9bc1d1e867ffb9c",
    "name": "Incident escalation",
    "short_name": "escalation",
    "template_body": "<p>Dear ${caller_id.first_name},</p>\r\n<p>Please note that your incident ${number} has been escalated to ${assignment_group}. An agent will be assigned on your case and will keep you updated. If you have more questions please reach out to our team.</p>\r\n<p>Regards,</p>\r\n<p>${sys_updated_by}</p>"
  }
]

```

Same query with an error response.

```
query("incident","fe4225a40a0a0b5700d0b8a790747812", "", 0, 0, false, "");
```

Error response:

```
[
  {
    "sys_id": "5fc1d65993003300a9bc1d1e867ffb9c",
    "name": "Incident escalation",
    "short_name": "escalation",
    "template_body": "<p>Dear ${caller.first_name},</p>\r\n<p>Please note that your incident ${number} has been escalated to ${assignment_group}. An agent will be assigned on your case and will keep you updated. If you have more questions please reach out to our team.</p>\r\n<p>Regards,</p>\r\n<p>${sys_updated_by}</p>",
    "evaluated_response": {
      "success": false,
      "error": {
        "unEvaluatedVariables": "caller.first_name",
        "message": "Cannot evaluate following variables: caller.first_name"
      },
      "evaluated_body": "<p>Dear <span style='color:#ff0000'>${caller.first_name}</span>,</p>\r\n<p>Please note that your incident INC0000049 has been escalated to Hardware. An agent will be assigned on your case and will keep you updated. If you have more questions please reach out to our team.</p>\r\n<p>Regards,</p>\r\n<p>admin</p>"
    }
  }
]

```

## ResponseTemplate - render\(String templateId, String tableName, String recordId, String errorFormat, Object opts\)

Renders the HTML body of a specified response template.

During rendering, all variables are resolved using the information from the specified table and record. If variables cannot be resolved, or any other problem occurs during rendering, the method returns an error message in the results.

<table id="table_uwn_2fr_vhb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

templateId

</td><td>

String

</td><td>

Sys ID of the response template to render.

</td></tr><tr><td>

tableName

</td><td>

String

</td><td>

Name of the table to use when rendering the variables on the response template.

</td></tr><tr><td>

recordId

</td><td>

String

</td><td>

Sys ID of the record to use when rendering the variables on the response template. This record must be in the table specified by **tableName**.

</td></tr><tr><td>

errorFormat

</td><td>

String

</td><td>

Optional. HTML formatting to use for errors. For example:

 `"<span style='color:#ffff00'>${%s}</span>"`

 Default: `"<span style='color:#ff0000'>${%s}</span>"`

</td></tr><tr><td>

opts

</td><td>

Object

</td><td>

Optional. Parameters to pass to the sn\_templated\_snip.response\_template extension point. The format and content of these parameters are dependent on the implementation of the extension point. For additional information on extension points, see [Using extension points to extend application functionality](../../../../../build/applications/concept/extension-points.md).

</td></tr></tbody>
</table><table id="table_vwn_2fr_vhb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Results of the render.-   **success**: Flag that indicates whether the render was successful.
-   **evaluated\_body**: String. For success, rendered response template body. For error, response template body which includes both rendered and non-renderable variables.
-   **error**: Object. Error message if render was unsuccessful.
    -   **unEvaluatedVariables**: Variables that could not be rendered.
    -   **message**: Error message.

</td></tr></tbody>
</table>This code example shows how to request a rendered response template for the incident table.

```
render("5fc1d65993003300a9bc1d1e867ffb9c","incident","ef4225a40a0a0b5700d0b8a790747812", "")
```

Successful response:

```
{
  "success": true,
  "evaluated_body": "<p>Dear Beth,</p>\r\n<p>Please note that your incident INC0000049 has been escalated to Hardware. An agent will be assigned on your case and will keep you updated. If you have more questions please reach out to our team.</p>\r\n<p>Regards,</p>\r\n<p>admin</p>"
}

```

Same render request but returning an error response.

```
render("5fc1d65993003300a9bc1d1e867ffb9c","incident","ef4225a40a0a0b5700d0b8a790747812", "")
```

Error response:

```
{
  "success": false,
  "error": {
    "unEvaluatedVariables": "caller.first_name",
    "message": "Cannot evaluate following variables: caller.first_name"
  },
  "evaluated_body": "<p>Dear <span style='color:#ff0000'>${caller.first_name}</span>,</p>\r\n<p>Please note that your incident INC0000049 has been escalated to Hardware. An agent will be assigned on your case and will keep you updated. If you have more questions please reach out to our team.</p>\r\n<p>Regards,</p>\r\n<p>admin</p>"
}

```

