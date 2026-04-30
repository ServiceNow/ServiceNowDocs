---
title: ArrayUtil - Global
description: The ArrayUtil script include provides methods for working with JavaScript arrays.Merge two arrays.Searches the array for the specified element. Returns true if the element exists in the array, otherwise returns false.Converts a Java object to an array.Finds the differences between two or more arrays.Returns an array from the specified object.Searches the array for the element. Returns the element index or -1 if not found.Searches the array for the element starting at the specified index. Returns the element index or -1 if not found.Finds the elements present in all arrays.Merge two or more arrays.Removes duplicate items from an array.
locale: en-US
release: yokohama
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 6
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# ArrayUtil- Global

The ArrayUtil script include provides methods for working with JavaScript arrays.

These methods are available to any server-side script.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## ArrayUtil - concat\(Array parent, Array child\)

Merge two arrays.

|Name|Type|Description|
|----|----|-----------|
|parent|Array|An array to merge|
|child|Array|An array to merge|

|Type|Description|
|----|-----------|
|Array|An array of elements from both input arrays. Duplicates are not removed.|

```
var arrayUtil = new ArrayUtil();
var a1 = new Array("a", "b", "c");
var a2 = new Array("c", "d", "e");
 
gs.print("concat a1, a2: " + arrayUtil.concat(a1, a2));
```

Output: concat a1, a2: a,b,c,c,d,e

## ArrayUtil - contains\(Array array, Object element\)

Searches the array for the specified element. Returns true if the element exists in the array, otherwise returns false.

|Name|Type|Description|
|----|----|-----------|
|array|Array|Array to search.|
|element|Object|Element to search for.|

<table id="table_acc_w5z_nt" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag indicating whether the element was found in the array.Possible values:

-   true: Element found in array.
-   false: Element not found in array.

</td></tr></tbody>
</table>```
var arrayUtil = new ArrayUtil();
var a1 = new Array("a", "b", "c");
 
gs.print("Contains b: " + arrayUtil.contains(a1, "b"));
gs.print("Contains x: " + arrayUtil.contains(a1, "x"));
```

Output:

```
Contains b: true
Contains x: false
```

## ArrayUtil - convertArray\(Object a\)

Converts a Java object to an array.

|Name|Type|Description|
|----|----|-----------|
|a|Object|Object to convert.|

|Type|Description|
|----|-----------|
|Array|Array created from the object.|

This example converts a Java object to an array.

```
var arrayUtil = new ArrayUtil();
// Returns a JavaObject with the logged in user's groups
var groupObj = gs.getUser().getMyGroups();
gs.print('groupObj: ' + Object.prototype.toString.call(groupObj));

var groupArr = arrayUtil.convertArray(groupObj);
gs.print('groupArr: ' + Object.prototype.toString.call(groupArr));
```

Output:

```
groupObj: [object JavaObject]
groupArr: [object Array]
```

## ArrayUtil - diff\(Array a, Array b\)

Finds the differences between two or more arrays.

Any number of arrays can be provided as parameters.

|Name|Type|Description|
|----|----|-----------|
|a|Array|An array|
|b|Array|An array|

|Type|Description|
|----|-----------|
|Array|Returns an array of items from array a that were not found in either array b or c, or other input arrays. Duplicates are removed from the result.|

```
var arrayUtil = new ArrayUtil();
var a1 = new Array("a", "b", "c");
var a2 = new Array("c", "d", "e");
gs.print(arrayUtil.diff(a1, a2));
```

Output: a,b

## ArrayUtil - ensureArray\(Object object\)

Returns an array from the specified object.

|Name|Type|Description|
|----|----|-----------|
|object|Object|Object from which to create an array.|

|Type|Description|
|----|-----------|
|Array|Array created from the object.|

The following example shows how to create an array from an object and display created array.

```
var arrayUtil = new ArrayUtil();
var o1 = {a:"1",b:"2",c:"3"};
gs.print('o1 is array: ' + Array.isArray(o1));
gs.print('o1 stringified: ' + JSON.stringify(o1));

var a1 = arrayUtil.ensureArray(o1);
gs.print('a1 is array: ' + Array.isArray(a1));
gs.print('a1 stringified: ' + JSON.stringify(a1));
```

Output:

```
o1 is array: false
o1 stringified: {"a":"1","b":"2","c":"3"}
a1 is array: true
a1 stringified: [{"a":"1","b":"2","c":"3"}]
```

The following example shows how to create an array from an object and display the contents of the array.

```
var stock = { 'name': 'Servicenow', 'sym': 'NOW' };

var arr = new ArrayUtil();
var stArray = arr.ensureArray(stock);

gs.info("Name is " + stArray[0]['name']);
gs.info("Symbol is " + stArray[0]['sym']);
```

Output:

```
Name is Servicenow
Symbol is NOW
```

## ArrayUtil - indexOf\(Array array, Object element\)

Searches the array for the element. Returns the element index or -1 if not found.

|Name|Type|Description|
|----|----|-----------|
|array|Array|Array to search.|
|element|Object|Element to search for.|

|Type|Description|
|----|-----------|
|Number|Position of the element in the array, or -1 if the element is not found.|

```
var arrayUtil = new ArrayUtil();
var arr = new Array("a", "b", "c", "x", "y", "z");
gs.print("Array: " + arr);

gs.print("Index of a: " + arrayUtil.indexOf(arr, "a"));
gs.print("Index of a starting at 2: " + arrayUtil.indexOf(arr, "a", 2));

gs.print("Index of c: " + arrayUtil.indexOf(arr, "c"));
gs.print("Index of c starting at 1: " + arrayUtil.indexOf(arr, "c", 1));

gs.print("Index of z: " + arrayUtil.indexOf(arr, "z"));
gs.print("Index of z starting at 4: " + arrayUtil.indexOf(arr, "z", 4));

// If negative value is sent as startIndex then (startIndex + length of array ) is considered as start index.

// startIndex = -1+(6); startIndex is considered as 5 in this case
gs.print("Index of c starting at -1 (Re-Calculated to 5): " + arrayUtil.indexOf(arr, "c", -1)); 

// startIndex = -10+(6) which is -4,if negative value again then startIndex is considered as 0
gs.print("Index of c starting at -10 (Re-Calculated to 0): " + arrayUtil.indexOf(arr, "c", -10)); 
```

Output:

```
Array: a,b,c,x,y,z
Index of a: 0
Index of a starting at 2: -1
Index of c: 2
Index of c starting at 1: 2
Index of z: 5
Index of z starting at 4: 5
Index of c starting at -1 (Re-Calculated to 5): -1
Index of c starting at -10 (Re-Calculated to 0): 2
```

## ArrayUtil - indexOf\(Array array, Object element, Number startIndex\)

Searches the array for the element starting at the specified index. Returns the element index or -1 if not found.

|Name|Type|Description|
|----|----|-----------|
|array|Array|Array to search.|
|element|Object|Element to search for.|
|startIndex|Number|Index to start searching from.|

|Type|Description|
|----|-----------|
|Number|Position of the element in the array, or -1 if the element is not found.|

```
var arrayUtil = new ArrayUtil();
var arr = new Array("a", "b", "c", "x", "y", "z");
gs.print("Array: " + arr);

gs.print("Index of a: " + arrayUtil.indexOf(arr, "a"));
gs.print("Index of a starting at 2: " + arrayUtil.indexOf(arr, "a", 2));

gs.print("Index of c: " + arrayUtil.indexOf(arr, "c"));
gs.print("Index of c starting at 1: " + arrayUtil.indexOf(arr, "c", 1));

gs.print("Index of z: " + arrayUtil.indexOf(arr, "z"));
gs.print("Index of z starting at 4: " + arrayUtil.indexOf(arr, "z", 4));

// If negative value is sent as startIndex then (startIndex + length of array ) is considered as start index.

// startIndex = -1+(6); startIndex is considered as 5 in this case
gs.print("Index of c starting at -1 (Re-Calculated to 5): " + arrayUtil.indexOf(arr, "c", -1)); 

// startIndex = -10+(6) which is -4,if negative value again then startIndex is considered as 0
gs.print("Index of c starting at -10 (Re-Calculated to 0): " + arrayUtil.indexOf(arr, "c", -10)); 
```

Output:

```
Array: a,b,c,x,y,z
Index of a: 0
Index of a starting at 2: -1
Index of c: 2
Index of c starting at 1: 2
Index of z: 5
Index of z starting at 4: 5
Index of c starting at -1 (Re-Calculated to 5): -1
Index of c starting at -10 (Re-Calculated to 0): 2
```

## ArrayUtil - intersect\(Array a, Array b\)

Finds the elements present in all arrays.

Any number of arrays can be provided as parameters.

|Name|Type|Description|
|----|----|-----------|
|a|Array|An array|
|b|Array|An array|

|Type|Description|
|----|-----------|
|Array|An array of elements from array a that were found in all of the other input arrays. Duplicates are removed.|

```
var arrayUtil = new ArrayUtil();
var a1 = new Array("a", "b", "c");
var a2 = new Array("c", "d", "e");
gs.print(arrayUtil.intersect(a1, a2));
```

Output: c

## ArrayUtil - union\(Array a, Array b\)

Merge two or more arrays.

Any number of arrays can be provided as parameters.

|Name|Type|Description|
|----|----|-----------|
|a|Array|An array|
|b|Array|An array|

|Type|Description|
|----|-----------|
|Array|An array of items from all the input arrays. Duplicates are removed.|

```
var arrayUtil = new ArrayUtil();
var a1 = new Array("a", "b", "c");
var a2 = new Array("c", "d", "e");
gs.print(arrayUtil.union(a1, a2));
```

Output: a,b,c,d,e

## ArrayUtil - unique\(Array a\)

Removes duplicate items from an array.

|Name|Type|Description|
|----|----|-----------|
|a|Array|The array to check for duplicate elements.|

|Type|Description|
|----|-----------|
|Array|An array of unique items from the input array.|

```
var arrayUtil = new ArrayUtil();
var a1 = new Array("a", "b", "c", "c", "b");
gs.print(arrayUtil.unique(a1));
```

Output: a,c,b

