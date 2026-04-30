---
title: GlideQueryCondition - Global
description: The GlideQueryCondition API provides additional AND or OR conditions that can be added to the current condition, allowing you to build complex queries.Adds an AND condition to the current condition.Appends a 2-or-3 parameter OR condition to an existing GlideQueryCondition.
locale: en-US
release: xanadu
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# GlideQueryCondition- Global

The GlideQueryCondition API provides additional `AND` or `OR` conditions that can be added to the current condition, allowing you to build complex queries.

Build complex queries such as:

```
category='hardware' OR category='software' AND priority='2' AND priority='1'
```

In the case of addCondition\(\), an implied `AND` is added.

This class has no constructor. A GlideQueryCondition object is returned by the following methods:

-   addActiveQuery\(\)
-   addInactiveQuery\(\)
-   addJoinQuery\(\)
-   addNotNullQuery\(\)
-   addNullQuery\(\)
-   addQuery\(\)

If there is a complicated set of `AND` and `OR` queries, a single encoded query containing all conditions simplifies the query creation. To simplify the query creation, create a query in a list view, right-click the query, and select **Copy query**. It creates a single encoded query string to return your result set. Use that string as a parameter in an addEncodedQuery\(\) method call.

Always test queries on a sub-production instance prior to deploying them on a production instance. An incorrectly constructed encoded query, such as including an invalid field name, produces an invalid query. When the invalid query is run, the invalid part of the query condition is dropped, and the results are based on the valid part of the query, which may return all records from the table. Using an insert\(\), update\(\), deleteRecord\(\), or deleteMultiple\(\) method on bad query results can result in data loss.

You can set the **glide.invalid\_query.returns\_no\_rows** system property to true to have queries with invalid encoded queries return no records. In some cases, the query may still return records in API results even when **glide.invalid\_query.returns\_no\_rows** is set to true. This happens in queries where an invalid query term is used with a WHERE operator. In such queries, the WHERE operator ignores the invalid term\(s\) but still interprets and returns the rest of the query statement. For more information about this system property and its functionality, see [Available system properties](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## GlideQueryCondition - addCondition\(String name, String oper, Object value\)

Adds an AND condition to the current condition.

|Name|Type|Description|
|----|----|-----------|
|name|String|The name of a field.|
|oper|String|\(Optional\) The operator for the query. If you do not specify an operator, the condition uses an equals operator.|
|value|Object|The value to query on.|

|Type|Description|
|----|-----------|
|GlideQueryCondition|A reference to a GlideQueryConditon that was added to the GlideRecord.|

```
var now_GR = new GlideRecord('incident');
var qc = now_GR.addQuery('category', 'Hardware');
qc.addCondition('category', 'Network');
now_GR.addQuery('number','INC0000003');
now_GR.next();
now_GR.number;
gs.info(now_GR.getEncodedQuery());
```

### Scoped equivalent

To use the addCondition\(\) method in a scoped application, use the corresponding scoped method: [addCondition\(\)](../../glideQueryConditionScoped/concept/c_GlideQueryConditionScopedAPI.md#).

## GlideQueryCondition - addOrCondition\(String name, String oper, Object value\)

Appends a 2-or-3 parameter OR condition to an existing GlideQueryCondition.

addOrCondition\(\) works in conjunction with any of the [addQuery\(\)](../../glideRecordScoped/concept/c_GlideRecordScopedAPI.md#)methods to `OR` the specified query parameters to the query previously constructed using addQuery\(\).

addOrCondition\(\) is typically called with three parameters; table field, operator, and comparison value. It can be called with only two parameters, table field and comparison value, such as `qc.addOrCondition('category', 'software');`. The operator in this case is assumed to be "equal to".

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

Field name

</td></tr><tr><td>

oper

</td><td>

String

</td><td>

\(Optional\) Query operator. The available values are dependent on the data type of the *value* parameter.Numbers:

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
-   STARTSWITH
-   ENDSWITH
-   CONTAINS
-   DOESNOTCONTAIN

</td></tr><tr><td>

value

</td><td>

Object

</td><td>

Value on which to query \(not case-sensitive\).**Note:** All passed in arrays must contain a minimum of two elements. Single element arrays are not supported.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|GlideQueryCondition|A reference to a GlideQueryConditon that was added to the GlideRecord.|

```
var now_GR = new GlideRecord('incident');
var qc = now_GR.addQuery('category', 'Hardware');
qc.addOrCondition('category', 'Network');
now_GR.addQuery('number','INC0000003');
now_GR.next();
now_GR.number;
gs.info(now_GR.getEncodedQuery());

```

To group AND/OR statements such as `(state < 3 OR state > 5) AND (priority = 1 OR priority = 5)` use code similar to the following:

```
var myObj = new GlideRecord('incident');
var q1 = myObj.addQuery('state', '<', 3);
q1.addOrCondition('state', '>', 5);
var q2 = myObj.addQuery('priority', 1);
q2.addOrCondition('priority', 5);
myObj.query();
```

### Scoped equivalent

To use the addOrCondition\(\) method in a scoped application, use the corresponding scoped method: [addOrCondition\(\)](../../glideQueryConditionScoped/concept/c_GlideQueryConditionScopedAPI.md#).

