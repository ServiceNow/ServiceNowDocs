---
title: v\_query – Scoped, Global
description: The v\_query API provides methods to obtain information about a scriptable object that represents a query running against a remote table.Gets an encoded query string for the specified field.Returns the query against a remote table as an encoded query stringGets the value of a field in an equality query condition.Returns the sys\_id value in a get query.Gets a text search query parameter.Determines if the query is a get query, that is, a query that retrieves a record by sys\_id.Indicates if the query contains a text query parameter.Sets the last error message in the GlideRecord.
locale: en-US
release: xanadu
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# v\_query – Scoped, Global

The v\_query API provides methods to obtain information about a scriptable object that represents a query running against a remote table.

This API requires the Remote Tables plugin \(com.glide.script.vtable\) to be activated. For additional information, see [Retrieving external data using remote tables and scripts](https://www.servicenow.com/docs/access?context=remote-tables&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

Remote table rows are created using the [v\_table](../../v_table/concept/v_tableAPI.md#) API.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## v\_query - getCondition\(String field\)

Gets an encoded query string for the specified field.

See also [v\_table](../../v_table/concept/v_tableAPI.md#) API.

|Name|Type|Description|
|----|----|-----------|
|field|String|Name of the field.|

|Type|Description|
|----|-----------|
|String|Returns an [encoded query string](https://www.servicenow.com/docs/access?context=c_EncodedQueryStrings&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US) for the given field.|

The following example shows results for a field with an encoded query of `number=INC0001^active=true`.

```
var result = v_query.getCondition("number");
gs.info(result);
```

Output:

```
number=INC0001
```

## v\_query - getEncodedQuery\(\)

Returns the query against a remote table as an encoded query string

For details, see [Encoded query strings](https://www.servicenow.com/docs/access?context=c_EncodedQueryStrings&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).

See also [v\_table](../../v_table/concept/v_tableAPI.md#) API.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The encoded query as a string.|

The following example is a snippet from [Retrieving specific records from a third-party source](https://www.servicenow.com/docs/access?context=remote-table-script-def-example2&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

```
gs.info(v_query.getEncodedQuery());
```

Output:

```
active=true^priority=1
```

## v\_query - getParameter\(String field\)

Gets the value of a field in an equality query condition.

See also:

-   [Retrieving specific records from a third-party source](https://www.servicenow.com/docs/access?context=remote-table-script-def-example2&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)
-   [v\_table](../../v_table/concept/v_tableAPI.md#) API

|Name|Type|Description|
|----|----|-----------|
|field|String|Name of the field to be queried.|

|Type|Description|
|----|-----------|
|String|Value of the field in the query condition. For example, if `name=John` is the encoded query, then getParameter\("name"\) returns `"John"`.|

The following example shows how to get the value of a caller ID field.

```
v_query.getParameter("caller_id");
```

Output:

```
12345123451234512345123451234501
```

## v\_query - getSysId\(\)

Returns the sys\_id value in a get query.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Sys\_id value in the get query, for example, if `sys_id=123`, this method returns `123`.|

The following example is a snippet from [Retrieving specific records from a third-party source](https://www.servicenow.com/docs/access?context=remote-table-script-def-example2&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

```
v_query.getSysId();
```

Output:

```
a3a7ffb6dba41010db2051735e4619b7
```

## v\_query - getTextSearch\(\)

Gets a text search query parameter.

See also:

-   [Encoded query strings](https://www.servicenow.com/docs/access?context=c_EncodedQueryStrings&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US)
-   [Querying tables in script](https://www.servicenow.com/docs/access?context=c_UsingGlideRecordToQueryTables&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US)
-   [v\_table](../../v_table/concept/v_tableAPI.md#) API

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Text search query parameter, for example `email`.|

In the following example, the method returns true if the query contains a text query parameter, such as `GOTO123TEXTQUERY321=email`.

```
// for query value GOTO123TEXTQUERY321=email
v_query.getTextSearch();
```

Output:

```
email
```

## v\_query - isGet\(\)

Determines if the query is a get query, that is, a query that retrieves a record by sys\_id.

See also:

-   [Retrieving specific records from a third-party source](https://www.servicenow.com/docs/access?context=remote-table-script-def-example2&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)
-   [v\_table](../../v_table/concept/v_tableAPI.md#) API

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_k3v_xm3_nlb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag indicates that query for a specific record has `sys_id=` as the query format. Valid values:

-   true: Query contains equality query condition on the sys\_id field.
-   false: Query does not include equality query condition on the sys\_id field.

</td></tr></tbody>
</table>In the following example, if the encoded query is `sys_id=d1954c744662010bd7e061e67a6776e`, the v\_query.isGet\(\) method returns true. If the encoded query is anything else, such as `Number=INC0000001`, the v\_query.isGet\(\) method returns false.

```
// Virtual table to query
var row = {
 sys_id: "d1954c744662010bd7e061e67a6776e",
 number: "INC0000001",
 short_description: "New laptop request",
 u_balance: 1200.23
};

v_table.addRow(row);

v_query.isGet();
```

## v\_query - isTextSearch\(\)

Indicates if the query contains a text query parameter.

See also:

-   [Encoded query strings](https://www.servicenow.com/docs/access?context=c_EncodedQueryStrings&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US)
-   [Querying tables in script](https://www.servicenow.com/docs/access?context=c_UsingGlideRecordToQueryTables&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US)
-   [v\_table](../../v_table/concept/v_tableAPI.md#) API

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_k3v_xm3_nlb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the query contains a text query parameter.Valid values:

-   true: Query contains a text query parameter.
-   false: Query does not contain a text query parameter.

</td></tr></tbody>
</table>In the following example, the method returns true if the query contains a text query parameter, such as `GOTO123TEXTQUERY321=email`.

```
v_query.isTextSearch();
```

## v\_query - setLastErrorMessage\(String message\)

Sets the last error message in the GlideRecord.

See also:

-   [Scoped GlideRecord - getLastErrorMessage\(\)](../../glideRecordScoped/concept/c_GlideRecordScopedAPI.md#)
-   [Retrieving specific records from a third-party source](https://www.servicenow.com/docs/access?context=remote-table-script-def-example2&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)
-   [v\_table](../../v_table/concept/v_tableAPI.md#) API

|Name|Type|Description|
|----|----|-----------|
|message|String|Error message.|

|Type|Description|
|----|-----------|
|None| |

The following example shows the basic structure used to set an error message.

```
(function executeQuery (v_table, v_query) {
 try {

 // Add code to test for errors during execution
 } catch(ex) {

  v_query.setLastErrorMessage(ex.message);

 }

}) (v_table, v_query);
```

The following example shows how to set the last error message in a REST API.

```
(function executeQuery (v_table, v_query) { 
 try {

 // call a REST API
 } catch(ex) {

  v_query.setLastErrorMessage("Error obtaining results from remote service");

 }

}) (v_table, v_query);
```

