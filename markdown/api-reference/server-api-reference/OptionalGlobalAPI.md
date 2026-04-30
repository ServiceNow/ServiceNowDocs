---
title: Optional - Scoped, Global
description: The Optional API interacts with a single record returned by the GlideQuery, Stream, or GlideRecord APIs, even when it does not exist. Write scripts that are less likely to result in an error by handling null or undefined query results.Returns an empty Optional object. Use this method in an Else clause to handle a query that might not return a result.Applies a predicate function, a function that takes a single value and returns true or false, to the record inside the Optional object. If the function returns true, the method returns the Optional record unchanged. If the function returns false, it returns an empty Optional object.Applies a function that returns an Optional object to the result of a query. Use this method to perform a second query using the result of the first.Returns the record inside the Optional object, or throws an error if the query does not return a record.Applies a function to the record within an Optional object. If the Optional object does not contain a record, the function does not execute.Returns true if the Optional object is empty.Checks whether an Optional object contains a value.Returns a new Optional object. Instead of containing the record, the object contains a function to get the record that is only called if and when requested in the code.Applies a function to the result of a query.Wraps a given value in an Optional object. For example, you can wrap the result of a GlideRecord query in an Optional object to use the associated methods.Adds a default value within the Optional object if the query does not return any results.
locale: en-US
release: yokohama
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 10
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# Optional - Scoped, Global

The Optional API interacts with a single record returned by the GlideQuery, Stream, or GlideRecord APIs, even when it does not exist. Write scripts that are less likely to result in an error by handling null or undefined query results.

You can get an Optional object in these ways:

-   Return an Optional object from these methods in the GlideQuery class. For more information, see [GlideQuery](../../GlideQuery/concept/GlideQueryGlobalAPI.md#).
    -   [getBy\(\)](../../GlideQuery/concept/GlideQueryGlobalAPI.md#)
    -   [get\(\)](../../GlideQuery/concept/GlideQueryGlobalAPI.md#)
    -   [insert\(\)](../../GlideQuery/concept/GlideQueryGlobalAPI.md#)
    -   [insertOrUpdate\(\)](../../GlideQuery/concept/GlideQueryGlobalAPI.md#)
    -   [update\(\)](../../GlideQuery/concept/GlideQueryGlobalAPI.md#)
    -   [selectOne\(\)](../../GlideQuery/concept/GlideQueryGlobalAPI.md#)
    -   [avg\(\)](../../GlideQuery/concept/GlideQueryGlobalAPI.md#)
    -   [max\(\)](../../GlideQuery/concept/GlideQueryGlobalAPI.md#)
    -   [min\(\)](../../GlideQuery/concept/GlideQueryGlobalAPI.md#)
    -   [sum\(\)](../../GlideQuery/concept/GlideQueryGlobalAPI.md#)
-   Return an Optional object from the [find\(\)](../../Stream/concept/StreamGlobalAPI.md#) method in the Stream class. For more information on Stream, see the [Stream](../../Stream/concept/StreamGlobalAPI.md#) API.
-   Use the [lazy\(\)](OptionalGlobalAPI.md#) method to generate the value of the Optional if ever needed.

These methods are static and do not require an instance of the class:

-   [lazy\(\)](OptionalGlobalAPI.md#)
-   [of\(\)](OptionalGlobalAPI.md#)
-   [empty\(\)](OptionalGlobalAPI.md#)

You can use these static methods with any API that returns a single value such as [GlideRecord](../../glideRecordScoped/concept/c_GlideRecordScopedAPI.md#).

Use the Optional API in scoped or global server-side scripts. This API requires the GlideQuery \[com.sn\_glidequery\] plugin.

## Implementation

This API can work with the [GlideQuery](../../GlideQuery/concept/GlideQueryGlobalAPI.md#) and [Stream](../../Stream/concept/StreamGlobalAPI.md#) APIs in a builder pattern where the method calls chain together, each method building on the returned result of the previous method. Use methods to define the attributes of the query. The methods do not execute until you call a terminal method, a method that returns a query result, allowing you to define the requirements of the query before executing it.

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

## Terminal methods

For performance reasons, a query only fetches data when you call a terminal method. These are the terminal methods from the Optional class:

-   [get\(\)](OptionalGlobalAPI.md#)
-   [orElse\(\)](OptionalGlobalAPI.md#)
-   [ifPresent\(\)](OptionalGlobalAPI.md#)
-   [isEmpty\(\)](OptionalGlobalAPI.md#)
-   [isPresent\(\)](OptionalGlobalAPI.md#)

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## Optional - empty\(String reason\)

Returns an empty Optional object. Use this method in an Else clause to handle a query that might not return a result.

**Note:** This method is static. You do not need an instance of the class to use this method.

|Name|Type|Description|
|----|----|-----------|
|reason|String|Optional. Reason displayed in the log when Optional.get\(\) is called on the empty Optional object.|

|Type|Description|
|----|-----------|
|Optional|Object used to interact with a single record.|

This example shows you how to generate an empty Optional object when a query does not return a result.

```
var now_GR = new GlideRecord('task');
now_GR.addQuery('approval', 'not requested'); 
now_GR.query();
var optional;
if (now_GR.next()) {
optional = Optional.of(now_GR.getUniqueValue());
} else {
    optional = Optional.empty("no results");
}

gs.info(optional.get());
```

Output:

```
NiceError: [2020-08-26T23:23:37.402Z]: get() called on empty Optional: no results
```

## Optional - filter\(Function predicate\)

Applies a predicate function, a function that takes a single value and returns true or false, to the record inside the Optional object. If the function returns true, the method returns the Optional record unchanged. If the function returns false, it returns an empty Optional object.

|Name|Type|Description|
|----|----|-----------|
|predicate|Function|Predicate function to apply to the value inside the Optional object. Must return a Boolean value.|

|Type|Description|
|----|-----------|
|Optional|Object used to interact with a single record.|

This example shows you how to apply a filter function to an Optional result.

```
var filteredQuery = new global.GlideQuery('sys_user')
    .getBy({ sys_id: 'f682abf03710200044e0bfc8bcbe5d38' }, ['phone'])
    .filter(function (user) {
        return phoneRegex.test(user.phone);
    });
```

## Optional - flatMap\(Function fn\)

Applies a function that returns an Optional object to the result of a query. Use this method to perform a second query using the result of the first.

|Name|Type|Description|
|----|----|-----------|
|fn|Function|Function to apply to the results of the query that returned the Optional object.|

|Type|Description|
|----|-----------|
|Optional|Object used to interact with a single record.|

This example shows how to execute a query of the User table based on the result of a previous query.

```
new global.GlideQuery('alm_asset')
    .whereNotNull('owned_by')
    .selectOne('owned_by')
    .flatMap(function (asset) {
        return new global.GlideQuery('sys_user')
            .getBy({ sys_id: asset.owned_by }, ['first_name', 'last_name', 'company.name'])
    })
    .ifPresent(GQ.jsonDebug);
```

Output:

```
{
  "sys_id": "46d59205a9fe198101d603f5de37bfa3",
  "first_name": "John",
  "last_name": "Bohnhamn",
  "company": {
    "name": "ACME North America"
  }
}
```

## Optional - get\(\)

Returns the record inside the Optional object, or throws an error if the query does not return a record.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Any|The record inside the Optional object. If the value is null or undefined, the system throws an error.|

This example shows how to get the value of a single record.

```
var value = new global.GlideQuery('sys_user')
    .selectOne('first_name') //Returns the result of the query inside an Optional object
    .get(); //Calls Optional.get() on the Optional object

gs.info(JSON.stringify(value));
```

Output:

```
{
   "first_name":"fred",
   "sys_id":"005d500b536073005e0addeeff7b12f4"
}
```

## Optional - ifPresent\(Function fn\)

Applies a function to the record within an Optional object. If the Optional object does not contain a record, the function does not execute.

|Name|Type|Description|
|----|----|-----------|
|fn|Function|The function to apply to the record within the Optional object.|

|Type|Description|
|----|-----------|
|None| |

This example shows how to print a value if it exists.

```
var user = new global.GlideQuery('sys_user')
    .where('sys_id', 'f682abf03710200044e0bfc8bcbe5d38')
    .selectOne('zip')
    .ifPresent(function (user) {
      gs.info('Zip Code: ' + user.zip);
    });
```

## Optional - isEmpty\(\)

Returns true if the Optional object is empty.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_zhd_b1l_4mb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the result of a query contains a value.

 Valid values:

-   true: The query returns null or undefined.
-   false: The query returns a value.

</td></tr></tbody>
</table>This example shows how to check whether the result of a query is empty.

```
var checkEmpty = new global.GlideQuery('sys_user')
    .where('last_name', 'Barker')
    .selectOne()
    .isEmpty();

gs.info(checkEmpty);
```

Output:

```
true
```

## Optional - isPresent\(\)

Checks whether an Optional object contains a value.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_jcx_c1l_4mb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the result of a query contains a value.

 Valid values:

-   true: The query returns a value.
-   false: The query returns null or undefined.

</td></tr></tbody>
</table>This example shows how to check whether a query returns a result.

```
var checkPresent = new global.GlideQuery('sys_user')    
   .where('last_name', 'Luddy')
   .selectOne('first_name')
   .isPresent();

gs.info(checkPresent);
```

Output:

```
true
```

## Optional - lazy\(Function lazyGetFn\)

Returns a new Optional object. Instead of containing the record, the object contains a function to get the record that is only called if and when requested in the code.

Use this method to delay getting the value until it's needed. You might do this if requesting the value from a slow source and don't want to slow down your code unnecessarily. Otherwise, you can return an Optional object using the [GlideQuery](../../GlideQuery/concept/GlideQueryGlobalAPI.md#) and [Stream](../../Stream/concept/StreamGlobalAPI.md#) APIs.

**Note:** This method is static. You do not need an instance of the class to use this method.

<table id="table_edm_lwj_5mb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

lazyGetFn

</td><td>

Function

</td><td>

Function that returns a single record as a result of a query. For example: ```
var userGr = new GlideRecord('sys_user');
```

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|Optional|Object containing the result of the query in the format `Optional<result>`.|

This example shows how to get an Optional object based on a GlideRecord query.

```
var userOptional = global.Optional.lazy(function () {
    var userGr = new GlideRecord('sys_user');
    userGr.setLimit(1);
    userGr.query();
    return userGr.next() ? userGr.getUniqueValue() : null;
});

gs.info(userOptional);
```

Output:

```
Optional<005d500b536073005e0addeeff7b12f4>
```

## Optional - map\(Function fn\)

Applies a function to the result of a query.

|Name|Type|Description|
|----|----|-----------|
|fn|Function|Function to apply to the result of the query.|

|Type|Description|
|----|-----------|
|Optional|Object containing the results of the query updated by the function in the format `Optional<result>`.|

This example shows how to apply a function that transforms a value to upper case to the result of a query.

```
var value = new global.GlideQuery('sys_user')
    .whereNotNull('first_name')
    .selectOne('first_name')
    .map(function (user) {
	       return user.first_name.toUpperCase();
    });

gs.info(value);
```

Output:

```
Optional<ABEL>
```

## Optional - of\(Any value\)

Wraps a given value in an Optional object. For example, you can wrap the result of a GlideRecord query in an Optional object to use the associated methods.

**Note:** This method is static. You do not need an instance of the class to use this method.

|Name|Type|Description|
|----|----|-----------|
|value|Any|Value inside the Optional object.|

|Type|Description|
|----|-----------|
|Optional|Object containing the passed-in value in the format `Optional<value>`.|

This example shows you how to generate an Optional object based on a GlideRecord query.

```
var now_GR = new GlideRecord('task');
now_GR.addQuery('approval', 'not requested'); 
now_GR.query();
var optional;
if (now_GR.next()) {
optional = Optional.of(now_GR.getUniqueValue());
} else {
    optional = Optional.empty("no results");
}

gs.info(optional.get());
```

Output:

```
00c269162d761010f87708b56757cbb3
```

## Optional - orElse\(Any defaultValue\)

Adds a default value within the Optional object if the query does not return any results.

|Name|Type|Description|
|----|----|-----------|
|defaultValue|Any|Value within the Optional object if the query does not return any results.|

|Type|Description|
|----|-----------|
|Any|Value within the Optional object if the query does not return any results.|

This example shows how to return a value, even when the query is incorrect.

```
var user = new global.GlideQuery('sys_user')
    .get('1234', ['first_name', 'last_name'])
    .orElse({ first_name: 'Default', last_name: 'User' });

gs.info(JSON.stringify(user))
```

Output:

```
{
   "first_name":"Default",
   "last_name":"User"
}
```

