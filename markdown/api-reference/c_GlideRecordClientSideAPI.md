---
title: GlideRecord - Client
description: The GlideRecord API provides methods that perform database operations. This API enables the use of some GlideRecord functionality in client-side scripts, such as client scripts and UI policy scripts.Creates an instance of the GlideRecord class for the specified table.Adds a column to order by in the query.Adds a query to return records where the specified field name is equal to a specified value \(or is in a list of values\).Adds a filter to return records where the field meets the specified condition \(field, operator, value\).Deletes the current record and calls the specified response function when complete.Executes a GlideRecord query for a record with the specified sys\_id. This method is expected to be used to query for single records, so a next operation is performed before returning.Retrieves the query condition of the current result set as an encoded query string.Returns the limit for records to be returned by the GlideRecord query.Retrieves the name of the table associated with this GlideRecord.Determines if there are any more records in the GlideRecord.Inserts a new record using the field values that have been set for the current record.Moves to the next record in the GlideRecord.Specifies an orderBy column. May be called more than once to order by multiple columns.Runs the query to the server against the table based on the addQuery\(\) filter. This method queries the GlideRecord table as well as any references of the table.Adds a specified encoded query string to the current query clause.Sets the limit for how many records are in the GlideRecord.
locale: en-US
release: xanadu
product: API Reference
classification: api-reference
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 10
breadcrumb: [Client API reference, API reference, API implementation and reference]
---

# GlideRecord- Client

The GlideRecord API provides methods that perform database operations. This API enables the use of some GlideRecord functionality in client-side scripts, such as client scripts and UI policy scripts.

A GlideRecord contains both records and fields. Queries made with client-side GlideRecord methods are executed on the server. Therefore, a request is made from the client browser to obtain the record data.

The client-side GlideRecord API is not supported in scoped applications. Instead, create a script include and use the [GlideAJAX](../../GlideAjax/concept/c_GlideAjaxAPI.md#) API, or use the REST APIs. In addition, this API applies access control lists \(ACLs\) based on the credentials of the user executing the script. To execute the code on the server without ACLs, use the [GlideAjax](../../GlideAjax/concept/c_GlideAjaxAPI.md#) API.

**Parent Topic:**[Client API reference](../../../../../build/applications/concept/api-client.md)

## Client side GlideRecord - GlideRecord\(String tableName\)

Creates an instance of the GlideRecord class for the specified table.

|Name|Type|Description|
|----|----|-----------|
|tableName|String|The table to be used.|

```
var now_GR = new GlideRecord('incident');
```

## Client side GlideRecord - addOrderBy\(String column\)

Adds a column to order by in the query.

|Name|Type|Description|
|----|----|-----------|
|column|String|The column by which to order the result set.|

|Type|Description|
|----|-----------|
|void| |

## Client side GlideRecord - addQuery\(String name, Object value\)

Adds a query to return records where the specified field name is equal to a specified value \(or is in a list of values\).

If you are familiar with SQL, this method is similar to the "where" clause. You can create one or more queries for a single filter by calling this method multiple times; for this method the queries are AND'ed. Once you define all of the desired queries, call the [Client side GlideRecord - query\(String name, Function responseFunction, String value\)](c_GlideRecordClientSideAPI.md#) to execute the specified query clause \(filter\).

To perform an operation other than AND, use either the [addQuery\(String name, Object operator, Object value\)](c_GlideRecordClientSideAPI.md#) method or the [setEncodedQuery\(\)](c_GlideRecordClientSideAPI.md#) method.

|Name|Type|Description|
|----|----|-----------|
|name|String|Name of the field to check.|
|value|Object|The value or list of values on which to query.|

|Type|Description|
|----|-----------|
|void| |

Example showing multiple queries.

```
var now_GR = new GlideRecord('incident');
now_GR.addQuery('priority', 4); // Priority is 4 – Low and,
now_GR.addQuery('state', 3); // State is On Hold
now_GR.query(response);
 
function response(result) {
    while(result.next()) {
       // Print all INC with priority 4 – Low AND state is On Hold
        console.log(result.getValue('number')); 
    }
}
```

Example showing how to pass a string object.

```
var now_GR = new GlideRecord('incident');
now_GR.addQuery('short_description', new String('USB device not working')); // string object
now_GR.addQuery('priority', 4); //number
now_GR.query(response);
 
function response(result) {
    while(result.next()) {
       // Print all INC with priority 4 – Low AND short description contains 'USB device not working'
        console.log(result.getValue('number')); 
    }
}
```

## Client side GlideRecord - addQuery\(String name, Object operator, Object value\)

Adds a filter to return records where the field meets the specified condition \(field, operator, value\).

If you are familiar with SQL, this method is similar to the "where" clause. You can create one or more queries for a single filter by calling this method multiple times. Once you define all of the desired queries, call the [Client side GlideRecord - query\(String name, Function responseFunction, String value\)](c_GlideRecordClientSideAPI.md#) to execute the specified query clause \(filter\).

To create more complex queries, use the [setEncodedQuery\(\)](c_GlideRecordClientSideAPI.md#) method.

<table id="table_wgh_cpv_hv" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

name

</td><td>

String

</td><td>

Name of the field to check.

</td></tr><tr><td>

operator

</td><td>

Object

</td><td>

Query operator. The available values are dependent on the data type of the *value* parameter.Numbers:

-   =
-   !=
-   &gt;
-   &gt;=
-   &lt;
-   &lt;=

 Strings \(must be in upper case\):

-   =
-   !=
-   IN
-   NOT IN
-   STARTSWITH
-   ENDSWITH
-   CONTAINS
-   DOES NOT CONTAIN
-   INSTANCEOF

**Note:** Don't use the LIKE operator. Use CONTAINS instead.

</td></tr><tr><td>

value

</td><td>

Object

</td><td>

Value on which to query \(not case-sensitive\).

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

Example showing how to add multiple queries to a filter.

```
var now_GR = new GlideRecord('incident');
now_GR.addQuery('priority', '<=', 2); // Priority is 2 or higher and,
now_GR.addQuery('short_description', 'CONTAINS', 'crash'); // Short description contains the word crash
now_GR.query(response);
 
function response(result) {
    while(result.next()) {
       // Print all INC with priority of 2 or higher AND short description contains "crash"
        console.log(result.getValue('number')); 
    }
}
```

Example showing how to pass in an array to verify multiple conditions in a single query.

```
var priorities = [4,2]; 
var now_GR = new GlideRecord('incident'); 
now_GR.addQuery('priority', 'IN', priorities); 
now_GR.query(response); 

function response(result) {
  while(result.next()) {
    console.log(result.getValue('number')); 
  } 
}
```

## Client side GlideRecord - deleteRecord\(Function responseFunction\)

Deletes the current record and calls the specified response function when complete.

|Name|Type|Description|
|----|----|-----------|
|responseFunction|Function|Response function for the callback.|

|Type|Description|
|----|-----------|
|None| |

This example deletes a record and then calls the response function *response* to log an alert message.

```
var recordGR = new GlideRecord('incident');
if (recordGR.get('99ebb4156fa831005be8883e6b3ee4b9')) {
  recordGR.deleteRecord(response);
}

function response(result) {
  alert('Deleted record sys_id: ' + result.getValue('sys_id'));
}
```

Output:

```
Deleted record sys_id: 99ebb4156fa831005be8883e6b3ee4b9
```

## Client side GlideRecord - get\(String sys\_id\)

Executes a GlideRecord query for a record with the specified sys\_id. This method is expected to be used to query for single records, so a next operation is performed before returning.

|Name|Type|Description|
|----|----|-----------|
|sys\_id|String|The sys\_id of the record to be found.|

|Type|Description|
|----|-----------|
|Boolean|True if one or more matching records was found. False if no records were found.|

## Client side GlideRecord - getEncodedQuery\(\)

Retrieves the query condition of the current result set as an encoded query string.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|An encoded query string containing all conditions that have been added to the query.|

## Client side GlideRecord - getLimit\(\)

Returns the limit for records to be returned by the GlideRecord query.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Number|The limit for records to be returned by the GlideRecord query.|

## Client side GlideRecord - getTableName\(\)

Retrieves the name of the table associated with this GlideRecord.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The table name|

```
var item = new GlideRecord('sc_request'); 
item.addQuery('sys_id', current.request); 
item.query(itemResponse); 
 
function itemResponse(item) {
   alert('The table is ' + item.getTableName());
}
```

## Client side GlideRecord - hasNext\(\)

Determines if there are any more records in the GlideRecord.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Boolean|True if there are more records in the query set.|

## Client side GlideRecord - insert\(Function responseFunction\)

Inserts a new record using the field values that have been set for the current record.

|Name|Type|Description|
|----|----|-----------|
|responseFunction|Function|Function to execute once the record is inserted.|

|Type|Description|
|----|-----------|
|String|Sys\_id of the inserted record, or null if the record was not inserted.|

```
var now_GR = new GlideRecord('incident');
now_GR.short_description = 'Learn about GlideRecord';
var recResponse = now_GR.insert(handleResponse);

function handleResponse(recResponse, answer) {
// Answer will be the sys_id of the created record or null
alert('Newly created sys_id is - ' + answer + ' exists');
}
```

## Client side GlideRecord - next\(\)

Moves to the next record in the GlideRecord.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Boolean|False if there are no more records in the query set.|

```
var rec = new GlideRecord('incident');
rec.query(recResponse);
 
function recResponse(rec) {
  while (rec.next()) { 
    alert(rec.number + ' exists');
  }
}
```

## Client side GlideRecord - orderBy\(String column\)

Specifies an orderBy column. May be called more than once to order by multiple columns.

|Name|Type|Description|
|----|----|-----------|
|column|String|The column name to be used to order the result set.|

|Type|Description|
|----|-----------|
|void| |

```
function UpdateProjectWBS(project) {
  var count = 0;
  var child = new GlideRecord('pm_project_task');
  child.addQuery('parent', project.sys_id);
  child.orderBy('order');
  child.orderBy('number');
  child.query(childResponse);
  g_form.addInfoMessage(count + ' Project Tasks updated');
}
 
function childResponse(child) {
  var len = child.getRowCount().toString().length;
  var seq = 0;
  while (child.next()) {
    count += UpdateProjectTaskWBS(child, 1, ++seq, len, '');
  }
}
```

## Client side GlideRecord - query\(String name, Function responseFunction, String value\)

Runs the query to the server against the table based on the addQuery\(\) filter. This method queries the GlideRecord table as well as any references of the table.

Do not make synchronous query calls. Performing a query without a response function makes the call synchronous, which means that the display will wait for the query response before continuing.

|Name|Type|Description|
|----|----|-----------|
|name|String|Optional. The name of a field to query.|
|responseFunction|Function|The function called when the query results are available.|
|value|String|Optional. The field value to query for. Any pair of literals is considered a query pair \(field : value\).|

|Type|Description|
|----|-----------|
|void| |

The following is a basic example with a response function.

```
var rec = new GlideRecord('incident');
rec.query(recResponse);
 
function recResponse(rec) {
  while (rec.next()) { 
   alert(rec.number + ' exists');
  } 
}
```

The following example shows the difference between synchronus and asynchronous syntax, with an asynchronous example.

```
// synchronous call syntax (no response function): DO NOT USE
        query();
        
        // asynchronous call syntax
        // performs query with current conditions, calls responseFunction when done
        query(responseFunction)
        
        // synchronous call syntax (no response function): DO NOT USE
        // adds "category=hardware" to current query conditions and performs query
        query('category', 'hardware')
        
        // asynchronous call syntax
        // adds "category=hardware" to current query conditions, performs query, and calls responseFunction when done
        query('category', 'hardware', responseFunction)
        
        // asynchronous call example
        // adds "user_name=abel.tuter" to current query conditions, performs query, and calls defined response function when done
        function onLoad() {
        var now_GR = new GlideRecord("sys_user");
        now_GR.query("user_name", "abel.tuter", function(now_GR) {
        if (now_GR.next()) {
        alert("You can access fields by name from the client API, just like in the server API:\n now_GR.name = " + now_GR.name);
        alert("You can also access fields using getValue():\n now_GR.getValue(\"email\") = " + now_GR.getValue("email"));
        if (now_GR.getDisplayValue) {
        alert("In Service Portal, Mobile, and Agent Workspace, you can access a field's display value:\n now_GR.getDisplayValue(\"company\") = " + now_GR.getDisplayValue("company"));
        } else {
        alert("On the desktop, you cannot access a field's display value, but can get its sys_id:\n now_GR.company = " + now_GR.company);
        }
        alert("You cannot dot-walk in the client API:\n now_GR.company.name = " + now_GR.company.name);
        }
        });
        }
```

## Client side GlideRecord - setEncodedQuery\(String encodedQuery\)

Adds a specified encoded query string to the current query clause.

This method enables you to specify complex filters \(encoded query strings\) in a single query call, unlike other client-side addQuery\(\) methods. Once you define all of the desired queries, call the [Client side GlideRecord - query\(String name, Function responseFunction, String value\)](c_GlideRecordClientSideAPI.md#) to execute the specified query clause \(filter\). For additional information on encoded query strings, refer to [Encoded query strings](https://www.servicenow.com/docs/access?context=c_EncodedQueryStrings&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).

If you call this method multiple times before calling the query\(\) method, the queries are AND'ed together.

|Name|Type|Description|
|----|----|-----------|
|encodedQuery|String|Encoded query string to add to the current query clause.|

|Type|Description|
|----|-----------|
|void| |

```
var now_GR = new GlideRecord('incident');
now_GR.setEncodedQuery('priority=4^ORstate=3');
now_GR.query(response);
 
function response(result) {
    while(result.next()) {
        console.log(result.getValue('number'));
    }
}

```

## Client side GlideRecord - setLimit\(Number maxQuery\)

Sets the limit for how many records are in the GlideRecord.

|Name|Type|Description|
|----|----|-----------|
|maxQuery|Number|The limit for the number of records to retrieve.|

|Type|Description|
|----|-----------|
|void| |

