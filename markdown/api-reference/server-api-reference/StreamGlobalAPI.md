---
title: Stream - Scoped, Global
description: The Stream API provides methods to interact with a stream of items such as records. For example, you can use the forEach\(\) method to update the state of each record in a stream returned by the GlideQuery API.Instantiates a Stream object.Returns results in batches of arrays, each containing the number of records passed to the method.Applies a predicate function to every item in the Stream object. If the predicate returns true for every item in the stream, the method returns true. If the predicate returns false for any item in the stream, the method returns false.Applies a predicate function to each item in the Stream object. If the predicate returns true, the method returns the stream. If the predicate returns false, it returns an empty Stream object.Returns the first record or item in the Stream object that matches the predicate function. If no predicate function is provided, then the method returns the first record or item in the Stream.Applies a function to every item in a stream. Returns another stream that you can iterate over.Applies the specified function to each record or item in the stream.Returns a Stream object that contains the values from the provided array.Limits the number of results returned by the stream.Applies a function to each item in a stream and returns the updated Stream object.Executes a reducer function on each item in the stream, resulting in single output value.Applies a predicate function, a function that takes a single value and returns true or false, to each item in the stream. If the predicate returns true for any item in the stream, the method returns true.Returns an array containing the given number of items from the stream.
locale: en-US
release: xanadu
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 13
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# Stream - Scoped, Global

The Stream API provides methods to interact with a stream of items such as records. For example, you can use the forEach\(\) method to update the state of each record in a stream returned by the GlideQuery API.

You can get a Stream object in these ways:

-   Instantiate a Stream object using the constructor.
-   Return a Stream object from the GlideQuery.select\(\) method. For more information, see [GlideQuery](../../GlideQuery/concept/GlideQueryGlobalAPI.md#).

This method is static and does not require an instance of the class: [fromArray\(\)](StreamGlobalAPI.md#).

Use the Stream API in scoped or global server-side scripts. This API requires the GlideQuery \[com.sn\_glidequery\] plugin.

## Implementation

This API can work with the [GlideQuery](../../GlideQuery/concept/GlideQueryGlobalAPI.md#) and [Optional](../../Optional/concept/OptionalGlobalAPI.md#) APIs in a builder pattern where the method calls chain together, each method building on the returned result of the previous method. Use methods to define the attributes of the query. The methods do not execute until you call a terminal method, a method that returns a query result, allowing you to define the requirements of the query before executing it.

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

For performance reasons, a query only fetches data when you call a terminal method. These are the terminal methods from the Stream class:

-   [every\(\)](StreamGlobalAPI.md#)
-   [find\(\)](StreamGlobalAPI.md#)
-   [forEach\(\)](StreamGlobalAPI.md#)
-   [reduce\(\)](StreamGlobalAPI.md#)
-   [some\(\)](StreamGlobalAPI.md#)
-   [toArray\(\)](StreamGlobalAPI.md#)

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## Stream - Stream\(Function nextFn\)

Instantiates a Stream object.

Instead of using this constructor, you can return a Stream object based on a query using the [GlideQuery](../../GlideQuery/concept/GlideQueryGlobalAPI.md#) API.

|Name|Type|Description|
|----|----|-----------|
|nextFn|Function|A function that retrieves the next item in the stream.|

This example shows you how to create a Stream object based on a random number generator. Make sure to include the limit\(\) method to avoid creating an infinite loop.

```
new Stream(Math.random)
   .map(Math.round)
   .map(function (num) { 
      return num === 1 ? 'heads' : 'tails'; 
   })
   .limit(10)
   .forEach(gs.info)

```

Output:

```
*** Script: tails
*** Script: heads
*** Script: tails
*** Script: heads
*** Script: tails
*** Script: heads
*** Script: tails
*** Script: tails
*** Script: tails
*** Script: tails
```

## Stream - chunk\(Number count\)

Returns results in batches of arrays, each containing the number of records passed to the method.

|Name|Type|Description|
|----|----|-----------|
|count|Number|Number of records in each array returned from the stream.|

|Type|Description|
|----|-----------|
|Stream|Object used to interact with a stream of items such as records.|

This example shows how to query a table and chunk the result into batches of arrays.

```
var chunkResult = new GlideQuery('cmdb_ci_hardware')
    .select('asset', 'purchase_date')
    .limit(10)
    .chunk(5) //Returns arrays of 5 sys_ids at a time
    .forEach(function (chunk){ 
        gs.info(JSON.stringify(chunk, null, 2)); 
    });
```

Output:

```
*** Script: [
  {
    "asset": "2fa9680d3790200044e0bfc8bcbe5dfb",
    "purchase_date": "2022-02-28",
    "sys_id": "2ba9680d3790200044e0bfc8bcbe5dfc"
  },
  {
    "asset": "73c1fa8837f3100044e0bfc8bcbe5ded",
    "purchase_date": "2017-12-05",
    "sys_id": "b4fd7c8437201000deeabfc8bcbe5dc1"
  },
  {
    "asset": "cbc1ba8837f3100044e0bfc8bcbe5dad",
    "purchase_date": "2017-12-05",
    "sys_id": "25fd3c8437201000deeabfc8bcbe5dea"
  },
  {
    "asset": "8fc1ba8837f3100044e0bfc8bcbe5da9",
    "purchase_date": null,
    "sys_id": "108a9205c611227500786e160f9d343e"
  },
  {
    "asset": "27c1fa8837f3100044e0bfc8bcbe5dd8",
    "purchase_date": "2017-06-06",
    "sys_id": "a9a2d111c611227601fb37542399caa8"
  }
]
*** Script: [
  {
    "asset": "93c1fa8837f3100044e0bfc8bcbe5d30",
    "purchase_date": "2017-12-05",
    "sys_id": "6b43105c37301000deeabfc8bcbe5db2"
  },
  {
    "asset": "a2c0b1213784200044e0bfc8bcbe5de3",
    "purchase_date": "2017-12-05",
    "sys_id": "aac0b1213784200044e0bfc8bcbe5de3"
  },
  {
    "asset": "33c1fa8837f3100044e0bfc8bcbe5def",
    "purchase_date": "2017-12-05",
    "sys_id": "d0e8761137201000deeabfc8bcbe5da7"
  },
  {
    "asset": "53c1fa8837f3100044e0bfc8bcbe5d1f",
    "purchase_date": "2017-12-05",
    "sys_id": "53fdbc8437201000deeabfc8bcbe5d10"
  },
  {
    "asset": "f1c031213784200044e0bfc8bcbe5de0",
    "purchase_date": "2017-12-05",
    "sys_id": "71c031213784200044e0bfc8bcbe5de1"
  }
]
```

This example shows how to create a child query using batches of IDs. When you call the flatMap\(\) method after using the chunk\(\) method, the system iterates over the batch of records instead of each individual record.

```
var chunkResult = new global.GlideQuery('cmdb_ci_hardware')
    .select('sys_id')
    .map(function (device) { return device.sys_id; })
    .chunk(5) //Returns arrays of 5 sys_ids at a time
    .flatMap(function (deviceIds) {
        return new GlideQuery('cmdb_sam_sw_install')
            .where('installed_on', 'IN', deviceIds)
            .select('software_model', 'installed_on');
    })

gs.info(JSON.stringify(chunkResult));
```

## Stream - every\(Function predicate\)

Applies a predicate function to every item in the Stream object. If the predicate returns true for every item in the stream, the method returns true. If the predicate returns false for any item in the stream, the method returns false.

|Name|Type|Description|
|----|----|-----------|
|predicate|Function|Predicate function to apply to every record or item inside the Stream object. The function must take each item in the stream as input and return a boolean.|

<table id="table_uyn_x2f_4mb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the predicate function returns true for every item in the stream.

 Valid values:

-   true: The predicate function returns true for every item in the stream.
-   false: The predicate function does not return true for every item in the stream.

</td></tr></tbody>
</table>This example shows how to apply a predicate function to every item in a stream.

```
var hasOnlyShortDescriptions = new global.GlideQuery('task')
   .whereNotNull('description')
   .select('description')
   .every(function (t) { 
       return t.description.length < 10; 
       });

gs.info(hasOnlyShortDescriptions);
```

Output:

```
false
```

## Stream - filter\(Function predicate\)

Applies a predicate function to each item in the Stream object. If the predicate returns true, the method returns the stream. If the predicate returns false, it returns an empty Stream object.

For better performance, use the where\(\), whereNotNull\(\), and whereNull\(\) methods in the GlideQuery class instead of this method where possible. See [GlideQuery](../../GlideQuery/concept/GlideQueryGlobalAPI.md#).

|Name|Type|Description|
|----|----|-----------|
|predicate|Function|Predicate function to apply to every record or item inside the Stream object. The function must take each item in the stream as input and return a boolean.|

|Type|Description|
|----|-----------|
|Stream|Object used to interact with a stream of items such as records.|

This example shows how to check all records in the Task table against a defined filter. If the records match the filter, the system returns the stream of records. Otherwise, it returns an empty Stream object.

```
var shoutingTasks = new global.GlideQuery('task')
   .whereNotNull('description')
   .select('description')
   .filter(function (task) { 
       return task.description.toUpperCase() === task.description; 
   })
```

## Stream - find\(Function predicate\)

Returns the first record or item in the Stream object that matches the predicate function. If no predicate function is provided, then the method returns the first record or item in the Stream.

|Name|Type|Description|
|----|----|-----------|
|predicate|Function|Optional. Predicate function to apply to the items inside the Stream object. The function must take each item in the stream as input and return a boolean.|

|Type|Description|
|----|-----------|
|Optional|Object containing the returned record.|

This example shows how to return the first record from the stream.

```
var UserOptional = new global.GlideQuery('sys_user')
   .where('active', true)
   .where('company.name', 'ServiceNow')
   .select()
   .find()
   .map(function (user) { 
      return JSON.stringify(user); 
   })

gs.info(UserOptional);
```

Output:

```
Optional<{"sys_id":"babb4639b76233004fbc2089ee11a97f"}>
```

## Stream - flatMap\(function fn\)

Applies a function to every item in a stream. Returns another stream that you can iterate over.

Use this method instead of map\(\) if the function returns a second stream of records.

|Name|Type|Description|
|----|----|-----------|
|fn|Function|Function to apply to the result of the query that returns a Stream object.|

|Type|Description|
|----|-----------|
|Stream|Object containing the stream of records updated after applying the function.|

This example shows you how to query the User table and then create a child query from the result. This example executes an N+1 query, which can cause performance issues. Avoid this use case in a production environment.

```
var records = new global.GlideQuery('sys_user')
   .where('last_login', '>', '2015-12-31')
   .select('first_name', 'last_name')
   .flatMap(function (u) {
      return new global.GlideQuery('task')
           .where('closed_by', u.sys_id)
           .select('closed_at', 'description')
           .map(function (t) {
                return {
                    first_name: u.first_name,
                    last_name: u.last_name,
                    description: t.description,
                    closed_at: t.closed_at
                 };
           });
      })
   .limit(5)
   .toArray(100);

gs.info(JSON.stringify(records));
```

Output:

```
[
   {
      "first_name":"System",
      "last_name":"Administrator",
      "description":null,
      "closed_at":"2020-08-23 13:14:56"
   },
   {
      "first_name":"System",
      "last_name":"Administrator",
      "description":null,
      "closed_at":"2020-08-23 13:07:43"
   },
   {
      "first_name":"System",
      "last_name":"Administrator",
      "description":null,
      "closed_at":"2020-06-15 06:59:05"
   },
   {
      "first_name":"System",
      "last_name":"Administrator",
      "description":null,
      "closed_at":"2020-08-23 13:07:33"
   },
   {
      "first_name":"System",
      "last_name":"Administrator",
      "description":null,
      "closed_at":"2020-08-23 13:07:14"
   }
]
```

## Stream - forEach\(Function fn\)

Applies the specified function to each record or item in the stream.

|Name|Type|Description|
|----|----|-----------|
|fn|Function|Function to apply to each item in the stream.|

|Type|Description|
|----|-----------|
|None| |

This example shows you how to print the result of each item in the stream.

```
var firstNames = new global.GlideQuery('sys_user')
   .select('first_name')
   .forEach(function (u) { 
      gs.debug(u.first_name); 
   });
```

Output:

```
*** Script: [DEBUG] survey
*** Script: [DEBUG] Lucius
*** Script: [DEBUG] Jimmie
*** Script: [DEBUG] Melinda
*** Script: [DEBUG] Jewel
*** Script: [DEBUG] Sean
*** Script: [DEBUG] Jacinto
*** Script: [DEBUG] Krystle
*** Script: [DEBUG] Billie
*** Script: [DEBUG] Christian
*** Script: [DEBUG] Naomi
...
```

## Stream - fromArray\(Object arr\)

Returns a Stream object that contains the values from the provided array.

**Note:** This method is static. You do not need an instance of the class to use this method.

|Name|Type|Description|
|----|----|-----------|
|arr|Array|Array of values to create the stream from.|

|Type|Description|
|----|-----------|
|Stream|Object used to interact with a stream of items such as records.|

This example shows how to create a Stream object containing an array of values.

```
var nameStream = Stream.fromArray(['Bob', 'Sue', 'Sam'])
   .map(function (name) { 
      return name.toUpperCase(); 
   })
   .toArray(3);

gs.info(JSON.stringify(nameStream));
```

Output:

```
["BOB","SUE","SAM"]
```

## Stream - limit\(Number count\)

Limits the number of results returned by the stream.

For better performance, use the limit\(\) method in the GlideQuery class where possible. See [GlideQuery](../../GlideQuery/concept/GlideQueryGlobalAPI.md#). You may need to use this method to limit results with the Stream.flatMap\(\) method.

|Name|Type|Description|
|----|----|-----------|
|count|Number|Number of records to return.|

|Type|Description|
|----|-----------|
|Stream|Object used to interact with a stream of items such as records.|

This example shows you how to limit the results returned from the Stream.flatMap\(\) method.

```
var records = new global.GlideQuery('sys_user')
   .where('last_login', '>', '2015-12-31')
   .select('first_name', 'last_name')
   .flatMap(function (u) {
      return new GlideQuery('task')
           .where('closed_by', u.sys_id)
           .select('closed_at', 'description')
           .map(function (t) {
                return {
                    first_name: u.first_name,
                    last_name: u.last_name,
                    description: t.description,
                    closed_at: t.closed_at
                 };
           });
      })
   .limit(5)
   .forEach(function (task){
      gs.info(JSON.stringify(task, null, 2));
   });
```

Output:

```
*** Script: {
  "first_name": "System",
  "last_name": "Administrator",
  "description": null,
  "closed_at": "2021-10-04 13:40:16"
}
*** Script: {
  "first_name": "System",
  "last_name": "Administrator",
  "description": null,
  "closed_at": "2021-10-04 13:40:22"
}
*** Script: {
  "first_name": "System",
  "last_name": "Administrator",
  "description": null,
  "closed_at": "2021-10-04 13:40:27"
}
*** Script: {
  "first_name": "System",
  "last_name": "Administrator",
  "description": null,
  "closed_at": "2021-10-04 13:40:31"
}
*** Script: {
  "first_name": "System",
  "last_name": "Administrator",
  "description": null,
  "closed_at": "2021-10-04 13:40:54"
}
```

## Stream - map\(Function fn\)

Applies a function to each item in a stream and returns the updated Stream object.

|Name|Type|Description|
|----|----|-----------|
|fn|Function|Function to apply to the result of the query that takes the each item in the stream as input.|

|Type|Description|
|----|-----------|
|Stream|Object containing the stream of records updated after applying the function.|

This example shows you how to apply a function to every item in the stream.

```
var users = new global.GlideQuery('sys_user')
   .whereNotNull('first_name')
   .select('first_name')
   .map(function (u) { 
      return u.first_name.toUpperCase(); 
   })
   .toArray(100);

gs.info(JSON.stringify(users));
```

Output:

```
[
   "SURVEY",
   "LUCIUS",
   "JIMMIE",
   "MELINDA",
   "JEWEL",
   "SEAN",
   "JACINTO",
   "KRYSTLE",
   "BILLIE",
   "CHRISTIAN",
   ...
]
```

## Stream - reduce\(function reducerFn, Any initialValue\)

Executes a reducer function on each item in the stream, resulting in single output value.

This method is similar to the native JavaScript reduce\(\) method. For more information, see [w3schools documentation](https://www.w3schools.com/jsref/jsref_reduce.asp).

<table id="table_ogx_bff_4mb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

reducerFn

</td><td>

Function

</td><td>

Function to apply to each item in the stream that reduces the stream to a single value. This function must take two arguments: -   `acc`: Accumulator that accumulates all values returned by the function.
-   `cur`: Current item being accumulated in the array.

</td></tr><tr><td>

initialValue

</td><td>

Any

</td><td>

Value passed to the function as the initial value.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|Any|Accumulated total of all items returned by the reducer function.|

This example shows you how to return the record with the longest name from the User table.

```
var longestName = new global.GlideQuery('sys_user')
   .whereNotNull('first_name')
   .select('first_name')
   .reduce(function (acc, cur) {
       return cur.first_name.length > acc.length
           ? cur.first_name
           : acc;
       }, '');

gs.info(JSON.stringify(longestName));
```

Output:

```
"ATF_TestItilUser1"
```

## Stream - some\(Function predicate\)

Applies a predicate function, a function that takes a single value and returns true or false, to each item in the stream. If the predicate returns true for any item in the stream, the method returns true.

|Name|Type|Description|
|----|----|-----------|
|predicate|Function|Predicate function to apply to the items inside the Stream object. Must return a Boolean value.|

<table id="table_r4v_v2f_4mb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the predicate function returned true for an item in the stream.

 Valid values:

-   true: The predicate function returned true for an item in the stream.
-   false: The predicate function did not return true for an item in the stream.

</td></tr></tbody>
</table>This example shows how to check whether any descriptions in the Task table are over 1,000 characters long.

```
var hasLongDescriptions = new global.GlideQuery('task')
   .whereNotNull('description')
   .select('description')
   .some(function (t) { 
      return t.description.length > 1000; 
   });


gs.info(hasLongDescriptions);
```

Output:

```
false
```

## Stream - toArray\(Number count\)

Returns an array containing the given number of items from the stream.

|Name|Type|Description|
|----|----|-----------|
|count|Number|The maximum number of items from the stream to return in the array.|

|Type|Description|
|----|-----------|
|Array|Array containing the given number of items from the stream.|

This example shows you how to transform a stream of records into a JavaScript array.

```
var users = new global.GlideQuery('sys_user')
    .limit(10)
    .select('first_name', 'last_name')
    .toArray(50);

gs.info(JSON.stringify(users));
```

Output:

```
[
   {
      "first_name":"Jewel",
      "last_name":"Agresta",
      "sys_id":"02826bf03710200044e0bfc8bcbe5d64"
   },
   {
      "first_name":"Sean",
      "last_name":"Bonnet",
      "sys_id":"02826bf03710200044e0bfc8bcbe5d6d"
   },
   {
      "first_name":"Jacinto",
      "last_name":"Gawron",
      "sys_id":"02826bf03710200044e0bfc8bcbe5d76"
   },
   {
      "first_name":"Krystle",
      "last_name":"Stika",
      "sys_id":"02826bf03710200044e0bfc8bcbe5d7f"
   },
   {
      "first_name":"Billie",
      "last_name":"Cowley",
      "sys_id":"02826bf03710200044e0bfc8bcbe5d88"
   },
   {
      "first_name":"Christian",
      "last_name":"Marnell",
      "sys_id":"02826bf03710200044e0bfc8bcbe5d91"
   }
]
```

