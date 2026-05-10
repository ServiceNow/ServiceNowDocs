---
title: GlideQueryCondition - Global
description: This API provides AND or OR conditions that can be added to the current condition, allowing you to build complex queries.Adds an AND condition to the current condition.Appends a two-or-three parameter OR condition to an existing GlideQueryCondition.Adds an AND condition to the current condition. Use this method to bypass query access.Appends a two-or-three parameter OR condition to an existing GlideQueryCondition. Use this method to bypass query access.Adds an AND condition to the current condition. Use this method to enforce query access based on the user.Appends a two-or-three parameter OR condition to an existing GlideQueryCondition. Use this method to enforce query access based on the user.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 15
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# GlideQueryCondition- Global

This API provides `AND` or `OR` conditions that can be added to the current condition, allowing you to build complex queries.

You can use this API to build complex queries such as the following:

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

If there is a complicated set of `AND` and `OR` queries, a single encoded query containing all conditions simplifies the query creation. To simplify the query creation, create a query in a list view, right-click the query, and select **Copy query**. It creates a single encoded query string to return your result set. Use that string as a parameter in an addEncodedQuery\(\) call.

Always test queries on a sub-production instance prior to deploying them on a production instance. An incorrectly constructed encoded query, such as including an invalid field name, produces an invalid query. When the invalid query is run, the invalid part of the query condition is dropped, and the results are based on the valid part of the query, which may return all records from the table. Using an insert\(\), update\(\), deleteRecord\(\), or deleteMultiple\(\) method on bad query results can result in data loss.

You can set the **glide.invalid\_query.returns\_no\_rows** system property to true to have queries with invalid encoded queries return no records. In some cases, the query may still return records in API results even when **glide.invalid\_query.returns\_no\_rows** is set to true. This happens in queries where an invalid query term is used with a WHERE operator. In such queries, the WHERE operator ignores the invalid term\(s\) but still interprets and returns the rest of the query statement. For more information about this system property and its functionality, see [Available system properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/r_AvailableSystemProperties.md).

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## GlideQueryCondition - addCondition\(String name, String oper, Object value\)

Adds an AND condition to the current condition.

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

\(Optional\) Query operator. The available values are dependent on the data type of the *value* parameter.If you do not specify an operator, the condition uses an equals operator.

Numbers:

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

The following example shows how to add an AND condition to a query.

```
var now_GR = new GlideRecord('incident');
var qc = now_GR.addQuery('category', 'Hardware');
qc.addCondition('category', 'Network');
now_GR.addQuery('number','INC0000003');
now_GR.next();
now_GR.number;
gs.info(now_GR.getEncodedQuery());
```

Output:

```
category=Hardware^ORcategory=Network^number=INC0000003
```

### Scoped equivalent

To use the addCondition\(\) method in a scoped application, use the corresponding scoped method: [addCondition\(\)](../../glideQueryConditionScoped/concept/c_GlideQueryConditionScopedAPI.md#).

## GlideQueryCondition - addOrCondition\(String name, String oper, Object value\)

Appends a two-or-three parameter OR condition to an existing GlideQueryCondition.

This method works in conjunction with [GlideRecord addQuery\(\)](../../GlideRecord/concept/c_GlideRecordAPI.md#) to `OR` the specified query parameters to the query previously constructed using addQuery\(\).

The addOrCondition\(\) can be called with only two parameters, table field and comparison value, such as `qc.addOrCondition('category', 'software');`. The operator in this case is assumed to be "equal to".

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

\(Optional\) Query operator. The available values are dependent on the data type of the *value* parameter.If you do not specify an operator, the condition uses an equals operator.

Numbers:

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

The following example shows how to add an OR condition to a query.

```
var now_GR = new GlideRecord('incident');
var qc = now_GR.addQuery('category', 'Hardware');
qc.addOrCondition('category', 'Network');
now_GR.addQuery('number','INC0000004');
now_GR.next();
now_GR.number;
gs.info(now_GR.getEncodedQuery());
```

Output:

```
category=Hardware^ORcategory=Network^number=INC0000004
```

To group AND/OR statements to make complex queries, such as getting 10 incidents with a \(state less than 3 OR greater than 5\) AND \(priority is 1 OR priority is 5\).

```
var myObj = new GlideRecord('incident');
var q1 = myObj.addQuery('state', '<', 3);
q1.addOrCondition('state', '>', 5);
var q2 = myObj.addQuery('priority', 1);
q2.addOrCondition('priority', 5);
myObj.setLimit(10);
myObj.query();

while (myObj.next()) {
  gs.info('Incident: ' + myObj.getValue('number') + ' State: ' + myObj.getValue('state') + ' Priority: ' + myObj.getValue('priority'));
}
```

Output:

```
Incident: INC0000001 State: 7 Priority: 1
Incident: INC0000004 State: 7 Priority: 1
Incident: INC0000012 State: 7 Priority: 5
Incident: INC0000013 State: 7 Priority: 1
Incident: INC0000024 State: 7 Priority: 5
Incident: INC0000028 State: 7 Priority: 5
Incident: INC0000031 State: 2 Priority: 1
Incident: INC0000057 State: 7 Priority: 5
Incident: INC0000057 State: 2 Priority: 5
Incident: INC0000058 State: 7 Priority: 5
```

### Scoped equivalent

To use the addOrCondition\(\) method in a scoped application, use the corresponding scoped method: [addOrCondition\(\)](../../glideQueryConditionScoped/concept/c_GlideQueryConditionScopedAPI.md#).

## GlideQueryCondition - addSystemCondition\(String name, String oper, Object value\)

Adds an AND condition to the current condition. Use this method to bypass query access.

Use this method when system-level access is intended, so that query ACL enforcement is explicitly bypassed for the user. Use[addUserCondition\(\)](c_GlideQueryConditionAPI.md#) to enforce query access.

Additional methods for system-level access that bypass query ACL checks:

-   [addSystemOrCondition\(\)](c_GlideQueryConditionAPI.md#)
-   [GlideRecord - addSystemEncodedQuery\(\)](../../GlideRecord/concept/c_GlideRecordAPI.md#)
-   [GlideRecord - addSystemOrderBy\(\)](../../GlideRecord/concept/c_GlideRecordAPI.md#)
-   [GlideRecord - addSystemOrderByDesc\(\)](../../GlideRecord/concept/c_GlideRecordAPI.md#)
-   [GlideRecord - addSystemQuery\(\)](../../GlideRecord/concept/c_GlideRecordAPI.md#)

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

\(Optional\) Query operator. The available values are dependent on the data type of the *value* parameter.If you do not specify an operator, the condition uses an equals operator.

Numbers:

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

To group AND statements to make complex queries, such as getting 20 incidents with a \(state less than 3 AND not 2\) and \(priority is greater than 1 AND priority is not 5\).

```
var myObj = new GlideRecord('incident');
var q1 = myObj.addSystemQuery('state', '<', 3);
q1.addSystemCondition('state', '!=', 2);
var q2 = myObj.addSystemQuery('priority', '>', 1);
q2.addSystemCondition('priority', '!=', 5);
myObj.setLimit(20);
myObj.query();

while (myObj.next()) {
  gs.info('Incident: ' + myObj.getValue('number') + ' State: ' + myObj.getValue('state') + ' Priority: ' + myObj.getValue('priority'));
}
```

Output:

```
Incident: INC0011238 State: 1 Priority: 4
Incident: INC0010127 State: 1 Priority: 2
Incident: INC0010143 State: 1 Priority: 2
Incident: INC0011760 State: 1 Priority: 2
Incident: INC0010708 State: 1 Priority: 3
Incident: INC0013048 State: 1 Priority: 4
Incident: INC0010658 State: 1 Priority: 2
Incident: INC0012021 State: 1 Priority: 3
Incident: INC0013308 State: 1 Priority: 4
Incident: INC0010155 State: 1 Priority: 3
Incident: INC0013312 State: 1 Priority: 4
Incident: INC0013049 State: 1 Priority: 3
Incident: INC0010068 State: 1 Priority: 4
Incident: INC0010135 State: 1 Priority: 2
Incident: INC0010132 State: 1 Priority: 4
Incident: INC0010700 State: 1 Priority: 3
Incident: INC0013311 State: 1 Priority: 2
Incident: INC0011758 State: 1 Priority: 4
Incident: INC0012278 State: 1 Priority: 3
Incident: INC0013306 State: 1 Priority: 4
```

## GlideQueryCondition - addSystemOrCondition\(String name, String oper, Object value\)

Appends a two-or-three parameter OR condition to an existing GlideQueryCondition. Use this method to bypass query access.

Use this method when system-level access is intended, so that query ACL enforcement is explicitly bypassed for the user. Use[addUserOrCondition](c_GlideQueryConditionAPI.md#) to enforce query access.

Additional methods for system-level access that bypass query ACL checks:

-   [addSystemCondition\(\)](c_GlideQueryConditionAPI.md#)
-   [GlideRecord - addSystemEncodedQuery\(\)](../../GlideRecord/concept/c_GlideRecordAPI.md#)
-   [GlideRecord - addSystemOrderBy\(\)](../../GlideRecord/concept/c_GlideRecordAPI.md#)
-   [GlideRecord - addSystemOrderByDesc\(\)](../../GlideRecord/concept/c_GlideRecordAPI.md#)
-   [GlideRecord - addSystemQuery\(\)](../../GlideRecord/concept/c_GlideRecordAPI.md#)

The addSystemOrCondition\(\) method works with the [GlideRecord addSystemQuery\(\)](../../GlideRecord/concept/c_GlideRecordAPI.md#) method to `OR` the specified query parameters to the query previously constructed using addSystemQuery\(\).

<table id="table_vy2_625_jq" class="parameters"><thead><tr><th>

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

\(Optional\) Query operator. The available values are dependent on the data type of the *value* parameter.If you do not specify an operator, the condition uses an equals operator.

Numbers:

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

To group AND/OR statements to make complex queries, such as getting 20 incidents with a \(state less than 3 OR greater than 5\) AND \(priority is 1 OR priority is 5\).

```
var myObj = new GlideRecord('incident');
var q1 = myObj.addSystemQuery('state', '<', 3);
q1.addSystemOrCondition('state', '>', 5);
var q2 = myObj.addSystemQuery('priority', 1);
q2.addSystemOrCondition('priority', 5);
myObj.setLimit(20);
myObj.query();

while (myObj.next()) {
  gs.info('Incident: ' + myObj.getValue('number') + ' State: ' + myObj.getValue('state') + ' Priority: ' + myObj.getValue('priority'));
}
```

Output:

```
Incident: INC0000001 State: 7 Priority: 1
Incident: INC0000004 State: 7 Priority: 1
Incident: INC0000012 State: 7 Priority: 5
Incident: INC0000013 State: 7 Priority: 1
Incident: INC0000024 State: 7 Priority: 5
Incident: INC0000028 State: 7 Priority: 5
Incident: INC0000031 State: 2 Priority: 1
Incident: INC0000057 State: 7 Priority: 5
Incident: INC0000057 State: 2 Priority: 5
Incident: INC0000058 State: 7 Priority: 5
Incident: INC0000058 State: 2 Priority: 5
Incident: INC0000059 State: 7 Priority: 5
Incident: INC0000060 State: 7 Priority: 5
Incident: INC0000061 State: 7 Priority: 5
Incident: INC0000062 State: 7 Priority: 5
Incident: INC0000064 State: 7 Priority: 5
Incident: INC0000065 State: 7 Priority: 5
Incident: INC0000066 State: 7 Priority: 5
Incident: INC0000069 State: 7 Priority: 5
Incident: INC0000072 State: 7 Priority: 5
```

## GlideQueryCondition - addUserCondition\(String name, String oper, Object value\)

Adds an AND condition to the current condition. Use this method to enforce query access based on the user.

This method returns only records that the current user has query access to \(based on ACLs\).

Related methods:

-   [addCondition\(\)](../../glideQueryConditionScoped/concept/c_GlideQueryConditionScopedAPI.md#) provides the same functionality without ACL enforcement.
-   [addSystemCondition\(\)](c_GlideQueryConditionAPI.md#) bypasses query access checks.

Additional methods for enforcing query ACL checks:

-   [addUserOrCondition\(\)](c_GlideQueryConditionAPI.md#)
-   [GlideRecord - addUserEncodedQuery\(\)](../../GlideRecord/concept/c_GlideRecordAPI.md#)
-   [GlideRecord - addUserOrderBy\(\)](../../GlideRecord/concept/c_GlideRecordAPI.md#)
-   [GlideRecord - addUserOrderByDesc\(\)](../../GlideRecord/concept/c_GlideRecordAPI.md#)
-   [GlideRecord - addUserQuery\(\)](../../GlideRecord/concept/c_GlideRecordAPI.md#)

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

\(Optional\) Query operator. The available values are dependent on the data type of the *value* parameter.If you do not specify an operator, the condition uses an equals operator.

Numbers:

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

To group AND statements to make complex queries, such as getting 20 incidents with a \(state less than 3 AND not 2\) and \(priority is greater than 1 AND priority is not 5\).

```
var myObj = new GlideRecord('incident');
var q1 = myObj.addUserQuery('state', '<', 3);
q1.addUserCondition('state', '!=', 2);
var q2 = myObj.addUserQuery('priority', '>', 1);
q2.addUserCondition('priority', '!=', 5);
myObj.setLimit(20);
myObj.query();

while (myObj.next()) {
  gs.info('Incident: ' + myObj.getValue('number') + ' State: ' + myObj.getValue('state') + ' Priority: ' + myObj.getValue('priority'));
}
```

Output:

```
Incident: INC0011238 State: 1 Priority: 4
Incident: INC0010127 State: 1 Priority: 2
Incident: INC0010143 State: 1 Priority: 2
Incident: INC0011760 State: 1 Priority: 2
Incident: INC0010708 State: 1 Priority: 3
Incident: INC0013048 State: 1 Priority: 4
Incident: INC0010658 State: 1 Priority: 2
Incident: INC0012021 State: 1 Priority: 3
Incident: INC0013308 State: 1 Priority: 4
Incident: INC0010155 State: 1 Priority: 3
Incident: INC0013312 State: 1 Priority: 4
Incident: INC0013049 State: 1 Priority: 3
Incident: INC0010068 State: 1 Priority: 4
Incident: INC0010135 State: 1 Priority: 2
Incident: INC0010132 State: 1 Priority: 4
Incident: INC0010700 State: 1 Priority: 3
Incident: INC0013311 State: 1 Priority: 2
Incident: INC0011758 State: 1 Priority: 4
Incident: INC0012278 State: 1 Priority: 3
Incident: INC0013306 State: 1 Priority: 4
```

## GlideQueryCondition - addUserOrCondition\(String name, String oper, Object value\)

Appends a two-or-three parameter OR condition to an existing GlideQueryCondition. Use this method to enforce query access based on the user.

This method returns only records that the current user has query access to \(based on ACLs\).

The addUserOrCondition\(\) method works with the [GlideRecord addUserQuery\(\)](../../GlideRecord/concept/c_GlideRecordAPI.md#) method to `OR` the specified query parameters to the query previously constructed using addUserQuery\(\).

Related methods:

-   [addOrCondition\(\)](../../glideQueryConditionScoped/concept/c_GlideQueryConditionScopedAPI.md#) provides the same functionality without ACL enforcement.
-   [addSystemOrCondition\(\)](c_GlideQueryConditionAPI.md#) bypasses query access checks.

Additional methods for enforcing query ACL checks:

-   [addUserCondition\(\)](c_GlideQueryConditionAPI.md#)
-   [GlideRecord - addUserEncodedQuery\(\)](../../GlideRecord/concept/c_GlideRecordAPI.md#)
-   [GlideRecord - addUserOrderBy\(\)](../../GlideRecord/concept/c_GlideRecordAPI.md#)
-   [GlideRecord - addUserOrderByDesc\(\)](../../GlideRecord/concept/c_GlideRecordAPI.md#)
-   [GlideRecord - addUserQuery\(\)](../../GlideRecord/concept/c_GlideRecordAPI.md#)

<table id="table_vy2_625_jq" class="parameters"><thead><tr><th>

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

\(Optional\) Query operator. The available values are dependent on the data type of the *value* parameter.If you do not specify an operator, the condition uses an equals operator.

Numbers:

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

To group AND/OR statements to make complex queries, such as getting 20 incidents with a \(state less than 3 OR greater than 5\) AND \(priority is 1 OR priority is 5\).

```
var myObj = new GlideRecord('incident');
var q1 = myObj.addUserQuery('state', '<', 3);
q1.addUserOrCondition('state', '>', 5);
var q2 = myObj.addUserQuery('priority', 1);
q2.addUserOrCondition('priority', 5);
myObj.setLimit(20);
myObj.query();

while (myObj.next()) {
  gs.info('Incident: ' + myObj.getValue('number') + ' State: ' + myObj.getValue('state') + ' Priority: ' + myObj.getValue('priority'));
}
```

Output:

```
Incident: INC0000001 State: 7 Priority: 1
Incident: INC0000004 State: 7 Priority: 1
Incident: INC0000012 State: 7 Priority: 5
Incident: INC0000013 State: 7 Priority: 1
Incident: INC0000024 State: 7 Priority: 5
Incident: INC0000028 State: 7 Priority: 5
Incident: INC0000031 State: 2 Priority: 1
Incident: INC0000057 State: 7 Priority: 5
Incident: INC0000057 State: 2 Priority: 5
Incident: INC0000058 State: 7 Priority: 5
Incident: INC0000058 State: 2 Priority: 5
Incident: INC0000059 State: 7 Priority: 5
Incident: INC0000060 State: 7 Priority: 5
Incident: INC0000061 State: 7 Priority: 5
Incident: INC0000062 State: 7 Priority: 5
Incident: INC0000064 State: 7 Priority: 5
Incident: INC0000065 State: 7 Priority: 5
Incident: INC0000066 State: 7 Priority: 5
Incident: INC0000069 State: 7 Priority: 5
Incident: INC0000072 State: 7 Priority: 5
```

