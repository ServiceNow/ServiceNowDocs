---
title: GlideQuery - Scoped, Global
description: The GlideQuery script include is an alternative to the GlideRecord API for performing CRUD operations on record data from server-side scripts.Instantiates a GlideQuery object used to build and execute record queries.Aggregates a field using a specified aggregation function.Returns the aggregate average of a given numeric field.Returns the number of records that match the query.Deletes all records in the table specified by the preceding Where clauses.Disables updating system fields, or fields with a name that starts with the sys prefix, such as sys\_created\_on, sys\_updated\_on, and sys\_mod\_count. Only applies to the specified query.Disables any business rules, flows, workflows, or audit records that would run or be created as the result of the query.Forces a database update even when no record changes are made. For example, you can use this method to force a business rule to execute.Returns a single record from the query.Returns an Optional object containing a single record based on a set of name-value pairs to query by. Assumes the '=' operator for each name-value pair.Groups the query results by a designated field or fields.Filters aggregate groups so that you can display only groups of results that match a specified condition.Inserts a record and returns an Optional object containing the record.Updates an existing record, or inserts a new record if one does not already exist.Limits the number of records returned in a query.Returns the aggregate maximum of a given field.Returns the aggregate minimum of a given field.Orders the returned result in ascending order by a given field.Orders the returned result in descending order by a given field.Adds an OR clause to a query that returns values based on a given condition.Adds an OR clause that returns records that do not contain a null value in a given field.Adds an OR clause to a query that returns records that contain a null value in a given field.Adds an encoded query to a new GlideQuery query.Returns the results of the query as a Stream object containing the specified fields.Returns the result of the query as an Optional object containing specified fields.Returns the aggregate sum of a given numeric field.Returns a GlideRecord object that represents the current query. Returns a GlideAggregrate object if the query uses the GlideQuery.aggregate\(\) method.Updates an existing record that matches the defined conditions.Updates all existing records that match the defined conditions. Returns the number of records updated.Adds a Where clause to the query that returns values based on a given condition.Returns records that do not contain a null value in a given field.Returns records that contain a null value in a given field.Executes the query using the GlideRecordSecure API to securely query the database while honoring ACLs.
locale: en-US
release: xanadu
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 30
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# GlideQuery - Scoped, Global

The GlideQuery script include is an alternative to the GlideRecord API for performing CRUD operations on record data from server-side scripts.

The GlideQuery script include lets you:

-   Use standard JavaScript objects and types for queries and results.
-   Quickly diagnose query errors with additional checks and clear error messages.
-   Simplify your code by avoiding boiler-plate query patterns.
-   Avoid common performance issues without needing deeper knowledge of the GlideRecord.

Use the GlideQuery script include in scoped or global server-side scripts. When used within a scoped app, it must be prefixed with the global scope.

```
new global.GlideQuery('sys_user')
// ...
```

This script include requires the GlideQuery \[com.sn\_glidequery\] plugin.

## Implementation

This script include works together with the [Stream](../../Stream/concept/StreamGlobalAPI.md#) and [Optional](../../Optional/concept/OptionalGlobalAPI.md#) APIs in a builder pattern where the method calls chain together, each method building on the returned result of the previous method. Use methods to define the attributes of the query. The methods do not execute until you call a terminal method, a method that returns a query result, allowing you to define the requirements of the query before executing it.

If the query returns a single record, the system wraps the result in an Optional object. If the query returns a stream of records, the system wraps the result in a Stream object. These objects let you manage the result using a set of methods in each API.

For example, this script performs a query on the Task table, groups the records by priority, and returns each priority that has total reassignments greater than four.

```
var query = new global.GlideQuery('task')
    .where('active', true) //Returns new GlideQuery object with a "where" clause.
    .groupBy('priority') //Returns new GlideQuery object with a "group by" clause.
    .aggregate('sum', 'reassignment_count') //Returns new GlideQuery object with a "sum(reassignment_count)" clause.
    .having('sum', 'reassignment_count', '>', 4) //Returns new GlideQuery object with a "having reassignment_count > 4" clause.
    .select() //Returns a stream of records wrapped in a Stream object.  
    .forEach(function (priority){ //Terminal method in the Stream class that executes the query and returns the result. 
      gs.info("Priority " + priority.group.priority + ": " + priority.sum.reassignment_count + " reassignments");
    });
```

Output:

```
Priority 1: 11 reassignments
Priority 3: 6 reassignments
Priority 5: 5 reassignments
```

## Error handling

The GlideQuery script include throws an error when your query has a problem and includes a clear explanation to help guide you. This script include checks for:

-   Invalid fields
-   Invalid value types for a field
-   Invalid values for choice fields
-   Invalid query operators

For example, the following code sample would throw an error because the queried field does not exist in the table.

```
new global.GlideQuery('task')
    .where('id', '4717dfe5a9fe198100450448b2404c16') // should be 'sys_id'
    .select('description', 'severity')
    .toArray(100);
  // Error: Unable to find field 'id' in table 'task'. Known fields: active, activity_due, ...
```

This code sample would throw an error because the data type of one of the arguments is incorrect.

```
new global.GlideQuery('task')
    .where('priority', 'one') // priority is an integer (should be 1)
    .select('description', 'severity')
    .toArray(100);
  // Error: Unable to match value ['one'] with field 'priority' in table 'task'. Expecting type 'integer'
```

## Reuse

Because GlideQuery objects are immutable, you can reuse them later in other parts of your code. For example, this script creates a query and then uses the GlideQuery object later to generate a report.

```
var highPriorityTasks = new global.GlideQuery('task')
    .where('active', true)
    .where('priority', 1);

generateReport(highPriorityTasks);
notifyOwners(highPriorityTasks);
var avgReassignmentCount = highPriorityTasks
    .avg('reassignment_count')
    .orElse(0)

```

## Limitations

The GlideQuery script include does not support:

-   Reading or writing to tables that do not allow access from other scopes.
-   Reading encoded queries.
-   GlideDate or GlideDateTime objects, which are read as JavaScript strings.
-   FX currency fields.
-   Updating journal field types.
-   Queries with ambiguous conditional logic. For example, the following query is unclear because the system does not know whether to execute `(active = true AND name != null) OR last_name = Luddy` or `active = true AND (name != null OR last_name = Luddy)`.

    ```
    var user = new global.GlideQuery('sys_user')
      .where('active', true)
      .whereNotNull('name')
      .orWhere('last_name', 'Luddy')
      .selectOne()
      .get()
    ```

    See the [where\(\)](GlideQueryGlobalAPI.md#) method to understand how to nest a child query instead.


**Note:** Because the GlideQuery script include converts GlideRecord objects into standard JavaScript objects, it may take longer to execute queries. To reduce performance issues, avoid creating loops that iterate over large numbers of records.

## Intermediate and terminal methods in GlideQuery

The GlideQuery script include uses two categories of methods: intermediate and terminal. Intermediate methods are those methods that return a [Stream](../../Stream/concept/StreamGlobalAPI.md#), an API used for interacting with a stream of items like records, allowing a fluent style of syntax where calls are chained together. Terminal methods are those methods that do not return a stream and therefore stop the chain of Stream method calls.

In the GlideQuery script include, methods such as where\(\), orderBy\(\), and disableWorkflow\(\) are intermediate methods that return a new GlideQuery object. Similarly, the GlideQuery script include's most popular terminal methods, select\(\) and selectOne\(\), are terminal methods. These methods are called when GlideQuery is done being configured and is ready to start processing records. The differences between these two method types is important to keep in mind when configuring calls to the GlideQuery script include according to your specific use cases. For more information about intermediate and terminal methods, see the article [GlideQuery - Stream Processing Part 1](https://developer.servicenow.com/blog.do?p=/post/glidequery-p6/).

The following methods are classified as intermediate:

-   aggregate\(String aggregateType, String field\)
-   disableAutoSysFields\(\)
-   disableWorkflow\(\)
-   forceUpdate\(\)
-   groupBy\(String fields\)
-   having\(String aggregateType, String field, String operator, Number value\)
-   limit\(Number limit\)
-   orderBy\(String fields\)
-   orderByDesc\(String fieldOrAggregate, String field\)
-   orWhere\(String fieldOrQuery, String operator, Any value\)
-   orWhereNotNull\(String field\)
-   orWhereNull\(String field\)
-   where\(String fieldOrQuery, String operator, Any value\)
-   whereNotNull\(String field\)
-   whereNull\(String field\)
-   withAcls\(\)

The following methods are classified as terminal:

-   avg\(String field\)
-   count\(\)
-   deleteMultiple\(\)
-   get\(String key, Array selectedFields\)
-   getBy\(Object keyValues, Array selectedFields\)
-   insert\(Object keyValues, Object selectedFields\)
-   insertOrUpdate\(Object changes, Object selectedFields\)
-   max\(String field\)
-   min\(String field\)
-   select\(String fields\)
-   selectOne\(String fields\)
-   sum\(String field\)
-   toGlideRecord\(\)
-   update\(Object changes, Object selectedFields\)
-   updateMultiple\(Object changes\)

**Note:** parse\(String table, String encoded\_query\) is neither intermediate or terminal, but static.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## GlideQuery - GlideQuery\(String table\)

Instantiates a GlideQuery object used to build and execute record queries.

|Name|Type|Description|
|----|----|-----------|
|table|String|Table to query.|

|Type|Description|
|----|-----------|
|None| |

This example instantiates a query of the User table.

```
var query = new global.GlideQuery('sys_user');
```

## GlideQuery - aggregate\(String aggregateType, String field\)

Aggregates a field using a specified aggregation function.

Use this method to build queries that aggregate against multiple fields or use multiple aggregate functions, or if you must use the groupBy\(\) method. If you only want to aggregate against one field with one function, and you don't need to use groupBy\(\), then use one of these methods instead:

-   avg\(\)
-   min\(\)
-   max\(\)
-   count\(\)

<table id="table_thy_rmc_nmb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

aggregateType

</td><td>

String

</td><td>

The type of aggregation function to perform. Options include:-   `min`: Returns the smallest value of all matching records.
-   `max`: Returns the largest value of all matching records.
-   `sum`: Returns the sum of all matching records.
-   `avg`: Returns the average of all matching records.
-   `count`: Returns the number of number of matching records.

</td></tr><tr><td>

field

</td><td>

String

</td><td>

Field on which to perform the operation.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|GlideQuery|The query object being built.|

This script performs a query on the Task table, groups the records by priority, and returns each priority that has total reassignments greater than four.

```
var query = new global.GlideQuery('task')
    .where('active', true) //Returns new GlideQuery object with a "where" clause.
    .groupBy('priority') //Returns new GlideQuery object with a "group by" clause.
    .aggregate('sum', 'reassignment_count') //Returns new GlideQuery object with a "sum(reassignment_count)" clause.
    .having('sum', 'reassignment_count', '>', 4) //Returns new GlideQuery object with a "having reassignment_count > 4" clause.
    .select() //Returns a stream of records wrapped in a Stream object.  
    .forEach(function (priority){ //Terminal method in the Stream class that executes the query and returns the result. 
      gs.info("Priority " + priority.group.priority + ": " + priority.sum.reassignment_count + " reassignments");
    });
```

Output:

```
Priority 1: 11 reassignments
Priority 3: 6 reassignments
Priority 5: 5 reassignments
```

## GlideQuery - avg\(String field\)

Returns the aggregate average of a given numeric field.

You can only use this method on fields of the following types:

-   Integer
-   Long
-   Floating point number
-   Double
-   Currency

|Name|Type|Description|
|----|----|-----------|
|field|String|Field on which to perform the operation.|

|Type|Description|
|----|-----------|
|Optional|Object that contains the aggregate average of the given field.|

This example shows how to return the average number of faults in the cmdb\_ci table.

```
var faults = new global.GlideQuery('cmdb_ci')
    .avg('fault_count')
    .orElse(0);

gs.info(JSON.stringify(faults));
```

Output:

```
0.0037
```

## GlideQuery - count\(\)

Returns the number of records that match the query.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Number|Number of records that match the query.|

This example returns the number of active records in the User table.

```
var userCount = new global.GlideQuery('sys_user')
    .where('active', true)
    .count();
```

Output:

```
612
```

## GlideQuery - deleteMultiple\(\)

Deletes all records in the table specified by the preceding Where clauses.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|None| |

This example deletes all active records in the User table where the last name is Jeter.

```
var query = new global.GlideQuery('sys_user')
    .where('active', true)
    .where('last_name', 'Jeter')
    .deleteMultiple();
```

## GlideQuery - disableAutoSysFields\(\)

Disables updating system fields, or fields with a name that starts with the `sys` prefix, such as sys\_created\_on, sys\_updated\_on, and sys\_mod\_count. Only applies to the specified query.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|GlideQuery|The query object being built.|

This example adds a record to the task table, but does not set system fields. Without calling this method, the below example would update sys\_updated\_on, sys\_mod\_count, and so on.

```
var query = new global.GlideQuery('task')
    .disableAutoSysFields()
    .insert({ description: 'example', priority: 1 });
```

## GlideQuery - disableWorkflow\(\)

Disables any business rules, flows, workflows, or audit records that would run or be created as the result of the query.

**Note:** This method only works for tables in the GLOBAL scope.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|GlideQuery|The query object being built.|

This example updates multiple records in the Task table without triggering any automatic business processes.

```
var query = new global.GlideQuery('task')
    .disableWorkflow()
    .where('active', true)
    .updateMultiple({ priority: 1 });
```

## GlideQuery - forceUpdate\(\)

Forces a database update even when no record changes are made. For example, you can use this method to force a business rule to execute.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|GlideQuery|The query object being built.|

This example force updates Task records with a certain sys\_id.

```
var forceUpdate = new global.GlideQuery('task')
    .forceUpdate()
    .where('sys_id', taskId)
    .update()
```

## GlideQuery - get\(String key, Array selectedFields\)

Returns a single record from the query.

<table id="table_u1k_flc_nmb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

key

</td><td>

String

</td><td>

Sys\_id of the record to return.

</td></tr><tr><td>

selectedFields

</td><td>

Array

</td><td>

Optional. Additional fields to return in the result. Default: The system always returns the sys\_id.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|Optional|Object used to interact with a single record.|

Example that returns a record based on sys\_id.

```
var user = new global.GlideQuery('sys_user')
    .get('5137153cc611227c000bbd1bd8cd2005', ['first_name', 'last_name']) //Returns an Optional object.
    .orElse({ first_name: 'Default', last_name: 'User' }); //Method in the Optional class to return a default value.

gs.info(JSON.stringify(user, null, 2));
```

Output:

```
{
   "sys_id":"5137153cc611227c000bbd1bd8cd2005",
   "first_name":"Fred",
   "last_name":"Luddy"
}
```

## GlideQuery - getBy\(Object keyValues, Array selectedFields\)

Returns an Optional object containing a single record based on a set of name-value pairs to query by. Assumes the '=' operator for each name-value pair.

<table id="table_ift_dlc_nmb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

keyValues

</td><td>

Object

</td><td>

Object where the keys are the name of the fields, and the values are the values to query for.

</td></tr><tr><td>

selectedFields

</td><td>

Array

</td><td>

Optional. Additional fields to return in the result. Default: The system always returns the sys\_id.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|Optional|Object used to interact with a single record.|

Example that returns a record by querying for a user's name.

```
var user = new global.GlideQuery('sys_user')
    .getBy({
        first_name: 'Fred',
        last_name: 'Luddy'
    }, ['first_name', 'last_name', 'city', 'active']) // select first_name, last_name, city, active
    .orElse({
        first_name: 'Nobody',
        last_name: 'Found',
        city: 'Nowhere',
        active: false
    });

gs.info(JSON.stringify(user, null, 2));
```

Output:

```
{
   "first_name":"Fred",
   "last_name":"Luddy",
   "city":null,
   "active":true,
   "sys_id":"5137153cc611227c000bbd1bd8cd2005"
}
```

## GlideQuery - groupBy\(String fields\)

Groups the query results by a designated field or fields.

You must use this method with the aggregate\(\) method.

|Name|Type|Description|
|----|----|-----------|
|fields|String or Array of Strings|Field or fields to group the results by.|

|Type|Description|
|----|-----------|
|GlideQuery|The query object being built.|

This script performs a query on the Task table, groups the records by priority, and returns each priority that has total reassignments greater than four.

```
var query = new global.GlideQuery('task')
    .where('active', true) //Returns new GlideQuery object with a "where" clause.
    .groupBy('priority') //Returns new GlideQuery object with a "group by" clause.
    .aggregate('sum', 'reassignment_count') //Returns new GlideQuery object with a "sum(reassignment_count)" clause.
    .having('sum', 'reassignment_count', '>', 4) //Returns new GlideQuery object with a "having reassignment_count > 4" clause.
    .select() //Returns a stream of records wrapped in a Stream object.  
    .forEach(function (priority){ //Terminal method in the Stream class that executes the query and returns the result. 
      gs.info("Priority " + priority.group.priority + ": " + priority.sum.reassignment_count + " reassignments");
    });
```

Output:

```
Priority 1: 11 reassignments
Priority 3: 6 reassignments
Priority 5: 5 reassignments
```

## GlideQuery - having\(String aggregateType, String field, String operator, Number value\)

Filters aggregate groups so that you can display only groups of results that match a specified condition.

Must use this method with the aggregate\(\) or groupBy\(\) methods.

<table id="table_jw3_vmc_nmb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

aggregateType

</td><td>

String

</td><td>

The type of aggregation function to perform. Options include:-   `min`: Returns the smallest value of all matching records.
-   `max`: Returns the largest value of all matching records.
-   `sum`: Returns the sum of all matching records.
-   `avg`: Returns the average of all matching records.
-   `count`: Returns the number of number of matching records.

</td></tr><tr><td>

field

</td><td>

String

</td><td>

Field on which to perform the operation.

</td></tr><tr><td>

operator

</td><td>

String

</td><td>

Numeric operator to use in the operation. Options include:

-   `>`: Greater than.
-   `<`: Less than.
-   `>=`: Greater than or equal to.
-   `<=`: Less than or equal to.
-   `=`: Equal to.
-   `!=`: Not equal to.

</td></tr><tr><td>

value

</td><td>

Number

</td><td>

Number value to use in the operation.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|GlideQuery|The query object being built.|

This script performs a query on the Task table, groups the records by priority, and returns each priority that has total reassignments greater than four.

```
var query = new global.GlideQuery('task')
    .where('active', true) //Returns new GlideQuery object with a "where" clause.
    .groupBy('priority') //Returns new GlideQuery object with a "group by" clause.
    .aggregate('sum', 'reassignment_count') //Returns new GlideQuery object with a "sum(reassignment_count)" clause.
    .having('sum', 'reassignment_count', '>', 4) //Returns new GlideQuery object with a "having reassignment_count > 4" clause.
    .select() //Returns a stream of records wrapped in a Stream object.  
    .forEach(function (priority){ //Terminal method in the Stream class that executes the query and returns the result. 
      gs.info("Priority " + priority.group.priority + ": " + priority.sum.reassignment_count + " reassignments");
    });
```

Output:

```
Priority 1: 11 reassignments
Priority 3: 6 reassignments
Priority 5: 5 reassignments
```

## GlideQuery - insert\(Object keyValues, Object selectedFields\)

Inserts a record and returns an Optional object containing the record.

<table id="table_m5f_hlc_nmb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

keyValues

</td><td>

Object

</td><td>

Object containing name-value pairs to insert into the record. Unspecified fields will be null.

</td></tr><tr><td>

selectedFields

</td><td>

Array

</td><td>

Optional. Additional fields to return in the result. Default: The system always returns the sys\_id.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|Optional|Object used to interact with a single record.|

This example shows how to insert a record based on a user's first and last name.

```
var fred = new global.GlideQuery('sys_user')
    .insert({ first_name: 'Fred', last_name: 'Luddy' })
    .get();

gs.info(JSON.stringify(fred, null, 2));
```

Output:

```
{
   "sys_id":"cf16eed0e82a9010f8778bda83d255d2",
   "first_name":"Fred",
   "last_name":"Luddy"
}
```

## GlideQuery - insertOrUpdate\(Object changes, Object selectedFields\)

Updates an existing record, or inserts a new record if one does not already exist.

<table id="table_sdt_3lc_nmb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

changes

</td><td>

Object

</td><td>

Object containing name-value pairs to update or insert into the record.

</td></tr><tr><td>

selectedFields

</td><td>

Array

</td><td>

Optional. Additional fields to return in the result. Default: The system always returns the sys\_id.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|Optional|Object used to interact with a single record.|

This example shows how to insert a new record that does not already exist in the system.

```
// insert a new record
var user = new GlideQuery('sys_user')
    .insertOrUpdate({
        first_name: 'George',
        last_name: 'Griffey'
    })
    .orElse(null);
```

This example shows how to update an existing record.

```
// update existing record
var user = new global.GlideQuery('sys_user')
    .insertOrUpdate({
        sys_id: '2d0efd6c73662300bb513198caf6a72e',
        first_name: 'George',
        last_name: 'Griffey' })
    .orElse(null);
```

## GlideQuery - limit\(Number limit\)

Limits the number of records returned in a query.

|Name|Type|Description|
|----|----|-----------|
|limit|Number|Number of records to return.|

|Type|Description|
|----|-----------|
|GlideQuery|The query object being built.|

This example shows how to limit the results returned to five records.

```
var incidents = new global.GlideQuery('incident')
    .limit(5)
    .select('priority', 'description')
    .forEach(function (incident){
        gs.info(JSON.stringify(incident, null, 2));
    });
```

Output:

```
*** Script: {
  "priority": 1,
  "description": "User can't get to any of his files on the file server.",
  "sys_id": "9d385017c611228701d22104cc95c371"
}
*** Script: {
  "priority": 1,
  "description": "I just moved from floor 2 to floor 3 and my laptop cannot connect to any wireless network.",
  "sys_id": "e8caedcbc0a80164017df472f39eaed1"
}
*** Script: {
  "priority": 1,
  "description": "User forgot their email password.",
  "sys_id": "9d3c1197c611228701cd1d94bc32d76d"
}
*** Script: {
  "priority": 1,
  "description": "When I try to print, my whole computer just freezes and stops working.",
  "sys_id": "8d6246c7c0a80164012fb063cecd4ace"
}
*** Script: {
  "priority": 3,
  "description": "Unable to login even though login credentials are correct.",
  "sys_id": "a9e30c7dc61122760116894de7bcc7bd"
}
```

## GlideQuery - max\(String field\)

Returns the aggregate maximum of a given field.

|Name|Type|Description|
|----|----|-----------|
|field|String|Field on which to perform the operation.|

|Type|Description|
|----|-----------|
|Optional|Object used to interact with a single record.|

This example shows how to return the maximum value, or highest alphanumeric value, of a given field.

```
var name = new global.GlideQuery('sys_user')
    .max('last_name')
    .orElse('');

gs.info(JSON.stringify(name));
```

Output:

```
"Zortman"
```

## GlideQuery - min\(String field\)

Returns the aggregate minimum of a given field.

|Name|Type|Description|
|----|----|-----------|
|field|String|Field on which to perform the operation.|

|Type|Description|
|----|-----------|
|Optional|Object used to interact with a single record.|

This example shows how to return the minimum value, or lowest alphanumeric value, of a given field.

```
var name = new global.GlideQuery('sys_user')
    .min('last_name')
    .orElse('');

gs.info(JSON.stringify(name));
```

Output:

```
"Abel"
```

## GlideQuery - orderBy\(String fields\)

Orders the returned result in ascending order by a given field.

|Name|Type|Description|
|----|----|-----------|
|fields|String|Comma-delimited fields to order the result by in ascending order.|

|Type|Description|
|----|-----------|
|GlideQuery|The query object being built.|

This example shows how to order results in ascending order by record number.

```
var query = new global.GlideQuery('incident')
    .orderBy('number')
    .limit(5)
    .select('number', 'description') //Returns a stream of records wrapped in a Stream object.  
    .forEach(function (incident){ //Terminal method in the Stream class that executes the query and returns the result.
        gs.info(JSON.stringify(incident, null, 2));
    });
```

Output:

```
*** Script: {
  "number": "INC0000001",
  "description": "User can't access email on mail.company.com.",
  "sys_id": "9c573169c611228700193229fff72400"
}
*** Script: {
  "number": "INC0000002",
  "description": "User can't get to any of his files on the file server.",
  "sys_id": "9d385017c611228701d22104cc95c371"
}
*** Script: {
  "number": "INC0000003",
  "description": "I just moved from floor 2 to floor 3 and my laptop cannot connect to any wireless network.",
  "sys_id": "e8caedcbc0a80164017df472f39eaed1"
}
*** Script: {
  "number": "INC0000004",
  "description": "User forgot their email password.",
  "sys_id": "9d3c1197c611228701cd1d94bc32d76d"
}
*** Script: {
  "number": "INC0000005",
  "description": "CPU was 100% busy for more than 10 minutes",
  "sys_id": "e8e875b0c0a80164009dc852b4d677d5"
}
```

## GlideQuery - orderByDesc\(String fieldOrAggregate, String field\)

Orders the returned result in descending order by a given field.

<table id="table_yxt_cmc_nmb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

fieldOrAggregate

</td><td>

String

</td><td>

If the query does not use the aggregate\(\) method, pass the field to order the results by. If the query uses the aggregate\(\) method, pass the type of aggregation function to perform.

 Options include:

-   `min`: Returns the smallest value of all matching records.
-   `max`: Returns the largest value of all matching records.
-   `sum`: Returns the sum of all matching records.
-   `avg`: Returns the average of all matching records.
-   `count`: Returns the number of number of matching records.

</td></tr><tr><td>

field

</td><td>

String

</td><td>

Optional. Field to order the result by in descending order. Required for queries using the aggregate\(\) method.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|GlideQuery|The query object being built.|

This example shows how to order the result in descending order by number.

```
var query = new global.GlideQuery('incident')
    .orderByDesc('number')
    .limit(5)
    .select('number', 'description') //Returns a stream of records wrapped in a Stream object.  
    .forEach(function (incident){ //Terminal method in the Stream class that executes the query and returns the result.
        gs.info(JSON.stringify(incident, null, 2));
    });
```

Output:

```
*** Script: {
  "number": "INC0009009",
  "description": "Unable to access the shared folder. Please provide access.",
  "sys_id": "57af7aec73d423002728660c4cf6a71c"
}
*** Script: {
  "number": "INC0009005",
  "description": "Unable to send or receive emails.",
  "sys_id": "ed92e8d173d023002728660c4cf6a7bc"
}
*** Script: {
  "number": "INC0009004",
  "description": "While launching the defect tracking base URL, it is redirecting to an error page.",
  "sys_id": "e329de99731423002728660c4cf6a73c"
}
*** Script: {
  "number": "INC0009003",
  "description": "Having an issue with users trying to access the company portal app",
  "sys_id": "9fffc328731823002728660c4cf6a742"
}
*** Script: {
  "number": "INC0009002",
  "description": "My computer is not detecting the headphone device. It could be an issue with the USB port.",
  "sys_id": "1c832706732023002728660c4cf6a7b9"
}
```

This example shows how to order an aggregate result by the sum of child incidents.

```
var aggQuery = new GlideQuery('incident')
    .aggregate('sum', 'child_incidents')
    .groupBy('category')
    .orderByDesc('sum', 'child_incidents')
    .select()
    .forEach(function (category){
        gs.info(JSON.stringify(category, null, 2));    
    });
```

Output:

```
*** Script: {
  "group": {
    "category": "hardware"
  },
  "sum": {
    "child_incidents": 2
  }
}
*** Script: {
  "group": {
    "category": "inquiry"
  },
  "sum": {
    "child_incidents": 1
  }
}
*** Script: {
  "group": {
    "category": "software"
  },
  "sum": {
    "child_incidents": 0
  }
}
*** Script: {
  "group": {
    "category": ""
  },
  "sum": {
    "child_incidents": null
  }
}
*** Script: {
  "group": {
    "category": "database"
  },
  "sum": {
    "child_incidents": null
  }
}
*** Script: {
  "group": {
    "category": "network"
  },
  "sum": {
    "child_incidents": null
  }
}
```

## GlideQuery - orWhere\(String fieldOrQuery, String operator, Any value\)

Adds an OR clause to a query that returns values based on a given condition.

**Note:** Precede this method with the where\(\), whereNull\(\), or whereNotNull\(\) methods.

|Name|Type|Description|
|----|----|-----------|
|fieldOrQuery|String or [GlideQuery](GlideQueryGlobalAPI.md#)|Field or another GlideQuery object used in the where clause. If passing a field, you can dot-walk to a desired value. For example, `'company.name'`.|
|operator|String|Optional. Operator used in the OR clause. If you do not pass an argument, the system uses the = operator. You do not need to include a placeholder value.|
|value|Any|Value used in the OR clause.|

|Type|Description|
|----|-----------|
|GlideQuery|The query object being built.|

This example shows how to add a simple OR clause to a query.

```
var query = new global.GlideQuery('sys_user')
   .where('failed_attempts', '>', 0)
   .orWhere('last_login', '<', '2019-04-15')
   .select()
   .forEach(function (user){
      gs.info(JSON.stringify(user, null, 2));
   });
```

Output:

```
*** Script: {
  "sys_id": "005d500b536073005e0addeeff7b12f4"
}
*** Script: {
  "sys_id": "d999e5fc77e72300454792718a10611d"
}
*** Script: {
  "sys_id": "30ad318577ab2300454792718a10619e"
}
*** Script: {
  "sys_id": "4ac73ecd738123002728660c4cf6a72c"
}
*** Script: {
  "sys_id": "3883f4c0730123002728660c4cf6a754"
}
*** Script: {
  "sys_id": "3988a3ca732023002728660c4cf6a757"
}
*** Script: {
  "sys_id": "8ff5b254b33213005e3de13516a8dcf7"
}
```

This example shows how to add an `orWhere` clause that contains a separate query.

```
// active = true OR (title = 'Vice President' AND state = 'CA')
var query = new GlideQuery('sys_user')
   .where('active', true)
   .orWhere(new GlideQuery()
       .where('title', 'Vice President')
       .where('state', 'CA'))
   .select('name')
   .limit(5)
   .forEach(function (user){
      gs.info(JSON.stringify(user, null, 2));
   });
```

Output:

```
*** Script: {
  "name": "ITIL User",
  "sys_id": "681b365ec0a80164000fb0b05854a0cd"
}
*** Script: {
  "name": "SOAP Guest",
  "sys_id": "155699460a0a0b2b009e27c10b7f68f6"
}
*** Script: {
  "name": "System Administrator",
  "sys_id": "6816f79cc0a8016401c5a33be04be441"
}
*** Script: {
  "name": "Alva Pennigton",
  "sys_id": "ca826bf03710200044e0bfc8bcbe5d89"
}
*** Script: {
  "name": "Benchmark Scheduler",
  "sys_id": "d3383a875b0132003d1c484c11f91a5b"
}
```

## GlideQuery - orWhereNotNull\(String field\)

Adds an OR clause that returns records that do not contain a null value in a given field.

**Note:** Precede this method with the where\(\), whereNull\(\), or whereNotNull\(\) methods.

|Name|Type|Description|
|----|----|-----------|
|field|String|Field used in the query.|

|Type|Description|
|----|-----------|
|GlideQuery|The query object being built.|

This example shows how to query the User table and return results where the first or last names are not null.

```
var query = new global.GlideQuery('sys_user')
   .whereNotNull('first_name')
   .orWhereNotNull('last_name')
   .select('name')
   .limit(5)
   .forEach(function (user){
      gs.info(JSON.stringify(user, null, 2));
   });
```

Output:

```
*** Script: {
  "name": "ITIL User",
  "sys_id": "681b365ec0a80164000fb0b05854a0cd"
}
*** Script: {
  "name": "System Administrator",
  "sys_id": "6816f79cc0a8016401c5a33be04be441"
}
*** Script: {
  "name": "Alva Pennigton",
  "sys_id": "ca826bf03710200044e0bfc8bcbe5d89"
}
*** Script: {
  "name": "Benchmark Scheduler",
  "sys_id": "d3383a875b0132003d1c484c11f91a5b"
}
*** Script: {
  "name": "Allyson Gillispie",
  "sys_id": "06826bf03710200044e0bfc8bcbe5d8a"
}
```

## GlideQuery - orWhereNull\(String field\)

Adds an OR clause to a query that returns records that contain a null value in a given field.

**Note:** Precede this method with the where\(\), whereNull\(\), or whereNotNull\(\) methods.

|Name|Type|Description|
|----|----|-----------|
|field|String|Field used in the query.|

|Type|Description|
|----|-----------|
|GlideQuery|The query object being built.|

This example shows how to query the User table and return records where the first or last names are null.

```
var query = new global.GlideQuery('sys_user')
   .whereNull('last_name')
   .orWhereNull('first_name')
   .select('first_name', 'last_name')
   .forEach(function (user){
      gs.info(JSON.stringify(user, null, 2));
   });
```

Output:

```
*** Script: {
  "first_name": "ml.admin",
  "last_name": null,
  "sys_id": "88aad6c5c73003005f1b78d48b9763a5"
}
*** Script: {
  "first_name": "Sitemap Scheduler User",
  "last_name": null,
  "sys_id": "85388c25b71011104eed4643ae11a993"
}
*** Script: {
  "first_name": null,
  "last_name": "Guest",
  "sys_id": "5136503cc611227c0183e96598c4f706"
}
*** Script: {
  "first_name": "ml_report.user",
  "last_name": null,
  "sys_id": "b6bad6c5c73003005f1b78d48b97632a"
}
```

## GlideQuery - parse\(String table, String encoded\_query \)

Adds an encoded query to a new GlideQuery query.

This method does not support all GlideRecord encoded query operators. The following operators are currently supported:

<table><tbody><tr><td>

`=`

</td><td>

`ANYTHING`

</td><td>

`GT_FIELD`

</td><td>

`NOT IN`

</td></tr><tr><td>

`!=`

</td><td>

`BETWEEN`

</td><td>

`GT_OR_EQUALS_FIELD`

</td><td>

`NOT LIKE`

</td></tr><tr><td>

`>`

</td><td>

`CONTAINS`

</td><td>

`IN`

</td><td>

`NSAMEAS`

</td></tr><tr><td>

`>=`

</td><td>

`DOES NOT CONTAIN`

</td><td>

`INSTANCEOF`

</td><td>

`ON`

</td></tr><tr><td>

`<`

</td><td>

`DYNAMIC`

</td><td>

`LIKE`

</td><td>

`SAMEAS`

</td></tr><tr><td>

`<=`

</td><td>

`EMPTYSTRING`

</td><td>

`LT_FIELD`

</td><td>

`STARTSWITH`

</td></tr><tr><td>

 

</td><td>

`ENDSWITH`

</td><td>

`LT_OR_EQUALS_FIELD`

</td><td>

 

</td></tr></tbody>
</table>|Name|Type|Description|
|----|----|-----------|
|table|String|Table to query, such as task or incident.|
|encoded\_query|String|[Encoded query](https://www.servicenow.com/docs/access?context=c_EncodedQueryStrings&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US) to apply to the records in the specified table.|

|Type|Description|
|----|-----------|
|GlideQuery|GlideQuery object containing the encoded query.|

The following example creates a GlideQuery object that contains all active records in the task table, ordered by the priority field, returned as a Stream object that contains just the description field.

```
GlideQuery.parse('task', 'active=true^ORDERBYpriority') // Pass the encoded query to use to parse the Task records
  .select('description') // Return the records that match the encoded query
  .forEach(doSomething); // Do some processing on each of the returned records
```

## GlideQuery - select\(String fields\)

Returns the results of the query as a Stream object containing the specified fields.

**Note:** Use a terminal method in the Stream class to get the result of the query. For more information, see [Stream](../../Stream/concept/StreamGlobalAPI.md#).

You can append a flag to a field name to return the field's metadata instead of the field's value. For example, using the field name `company$DISPLAY` returns the display value of a company field. Possible flags include:

-   `DISPLAY`: Returns the display value of a field.
-   `CURRENCY_CODE`: Returns the currency code of a currency field. For example, `USD`.
-   `CURRENCY_DISPLAY`: Returns the currency display value of a currency field. For example, `¥123.45`.
-   `CURRENCY_STRING`: Returns the currency string of a currency field. For example, `JPY;123.45`.

<table id="table_ktr_qlc_nmb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

fields

</td><td>

String or Array of Strings

</td><td>

Optional. Fields to display in the result. You can provide any number of fields as arguments, dot-walk to a desired value, or use a flag. For example: ```
select('first_name', 'location.city', 'company$DISPLAY');
```

or```
select(['first_name', 'location.city', 'company$DISPLAY']);
```

 Default: The system always returns the sys\_id.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|Stream|Object used to interact with a stream of items such as records.|

This example shows how to select fields to display from the query and use `$DISPLAY` to return the display value of a field.

```
var stream = new global.GlideQuery('sys_user')
   .select('first_name', 'last_name', 'company$DISPLAY')
   .limit(5)
   .forEach(function (user){
      gs.info(JSON.stringify(user, null, 2));
   });
```

Output:

```
*** Script: {
  "first_name": "System",
  "last_name": "Administrator",
  "company$DISPLAY": "",
  "sys_id": "6816f79cc0a8016401c5a33be04be441"
}
*** Script: {
  "first_name": "Alva",
  "last_name": "Pennigton",
  "company$DISPLAY": "ACME North America",
  "sys_id": "ca826bf03710200044e0bfc8bcbe5d89"
}
*** Script: {
  "first_name": "Benchmark",
  "last_name": "Scheduler",
  "company$DISPLAY": "",
  "sys_id": "d3383a875b0132003d1c484c11f91a5b"
}
*** Script: {
  "first_name": "Allyson",
  "last_name": "Gillispie",
  "company$DISPLAY": "ACME North America",
  "sys_id": "06826bf03710200044e0bfc8bcbe5d8a"
}
*** Script: {
  "first_name": "SOAP",
  "last_name": "Guest",
  "company$DISPLAY": "",
  "sys_id": "155699460a0a0b2b009e27c10b7f68f6"
}
```

## GlideQuery - selectOne\(String fields\)

Returns the result of the query as an Optional object containing specified fields.

Use this method when returning a single record, or to test if a record exists. If returning multiple records, use the select\(\) method to return a Stream object.

You can append a flag to a field name to return the field's metadata instead of the field's value. For example, using the field name `company$DISPLAY` returns the display value of a company field. Possible flags include:

-   `DISPLAY`: Returns the display value of a field.
-   `CURRENCY_CODE`: Returns the currency code of a currency field. For example, `USD`.
-   `CURRENCY_DISPLAY`: Returns the currency display value of a currency field. For example, `¥123.45`.
-   `CURRENCY_STRING`: Returns the currency string of a currency field. For example, `JPY;123.45`.

<table id="table_pw3_slc_nmb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

fields

</td><td>

String or Array of Strings

</td><td>

Optional. Fields to display in the result. You can provide any number of fields as arguments, dot-walk to a desired value, or use a flag. For example: ```
selectOne('first_name', 'location.city', 'company$DISPLAY');
```

or```
selectOne(['first_name', 'location.city', 'company$DISPLAY']);
```

 Default: The system always returns the sys\_id.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|Optional|Object used to interact with a single record.|

This example shows how to return a single record as an Optional object and display specified fields.

```
var user = new global.GlideQuery('sys_user')
    .where('zip', '12345')
    .whereNotNull('last_name')
    .selectOne('first_name', 'last_name', 'company$DISPLAY')
    .get();

gs.info(JSON.stringify(user, null, 2));
```

Output:

```
{
   "first_name":"Abel",
   "last_name":"Tuter",
   "company$DISPLAY":"ACME South America",
   "sys_id":"62826bf03710200044e0bfc8bcbe5df1"
}
```

## GlideQuery - sum\(String field\)

Returns the aggregate sum of a given numeric field.

You can only use this method on fields of the following types:

-   Integer
-   Long
-   Floating point number
-   Double
-   Currency

|Name|Type|Description|
|----|----|-----------|
|field|String|Field on which to perform the operation.|

|Type|Description|
|----|-----------|
|Optional|Object used to interact with a single record.|

This example shows how to return the sum of all faults in the cmdb\_ci table.

```
var totalFaults = new global.GlideQuery('cmdb_ci')
    .sum('fault_count')
    .orElse(0);

gs.info(JSON.stringify(totalFaults));
```

Output:

```
10
```

## GlideQuery - toGlideRecord\(\)

Returns a GlideRecord object that represents the current query. Returns a GlideAggregrate object if the query uses the GlideQuery.aggregate\(\) method.

After transforming the query, use the query\(\) method in the [GlideRecord](../../glideRecordScoped/concept/c_GlideRecordScopedAPI.md#) or [GlideAggregate](../../glideAggregateScoped/concept/c_GlideAggregateScopedAPI.md#) classes to query the database.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|GlideRecord or GlideAggregate|GlideRecord object that contains the query. If you used the GlideQuery.aggregate\(\) method, then the method returns a GlideAggregrate object instead.|

This example shows how to transform a GlideQuery object into a GlideRecord.

```
var userGr = new global.GlideQuery('sys_user')
    .where('active', true)
    .whereNotNull('first_name')
    .limit(10)
    .toGlideRecord();
userGr.query();
```

## GlideQuery - update\(Object changes, Object selectedFields\)

Updates an existing record that matches the defined conditions.

Before using this method, call the where\(\) method to specify the conditions that a record must meet to be updated.

<table id="table_cbg_klc_nmb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

changes

</td><td>

Object

</td><td>

Object containing name-value pairs to update in the record. Names must match fields in the table.

</td></tr><tr><td>

selectedFields

</td><td>

Array

</td><td>

Optional. Additional fields to return in the result. Default: The system always returns the sys\_id.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|Optional|Object used to interact with a single record.|

This example shows how to update a record with new values.

```
var updateRecord = new global.GlideQuery('sys_user')
    .where('sys_id', '0a826bf03710200044e0bfc8bcbe5d7a')
    .update({ city: 'Los Angeles' });
```

## GlideQuery - updateMultiple\(Object changes\)

Updates all existing records that match the defined conditions. Returns the number of records updated.

Before using this method, call the where\(\) method to specify the conditions that the records must meet to be updated.

|Name|Type|Description|
|----|----|-----------|
|changes|Object|Object containing name-value pairs to update in the record. Names must match fields in the table.|

<table id="table_zwr_llc_nmb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Object containing the number of records that were updated. Keys include: -   `rowCount`: Number of rows updated in the table.

</td></tr></tbody>
</table>This example shows how to update any records that fit a defined criteria.

```
var update = new global.GlideQuery('sys_user')
    .where('active', false)
    .where('last_name', 'Griffey')
    .updateMultiple({ active: true });

gs.info(JSON.stringify(update));
```

Output:

```
{"rowCount":1}
```

## GlideQuery - where\(String fieldOrQuery, String operator, Any value\)

Adds a Where clause to the query that returns values based on a given condition.

**Note:** Do not precede this method with the orWhere\(\), orWhereNull\(\), or orWhereNotNull\(\) methods.

|Name|Type|Description|
|----|----|-----------|
|fieldOrQuery|String or [GlideQuery](GlideQueryGlobalAPI.md#)|Field or another GlideQuery object used in the where clause. If passing a field, you can dot-walk to a desired value. For example, `'company.name'`.|
|operator|String|Optional. Operator used in the where clause. If you do not pass an argument, the system uses the = operator.|
|value|Any|Value used in the where clause.|

|Type|Description|
|----|-----------|
|GlideQuery|The query object being built.|

This example shows how to return records from the User table where active is true and the user's last login is after a specified date.

```
var query = new global.GlideQuery('sys_user')
   .where('active', true)
   .where('last_login', '>', '2018-01-01')
   .limit(5)
   .select()
   .forEach(function (user){
      gs.info(JSON.stringify(user, null, 2));
   });
```

Output:

```
*** Script: {
  "sys_id": "6816f79cc0a8016401c5a33be04be441"
}
*** Script: {
  "sys_id": "005d500b536073005e0addeeff7b12f4"
}
*** Script: {
  "sys_id": "d999e5fc77e72300454792718a10611d"
}
*** Script: {
  "sys_id": "30ad318577ab2300454792718a10619e"
}
*** Script: {
  "sys_id": "3883f4c0730123002728660c4cf6a754"
}
```

This example shows how to return records from the Incident table where active is true and the priority or severity is 1.

```
// active = true AND (priority = 1 OR severity = 1)
var query = new GlideQuery('incident')
    .where('active', true)
    .where(new GlideQuery()
        .where('priority', 1)
        .orWhere('severity', 1))
   .limit(5)
   .select()
   .toArray(5)

gs.info(JSON.stringify(query, null, 2));
```

Output:

```
[
   {
      "sys_id":"b0f31e5673500010c2e7660c4cf6a711"
   },
   {
      "sys_id":"8ff5b254b33213005e3de13516a8dcf7"
   },
   {
      "sys_id":"d999e5fc77e72300454792718a10611d"
   },
   {
      "sys_id":"30ad318577ab2300454792718a10619e"
   },
   {
      "sys_id":"3883f4c0730123002728660c4cf6a754"
   }
]
```

## GlideQuery - whereNotNull\(String field\)

Returns records that do not contain a null value in a given field.

**Note:** Do not precede this method with the orWhere\(\), orWhereNull\(\), or orWhereNotNull\(\) methods.

|Name|Type|Description|
|----|----|-----------|
|field|String|Field used in the query.|

|Type|Description|
|----|-----------|
|GlideQuery|The query object being built.|

This example shows how to query the User table and return results where the first\_name field is not null.

```
var query = new global.GlideQuery('sys_user')
   .whereNotNull('first_name')
   .select('name')
   .limit(5)
   .forEach(function (user){
      gs.info(JSON.stringify(user, null, 2));
   });
```

Output:

```
*** Script: {
  "name": "System Administrator",
  "sys_id": "6816f79cc0a8016401c5a33be04be441"
}
*** Script: {
  "name": "Alva Pennigton",
  "sys_id": "ca826bf03710200044e0bfc8bcbe5d89"
}
*** Script: {
  "name": "Benchmark Scheduler",
  "sys_id": "d3383a875b0132003d1c484c11f91a5b"
}
*** Script: {
  "name": "Allyson Gillispie",
  "sys_id": "06826bf03710200044e0bfc8bcbe5d8a"
}
*** Script: {
  "name": "SOAP Guest",
  "sys_id": "155699460a0a0b2b009e27c10b7f68f6"
}
```

## GlideQuery - whereNull\(String field\)

Returns records that contain a null value in a given field.

**Note:** Do not precede this method with the orWhere\(\), orWhereNull\(\), or orWhereNotNull\(\) methods.

|Name|Type|Description|
|----|----|-----------|
|field|String|Field used in the query.|

|Type|Description|
|----|-----------|
|GlideQuery|The query object being built.|

This example shows how to query the User table and return records where the first or last names are null.

```
var query = new global.GlideQuery('sys_user')
   .whereNull('last_name')
   .orWhereNull('first_name')
   .select('first_name', 'last_name')
   .forEach(function (user){
      gs.info(JSON.stringify(user, null, 2));
   });
```

Output:

```
*** Script: {
  "first_name": "ml.admin",
  "last_name": null,
  "sys_id": "88aad6c5c73003005f1b78d48b9763a5"
}
*** Script: {
  "first_name": "Sitemap Scheduler User",
  "last_name": null,
  "sys_id": "85388c25b71011104eed4643ae11a993"
}
*** Script: {
  "first_name": null,
  "last_name": "Guest",
  "sys_id": "5136503cc611227c0183e96598c4f706"
}
*** Script: {
  "first_name": "ml_report.user",
  "last_name": null,
  "sys_id": "b6bad6c5c73003005f1b78d48b97632a"
}
```

## GlideQuery - withAcls\(\)

Executes the query using the GlideRecordSecure API to securely query the database while honoring ACLs.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|GlideQuery|The query object being built.|

This example shows how to execute a secure query using ACLs.

```
var users = new global.GlideQuery('sys_user')
    .withAcls()
    .limit(5)
    .orderByDesc('first_name')
    .select('first_name')
    .forEach(function (user){
        gs.info(JSON.stringify(user, null, 2));
    });
```

Output:

```
*** Script: {
  "first_name": "Zane",
  "sys_id": "16826bf03710200044e0bfc8bcbe5dbc"
}
*** Script: {
  "first_name": "Zackary",
  "sys_id": "8a826bf03710200044e0bfc8bcbe5d69"
}
*** Script: {
  "first_name": "Yvette",
  "sys_id": "4e826bf03710200044e0bfc8bcbe5d57"
}
*** Script: {
  "first_name": "Winnie",
  "sys_id": "f682abf03710200044e0bfc8bcbe5d1d"
}
*** Script: {
  "first_name": "Wilmer",
  "sys_id": "42826bf03710200044e0bfc8bcbe5d7b"
}
```

