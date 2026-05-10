---
title: Fetch RequestInit - Scoped, Global
description: The RequestInit API provides options to configure a Fetch request.Set options to configure a Fetch request. You can pass a RequestInit object into the Request\(\) constructor or directly into the fetch\(\) function call.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 9
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# Fetch RequestInit- Scoped, Global

The RequestInit API provides options to configure a Fetch request.

You can pass a RequestInit object into the Request\(\) constructor, or directly into the fetch\(\) function call. You can also construct a Request with a RequestInit\(\) call, and pass the Request to a fetch\(\) call along with another RequestInit\(\). If you do this when the same option is set in both places, then the value passed directly into fetch\(\) is used.

This API is part of a set of Fetch APIs, which provide various actions for fetching resources from external websites. The full Fetch API collection includes:

-   [Fetch - fetch\(String resource, Object options\)](FetchAPI.md#): Starts the process of fetching a resource from the network.
-   [Fetch Headers - Scoped, Global](Fetch.HeadersAPI.md#): Retrieve and modify request and response headers.
-   [Fetch Request - Scoped, Global](Fetch.RequestAPI.md#): Create a new request object.
-   [Fetch RequestInit - Scoped, Global](Fetch.RequestInitAPI.md#): Set options to configure a fetch request.
-   [Fetch Response - Scoped,Global](Fetch.ResponseAPI.md#): Create a new response object.

To support fetch actions, the system property, `glide.hosts.allowlist`, allows controls over what hosts a fetch method can access. It applies to HTTP APIs like RestMessageV2 and those mentioned above. For more information about `glide.hosts.allowlist`, see [Available system properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/r_AvailableSystemProperties.md).

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## Fetch RequestInit - RequestInit

Set options to configure a Fetch request. You can pass a RequestInit object into the Request\(\) constructor or directly into the fetch\(\) function call.

### RequestInit properties

The RequestInit API supports several optional properties that can be used to configure HTTP request behavior. Its properties include `method` \(HTTP method\), `headers` \(request headers\), `body` \(data to send\), `mode` \(CORS mode\), `credentials` \(authentication details\), `cache` \(cache behavior\), and others like `redirect`, `referrer`, and `integrity`. These options let you fine-tune request behavior for various use cases. To read more in-depth explanations about each property, see [https://developer.mozilla.org/en-US/docs/Web/API/RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/RequestInit).

<table id="table_t5x_2qw_jdc"><thead><tr><th>

Property name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

attributionReporting

</td><td>

Optional. Indicates that you want the request's response to be able to register a JavaScript-based attribution source or attribution trigger. `attributionReporting` is an object containing the following properties:

-   eventSourceEligible: Boolean. If set to `true`, the request's response is eligible to register an attribution source. If set to `false`, it isn't eligible for registration as an attribution source.
-   triggerEligible: Boolean. If set to `true`, the request's response is eligible to register an attribution trigger. If set to `false`, it isn't eligible for registration as an attribution trigger.

Data type: Object

</td></tr><tr><td>

body

</td><td>

Optional. The request body contains content to send to the server, for example in a POST or PUT request. Accepted types:

-   ArrayBuffer
-   a string
-   Blob
-   DataView
-   File
-   FormData
-   ReadableStream
-   TypedArray
-   URLSearchParams

</td></tr><tr><td>

browsingTopics

</td><td>

Optional. Flag indicating whether the selected topics for the current user should be sent in a Sec-Browsing-Topics header with the associated request.Accepted values:

-   true: Selected topics for the current user should be sent in a Sec-Browsing-Topics header
-   false: Selected topics for the current user shouldn't be sent in a Sec-Browsing-Topics header.

Data type: Boolean

</td></tr><tr><td>

cache

</td><td>

Optional. The cache mode to use for the request. Accepted values:

-   default: The browser looks in its HTTP cache for a response matching the request.
-   force-cache: The browser looks in its HTTP cache for a response matching the request.
-   no-cache: The browser looks in its HTTP cache for a response matching the request.
-   no-store: The browser fetches the resource from the remote server without first looking in the cache, and will not update the cache with the downloaded resource.
-   only-if-cached: The browser looks in its HTTP cache for a response matching the request.
-   reload: The browser fetches the resource from the remote server without first looking in the cache, but then will update the cache with the downloaded resource.

The `only-if-cached` mode can only be used if the request's mode is `same-origin`. Cached redirects will be followed if the request's `redirect` property is `follow` and the redirects do not violate the `same-origin` mode.

Data type: String

</td></tr><tr><td>

credentials

</td><td>

Optional. Controls whether or not the browser sends credentials with the request, as well as whether any Set-Cookie response headers are respected. Credentials are cookies, TLS client certificates, or authentication headers containing a username and password.Accepted values:

-   include: Always include credentials, even for cross-origin requests.

**Note:** Including credentials in cross-origin requests can make a site vulnerable to CSRF attacks, so even if `credentials` is set to `include`, the server must also agree to their inclusion by including the Access-Control-Allow-Credentials in its response. Additionally, in this situation the server must explicitly specify the client's origin in the Access-Control-Allow-Origin response header \(that is, `*`is not allowed\).

-   omit: Never send credentials in the request or include credentials in the response.
-   same-origin: Only send and include credentials for same-origin requests.

Default: same-origin

Data type: String

</td></tr><tr><td>

headers

</td><td>

Optional. Any headers to add to your request, contained within a Headers object or an object literal whose keys are the names of headers and whose values are the header values.Many headers are set automatically by the browser and can't be set by a script; these are called Forbidden header names.

If the `mode` option is set to `no-cors`, you can only set CORS-safelisted request headers.

Data type: String

</td></tr><tr><td>

integrity

</td><td>

Optional. Contains the subresource integrity value of the request. This is checked when the resource is fetched. The browser computes the hash of the fetched resource using the specified algorithm, and if the result does not match the value specified, the browser rejects the fetch request with a network error.The format of this option is `<hash-algo>-<hash-source>` where:

-   &lt;hash-algo&gt;: is one of the following values: sha256, sha384, or sha512.
-   &lt;hash-source&gt;: is the Base64-encoding of the result of hashing the resource with the specified hash algorithm.

Defaults to an empty string.

Data type: String

</td></tr><tr><td>

keepalive

</td><td>

Optional. Flag that indicates whether to abort the associated request if the page that initiated it is unloaded before the request is complete.The body size for `keepalive` requests is limited to 64 kibibytes.

Valid values:

-   true: The browser doesn't abort the associated request.
-   false: Aborts the associated request.

Data type: Boolean

Default: false

</td></tr><tr><td>

method

</td><td>

Optional. The request method.Data type: String

Default: GET

</td></tr><tr><td>

mode

</td><td>

Optional. Sets cross-origin behavior for the request.Valid values:

-   same-origin: Disallows cross-origin requests. If a `same-origin` request is sent to a different origin, the result is a network error.
-   cors: If the request is cross-origin then it will use the Cross-Origin Resource Sharing \(CORS\) mechanism. Only CORS-safelisted response headers are exposed in the response.
-   no-cors: Disables CORS for cross-origin requests. This option comes with the following restrictions:
    -   The method may only be one of `HEAD`, `GET` or `POST`.
    -   The headers may only be CORS-safelisted request headers, with the additional restriction that the Range header is also not allowed. This also applies to any headers added by service workers.
    -   The response is opaque, meaning that its headers and body are not available to JavaScript, and its status code is always `0`.
-   navigate: Used only by HTML navigation. A `navigate` request is created only while navigating between documents.

Data type: String

Default: cors

</td></tr><tr><td>

priority

</td><td>

Optional. Specifies the priority of the fetch request relative to other requests of the same type.Valid values:

-   auto: No user preference for the fetch priority. It is used if no value is set or if an invalid value is set.
-   high: A high priority fetch request relative to other requests of the same type.
-   low: A low priority fetch request relative to other requests of the same type.

Data type: String

Default: auto

</td></tr><tr><td>

redirect

</td><td>

Optional. Determines the browser's behavior in case the server replies with a redirect status.Accepted values:

-   follow: Automatically follow redirects.
-   error: Reject the promise with a network error when a redirect status is returned.
-   manual: Return a response with almost all fields filtered out, to enable a service worker to store the response and later replay it.

Data type: String

Default: follow

</td></tr><tr><td>

referrer

</td><td>

Optional. A string specifying the value to use for the request's Referrer header. Accepted values and data types:

-   about:client: Set the `Referrer` header to the default value for the context of the request \(for example, the URL of the page that made the request\).
-   empty string: Omit the `Referrer` header.
-   same-origin relative or absolute URL: Set the `Referrer` header to the given value. Relative URLs are resolved relative to the URL of the page that made the request.

Default: about:client

</td></tr><tr><td>

referrerPolicy

</td><td>

Optional. A string that sets a policy for the Referrer header. The syntax and semantics of this option are exactly the same as for the Referrer-Policy header.Data type: String

</td></tr><tr><td>

signal

</td><td>

Optional. An AbortSignal. If this option is set, the request can be canceled by calling abort\(\) on the corresponding `AbortController`.Data type: String

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

### Pass options into fetch\(\)

This example shows how to pass the method, body, and headers options directly into the fetch\(\) method:

```
async function post() {
  const response = await fetch("https://example.org/post", {
    method: "POST",
    body: JSON.stringify({ username: "example" }),
    headers: {
      "Content-Type": "application/json",
    },
  });

  console.log(response.status);
}
```

### Pass options into the Request\(\) constructor

This example shows how to create a Request and pass the method, body, and headers options into the constructor and pass the request into fetch\(\):

```
async function post() {
  const request = new Request("https://example.org/post", {
    method: "POST",
    body: JSON.stringify({ username: "example" }),
    headers: {
      "Content-Type": "application/json",
    },
  });

  const response = await fetch(request);

  console.log(response.status);
}
```

### Pass options into both Request\(\) and fetch\(\)

This example shows ho to create a Request\(\) and pass the method, body, and headers options into the constructor. The script then passes the request into fetch\(\) along with the body and referrer options.

In this case the request will be sent with the following options:

-   method: "POST"
-   headers: \{"Content-Type": "application/json"\}
-   body: '\{"username":"example2"\}'
-   referrer: ""

```
async function post() {
  const request = new Request("https://example.org/post", {
    method: "POST",
    headers: {
      "Content-Type": "application/json",
    },
    body: JSON.stringify({ username: "example1" }),
  });

  const response = await fetch(request, {
    body: JSON.stringify({ username: "example2" }),
    referrer: "",
  });

  console.log(response.status);
}
```

