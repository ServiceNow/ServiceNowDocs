---
title: Fetch - Scoped, Global
description: The Fetch API provides methods for fetching resources using request and response objects.Starts the process of fetching a resource from the network and returns a promise that is fulfilled once the response is available.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# Fetch - Scoped, Global

The Fetch API provides methods for fetching resources using request and response objects.

You can use the Fetch API in a background script and wherever you can make HTTP calls \(like a REST endpoint\). The Fetch API allows you to make both simple and more complicated fetch requests by setting headers, body options, and so on.

This API is part of a set of Fetch APIs, which provide various actions for fetching resources from external websites. The full Fetch API collection includes:

-   [Fetch - fetch\(String resource, Object options\)](FetchAPI.md#): Starts the process of fetching a resource from the network.
-   [Fetch Headers - Scoped, Global](Fetch.HeadersAPI.md#): Retrieve and modify request and response headers.
-   [Fetch Request - Scoped, Global](Fetch.RequestAPI.md#): Create a new request object.
-   [Fetch RequestInit - Scoped, Global](Fetch.RequestInitAPI.md#): Set options to configure a fetch request.
-   [Fetch Response - Scoped,Global](Fetch.ResponseAPI.md#): Create a new response object.

To support fetch actions, the system property, `glide.hosts.allowlist`, allows controls over what hosts a fetch method can access. It applies to HTTP APIs like RestMessageV2 and those mentioned above. For more information about `glide.hosts.allowlist`, see [Available system properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/r_AvailableSystemProperties.md).

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## Fetch - fetch\(String resource, Object options\)

Starts the process of fetching a resource from the network and returns a promise that is fulfilled once the response is available.

<table id="table_arq_npb_jdc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

resource

</td><td>

String or Object

</td><td>

Required. The resource to fetch. Accepted values:

-   A string or an object with a stringifier, including a URL object, that provides the URL of the resource you want to fetch. The URL may be relative to the base URL which is the document's baseURI.
-   A [Fetch Request - Request\(\)](Fetch.RequestAPI.md#) object.

</td></tr><tr><td>

options

</td><td>

Object

</td><td>

Optional. A [Fetch RequestInit - Scoped, Global](Fetch.RequestInitAPI.md#) object containing custom settings to apply to the request.Default: The request is passed without any customization settings.

</td></tr></tbody>
</table><table id="table_brq_npb_jdc" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

A promise that resolves to a response object.A fetch\(\) promise only rejects when the request fails, for example, because of a badly-formed request URL or a network error.

**Note:** A fetch\(\) promise is not considered as rejected if the server responds with HTTP status codes that indicate errors like 404 or 504. In this instance, use a then\(\) handler to check the ok and status [Fetch Response - Scoped,Global](Fetch.ResponseAPI.md#)properties.

</td></tr></tbody>
</table>The following example demonstrates how to form a new Request object using [Fetch Request - Request\(\)](Fetch.RequestAPI.md#) and then fetch\(\) to retrieve its data. Here is a simple explanation of how each part of the code is used:

-   request\(\): Configures the API request with URL, method, and headers.
-   fetch\(\): Makes the fetch request.
-   response.json\(\): Parses the JSON response body into a JavaScript object. \(See [Fetch Response - json\(\)](Fetch.ResponseAPI.md#) for more information.\)
-   console.log\(\): Outputs the incidents \(data.result\) using the Console API \(See [Console - log\(Object val1...val2, String msg, String subst1...subst2\)](../../Console/concept/ConsoleAPI.md#)\).

```
async function fetchIncidents() {
    const url = 'https://your-instance.service-now.com/api/now/table/incident';
    const username = 'your_username';
    const password = 'your_password';

    // Create a Request object
    const request = new Request(url, {
        method: 'GET',
        headers: {
            'Content-Type': 'application/json',
            Authorization: 'Basic ' + btoa(`${username}:${password}`)
        }
    });

    // Fetch data and use response.json() to process it
    const response = await fetch(request);
    const data = await response.json(); // Parse the response to JSON
    console.log(data.result); // Log the incidents data to system logs
}

fetchIncidents();
```

Output:

```
[
    { "number": "INC0001", "short_description": "System outage" },
    { "number": "INC0002", "short_description": "Password reset request" }
]
```

