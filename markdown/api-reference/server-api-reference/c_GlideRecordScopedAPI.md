---
title: GlideRecord - Scoped
description: The scoped GlideRecord API is used for database operations.Adds a filter to return active records.Adds an encoded query to other queries that may have been set.Applies a pre-defined GlideDBFunctionBuilder object to a record.Adds a filter to return records based on a relationship in a table related to the current GlideRecord.A filter that specifies records where the value of the field passed in the parameter is not null.Adds a filter to return records where the value of the specified field is null.Adds a filter to return records using an encoded query string.Build a search query and return the rows that match the request.Provides the ability to build a request, which when executed, returns the rows from the specified table, that match the request.Provides atomic add and subtract operations on a specified number field at the database level for the current GlideRecord object.Sets the values of the specified encoded query terms and applies them to the current GlideRecord.Determines if the Access Control Rules, which include the user's roles, permit inserting new records in this table.Determines if the Access Control Rules, which include the user's roles, permit deleting records in this table.Determines if the Access Control Rules \(ACLs\) permit reading records in this table. This method evaluates all ACL types, such as user roles, scripted ACLs, ACLs with scripted conditions, and so on.Determines if the Access Control Rules, which include the user's roles, permit editing records in this table.Sets a range of rows to be returned by subsequent queries.Deletes all records that satisfy the query.Deletes the current record.Disables the default optimization that prevents an extra database query from running when a user passes in a large number of sys\_ids, such as grIncident.addQuery\('sys\_id', 'IN', listOf200SysIds\). Returns the specified record in the current GlideRecord object.Returns the dictionary attributes for the specified field.Returns the current table's label.Retrieves the display value for the current record.Returns the element's descriptor.Retrieves the GlideElement object for the specified field.Returns an array of GlideElement objects. Each object describes a field in the current GlideRecord.Retrieves the query condition of the current result set as an encoded query string. Returns the field's label.Retrieves the last error message. If there is no last error message, null is returned.Retrieves the link to the current record.Retrieves the class name for the current record.Retrieves the number of rows \(records\) in the current GlideRecord object.Retrieves the name of the table associated with the GlideRecord.Gets the primary key of the record, which is usually the sys\_id unless otherwise specified.Retrieves the string value of an underlying element in a field.Creates an instance of the GlideRecord class for the specified table.Determines if there are any more records in the GlideRecord object.Inserts a new record using the field values that have been set for the current record.Creates an empty record suitable for population before an insert.Checks to see if the current database action is to be aborted.Verifies whether the specified encoded query is valid.Checks if the current record is a new record that has not yet been inserted into the database.Determines if the current table is valid or if the record was successfully retrieved.Verifies whether the syntax of the encoded query is correct.Determines if the specified field is defined in the current table.Determines if a record was actually returned by the query/get record operation.Verifies whether the record was created in a view or a table.Creates a new GlideRecord record, sets the default values for the fields, and assigns a unique ID to the record.Moves to the next record in the GlideRecord object.Moves to the next record in the GlideRecord. Provides the same functionality as next\(\), use this method if the GlideRecord has a column named next.Determines if an operation is insert, update, or delete.Specifies an orderBy column.Specifies a descending orderBy column.Runs a query against the table based on the filters specified in the query methods such as addQuery\(\) and addEncodedQuery\(\).Runs a query against the table based on the filters specified in the query methods such as addQuery\(\) and addEncodedQuery\(\). This method is intended to be used on tables in which there's a column named "query", which might cause errors running the query\(\) method.Sets a flag to indicate if the next database action \(insert, update, delete\) is to be aborted. This is often used in business rules.Sets the limit for number of records are fetched by the GlideRecord query.Sets the sys\_id value for the current record.Stops a GlideRecord query from running a COUNT\(\*\) query.Sets the value of the field with the specified name to the specified value.Enables or disables the running of business rules, script engines, and audit.Updates the GlideRecord with any changes that have been made. If the record does not already exist, it is inserted.Updates each GlideRecord in a stated query with a specified set of changes.Updates a record and also inserts or updates any related records with the information provided.
locale: en-US
release: yokohama
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 55
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# GlideRecord- Scoped

The scoped GlideRecord API is used for database operations.

The GlideRecord API is the primary means of interfacing with the database on the server-side code. A GlideRecord is an object that contains records from a single table. Use the API to instantiate a GlideRecord object and add query parameters, filters, limits, and ordering.

See the [GlideRecord](https://developer.servicenow.com/dev.do#!/learn/courses/utah/app_store_learnv2_scripting_utah_scripting_in_servicenow/app_store_learnv2_scripting_utah_server_side_scripting/app_store_learnv2_scripting_utah_gliderecord) article for details on building and running queries.

For information on a class that performs the same functions as GlideRecord and enforces ACLs, see [Using GlideRecordSecure](../../../../../script/glide-server-apis/topic/p_GlideServerAPIs.md#).

Always test queries on a sub-production instance prior to deploying them on a production instance. An incorrectly constructed encoded query, such as including an invalid field name, produces an invalid query. When the invalid query is run, the invalid part of the query condition is dropped, and the results are based on the valid part of the query, which may return all records from the table. Using an insert\(\), update\(\), deleteRecord\(\), or deleteMultiple\(\) method on bad query results can result in data loss.

You can set the **glide.invalid\_query.returns\_no\_rows** system property to true to have queries with invalid encoded queries return no records. In some cases, the query may still return records in API results even when **glide.invalid\_query.returns\_no\_rows** is set to true. This happens in queries where an invalid query term is used with a WHERE operator. In such queries, the WHERE operator ignores the invalid term\(s\) but still interprets and returns the rest of the query statement. For more information about this system property and its functionality, see [Available system properties](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

## Retrieve values from records

In most cases, don’t use dot-walking to get values from a record. Dot-walking retrieves the entire object instead of the field value. Retrieving the object uses more storage and might cause undesirable results when used in arrays or in Service Portal.

Instead of retrieving the entire object, you can use one of the following methods to copy the field values:

-   [getValue\(\)](c_GlideRecordScopedAPI.md#)
-   [getDisplayValue\(\)](c_GlideRecordScopedAPI.md#)

If dot-walking through a GlideElement object is necessary, use the toString\(\) method to retrieve values. For example, you might need the current caller's manager sys\_id to set another reference field. The following example shows how to get the string value instead of the entire object:

```
var mgr = current.caller_id.manager.toString();
```

See also:

-   [GlideAggregate](../../glideAggregateScoped/concept/c_GlideAggregateScopedAPI.md#)
-   [GlideElement](../../glideElement/concept/c_GlideElementScopedAPI.md#)
-   [GlideQuery](../../GlideQuery/concept/GlideQueryGlobalAPI.md#)

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## Scoped GlideRecord - addActiveQuery\(\)

Adds a filter to return active records.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|GlideQueryCondition|Filter to return active records.|

```
var inc = new GlideRecord('incident');
inc.addActiveQuery();
inc.query();
```

## Scoped GlideRecord - addEncodedQuery\(String query, Boolean enforceFieldACL\)

Adds an encoded query to other queries that may have been set.

Always test queries on a sub-production instance prior to deploying them on a production instance. An incorrectly constructed encoded query, such as including an invalid field name, produces an invalid query. When the invalid query is run, the invalid part of the query condition is dropped, and the results are based on the valid part of the query, which may return all records from the table. Using an insert\(\), update\(\), deleteRecord\(\), or deleteMultiple\(\) method on bad query results can result in data loss.

You can set the **glide.invalid\_query.returns\_no\_rows** system property to true to have queries with invalid encoded queries return no records. In some cases, the query may still return records in API results even when **glide.invalid\_query.returns\_no\_rows** is set to true. This happens in queries where an invalid query term is used with a WHERE operator. In such queries, the WHERE operator ignores the invalid term\(s\) but still interprets and returns the rest of the query statement. For more information about this system property and its functionality, see [Available system properties](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

<table id="table_vy2_525_jq" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

query

</td><td>

String

</td><td>

An [encoded query string](https://www.servicenow.com/docs/access?context=c_EncodedQueryStrings&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US).

</td></tr><tr><td>

enforceFieldACL

</td><td>

Boolean

</td><td>

Optional. Flag that indicates whether to enforce field ACL \(Access Control List\) rules.Valid values:

-   true: Enforce field ACLs.
-   false: Don't enforce field ACLs.

Default: false

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

```
var queryString = "priority=1^ORpriority=2";
var now_GR = new GlideRecord('incident');
now_GR.addEncodedQuery(queryString);
now_GR.query();
while (now_GR.next()) {
  gs.addInfoMessage(now_GR.getValue('number'));
}
```

## Scoped GlideRecord - addFunction\(Object function\)

Applies a pre-defined GlideDBFunctionBuilder object to a record.

Use the GlideDBFunctionBuilder scoped class to define a function. After the function is defined, use the addFunction\(Object function\) method to apply the function to a record.

|Name|Type|Description|
|----|----|-----------|
|function|Object|GlideDBFunctionBuilder object that defines a SQL operation.|

|Type|Description|
|----|-----------|
|void| |

```
var functionBuilder = new GlideDBFunctionBuilder();
var myAddingFunction = functionBuilder.add();
myAddingFunction = functionBuilder.field('order');
myAddingFunction = functionBuilder.field('priority');
myAddingFunction = functionBuilder.build();

// Query incidents in which order + priority is less than 5 and display that added value
var now_GR = new GlideRecord('incident');
now_GR.addFunction(myAddingFunction);
now_GR.addQuery(myAddingFunction, '<', 5);
now_GR.query();
while(now_GR.next())
  gs.info(now_GR.getValue(myAddingFunction));
```

Output:

```
1
4
3
1
1
2
1
```

## Scoped GlideRecord – addJoinQuery\(String joinTable, String primaryField, String joinTableField\)

Adds a filter to return records based on a relationship in a table related to the current GlideRecord.

You can use this method to find all the users that are in the database group via the Group Member \[sys\_user\_grmember\] table, or to find all problems that have an assigned incident via the incident.problem\_id relationship.

This is not a true database join; rather, addJoinQuery\(\) adds a subquery. So, while the result set is limited based on the join, the only fields that you have access to are those on the base table \(those which are in the table with which the GlideRecord was initialized.\)

Always test queries on a sub-production instance prior to deploying them on a production instance. An incorrectly constructed encoded query, such as including an invalid field name, produces an invalid query. When the invalid query is run, the invalid part of the query condition is dropped, and the results are based on the valid part of the query, which may return all records from the table. Using an insert\(\), update\(\), deleteRecord\(\), or deleteMultiple\(\) method on bad query results can result in data loss.

You can set the **glide.invalid\_query.returns\_no\_rows** system property to true to have queries with invalid encoded queries return no records. In some cases, the query may still return records in API results even when **glide.invalid\_query.returns\_no\_rows** is set to true. This happens in queries where an invalid query term is used with a WHERE operator. In such queries, the WHERE operator ignores the invalid term\(s\) but still interprets and returns the rest of the query statement. For more information about this system property and its functionality, see [Available system properties](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

<table id="table_vy2_525_jq" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

joinTable

</td><td>

String

</td><td>

Name of table to use in the join, such as **'incident'**.

</td></tr><tr><td>

primaryField

</td><td>

String

</td><td>

Optional. Name of the field in the GlideRecord to use to join the field specified in the **joinTableField** parameter.Default: sys\_id

</td></tr><tr><td>

joinTableField

</td><td>

String

</td><td>

Optional. Name of the field in the table specified in **joinTable** to use to join the tables.Default: First field in the table specified in **joinTable** that is a reference field to the current GlideRecord table.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|GlideQueryCondition|Filter that lists records where the relationships match.|

Find problems that have an incident attached. This example returns problems that have associated incidents. However, it won't pull values from the incidents that are returned as a part of the query.

```
var prob = new GlideRecord('problem');
prob.addJoinQuery('incident');
prob.query();
```

Find inactive problems with associated incidents.

```
// Look for Problem records that have associated Incident records
var now_GR = new GlideRecord('problem');
var grSQ = now_GR.addJoinQuery('incident');
 
// Where the Problem records are "active=false"
now_GR.addQuery('active', 'false');
 
// And the Incident records are "active=true"
grSQ.addCondition('active', 'true');
 
// Query
now_GR.query();
 
// Iterate and output results
while (now_GR.next()) {
gs.info(now_GR.getValue('number'));
}
```

Find problems that have incidents associated where the incident **caller\_id** field value matches that of the problem **opened\_by** field.

```
var now_GR = new GlideRecord('problem'); 
        now_GR.addJoinQuery('incident', 'opened_by', 'caller_id'); 
        now_GR.query();
```

## Scoped GlideRecord - addNotNullQuery\(String fieldName\)

A filter that specifies records where the value of the field passed in the parameter is not null.

Always test queries on a sub-production instance prior to deploying them on a production instance. An incorrectly constructed encoded query, such as including an invalid field name, produces an invalid query. When the invalid query is run, the invalid part of the query condition is dropped, and the results are based on the valid part of the query, which may return all records from the table. Using an insert\(\), update\(\), deleteRecord\(\), or deleteMultiple\(\) method on bad query results can result in data loss.

You can set the **glide.invalid\_query.returns\_no\_rows** system property to true to have queries with invalid encoded queries return no records. In some cases, the query may still return records in API results even when **glide.invalid\_query.returns\_no\_rows** is set to true. This happens in queries where an invalid query term is used with a WHERE operator. In such queries, the WHERE operator ignores the invalid term\(s\) but still interprets and returns the rest of the query statement. For more information about this system property and its functionality, see [Available system properties](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

|Name|Type|Description|
|----|----|-----------|
|fieldName|String|The name of the field to be checked.|

|Type|Description|
|----|-----------|
|GlideQueryCondition|A filter that specifies records where the value of the field passed in the parameter is not null.|

```
var target = new GlideRecord('incident'); 
target.addNotNullQuery('short_description');
target.query();   // Issue the query to the database to get all records where short_description is not null
while (target.next()) {   
     // add code here to process the incident record
}
```

## Scoped GlideRecord - addNullQuery\(String fieldName\)

Adds a filter to return records where the value of the specified field is null.

Always test queries on a sub-production instance prior to deploying them on a production instance. An incorrectly constructed encoded query, such as including an invalid field name, produces an invalid query. When the invalid query is run, the invalid part of the query condition is dropped, and the results are based on the valid part of the query, which may return all records from the table. Using an insert\(\), update\(\), deleteRecord\(\), or deleteMultiple\(\) method on bad query results can result in data loss.

You can set the **glide.invalid\_query.returns\_no\_rows** system property to true to have queries with invalid encoded queries return no records. In some cases, the query may still return records in API results even when **glide.invalid\_query.returns\_no\_rows** is set to true. This happens in queries where an invalid query term is used with a WHERE operator. In such queries, the WHERE operator ignores the invalid term\(s\) but still interprets and returns the rest of the query statement. For more information about this system property and its functionality, see [Available system properties](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

|Name|Type|Description|
|----|----|-----------|
|fieldName|String|The name of the field to be checked.|

|Type|Description|
|----|-----------|
|GlideQueryCondition|The query condition added to the GlideRecord.|

```
var target = new GlideRecord('incident'); 
target.addNullQuery('short_description');
target.query();   // Issue the query to the database to get all records where short_description is null
while (target.next()) {   
   // add code here to process the incident record
}
```

## Scoped GlideRecord - addQuery\(String query\)

Adds a filter to return records using an encoded query string.

Always test queries on a sub-production instance prior to deploying them on a production instance. An incorrectly constructed encoded query, such as including an invalid field name, produces an invalid query. When the invalid query is run, the invalid part of the query condition is dropped, and the results are based on the valid part of the query, which may return all records from the table. Using an insert\(\), update\(\), deleteRecord\(\), or deleteMultiple\(\) method on bad query results can result in data loss.

You can set the **glide.invalid\_query.returns\_no\_rows** system property to true to have queries with invalid encoded queries return no records. In some cases, the query may still return records in API results even when **glide.invalid\_query.returns\_no\_rows** is set to true. This happens in queries where an invalid query term is used with a WHERE operator. In such queries, the WHERE operator ignores the invalid term\(s\) but still interprets and returns the rest of the query statement. For more information about this system property and its functionality, see [Available system properties](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

|Name|Type|Description|
|----|----|-----------|
|query|String|An [encoded query string](https://www.servicenow.com/docs/access?context=c_EncodedQueryStrings&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US) .|

|Type|Description|
|----|-----------|
|GlideQueryCondition|The query condition added to the GlideRecord.|

```
var rec = new GlideRecord('incident');
rec.addQuery('active=true');
rec.query();
while (rec.next()) {
  rec.setValue('active', false);
  gs.info('Active incident ' + rec.getValue('number') + ' closed');
  rec.update();
}
```

## Scoped GlideRecord - addQuery\(String name, Object value\)

Build a search query and return the rows that match the request.

If you are familiar with SQL, this method is similar to the "where" clause. One or more addQuery\(\) calls can be made in a single query; in this case the queries are AND'ed. If any of the query statements need to be OR'ed, use the GlideQueryCondition method [addOrCondition\(\)](../../glideQueryConditionScoped/concept/c_GlideQueryConditionScopedAPI.md#).

When addQuery\(\) is called with only two parameters, table name and comparison value, such as `myObj.addQuery('category','Hardware');`, the operator is assumed to be "equal to".

Always test queries on a sub-production instance prior to deploying them on a production instance. An incorrectly constructed encoded query, such as including an invalid field name, produces an invalid query. When the invalid query is run, the invalid part of the query condition is dropped, and the results are based on the valid part of the query, which may return all records from the table. Using an insert\(\), update\(\), deleteRecord\(\), or deleteMultiple\(\) method on bad query results can result in data loss.

You can set the **glide.invalid\_query.returns\_no\_rows** system property to true to have queries with invalid encoded queries return no records. In some cases, the query may still return records in API results even when **glide.invalid\_query.returns\_no\_rows** is set to true. This happens in queries where an invalid query term is used with a WHERE operator. In such queries, the WHERE operator ignores the invalid term\(s\) but still interprets and returns the rest of the query statement. For more information about this system property and its functionality, see [Available system properties](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

<table id="table_vy2_525_jq" class="parameters"><thead><tr><th>

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

Name of the table field to query, or one of the following reserved names:-   123TEXTQUERY321: Adds a string search term to the query. Specify the string you want to match as the value. Use this option to return records with field values containing the search string. This option searches against all fields in the table, which must be configured for indexing and search. For more information about configuring tables for indexing and search, see [Configure a single table for indexing and searching](https://www.servicenow.com/docs/access?context=configure-single-table-for-indexing&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).
-   123TEXTINDEXGROUP321: Adds a text index group to the query. Specify the name of the text index group from the Text Index Groups \[ts\_index\_group\] table you want to query as the value. Use this option to return search results from one of the tables in a text index group, with result relevancy scores normalized using that text index group's settings. For more information about configuring text index groups, see [Configure multiple tables for indexing and searching](https://www.servicenow.com/docs/access?context=index-multiple-tables&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

**Note:** For more details on the use of the reserved names, see [Querying tables in script](../../../../../script/server-scripting/concept/c_UsingGlideRecordToQueryTables.md#).

</td></tr><tr><td>

value

</td><td>

Object

</td><td>

Value on which to query \(not case-sensitive\).

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|GlideQueryCondition|Query condition added to the GlideRecord.|

This code example shows how to query the active records in the incident table and then set them all to inactive.

```
var rec = new GlideRecord('incident');
rec.addQuery('active', true);
rec.query();
while (rec.next()) {
  rec.setValue('active', false);
  rec.update();
}
```

This code example adds a query for records that match "email server" in the kb\_knowledge table, with search result relevancy values computed using settings from the portal text index group.

```
var now_GR = new GlideRecord("kb_knowledge);
now_GR.addQuery("123TEXTQUERY321", "email server");
now_GR.addQuery("123TEXTINDEXGROUP321", "portal");
now_GR.query();
```

## Scoped GlideRecord - addQuery\(String name, String operator, Object value\)

Provides the ability to build a request, which when executed, returns the rows from the specified table, that match the request.

If you are familiar with SQL, this method is similar to the "where" clause. One or more addQuery\(\) calls can be made in a single query; in this case the queries are AND'ed. If any of the query statements need to be OR'ed, use the GlideQueryCondition method [addOrCondition\(\)](../../glideQueryConditionScoped/concept/c_GlideQueryConditionScopedAPI.md#).

Always test queries on a sub-production instance prior to deploying them on a production instance. An incorrectly constructed encoded query, such as including an invalid field name, produces an invalid query. When the invalid query is run, the invalid part of the query condition is dropped, and the results are based on the valid part of the query, which may return all records from the table. Using an insert\(\), update\(\), deleteRecord\(\), or deleteMultiple\(\) method on bad query results can result in data loss.

You can set the **glide.invalid\_query.returns\_no\_rows** system property to true to have queries with invalid encoded queries return no records. In some cases, the query may still return records in API results even when **glide.invalid\_query.returns\_no\_rows** is set to true. This happens in queries where an invalid query term is used with a WHERE operator. In such queries, the WHERE operator ignores the invalid term\(s\) but still interprets and returns the rest of the query statement. For more information about this system property and its functionality, see [Available system properties](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

<table id="table_vy2_525_jq" class="parameters"><thead><tr><th>

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

Table field name.

</td></tr><tr><td>

operator

</td><td>

String

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

**Note:** Use CONTAINS instead of the LIKE operator.

</td></tr><tr><td>

value

</td><td>

Object

</td><td>

Value on which to query \(not case-sensitive\).

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|GlideQueryCondition|The query condition that was added to the GlideRecord.|

```
var rec = new GlideRecord('incident');
rec.addQuery('active',true);
rec.addQuery('sys_created_on', ">", "2010-01-19 04:05:00");
rec.query();
while (rec.next()) {
  rec.setValue('active', false);
  gs.info('Active incident ' + rec.getValue('number') + ' closed');
  rec.update();
}
```

Using the IN operator.

```
var now_GR = new GlideRecord('incident');
now_GR.addQuery('number','IN','INC00001,INC00002');
now_GR.query();
while(now_GR.next()) {
  //do something....
}
```

## Scoped GlideRecord - addValue\(String field, Number value\)

Provides atomic add and subtract operations on a specified number field at the database level for the current GlideRecord object.

Typically, a GlideRecord object is written as one record in a database. Individual field values are stored as defined. For code that adds a value to a GlideRecord field, it simply saves the field to the database with the new value, rather than atomically incrementing it.

For example, when the following code is executed, the value of the *u\_count* field in the database is 2.

```
gs.info(now_GR.u_count); // "1" 
now_GR.u_count += 1;
now_GR.update();
now_GR.get(now_GR.sys_id);
gs.info(now_GR.u_count); // "2"
```

If another user concurrently runs identical code, instead of the two operations each adding 1 to *u\_count*, the net effect is that *u\_count* only contains 2, with one operation's update actually being lost.

Conversely, the addValue\(\) method performs the addition/subtraction in the database when the record is updated as an atomic operation. Two operations running concurrently each properly update the field.

```
gs.info(now_GR.u_count); // "1" 
now_GR.addValue("u_count", 1); 
now_GR.update(); 
now_GR.get(now_GR.sys_id); // The record must be reloaded from the database to observe the result
gs.info(now_GR.u_count); // "3", if executed concurrently with another user 
```

**Note:** The new value is not read back from the database unless explicitly done so.

Like setValue\(\), addValue\(\) changes only take effect in the database after a subsequent call to update\(\) or insert\(\). If insert\(\) is called, the specified field is initialized with the **value** parameter passed into addValue\(\).

**Note:** If setValue\(\) is called for the specified field prior to calling addValue\(\), the addValue\(\) method is not processed and an error message is logged.

<table id="table_h43_tjt_hlb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

field

</td><td>

String

</td><td>

Name of the field in this GlideRecord to modify. **Note:** The associated field's data type must be an integer. This method doesn't support other data types such as longs.

</td></tr><tr><td>

value

</td><td>

Integer

</td><td>

Amount to add to the value when the record is saved. To perform a subtraction operation, simply pass a negative value.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

Shows a value being added.

```
gs.info(now_GR.u_count); // "1" 
now_GR.addValue("u_count", 1); 
now_GR.update(); 
now_GR.get(now_GR.sys_id); // The record must be reloaded from the database to observe the result
gs.info(now_GR.u_count);
```

Output:

```
2
```

Shows a value being subtracted.

```
gs.info(now_GR.u_count); // "4" 
now_GR.addValue("u_count", -1); 
now_GR.update(); 
now_GR.get(now_GR.sys_id); // The record must be reloaded from the database to observe the result
gs.info(now_GR.u_count);
```

Output:

```
3
```

## Scoped GlideRecord - applyEncodedQuery\(String queryString\)

Sets the values of the specified encoded query terms and applies them to the current GlideRecord.

|Name|Type|Description|
|----|----|-----------|
|queryString|String|Encoded query to apply to the current GlideRecord.|

|Type|Description|
|----|-----------|
|None| |

```
function createAcl(table, role) {
  gs.info("Checking security on table " + table);
  var now_GR = new GlideRecord("sys_security_acl");
  now_GR.addQuery("name", table);
  now_GR.addQuery("operation", "read");
  now_GR.query();
  var encQuery = now_GR.getEncodedQuery();
  if (now_GR.next()) {
  // existing acl found so use it
    createAclRole(now_GR.getValue('sys_id'), role);
    return;
  } else {
    now_GR.initialize();
    now_GR.applyEncodedQuery(encQuery);
    var acl = now_GR.insert();
    gs.info("Added read access control on " + table);
    createAclRole(acl, role);
  }
}
```

## Scoped GlideRecord - canCreate\(\)

Determines if the Access Control Rules, which include the user's roles, permit inserting new records in this table.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_g2l_vtb_2r" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the user's roles permit creating of records in this table.Valid values:

-   true: Creating permitted
-   false: Creating is not permitted

</td></tr></tbody>
</table>This code example writes whether the current user can create records in the Incident table in the system log.

```
var now_GR = new GlideRecord('incident');
gs.info(now_GR.canCreate());
```

## Scoped GlideRecord - canDelete\(\)

Determines if the Access Control Rules, which include the user's roles, permit deleting records in this table.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_pdw_ftb_2r" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the user's roles permit deleting of records in this table.Valid values:

-   true: Deleting permitted
-   false: Deleting is not permitted

</td></tr></tbody>
</table>This code example writes whether the current user can delete records in the Incident table in the system log.

```
var att = new GlideRecord('sys_attachment');
gs.info(att.canDelete());
```

## Scoped GlideRecord - canRead\(\)

Determines if the Access Control Rules \(ACLs\) permit reading records in this table. This method evaluates all ACL types, such as user roles, scripted ACLs, ACLs with scripted conditions, and so on.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_zmp_ttb_2r" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the user's roles permit reading of records in this table.Valid values:

-   true: Reading permitted
-   false: Reading is not permitted

</td></tr></tbody>
</table>This code example writes whether the current user can read records in the Incident table in the system log.

```
var now_GR = new GlideRecord('incident');
gs.info(now_GR.canRead());
```

## Scoped GlideRecord - canWrite\(\)

Determines if the Access Control Rules, which include the user's roles, permit editing records in this table.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_sq3_ttb_2r" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the user's roles permit writing of records in this table.Valid values:

-   true: Writing permitted
-   false: Writing is not permitted

</td></tr></tbody>
</table>This code example writes whether the current user can write records in the Incident table in the system log.

```
var now_GR = new GlideRecord('incident');
gs.info(now_GR.canWrite());
```

## Scoped GlideRecord - chooseWindow\(Number firstRow, Number lastRow, Boolean forceCount\)

Sets a range of rows to be returned by subsequent queries.

-   **Using setLimit\(\) with chooseWindow\(\)**

    The setLimit\(\) method implicitly calls the chooseWindow\(\) method and might cause unexpected results when used with chooseWindow\(\) in a query.

    -   If the chooseWindow\(\) method is called first, its record window is overwritten by the setLimit\(\) method.

        Using the following lines in a query returns 100 records starting at row 1:

        ```
        grIncident.chooseWindow(20,30);
        grIncident.setLimit(100);
        ```

    -   If the setLimit\(\) method is called first, the window set by chooseWindow\(\) is used and the limit is overwritten.

        Using the following lines in a query returns 10 records starting at row 21:

        ```
        grIncident.setLimit(5);
        grIncident.chooseWindow(20,30);
        ```

        **Note:** Running query\(\) with the chooseWindow\(\) method triggers a `COUNT(*)` query, which can result in slow performance on tables with a large number of records. You can use setLimit\(\) before chooseWindow\(\) to skip running the `COUNT(*)` query, but the same performance benefit is achievable using setNoCount\(\).


See also:

-   [query\(\)](c_GlideRecordScopedAPI.md#)
-   [setLimit\(\)](c_GlideRecordScopedAPI.md#)
-   [setNoCount\(\)](c_GlideRecordScopedAPI.md#)

<table id="table_vy2_525_jq" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

firstRow

</td><td>

Number

</td><td>

Zero-based index of the starting row for the range, inclusive. \(A value of 0 returns the first row.\)

</td></tr><tr><td>

lastRow

</td><td>

Number

</td><td>

Zero-based index of the ending row for the range, exclusive.For example, if **firstRow** = 1 and **lastRow** = 5, four records are returned \(2-5\).

</td></tr><tr><td>

forceCount

</td><td>

Boolean

</td><td>

Optional. Flag that indicates whether to force a row count query. In most implementations of this call, the row count is performed. There are some outlying cases, such as text searches, were a row count is not performed. Setting this flag ensures that the row count occurs.Valid values:

-   true: Row count always occurs.
-   false: Row count occurs if implemented in normal execution of method.

 Default: false

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

This example shows how to return records 3 and 4 from the Incident \[incident\] table.

```
var now_GR = new GlideRecord('incident');
now_GR.orderBy('number');
now_GR.chooseWindow(2, 4);
now_GR.query();
while (now_GR.next()) {
  gs.info(now_GR.getValue('number') + ' is within window');
}
```

Output:

```
*** Script: INC0000003 is within window
*** Script: INC0000004 is within window
```

## Scoped GlideRecord - deleteMultiple\(\)

Deletes all records that satisfy the query.

This method does not delete attachments.

Do not use deleteMultiple\(\) on tables with currency fields. Always delete each record individually. Also, do not use this method with the chooseWindow\(\) or setLimit\(\) methods when working with large tables. The setLimit\(\) method does not limit the number of records that are deleted with deleteMultiple\(\). All records returned by the query are deleted regardless of setLimit\(\).

The **glide.db.forced.chunk.threshold** system property sets the threshold above which forces chunk record deletions and updates. Chunking helps to prevent non-primary key deletions on huge tables from causing replication problems. For more information, see [Available system properties](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|None| |

This example shows how to delete all inactive records from the Incident table.

```
var now_GR = new GlideRecord('incident');
now_GR.addQuery('active','false');
now_GR.query();
now_GR.deleteMultiple();
```

## Scoped GlideRecord - deleteRecord\(\)

Deletes the current record.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_rrm_4tb_2r" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the record was successfully deleted.Valid values:

-   true: Record was deleted.
-   false: No record was found to delete.

</td></tr></tbody>
</table>This example shows how to delete a specified record from the Incident table.

```
var now_GR = new GlideRecord('incident');
//to delete one record
if (now_GR.get('99ebb4156fa831005be8883e6b3ee4b9'))
    now_GR.deleteRecord();
```

This example shows how to delete a record from the Incident table immediately after it is inserted. The incident GlideRecord must be reloaded after the insert before it can be deleted.

```
var grTicket = new GlideRecord('incident');
grTicket.initialize();
grTicket.short_description = 'Example ticket';
grTicket.work_notes = 'An update about the ticket';
var ins_sys_id = grTicket.insert(); // Insert the record
grTicket.get(ins_sys_id); // Reload the inserted record
gs.info(grTicket.deleteRecord()); // Delete the record
```

Output:

```
true
```

## Scoped GlideRecord - disableSysIdInOptimization\(\)

Disables the default optimization that prevents an extra database query from running when a user passes in a large number of sys\_ids, such as `grIncident.addQuery('sys_id', 'IN', listOf200SysIds)`.

This method only effects the GlideRecord on which it’s called. To modify the sys\_id limit optimization for all GlideRecords, adjust the value in the **glide.db.first\_pass\_sys\_id\_list\_size.max** system property \(default 100\).

If you don't either call this method or adjust the **glide.db.first\_pass\_sys\_id\_list\_size.max** system property and pass a list that contains more sys\_id entries than defined in **glide.db.first\_pass\_sys\_id\_list\_size.max**, the returned value from GlideRecord.getRowCount\(\) may be incorrect.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|None| |

The following code example shows how to use the disableSysIdInOptimiation\(\) method to disable the sys\_id limit optimization when passing an Incident sys\_id list that contains 200 entries.

```
var listOf200SysIds = [ ... ]; // 200 comma separated sys_ids
var grIncident = new GlideRecord('incident');
grIncident.addQuery('sys_id', 'IN', listOf200SysIds);
grIncident.disableSysIdInOptimization(); // Rowcount could be incorrect without this method call
grIncident.query();
if (grIncident.next())
    gs.info("Rowcount: " + grIncident.getRowCount());
```

Output:

```
Rowcount: 200
```

## Scoped GlideRecord - get\(Object name, Object value\)

Returns the specified record in the current GlideRecord object.

This method accepts either one or two parameters. If only a single parameter is passed in, the method assumes that it is the sys\_id of the desired record. If not found, it then tries to match the value against the display value. If two parameters are passed in, the first is the name of the column within the GlideRecord to search. The second is the value to search for. If multiple records are found, use next\(\) to access the additional records.

|Name|Type|Description|
|----|----|-----------|
|name|Object|Optional. Name of the instantiated GlideRecord column to search for the specified **value** parameter. If only a single parameter is passed in, the method assumes that this parameter is the sys\_id or display value.|
|value|Object|Value to match. For calculated fields, the value is matched as is rather than running a calculation on a scripted default value for a field in the record.|

<table id="table_qpt_3f5_jq" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Indicates whether the requested record was located:-   true: record was found
-   false: record was not found

</td></tr></tbody>
</table>This example shows how to obtain an incident record by passing in the sys\_id.

```
var grIncident = new GlideRecord('incident');
var returnValue = grIncident.get('99ebb4156fa831005be8883e6b3ee4b9');
gs.info(returnValue); // logs true or false
gs.info(grIncident.short_description); // logs Incident Short description
```

This example shows how to obtain an incident record by passing the field to search \(caller\_id.name\) and the value to match within that field.

```
var grIncident = new GlideRecord('incident');
var returnValue = grIncident.get('caller_id.name','Sylivia Wayland');
gs.info(returnValue); // logs true or false
gs.info(grIncident.getValue('number')); // logs Incident Number
```

## Scoped GlideRecord - getAttribute\(String fieldName\)

Returns the dictionary attributes for the specified field.

|Name|Type|Description|
|----|----|-----------|
|fieldName|String|Field name for which to return the dictionary attributes|

|Type|Description|
|----|-----------|
|String|Dictionary attributes|

```
doit();
function doit() {
  var now_GR = new GlideRecord('sys_user');
  now_GR.query("user_name","admin");
  if (now_GR.next()) {
    gs.info("we got one");
    gs.info(now_GR.location.getAttribute("tree_picker"));
  }
}
```

## Scoped GlideRecord - getClassDisplayValue\(\)

Returns the current table's label.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Label that identifies the table.|

This example prints the label of the passed in table.

```
// Display the incident table label
var now_GR = new GlideRecord("incident");
var value = now_GR.getClassDisplayValue();
gs.info("The table label is " + value + ".");
```

Output:

```
The table label is Incident.
```

## Scoped GlideRecord - getDisplayValue\(\)

Retrieves the display value for the current record.

Display values are manipulated based on the actual value in the database and user or system settings and preferences.

The display value that is returned is dependent on the field type.

-   Choice fields: The database value may be a number, but the display value will be more descriptive.
-   Date fields: The database value is in UTC format, while the display value is based on the user's time zone.
-   Encrypted text: The database value is encrypted, while the displayed value is unencrypted based on the user's encryption context.
-   Reference fields: The database value is sys\_id, but the display value is a display field of the referenced record.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Display value for the current record.|

This example writes the display value of a specified incident record into the log.

```
var now_GR = new GlideRecord('incident');
now_GR.get('sys_id','<sys_id>');
gs.info(now_GR.getDisplayValue());
```

Output:

```
INC0000050
```

## Scoped GlideRecord - getED\(\)

Returns the element's descriptor.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|GlideElementDescriptor|The element's descriptor.|

This example shows how to retrieve the name field for an incident GlideRecord.

```
var grInc = new GlideRecord('incident');
grInc.get('sys_id','ef43c6d40a0a0b5700c77f9bf387afe3');

var field = grInc.getElement('priority');
var ed = field.getED();

var isEdge = ed.getLabel();
gs.info("Label is - " + isEdge);
```

Output:

```
Label is - Priority
```

## Scoped GlideRecord - getElement\(String fieldName\)

Retrieves the GlideElement object for the specified field.

The value returned by this method is a complete GlideElement object. The results are the equivalent of dot-walking a field value. For example, `now_GR.getElement('short_description')` provides the same result as `nowGR.short_description`.

In most cases, don’t use dot-walking to get values from a record. Dot-walking retrieves the entire object instead of the field value. Retrieving the object uses more storage and might cause undesirable results when used in arrays or in Service Portal.

Instead of retrieving the entire object, you can use one of the following methods to copy the field values:

-   [getValue\(\)](c_GlideRecordScopedAPI.md#)
-   [getDisplayValue\(\)](c_GlideRecordScopedAPI.md#)

If dot-walking through a GlideElement object is necessary, use the toString\(\) method to retrieve values. For example, you might need the current caller's manager sys\_id to set another reference field. The following example shows how to get the string value instead of the entire object:

```
var mgr = current.caller_id.manager.toString();
```

See also:

-   [GlideElement – toString\(\)](../../glideElement/concept/c_GlideElementScopedAPI.md#)
-   [getElements\(\)](c_GlideRecordScopedAPI.md#)

|Name|Type|Description|
|----|----|-----------|
|fieldName|String|Column name for which to return the GlideElement object.|

|Type|Description|
|----|-----------|
|GlideElement|The GlideElement for the specified column of the current record. Each object describes a field in the current GlideRecord.|

The following example shows how to add a new incident record with details in the **Short Description** field.

```
var elementName = 'short_description'; 
var now_GR = new GlideRecord('incident'); 
now_GR.newRecord(); 
now_GR.setValue(elementName, "My DB is not working");
now_GR.insert();
 
var sdesc = now_GR.getElement('short_description');
gs.info(sdesc.getValue());
```

Output:

```
My DB is not working
```

## Scoped GlideRecord - getElements\(\)

Returns an array of GlideElement objects. Each object describes a field in the current GlideRecord.

If dot-walking through a GlideElement object is necessary, use the toString\(\) method to retrieve values. For example, you might need the current caller's manager sys\_id to set another reference field. The following example shows how to get the string value instead of the entire object:

```
var mgr = current.caller_id.manager.toString();
```

See also:

-   [GlideElement – toString\(\)](../../glideElement/concept/c_GlideElementScopedAPI.md#)
-   [getElement\(\)](c_GlideRecordScopedAPI.md#)

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Array|Array of [GlideElement](../../glideElement/concept/c_GlideElementScopedAPI.md#) objects. Each object describes a field in the current GlideRecord.|

The following example displays the value of the name field for the five most recent records created in the Question \[question\] table.

```
var now_GR = new GlideRecord('question');
var elementArr = now_GR.getElements();
now_GR.orderByDesc('sys_created_on');
now_GR.setLimit(5);
now_GR.query();

while (now_GR.next()){
  var qNames = now_GR.name.toString();
  elementArr.push(qNames);
  gs.info(qNames);
}
```

Output:

```
delivery_time_var
delivery_time
sequence
priority
assigned_group
```

## Scoped GlideRecord - getEncodedQuery\(\)

Retrieves the query condition of the current result set as an encoded query string.

For details, see [Encoded query strings](https://www.servicenow.com/docs/access?context=c_EncodedQueryStrings&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US).

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String| |

```
var now_GR = new GlideRecord('incident'); 
now_GR.addQuery('active', true);
now_GR.addQuery('priority', 1); 
now_GR.query(); 
var encodedQuery = now_GR.getEncodedQuery(); 
gs.info(encodedQuery);
```

Output:

```
active=true^priority=1
```

## Scoped GlideRecord - getLabel\(\)

Returns the field's label.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Field's label|

```
template.print("Summary of Requested items:\n");  
var now_GR = new GlideRecord("sc_req_item");
now_GR.addQuery("request", current.sysapproval);
now_GR.query();
while(now_GR.next()) {
var nicePrice = now_GR.price.toString();
  if (nicePrice != '') {
    nicePrice = parseFloat(nicePrice);
    nicePrice = nicePrice.toFixed(2);
  }
  template.print(now_GR.number + ":  " + now_GR.quantity + " X " + now_GR.cat_item.getDisplayValue() 
    + " at $" + nicePrice + " each \n");
  template.print("    Options:\n");
  for (key in now_GR.variables) {
  var now_V = now_GR.variables[key];
    if(now_V.getGlideObject().getQuestion().getLabel() != '') {
      template.space(4);
      template.print('     ' +  now_V.getGlideObject().getQuestion().getLabel() + " = " 
        + now_V.getDisplayValue() + "\n");  
    }
  }
}
```

## Scoped GlideRecord - getLastErrorMessage\(\)

Retrieves the last error message. If there is no last error message, null is returned.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The last error message as a string.|

```
// Setup a data policy where short_description field in incident is mandatory
var now_GR = new GlideRecord('incident');
now_GR.insert(); // insert without data in mandatory field
var errormessage = now_GR.getLastErrorMessage(); 
gs.info(errormessage);
```

Output:

```
Data Policy Exception: Short description is mandatory
```

## Scoped GlideRecord - getLink\(Boolean noStack\)

Retrieves the link to the current record.

<table id="table_vy2_525_jq" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

noStack

</td><td>

Boolean

</td><td>

Flag indicating whether to append the sysparm\_stack parameter to the returned link. This parameter specifies the page to visit after closing the current link. Valid values:

-   true: Do not attach the sysparm\_stack parameter.
-   false: Attach the sysparm\_stack parameter.

If true, the sysparm\_stack parameter is not appended to the link.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|String|Link to the current record.|

This example queries all Incident records with a priority of "1" and writes the servlet URI and the current record's link to the system log.

```
var now_GR = new GlideRecord('incident');
now_GR.addActiveQuery();
now_GR.addQuery("priority", 1);
now_GR.query();
now_GR.next();
gs.info(gs.getProperty('glide.servlet.uri') + now_GR.getLink(false));
```

Output:

```
https://instance.service-now.com/incident.do?sys_id=46e2fee9a9fe19810049b49dee0daf58&sysparm_stack=incident_list.do?sysparm_query=active=true
```

## Scoped GlideRecord - getRecordClassName\(\)

Retrieves the class name for the current record.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The class name.|

```
var now_GR = new GlideRecord('incident'); 
var recordClassName = now_GR.getRecordClassName(); 
gs.info(recordClassName);
```

Output:

```
incident
```

## Scoped GlideRecord - getRowCount\(\)

Retrieves the number of rows \(records\) in the current GlideRecord object.

**Note:** GlideRecord returns matching records, so it might not be as efficient as GlideAggregate when you only need the number of records. If you only need a record count and aren’t iterating over the matching records, use GlideAggregate.

-   **Retrieving the number of records in GlideRecord or GlideAggregate**

    The GlideRecord getRowCount\(\) and [GlideAggregate getAggregate\(\)](../../glideAggregateScoped/concept/c_GlideAggregateScopedAPI.md#) APIs offer similar information. Use the following criteria to determine which option is best for you.

    -   The GlideRecord getRowCount\(\) method tells you how many records have been returned from a query along with the records themselves. If you need the number of records in the result set before or after you iterate over the set to perform actions on the records, use this method.
    -   The GlideAggregate getAggregate\(\) method retrieves only a count of records matching the query, excluding the actual records. The aggregate must be set on the GlideAggregate object before issuing the query.
    Retrieving the records and count with GlideRecord getRowCount\(\)

    The following example shows how to get the total number of active incidents with GlideRecord getRowCount\(\):

    ```
    var incident = new GlideRecord("incident");
    incident.addQuery("active", true);
    incident.query();
     
    gs.info("*** Total number of active incidents: {0}", incident.getRowCount());
    ```

    Retrieving only the number of records with GlideAggregate getAggregate\(\)

    The following example shows how to return only the number of records. Because this method doesn’t use the matching records, it’s much more efficient to use an aggregate query and return just the count.

    ```
    var incident = new GlideAggregate("incident");
    incident.addQuery("active", true);
    incident.addAggregate("COUNT");
    incident.query();
     
    if (incident.next())
        gs.info("*** Total number of active incidents: {0}", incident.getAggregate("COUNT"));
    ```

    Deciding which option is best for your solution

    If you only want to retrieve the number of records, the GlideAggregate getAggregate\(\) method is the best option. To use the individual records and retrieve the number of results, use GlideRecord getRowCount\(\), because a single query provides this functionality.


**Note:** If you want to use the getRowCount\(\) method when using `sys_id IN` with more than 100 sys\_id values, such as `grIncident.addQuery('sys_id', 'IN', listOf200SysIds)`, you must either:

-   Call the disableSysIdInOptimization\(\) method on the GlideRecord.
-   Or, adjust the **glide.db.first\_pass\_sys\_id\_list\_size.max** system property to a value higher than the number of sys\_ids in the list.

In addition, ensure that you call the .next\(\) method before calling the getRowCount\(\) method.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Number|Number of rows in the current GlideRecord.|

The following example shows how to get the number of incidents from the Incident \[incident\] table.

```
var numberOfIncidents = new GlideRecord('incident');
numberOfIncidents.query();
gs.info("Records in incident table: " + numberOfIncidents.getRowCount());
```

Output:

```
Records in incident table: 6920
```

The following code example shows how to use the disableSysIdInOptimiation\(\) method to disable the sys\_id limit optimization when passing an Incident sys\_id list that contains 200 entries.

```
var listOf200SysIds = [ ... ]; // 200 comma separated sys_ids
var grIncident = new GlideRecord('incident');
grIncident.addQuery('sys_id', 'IN', listOf200SysIds);
grIncident.disableSysIdInOptimization(); // Rowcount could be incorrect without this method call
grIncident.query();
if (grIncident.next())
    gs.info("Rowcount: " + grIncident.getRowCount());
```

Output:

```
Rowcount: 200
```

## Scoped GlideRecord - getTableName\(\)

Retrieves the name of the table associated with the GlideRecord.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The table name|

```
var now_GR = new GlideRecord('incident');
gs.info(now_GR.getTableName());
```

## Scoped GlideRecord - getUniqueValue\(\)

Gets the primary key of the record, which is usually the sys\_id unless otherwise specified.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The unique primary key as a String, or null if the key is null.|

```
var now_GR = new GlideRecord('kb_knowledge');
now_GR.query();
now_GR.next();
var uniqueid = now_GR.getUniqueValue();
gs.info(uniqueid);
```

## Scoped GlideRecord - getValue\(String name\)

Retrieves the string value of an underlying element in a field.

**Note:** If the Field Encryption Enterprise plugin is enabled and the instance has access to the key, this method returns clear text values from encrypted fields. If the instance does not have access to the key, this method returns the encrypted value. For more information, see [Platform Encryption](https://www.servicenow.com/docs/access?context=now-platform-encryption&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

|Name|Type|Description|
|----|----|-----------|
|name|String|The name of the field to get the value from.|

|Type|Description|
|----|-----------|
|String|The string value of the underlying element. Returns null if the field is empty or the field does not exist. Boolean values return as `"0"` and `"1"` string values instead of false and true.|

```
var now_GR = new GlideRecord('incident'); 
now_GR.orderBy('number');
now_GR.query('active','true'); 
now_GR.next(); 
gs.info(now_GR.getValue('number'));
```

Output:

```
INC0000002
```

## Scoped GlideRecord - GlideRecord\(String tableName\)

Creates an instance of the GlideRecord class for the specified table.

|Name|Type|Description|
|----|----|-----------|
|tableName|String|The table to be used.|

```
var now_GR = new GlideRecord('incident');
```

## Scoped GlideRecord - hasNext\(\)

Determines if there are any more records in the GlideRecord object.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Boolean|True if there are more records in the query result set.|

```
var rec = new GlideRecord('incident'); 
rec.query(); 
if (rec.hasNext()) { 
  gs.info("Table is not empty"); 
}
```

## Scoped GlideRecord - insert\(\)

Inserts a new record using the field values that have been set for the current record.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Sys\_id of the inserted record, or null if the record is not inserted.|

```
var now_GR = new GlideRecord('incident');
now_GR.initialize();
now_GR.setValue('name', 'New Incident');
now_GR.setValue('description', 'Incident description');
now_GR.insert();
```

Output:

```
138fb4111b4d4d907cf30d03cd4bcb57
```

## Scoped GlideRecord - initialize\(\)

Creates an empty record suitable for population before an insert.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void| |

```
var grIncident = new GlideRecord('incident');
grIncident.initialize();
grIncident.setValue('short_description', 'New Incident');
grIncident.setValue('description', 'Incident description');
grIncident.insert();
```

## Scoped GlideRecord - isActionAborted\(\)

Checks to see if the current database action is to be aborted.

isActionAborted\(\) is initialized \(set to false\) for new threads and by the next\(\) method.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_hqg_mvt_vr" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates if the current database action is to be aborted.Valid values:

-   true: The current database action is to be aborted.
-   false: The current database action is not to be aborted.

</td></tr></tbody>
</table>```
var now_GR = new GlideRecord('incident');
 
gs.info(now_GR.isActionAborted());
```

Output:

```
false
```

## Scoped GlideRecord - isEncodedQueryValid\(String query\)

Verifies whether the specified encoded query is valid.

If the specified encoded query is valid, then the query is applied, just as if you had called [addEncodedQuery\(\)](c_GlideRecordScopedAPI.md#). If the specified encoded query is invalid, then `sys_idNotValidnull` is added as the encoded query.

**Note:** This method has been deprecated and replaced with the [isValidEncodedQuery\(\)](c_GlideRecordScopedAPI.md#) method which does not execute the query.

|Name|Type|Description|
|----|----|-----------|
|query|String|Encoded query to validate. See [Encoded query strings](https://www.servicenow.com/docs/access?context=c_EncodedQueryStrings&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US).|

<table id="table_obb_bv4_2gb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the specified encoded query is valid.-   true: Passed-in encoded query is valid.
-   false: Passed-in encoded query is not valid.

</td></tr></tbody>
</table>This code example shows how to validate an encoded query and then execute logic if the query is valid.

```
var now_GR = new GlideRecord('incident_sla');
var isValidQuery = now_GR.isEncodedQueryValid('inc_impact=1^taskslatable_active=true');
if (isValidQuery) {
  now_GR.query();
  .
  .
  .
}
```

## Scoped GlideRecord - isNewRecord\(\)

Checks if the current record is a new record that has not yet been inserted into the database.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Boolean|True if the record is new and has not been inserted into the database.|

```
var now_GR = new GlideRecord("x_app_table"); 
now_GR.newRecord(); // create a new record and populate it with default values
gs.info(now_GR.isNewRecord());
```

## Scoped GlideRecord - isValid\(\)

Determines if the current table is valid or if the record was successfully retrieved.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_qpt_3f5_jq" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates if the table is valid or if the record was successfully retrieved.Possible values:

-   true: Table is valid or the record was successfully retrieved.
-   false: Table is invalid or the record was not successfully retrieved.

</td></tr></tbody>
</table>```
var comment_GR = new GlideRecord('cf_comment');
var commentId = '99ebb4156fa831005be8883e6b3ee4b9';
comment_GR.get(commentId);
gs.info(comment_GR.isValid());
```

## Scoped GlideRecord - isValidEncodedQuery\(String query\)

Verifies whether the syntax of the encoded query is correct.

When passing an empty string \(`""`\) as the provide query:

-   The empty string \(`""`\) represents the absence of a query and returns false.
-   Calling `GlideRecord.addEncodedQuery("")` followed by `GlideRecord.query()` returns all rows. The query method is similar to a SQL SELECT statement. In SQL, when using "SELECT \* FROM foo WHERE X", the value X represents the query. If no query value is provided, all records are returned \(e.g., SELECT \* FROM foo\).

|Name|Type|Description|
|----|----|-----------|
|query|String|Encoded query to validate. See [Encoded query strings](https://www.servicenow.com/docs/access?context=c_EncodedQueryStrings&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US).|

<table id="table_vrg_zqs_j5b" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the specified encoded query is valid.-   true: Passed-in encoded query is valid.
-   false: Passed-in encoded query is not valid.

</td></tr></tbody>
</table>This code example shows how to check if the encoded query is valid.

```
var queryString = "priority=1^ORpriority=2";
var now_GR = new GlideRecord('incident');
var isValidQuery = now_GR.isValidEncodedQuery(queryString);
if (isValidQuery) {
  now_GR.addEncodedQuery(queryString);
  now_GR.query();
  .
  .
  .
}
```

## Scoped GlideRecord - isValidField\(String columnName\)

Determines if the specified field is defined in the current table.

|Name|Type|Description|
|----|----|-----------|
|columnName|String|The name of the field.|

|Type|Description|
|----|-----------|
|Boolean|True if the field is defined for the current table.|

```
var now_GR = new GlideRecord('incident'); 
now_GR.initialize(); 
gs.info(now_GR.isValidField("short_description"));
```

## Scoped GlideRecord - isValidRecord\(\)

Determines if a record was actually returned by the query/get record operation.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_qpt_3f5_jq" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether a record was actually returned by the query/get operation.Valid values:

-   true: Record returned by query/get operation.
-   false: End of record set, no record returned.

</td></tr></tbody>
</table>```
var rec = new GlideRecord('incident');
rec.query();
while (rec.next()) { 
  gs.info(rec.number + ' exists');
}
gs.info(rec.isValidRecord());
```

## Scoped GlideRecord - isView\(\)

Verifies whether the record was created in a view or a table.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_obb_bv4_2gb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the record was created in table that is a view.-   true: The record was created in a view.
-   false: The record was created in a table.

</td></tr></tbody>
</table>This code example shows how to determine if a GlideRecord was created in a view or a table.

```
var mySLA = new GlideRecord('incident_sla');

if (mySLA.isView() == true){
   gs.info('This record was created in a view.');
} else {
   gs.info('This record was created in a table.');
}
```

Output:

```
This record was created in a view.
```

## Scoped GlideRecord - newRecord\(\)

Creates a new GlideRecord record, sets the default values for the fields, and assigns a unique ID to the record.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void| |

```
var now_GR = new GlideRecord("x_app_table"); 
now_GR.newRecord(); 
gs.info(now_GR.isNewRecord());
```

Output:

```
true
```

## Scoped GlideRecord - next\(\)

Moves to the next record in the GlideRecord object.

**Note:** This method fails if there is a field in the table called "next". If that is the case, use the method [\_next\(\)](c_GlideRecordScopedAPI.md#).

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_qpt_3f5_jq" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates if there is a "next" record in the GlideRecord. Valid values:

-   true: Move to the next record was successful.
-   false: No more records in the result set.

</td></tr></tbody>
</table>```
var rec = new GlideRecord('incident');
rec.query();
while (rec.next()) {
 gs.info(rec.getValue('number') + ' exists');
}
```

Output:

```
INC0010112 exists
INC0010114 exists
INC0010119 exists
INC0010127 exists
```

## Scoped GlideRecord - \_next\(\)

Moves to the next record in the GlideRecord. Provides the same functionality as next\(\), use this method if the GlideRecord has a column named next.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_f3x_4yj_my" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether there are more records in the query set.Possible values:

-   true: More records in the query set.
-   false: No more records in the query set.

</td></tr></tbody>
</table>The following example shows how to list each record in the Incidents \[incident\] table.

```
var rec = new GlideRecord('incident');
rec.query();
while (rec._next()) {
  gs.info(rec.getValue('number') + ' exists');
}
```

Output:

```
INC0000060 exists
INC0009002 exists
INC0000009 exists
INC0000010 exists
INC0000011 exists
INC0000012 exists
...
```

## Scoped GlideRecord - operation\(\)

Determines if an operation is insert, update, or delete.

Knowing the operation enables using current.operation\(\) to make a generic business rule which can handle each operation uniquely.

For information on using the global variable current, refer to [Global variables in business rules](../../../../../script/business-rules/concept/c_BusinessRules.md#).

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="gr-operation-returns" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

The current operation.Possible values:

-   delete
-   insert
-   update

</td></tr></tbody>
</table>The following example shows how to use this method in a business rule. The operation\(\) method detects which operation triggered an event and performs a different action depending for update and insert operations.

```
if(current.operation() == "update") {
  current.updates ++; } 
if(current.operation() == "insert") {
  current.updates = 0; }
```

## Scoped GlideRecord - orderBy\(String name\)

Specifies an orderBy column.

Call this method more than once to order by multiple columns. Results are arranged in ascending order. To arrange records in descending order, see [Scoped GlideRecord - orderByDesc\(String name\)](c_GlideRecordScopedAPI.md#).

|Name|Type|Description|
|----|----|-----------|
|name|String|Column name to use to order the records in this GlideRecord object.|

|Type|Description|
|----|-----------|
|void| |

The following example shows how to order incident records in ascending order by Short Description.

```
var queryString = "priority=2";
var now_GR = new GlideRecord('incident');
now_GR.orderBy('short_description'); // Ascending Order
now_GR.addEncodedQuery(queryString);
now_GR.query();
while (now_GR.next()) {
  gs.info(now_GR.getValue('short_description'));
}
```

Output:

```
Can't launch 64-bit Windows 7 virtual machine
Can't log into SAP from my laptop today
Network storage unavailable
Please remove the latest hotfix from my PC
```

## Scoped GlideRecord - orderByDesc\(String name\)

Specifies a descending orderBy column.

Call this method more than once to order by multiple columns. Results are arranged in descending order. To arrange records in ascending order, see [Scoped GlideRecord - orderBy\(String name\)](c_GlideRecordScopedAPI.md#).

|Name|Type|Description|
|----|----|-----------|
|name|String|Column name to use to order the records in a GlideRecord object.|

|Type|Description|
|----|-----------|
|void| |

The following example shows how to order incident records in descending order by Short Description.

```
var queryString = "priority=2";
var now_GR = new GlideRecord('incident');
now_GR.orderByDesc('short_description'); //Descending Order
now_GR.addEncodedQuery(queryString);
now_GR.query();
while (now_GR.next()) {
  gs.info(now_GR.getValue('short_description'));
}
```

Output:

```
Please remove the latest hotfix from my PC
Network storage unavailable
Can't log into SAP from my laptop today
Can't launch 64-bit Windows 7 virtual machine
```

## Scoped GlideRecord - query\(String field, String value\)

Runs a query against the table based on the filters specified in the query methods such as addQuery\(\) and addEncodedQuery\(\).

This method queries the GlideRecord table as well as any references of the table. For more information, see [Querying tables in script](../../../../../script/server-scripting/concept/c_UsingGlideRecordToQueryTables.md#).

**Note:** This method fails if there is a field in the table called "query". If that is the case, use the[\_query\(\)](c_GlideRecordScopedAPI.md#) method instead.

See the [GlideRecord](https://developer.servicenow.com/dev.do#!/learn/courses/utah/app_store_learnv2_scripting_utah_scripting_in_servicenow/app_store_learnv2_scripting_utah_server_side_scripting/app_store_learnv2_scripting_utah_gliderecord) article for details on building and running queries.

See also:

-   [GlideAggregate - Scoped](../../glideAggregateScoped/concept/c_GlideAggregateScopedAPI.md#)
-   [GlideQuery - Scoped, Global](../../GlideQuery/concept/GlideQueryGlobalAPI.md#)
-   [GlideQueryCondition - Scoped](../../glideQueryConditionScoped/concept/c_GlideQueryConditionScopedAPI.md#)

<table id="id_nxt_s5d_lpb" class="parameters"><thead><tr><th>

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

Optional - must also specify a value parameter. Name of the field to search for the value specified in the value parameter.**Note:** This method is typically run without arguments, but you can specify a name-value pair to filter records containing the specified values. If the parameters are specified, the "name=value" condition is added to the query.

</td></tr><tr><td>

value

</td><td>

String

</td><td>

Optional - must also specify a field parameter. Value to search for in the specified field parameter.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

The following example shows how to scan the System Dictionary \[sys\_dictionary\] for tables with a query field.

```
var tableArr = [];

var now_GR = new GlideRecord('sys_dictionary');
now_GR.addQuery('element', 'query');
now_GR.setLimit(6);

now_GR.query();

while(now_GR.next()){
   tableArr.push(now_GR.name.getValue());
};

gs.info('The following tables have a field column called "query":');

for (i = 0; i < tableArr.length; i++) {
   gs.info(tableArr[i]);
};
```

Output:

```
The following tables have a field column called "query":
cmdb_convert_bulk_services
cmdb_multisource_query_status
cmdb_qb_result_base
cmdb_qb_table_mapping
discovery_probes_cim_query
kb_feedback
```

## Scoped GlideRecord - \_query\(String field, String value\)

Runs a query against the table based on the filters specified in the query methods such as addQuery\(\) and addEncodedQuery\(\). This method is intended to be used on tables in which there's a column named "query", which might cause errors running the query\(\) method.

This method queries the GlideRecord table as well as any references of the table. For more information, see [Querying tables in script](../../../../../script/server-scripting/concept/c_UsingGlideRecordToQueryTables.md#).

See the [GlideRecord](https://developer.servicenow.com/dev.do#!/learn/courses/utah/app_store_learnv2_scripting_utah_scripting_in_servicenow/app_store_learnv2_scripting_utah_server_side_scripting/app_store_learnv2_scripting_utah_gliderecord) article for details on building and running queries.

See also:

-   [GlideAggregate - Scoped](../../glideAggregateScoped/concept/c_GlideAggregateScopedAPI.md#)
-   [GlideQuery - Scoped, Global](../../GlideQuery/concept/GlideQueryGlobalAPI.md#)
-   [GlideQueryCondition - Scoped](../../glideQueryConditionScoped/concept/c_GlideQueryConditionScopedAPI.md#)

<table id="id_a3y_t5d_lpb" class="parameters"><thead><tr><th>

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

Optional - must also specify a value parameter. Name of the field to search for the value specified in the value parameter.**Note:** This method is typically run without arguments, but you can specify a name-value pair to filter records containing the specified values. If the parameters are specified, the "name=value" condition is added to the query.

</td></tr><tr><td>

value

</td><td>

String

</td><td>

Optional - must also specify a field parameter. Value to search for in the specified field parameter.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

The following example shows how query the Knowledge Feedback \[kb\_feedback\] table and list KB articles with comments that include Excel.

```
var rec = new GlideRecord('kb_feedback');
rec.addQuery('comments', 'CONTAINS', 'Excel');
rec._query();
while (rec.next()) { 
 gs.info(rec.getDisplayValue('article') + " comment: " + rec.getValue('comments'));
}
```

Output:

```
KB0000005 comment: 
	     Can you please add the version of Excel this applies to? All?
		
KB0000005 comment: 
	     Does this work for all Excel versions? OSX and Windows alike?
```

## Scoped GlideRecord - setAbortAction\(Boolean b\)

Sets a flag to indicate if the next database action \(insert, update, delete\) is to be aborted. This is often used in business rules.

Use in an `onBefore` business rule to prevent the database action from being done. The business rule continues to run after setAbortAction\(\) is called. Calling setAbortAction\(\) does not stop subsequent business rules from executing. Calling this method only prevents the database action from occurring.

|Name|Type|Description|
|----|----|-----------|
|b|Boolean|True to abort the next action. False if the action is to be allowed.|

|Type|Description|
|----|-----------|
|void| |

```
// Often used in business rule to check whether the current operation should be aborted.
if (current.size > 16) {
  current.setAbortAction(true);
}
```

## Scoped GlideRecord - setLimit\(Number maxNumRecords\)

Sets the limit for number of records are fetched by the GlideRecord query.

-   **Using setLimit\(\) with chooseWindow\(\)**

    The setLimit\(\) method implicitly calls the chooseWindow\(\) method and might cause unexpected results when used with chooseWindow\(\) in a query.

    -   If the chooseWindow\(\) method is called first, its record window is overwritten by the setLimit\(\) method.

        Using the following lines in a query returns 100 records starting at row 1:

        ```
        grIncident.chooseWindow(20,30);
        grIncident.setLimit(100);
        ```

    -   If the setLimit\(\) method is called first, the window set by chooseWindow\(\) is used and the limit is overwritten.

        Using the following lines in a query returns 10 records starting at row 21:

        ```
        grIncident.setLimit(5);
        grIncident.chooseWindow(20,30);
        ```

        **Note:** Running query\(\) with the chooseWindow\(\) method triggers a `COUNT(*)` query, which can result in slow performance on tables with a large number of records. You can use setLimit\(\) before chooseWindow\(\) to skip running the `COUNT(*)` query, but the same performance benefit is achievable using setNoCount\(\).


See also:

-   [chooseWindow\(\)](c_GlideRecordScopedAPI.md#)
-   [query\(\)](c_GlideRecordScopedAPI.md#)
-   [setNoCount\(\)](c_GlideRecordScopedAPI.md#)

|Name|Type|Description|
|----|----|-----------|
|maxNumRecords|Number|The maximum number of records to fetch.|

|Type|Description|
|----|-----------|
|void| |

```
var now_GR = new GlideRecord('incident');
now_GR.orderByDesc('sys_created_on');
now_GR.setLimit(10);
now_GR.query(); // this retrieves latest 10 incident records created
```

## Scoped GlideRecord - setNewGuidValue\(String guid\)

Sets the sys\_id value for the current record.

|Name|Type|Description|
|----|----|-----------|
|guid|String|GUID to assign to the current record.|

|Type|Description|
|----|-----------|
|void| |

```
var now_GR = new GlideRecord('incident');
now_GR.setValue('short_description', 'The third floor printer is broken');
now_GR.setNewGuidValue('eb4636ca6f6d31005be8883e6b3ee333');
now_GR.insert();
gs.info(now_GR.getValue('sys_id'));
```

## Scoped GlideRecord - setNoCount\(\)

Stops a GlideRecord query from running a `COUNT(*)` query.

Running query\(\) with some methods trigger a `COUNT(*)` query, such as the chooseWindow\(\) and getRowCount\(\) methods. The `COUNT(*)` query might cause slow performance on tables with a million or more records. For more information, see the [Performance Improvement - Remove Pagination Count \[KB0817996\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0817996) article in the Now Support Knowledge Base.

**Note:** The setLimit\(\) method also stops a `COUNT(*)`. Using setNoCount\(\) is unnecessary if the setLimit\(\) method is included in the query.

See also:

-   [chooseWindow\(\)](c_GlideRecordScopedAPI.md#)
-   [query\(\)](c_GlideRecordScopedAPI.md#)

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void| |

The following code example shows how to use setNoCount\(\) to skip the `COUNT(*)` query on a windowed query set using the chooseWindow\(\) method.

```
var  grIncident = new GlideRecord('incident');

grIncident.chooseWindow(6915, 6920, true);
grIncident.setNoCount();
grIncident.query();

while (grIncident.next()) { // Iterate through the returned records
    gs.info('Incident Number: ' + grIncident.number + ', Short Description: ' + grIncident.short_description);
};
```

Output:

```
Incident Number: INC0006811, Short Description: Request an account to be created for Fidelity 401(k) Plans
Incident Number: INC0006918, Short Description: Please grant me additional roles in Oracle Fin Collections
Incident Number: INC0006812, Short Description: Taxware Value-added Tax crashes when I try to launch it
Incident Number: INC0006919, Short Description: Unable to Access SuccessFactors Learning
Incident Number: INC0010004, Short Description: Incident for assessment not generating
```

## Scoped GlideRecord - setValue\(String name, Object value\)

Sets the value of the field with the specified name to the specified value.

Normally the script does a `now_GR.category = value`. However, if the element name is itself a variable then you can use `now_GR.setValue(elementName, value)`. When setting a value, ensure the data type of the field matches the data type of the value you enter.

**Note:** If the Field Encryption Enterprise plugin is enabled and the instance has access to the key, this method can insert encrypted data into encrypted fields. If the instance does not have access to the key, this method returns an error. For more information, see [Platform Encryption](https://www.servicenow.com/docs/access?context=now-platform-encryption&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

-   **Not for authentication with password2 fields**

    The setValue\(\) method passes password2 data as clear text, which results in an error about expecting encrypted data. Additionally, using the setValue\(\) method for password2 fields exposes data that should be encrypted.

    For password2 authentication, use the setDisplayValue\(\) method instead.

    See also:

    -   [Deprecate GlideEncrypter usage of 3DES for password2 fields](https://www.servicenow.com/docs/access?context=password2-3des-deprecation&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US)
    -   [Alternatives to GlideEncrypter usage in knowledge base article KB1320986](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1320986)
    -   [Password2 encryption with the Key Management Framework \(KMF\)](https://www.servicenow.com/docs/access?context=password-2way-encrypted-fields&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US)

|Name|Type|Description|
|----|----|-----------|
|name|String|Name of the field.|
|value|Object|Value to assign to the field.|

|Type|Description|
|----|-----------|
|None| |

```
var elementName = 'short_description'; 
var now_GR = new GlideRecord('incident'); 
now_GR.initialize(); 
now_GR.setValue(elementName, "My DB is not working");
now_GR.insert();
```

## Scoped GlideRecord - setWorkflow\(Boolean enable\)

Enables or disables the running of business rules, script engines, and audit.

**Warning:** Disabling the running of business rules, script engines, and audit can have a significant impact on your ServiceNow® instance and how it operates. Ensure that you thoroughly test this change before deploying it to production.

**Note:** This method can't be set for cross scoped applications. For additional information, see the following KB article [https://support.servicenow.com/kb?id=kb\_article\_view&amp;sysparm\_article=KB0820691](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0820691).

<table id="table_vy2_525_jq" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

enable

</td><td>

Boolean

</td><td>

Flag that indicates whether to enable or disable the running of business rules, script engines, and audit.Valid values:

-   true: Enable the running of business rules, script engines, and audit.
-   false: Disable the running of business rules, script engines, and audit.

Default: true

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

```
//Enable business rules, scripts engines for x_app_table
var now_GR = new GlideRecord("x_app_table"); 
now_GR.setWorkflow(true);
```

## Scoped GlideRecord - update\(String reason\)

Updates the GlideRecord with any changes that have been made. If the record does not already exist, it is inserted.

|Name|Type|Description|
|----|----|-----------|
|reason|String|Optional. Reason for the update. The reason appears in the audit record.|

|Type|Description|
|----|-----------|
|String|Sys\_id of the new or updated record. Returns null if the update fails.|

The following example shows how to update the Short Description field of an incident.

```
var now_GR = new GlideRecord('incident');
now_GR.get('99ebb4156fa831005be8883e6b3ee4b9');
now_GR.setValue('short_description', 'Update the short description');
now_GR.update();
gs.info(now_GR.getElement('short_description'));
```

Output:

```
Update the short description.
```

## Scoped GlideRecord - updateMultiple\(\)

Updates each GlideRecord in a stated query with a specified set of changes.

This method does not support adding multiple journal entries.

The **glide.db.forced.chunk.threshold** system property sets the threshold above which forces chunk record deletions and updates. Chunking helps to prevent non-primary key deletions on huge tables from causing replication problems. For more information, see [Available system properties](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

**Note:** To ensure expected results, use the setValue\(\) method instead of direct assignments. That is, use `gr_Now.setValue('<field_name>', '4'));` instead of `gr_Now.<field_name> = 4`.

**Note:** Do not use this method with the chooseWindow\(\) or setLimit\(\) methods when working with large tables.

This method sets new values and does not clear existing values. To clear an existing value, use the setValue\(\) method and set the field to 'NULL'. For more information, see [Setting a GlideRecord variable to 'NULL'](../../../../../script/server-scripting/reference/r_SettingAGlideRecordVariableToNull.md).

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|None| |

This example shows how to update the state of all active incidents to 4 - "Awaiting User Info".

```
var now_GR = new GlideRecord('incident');
now_GR.addQuery('active', true);
now_GR.setValue('state',  4);
now_GR.updateMultiple();
```

This example shows how to clear existing values of the description field for priority 1 incidents.

```
var test = new GlideRecord('incident');
test.addEncodedQuery('priority=1');
test.query();
 
test.setValue('description','NULL');
test.updateMultiple();
```

## Scoped GlideRecord - updateWithReferences\(Object reason\)

Updates a record and also inserts or updates any related records with the information provided.

|Name|Type|Description|
|----|----|-----------|
|reason|Object|Reason for the updates. The reason is displayed in the audit record.|

|Type|Description|
|----|-----------|
|String|The sys\_id for the record being updated.|

If processing an incident where the Caller ID is set to reference sys\_user record 'John Doe,' then the following code would update John Doe's user record. If processing an incident where there's no caller ID specified, then the following code creates a new sys\_user record with the provided information \(first\_name, last\_name\) and sets the caller ID value to the newly created sys\_user record.

```
var inc = new GlideRecord('incident');
inc.get(inc_sys_id);  // Looking up an existing incident record where 'inc_sys_id' represents the sys_id of a incident record
inc.caller_id.first_name = 'John';
inc.caller_id.last_name = 'Doe';
inc.updateWithReferences();
}
```

