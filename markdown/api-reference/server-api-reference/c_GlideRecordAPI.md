---
title: GlideRecord - Global
description: The GlideRecord API is used for database operations.Creates an instance of the GlideRecord class for the specified table.Adds a filter to return active records.Changes the domain used for the query from the user's domain to the domain of the provided GlideRecord.Adds an encoded query to other queries that may have been set.Queries one or more dot-walked fields from a form or script in a single request.Applies a pre-defined GlideDBFunctionBuilder object to a record.Adds a filter to return inactive records. Inactive records have the active flag set to false.Adds a filter to return records based on a relationship in a related table.Adds a filter to return records based on a relationship in a related table.Adds a filter to return records based on a relationship in a related table.Adds a filter to return records where the specified field is not null.Adds a filter to return records where the specified field is null.Provides the ability to build a request, which when executed, returns the rows from the specified table that match the request.Provides atomic add and subtract operations on a specified number field at the database level for the current GlideRecord object.Sets the values of the specified encoded query terms and applies them to the current GlideRecord.Apply a template record from the Template table \[sys\_template\] to the current record. If the specified template is not found, no action is taken.Enables or disables the update to the fields sys\_updated\_by, sys\_updated\_on, sys\_mod\_count, sys\_created\_by, and sys\_created\_on. This is often used for manually updating field values on a record while leaving historical information unchanged.Determines if the access control rules \(which includes the user's role\) permit inserting new records in this table.Determines if the access control rules \(which includes the user's role\) permit deletion of records in this table.Indicates whether the Access Control Rules \(ACLs\) permit the current user to read the current record within the associated GlideRecord table. This method evaluates all available ACLs for the specific resource.Determines if the access control rules \(which includes the user's role\) permit updates to records in this table.Determines whether any of the fields in the record have changed.Sets a range of rows to be returned by subsequent queries.Deletes all records that satisfy the query.Deletes a single record.Disables the default optimization that prevents an extra database query from running when a user passes in a large number of sys\_ids, such as grIncident.addQuery\('sys\_id', 'IN', listOf200SysIds\). Returns true if any record has a matching value in the specified column. If found, it also moves to the first record that matches, essentially executing next\(\) until the record is returned.Returns the specified record in the current GlideRecord object.Returns the dictionary attributes on the specified field.Returns the table's label.Retrieves the display value for the current record or the display value of an attribute in a dynamic attribute store.Returns the GlideElementDynamicAttribute object for the specified dynamic attribute store path.Returns a GlideElementDynamicAttribute object that contains the dynamic attribute located at the specified table field and attribute path.Returns the value of the dynamic attribute located at a specified path.Returns the value of the dynamic attribute located at a specified field in the current table and a specified attribute path.Returns the display value of the dynamic attribute located at the specified path.Returns the display value of the dynamic attribute located in a specified table field and attribute path.Returns the element's descriptor.Retrieves the GlideElement for a specified field.Retrieves the query condition of the current result set as an encoded query string.Retrieves the field value for the display field of the current record and adds escape characters for use in Jelly scripts.Retrieves a Java ArrayList of fields in the current record.Retrieves the field's label.Retrieves the link for the current record.Retrieves the row number of the current record within the table.Retrieves the plural label of the GlideRecord table.Retrieves the class \(table\) name for the current record.Retrieves a list of names and display values of related lists associated with the current GlideRecord.Retrieves a list of names and display values of tables that are referred to by the current record.Retrieves the number of rows \(records\) in the current GlideRecord object.Retrieves the row number set by saveLocation\(\) or setLocation\(\).Retrieves the table name associated with this GlideRecord.Gets the primary key of the record, which is usually the sys\_id unless otherwise specified.Retrieves the string value of a specified field or the string value of an attribute in a dynamic attribute store.Determines if the current GlideRecord has any attachments.Determines if there are any more records in the GlideRecord.Creates an empty record within the current GlideRecord that is suitable for population before an insert.Inserts a new record with the field values that have been set for the current record.Inserts a new record and also inserts or updates any related records with the provided information.Checks a table for the type\\class of table.Determines whether the current record has been inserted into the database.Determines if the current GlideRecord table exists.Determines if the specified field is defined in the current GlideRecord table.Determines if the current record is valid.Creates a GlideRecord, sets the default values for the fields, and assigns a unique ID to the record.Moves to the next record in the GlideRecord.Moves to the next record in the GlideRecord. Provides the same functionality as next\(\), intended to be used in cases where the GlideRecord has a column named next.Determines if an operation is insert, update, or delete.Specifies a field name, or path to an attribute within a dynamic attribute store, to use to order the query set. To order by multiple fields, call this method multiple times with different field values.Specifies the field, or an attribute in a dynamic attribute store, to use to order the query set in descending order.Runs a query against the table based on the filters specified in the query methods such as addQuery\(\) and addEncodedQuery\(\).Runs a query against the table based on the filters specified in the query methods such as addQuery\(\) and addEncodedQuery\(\). This method is intended to be used on tables in which there's a column named "query", which might cause errors running the query\(\) method.Used in domain-separated instances. Similar to query\(\), runs the query against the table based on the filters specified by addQuery\(\) and addEncodedQuery\(\), but ignores domains.Sets the current record to be the record that was saved with saveLocation\(\). If saveLocation\(\) has not been called, the current record is set to the first record of the GlideRecord.Saves the current row number so you can return to this location using the restoreLocation\(\) method.Sets a flag to indicate if the next database action \(insert, update, delete\) is to be aborted.Sets a specified field, or an attribute in a dynamic attribute store, to a specified display value.Sets the value of the dynamic attribute located at a specified path.Sets the value of the dynamic attribute located in a specified field of the current GlideRecord and a specified attribute path.Sets the display value of the dynamic attribute located at a specified path.Sets the display value of the dynamic attribute located in a specified field of the current GlideRecord and a specified attribute path.Sets one or more dynamic attribute values with values specified in the passed GlideDynamicAttributeStore object.Updates the record even if fields have not changed.Sets the maximum number of records to return in the GlideRecord from a query.Sets the current row location to the specified value.Generates a new GUID and sets it as the unique ID \(sys\_id\) for the current record.Generates a new GUID and sets it as the unique ID for the current record, when inserting a new record.Stops a GlideRecord query from running a COUNT\(\*\) query.Enables or disables using the reference field's display name when querying a reference field.Disables or enables the running of any engines \(approval rules / assignment rules\).Sets the specified field, or an attribute in a dynamic attribute store, to a specified value.Enables or disables the running of business rules that might normally be triggered by subsequent actions. If the e parameter is set to false, an insert/update will not be audited. Auditing only happens when the parameter is set to true for a GlideRecord operation.Updates the GlideRecord with any changes that have been made. If the record does not exist, it is inserted.Updates each GlideRecord in a stated query with a specified set of changes.Updates a record and also inserts or updates any related records with the information provided.
locale: en-US
release: xanadu
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 95
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# GlideRecord- Global

The GlideRecord API is used for database operations.

The GlideRecord API is the primary means of interfacing with the database on the server-side code. A GlideRecord is an object that contains records from a single table. Use the API to instantiate a GlideRecord object and add query parameters, filters, limits, and ordering.

To use this API to create dynamic attributes you must have the dynamic\_schema\_writer role. To read dynamic data using this API you must have the dynamic\_schema\_reader role.

For more information on dynamic attributes, see [Dynamic Schema](https://www.servicenow.com/docs/access?context=dynamic-schema&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

See the [GlideRecord](https://developer.servicenow.com/dev.do#!/learn/courses/utah/app_store_learnv2_scripting_utah_scripting_in_servicenow/app_store_learnv2_scripting_utah_server_side_scripting/app_store_learnv2_scripting_utah_gliderecord) article for details on building and running queries.

For information about GlideRecordSecure, which is a class inherited from GlideRecord that performs the same functions as GlideRecord and also enforces ACLs, see the [GlideServer APIs](https://www.servicenow.com/docs/access?context=p_GlideServerAPIs&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US).

Always test queries on a sub-production instance prior to deploying them on a production instance. An incorrectly constructed encoded query, such as including an invalid field name, produces an invalid query. When the invalid query is run, the invalid part of the query condition is dropped, and the results are based on the valid part of the query, which may return all records from the table. Using an insert\(\), update\(\), deleteRecord\(\), or deleteMultiple\(\) method on bad query results can result in data loss.

You can set the **glide.invalid\_query.returns\_no\_rows** system property to true to have queries with invalid encoded queries return no records. In some cases, the query may still return records in API results even when **glide.invalid\_query.returns\_no\_rows** is set to true. This happens in queries where an invalid query term is used with a WHERE operator. In such queries, the WHERE operator ignores the invalid term\(s\) but still interprets and returns the rest of the query statement. For more information about this system property and its functionality, see [Available system properties](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

## Retrieve values from records

In most cases, don’t use dot-walking to get values from a record. Dot-walking retrieves the entire object instead of the field value. Retrieving the object uses more storage and might cause undesirable results when used in arrays or in Service Portal.

Instead of retrieving the entire object, you can use one of the following methods to copy the field values:

-   [getValue\(\)](c_GlideRecordAPI.md#)
-   [getDisplayValue\(\)](c_GlideRecordAPI.md#)

If dot-walking through a GlideElement object is necessary, use the toString\(\) method to retrieve values. For example, you might need the current caller's manager sys\_id to set another reference field. The following example shows how to get the string value instead of the entire object:

```
var mgr = current.caller_id.manager.toString();
```

## Dynamic attributes

There are methods in this API that have the same functionality as dynamic schema methods in the [GlideDynamicAttributeStore - Global](../../GlideDynamicAttributeStore/concept/GlideDynamicAttStoreAPI.md#) API. Use the dynamic attribute methods in this API to perform actions on a specified GlideRecord. Use the methods in the GlideDynamicAttributeStore API if you want to set the same group of dynamic attributes on multiple records. Using this API, you can stage a GlideDynamicAttributeStore object with the desired attributes and then copy that object to multiple GlideRecords using the various setDynamicAttributeValues\(\) methods.

See also:

-   [GlideAggregate](../../GlideAggregate/concept/c_GlideAggregateAPI.md#)
-   [GlideElement](../../GlideElement_global/concept/c_GlideElementAPI.md#)
-   [GlideQuery](../../GlideQuery/concept/GlideQueryGlobalAPI.md#)

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## GlideRecord - GlideRecord\(String tableName\)

Creates an instance of the GlideRecord class for the specified table.

|Name|Type|Description|
|----|----|-----------|
|tableName|String|Table to use.|

```
var now_GR = new GlideRecord('incident');
```

## GlideRecord - addActiveQuery\(\)

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

### Scoped equivalent

To use the addActiveQuery\(\) method in a scoped application, use the corresponding scoped method: [addActiveQuery\(\)](../../glideRecordScoped/concept/c_GlideRecordScopedAPI.md#).

## GlideRecord - addDomainQuery\(Object glideRecord\)

Changes the domain used for the query from the user's domain to the domain of the provided GlideRecord.

Always test queries on a sub-production instance prior to deploying them on a production instance. An incorrectly constructed encoded query, such as including an invalid field name, produces an invalid query. When the invalid query is run, the invalid part of the query condition is dropped, and the results are based on the valid part of the query, which may return all records from the table. Using an insert\(\), update\(\), deleteRecord\(\), or deleteMultiple\(\) method on bad query results can result in data loss.

You can set the **glide.invalid\_query.returns\_no\_rows** system property to true to have queries with invalid encoded queries return no records. In some cases, the query may still return records in API results even when **glide.invalid\_query.returns\_no\_rows** is set to true. This happens in queries where an invalid query term is used with a WHERE operator. In such queries, the WHERE operator ignores the invalid term\(s\) but still interprets and returns the rest of the query statement. For more information about this system property and its functionality, see [Available system properties](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

This function requires the Domain Support - Domain Extensions Installer \(com.glide.domain.msp\_extensions.installer\) plugin.

|Name|Type|Description|
|----|----|-----------|
|glideRecord|Object|GlideRecord from which to obtain the domain.|

|Type|Description|
|----|-----------|
|void| |

```
//This example requires the Domain plugin be active, the Group table is the specified 
//Domain table, and the ITIL user is in the Database Atlanta domain
//From any domain (using queryNoDomain()) look up the incidents that an ITIL user can only see 
//who is in the Database Atlanta domain, should expect all incidents with the global or the
//Database Atlanta domain specified.
var domain = new GlideRecord('sys_user');
domain.addQuery('user_name', 'itil');
domain.queryNoDomain();
if (domain.next()) {
    var domainQuery = new GlideRecord('incident');
    domainQuery.addQuery('active', true);
    domainQuery.addDomainQuery(domain);
    domainQuery.query();
    gs.print('Number of Incidents for ITIL user: ' + domainQuery.getRowCount());
    while (domainQuery.next())
        gs.print(domainQuery.number);
}
```

### Scoped equivalent

This method is not available in scoped applications.

## GlideRecord - addEncodedQuery\(String query, Boolean enforceFieldACL\)

Adds an encoded query to other queries that may have been set.

Always test queries on a sub-production instance prior to deploying them on a production instance. An incorrectly constructed encoded query, such as including an invalid field name, produces an invalid query. When the invalid query is run, the invalid part of the query condition is dropped, and the results are based on the valid part of the query, which may return all records from the table. Using an insert\(\), update\(\), deleteRecord\(\), or deleteMultiple\(\) method on bad query results can result in data loss.

You can set the **glide.invalid\_query.returns\_no\_rows** system property to true to have queries with invalid encoded queries return no records. In some cases, the query may still return records in API results even when **glide.invalid\_query.returns\_no\_rows** is set to true. This happens in queries where an invalid query term is used with a WHERE operator. In such queries, the WHERE operator ignores the invalid term\(s\) but still interprets and returns the rest of the query statement. For more information about this system property and its functionality, see [Available system properties](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

<table id="table_j3p_mlp_dt" class="parameters"><thead><tr><th>

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

An [encoded query string](https://www.servicenow.com/docs/access?context=c_EncodedQueryStrings&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).

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
 gs.addInfoMessage(now_GR.number);
 }
```

### Scoped equivalent

To use the addEncodedQuery\(\) method in a scoped application, use the corresponding scoped method: [addEncodedQuery\(\)](../../glideRecordScoped/concept/c_GlideRecordScopedAPI.md#).

## GlideRecord - addExtraField\(String dotWalkedField\)

Queries one or more dot-walked fields from a form or script in a single request.

The addExtraField\(\) method allows you to query dot-walked fields in a single database request, rather than perform multiple queries per dot-walked element in a form or script \(which requires multiple round trips to the database\).

<table id="table_ctk_qcx_hzb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

dotWalkedField

</td><td>

String

</td><td>

The dot-walked field name. Levels of field names are separated by dots \(periods\). For example, enter the value `Caller.Company` if you want to query the **Company** &gt; **Caller** condition in the Incident \[incident\] table.The format of **dotWalkedField** follows the left-to-right order of fields in a dotwalked form or script.

</td></tr></tbody>
</table><table id="table_dtk_qcx_hzb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

None

</td><td>

**Note:** The addExtraField\(\) method does not impact output results; the output is always the same regardless if you use this method in your script.

</td></tr></tbody>
</table>The following example shows how to query the contact name field of cmn\_location \(referenced from the “location” reference field in a cmdb\_ci field\).

**Note:** The dotWalkedField value in this example, `cmdb_ci.location.contact.name`, looks like “cmdb\_ci fields” =&gt; “cmn\_location fields” =&gt; “sys\_user fields” in the ServiceNow® UI when selecting fields in a list.

```
var gliderecord = new GlideRecord("incident");
gliderecord.addQuery("number", "INC0041457");
gliderecord.addExtraField("cmdb_ci.location.contact.name");
gliderecord.query();
gliderecord.next();
gs.print(gliderecord.cmdb_ci.location.contact.name);
```

The output is the same as `gs.print(gr.cmdb_ci.location.contact.name)` without using addExtraField\(\). The addExtraField\(\) method optimizes the querying of the dot-walked fields. Example output:

```
Abel Tuter
```

## GlideRecord - addFunction\(Object function\)

Applies a pre-defined GlideDBFunctionBuilder object to a record.

Use the GlideDBFunctionBuilder scoped class to define a function. After the function is defined, use the addFunction\(Object function\) method to apply the function to a record.

|Name|Type|Description|
|----|----|-----------|
|function|Object|A GlideDBFunctionBuilder or GlideDBCaseStatementBuilder object that defines a SQL operation.|

|Type|Description|
|----|-----------|
|void| |

```
var functionBuilder = new GlideDBFunctionBuilder();
var myAddingFunction = functionBuilder.add();
myAddingFunction = functionBuilder.field('order');
myAddingFunction = functionBuilder.field('priority');
myAddingFunction = functionBuilder.build();

var now_GR = new GlideRecord('incident');
now_GR.addFunction(myAddingFunction);
now_GR.addQuery(myAddingFunction, '<', 5);
now_GR.query();
while(now_GR.next())
gs.log(now_GR.getValue(myAddingFunction));

```

Output:

```
*** Script: 1
*** Script: 4
*** Script: 3
*** Script: 1
*** Script: 1
*** Script: 2
*** Script: 1
*** Script: 1
```

## GlideRecord - addInactiveQuery\(\)

Adds a filter to return inactive records. Inactive records have the active flag set to false.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|GlideQueryCondition|Records where the active flag is false.|

```
var inc = new GlideRecord('incident');
inc.addInactiveQuery();
inc.query();
```

### Scoped equivalent

In scoped applications use the scoped method [addQuery\("active","false"\)](../../glideRecordScoped/concept/c_GlideRecordScopedAPI.md#).

## GlideRecord - addJoinQuery\(String table\)

Adds a filter to return records based on a relationship in a related table.

For example, find all the users that are in the database group \(users via sys\_user\_grmember table\). Another example would be find all problems that have an assigned incident \(problems via the incident.problem\_id relationship\).

This is not a true database join; rather, addJoinQuery\(\) adds a subquery. So, while the result set is limited based on the join, the only fields that you have access to are those on the base table \(those which are in the table with which the GlideRecord was initialized\).

Always test queries on a sub-production instance prior to deploying them on a production instance. An incorrectly constructed encoded query, such as including an invalid field name, produces an invalid query. When the invalid query is run, the invalid part of the query condition is dropped, and the results are based on the valid part of the query, which may return all records from the table. Using an insert\(\), update\(\), deleteRecord\(\), or deleteMultiple\(\) method on bad query results can result in data loss.

You can set the **glide.invalid\_query.returns\_no\_rows** system property to true to have queries with invalid encoded queries return no records. In some cases, the query may still return records in API results even when **glide.invalid\_query.returns\_no\_rows** is set to true. This happens in queries where an invalid query term is used with a WHERE operator. In such queries, the WHERE operator ignores the invalid term\(s\) but still interprets and returns the rest of the query statement. For more information about this system property and its functionality, see [Available system properties](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

|Name|Type|Description|
|----|----|-----------|
|table|String|Table name|

|Type|Description|
|----|-----------|
|GlideQueryCondition|Records where the relationships match.|

Find problems that have an incident attached. This example returns problems that have associated incidents. However, it won't pull values from the incidents that are returned as a part of the query.

```
var prob = new GlideRecord('problem');
prob.addJoinQuery('incident');
prob.query();
```

Find active=false problems with associated incidents.

```
// Look for Problem records
var now_GR = new GlideRecord('problem');
 
// That have associated Incident records
var grSQ = now_GR.addJoinQuery('incident');
 
// Where the Problem records are "active=false"
now_GR.addQuery('active', 'false');
 
// And the Incident records are "active=true"
grSQ.addCondition('active', 'true');
 
// Query
now_GR.query();
 
// Iterate and print results
while (now_GR.next()) {
    gs.print(now_GR.getValue('number'));
}
```

### Scoped equivalent

To use the addJoinQuery\(\) method in a scoped application, use the corresponding scoped method: [addJoinQuery\(\)](../../glideRecordScoped/concept/c_GlideRecordScopedAPI.md#).

## GlideRecord - addJoinQuery\(String table, String primaryField\)

Adds a filter to return records based on a relationship in a related table.

For example, find all the users that are in the database group \(users via sys\_user\_grmember table\). Another example would be find all problems that have an assigned incident \(problems via the incident.problem\_id relationship\).

This is not a true database join; rather, addJoinQuery\(\) adds a subquery. So, while the result set is limited based on the join, the only fields that you have access to are those on the base table \(those which are in the table with which the GlideRecord was initialized\).

Always test queries on a sub-production instance prior to deploying them on a production instance. An incorrectly constructed encoded query, such as including an invalid field name, produces an invalid query. When the invalid query is run, the invalid part of the query condition is dropped, and the results are based on the valid part of the query, which may return all records from the table. Using an insert\(\), update\(\), deleteRecord\(\), or deleteMultiple\(\) method on bad query results can result in data loss.

You can set the **glide.invalid\_query.returns\_no\_rows** system property to true to have queries with invalid encoded queries return no records. In some cases, the query may still return records in API results even when **glide.invalid\_query.returns\_no\_rows** is set to true. This happens in queries where an invalid query term is used with a WHERE operator. In such queries, the WHERE operator ignores the invalid term\(s\) but still interprets and returns the rest of the query statement. For more information about this system property and its functionality, see [Available system properties](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

|Name|Type|Description|
|----|----|-----------|
|table|String|Table name|
|primaryField|String|If other than sys\_id, the primary field.|

|Type|Description|
|----|-----------|
|GlideQueryCondition|Records where the relationships match.|

Find problems that have incidents using the open\_by field at the join key instead of the sys\_id.

```
var now_GR = new GlideRecord('problem'); 
now_GR.addJoinQuery('incident', 'opened_by'); 
now_GR.query();
```

### Scoped equivalent

To use the addJoinQuery\(\) method in a scoped application, use the corresponding scoped method: [addJoinQuery\(\)](../../glideRecordScoped/concept/c_GlideRecordScopedAPI.md#).

## GlideRecord - addJoinQuery\(String table, String primaryField, String joinTableField\)

Adds a filter to return records based on a relationship in a related table.

For example, find all the users that are in the database group \(users via sys\_user\_grmember table\). Another example would be find all problems that have an assigned incident \(problems via the incident.problem\_id relationship\).

This is not a true database join; rather, addJoinQuery\(\) adds a subquery. So, while the result set is limited based on the join, the only fields that you have access to are those on the base table \(those which are in the table with which the GlideRecord was initialized\).

Always test queries on a sub-production instance prior to deploying them on a production instance. An incorrectly constructed encoded query, such as including an invalid field name, produces an invalid query. When the invalid query is run, the invalid part of the query condition is dropped, and the results are based on the valid part of the query, which may return all records from the table. Using an insert\(\), update\(\), deleteRecord\(\), or deleteMultiple\(\) method on bad query results can result in data loss.

You can set the **glide.invalid\_query.returns\_no\_rows** system property to true to have queries with invalid encoded queries return no records. In some cases, the query may still return records in API results even when **glide.invalid\_query.returns\_no\_rows** is set to true. This happens in queries where an invalid query term is used with a WHERE operator. In such queries, the WHERE operator ignores the invalid term\(s\) but still interprets and returns the rest of the query statement. For more information about this system property and its functionality, see [Available system properties](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

|Name|Type|Description|
|----|----|-----------|
|table|String|Table name|
|primaryField|String|If other than sys\_id, the primary field.|
|joinTableField|String|If other than sys\_id, the field that joins the tables|

|Type|Description|
|----|-----------|
|GlideQueryCondition|Records where the relationships match.|

Find problems that have incidents associated where the incident caller\_id field value matches that of the problem opened\_by field.

```
var now_GR = new GlideRecord('problem'); 
now_GR.addJoinQuery('incident', 'opened_by', 'caller_id'); 
now_GR.query();
```

### Scoped equivalent

To use the addJoinQuery\(\) method in a scoped application, use the corresponding scoped method: [addJoinQuery\(\)](../../glideRecordScoped/concept/c_GlideRecordScopedAPI.md#).

## GlideRecord - addNotNullQuery\(String fieldName\)

Adds a filter to return records where the specified field is not null.

|Name|Type|Description|
|----|----|-----------|
|fieldName|String|The field name.|

|Type|Description|
|----|-----------|
|GlideQueryCondition|GlideQueryCondition of records where the parameter field is not null.|

```
var target = new GlideRecord('incident'); 
  target.addNotNullQuery('short_description');
  target.query();   // Issue the query to the database to get all records
  while (target.next()) {   
     // add code here to process the incident record
  }
```

### Scoped equivalent

To use the addNotNullQuery\(\) method in a scoped application, use the corresponding scoped method: [addNotNullQuery\(\)](../../glideRecordScoped/concept/c_GlideRecordScopedAPI.md#).

## GlideRecord - addNullQuery\(String fieldName\)

Adds a filter to return records where the specified field is null.

|Name|Type|Description|
|----|----|-----------|
|fieldName|String|The field name.|

|Type|Description|
|----|-----------|
|GlideQueryCondition|GlideQueryCondition of records where the specified field is null.|

```
var target = new GlideRecord('incident'); 
  target.addNullQuery('short_description');
  target.query();   // Issue the query to the database to get all records
  while (target.next()) {   
     // add code here to process the incident record
  }
```

### Scoped equivalent

To use the addNullQuery\(\) method in a scoped application, use the corresponding scoped method: [addNullQuery\(\)](../../glideRecordScoped/concept/c_GlideRecordScopedAPI.md#).

## GlideRecord - addQuery\(String name, Object operator, Object value\)

Provides the ability to build a request, which when executed, returns the rows from the specified table that match the request.

If you're familiar with SQL, this method is similar to the "where" clause. You can make one or more addQuery\(\) calls in a single query. For this method the queries are AND'ed. If any of the query statements need to be OR'ed, use the class [GlideQueryCondition](../../GlideQueryCondition/concept/c_GlideQueryConditionAPI.md#).

addQuery\(\) is typically called with three parameters; table field, operator, and comparison value. It can be called with only two parameters, table field and comparison value, such as `myObj.addQuery('category','Hardware');`. The operator in this case is assumed to be "equal to".

For additional information on using queries, see [Querying tables in script](https://www.servicenow.com/docs/access?context=c_UsingGlideRecordToQueryTables&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US).

Always test queries on a sub-production instance prior to deploying them on a production instance. An incorrectly constructed encoded query, such as including an invalid field name, produces an invalid query. When the invalid query is run, the invalid part of the query condition is dropped, and the results are based on the valid part of the query, which may return all records from the table. Using an insert\(\), update\(\), deleteRecord\(\), or deleteMultiple\(\) method on bad query results can result in data loss.

You can set the **glide.invalid\_query.returns\_no\_rows** system property to true to have queries with invalid encoded queries return no records. In some cases, the query may still return records in API results even when **glide.invalid\_query.returns\_no\_rows** is set to true. This happens in queries where an invalid query term is used with a WHERE operator. In such queries, the WHERE operator ignores the invalid term\(s\) but still interprets and returns the rest of the query statement. For more information about this system property and its functionality, see [Available system properties](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

<table id="table_ix2_hvp_dt" class="parameters"><thead><tr><th>

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

Table field name or path to an attribute within a dynamic attribute store element.Format of the dynamic path: `dyn_att_field->group_name->attribute_name`

-   `dyn_att_field`: Name of a dynamic attribute store field on the table.
-   `group_name`: Name of the group that the attribute is associated with. Located in the group\_name field of the Dynamic Attribute Group \[dynamic\_attribute\_group\] table.
-   `attr_name`: Name of the dynamic attribute. Located in the attribute field of the Dynamic Attribute \[dynamic\_attribute\] table.

For more information on dynamic attributes, see [Dynamic Schema](https://www.servicenow.com/docs/access?context=dynamic-schema&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

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

**Note:** Use CONTAINS instead of the LIKE operator.

Dynamic schema operators:

-   =
-   !=
-   &lt;
-   &gt;
-   &lt;=
-   &gt;=
-   BETWEEN
-   CONTAINS
-   DOES\_NOT\_CONTAIN
-   ENDSWITH
-   GT\_FIELD
-   GT\_OR\_EQUALS\_FIELD
-   IN
-   ISEMPTY
-   ISNOTEMPTY
-   IS\_NOT\_NULL
-   IS\_NULL
-   LIKE
-   LT\_FIELD
-   LT\_OR\_EQUALS\_FIELD
-   MATCHES
-   NOT\_IN
-   NOT\_LIKE
-   NOT\_MATCHES
-   NSAMEAS
-   SAMEAS
-   STARTSWITH

</td></tr><tr><td>

value

</td><td>

Object

</td><td>

Value on which to query \(not case-sensitive\).

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|GlideQueryCondition|Reference to the GlideQueryCondition that was added to the GlideRecord.|

The following example shows how to call this method.

```
var rec = new GlideRecord('incident');
rec.addQuery('active',true);
rec.addQuery('sys_created_on', ">", "2010-01-19 04:05:00");
rec.query();
while (rec.next()) { 
 rec.active = false;
 gs.print('Active incident ' + rec.number + ' closed');
 rec.update();
}
```

The following example shows how to use the `IN` operator.

```
var que = new GlideRecord('incident');
que.addQuery('number','IN','INC00001,INC00002');
que.query();
while(que.next()) {
 //do something....
}
```

The following example shows how to call this method for using attributes in a dynamic attribute store.

```
var gr_Inc = new GlideRecord('incident');
gr_Inc.addQuery('inc_dynamic_schema->cars->avg_mpg', 'GT_FIELD', 'inc_dynamic_schema2->cars->avg_mpg'); 
gr_Inc.query();
while(gr_Inc.next()) {
    gs.info(gr_Inc.number + " Gas Mileage 1: " + gr_Inc.getDynamicAttributeValue('inc_dynamic_schema->cars->avg_mpg') +  " GT_FIELD Gas Mileage 2 :" + gr_Inc.getDynamicAttributeValue('inc_dynamic_schema2->cars->avg_mpg'));
}
```

### Scoped equivalent

To use the addQuery\(\) method in a scoped application, use the corresponding scoped method: [addQuery\(\)](../../glideRecordScoped/concept/c_GlideRecordScopedAPI.md#).

## GlideRecord - addValue\(String field, Number value\)

Provides atomic add and subtract operations on a specified number field at the database level for the current GlideRecord object.

Typically, a GlideRecord object is written as one record in a database. Individual field values are stored as defined. For code that adds a value to a GlideRecord field, it simply saves the field to the database with the new value, rather than atomically incrementing it.

For example, when the following code is executed, the value of the u\_count field in the database is 2.

```
gs.print(now_now_GR.u_count); // "1" 
now_GR.u_count += 1; 
now_GR.update(); 
now_GR.get(now_now_GR.sys_id); 
gs.print(now_now_GR.u_count); // "2"   
```

If another user concurrently runs identical code, instead of the two operations each adding 1 to u\_count, the net effect is that u\_count only contains 2, with one operation's update actually being lost.

Conversely, the addValue\(\) method performs the addition/subtraction in the database when the record is updated as an atomic operation. Two operations running concurrently each properly update the field.

```
gs.print(now_now_GR.u_count); // "1" 
now_GR.addValue("u_count", 1); 
now_GR.update(); 
now_GR.get(now_GR); // The record must be reloaded from the database to observe the result
gs.print(now_now_GR.u_count); // "3", if executed concurrently with another user 
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

The name of the field in this GlideRecord to modify. If the associated field is not a numeric type, the operation is ignored.

</td></tr><tr><td>

value

</td><td>

Number

</td><td>

The amount to add to the value when the record is saved. To perform a subtraction operation, simply pass a negative value.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

Shows a value being added.

```
gs.print(now_GR.u_count); // "1" 
now_GR.addValue("u_count", 1); 
now_GR.update(); 
now_GR.get(now_GR.sys_id); // The record must be reloaded from the database to observe the result
gs.print(now_GR.u_count);
```

Output: 2

Shows a value being subtracted.

```
gs.print(now_GR.u_count); // "4" 
now_GR.addValue("u_count", -1); 
now_GR.update(); 
now_GR.get(now_GR.sys_id); // The record must be reloaded from the database to observe the result
gs.print(now_GR.u_count);
```

Output: 3

## GlideRecord - applyEncodedQuery\(String queryString\)

Sets the values of the specified encoded query terms and applies them to the current GlideRecord.

|Name|Type|Description|
|----|----|-----------|
|queryString|String|Encoded query to apply to the current GlideRecord.|

|Type|Description|
|----|-----------|
|None| |

```
function createAcl(table, role) {
  gs.print("Checking security on table " + table);
  var now_GR = new GlideRecord("sys_security_acl");
  now_GR.addQuery("name", table);
  now_GR.addQuery("operation", "read");
  now_GR.query();
  var encQuery = now_GR.getEncodedQuery();
  if (now_GR.next()) {
    // existing acl found so use it
    createAclRole(now_GR.sys_id.toString(), role);
    return;
  } else {
  now_GR.initialize();
  now_GR.applyEncodedQuery(encQuery);
  var acl = now_GR.insert();
    gs.print("Added read access control on " + table);
    createAclRole(acl, role);
  } 
}
```

## GlideRecord - applyTemplate\(String template\)

Apply a template record from the Template table \[sys\_template\] to the current record. If the specified template is not found, no action is taken.

**Note:** This method automatically instantiates a now\_GR.insert\(\) method if a template has the **Next Related Child Template** field filled. For information, see [Create templates for related task records](https://www.servicenow.com/docs/access?context=create-templates-for-related-task-records&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

|Name|Type|Description|
|----|----|-----------|
|template|String|Name of a template from the Templates \[sys\_template\] table.|

|Type|Description|
|----|-----------|
|void| |

```
var rec1 = new GlideRecord("incident");
rec1.initialize();
rec1.applyTemplate("my_incident_template");
rec1.insert();
```

## GlideRecord - autoSysFields\(Boolean e\)

Enables or disables the update to the fields sys\_updated\_by, sys\_updated\_on, sys\_mod\_count, sys\_created\_by, and sys\_created\_on. This is often used for manually updating field values on a record while leaving historical information unchanged.

**Warning:** Use caution if you use this method. When you use this method the sys\_mod\_count field will not be incremented, and other sys\_ fields will not be updated. This can break functionality including, but not limited to, the Activity Formatter, History Sets, Notifications, and Metrics.

|Name|Type|Description|
|----|----|-----------|
|e|Boolean|If false disables updates to sys\_updated\_by, sys\_updated\_on, sys\_mod\_count, sys\_created\_by, and sys\_created\_on.|

|Type|Description|
|----|-----------|
|void| |

```
var inc = new GlideRecord('incident');
 
// Change all Open(1) incidents to Active(2)
 
inc.addQuery('state', 1);
inc.query();
 
while (inc.next()) {
  inc.autoSysFields(false);  // Do not update sys_updated_by, sys_updated_on, sys_mod_count, sys_created_by, and sys_created_on
  inc.setWorkflow(false);    // Do not run any other business rules
  inc.setValue('state', 2);
  inc.update();
}
```

## GlideRecord - canCreate\(\)

Determines if the access control rules \(which includes the user's role\) permit inserting new records in this table.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_ryz_pwp_dt" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the user's roles permit creating of records in this table.Possible values:

-   true: Creating permitted
-   false: Creating is not permitted

</td></tr></tbody>
</table>This example shows whether records can be created on the benefit\_plan table.

```
canCreateBenefitPlan : function() {
  var now_GR = new GlideRecord('benefit_plan');
  return now_GR.canCreate();
}
```

### Scoped equivalent

To use the canCreate\(\) method in a scoped application, use the corresponding scoped method: [canCreate\(\)](../../glideRecordScoped/concept/c_GlideRecordScopedAPI.md#).

## GlideRecord - canDelete\(\)

Determines if the access control rules \(which includes the user's role\) permit deletion of records in this table.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_lmz_zwp_dt" class="returns"><thead><tr><th>

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
</table>```
var att = new GlideRecord('sys_attachment');
att.get('$[sys_attachment.sys_id]');
var sm = GlideSecurityManager.get();
var checkMe = 'record/sys_attachment/delete';
var canDelete = sm.hasRightsTo(checkMe, att);
gs.log('canDelete: ' + canDelete);
```

### Scoped equivalent

To use the canDelete\(\) method in a scoped application, use the corresponding scoped method: [canDelete\(\)](../../glideRecordScoped/concept/c_GlideRecordScopedAPI.md#).

## GlideRecord - canRead\(\)

Indicates whether the Access Control Rules \(ACLs\) permit the current user to read the current record within the associated GlideRecord table. This method evaluates all available ACLs for the specific resource.

**Note:** You shouldn’t use this method to check for table-level access. A single call to this method might not be sufficient to get a conclusive table-level access rights check result. To perform a table-level access check, use the GlideSecurityManager.hasRightsTo\(\) method.

For additional information on ACLs, see [Access Controls Evaluation Order](https://developer.servicenow.com/dev.do#!/learn/learning-plans/yokohama/servicenow_application_developer/app_store_learnv2_securingapps_yokohama_access_controls_evaluation_order).

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_d3g_4xp_dt" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the user's roles permit reading of the current record.Valid values:

-   true: Reading permitted
-   false: Reading isn't permitted

</td></tr></tbody>
</table>This example shows how to iterate through the Incident \[incident\] table and check if the user has read rights to each record.

```
var grTable = new GlideRecord('incident');
grTable.query();
while (grTable.next()) {
  if (grTable.canRead()) 
		…
}
```

### Scoped equivalent

To use the canRead\(\) method in a scoped application, use the corresponding scoped method: [canRead\(\)](../../glideRecordScoped/concept/c_GlideRecordScopedAPI.md#).

## GlideRecord - canWrite\(\)

Determines if the access control rules \(which includes the user's role\) permit updates to records in this table.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_trp_xxp_dt" class="returns"><thead><tr><th>

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
</table>This example shows whether records can be written to the benefit\_plan table.

```
canWriteBenefitPlan : function() {
  var now_GR = new GlideRecord('benefit_plan');
  return now_GR.canWrite();
}
```

### Scoped equivalent

To use the canWrite\(\) method in a scoped application, use the corresponding scoped method: [canWrite\(\)](../../glideRecordScoped/concept/c_GlideRecordScopedAPI.md#).

## GlideRecord - changes\(\)

Determines whether any of the fields in the record have changed.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_pfg_gyp_dt" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether there are changes in the specified record.Possible values:

-   true: Fields in the specified record have changed.
-   false: No fields have changed.

</td></tr></tbody>
</table>This example shows how to check if there are changes in an incident record.

```
var now_GR = new GlideRecord("incident");
now_GR.query();
now_GR.next();
if (now_GR.changes()) {
  gs.print("The incident record reported changes right after being read");
} else {
  gs.print("The incident record has not changed");
}
```

### Scoped equivalent

To implement this functionality in a scoped application, add code similar to the following:

```
var now_GR = new GlideRecord("incident");
   now_GR.get("965c9e5347c12200e0ef563dbb9a7156");
   now_GR.short_description = "test";
   var elements = now_GR.getElements();
   var hasChanged = false;
   for(var i=0; i < elements.length;i++){
     var element = elements[i];
     hasChanged = hasChanged || element.changes();
     gs.info(element.getName() + ":" + element.changes());
   }
   gs.info(hasChanged);
```

## GlideRecord - chooseWindow\(Number firstRow, Number lastRow, Boolean forceCount\)

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

-   [query\(\)](c_GlideRecordAPI.md#)
-   [setLimit\(\)](c_GlideRecordAPI.md#)
-   [setNoCount\(\)](c_GlideRecordAPI.md#)

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

## GlideRecord - deleteMultiple\(\)

Deletes all records that satisfy the query.

This method does not delete attachments.

Dot-walking is not supported for this method. When using the deleteMultiple\(\) function on referenced tables, all the records in the table are deleted. Also, when using deleteRecord\(\) to cascade delete, prior calls to setWorkflow\(\) on the same GlideRecord object are ignored.

Do not use deleteMultiple\(\) on tables with currency fields. Always delete each record individually. Also, do not use this method with the chooseWindow\(\) or setLimit\(\) methods when working with large tables. The setLimit\(\) method does not limit the number of records that are deleted with deleteMultiple\(\). All records returned by the query are deleted regardless of setLimit\(\).

The **glide.db.forced.chunk.threshold** system property sets the threshold above which forces chunk record deletions and updates. Chunking helps to prevent non-primary key deletions on huge tables from causing replication problems. For more information, see [Available system properties](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

**Note:** When using deleteMultiple\(\) to cascade delete, prior calls to setWorkflow\(\) on the same GlideRecord object are ignored.

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

### Scoped equivalent

To use the deleteMultiple\(\) method in a scoped application, use the corresponding scoped method: [deleteMultiple\(\)](../../glideRecordScoped/concept/c_GlideRecordScopedAPI.md#).

## GlideRecord - deleteRecord\(\)

Deletes a single record.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_yqy_s1x_dt" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the record was successfully deleted.Possible values:

-   true: Record was deleted.
-   false: No record was found to delete.

</td></tr></tbody>
</table>This example shows how to delete all inactive records from the Incident table.

```
var rec = new GlideRecord('incident');
rec.addQuery('active',false);
rec.query();
while (rec.next()) { 
 gs.info('Inactive incident ' + rec.number + ' deleted');
 rec.deleteRecord();
}
```

Output:

```
Inactive incident INC0010010 deleted
Inactive incident INC0010011 deleted
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

### Scoped equivalent

To use the deleteRecord\(\) method in a scoped application, use the corresponding scoped method: [deleteRecord\(\)](../../glideRecordScoped/concept/c_GlideRecordScopedAPI.md#).

## GlideRecord - disableSysIdInOptimization\(\)

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

## GlideRecord - find\(String columnName, String value\)

Returns true if any record has a matching value in the specified column. If found, it also moves to the first record that matches, essentially executing next\(\) until the record is returned.

**Note:** This method creates a record instead of updating the existing record if you apply the update\(\) method after modifying the GlideRecord. To avoid creating a record, call the next\(\) method before calling find\(\). For example:

```
var existingMaterials = new GlideRecord('u_m2m_material_num_service_instance');
existingMaterials.addQuery('u_service_instance', serviceInstance.sys_id);
existingMaterials.query();
existingMaterials.next(); // This line added to prevent new record creation

existingMaterials.find('u_material_number', 'ca41b9fd37a84200fdc25ca543990ed8');

existingMaterials.u_material_quantity = 5;
existingMaterials.update("Modify request via catalog");
```

See also:

-   [next\(\)](c_GlideRecordAPI.md#)
-   [update\(\)](c_GlideRecordAPI.md#)

|Name|Type|Description|
|----|----|-----------|
|columnName|String|Field name to search.|
|value|String|Value to check for in the specified field.|

<table id="table_l1m_qyp_dt" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether any record within the current table has a matching value in the specified field.Possible values:

-   true: Matching field.
-   false: No matching field.

</td></tr></tbody>
</table>This example shows how to find a record in the Incident table with "Critical" in the short description field.

```
var now_GR = new GlideRecord("incident");
now_GR.query();
var shortDescription = "Critical";
if (now_GR.find("short_description", shortDescription)) {
  gs.print("An incident with the specified field value was found");
  var recordID = now_GR.getValue("sys_id");
  gs.print("Found in the following record: " + recordID);
} else {
  gs.print("An incident with the specified field value was not found");
}
```

Output:

```
An incident with the specified field value was found
Found in the following record: 552c48888c033300964f4932b03eb092
```

## GlideRecord - get\(Object name, Object value\)

Returns the specified record in the current GlideRecord object.

This method accepts either one or two parameters. If only a single parameter is passed in, the method assumes that it is the sys\_id of the desired record. If not found, it then tries to match the value against the display value. If two parameters are passed in, the first is the name of the column within the GlideRecord to search. The second is the value to search for. If multiple records are found, use next\(\) to access the additional records.

|Name|Type|Description|
|----|----|-----------|
|name|Object|Optional. Name of the instantiated GlideRecord column to search for the specified **value** parameter. If only a single parameter is passed in, the method assumes that this parameter is sys\_id.|
|value|Object|Value to match. For calculated fields, the value is matched as is rather than running a calculation on a scripted default value for a field in the record.|

<table id="table_cwp_pcr_dt" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Indicates whether the requested record was located.Possible values:

-   true: Record was found
-   false: Record was not found

</td></tr></tbody>
</table>This example gets an incident record by passing in the sys\_id.

```
var grIncident = new GlideRecord('incident');
var returnValue = grIncident.get('99ebb4156fa831005be8883e6b3ee4b9');
gs.info(returnValue); // logs true or false
gs.info(grIncident.number); // logs Incident Number
```

This example gets an incident record by passing in the column in the record to search and the value to search for.

```
var grIncident = new GlideRecord('incident');
var returnValue = grIncident.get('caller_id.name','Sylivia Wayland');
gs.info(returnValue); // logs true or false
gs.info(grIncident.number); // logs Incident Number
```

### Scoped equivalent

To use the get\(\) method in a scoped application, use the corresponding scoped method: [get\(\)](../../glideRecordScoped/concept/c_GlideRecordScopedAPI.md#).

## GlideRecord - getAttribute\(String fieldName\)

Returns the dictionary attributes on the specified field.

|Name|Type|Description|
|----|----|-----------|
|fieldName|String|Field name for which to return the dictionary attributes|

|Type|Description|
|----|-----------|
|String|Dictionary attributes|

This example shows how to return the dictionary attributes for "tree\_picker".

```
function doit() {
  var now_GR = new GlideRecord('sys_user');
  now_GR.query("user_name","admin");
  if (now_GR.next()) {
    gs.print("we got one");
    gs.print(now_GR.location.getAttribute("tree_picker"));
  }
}
```

### Scoped equivalent

To use the getAttribute\(\) method in a scoped application, use the corresponding scoped method: [getAttribute\(\)](../../glideRecordScoped/concept/c_GlideRecordScopedAPI.md#).

## GlideRecord - getClassDisplayValue\(\)

Returns the table's label.

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

### Scoped equivalent

To use the getClassDisplayValue\(\) method in a scoped application, use the corresponding scoped method: [getClassDisplayValue\(\)](../../glideRecordScoped/concept/c_GlideRecordScopedAPI.md#).

## GlideRecord - getDisplayValue\(String name\)

Retrieves the display value for the current record or the display value of an attribute in a dynamic attribute store.

[Display values](https://www.servicenow.com/docs/access?context=c_DisplayValues&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US) are manipulated based on the actual value in the database and user or system settings and preferences.

The display value that is returned is dependent on the field type.

-   Choice fields: The database value may be a number, but the display value is more descriptive.
-   Date fields: The database value is in UTC format, while the display value is based on the user's time zone.
-   Encrypted text: The database value is encrypted, while the displayed value is unencrypted based on the user's encryption context.
-   Reference fields: The database value is sys\_id, but the display value is the display field of the referenced record.

For more information on dynamic attributes, see [Dynamic Schema](https://www.servicenow.com/docs/access?context=dynamic-schema&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

<table id="table_kps_f2r_dt" class="parameters"><thead><tr><th>

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

Optional. Only required when requesting the display value for a dynamic attribute. Path to an attribute within a dynamic schema to retrieve.

Format of the dynamic path: `dyn_att_field->group_name->attribute_name`

-   `dyn_att_field`: Name of a dynamic attribute store field on the table.
-   `group_name`: Name of the group that the attribute is associated with. Located in the group\_name field of the Dynamic Attribute Group \[dynamic\_attribute\_group\] table.
-   `attr_name`: Name of the dynamic attribute. Located in the attribute field of the Dynamic Attribute \[dynamic\_attribute\] table.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|String|Display value for the current record or specified element.|

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

This example shows how to retrieve the display value of an attribute within a dynamic attribute store element.

```
var gr_AppTab = new GlideRecord('application_table'); 
gr_AppTab.setValue('dyn_att_field->group->attr', 42); 
gr_AppTab.setDisplayValue('dyn_att_field->group->attr2, true);
gr_AppTab.update();
gs.info('Attr value: ' + 
gr_AppTab.getDisplayValue('dyn_att_field->group->attr);
gs.info('Attr2 value: ' + 
gr_AppTab.getDisplayValue('dyn_att_field->group->attr2);
```

Output:

```
Attr value: System error
Attr2 value: true
```

### Scoped equivalent

To use the getDisplayValue\(\) method in a scoped application, use the corresponding scoped method: [getDisplayValue\(\)](../../glideRecordScoped/concept/c_GlideRecordScopedAPI.md#).

## GlideRecord - getDynamicAttribute\(String fullPath\)

Returns the GlideElementDynamicAttribute object for the specified dynamic attribute store path.

For more information on dynamic attributes, see [Dynamic Schema](https://www.servicenow.com/docs/access?context=dynamic-schema&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

<table id="table_rgk_h1x_1bc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

fullPath

</td><td>

String

</td><td>

Path to use to locate the desired dynamic attribute. Format of the dynamic path: `dyn_att_field->group_name->attribute_name`

-   `dyn_att_field`: Name of a dynamic attribute store field on the table.
-   `group_name`: Name of the group that the attribute is associated with. Located in the group\_name field of the Dynamic Attribute Group \[dynamic\_attribute\_group\] table.
-   `attr_name`: Name of the dynamic attribute. Located in the attribute field of the Dynamic Attribute \[dynamic\_attribute\] table.

</td></tr></tbody>
</table><table id="table_sgk_h1x_1bc" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

GlideElementDynamicAttribute object containing the specified dynamic attribute.If the **fullPath** parameter is invalid, returns null.

</td></tr></tbody>
</table>The following code example shows how to call this method.

```
var gr_Inc = new GlideRecord('incident');
gr_Inc.get('number', 'INC0009009');
gr_Inc.getDynamicAttribute('attr_store->car->color').setValue('Blue');
gr_Inc.update();

gr_Inc = new GlideRecord('incident');
gr_Inc.get('number', 'INC0009009');
gs.info(gr_Inc.getDynamicAttribute('attr_store', 'car->color'));
```

Output:

```
*** Script: Blue
```

## GlideRecord - getDynamicAttribute\(String dynamicAttributeField, String groupAttrPath\)

Returns a GlideElementDynamicAttribute object that contains the dynamic attribute located at the specified table field and attribute path.

<table id="table_yzz_p1x_1bc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

dynamicAttributeField

</td><td>

String

</td><td id="DynS-dynamicAttributeField-entry">

Name of the field in the table that contains the dynamic attribute.

</td></tr><tr><td>

groupAttrPath

</td><td>

String

</td><td>

Attribute path to use to locate the associated dynamic schema attribute.Format: `"group_name->attr_name"`

-   `group_name`: Name of the group that the attribute is associated with. Located in the Name field of the Dynamic Attribute Group \[dynamic\_attribute\_group\] table or the Group field of the Dynamic Attribute \[dynamic\_attribute\] table.
-   `attr_name`: Name of the dynamic attribute within the dynamic group. Located in the Name field of the Dynamic Attribute \[dynamic\_attribute\] table.

For example: `"car->color"`

</td></tr></tbody>
</table><table id="table_zzz_p1x_1bc" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

GlideElementDynamicAttribute object containing the specified dynamic attribute.If either the **dynamicAttributeField** or **groupAttrPath** parameters are invalid, returns null.

</td></tr></tbody>
</table>The following code example shows how to call this method.

```
var gr_Inc = new GlideRecord('incident');
gr_Inc.get('number', 'INC0009009');
gr_Inc.getDynamicAttribute('attr_store->car->color').setValue('Blue');
gr_Inc.update();

gr_Inc = new GlideRecord('incident');
gr_Inc.get('number', 'INC0009009');
gs.info(gr_Inc.getDynamicAttribute('attr_store', 'car->color'));
```

Output:

```
*** Script: Blue
```

## GlideRecord - getDynamicAttributeValue\(String fullPath\)

Returns the value of the dynamic attribute located at a specified path.

<table id="table_oh3_x1x_1bc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

fullPath

</td><td>

String

</td><td>

Path to use to locate the desired dynamic attribute. Format of the dynamic path: `dyn_att_field->group_name->attribute_name`

-   `dyn_att_field`: Name of a dynamic attribute store field on the table.
-   `group_name`: Name of the group that the attribute is associated with. Located in the group\_name field of the Dynamic Attribute Group \[dynamic\_attribute\_group\] table.
-   `attr_name`: Name of the dynamic attribute. Located in the attribute field of the Dynamic Attribute \[dynamic\_attribute\] table.

</td></tr></tbody>
</table><table id="table_ph3_x1x_1bc" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Value of the dynamic attribute located at the specified path.If the **fullPath** parameter contains invalid data or the specified attribute value isn't one of the supported data types, returns null.

</td></tr></tbody>
</table>The following code example shows how to call this method.

```
// Update the value of the attribute 'attribute_store->car->time_of_purchase' incident `INC0009009` to a timestamp (in UTC)
var gr1 = new GlideRecord('incident');
gr1.get('number', 'INC0009009');
gr1.setDynamicAttributeValue('attribute_store->car->time_of_purchase', '2020-05-13 13:52:44');
gr1.update();

// Then retrieve the value of the attribute on the same record
var gr2 = new GlideRecord('incident');
gr2.get('number', 'INC0009009');
gs.info("Time of Purchase Value        (UTC): " + gr2.getDynamicAttributeValue('attribute_store->car->time_of_purchase'));
gs.info("Time of Purchase DisplayValue (PST): " + gr2.getDynamicAttributeDisplayValue('attribute_store->car->time_of_purchase'));
```

Output:

```
*** Script: Time of Purchase Value        (UTC): 2020-05-13 13:52:44
*** Script: Time of Purchase DisplayValue (PST): 2020-05-13 06:52:44
```

## GlideRecord - getDynamicAttributeValue\(String dynamicAttributeField, String groupAttrPath\)

Returns the value of the dynamic attribute located at a specified field in the current table and a specified attribute path.

<table id="table_n1f_fbx_1bc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

dynamicAttributeField

</td><td>

String

</td><td id="DynS-dynamicAttributeField-entry">

Name of the field in the table that contains the dynamic attribute.

</td></tr><tr><td>

groupAttrPath

</td><td>

String

</td><td>

Attribute path to use to locate the associated dynamic schema attribute.Format: `"group_name->attr_name"`

-   `group_name`: Name of the group that the attribute is associated with. Located in the Name field of the Dynamic Attribute Group \[dynamic\_attribute\_group\] table or the Group field of the Dynamic Attribute \[dynamic\_attribute\] table.
-   `attr_name`: Name of the dynamic attribute within the dynamic group. Located in the Name field of the Dynamic Attribute \[dynamic\_attribute\] table.

For example: `"car->color"`

</td></tr></tbody>
</table><table id="table_o1f_fbx_1bc" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Value of the dynamic attribute located at the specified path.If either the **dynamicAttributeField** or **groupAttrPath** parameters are invalid, returns null.

</td></tr></tbody>
</table>The following code example shows how to call this method.

```
// Update the value of the attribute 'attribute_store->car->time_of_purchase' incident `INC0009009` to a timestamp (in UTC)
var gr1 = new GlideRecord('incident');
gr1.get('number', 'INC0009009');
gr1.setDynamicAttributeValue('attribute_store', 'car->time_of_purchase', '2020-05-13 13:52:44');
gr1.update();

// Then retrieve the value of the attribute on the same record
var gr2 = new GlideRecord('incident');
gr2.get('number', 'INC0009009');
gs.info("Time of Purchase Value        (UTC): " + gr2.getDynamicAttributeValue('attribute_store', 'car->time_of_purchase'));
gs.info("Time of Purchase DisplayValue (PST): " + gr2.getDynamicAttributeDisplayValue('attribute_store', 'car->time_of_purchase'));
```

Output:

```
*** Script: Time of Purchase Value        (UTC): 2020-05-13 13:52:44
*** Script: Time of Purchase DisplayValue (PST): 2020-05-13 06:52:44
```

## GlideRecord - getDynamicAttributeDisplayValue\(String fullPath\)

Returns the display value of the dynamic attribute located at the specified path.

<table id="table_nht_nbx_1bc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

fullPath

</td><td>

String

</td><td>

Path to use to locate the desired dynamic attribute. Format of the dynamic path: `dyn_att_field->group_name->attribute_name`

-   `dyn_att_field`: Name of a dynamic attribute store field on the table.
-   `group_name`: Name of the group that the attribute is associated with. Located in the group\_name field of the Dynamic Attribute Group \[dynamic\_attribute\_group\] table.
-   `attr_name`: Name of the dynamic attribute. Located in the attribute field of the Dynamic Attribute \[dynamic\_attribute\] table.

</td></tr></tbody>
</table><table id="table_oht_nbx_1bc" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

Display value of the dynamic attribute located at the specified path.If the **fullPath** parameter is invalid, returns null.

</td></tr></tbody>
</table>The following code example shows how to call this method.

```
// Update the value of the attribute 'attribute_store->car->time_of_purchase' incident `INC0009009` to a timestamp (in UTC)
var gr1 = new GlideRecord('incident');
gr1.get('number', 'INC0009009');
gr1.setDynamicAttributeValue('attribute_store->car->time_of_purchase', '2020-05-13 13:52:44');
gr1.update();

// Then retrieve the value of the attribute on the same record
var gr2 = new GlideRecord('incident');
gr2.get('number', 'INC0009009');
gs.info("Time of Purcahse Value        (UTC): " + gr2.getDynamicAttributeValue('attribute_store->car->time_of_purchase'));
gs.info("Time of Purcahse DisplayValue (PST): " + gr2.getDynamicAttributeDisplayValue('attribute_store->car->time_of_purchase'));
```

Output:

```
*** Script: Time of Purcahse Value        (UTC): 2020-05-13 13:52:44
*** Script: Time of Purcahse DisplayValue (PST): 2020-05-13 06:52:44
```

## GlideRecord - getDynamicAttributeDisplayValue\(String dynamicAttributeField, String groupAttrPath\)

Returns the display value of the dynamic attribute located in a specified table field and attribute path.

<table id="table_vm3_wbx_1bc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

dynamicAttributeField

</td><td>

String

</td><td id="DynS-dynamicAttributeField-entry">

Name of the field in the table that contains the dynamic attribute.

</td></tr><tr><td>

groupAttrPath

</td><td>

String

</td><td>

Attribute path to use to locate the associated dynamic schema attribute.Format: `"group_name->attr_name"`

-   `group_name`: Name of the group that the attribute is associated with. Located in the Name field of the Dynamic Attribute Group \[dynamic\_attribute\_group\] table or the Group field of the Dynamic Attribute \[dynamic\_attribute\] table.
-   `attr_name`: Name of the dynamic attribute within the dynamic group. Located in the Name field of the Dynamic Attribute \[dynamic\_attribute\] table.

For example: `"car->color"`

</td></tr></tbody>
</table><table id="table_wm3_wbx_1bc" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

Display value of the dynamic attribute located at the specified path.If either the **dynamicAttributeField** or **groupAttrPath** parameters are invalid, returns null.

</td></tr></tbody>
</table>The following code example shows how to call this method.

```
// Update the value of the attribute 'attribute_store->car->time_of_purchase' incident `INC0009009` to a timestamp (in UTC)
var gr1 = new GlideRecord('incident');
gr1.get('number', 'INC0009009');
gr1.setDynamicAttributeValue('attribute_store', 'car->time_of_purchase', '2020-05-13 13:52:44');
gr1.update();

// Then retrieve the value of the attribute on the same record
var gr2 = new GlideRecord('incident');
gr2.get('number', 'INC0009009');
gs.info("Time of Purchase Value        (UTC): " + gr2.getDynamicAttributeValue('attribute_store', 'car->time_of_purchase'));
gs.info("Time of Purchase DisplayValue (PST): " + gr2.getDynamicAttributeDisplayValue('attribute_store', 'car->time_of_purchase'));
```

Output:

```
*** Script: Time of Purchase Value        (UTC): 2020-05-13 13:52:44
*** Script: Time of Purchase DisplayValue (PST): 2020-05-13 06:52:44
```

## GlideRecord - getED\(\)

Returns the element's descriptor.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|GlideElementDescriptor|The element's descriptor.|

This example shows how to retrieve the name field for an incident GlideRecord.

```
grInc = new GlideRecord('incident');
grInc.getActiveQuery();
grInc.query();
if (grInc.next())
  gs.info("Table Descriptor is - " + grInc.getED().getName());

```

Output:

```
Table Descriptor is - incident
```

### Scoped equivalent

To use the getED\(\) method in a scoped application, use the corresponding scoped method: [getED\(\)](../../glideRecordScoped/concept/c_GlideRecordScopedAPI.md#).

## GlideRecord - getElement\(String fieldName\)

Retrieves the GlideElement for a specified field.

The value returned by this method is a complete GlideElement object. The results are the equivalent of dot-walking a field value. For example, `now_GR.getElement('short_description')` provides the same result as `nowGR.short_description`.

In most cases, don’t use dot-walking to get values from a record. Dot-walking retrieves the entire object instead of the field value. Retrieving the object uses more storage and might cause undesirable results when used in arrays or in Service Portal.

Instead of retrieving the entire object, you can use one of the following methods to copy the field values:

-   [getValue\(\)](c_GlideRecordAPI.md#)
-   [getDisplayValue\(\)](c_GlideRecordAPI.md#)

If dot-walking through a GlideElement object is necessary, use the toString\(\) method to retrieve values. For example, you might need the current caller's manager sys\_id to set another reference field. The following example shows how to get the string value instead of the entire object:

```
var mgr = current.caller_id.manager.toString();
```

See also: [GlideElement - toString\(\)](../../GlideElement_global/concept/c_GlideElementAPI.md#).

|Name|Type|Description|
|----|----|-----------|
|fieldName|String|Column name for which to return the GlideElement object.|

|Type|Description|
|----|-----------|
|GlideElement|The GlideElement for the specified column of the current record. Each object describes a field in the current GlideRecord.|

This example shows how to obtain the GlideElement object for a passed in table and compare them with the expected system metadata values.

```
function compareElement(comment, table, element, /*{}*/ expected) {
  var now_GR = new GlideRecord(table);
  var el = now_GR.getElement(element);
  for (var n in expected) {
    assertEquals(comment + ":" + table + "." + element, expected[n], el.sys_meta[n]);
  }
}
```

### Scoped equivalent

To use the getElement\(\) method in a scoped application, use the corresponding scoped method: [getElement\(\)](../../glideRecordScoped/concept/c_GlideRecordScopedAPI.md#).

## GlideRecord - getEncodedQuery\(\)

Retrieves the query condition of the current result set as an encoded query string.

For details, see [Encoded query strings](https://www.servicenow.com/docs/access?context=c_EncodedQueryStrings&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String| |

This example shows how to obtain the current encoded query to use later to create a read ACL role.

```
function createAcl(table, role) {
  gs.print("Checking security on table " + table);
  var now_GR = new GlideRecord("sys_security_acl");
  now_GR.addQuery("name", table);
  now_GR.addQuery("operation", "read");
  now_GR.query();
  var encQuery = now_GR.getEncodedQuery();
  if (now_GR.next()) {
    // existing acl found so use it
    createAclRole(now_GR.sys_id.toString(), role);
   return;
  } else {
    now_GR.initialize();
    now_GR.applyEncodedQuery(encQuery);
    var acl = now_GR.insert();
    gs.print("   Added read access control on " + table);
    createAclRole(acl, role);
  }
}
```

### Scoped equivalent

To use the getEncodedQuery\(\) method in a scoped application, use the corresponding scoped method: [getEncodedQuery\(\)](../../glideRecordScoped/concept/c_GlideRecordScopedAPI.md#).

## GlideRecord - getEscapedDisplayValue\(\)

Retrieves the field value for the display field of the current record and adds escape characters for use in Jelly scripts.

**Note:** For this method to work, a display value must have been set on the associated table. For information on how to do this, see [Select a field as the table display value](https://www.servicenow.com/docs/access?context=t_SelectTheDisplayValue&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Escaped value of the current table's display field.|

This example shows how to obtain the user\_name escaped display value from the User \[sys\_user\] table.

```
var userName = "Michael J'ones";
var now_GR = new GlideRecord("sys_user");
if (now_GR.get("user_name", userName)) {
  gs.print("Deleting existing user=" + userName);
  now_GR.deleteRecord();
}
now_GR.initialize();

var name = userName.split(" ", 2);
var firstName = name[0];
var lastName = name[1];
now_GR.setValue("user_name", userName);
gs.print("Name: " + now_GR.getValue("user_name"));
now_GR.setValue("first_name", firstName);
now_GR.setValue("last_name", lastName);
var escapeValue = now_GR.getEscapedDisplayValue();
gs.print("Escaped name: " + escapeValue);
```

Output:

```
Name: Michael J'ones
Escaped name: Michael J\'ones
```

## GlideRecord - getFields\(\)

Retrieves a Java ArrayList of fields in the current record.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Java ArrayList|Fields in the current record|

```
// This can be run in "Scripts - Background" for demonstration purposes
 
// Get a single incident record
var grINC = new GlideRecord('incident');
grINC.query();
grINC.next();
gs.print('Using ' + grINC.getValue('number'));
gs.print('');
 
// getFields() returns a Java ArrayList
var fields = grINC.getFields();
 
// Enumerate GlideElements in the GlideRecord object that have values
gs.print('Enumerating over all fields with values:');
for (var i = 0; i < fields.size(); i++) {
  var glideElement = fields.get(i);
  if (glideElement.hasValue()) {
    gs.print('  ' + glideElement.getName() + '\t' + glideElement);
  }
}
gs.print('');
 
// Get a specific GlideElement: number
gs.print('Getting the number field:');
for (var i = 0; i < fields.size(); i++) {
  var glideElement = fields.get(i);
  if (glideElement.hasValue() && glideElement.getName() == 'number') {
    gs.print('  ' + glideElement.getName() + '\t' + glideElement);
  }
}
```

## GlideRecord - getLabel\(\)

Retrieves the field's label.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The field's label|

This example shows how to retrieve a label of a question field in the Requested Item table and print the label and its display name.

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
         template.print('     ' + now_V.getGlideObject().getQuestion().getLabel() + " = " 
                     + vnow_V.getDisplayValue() + "\n");  
      }
    }
}
```

### Scoped equivalent

To use the getLabel\(\) method in a scoped application, use the corresponding scoped method: [getLabel\(\)](../../glideRecordScoped/concept/c_GlideRecordScopedAPI.md#).

## GlideRecord - getLink\(Boolean noStack\)

Retrieves the link for the current record.

<table id="table_evz_2hr_dt" class="parameters"><thead><tr><th>

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

Flag that indicates whether to append the generated link to the end of the URL. For example: `&sysparm_stack=[tablename]_list.do? sysparm_query=active=true`.Valid values:

-   true: Append link.
-   false: Do not append link.

 Default: false

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|String|URL of the current record.|

This example checks for attachments and adds the link if any are found.

```
var attachment_link = '';
var rec = new GlideRecord('sc_req_item');
rec.addQuery('sys_id', current.request_item);
rec.query();
if(rec.next()){
  if(rec.hasAttachments()){
    attachment_link = gs.getProperty('glide.servlet.uri') + rec.getLink();
  }   
}
```

### Scoped equivalent

To use the getLink\(\) method in a scoped application, use the corresponding scoped method: [getLink\(\)](../../glideRecordScoped/concept/c_GlideRecordScopedAPI.md#).

## GlideRecord - getLocation\(\)

Retrieves the row number of the current record within the table.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Number|Zero-based row number of the current record within the table.|

This example shows how to check if a record within the Incident table is not retrieved properly by comparing the record count to the record location number.

```
var now_GR = new GlideRecord("incident");
now_GR.addQuery("priority", "4");
now_GR.query();
for (x=0; x <4; x++) {
  now_GR.next();
  gs.print("Location value: " + now_GR.getLocation());
}
```

Output:

```
Location value: 0
Location value: 1
Location value: 2
Location value: 3
```

## GlideRecord - getPlural\(\)

Retrieves the plural label of the GlideRecord table.

For example, if the table name is "Change Request," this method returns "Change Requests."

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The plural label of the GlideRecord's table.|

This example shows checks the return values for getLabel\(\) and getPlural\(\) for the Incident table.

```
var now_GR = new GlideRecord('incident');
gs.print(now_GR.getLabel());
if (now_GR.getLabel() != 'Incident')
throw "GlideRecord.getLabel() returned unexpected value for table 'incident': " + now_GR.getLabel();

gs.print(now_GR.getPlural());
if (now_GR.getPlural() != 'Incidents')
throw "GlideRecord.getPlural() returned unexpected value for table 'incident': " + now_GR.getPlural();
"success";
```

### Scoped equivalent

To use the getPlural\(\) method in a scoped application, use the scoped [GlideRecord.getED\(\)](c_GlideRecordAPI.md#) method to obtain the field's descriptor, and then use the scoped [GlideElementDescriptor.getPlural\(\)](../../glideElementDescriptor/concept/c_GlideElementDescriptorScopedAPI.md#) method.

## GlideRecord - getRecordClassName\(\)

Retrieves the class \(table\) name for the current record.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Class or table name|

```
function TaskAssignmentFilter() {
  var classname = current.getRecordClassName();
  var filter = "type=null";
  if (classname == "incident" && current.category == "database") {
    filter = GetGroupFilter("database");
  }
  else {
    // append exclusion for 'catalog' to the filter
    var cat = new GlideRecord("sys_user_group_type");  
    cat.addQuery("name", "catalog");
    cat.query();
    if (cat.next()) {
      filter += "^ORtype!=" + cat.sys_id;
    }
  }
  gs.log("TaskAssignmentFilter: " + filter);
  return filter;
}
```

### Scoped equivalent

To use the getRecordClassName\(\) method in a scoped application, use the corresponding scoped method: [getRecordClassName\(\)](../../glideRecordScoped/concept/c_GlideRecordScopedAPI.md#).

## GlideRecord - getRelatedLists\(\)

Retrieves a list of names and display values of related lists associated with the current GlideRecord.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|HashMap|Hash map with names and display values of related lists.|

This example shows how to obtain the list of names and display values of related lists associated with the current GlideRecord, store them in an array, and then print their values.

```
var now_GR = new GlideRecord('incident');
var c = now_GR.getRelatedLists().values().toArray();
var numElements = c.length;
for( var i = 0; i < numElements; ++i){
  gs.print(i+": "+c[i]);
}
```

## GlideRecord - getRelatedTables\(\)

Retrieves a list of names and display values of tables that are referred to by the current record.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|HashMap|Hash map with names and display values of related tables.|

This example shows how to obtain the list of names and display values of tables related to the current GlideRecord, store them in an array, and then print their values.

```
var now_GR = new GlideRecord('incident');
var c = now_GR.getRelatedTables().values().toArray();
var numElements = c.length;
for( var i = 0; i < numElements; ++i){
  gs.print(i+": "+c[i]);
}
```

## GlideRecord - getRowCount\(\)

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

### Scoped equivalent

To use the getRowCount\(\) method in a scoped application, use the corresponding scoped method: [getRowCount\(\)](../../glideRecordScoped/concept/c_GlideRecordScopedAPI.md#).

## GlideRecord - getRowNumber\(\)

Retrieves the row number set by saveLocation\(\) or setLocation\(\).

To get the current row number, use getLocation\(\).

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Number|Saved row number.|

This example shows how to save a row location in the Users table and then obtain that row number.

```
var now_GR = new GlideRecord('sys_user');
now_GR.addQuery();
now_GR.query();
now_GR.saveLocation(5);
var savedRow = now_GR.getRowNumber();
gs.print("Saved row: " + savedRow);
```

Output:

```
Saved row: 5
```

## GlideRecord - getTableName\(\)

Retrieves the table name associated with this GlideRecord.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|A table name|

This example shows how to write the current table name in the system log.

```
gs.log('Table: ' + current.getTableName()); 
gs.log('Parent: ' + current.parent.sys_id); 
var item = new GlideRecord('sc_req_item'); 
item.addQuery('sys_id', current.parent.sys_id); 
item.query(); 
if(item.next()){ 
  for(var variable in item.variable_pool) {
    gs.log(variable); 
    var answer = eval ("item.variable_pool." + variable + ".getDisplayValue()");
    gs.log(answer);
  }
}
```

### Scoped equivalent

To use the getTableName\(\) method in a scoped application, use the corresponding scoped method: [getTableName\(\)](../../glideRecordScoped/concept/c_GlideRecordScopedAPI.md#).

## GlideRecord - getUniqueValue\(\)

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

## GlideRecord - getValue\(String fieldName\)

Retrieves the string value of a specified field or the string value of an attribute in a dynamic attribute store.

**Note:** If the Column Level Encryption Enterprise plugin is enabled and the instance has access to the key, this method returns clear text values from encrypted fields. If the instance does not have access to the key, this method returns the encrypted value. For more information, see [Platform Encryption](https://www.servicenow.com/docs/access?context=now-platform-encryption&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).

For more information on dynamic attributes, see [Dynamic Schema](https://www.servicenow.com/docs/access?context=dynamic-schema&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

<table id="table_ev2_flr_dt" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

fieldName

</td><td>

String

</td><td>

The name of the field whose value you want to retrieve or the path to an attribute within a dynamic attribute store to retrieve.Format of the dynamic path: `dyn_att_field->group_name->attribute_name`

-   `dyn_att_field`: Name of a dynamic attribute store field on the table.
-   `group_name`: Name of the group that the attribute is associated with. Located in the group\_name field of the Dynamic Attribute Group \[dynamic\_attribute\_group\] table.
-   `attr_name`: Name of the dynamic attribute. Located in the attribute field of the Dynamic Attribute \[dynamic\_attribute\] table.

</td></tr></tbody>
</table><table id="table_fv2_flr_dt" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

Value of the specified element. Returns null if the field is empty or the field doesn't exist. **Note:** Boolean values return as `"0"` and `"1"` string values instead of false and true.

</td></tr></tbody>
</table>This example uses the getValue\(\) method to obtain field values in two GlideRecords that are being compared.

```
function() {
  var jobExists = true;
  var jobGr;
  while(jobExists){
    jobGr = new GlideRecord("sys_trigger");
    jobExists = jobGr.get("name", "BaselineAPI: Create Baseline Job");
  }
  var baselineGr =  new GlideRecord('pm_project_baseline');
  baselineGr.get('baseline_name','Test Project Baseline');
  baselineGr.query();
 
  Assert.assertEquals(true, baselineGr.next());
  var projectGr =  new GlideRecord('pm_project');
  projectGr.get(this._project);
  Assert.assertEquals(projectGr.getValue('cost'), baselineGr.getValue('cost'));
  Assert.assertEquals((projectGr.getValue('capex_cost')), baselineGr.getValue('capex_cost'));
  Assert.assertEquals((projectGr.getValue('opex_cost')), baselineGr.getValue('opex_cost'));
  Assert.assertEquals((projectGr.getValue('budget_cost')), baselineGr.getValue('budget_cost'));
  Assert.assertEquals((projectGr.getValue('value')), baselineGr.getValue('value'));
  Assert.assertEquals((projectGr.getValue('npv_value')), baselineGr.getValue('npv_value'));  Assert.assertEquals((projectGr.getValue('score')), baselineGr.getValue('score'));
}
```

This example shows how to retrieve the value of a dynamic attribute.

```
// Update the value of the attribute 'attribute_store->car->color' to 'Red' on incident `INC0009009`
var gr1 = new GlideRecord('incident');
gr1.get('number', 'INC0009009');
gr1.setDynamicAttributeValue('attribute_store->car->color', 'Red');
gr1.update();

// Then retrieve the value of the attribute on the same record
var gr2 = new GlideRecord('incident');
gr2.get('number', 'INC0009009');
gs.info(gr2.getValue('attribute_store->car->color'));
```

Output:

```
*** Script: Red
```

### Scoped equivalent

To use the getValue\(\) method in a scoped application, use the corresponding scoped method: [getValue\(\)](../../glideRecordScoped/concept/c_GlideRecordScopedAPI.md#).

## GlideRecord - hasAttachments\(\)

Determines if the current GlideRecord has any attachments.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Boolean|True if the current record has attachments, false otherwise.|

This example checks for attachments and creates a link if there are any.

```
var attachment_link = '';
var rec = new GlideRecord('sc_req_item');
rec.addQuery('sys_id', current.request_item);
rec.query();
if(rec.next()){
  if(rec.hasAttachments()){
    attachment_link = gs.getProperty('glide.servlet.uri') + rec.getLink();
  }   
}
```

## GlideRecord - hasNext\(\)

Determines if there are any more records in the GlideRecord.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Boolean|True if there are more records in the query set, otherwise false.|

This example shows how to call different functions based on whether there are additional records in the current GlideRecord.

```
if (now_GR.hasNext()) {
  dothis(); // found it, do it
} else {
  dothat(); // didn't find it
};
```

### Scoped equivalent

To use the hasNext\(\) method in a scoped application, use the corresponding scoped method: [hasNext\(\)](../../glideRecordScoped/concept/c_GlideRecordScopedAPI.md#).

## GlideRecord - initialize\(\)

Creates an empty record within the current GlideRecord that is suitable for population before an insert.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void| |

This example initializes a new record in the to\_do table, creates a record, and then inserts it into the table.

```
var now_GR = new GlideRecord('to_do');
now_GR.initialize(); 
now_GR.name = 'first to do item'; 
now_GR.description = 'learn about GlideRecord'; 
now_GR.insert();
```

### Scoped equivalent

To use the initialize\(\) method in a scoped application, use the corresponding scoped method: [initialize\(\)](../../glideRecordScoped/concept/c_GlideRecordScopedAPI.md#).

## GlideRecord - insert\(\)

Inserts a new record with the field values that have been set for the current record.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The sys\_id of the inserted record, or null if the record is not inserted.|

This example creates a new record in the to\_do table, sets values for some record fields, and then inserts the record into the table.

```
var now_GR = new GlideRecord('to_do');
now_GR.initialize(); 
now_GR.name = 'first to do item'; 
now_GR.description = 'learn about GlideRecord'; 
now_GR.insert();
```

### Scoped equivalent

To use the insert\(\) method in a scoped application, use the corresponding scoped method: [insert\(\)](../../glideRecordScoped/concept/c_GlideRecordScopedAPI.md#).

## GlideRecord - insertWithReferences\(\)

Inserts a new record and also inserts or updates any related records with the provided information.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|sys\_id of the inserted record or null if the record was not inserted.|

If a reference value is not specified \(as below\), then a new user record is created with the provided first\_name and last\_name, and the caller\_id value is set to this newly created sys\_user record. The result is a new sys\_user record with the provided first\_name and last\_name and a new incident record with the provided short\_description and caller\_id.

```
var inc = new GlideRecord('incident');
inc.initialize();
inc.short_description = 'New incident 1';
inc.caller_id.first_name = 'John';
inc.caller_id.last_name = 'Doe';
inc.insertWithReferences();
```

If a caller\_id value is specified, then that caller\_id is updated with the provided first\_name and last\_name. The result is a newly created incident record with values set for short\_description and caller\_id.

```
var inc = new GlideRecord('incident');
inc.initialize();
inc.short_description = 'New incident 1';
inc.caller_id.setDisplayValue('David Loo');
inc.caller_id.first_name = 'John';
inc.caller_id.last_name = 'Doe';
inc.insertWithReferences();
```

## GlideRecord - instanceOf\(String className\)

Checks a table for the type\\class of table.

|Name|Type|Description|
|----|----|-----------|
|className|String|Name of a type or class of record.|

|Type|Description|
|----|-----------|
|Boolean|True if table is an instance of the specified class.|

This example checks if the passed in group/user is of the sys\_user table/class type.

```
function(groupOrUser, label, grantedBy) {
  var labelCheck;
  var labelRecord;
  if (typeof label === "string") {
    labelRecord = new GlideRecord('label');
    labelRecord.addQuery('name', label);
    labelRecord.query();
    labelRecord.next();
  } else {
    labelRecord = label;
  }
  if (groupOrUser.instanceOf('sys_user')) {
    labelCheck = new GlideRecord('label_user_m2m');
    labelCheck.addQuery('user', groupOrUser.sys_id);
  } else {
    labelCheck = new GlideRecord('label_group_m2m');
    labelCheck.addQuery('group', groupOrUser.sys_id);
  }
  labelCheck.addQuery('label', labelRecord.sys_id);
  if (grantedBy !== "undefined") {
    labelCheck.addQuery('granted_by', grantedBy.sys_id);
  }
  labelCheck.query();
  return labelCheck.hasNext();
}
```

## GlideRecord - isNewRecord\(\)

Determines whether the current record has been inserted into the database.

This method returns true only if the newRecord\(\) method has been called. This method is useful for scripted ACL, and in the condition of UI actions, but should not be used in background scripts.

**Note:** This method returns true for any new record during a business rule, or if the newRecord\(\) method is used to initialize a record with default values and a unique ID \(sys\_id\). In all other cases, it returns false.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_wbn_g4q_dt" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the current record is new \(has not been inserted into the database.\)Possible values:

-   true: Record is new.
-   false: Record is not new.

</td></tr></tbody>
</table>This example checks if the new record has been inserted into the sys\_user table.

```
var now_GR = new GlideRecord("sys_user");
now_GR.newRecord();
now_GR.setValue("user_name", "John Smith");
gs.print("Is this a new record: " + now_GR.isNewRecord());

var now_GR2 = new GlideRecord("sys_user");
now_GR2.addQuery("user_name", "Abel Tutor");
now_GR2.query();
now_GR2.next();
gs.print("Is this a new record: " + now_GR2.isNewRecord());
```

## GlideRecord - isValid\(\)

Determines if the current GlideRecord table exists.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Boolean|True if the table is exists \(valid\), otherwise false.|

This example checks if the Incident table exists.

```
var testTable = new GlideRecord('incident');
gs.print(testTable.isValid());
```

### Scoped equivalent

To use the isValid\(\) method in a scoped application, use the corresponding scoped method: [isValid\(\)](../../glideRecordScoped/concept/c_GlideRecordScopedAPI.md#).

## GlideRecord - isValidField\(String columnName\)

Determines if the specified field is defined in the current GlideRecord table.

|Name|Type|Description|
|----|----|-----------|
|columnName|String|Name of a column to check.|

|Type|Description|
|----|-----------|
|Boolean|True if the field is defined in the table, otherwise false.|

This example checks if the sys\_class\_name field exists in the cmds\_software\_instance table.

```
var gobj = new GlideRecord('sys_db_object');
gobj.addQuery('name','cmdb_software_instance');
gobj.query();
if (!gobj.next()) {
  var si = new GlideRecord('cmdb_software_instance');
  si.query();
  var count = 0;
  while (si.next()) {
    if (!si.isValidField('sys_class_name')) {
      var ci = new GlideRecord('cmdb_ci');
      ci.name = si.name;
      ci.setNewGuidValue(si.sys_id);
      ci.sys_class_name = 'cmdb_software_instance';
      ci.insert();
      count++;
    }
  }
}
```

### Scoped equivalent

To use the isValidField\(\) method in a scoped application, use the corresponding scoped method: [isValidField\(\)](../../glideRecordScoped/concept/c_GlideRecordScopedAPI.md#).

## GlideRecord - isValidRecord\(\)

Determines if the current record is valid.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_md5_3qq_dt" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag indicating whether the current record is valid.Valid values:

-   true: Record is valid.
-   false: Past the end of the record set.

</td></tr></tbody>
</table>This example checks if the record identifier by the passed in sys\_id is a valid record in the idea table.

```
function(sysId) {
  this.log('Inside acceptIdea sysId = ' + sysId);
  var now_GR = new GlideRecord('idea');
  now_GR.get(sysId);
  this.log('now_GR.isValidRecord() = ' + now_GR.isValidRecord());
  if(now_GR.isValidRecord()) {
    now_GR.setValue('state', 2);
    this.log('Updating gliderecord');
    this.log('gliderecord table name' + now_GR.getTableName());
    now_GR.update();
  }
}
```

### Scoped equivalent

To use the isValidRecord\(\) method in a scoped application, use the corresponding scoped method: [isValidRecord\(\)](../../glideRecordScoped/concept/c_GlideRecordScopedAPI.md#).

## GlideRecord - newRecord\(\)

Creates a GlideRecord, sets the default values for the fields, and assigns a unique ID to the record.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void| |

This example checks if the new record has been inserted into the sys\_user table.

```
var now_GR = new GlideRecord("sys_user");
now_GR.newRecord();
now_GR.setValue("user_name", "John Smith");
gs.print("Is this a new record: " + now_GR.isNewRecord());

var now_GR2 = new GlideRecord("sys_user");
now_GR2.addQuery("user_name", "Abel Tutor");
now_GR2.query();
now_GR2.next();
gs.print("Is this a new record: " + now_GR2.isNewRecord());
```

### Scoped equivalent

To use the newRecord\(\) method in a scoped application, use the corresponding scoped method: [newRecord\(\)](../../glideRecordScoped/concept/c_GlideRecordScopedAPI.md#).

## GlideRecord - next\(\)

Moves to the next record in the GlideRecord.

Use this method to iterate through the records returned by a GlideRecord query.

**Note:** This method fails if there is a field in the table called "next". If that is the case, use the method [\_next\(\)](c_GlideRecordAPI.md#).

**Note:** The `if(myObj.next())` construct only processes the first record returned.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_t2n_yqq_dt" class="returns"><thead><tr><th>

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
</table>This example shows how to iterate through the Incident table using the next\(\) method.

```
var rec = new GlideRecord('incident');
rec.query();
while (rec.next()) { 
  gs.print(rec.number + ' exists');
}
```

### Scoped equivalent

To use the next\(\) method in a scoped application, use the corresponding scoped method: [next\(\)](../../glideRecordScoped/concept/c_GlideRecordScopedAPI.md#).

## GlideRecord - \_next\(\)

Moves to the next record in the GlideRecord. Provides the same functionality as next\(\), intended to be used in cases where the GlideRecord has a column named next.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Boolean|True if there are more records in the query set.|

```
var rec = new GlideRecord('sys_template');
rec.query();
while (rec._next()) { 
  gs.print(rec.number + ' exists');
}
```

### Scoped equivalent

To use the \_next\(\) method in a scoped application, use the corresponding scoped method: [\_next\(\)](../../glideRecordScoped/concept/c_GlideRecordScopedAPI.md#).

## GlideRecord - operation\(\)

Determines if an operation is insert, update, or delete.

Knowing the operation enables using current.operation\(\) to make a generic business rule which can handle each operation uniquely.

For information on using the global variable current, refer to [Global variables in business rules](https://www.servicenow.com/docs/access?context=c_BusinessRules&version=xanadu&pubname=xanadu-application-development&section=c_UsingPredefinedGlobalVariables&ft:locale=en-US).

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

This example shows how to use the operation\(\) method to pass the operation value into the startFlow\(\) method.

```
function createNewTransferOrder() {
  var toGr = new GlideRecord("alm_transfer_order");
  toGr.initialize();
  // From Stockroom - Southern California Warehouse
  toGr.setValue('from_stockroom', fromStockroomSysId);
  // To Stockroom - San Diego North - Pickup/Dropoff
  toGr.setValue('to_stockroom', toStockroomSysId);
  var transferOrder = toGr.insert();

  if(toGr.get(transferOrder)){
  // Start Transfer Order Workflow
  var wf = new Workflow();
  var context = wf.startFlow(toWorkflowSysId, toGr, toGr.operation(),{});
    createNewTransferOrderLine(transferOrder);
  } 
}
```

### Scoped equivalent

To use the operation\(\) method in a scoped application, use the corresponding scoped method: [operation\(\)](../../glideRecordScoped/concept/c_GlideRecordScopedAPI.md#).

## GlideRecord - orderBy\(String fieldName\)

Specifies a field name, or path to an attribute within a dynamic attribute store, to use to order the query set. To order by multiple fields, call this method multiple times with different field values.

<table id="table_rr5_fsq_dt" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

fieldName

</td><td>

String

</td><td>

Table field name, or path to an attribute within a dynamic attribute store, on which to order the query set.Format of the dynamic path: `dyn_att_field->group_name->attribute_name`

-   `dyn_att_field`: Name of a dynamic attribute store field on the table.
-   `group_name`: Name of the group that the attribute is associated with. Located in the group\_name field of the Dynamic Attribute Group \[dynamic\_attribute\_group\] table.
-   `attr_name`: Name of the dynamic attribute. Located in the attribute field of the Dynamic Attribute \[dynamic\_attribute\] table.

For more information on dynamic attributes, see [Dynamic Schema](https://www.servicenow.com/docs/access?context=dynamic-schema&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

This example shows how to order the query set by "order" and then by "number".

```
function UpdateProjectWBS(project) {
  var count = 0;
  var child = new GlideRecord('pm_project_task');
  child.addQuery('parent', project.sys_id);
  child.orderBy('order');
  child.orderBy('number');
  child.query();
  var len = child.getRowCount().toString().length;
  var seq = 0;
  while (child.next()) {
    count += UpdateProjectTaskWBS(child, 1, ++seq, len, '');
  }
  gs.addInfoMessage(count + ' Project Tasks updated');
}
```

This example shows how to order the query set by an attribute within a dynamic attribute store.

```
var gr_Inc = new GlideRecord('incident');
gr_Inc.orderBy('attribute_store->caller_id->first_name');
gr_Inc.query();

while(gr_Inc.next()) {
  gs.info("first_name: " + gr_Inc.getValue('attribute_store->caller_id->first_name'));
}
```

Output:

```
*** Script: first_name: Alejandro
*** Script: first_name: Bertie
*** Script: first_name: Beth
*** Script: first_name: Bow
*** Script: first_name: Bud
*** Script: first_name: Carol
*** Script: first_name: Charlie
*** Script: first_name: Christen
*** Script: first_name: David
```

### Scoped equivalent

To use the orderBy\(\) method in a scoped application, use the corresponding scoped method: [orderBy\(\)](../../glideRecordScoped/concept/c_GlideRecordScopedAPI.md#).

## GlideRecord - orderByDesc\(String fieldName\)

Specifies the field, or an attribute in a dynamic attribute store, to use to order the query set in descending order.

<table id="table_yht_ysq_dt" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

fieldName

</td><td>

String

</td><td>

Table field name, or path to an attribute within a dynamic attribute store, on which to order the query set in descending order.Format of the dynamic path: `dyn_att_field->group_name->attribute_name`

-   `dyn_att_field`: Name of a dynamic attribute store field on the table.
-   `group_name`: Name of the group that the attribute is associated with. Located in the group\_name field of the Dynamic Attribute Group \[dynamic\_attribute\_group\] table.
-   `attr_name`: Name of the dynamic attribute. Located in the attribute field of the Dynamic Attribute \[dynamic\_attribute\] table.

For more information on dynamic attributes, see [Dynamic Schema](https://www.servicenow.com/docs/access?context=dynamic-schema&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

This example shows how to order the query set in ascending or descending order.

```
function(fiscalType, orderByDesc) {
  var now_GR = new GlideRecord('fiscal_period');
  now_GR.addQuery('fiscal_type', fiscalType);
  if (orderByDesc) {
    now_GR.orderByDesc('fiscal_start_date_time');
  } else {
    now_GR.orderBy('fiscal_start_date_time');
  }
  now_GR.setLimit(1);
  now_GR.query();
  now_GR.next();
  return now_GR.sys_id;
}
```

This example shows how to order the query set by an attribute within a dynamic attribute store.

```
var gr_Inc = new GlideRecord('incident');
gr_Inc.orderByDesc('attribute_store->caller_id->first_name');
gr_Inc.query();

while(gr_Inc.next()) {
  gs.info("first_name: " + gr_Inc.getValue('attribute_store->caller_id->first_name'));
}
```

Output:

```

*** Script: first_name: David
*** Script: first_name: Christen
*** Script: first_name: Charlie
*** Script: first_name: Carol
*** Script: first_name: Bud
*** Script: first_name: Bow
*** Script: first_name: Beth
*** Script: first_name: Bertie
*** Script: first_name: Alejandro
```

### Scoped equivalent

To use the orderByDesc\(\) method in a scoped application, use the corresponding scoped method: [orderByDesc\(\)](../../glideRecordScoped/concept/c_GlideRecordScopedAPI.md#).

## GlideRecord - query\(String field, String value\)

Runs a query against the table based on the filters specified in the query methods such as addQuery\(\) and addEncodedQuery\(\).

This method queries the GlideRecord table as well as any references of the table. For more information, see [Querying tables in script](../../../../../script/server-scripting/concept/c_UsingGlideRecordToQueryTables.md#).

**Note:** This method fails if there is a field in the table called "query". If that is the case, use the method [\_query\(\)](c_GlideRecordAPI.md#). To run queries in a domain-separated instance, use the method [queryNoDomain\(\)](c_GlideRecordAPI.md#).

See the [GlideRecord](https://developer.servicenow.com/dev.do#!/learn/courses/utah/app_store_learnv2_scripting_utah_scripting_in_servicenow/app_store_learnv2_scripting_utah_server_side_scripting/app_store_learnv2_scripting_utah_gliderecord) article for details on building and running queries.

See also:

-   [GlideAggregate - Global](../../GlideAggregate/concept/c_GlideAggregateAPI.md#)
-   [GlideQuery\(\)](../../GlideQuery/concept/GlideQueryGlobalAPI.md#)
-   [GlideQueryCondition - Global](../../GlideQueryCondition/concept/c_GlideQueryConditionAPI.md#)

<table id="id_g13_kwd_lpb" class="parameters"><thead><tr><th>

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

### Scoped equivalent

To use the query\(\) method in a scoped application, use the corresponding scoped method: [query\(\)](../../glideRecordScoped/concept/c_GlideRecordScopedAPI.md#).

## GlideRecord - \_query\(String field, String value\)

Runs a query against the table based on the filters specified in the query methods such as addQuery\(\) and addEncodedQuery\(\). This method is intended to be used on tables in which there's a column named "query", which might cause errors running the query\(\) method.

This method queries the GlideRecord table as well as any references of the table. For more information, see [Querying tables in script](../../../../../script/server-scripting/concept/c_UsingGlideRecordToQueryTables.md#).

See the [GlideRecord](https://developer.servicenow.com/dev.do#!/learn/courses/utah/app_store_learnv2_scripting_utah_scripting_in_servicenow/app_store_learnv2_scripting_utah_server_side_scripting/app_store_learnv2_scripting_utah_gliderecord) article for details on building and running queries.

See also:

-   [GlideAggregate - Global](../../GlideAggregate/concept/c_GlideAggregateAPI.md#)
-   [GlideQuery\(\)](../../GlideQuery/concept/GlideQueryGlobalAPI.md#)
-   [GlideQueryCondition - Global](../../GlideQueryCondition/concept/c_GlideQueryConditionAPI.md#)

<table id="id_z1c_ptd_lpb" class="parameters"><thead><tr><th>

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

### Scoped equivalent

To use the \_query\(\) method in a scoped application, use the corresponding scoped method: [\_query\(\)](../../glideRecordScoped/concept/c_GlideRecordScopedAPI.md#).

## GlideRecord - queryNoDomain\(String field, String value\)

Used in domain-separated instances. Similar to query\(\), runs the query against the table based on the filters specified by addQuery\(\) and addEncodedQuery\(\), but ignores domains.

This method queries the GlideRecord table as well as any references of the table. For more information, see [Querying tables in script](../../../../../script/server-scripting/concept/c_UsingGlideRecordToQueryTables.md#).

<table id="id_n1d_1jk_lpb" class="parameters"><thead><tr><th>

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

This example shows how to query the incident table for all domains.

```
var rec = new GlideRecord('incident');
rec.queryNoDomain();
while (rec.next()) { 
 gs.print(rec.number + ' exists');
}
```

## GlideRecord - restoreLocation\(\)

Sets the current record to be the record that was saved with saveLocation\(\). If saveLocation\(\) has not been called, the current record is set to the first record of the GlideRecord.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void| |

This example shows how save the current record location, move to the next record, and then return back to the saved location.

```
function() {
  var now_GR = new GlideRecord("incident");
  now_GR.query();
  now_GR.next();
  var firstID = now_GR.getValue("sys_id");
  now_GR.next();
  var restoreID = now_GR.getValue("sys_id");
  now_GR.saveLocation();
  now_GR.next();
  var lastID = now_GR.getValue("sys_id");
  now_GR.restoreLocation();
  now_GR.next();
  var thisID = now_GR.getValue("sys_id");
  var progress = "first id=" + firstID
    + "\n\t last id=" + lastID
    + "\n\t saved id=" + restoreID
    + "\n\t restored id=" + thisID;
  gs.print("Progress:\n\t" + progress);
}
```

## GlideRecord - saveLocation\(\)

Saves the current row number so you can return to this location using the restoreLocation\(\) method.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void| |

This example shows how save the current record location, move to the next record, and then return back to the saved location.

```
function() {
  var now_GR = new GlideRecord("incident");
  now_GR.query();
  now_GR.next();
  var firstID = now_GR.getValue("sys_id");
  now_GR.next();
  var restoreID = now_GR.getValue("sys_id");
  now_GR.saveLocation();
  now_GR.next();
  var lastID = now_GR.getValue("sys_id");
  now_GR.restoreLocation();
  now_GR.next();
  var thisID = now_GR.getValue("sys_id");
  var progress = "first id=" + firstID
    + "\n\t last id=" + lastID
    + "\n\t saved id=" + restoreID
    + "\n\t restored id=" + thisID;
  gs.print("Progress:\n\t" + progress);
}
```

## GlideRecord - setAbortAction\(Boolean b\)

Sets a flag to indicate if the next database action \(insert, update, delete\) is to be aborted.

Use in an `onBefore` business rule to prevent the database action from being done. The business rule continues to run after setAbortAction\(\) is called. Calling setAbortAction\(\) does not stop subsequent business rules from executing. Calling this method only prevents the database action from occurring.

|Name|Type|Description|
|----|----|-----------|
|b|Boolean|True to abort next action, or false to allow the next action.|

|Type|Description|
|----|-----------|
|void| |

```
if ((!current.u_date1.nil()) && (!current.u_date2.nil())) {
  var start = current.u_date1.getGlideObject().getNumericValue();
  var end = current.u_date2.getGlideObject().getNumericValue();
  if (start > end) {
    gs.addInfoMessage('start must be before end');
    current.u_date1.setError('start must be before end');
    current.setAbortAction(true);
  }
}
```

### Scoped equivalent

To use the setAbortAction\(\) method in a scoped application, use the corresponding scoped method: [setAbortAction\(\)](../../glideRecordScoped/concept/c_GlideRecordScopedAPI.md#).

## GlideRecord - setDisplayValue\(String name, Object value\)

Sets a specified field, or an attribute in a dynamic attribute store, to a specified display value.

For a reference field, this is the display value for the table. For a date/time, this is the time in the caller's current time zone.

<table id="table_ijf_wgw_dt" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

name

</td><td>

String

</td><td id="DynS-name-entry">

Name of the field whose value you want to set or the path to an attribute within a dynamic attribute store.Format of the dynamic path: `dyn_att_field->group_name->attribute_name`

-   `dyn_att_field`: Name of a dynamic attribute store field on the table.
-   `group_name`: Name of the group that the attribute is associated with. Located in the group\_name field of the Dynamic Attribute Group \[dynamic\_attribute\_group\] table.
-   `attr_name`: Name of the dynamic attribute. Located in the attribute field of the Dynamic Attribute \[dynamic\_attribute\] table.

</td></tr><tr><td>

value

</td><td>

Object

</td><td id="DynS-value-entry">

Value to set in the specified attribute.**Note:** For dynamic attributes, only the following data types are supported:

-   Boolean \(True/False\)
-   Decimal
-   Floating Point Number
-   GlideDate
-   GlideDateTime
-   Integer
-   String

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

The following code example shows how to set a display value in a record and then update the record.

```
var now_GR = new GlideRecord('incident');
now_GR.get('46f09e75a9fe198100f4ffd8d366d17b');
now_GR.setDisplayValue('opened_at','2011-02-13 4:30:00');
now_GR.update();
```

The following code example shows how to set a display value in a dynamic attribute store.

```
var gr_AppTab = new GlideRecord('application_table'); 
gr_AppTab.setValue('dyn_att_field->group->attr', 42); 
gr_AppTab.setDisplayValue('dyn_att_field->group->attr2, true);
gr_AppTab.update();
gs.info('Attr value: ' + 
gr_AppTab.getDisplayValue('dyn_att_field->group->attr);
gs.info('Attr2 value: ' + 
gr_AppTab.getDisplayValue('dyn_att_field->group->attr2);
```

## GlideRecord - setDynamicAttributeValue\(String fullPath, Object value\)

Sets the value of the dynamic attribute located at a specified path.

<table id="table_ynk_tdx_1bc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

fullPath

</td><td>

String

</td><td>

Path to use to locate the desired dynamic attribute. Format of the dynamic path: `dyn_att_field->group_name->attribute_name`

-   `dyn_att_field`: Name of a dynamic attribute store field on the table.
-   `group_name`: Name of the group that the attribute is associated with. Located in the group\_name field of the Dynamic Attribute Group \[dynamic\_attribute\_group\] table.
-   `attr_name`: Name of the dynamic attribute. Located in the attribute field of the Dynamic Attribute \[dynamic\_attribute\] table.

</td></tr><tr><td>

value

</td><td>

Object

</td><td>

Value to set the specified dynamic attribute to.The passed value must be of one of the following data types:

-   Boolean \(True/False\)
-   Decimal
-   Floating Point Number
-   GlideDate
-   GlideDateTime
-   Integer
-   String

</td></tr></tbody>
</table><table id="table_znk_tdx_1bc" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the dynamic attribute was successfully updated.Possible values:

-   true: Dynamic attribute was successfully updated.
-   false: Error occurred. Dynamic attribute wasn't updated. Verify that the **fullPath** parameter contains a valid path to the desired attribute.

</td></tr></tbody>
</table>The following code example shows how to call this method.

```
var gr_Inc = new GlideRecord('incident');
gr_Inc.setValue('inc_dynamic_groups', '78db044fc4b44210f8770961513dd7fe'); //Sysid of cars dimensions group
gr_Inc.setDynamicAttributeValue("inc_dynamic_schema->cars->color","black");
gr_Inc.setDynamicAttributeValue("inc_dynamic_schema->cars->make","Honda");
gr_Inc.setDynamicAttributeValue("inc_dynamic_schema->cars->model","CRV");
gr_Inc.setDynamicAttributeValue("inc_dynamic_schema->cars->luxury",false);
gr_Inc.setDynamicAttributeValue("inc_dynamic_schema->cars->cost",20000);
gr_Inc.setDynamicAttributeValue("inc_dynamic_schema->cars->avg_mpg",28.4);
gr_Inc.setDynamicAttributeValue("inc_dynamic_schema->cars->date_purchased", new GlideDateTime());
gr_Inc.setValue("inc_dynamic_schema->cars->total_miles", 10000.12345);
gr_Inc.insert();

```

## GlideRecord - setDynamicAttributeValue\(String dynamicAttributeField, String groupAttrPath, Object value\)

Sets the value of the dynamic attribute located in a specified field of the current GlideRecord and a specified attribute path.

<table id="table_l12_f2x_1bc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

dynamicAttributeField

</td><td>

String

</td><td id="DynS-dynamicAttributeField-entry">

Name of the field in the table that contains the dynamic attribute.

</td></tr><tr><td>

attributePath

</td><td>

String

</td><td>

Attribute path to use to locate the associated dynamic schema attribute.Format: `"group_name->attr_name"`

-   `group_name`: Name of the group that the attribute is associated with. Located in the Name field of the Dynamic Attribute Group \[dynamic\_attribute\_group\] table or the Group field of the Dynamic Attribute \[dynamic\_attribute\] table.
-   `attr_name`: Name of the dynamic attribute within the dynamic group. Located in the Name field of the Dynamic Attribute \[dynamic\_attribute\] table.

For example: `"car->color"`

</td></tr><tr><td>

value

</td><td>

Object

</td><td>

Value to set the specified dynamic attribute to.The passed value must be of one of the following data types:

-   Boolean \(True/False\)
-   Decimal
-   Floating Point Number
-   GlideDate
-   GlideDateTime
-   Integer
-   String

</td></tr></tbody>
</table><table id="table_m12_f2x_1bc" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the dynamic attribute was successfully updated.Possible values:

-   true: Dynamic attribute was successfully updated.
-   false: Error occurred. Dynamic attribute wasn't updated. Verify that the **dynamicAttributeField** and **groupAttrPath** parameters contain valid data.

</td></tr></tbody>
</table>The following code example shows how to call this method.

```
// Update the value of the attribute 'attribute_store->car->time_of_purchase' incident `INC0009009` to a timestamp (in UTC)
var gr1 = new GlideRecord('incident');
gr1.get('number', 'INC0009009');
gr1.setDynamicAttributeValue('attribute_store', 'car->time_of_purchase', '2020-05-13 13:52:44');
gr1.update();

// Then retrieve the value of the attribute on the same record
var gr2 = new GlideRecord('incident');
gr2.get('number', 'INC0009009');
gs.info("Time of Purchase Value        (UTC): " + gr2.getDynamicAttributeValue('attribute_store', 'car->time_of_purchase'));
gs.info("Time of Purchase DisplayValue (PST): " + gr2.getDynamicAttributeDisplayValue('attribute_store', 'car->time_of_purchase'));
```

Output:

```
*** Script: Time of Purchase Value        (UTC): 2020-05-13 13:52:44
*** Script: Time of Purchase DisplayValue (PST): 2020-05-13 06:52:44
```

## GlideRecord - setDynamicAttributeDisplayValue\(String fullPath, Object value\)

Sets the display value of the dynamic attribute located at a specified path.

<table id="table_g4h_s2x_1bc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

fullPath

</td><td>

String

</td><td>

Path to use to locate the dynamic attribute whose display value you want to update. Format of the dynamic path: `dyn_att_field->group_name->attribute_name`

-   `dyn_att_field`: Name of a dynamic attribute store field on the table.
-   `group_name`: Name of the group that the attribute is associated with. Located in the group\_name field of the Dynamic Attribute Group \[dynamic\_attribute\_group\] table.
-   `attr_name`: Name of the dynamic attribute. Located in the attribute field of the Dynamic Attribute \[dynamic\_attribute\] table.

</td></tr><tr><td>

value

</td><td>

Object

</td><td>

Display value to set the specified dynamic attribute to.The passed value must be of one of the following data types:

-   Boolean \(True/False\)
-   Decimal
-   Floating Point Number
-   GlideDate
-   GlideDateTime
-   Integer
-   String

</td></tr></tbody>
</table><table id="table_h4h_s2x_1bc" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the display value of the dynamic attribute was successfully updated.Possible values:

-   true: Display value of the dynamic attribute was successfully updated.
-   false: Error occurred. Display value of the dynamic attribute wasn't updated. Verify that the **fullPath** parameter contains a valid path to the desired attribute.

</td></tr></tbody>
</table>The following code example shows how to call this method.

```
var grProdTab = new GlideRecord('products_table');
grProdTab.query();
grProdTab.next();
var val = grProdTab.setDynamicAttributeDisplayValue('product_details->cars->date_purchased', '2023-03-31 08:54:26');
```

## GlideRecord - setDynamicAttributeDisplayValue\(String dynamicAttributeField, String groupAttrPath, Object value\)

Sets the display value of the dynamic attribute located in a specified field of the current GlideRecord and a specified attribute path.

<table id="table_l1k_1fx_1bc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

dynamicAttributeField

</td><td>

String

</td><td id="DynS-dynamicAttributeField-entry">

Name of the field in the table that contains the dynamic attribute.

</td></tr><tr><td>

groupAttrPath

</td><td>

String

</td><td>

Attribute path to use to locate the associated dynamic schema attribute.Format: `"group_name->attr_name"`

-   `group_name`: Name of the group that the attribute is associated with. Located in the Name field of the Dynamic Attribute Group \[dynamic\_attribute\_group\] table or the Group field of the Dynamic Attribute \[dynamic\_attribute\] table.
-   `attr_name`: Name of the dynamic attribute within the dynamic group. Located in the Name field of the Dynamic Attribute \[dynamic\_attribute\] table.

For example: `"car->color"`

</td></tr><tr><td>

value

</td><td>

Object

</td><td>

Display value to set the specified dynamic attribute to.The passed value must be of one of the following data types:

-   Boolean \(True/False\)
-   Decimal
-   Floating Point Number
-   GlideDate
-   GlideDateTime
-   Integer
-   String

</td></tr></tbody>
</table><table id="table_m1k_1fx_1bc" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the display value of the dynamic attribute was successfully updated.Possible values:

-   true: Display value of the dynamic attribute was successfully updated.
-   false: Error occurred. Display value of the dynamic attribute wasn't updated. Verify that the **dynamicAttributeField** and **groupAttrPath** parameters contain valid data.

</td></tr></tbody>
</table>The following code example shows how to call this method.

```
var grProdTab = new GlideRecord('products_table');
grProdTab.query();
grProdTab.next();
var val = grProdTab.setDynamicAttributeDisplayValue('product_details', 'cars->date_purchased', '2023-03-31 08:54:26');
```

## GlideRecord - setDynamicAttributeValues\(String dynamicAttributeField, GlideDynamicAttributeStore values\)

Sets one or more dynamic attribute values with values specified in the passed GlideDynamicAttributeStore object.

This method only updates the attributes and values passed in as arguments. Attributes and values on the GlideRecord that aren't specified are unaffected by this call. Any invalid groups, attributes, or values are ignored. Check the log messages for possible error information.

<table id="table_r5l_4fx_1bc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

dynamicAttributeField

</td><td>

String

</td><td>

Name of the field in the current table that contains the [dynamic schema](https://www.servicenow.com/docs/access?context=dynamic-schema&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

</td></tr><tr><td>

values

</td><td>

[GlideDynamicAttributeStore](../../GlideDynamicAttributeStore/concept/GlideDynamicAttStoreAPI.md#)

</td><td>

GlideDynamicAttributeStore object that contains the dynamic attributes to update.The values populated in the object must be of the following data types:

-   Boolean \(True/False\)
-   Decimal
-   Floating Point Number
-   GlideDate
-   GlideDateTime
-   Integer
-   String

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

The following code example shows how to call this method.

```
var das = new GlideDynamicAttributeStore();
das.setDynamicAttributeValue('group->attribute1', 'Apple');
das.setDynamicAttributeValue('group->attribute2', 1234);

var gr_Inc = new GlideRecord('incident');
gr_Inc.query();
gr_Inc.next();
gr_Inc.setDynamicAttributeValues(das);
```

## GlideRecord - setForceUpdate\(Boolean force\)

Updates the record even if fields have not changed.

|Name|Type|Description|
|----|----|-----------|
|force|Boolean|True to update even if fields have not changed, otherwise false.|

|Type|Description|
|----|-----------|
|void| |

This example shows how to force a record in the itfm\_cost\_model table to update even without changes.

```
function() {
  gs.log("Update Script: Upgrade_cost_model_data.js started");
  var now_GR = new GlideRecord("itfm_cost_model");
  now_GR.initialize();
  now_GR.addNullQuery("source_table");
  now_GR.query();
  while (now_GR.next()) {
    now_GR.setForceUpdate(true);
    var sourceTable = getSourceTable(now_GR.getValue('clone_from'));
    if(sourceTable){
      now_GR.setValue("source_table", sourceTable);
      now_GR.setWorkflow(false);
      now_GR.update();
    }
  }
}
```

## GlideRecord - setLimit\(Number limit\)

Sets the maximum number of records to return in the GlideRecord from a query.

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

-   [chooseWindow\(\)](c_GlideRecordAPI.md#)
-   [query\(\)](c_GlideRecordAPI.md#)
-   [setNoCount\(\)](c_GlideRecordAPI.md#)

|Name|Type|Description|
|----|----|-----------|
|limit|Number|Limit for records to fetch.|

|Type|Description|
|----|-----------|
|void| |

This example sets the number of records returned in the query to a maximum of ten.

```
var now_GR = new GlideRecord('incident');
now_GR.orderByDesc('sys_created_on');
now_GR.setLimit(10);
now_GR.query();
```

### Scoped equivalent

To use the setLimit\(\) method in a scoped application, use the corresponding scoped method: [setLimit\(\)](../../glideRecordScoped/concept/c_GlideRecordScopedAPI.md#).

## GlideRecord - setLocation\(Number rowNumber\)

Sets the current row location to the specified value.

|Name|Type|Description|
|----|----|-----------|
|rowNumber|Number|Row number to set as the current row.|

|Type|Description|
|----|-----------|
|void| |

This example shows how to set the record position in the Incident table

```
verifySetLocation : function() {
  var now_GR = new GlideRecord("incident");
  now_GR.query();
  var recordIDs = new Array();
  while(now_GR.next()) {
  recordIDs.push(now_GR.getValue("sys_id"));
  }
  for (var ix = recordIDs.length - 1; ix >= 0; ix--) {
    now_GR.setLocation(ix);
    Assert.assertEquals(recordIDs[ix], now_GR.getValue("sys_id"),
      "The entry retrieved for the index " + ix + " is not valid");
  }
}
```

## GlideRecord - setNewGuid\(\)

Generates a new GUID and sets it as the unique ID \(sys\_id\) for the current record.

This function applies only to new records. You cannot change the GUID for an existing record.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Sys\_id of the current record.|

This example creates a new task record and stores the ID in the task\_rel\_task table.

```
var task = new GlideRecord ('task');
var tsk_id = task.setNewGuid();
 
task.description = "Request: " + current.request.number;
task.description = task.description + "\n" + "Requested by: " + current.request.u_requested_by.name;
task.description = task.description + "\n" + "Requested for: " + current.request.u_requested_for.name;
task.description = task.description + "\n" + "Item: " + current.cat_item.name;
 
var now_GR = new GlideRecord ('task_rel_task');
//link the incident to the request
now_GR.parent = current.request;
now_GR.child = tsk_id;
now_GR.insert();
```

## GlideRecord - setNewGuidValue \(String guid\)

Generates a new GUID and sets it as the unique ID for the current record, when inserting a new record.

|Name|Type|Description|
|----|----|-----------|
|guid|String|Value for the new GUID.|

|Type|Description|
|----|-----------|
|void| |

This example generates a new GUID and sets it as the unique ID for the newly created cmdb\_software\_instance record.

```
var gobj = new GlideRecord('sys_db_object');
gobj.addQuery('name','cmdb_software_instance');
gobj.query();
if (!gobj.next()) {
  var si = new GlideRecord('cmdb_software_instance');
  si.query();
  var count = 0;
  while (si.next()) {
  if (!si.isValidField('sys_class_name')) {
    var ci = new GlideRecord('cmdb_ci');
    ci.name = si.name;
    ci.setNewGuidValue(si.sys_id);
    ci.sys_class_name = 'cmdb_software_instance';
    ci.insert();
    count++;
  }
}
```

### Scoped equivalent

To use the setNewGuidValue\(\) method in a scoped application, use the corresponding scoped method: [setNewGuidValue\(\)](../../glideRecordScoped/concept/c_GlideRecordScopedAPI.md#).

## GlideRecord - setNoCount\(\)

Stops a GlideRecord query from running a `COUNT(*)` query.

Running query\(\) with some methods trigger a `COUNT(*)` query, such as the chooseWindow\(\) and getRowCount\(\) methods. The `COUNT(*)` query might cause slow performance on tables with a million or more records. For more information, see the [Performance Improvement - Remove Pagination Count \[KB0817996\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0817996) article in the Now Support Knowledge Base.

**Note:** The setLimit\(\) method also stops a `COUNT(*)`. Using setNoCount\(\) is unnecessary if the setLimit\(\) method is included in the query.

See also:

-   [chooseWindow\(\)](c_GlideRecordAPI.md#)
-   [query\(\)](c_GlideRecordAPI.md#)

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

### Scoped equivalent

To use the setNoCount\(\) method in a scoped application, use the corresponding scoped method: [setNoCount\(\)](../../glideRecordScoped/concept/c_GlideRecordScopedAPI.md#).

## GlideRecord - setQueryReferences\(Boolean queryReferences\)

Enables or disables using the reference field's display name when querying a reference field.

<table id="table_zyr_ljw_dt" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

queryReferences

</td><td>

Boolean

</td><td>

Flag indicating what time of data to generate.Valid values:

-   true: Generate a string of display names.
-   false: Generate a string of sys\_ids.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

```
var grByName = new GlideRecord(this.TEST_TABLE);
grByName.addQuery("caller_id", userDisplayName);
grByName.setQueryReferences(true);
grByName.query();
if (grByName.hasNext()) {
  while(grByName.next()) {
    gs.print("Incident caller_id=" + grByName.caller_id);
  }
} else {
  gs.print("NO RESULTS");
}
```

## GlideRecord - setUseEngines\(Boolean e\)

Disables or enables the running of any engines \(approval rules / assignment rules\).

**Warning:** Disabling the running of engines can have a significant impact on your ServiceNow® instance and how it operates. Ensure that you thoroughly test this change before deploying it to production.

<table id="table_gdy_vjw_dt" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

e

</td><td>

Boolean

</td><td>

Flag that indicates whether to enable or disable the running of any engines.Valid values:

-   true: Enable engines
-   false: Disable engines

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

This example shows how to disable engines and business rules before executing a query.

```
function auditOAuthInboundRequestsUsage(){
  var now_GR = new GlideRecord("oauth_credential");
  var oauthClient = now_GR.addJoinQuery("oauth_entity", "peer", "sys_id");
  now_GR.addQuery("type", "access_token");
  now_GR.addQuery("expires", ">", nowDateTime());
  now_GR.addNullQuery("oauth_requestor_profile");
  oauthClient.addCondition("active", "true");
  oauthClient.addCondition("type", "client");
  now_GR.setUseEngines(false);
  now_GR.setWorkflow(false);
  now_GR.query();
  return now_GR.hasNext();
}
```

## GlideRecord - setValue\(String name, Object value\)

Sets the specified field, or an attribute in a dynamic attribute store, to a specified value.

Normally a script would do a direct assignment, for example `now_GR.category = value`. However, if in a script the element name is a variable, then you can use `now_GR.setValue(elementName, value)`. When setting a value, ensure that the data type of the field matches the data type of the value you enter.

If the value parameter is null, the record isn't updated, and an error isn't thrown.

**Note:** This method can't be used on journal fields. Use [GlideElement.setJournalEntry\(\)](../../GlideElement_global/concept/c_GlideElementAPI.md#) instead.

**Note:** If the Column Level Encryption Enterprise plugin is enabled and the instance has access to the key, this method can insert encrypted data into encrypted fields. If the instance does not have access to the key, this method returns an error. For more information, see [Platform Encryption](https://www.servicenow.com/docs/access?context=now-platform-encryption&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).

-   **Not for authentication with password2 fields**

    The setValue\(\) method passes password2 data as clear text, which results in an error about expecting encrypted data. Additionally, using the setValue\(\) method for password2 fields exposes data that should be encrypted.

    For password2 authentication, use the setDisplayValue\(\) method instead.

    See also:

    -   [Deprecate GlideEncrypter usage of 3DES for password2 fields](https://www.servicenow.com/docs/access?context=password2-3des-deprecation&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US)
    -   [Alternatives to GlideEncrypter usage in knowledge base article KB1320986](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1320986)
    -   [Password2 encryption with the Key Management Framework \(KMF\)](https://www.servicenow.com/docs/access?context=password-2way-encrypted-fields&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US)

<table id="table_yps_2kw_dt" class="parameters"><thead><tr><th>

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

Name of the field whose value you want to set or the path to an attribute within a dynamic attribute store.Format of the dynamic path: `dyn_att_field->group_name->attribute_name`

-   `dyn_att_field`: Name of a dynamic attribute store field on the table.
-   `group_name`: Name of the group that the attribute is associated with. Located in the group\_name field of the Dynamic Attribute Group \[dynamic\_attribute\_group\] table.
-   `attr_name`: Name of the dynamic attribute. Located in the attribute field of the Dynamic Attribute \[dynamic\_attribute\] table.

For more information on dynamic attributes, see [Dynamic Schema](https://www.servicenow.com/docs/access?context=dynamic-schema&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

</td></tr><tr><td>

value

</td><td>

Object

</td><td>

Value to set in the specified field.**Note:** For a dynamic attribute, only the following data types are supported:

-   Boolean \(True/False\)
-   Decimal
-   Floating Point Number
-   GlideDate
-   GlideDateTime
-   Integer
-   String

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

This example shows how to set the value of the state field in the planned\_task table.

```
function() {
  var topTask = new GlideRecord('planned_task');
  topTask.setValue('state', -5);
  var childTask = new GlideRecord('planned_task');
  childTask.setValue('state', -5);
  var s = new PlannedTaskStateManagement(childTask, topTask);
  var state = s.manageStateChange(false);
  Assert.assertEquals("-5", state);
}
```

This example shows how to set the value of a dynamic attribute.

```
var gr_Inc = new GlideRecord('incident');
gr_Inc.setValue('inc_dynamic_groups', '78db044fc4b44210f8770961513dd7fe'); //Sysid of cars dimensions group
gr_Inc.setValue("inc_dynamic_schema->cars->color", "black");
gr_Inc.setValue("inc_dynamic_schema->cars->make", "Honda"); 
gr_Inc.setValue("inc_dynamic_schema->cars->model", "CRV");
gr_Inc.setValue("inc_dynamic_schema->cars->luxury", false); 
gr_Inc.setValue("inc_dynamic_schema->cars->cost", 25000);
gr_Inc.setValue("inc_dynamic_schema->cars->avg_mpg", 28.4);
gr_Inc.setValue("inc_dynamic_schema->cars->date_purchased", new GlideDateTime());
gr_Inc.setValue("inc_dynamic_schema->cars->total_miles", 10000.12345);
gr_Inc.insert();
```

### Scoped equivalent

To use the setValue\(\) method in a scoped application, use the corresponding scoped method: [setValue\(\)](../../glideRecordScoped/concept/c_GlideRecordScopedAPI.md#).

## GlideRecord - setWorkflow\(Boolean e\)

Enables or disables the running of business rules that might normally be triggered by subsequent actions. If the **e** parameter is set to false, an insert/update will not be audited. Auditing only happens when the parameter is set to true for a GlideRecord operation.

**Note:** The setWorkflow\(\) method is ignored when subsequently using either the deleteProblem\(\) or deleteMultiple\(\) methods to cascade delete.

**Warning:** Disabling the running of business rules can have a significant impact on your ServiceNow® instance and how it operates. Ensure that you thoroughly test this change before deploying it to production.

<table id="table_xdz_skw_dt" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

e

</td><td>

Boolean

</td><td>

Flag that indicates whether to enable or disable the running of business rules.Valid values:

-   true: Enable business rules
-   false: Disable business rules

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

```
doit('name1','name2'); 
 
function doit(username1,username2) { 
 
  var usr1 = new GlideRecord('sys_user');
  var usr2 = new GlideRecord('sys_user');
  var num = 0;
 
  if (usr1.get('user_name',username1) && usr2.get('user_name',username2)) {
    var ref;
    var dict = new GlideRecord('sys_dictionary');
    dict.addQuery('reference','sys_user');
    dict.addQuery('internal_type','reference');
    dict.query();
    while (dict.next()) {
      num = 0;
      ref = new GlideRecord(dict.name.toString());
      ref.addQuery(dict.element,usr1.sys_id);
      ref.query();
      while (ref.next()) {
        ref.setValue(dict.element.toString(),usr2.sys_id); 
        ref.setWorkflow(false);
        ref.update();
        num++;
      }
      if (num > 0) {
        gs.print(dict.element + ' changed from ' + usr1.user_name + 
          ' to ' + usr2.user_name + ' in ' + num + ' ' + dict.name + ' records');
      }
    }
  }
}
```

### Scoped equivalent

To use the setWorkflow\(\) method in a scoped application, use the corresponding scoped method: [setWorkflow\(\)](../../glideRecordScoped/concept/c_GlideRecordScopedAPI.md#).

## GlideRecord - update\(Object reason\)

Updates the GlideRecord with any changes that have been made. If the record does not exist, it is inserted.

|Name|Type|Description|
|----|----|-----------|
|reason|Object|Optional. Reason for the update. The reason appears in the audit record.|

|Type|Description|
|----|-----------|
|String|The sys\_id of the new or update record. Returns null if the update fails.|

This example updates a record in the task\_ci table.

```
var now_GR = new GlideRecord('task_ci');
now_GR.addQuery();
now_GR.query();
var count = now_GR.getRowCount();
if (count > 0) {
   var allocation = parseInt(10000 / count) / 100;
   while (now_GR.next()) {
      now_GR.u_allocation = allocation;
      now_GR.update();
   }
}
```

### Scoped equivalent

To use the update\(\) method in a scoped application, use the corresponding scoped method: [update\(\)](../../glideRecordScoped/concept/c_GlideRecordScopedAPI.md#).

## GlideRecord - updateMultiple\(\)

Updates each GlideRecord in a stated query with a specified set of changes.

For information on adding journal entries, refer to the [setJournalEntry\(\)](../../GlideElement_global/concept/c_GlideElementAPI.md#) method.

The **glide.db.forced.chunk.threshold** system property sets the threshold above which forces chunk record deletions and updates. Chunking helps to prevent non-primary key deletions on huge tables from causing replication problems. For more information, see [Available system properties](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

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

### Scoped equivalent

To use the updateMultiple\(\) method in a scoped application, use the corresponding scoped method: [updateMultiple\(\)](../../glideRecordScoped/concept/c_GlideRecordScopedAPI.md#).

## GlideRecord - updateWithReferences\(Object reason\)

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

