---
title: v\_table – Scoped, Global
description: The v\_table API provides methods to add rows to a remote table through a scriptable object.Adds rows to the remote table.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# v\_table – Scoped, Global

The v\_table API provides methods to add rows to a remote table through a scriptable object.

This API requires the Remote Tables plugin \(com.glide.script.vtable\) to be activated. For additional information, see [Retrieving external data using remote tables and scripts](https://www.servicenow.com/docs/access?context=remote-tables&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

Use the [v\_query](../../v_query/concept/v_queryAPI.md#) scriptable object to query remote tables.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## v\_table - addRow\(Object row\)

Adds rows to the remote table.

See also:

-   [Create a script definition for a remote table](https://www.servicenow.com/docs/access?context=create-remote-table-script&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US)
-   [Lookup remote information in the system of record](https://www.servicenow.com/docs/access?context=fso-int_guide-agt_table_lookup&version=australia&pubname=australia-financial-services-operations&ft:locale=en-US)
-   [Retrieving specific records from a third-party source](https://www.servicenow.com/docs/access?context=remote-table-script-def-example2&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US)
-   [v\_query API](../../v_query/concept/v_queryAPI.md#)

<table id="table_udd_bdj_nlb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

row

</td><td>

Object

</td><td>

JavaScript object containing field name and value map in which the key is the field name, for example, `{number: "INC0001", sys_id: "a34"}`.```
{ "<field name>": "value" }

```

</td></tr><tr><td>

row.&lt;field value&gt;

</td><td>

String

</td><td>

Represents the value of the selected field. Although no fields are mandatory, provide the sys\_id at a minimum.Example listing only sys\_id field and value:

 ```
{ "sys_id": "<uniqueID>" }

```

</td></tr></tbody>
</table><table id="table_vdd_bdj_nlb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the row was added to the remote table.Valid values:

-   true: Success.
-   false: Row was not added.

</td></tr></tbody>
</table>The following example shows how to use the [RESTMessageV2](../../RESTMessageV2/concept/c_RESTMessageV2API.md#) API to create and execute the REST call to an external bank application. The script shows how to use the addRow\(\) method to store return results in a remote table.

```
(function executeQuery (v_table, v_query) {
  // Parameters needed in the request body of the REST endpoint
  var requestBody = {
    'financial_account':v_query.getParameter('financial_account')
  };

  // Instantiate the RESTMessageV2 object
  var request = new sn_ws.RESTMessageV2();
  // Set the HTTP method as "GET"
  request.setHttpMethod('get');
  // URL of the endpoint on the bank application
  request.setEndpoint('https://<yourbankapphost>/api/getTransactionDetails');
  // Request body as a string
  request.setRequestBody(JSON.stringify(requestBody));
  // Call the REST endpoint
  var response = request.execute();
  // Get the response body
  var responseBody = response.getBody();
  // Parse the response body into an object
  var responseObj = JSON.parse(responseBody);

  // Store the response body into a virtual table
  v_table.addRow({
    sys_id: gs.generateGUID(),
    amount: responseObj.amount,
    description: responseObj.description,
    posting_date: responseObj.posting_date,
    transaction_date: responseObj.transaction_date
  });

}) (v_table, v_query);
```

