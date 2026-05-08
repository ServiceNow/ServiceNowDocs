---
title: Fetch Request - Scoped, Global
description: The Fetch Request API contains methods for creating or retrieving a Request object to allow applications to asynchronously request resources, such as JSON, text, or binary data, from a server, and handle the response. This API supports various HTTP methods like GET, POST, PUT, DELETE, and so on.Creates a new Request object. Optionally create the Request object from a URL or object resource.Reads the request body and returns it as a promise that resolves with an arrayBuffer.Reads the request body and returns it as a promise that resolves with a Blob.Reads the request body and returns it as a promise that resolves with an Uint8Array.Creates a copy of the current Request object.Reads the request body and returns it as a promise that resolves with a FormData object.Reads the request body, parses the content as JSON, and returns a promise that resolves with the parsed result.Reads the request body and returns it as a promise that resolves with a String decoded using UTF-8.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 16
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# Fetch Request- Scoped, Global

The Fetch Request API contains methods for creating or retrieving a Request object to allow applications to asynchronously request resources, such as JSON, text, or binary data, from a server, and handle the response. This API supports various HTTP methods like GET, POST, PUT, DELETE, and so on.

This API is part of a set of Fetch APIs, which provide various actions for fetching resources from external websites. The full Fetch API collection includes:

-   [Fetch - fetch\(String resource, Object options\)](FetchAPI.md#): Start the process of fetching a resource from the network.
-   [Fetch Headers - Scoped, Global](Fetch.HeadersAPI.md#): Retrieve and modify request and response headers.
-   [Fetch Request - Scoped, Global](Fetch.RequestAPI.md#): Create a new request object.
-   [Fetch RequestInit - Scoped, Global](Fetch.RequestInitAPI.md#): Set options to configure a fetch request.
-   [Fetch Response - Scoped,Global](Fetch.ResponseAPI.md#): Create a new response object.

To support fetch actions, the system property, `glide.hosts.allowlist`, allows controls over what hosts a fetch method can access. It applies to HTTP APIs like RestMessageV2 and those mentioned above. For more information about `glide.hosts.allowlist`, see Available system properties.

## Request properties

The Fetch Request API supports several read-only properties that offer detailed information about an HTTP request. Some of these include `url` \(the URL of the request\), `method` \(the HTTP method\), `headers` \(the associated headers\), and `body` \(the request body as a stream\). Other properties include settings for caching, credentials, and referrers. These properties are read-only, meaning they can be accessed but not modified after the request is created. To read more about each property, see [https://developer.mozilla.org/en-US/docs/Web/API/Request](https://developer.mozilla.org/en-US/docs/Web/API/Request).

<table id="table_t5x_2qw_jdc"><thead><tr><th>

Property name

</th><th>

Description

</th><th>

Example

</th></tr></thead><tbody><tr><td>

body

</td><td>

Ready-only property. Contains a readable stream of byte data with the body contents that have been added to the request.Data type/value: A ReadableStream or null.

</td><td>

```
const request = new Request("/myEndpoint", {
  method: "POST",
  body: "Hello world",
});

request.body; // ReadableStream
```

</td></tr><tr><td>

bodyUsed

</td><td>

Ready-only property. Flag that indicates whether the request body has been read yet.Accepted value:

-   true: The request body has been read.
-   false: The request body hasn't been read.

Data type: Boolean

</td><td>

```
const request = new Request("/myEndpoint", {
  method: "POST",
  body: "Hello world",
});

request.bodyUsed; // false

request.text().then((bodyAsText) => {
  console.log(request.bodyUsed); // true
});
```

</td></tr><tr><td>

cache

</td><td>

Ready-only property. Contains the cache mode of the request which controls how the request interacts with the browser's HTTP cache. Accepted values:

-   default: The browser looks for a matching request in its HTTP cache.
    -   If there is a match and it is fresh, it is returned from the cache.
    -   If there is a match but it is stale, the browser makes a conditional request to the remote server. If the server indicates that the resource has not changed, it is returned from the cache. Otherwise the resource is downloaded from the server and the cache will be updated.
    -   If there is no match, the browser makes a normal request, and updates the cache with the downloaded resource.
-   force-cache: The browser looks for a matching request in its HTTP cache.
    -   If there is a match, fresh or stale, it is returned from the cache.
    -   If there is no match, the browser makes a normal request and updates the cache with the downloaded resource.
-   no-cache: The browser looks for a matching request in its HTTP cache.
    -   If there is a match, fresh or stale, the browser makes a conditional request to the remote server. If the server indicates that the resource has not changed, it is returned from the cache. Otherwise the resource is downloaded from the server and the cache is updated.
    -   If there is no match, the browser makes a normal request, and updates the cache with the downloaded resource.
-   no-store: The browser fetches the resource from the remote server without first looking in the cache, and does not update the cache with the downloaded resource.
-   only-if-cached: The browser looks for a matching request in its HTTP cache.

    -   If there is a match, fresh or stale, it is returned from the cache.
    -   If there is no match, the browser responds with 504 Gateway timeout status.
The `only-if-cached` mode can only be used if the request's mode is `same-origin`. Cached redirects are followed if the request's `redirect` property is `follow` and the redirects do not violate the `same-origin` mode.

-   reload: The browser fetches the resource from the remote server without first looking in the cache, but then updates the cache with the downloaded resource.

Data type: String

</td><td>

```
// Download a resource with cache busting, to bypass the cache
// completely.
fetch("some.json", { cache: "no-store" }).then((response) => {
  /* consume the response */
});

// Download a resource with cache busting, but update the HTTP
// cache with the downloaded resource.
fetch("some.json", { cache: "reload" }).then((response) => {
  /* consume the response */
});

// Download a resource with cache busting when dealing with a
// properly configured server that will send the correct ETag
// and Date headers and properly handle If-Modified-Since and
// If-None-Match request headers, therefore we can rely on the
// validation to guarantee a fresh response.
fetch("some.json", { cache: "no-cache" }).then((response) => {
  /* consume the response */
});

// Download a resource with economics in mind! Prefer a cached
// albeit stale response to conserve as much bandwidth as possible.
fetch("some.json", { cache: "force-cache" }).then((response) => {
  /* consume the response */
});

// Naive stale-while-revalidate client-level implementation.
// Prefer a cached albeit stale response; but update if it's too old.
// AbortController and signal to allow better memory cleaning.
// In reality; this would be a function that takes a path and a
// reference to the controller since it would need to change the value
let controller = new AbortController();
fetch("some.json", {
  cache: "only-if-cached",
  mode: "same-origin",
  signal: controller.signal,
})
  .catch((e) =>
    e instanceof TypeError && e.message === "Failed to fetch"
      ? { status: 504 } // Workaround for chrome; which fails with a TypeError
      : Promise.reject(e),
  )
  .then((res) => {
    if (res.status === 504) {
      controller.abort();
      controller = new AbortController();
      return fetch("some.json", {
        cache: "force-cache",
        mode: "same-origin",
        signal: controller.signal,
      });
    }
    const date = res.headers.get("date"),
      dt = date ? new Date(date).getTime() : 0;
    if (dt < Date.now() - 86_400_000) {
      // if older than 24 hours
      controller.abort();
      controller = new AbortController();
      return fetch("some.json", {
        cache: "reload",
        mode: "same-origin",
        signal: controller.signal,
      });
    }

    // Other possible conditions
    if (dt < Date.now() - 300_000)
      // If it's older than 5 minutes
      fetch("some.json", { cache: "no-cache", mode: "same-origin" }); // no cancellation or return value.
    return res;
  })
  .then((response) => {
    /* consume the (possibly stale) response */
  })
  .catch((error) => {
    /* Can be an AbortError/DOMException or a TypeError */
  });
```

</td></tr><tr><td>

credentials

</td><td>

Read-only. Reflects the value given to the Request\(\) constructor in the credentials option. Credentials are cookies, TLS client certificates, or authentication headers containing a username and password.Accepted values:

-   include: Always include credentials, even for cross-origin requests.
-   omit: Never send credentials in the request or include credentials in the response.
-   same-origin: Only send and include credentials for same-origin requests.

Data type: String

</td><td>

```
const request = new Request("flowers.jpg");
const request = request.request; // returns "same-origin" by default
```

</td></tr><tr><td>

destination

</td><td>

Read-only. Returns a string describing the type of content being requested.Accepted values:

-   audio: The target is audio data.
-   audioworklet: The target is data being fetched for use by an audio worklet.
-   document: The target is an HTML or XML document.
-   embed: The taget is embedded content.
-   fencedframe: The target is a fenced frame.
-   font: The target is a font.
-   frame: The target is a frame.
-   iframe: The target is an iframe.
-   image: The target is an image.
-   json: The target is a JSON file
-   manifest: The target is a manifest.
-   object: The target is a object.
-   paintworklet: The target is a paint worklet.
-   report: The target is a report.
-   script: The target is a script.
-   sharedworker: The target is a shared worker.
-   style: The target is a style.
-   track: The target is an HTML &lt;track&gt;.
-   video: The target is video data.
-   worker: The target is a worker.
-   xslt: The target is an XSLT transform.

Data type: String

</td><td>

```
fetch('https://example.com/image.jpg', {
  destination: 'image'
})
  .then(response => response.blob())
  .then(blob => {
    console.log('Image fetched successfully', blob);
  })
  .catch(error => console.error('Error:', error));
```

</td></tr><tr><td>

headers

</td><td>

Read-only. The Headers object associated with the request.Data type: Headers object

</td><td>

```
const myRequest = new Request("flowers.jpg");
const myHeaders = myRequest.headers; // Headers {}
```

</td></tr><tr><td>

integrity

</td><td>

Read-only. The subresource integrity value of the request.Value: The value that was passed as the **options.integrity** argument when constructing the request. If an integrity has not been specified, the property returns `''`.

</td><td>

```
const myRequest = new Request("flowers.jpg", {
  integrity: "sha256-abc123",
});
console.log(myRequest.integrity); // "sha256-abc123"
```

</td></tr><tr><td>

isHistoryNavigation

</td><td>

Read-only. Boolean indicating whether the request is a history navigation.Accepted values:

-   true: The request is a history navigation.
-   false: The request is not a history navigation.

Data type: Boolean

</td><td>

```
self.addEventListener("request", (event) => {
  // ...

  if (event.request.isHistoryNavigation) {
    event.respondWith(
      caches.match(event.request).then((response) => {
        if (response !== undefined) {
          return response;
        } else {
          return fetch(event.request).then((response) => {
            let responseClone = response.clone();

            caches.open("v1").then((cache) => {
              cache.put(event.request, responseClone);
            });

            return response;
          });
        }
      }),
    );
  }

  // ...
});
```

</td></tr><tr><td>

keepalive

</td><td>

Read-only. The request's keepalive setting \(true or false\). Returns an empty string if an integrity value is not passed in the request.Accepted values:

-   true: The browser keeps the associated request alive if the page that initiated it is unloaded before the request is complete.
-   false: The browser doesn't keep the associated request alive if the page that initiated it is unloaded before the request is complete.

Data type: Boolean

</td><td>

```
const options = {
  keepalive: true,
};

const myRequest = new Request("flowers.jpg", options);
let myKeepAlive = myRequest.keepalive; // true
```

</td></tr><tr><td>

method

</td><td>

Read-only. The request's method \(`GET`, `POST`, etc.\)Data type: String

</td><td>

```
const myRequest = new Request("flowers.jpg");
const myMethod = myRequest.method; // GET
```

</td></tr><tr><td>

mode

</td><td>

Read-only. Mode of the request. Used to determine if cross-origin requests lead to valid responses, and which properties of the response are readable.Accepted values:

-   cors: If the request is cross-origin then it will use the Cross-Origin Resource Sharing \(CORS\) mechanism.
-   navigate: A mode for supporting navigation. The navigate value is intended to be used only by HTML navigation. A navigate request is created only while navigating between documents.
-   no-cors: Disables CORS for cross-origin requests. The response is opaque, meaning that its headers and body are not available to JavaScript.
-   same-origin: Disallows cross-origin requests. If a request is made to another origin with this mode set, the result is an error.

Requests can be initiated in a variety of ways, and the mode for a request depends on the particular means by which it was initiated. For example, when a Request object is created using the Request\(\) constructor, the value of the mode property for that Request is set to cors. However, for requests created other than by the Request\(\) constructor, no-cors is typically used as the mode; for example, for embedded resources where the request is initiated from markup, unless the crossorigin attribute is present, the request is in most cases made using the no-cors mode — that is, for the &lt;link&gt; or &lt;script&gt; elements \(except when used with modules\), or &lt;img&gt;, &lt;audio&gt;,&lt;video&gt;, &lt;object&gt;, &lt;embed&gt;, or &lt;iframe&gt; elements.

Data type: String

</td><td>

```
const myRequest = new Request("flowers.jpg");
const myMode = myRequest.mode; // returns "cors" by default
```

</td></tr><tr><td>

redirect

</td><td>

Read-only. Mode for how redirects are handled.Valid values:

-   error
-   follow
-   manual

Data type: String

Default: follow

</td><td>

```
const myRequest = new Request("flowers.jpg");
const myCred = myRequest.redirect;
```

</td></tr><tr><td>

referrer

</td><td>

Read-only. The referrer of the request \(for example, `client`, `no-referrer`, or a URL\). A value of `no-referrer` returns an empty string.Data type: String

</td><td>

```
const myRequest = new Request("flowers.jpg");
const myReferrer = myRequest.referrer; // returns "about:client" by default
```

</td></tr><tr><td>

referrerPolicy

</td><td>

Read-only. The referrer policy which governs what referrer information is sent in the Referrer header with the request.Data type: String

</td><td>

```
const myRequest = new Request("flowers.jpg");
const myReferrer = myRequest.referrerPolicy; // returns "" by default
```

</td></tr><tr><td>

signal

</td><td>

Read-only. AbortSignal associated with the request.Data type: String

</td><td>

```
// Create a new abort controller
const controller = new AbortController();

// Create a request with this controller's AbortSignal object
const req = new Request("/", { signal: controller.signal });

// Add an event handler logging a message in case of abort
req.signal.addEventListener("abort", () => {
  console.log("abort");
});

// In case of abort, log the AbortSignal reason, if any
fetch(req).catch(() => {
  if (req.signal.aborted) {
    if (req.signal.reason) {
      console.log(`Request aborted with reason: ${req.signal.reason}`);
    } else {
      console.log("Request aborted but no reason was given.");
    }
  } else {
    console.log("Request not aborted, but terminated abnormally.");
  }
});

// Actually abort the request
controller.abort();
```

</td></tr><tr><td>

url

</td><td>

Read-only. URL of the request.Data type: String

</td><td>

```
const myRequest = new Request("flowers.jpg");
const myURL = myRequest.url; // "https://github.com/mdn/dom-examples/tree/main/fetch/fetch-request/flowers.jpg"
```

</td></tr></tbody>
</table>**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## Fetch Request - Request\(\)

Creates a new Request object. Optionally create the Request object from a URL or object resource.

<table id="table_kxr_wvv_gdc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

input

</td><td>

String or Object

</td><td>

Optional. The resource to retrieve.Valid values:

-   A string containing the URL of the resource to fetch. The API doesn't accept URLs containing credentials, such as `http://user.password.example.com`. An exception is thrown if the URL can't be parsed.
-   A Request object, effectively creating a copy of an existing Request object. The object structure is dictated by the Request class.

**Note:** Note the following behavioral updates to retain security while making the constructor less likely to throw exceptions:

    -   If this object exists on another origin to the constructor call, the  Request.referrer  property is stripped out.
    -   If this object has a  Request.mode  property of  `navigate`, the  mode  value is converted to  `same-origin`.

</td></tr><tr><td>

options

</td><td>

Object

</td><td>

Optional. A [Fetch RequestInit - Scoped, Global](Fetch.RequestInitAPI.md#) object containing any custom settings to apply to the request. If you construct a new request from an existing request, options set in the new request override any corresponding options in the original request.Default: Returns default values for all properties.

</td></tr></tbody>
</table>The following example shows how to create a new Request object using the Request\(\) constructor.

```
var myImage = document.querySelector("img");
var myRequest = new Request("flowers.jpg");
```

The following example shows how to create the new Request object using the input parameter to retrieve a URL or object.

```
var myImage = document.querySelector("img");
var myRequest = new Request("flowers.jpg");

fetch(myRequest)
  .then((response) => response.blob())
  .then((response) => {
    var objectURL = URL.createObjectURL(response);
    myImage.src = objectURL;
  });
```

The following example shows how to create the new Request object with header options using an object literal.

```
var myImage = document.querySelector("img");
var myRequest = new Request("flowers.jpg");

var options = {
  headers: {
    "Cache-Control": "max-age=60480",
  },
};
```

## Fetch Request - arrayBuffer\(\)

Reads the request body and returns it as a promise that resolves with an arrayBuffer.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Promise|A promise that resolves with an [arrayBuffer](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/ArrayBuffer).|

The following shows how to create a new request using the arrayBuffer\(\) method.

```
var myArray = new Uint8Array(10);

var request = new Request("/myEndpoint", {
  method: "POST",
  body: myArray,
});

request.arrayBuffer().then((buffer) => {
  // perform an action with the buffer sent in the request
});
```

## Fetch Request - blob\(\)

Reads the request body and returns it as a promise that resolves with a Blob.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Object|A promise that resolves with a [Blob](https://developer.mozilla.org/en-US/docs/Web/API/Blob).|

The following example shows how to form a request with the blob\(\) method.

```
var obj = { hello: "world" };
var myBlob = new Blob([JSON.stringify(obj, null, 2)], {
  type: "application/json",
});

var request = new Request("/myEndpoint", {
  method: "POST",
  body: myBlob,
});

request.blob().then((myBlob) => {
  // do something with the blob sent in the request
});
```

## Fetch Request - bytes\(\)

Reads the request body and returns it as a promise that resolves with an Uint8Array.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Object|A promise that resolves with an [Uint8Array](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Uint8Array).|

The following shows how to create a new request using the bytes\(\) method.

```
var myArray = new Uint8Array(10);

var request = new Request("/myEndpoint", {
  method: "POST",
  body: myArray,
});

request.bytes().then((buffer) => {
  // do something with the buffer sent in the request
});
```

## Fetch Request - clone\(\)

Creates a copy of the current Request object.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Request|A Request object that is an exact copy of the request that `clone()` was called on. `clone()` throws a error if the request body has already been used. If you want to modify the request, you use the [Fetch Request - Request\(\)](Fetch.RequestAPI.md#) constructor.|

The following example demonstrates how to create a new request using request\(\) and then copy it using clone\(\).

```
var myRequest = new Request("flowers.jpg");
var newRequest = myRequest.clone(); // a copy of the request is now stored in newRequest
```

## Fetch Request - formData\(\)

Reads the request body and returns it as a promise that resolves with a FormData object.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|None|A Promise that resolves with a [FormData](https://developer.mozilla.org/en-US/docs/Web/API/FormData) object.|

The following example demonstrates how to create a new request using request\(\) and then resolve it with the formData\(\) method to resolve it as a FormData object.

```
var formData = new FormData();
var fileField = document.querySelector('input[type="file"]');

formData.append("username", "abc123");
formData.append("avatar", fileField.files[0]);

var request = new Request("/myEndpoint", {
  method: "POST",
  body: formData,
});

request.formData().then((data) => {
  // do something with the formdata sent in the request
});
```

## Fetch Request - json\(\)

Reads the request body, parses the content as JSON, and returns a promise that resolves with the parsed result.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Object|A promise \(the eventual completion, or failure, of an asynchronous operation and its resulting value\) that resolves to a JavaScript object. This object could be anything that can be represented by JSON: an object, an array, a string, a number, and so on.|

The following example demonstrates how to create a new request using request\(\) and then json\(\) to parse the request and return it as a JSON object.

```
var obj = { hello: "world" };

var request = new Request("/myEndpoint", {
  method: "POST",
  body: JSON.stringify(obj),
});

request.json().then((data) => {
  // process the data sent in the request
});
```

## Fetch Request - text\(\)

Reads the request body and returns it as a promise that resolves with a String decoded using UTF-8.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|None|A promise that resolves with a String in UTF-8 format.|

This example shows how to call text\(\).

```
var text = "Hello world";

var request = new Request("/myEndpoint", {
  method: "POST",
  body: text,
});

request.text().then((text) => {
  // process the data sent in the request
});
```

