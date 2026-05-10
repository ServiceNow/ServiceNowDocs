---
title: Fetch Response - Scoped,Global
description: The Fetch Response API provides methods for creating a new Response object and for handling the response body created by a Fetch Request API method.Creates a new Response object using the Response\(\) constructor.Returns a promise that resolves with an ArrayBuffer.Returns a promise that resolves with a Blob.Returns a promise that resolves with an Uint8Array.Returns a promise that resolves with a FormData object.Returns a promise that resolves to the result of parsing the body text as JSON.Reads the response body and returns it as a plain string. The response is always decoded using UTF-8.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 12
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# Fetch Response- Scoped,Global

The Fetch Response API provides methods for creating a new Response object and for handling the response body created by a Fetch Request API method.

The Fetch Response API is part of a set of Fetch APIs, which provide various actions for fetching resources from external websites. The full Fetch API collection includes:

-   [Fetch - fetch\(String resource, Object options\)](FetchAPI.md#): Starts the process of fetching a resource from the network.
-   [Fetch Headers - Scoped, Global](Fetch.HeadersAPI.md#): Retrieve and modify request and response headers.
-   [Fetch Request - Scoped, Global](Fetch.RequestAPI.md#): Create a new request object.
-   [Fetch RequestInit - Scoped, Global](Fetch.RequestInitAPI.md#): Set options to configure a fetch request.
-   [Fetch Response - Scoped,Global](Fetch.ResponseAPI.md#): Create a new response object.

To support fetch actions, the system property, `glide.hosts.allowlist`, allows controls over what hosts a fetch method can access. It applies to HTTP APIs like RestMessageV2 and those mentioned above. For more information about `glide.hosts.allowlist`, see [Available system properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/r_AvailableSystemProperties.md).

## Response properties

The Response API provides properties that return details about the HTTP response. These properties allow you to access metadata \(like `status`, `headers`, `type`\) and the response body \(`body`\) for further processing. They enable checking the success of a request \(`ok`\) and parsing the returned data in various formats \(for example, JSON or text\). These properties are important for validating and handling server responses in client-side applications. To read more in-depth explanations about each property, see [https://developer.mozilla.org/en-US/docs/Web/API/Response](https://developer.mozilla.org/en-US/docs/Web/API/Response).

<table id="table_t5x_2qw_jdc"><thead><tr><th>

Property name

</th><th>

Description

</th><th>

Example

</th></tr></thead><tbody><tr><td>

body

</td><td>

Ready-only. Contains a readable stream of byte data in the response body contents.Valid values: A ReadableStream or null.

Data type: String

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

Ready-only. Flag that indicates whether the body has been read yet.Accepted values:

-   true: Body has been read.
-   false: Body hasn't been read.

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

headers

</td><td>

Read-only. The Headers object associated with the response.Data type: Headers object

</td><td>

```
const myRequest = new Request("flowers.jpg");
const myHeaders = myRequest.headers; // Headers {}
```

</td></tr><tr><td>

ok

</td><td>

Ready-only. Flag indicating whether the response was successful \(status in the range 200-299\) or not.Accepted values:

-   true: The response was successful.
-   false: The response wasn't successful.

Data type: Boolean

</td><td>

```
const myImage = document.querySelector("img");

const myRequest = new Request("flowers.jpg");

fetch(myRequest).then((response) => {
  console.log(response.ok); // returns true if the response returned successfully
  response.blob().then((myBlob) => {
    const objectURL = URL.createObjectURL(myBlob);
    myImage.src = objectURL;
  });
});
```

</td></tr><tr><td>

redirected

</td><td>

Read-only. Flag indicating whether the response is a result that the request was redirected.Accepted values:

-   true: request was redirected.
-   false: request wasn't redirected.

Data type: Boolean

</td><td>

```
const myRequest = new Request("flowers.jpg");
const myCred = myRequest.redirect;
```

</td></tr><tr><td>

status

</td><td>

Read-only. HTTP status codes of the response. For example, 200 for a success.Data type: Number

</td><td>

```
const myImage = document.querySelector("img");

const myRequest = new Request("flowers.jpg");

fetch(myRequest)
  .then((response) => {
    console.log("response.status =", response.status); // response.status = 200
    return response.blob();
  })
  .then((myBlob) => {
    const objectURL = URL.createObjectURL(myBlob);
    myImage.src = objectURL;
  });
```

</td></tr><tr><td>

statusText

</td><td>

Read-only. Status message corresponding to the HTTP status code in response.status. For example, this would be `OK` for a status code `200`, `Continue` for `100`, `Not Found` for `404`.Data type: String

</td><td>

```
const myRequest = new Request("flowers.jpg");

 // Log the HTTP status and status text
    console.log(`Status: ${response.status}`);
    console.log(`Status Text: ${response.statusText}`);
    
    // Check if the response is successful
    if (response.ok) {
      console.log("Request succeeded!");
    } else {
      console.log("Request failed.");
    }
  } catch (error) {
    console.error("Error fetching the URL:", error);
  }
}
```

</td></tr><tr><td>

type

</td><td>

Read-only. Type of response.Accepted values:

-   basic: Normal, same origin response, with all headers exposed except "Set-Cookie".
-   cors: Response was received from a valid cross-origin request. Certain headers and the body may be accessed.
-   error: Network error. No useful information describing the error is available. The Response's status is 0, headers are empty and immutable. This is the type for a Response obtained from `Response.error()`.
-   opaque: Response for "no-cors" request to cross-origin resource. Severely restricted.
-   opaqueredirect: The fetch request was made with `redirect: "manual"`. The Response's status is 0, headers are empty, body is null and trailer is empty.

Data type: String

</td><td>

```
const myImage = document.querySelector("img");

const myRequest = new Request("flowers.jpg");

fetch(myRequest)
  .then((response) => {
    console.log("response.type =", response.type); // response.type = 'basic'
    return response.blob();
  })
  .then((myBlob) => {
    const objectURL = URL.createObjectURL(myBlob);
    myImage.src = objectURL;
  });
```

</td></tr><tr><td>

url

</td><td>

Read-only. URL of the response.Data type: String

</td><td>

```
const myRequest = new Request("flowers.jpg");
const myURL = myRequest.url; // "https://github.com/mdn/dom-examples/tree/main/fetch/fetch-request/flowers.jpg"
```

</td></tr></tbody>
</table>**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## Fetch Response - Response\(Object body, Object options\)

Creates a new Response object using the Response\(\) constructor.

<table id="table_bt1_vly_12c" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

body

</td><td>

Object

</td><td>

Optional. An object defining a body for the response.Valid types:

-   ArrayBuffer
-   Blob
-   DataView
-   FormData
-   ReadableStream
-   String
-   String literal
-   TypedArray
-   URLSearchParams

Default: null

</td></tr><tr><td>

options

</td><td>

Object

</td><td>

Optional. An options object containing any custom settings that you want to apply to the response, or an empty object \(which is the default value\). The possible options are:-   headers: Any headers you want to add to your response, contained within a [Fetch Headers - Scoped, Global](Fetch.HeadersAPI.md#) object or object literal of string key/value pairs \(see [HTTP headers](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers) for a reference\). Empty by default.
-   status: The status code for the response. The default value is `200`.
-   statusText: The status message associated with the status code, such as `"OK"`. The default value is `""`.

</td></tr></tbody>
</table>In this example, we create a new Response object using the constructor, passing a new Blob as a body, and an init object containing custom status and statusText options:

```
const myBlob = new Blob();
const myOptions = { status: 200, statusText: "Status message!" };
const myResponse = new Response(myBlob, myOptions);
```

## Fetch Response - arrayBuffer\(\)

Returns a promise that resolves with an ArrayBuffer.

The arrayBuffer\(\) method is useful when working with binary data like images, audio files, or any other binary file that needs to be processed.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Object|A promise that resolves with an [ArrayBuffer](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/ArrayBuffer), which represents a generic raw binary data buffer.|

<table id="table_szf_1gs_kdc" class="returns"><thead><tr><th>

Exception

</th><th>

Description

</th></tr></thead><tbody><tr><td>

DOMException - AbortError

</td><td>

An exception stating that the request was aborted.

</td></tr><tr><td>

TypeError

</td><td>

Thrown for one of the following reasons: -   The response body is disturbed or locked.
-   There was an error decoding the body content \(for example, because the Content-Encoding header is incorrect\).

</td></tr><tr><td>

RangeError

</td><td>

There was a problem creating the associated `ArrayBuffer`. For example, if the data size is too large.

</td></tr></tbody>
</table>The following example script fetches binary data from a server and processes it while utilizing the arrayBuffer\(\) method using these steps:

1.  fetch\(\): Fetches a resource from the specified URL.
2.  **response.ok**: Checks if the response status is in the 200-299 range.
3.  arrayBuffer\(\): Reads the response body and converts it into an ArrayBuffer, which represents a generic, fixed-length raw binary data buffer.
4.  Uint8Array: Converts the ArrayBuffer into a Uint8Array, which is a typed array for easy manipulation of binary data.

```
javascriptCopy code// Simple API to fetch binary data and process it using arrayBuffer()asyncfunctionfetchBinaryData(url) {
  try {
    // Fetch the resource from the provided URLconst response = awaitfetch(url);

    // Check if the response is successfulif (!response.ok) {
      thrownewError(`HTTP error! Status: ${response.status}`);
    }

    // Convert the response body to an ArrayBufferconst arrayBuffer = await response.arrayBuffer();

    // Process the ArrayBuffer (e.g., convert it to a typed array)const uint8Array = newUint8Array(arrayBuffer);

    // Return the processed datareturn uint8Array;
  } catch (error) {
    console.error("Error fetching or processing binary data:", error);
    throw error;
  }
}

// Example usageconst binaryDataUrl = 'https://example.com/path/to/binary/data';

fetchBinaryData(binaryDataUrl)
  .then((data) => {
    console.log("Binary data as Uint8Array:", data);
    // Further processing can be done here, e.g., rendering an image or playing audio
  })
  .catch((error) => {
    console.error("Failed to fetch binary data:", error);
  });
```

## Fetch Response - blob\(\)

Returns a promise that resolves with a Blob.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Object|A promise that resolves with a [Blob](https://developer.mozilla.org/en-US/docs/Web/API/Blob).|

<table id="table_szf_1gs_kdc" class="returns"><thead><tr><th>

Exception

</th><th>

Description

</th></tr></thead><tbody><tr><td>

DOMException - AbortError

</td><td>

An exception stating that the request was aborted.

</td></tr><tr><td>

TypeError

</td><td>

Thrown for one of the following reasons: -   The response body is disturbed or locked.
-   There was an error decoding the body content \(for example, because the Content-Encoding header is incorrect\).

</td></tr></tbody>
</table>The following example demonstrates how to use the blob\(\) method with the Fetch API using the following steps. This use case is great for fetching images or other binary content \(like videos or PDFs\) and displaying them dynamically.

1.  fetch\(url\): Fetches a resource from the specified URL.
2.  response.blob\(\): Converts the response body into a Blob object, which represents binary data.
3.  URL.createObjectURL\(blob\): Generates a temporary URL for the Blob, which can be used in the DOM \(for example, as an image source\).
4.  Appending the image to the DOM: Dynamically creates an image element, sets the blob URL as its source, and appends it to the document body.

```

async function fetchBlob(url) {
  try {
    // Fetch the resource from the provided URL
    const response = await fetch(url);

    // Check if the response is successful
    if (!response.ok) {
      throw new Error(`HTTP error! Status: ${response.status}`);
    }

    // Convert the response body to a Blob
    const blob = await response.blob();

    // Create a URL for the Blob and log it
    const blobUrl = URL.createObjectURL(blob);
    console.log("Blob URL:", blobUrl);

    // For example, you can set it as the source of an image
    const img = document.createElement('img');
    img.src = blobUrl;
    img.alt = "Fetched Blob Image";
    document.body.appendChild(img);
  } catch (error) {
    console.error("Error fetching or processing blob:", error);
  }
}

// Example usage with an image URL
const imageUrl = 'https://via.placeholder.com/150';
fetchBlob(imageUrl);
```

## Fetch Response - bytes\(\)

Returns a promise that resolves with an Uint8Array.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Object|A promise that resolves with an Uint8Array.|

<table id="table_szf_1gs_kdc" class="returns"><thead><tr><th>

Exception

</th><th>

Description

</th></tr></thead><tbody><tr><td>

DOMException- AbortError

</td><td>

The request was aborted.

</td></tr><tr><td>

TypeError

</td><td>

Thrown for one of the following reasons: -   The response body is disturbed or locked.
-   There was an error decoding the body content \(for example, because the Content-Encoding header is incorrect\).

</td></tr><tr><td>

RangeError

</td><td>

There was a problem creating the associated `ArrayBuffer`. For example, if the data size is too large.

</td></tr></tbody>
</table>The following example shows how to fetch a text file, return the body as a Uint8Array, and then decode this into a string.

```
const response = await fetch("https://www.example.com/textfile.txt");
const textFile = await response.bytes();
const string = new TextDecoder().decode(textFile);
console.log(string);
```

## Fetch Response - formData\(\)

Returns a promise that resolves with a FormData object.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Object|A promise that resolves with a [FormData](https://developer.mozilla.org/en-US/docs/Web/API/FormData) object.|

<table id="table_szf_1gs_kdc" class="returns"><thead><tr><th>

Exception

</th><th>

Description

</th></tr></thead><tbody><tr><td>

DOMException- AbortError

</td><td>

The request was aborted.

</td></tr><tr><td>

TypeError

</td><td>

Thrown for one of the following reasons: -   The response body is disturbed or locked.
-   There was an error decoding the body content \(for example, because the Content-Encoding header is incorrect\).

</td></tr></tbody>
</table>The following example demonstrates how to use formData\(\) to process a form submission response using the following steps:

1.  Request Body: Used `JSON.stringify()` to send the form data as JSON instead of URL-encoded parameters.
2.  Content-Type: Set to `application/json` to indicate the request body format.

```
// Example of using Response.formData()
async function fetchFormData(url) {
  try {
    // Make a POST request to fetch the form data
    const response = await fetch(url, {
      method: 'POST',
      body: JSON.stringify({
        name: 'John Doe',
        email: 'john.doe@example.com',
      }),
      headers: {
        'Content-Type': 'application/json',
      },
    });

    // Check if the response is successful
    if (!response.ok) {
      throw new Error(`HTTP error! Status: ${response.status}`);
    }

    // Parse the response as FormData
    const formData = await response.formData();

    // Iterate through the FormData entries
    for (const [key, value] of formData.entries()) {
      console.log(`${key}: ${value}`);
    }
  } catch (error) {
    console.error("Error fetching or processing form data:", error);
  }
}

// Example usage
const formEndpoint = 'https://httpbin.org/post'; // Replace with your form endpoint
fetchFormData(formEndpoint);
```

Output:

```
name: John Doe
email: john.doe@example.com
```

## Fetch Response - json\(\)

Returns a promise that resolves to the result of parsing the body text as JSON.

**Note:** Despite the name of this method, the result of json\(\) is not JSON but is instead the result of taking JSON as input and parsing it to produce a JavaScript object.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Object|A promise that resolves to a JavaScript object. This object could be anything that can be represented by JSON, like an object, array, string, number, and so on.|

<table id="table_szf_1gs_kdc" class="returns"><thead><tr><th>

Exception

</th><th>

Description

</th></tr></thead><tbody><tr><td>

DOMException- AbortError

</td><td>

The request was aborted.

</td></tr><tr><td>

TypeError

</td><td>

Thrown for one of the following reasons: -   The response body is disturbed or locked.
-   There was an error decoding the body content \(for example, because the Content-Encoding header is incorrect\).

</td></tr><tr><td>

SyntaxError

</td><td>

The response body cannot be parsed as JSON.

</td></tr></tbody>
</table>The following example demonstrates how to use json\(\) to form a response:

1.  fetch\(\) makes a GET request to the URL.
2.  The **response.ok** checks if the request was successful \(status code 200–299\).
3.  If successful, response.json\(\) is called to parse the JSON data from the response.
4.  The parsed data is logged to system logs using the Console API. If any error occurs during the request or parsing, it's caught and logged.

```
fetch('https://jsonplaceholder.typicode.com/posts/1')
  .then(response => {
    if (!response.ok) {
      throw new Error('Network response was not ok');
    }
    return response.json();
  })
  .then(data => console.log(data))
  .catch(error => console.error('Fetch error:', error));
```

## Fetch Response - text\(\)

Reads the response body and returns it as a plain string. The response is always decoded using UTF-8.

The text\(\) method is useful for responses that contain textual data, such as HTML, JSON \(if you want to handle it manually\), XML, or plain text files that are meant to be treated as plain strings.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|None|A promise that resolves with a UTF-8-enconded string.|

<table id="table_szf_1gs_kdc" class="returns"><thead><tr><th>

Exception

</th><th>

Description

</th></tr></thead><tbody><tr><td>

DOMException- AbortError

</td><td>

The request was aborted.

</td></tr><tr><td>

TypeError

</td><td>

Thrown for one of the following reasons: -   The response body is disturbed or locked.
-   There was an error decoding the body content \(for example, because the Content-Encoding header is incorrect\).

</td></tr></tbody>
</table>The following example shows how a simple way to use text\(\) when the server returns plain text, like `Hello, world! This is a sample response`.

```
const response = awaitfetch('https://example.com/text-endpoint');
const text = await response.text();
console.log(text); // Outputs: Hello, world! This is a sample response.
```

Output:

```
Hello, world! This is a sample response.
```

