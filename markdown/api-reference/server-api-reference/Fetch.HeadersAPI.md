---
title: Fetch Headers - Scoped, Global
description: The Fetch Headers API allows you to retrieve, set, add to, and remove headers from a list of request or response headers.The Headers\(\) constructor creates a new, empty Headers object. You can also create and pre-populate a new Headers object with list of HTTP headers using the init parameter.Adds a new value to an existing header inside a Headers object, or adds the header if it does not already exist.Deletes a header from the current Headers object.Returns an iterator allowing you to cycle through all key-value pairs \(represented with strings\) contained in the Headers object.Executes a callback function once per each key/value pair in the Headers object.Returns a string of all header values of a specified Headers object, or returns null if the header does not exist.Returns all Set-Cookie headers associated with a response.Returns a Boolean indicating whether a Headers object contains the given header.Returns an iterator allowing you to cycle through all keys contained in a Headers object.Updates a value of an existing header inside the Headers object, or creates a new header with the given value if the header does not already exist.Returns an iterator allowing you to cycle through all header values contained in the Headers object.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 9
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# Fetch Headers- Scoped, Global

The Fetch Headers API allows you to retrieve, set, add to, and remove headers from a list of request or response headers.

This API is part of a set of Fetch APIs, which provide various actions for fetching resources from external websites. The full Fetch API collection includes:

-   [Fetch - fetch\(String resource, Object options\)](FetchAPI.md#): Starts the process of fetching a resource from the network.
-   [Fetch Headers - Scoped, Global](Fetch.HeadersAPI.md#): Retrieve and modify request and response headers.
-   [Fetch Request - Scoped, Global](Fetch.RequestAPI.md#): Create a new request object.
-   [Fetch RequestInit - Scoped, Global](Fetch.RequestInitAPI.md#): Set options to configure a fetch request.
-   [Fetch Response - Scoped,Global](Fetch.ResponseAPI.md#): Create a new response object.

To support fetch actions, the system property, `glide.hosts.allowlist`, allows controls over what hosts a fetch method can access. It applies to HTTP APIs like RestMessageV2 and those mentioned above. For more information about `glide.hosts.allowlist`, see Available system properties.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## Fetch Headers - Headers\(init\)

The Headers\(\) constructor creates a new, empty Headers object. You can also create and pre-populate a new Headers object with list of HTTP headers using the **init** parameter.

**Note:** To add headers to an existing Headers object, use [Fetch Headers - append\(String name, String value\)](Fetch.HeadersAPI.md#).

<table id="table_nzn_3rv_gdc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

init

</td><td>

Object

</td><td>

Optional. An object literal containing HTTP headers to pre-populate the new Headers object with. Valid values:

-   An object literal with string values,
-   An array of name-value pairs,
-   An existing Headers object \(where the new object copies data from the existing object\).

Default: Creates an empty Headers object

</td></tr></tbody>
</table>The following example shows how to use the Headers\(\) constructor to create a new Headers object with and without headers.

```
//Intializes an empty Headers object.
var headers = new Headers();

//Sets the new Headers object with a list of headers.
var httpHeaders = {
  "Content-Type": "application/json", 
  "X-My-Custom-Header": "XYZ", 
}; 

var myHeaders = new Headers(httpHeaders);
```

## Fetch Headers - append\(String name, String value\)

Adds a new value to an existing header inside a Headers object, or adds the header if it does not already exist.

If the specified header already exists, `append()` changes its existing value to the specified value. If the specified header already exists and accepts multiple values, `append()` appends the new value to the end of the value set. To overwrite the old value with a new one, use [Fetch Headers - set\(String name, String value\)](Fetch.HeadersAPI.md#).

|Name|Type|Description|
|----|----|-----------|
|name|String|Required. The name of the HTTP header to add to the Headers object.|
|value|String|Required. The value of the HTTP header to add.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to add a header using append\(\):

```
var myHeaders = new Headers(); // Currently empty
myHeaders.append("Content-Type", "image/jpeg");
myHeaders.get("Content-Type"); // Returns 'image/jpeg'
```

Output:

```
“image/jpeg”
```

The following example shows how to append a new header that accepts multiple values:

```
var myHeaders = new Headers(); // Currently empty
myHeaders.append("Accept-Encoding", "deflate");
myHeaders.append("Accept-Encoding", "gzip");
myHeaders.get("Accept-Encoding"); // Returns 'deflate, gzip'
```

Output:

```
{“deflate”, “gzip”} 
```

## Fetch Headers - delete\(String name\)

Deletes a header from the current Headers object.

|Name|Type|Description|
|----|----|-----------|
|name|String|The name of the HTTP header to delete from the Headers object.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to first add a header to the Headers object using append\(\), and then delete the same header using delete\(\).

```
var myHeaders =newHeaders();// Currently empty
myHeaders.append("Content-Type","image/jpeg");
myHeaders.get("Content-Type");// Returns 'image/jpeg'
```

The following example shows that the endpoint returns a value of null if the Headers object is already deleted:

```
myHeaders.delete("Content-Type");
myHeaders.get("Content-Type");// Returns null, as it has been deleted
```

Output:

```
null
```

## Fetch Headers - entries\(\)

Returns an iterator allowing you to cycle through all key-value pairs \(represented with strings\) contained in the Headers object.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Iterator|Returns an iterator object, where both the key and value pairs are String objects.|

The following example shows how to create a test Headers object and then use the entries\(\) method to return an iterator of all values in the Headers object.

```
// Create a test Headers object
var myHeaders = new Headers();
myHeaders.append("Content-Type", "text/xml");
myHeaders.append("Vary", "Accept-Language");

// Display the key/value pairs
for (var pair of myHeaders.entries()) {
  console.log(`${pair[0]}: ${pair[1]}`);
}
```

Output:

```
content-type: text/xml
vary: Accept-Language
```

## Fetch Headers - forEach\(Function callbackFn, Object thisArg\)

Executes a callback function once per each key/value pair in the Headers object.

The callback function does not execute for deleted keys but does for existing keys even if the value is undefined.

<table id="table_pjv_xcq_jdc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

callbackFn

</td><td>

Function

</td><td>

Function to execute for each key/value pair in the Headers object. Conforms to the format: `callbackFn(string key, string value)`.

</td></tr><tr><td>

callbackFn.value

</td><td>

String

</td><td>

Value of the header entry.

</td></tr><tr><td>

callbackFn.key

</td><td>

String

</td><td>

Name of the header entry.

</td></tr><tr><td>

callBackFn.object

</td><td>

Header

</td><td>

The Headers object to iterate.

</td></tr><tr><td>

thisArg

</td><td>

Object

</td><td>

Value to use as `this` when executing `callback`.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

The following example logs a line for each key/value pair in the Headers object:

```
// Create a new test Headers object
var myHeaders = new Headers();
myHeaders.append("Content-Type", "application/json");
myHeaders.append("Cookie", "This is a demo cookie");
myHeaders.append("compression", "gzip");

// Display the key/value pairs
myHeaders.forEach((value, key) => {
  console.log(`${key} ==> ${value}`);
});
```

Output:

```
compression ==> gzip
content-type ==> application/json
cookie ==> This is a demo cookie
```

## Fetch Headers - get\(String name\)

Returns a string of all header values of a specified Headers object, or returns null if the header does not exist.

|Name|Type|Description|
|----|----|-----------|
|name|String|The name of the HTTP header whose headers values you want to retrieve \(case-insensitive\).|

<table id="table_mg2_kfq_jdc" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

The value of the retrieved header \(represented as a string\), or null if the header is not set.Returns an error if the header does not exist. Returns a type error if the given name is not that of an HTTP header.

</td></tr></tbody>
</table>The following shows how to create a headers object with multiple headers using append\(\), and then return the header's values using the get\(\) method.

```
var myHeaders = new Headers(); // Currently empty
myHeaders.append("Accept-Encoding", "deflate");
myHeaders.append("Accept-Encoding", "gzip");
myHeaders.get("Accept-Encoding"); // Returns "deflate, gzip"
myHeaders
  .get("Accept-Encoding")
  .split(",")
  .map((v) => v.trimStart()); // Returns [ "deflate", "gzip"

```

Output:

```
[ "deflate", "gzip" ]
```

## Fetch Headers - getSetCookie\(\)

Returns all Set-Cookie headers associated with a response.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Array of strings|An array of strings containing the values of all Set-Cookie headers associated with a response. The method returns an empty array if no Set-Cookie headers are set.|

The following script example shows how to use getSetCookie\(\) to return the header values associated with the response:

```
var headers = new Headers({
  "Set-Cookie": "name1=value1",
});

headers.append("Set-Cookie", "name2=value2");

headers.getSetCookie();
```

Output:

```
["name1=value1", "name2=value2"]
```

## Fetch Headers - has\(String name\)

Returns a Boolean indicating whether a Headers object contains the given header.

|Name|Type|Description|
|----|----|-----------|
|name|String|The name of the HTTP header to check whether it exists on the Headers object or not.|

<table id="table_cvr_r3q_jdc" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the specified header exists in the Headers object. A TypeError is returned if the given header is not a valid HTTP header name.Possible values:

-   true: The header exists on the object.
-   false: The header doesn't exist on the object.

</td></tr></tbody>
</table>The following example uses the Headers\(\) and append\(\) methods to create and set a Headers object with the Content-Type header. The example then uses the has\(\) method to show that the Content-Type header exists on the Headers object but a Accept-Coding header does not.

```
var myHeaders = new Headers(); // Currently empty
myHeaders.append("Content-Type", "image/jpeg");
myHeaders.has("Content-Type"); // Returns true
myHeaders.has("Accept-Encoding"); // Returns false
```

Output:

```
true
false
```

## Fetch Headers - keys\(\)

Returns an iterator allowing you to cycle through all keys contained in a Headers object.

Use the [Fetch Headers - values\(\)](Fetch.HeadersAPI.md#) method to return all header keys.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Iterator|Returns an iterator, where header keys are represented as Strings.|

The following example shows how to create a Headers object with keys, and then use the keys\(\) method to return a list of available headers.

```
// Create a test Headers object
var myHeaders = new Headers();
myHeaders.append("Content-Type", "text/xml");
myHeaders.append("Vary", "Accept-Language");

// Display the keys
for (var key of myHeaders.keys()) {
  console.log(key);
}
```

Output:

```
content-type
vary
```

## Fetch Headers - set\(String name, String value\)

Updates a value of an existing header inside the Headers object, or creates a new header with the given value if the header does not already exist.

To simply append a new value to an existing header without overwriting any data, use the [Fetch Headers - append\(String name, String value\)](Fetch.HeadersAPI.md#) method.

|Name|Type|Description|
|----|----|-----------|
|name|String|The name of the HTTP header in which to set a new value. Throws TypeError if the given name is not the name of an HTTP header.|
|value|String|The new value to set for the given header.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to set a header in new Headers object using append\(\), and then reset the value using set\(\).

```
var myHeaders = new Headers(); // Currently empty
myHeaders.append("Content-Type", "image/jpeg");
myHeaders.set("Content-Type", "text/html");
```

Output:

```
text/html
```

The following example shows how to set a value in a Headers object when it accepts multiple values:

```
myHeaders.set("Accept-Encoding", "deflate");
myHeaders.set("Accept-Encoding", "gzip");
myHeaders.get("Accept-Encoding");
```

Output:

```
gzip
```

## Fetch Headers - values\(\)

Returns an iterator allowing you to cycle through all header values contained in the Headers object.

Use the [Fetch Headers - keys\(\)](Fetch.HeadersAPI.md#) method to return all header values.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Returns an iterator, where the header values are represented as strings.|

The following example shows how to fist create and set a new Headers object with multiple headers using the append\(\) method, and then return a list of all header values in the new object by calling the values\(\) method. Console.log\(\) logs the line to system logs.

```
// Create a test Headers object
var myHeaders = new Headers();
myHeaders.append("Content-Type", "text/xml");
myHeaders.append("Vary", "Accept-Language");

// Display the values
for (var value of myHeaders.values()) {
  console.log(value);
}
```

Output:

```
text/xml
Accept-Language
```

