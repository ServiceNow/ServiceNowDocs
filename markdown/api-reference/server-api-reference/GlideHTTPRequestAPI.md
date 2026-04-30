---
title: GlideHTTPRequest - Global
description: The GlideHTTPRequest API provides utility methods to perform common functions with Glide HTTP requests.Adds a header to your HTTP request.Adds a parameter to your HTTP request.Sets a user name and password for basic authentication.Sets the Content-Type header for your HTTP request to the specified value.Enables or disables the follow redirect option for a REST endpoint call.Sets the HTTP timeout value in milliseconds.Sets the log level for an HTTP request.Sets the proxy host and port for the associated REST call.
locale: en-US
release: xanadu
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 6
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# GlideHTTPRequest- Global

The GlideHTTPRequest API provides utility methods to perform common functions with Glide HTTP requests.

You can use this API in global server-side scripts. To use this class, instantiate a GlideHTTPRequest object using the constructor. The constructor requires an endpoint URL as an input parameter.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## GlideHTTPRequest - addHeader\(String name, String value\)

Adds a header to your HTTP request.

|Name|Type|Description|
|----|----|-----------|
|name|String|Header name, such as `Accept` or `Content-Type`.|
|value|String|Header value, such as `application/json`.|

|Type|Description|
|----|-----------|
|void| |

This example adds the request header "Accept" and returns the number of the incidents from a ServiceNow Instance, parsing the JSON or XML responses.

```
var instance = 'dev12345';
var username = 'admin';
var password = 'yourpassword';

// Instantiate request with ServiceNow API incidents table endpoint
var request = new GlideHTTPRequest('https://'+instance+'.service-now.com/api/now/table/incident');

// Add authentication data
request.setBasicAuth(username, password);

// Add the Accept header to get JSON response
request.addHeader('Accept', 'application/json');

// Execute the GET request
var response = request.get();

// Print the results: status code and number of records returned
gs.print(response.getStatusCode());
gs.print('(JSON) Incidents returned: ' + JSON.parse(response.getBody()).result.length);

// Replace the Accept header to get XML response
request.addHeader('Accept', 'application/xml');

// Execute the GET request
var response = request.get();

// Print the results: status code and number of records returned
gs.print(response.getStatusCode());
gs.print('(XML) Incidents returned: ' + gs.xmlToJSON(response.getBody()).response.result.length);
```

Output

```
200
(JSON) Incidents returned: 66
200
(XML) Incidents returned: 66
```

## GlideHTTPRequest - addParameter\(String name, String value\)

Adds a parameter to your HTTP request.

|Name|Type|Description|
|----|----|-----------|
|name|String|Parameter to add, such as **sysparm\_limit**.|
|value|String|Value for the parameter.|

|Type|Description|
|----|-----------|
|void| |

This example shows how to add the **sysparm\_limit** parameter to the REST endpoint call to limit the number of returned responses.

```
var instance = 'dev12345';
var username = 'admin';
var password = 'yourpassword';

// Instantiate request with ServiceNow API incidents table endpoint
var request = new GlideHTTPRequest('https://'+instance+'.service-now.com/api/now/table/incident');

// Add authentication data
request.setBasicAuth(username, password);

// Add the 'sysparm_limit' parameter to limit the number of records returned
request.addParameter('sysparm_limit', 1);

// Execute the GET request
var response = request.get();

// Print the results: status code and number of records returned
gs.print(response.getStatusCode());
gs.print('Incidents returned: ' + JSON.parse(response.getBody()).result.length);
```

Output:

```
200
Incidents returned: 1
```

## GlideHTTPRequest - setBasicAuth\(String userName, String password\)

Sets a user name and password for basic authentication.

|Name|Type|Description|
|----|----|-----------|
|userName|String|User name to use for authentication.|
|password|String|User's password to use for authentication.|

|Type|Description|
|----|-----------|
|void| |

This example shows how to use the setBasicAuth\(\) method to set the user name and password for the associated REST endpoint call.

```
var instance = 'dev12345';
var username = 'admin';
var password = 'yourpassword';

// Instantiate request with ServiceNow API incidents table endpoint
var request = new GlideHTTPRequest('https://'+instance+'.service-now.com/api/now/table/incident');

// Add authentication data
request.setBasicAuth(username, password);

// Add the Accept header to get JSON response
request.addHeader('Accept', 'application/json');

// Execute the GET request
var response = request.get();

// Print the results: status code and number of records returned
gs.print(response.getStatusCode());
gs.print('(JSON) Incidents returned: ' + JSON.parse(response.getBody()).result.length);

// Replace the Accept header to get XML response
request.addHeader('Accept', 'application/xml');

// Execute the GET request
var response = request.get();

// Print the results: status code and number of records returned
gs.print(response.getStatusCode());
gs.print('(XML) Incidents returned: ' + gs.xmlToJSON(response.getBody()).response.result.length);
```

Output

```
200
(JSON) Incidents returned: 66
200
(XML) Incidents returned: 66
```

## GlideHTTPRequest - setContentType\(String type\)

Sets the Content-Type header for your HTTP request to the specified value.

|Name|Type|Description|
|----|----|-----------|
|type|String|Content type to set, such as `application/json` or `multipart/form-data`. For additional information on Content-Type, see [https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Type](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Type).|

|Type|Description|
|----|-----------|
|void| |

This example shows how to set the `Content-Type` request header for a REST endpoint call using the setContentType\(\) method.

```
var instance = 'dev12345';
var username = 'admin';
var password = 'yourpassword';

// Instantiate request with ServiceNow API incidents table endpoint
var request = new GlideHTTPRequest('https://'+instance+'.service-now.com/api/now/table/incident');

// Add authentication data
request.setBasicAuth(username, password);

// Set up incident record to post

// Set the Content-Type of the POST
request.setContentType('application/json');

// Execute the POST request
var response = request.post();

// Print the results: status code and number of records returned
gs.print(response.getStatusCode());
```

Output

```
200

```

## GlideHTTPRequest - setFollowRedirect\(boolean followRedirect\)

Enables or disables the follow redirect option for a REST endpoint call.

For additional information on HTTP redirects, see [https://developer.mozilla.org/en-US/docs/Web/HTTP/Redirections](https://developer.mozilla.org/en-US/docs/Web/HTTP/Redirections).

<table id="table_kzt_pwy_cfb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

followRedirect

</td><td>

Boolean

</td><td>

Flag that indicates whether the endpoint should follow any URL redirect returned by the endpoint. Valid values:

-   true: Following any returned redirect.
-   false: Ignore any returned redirect.

Default: true

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

This example shows how to turn off redirects for an endpoint call using the setFollowRedirect\(\) method.

```
var instance = 'dev12345';
var username = 'admin';
var password = 'yourpassword';

// Instantiate request with ServiceNow API incidents table endpoint
var request = new GlideHTTPRequest('https://'+instance+'.service-now.com/api/now/table/incident');

// Add authentication data
request.setBasicAuth(username, password);

// Add the Accept header to get JSON response
request.addHeader('Accept', 'application/json');

// Turn off follow redirect - default is on (true)
request.setFollowRedirect(false);

// Execute the GET request
var response = request.get();

// Print the results: status code and number of records returned
gs.print(response.getStatusCode());
```

Output

```
200
```

## GlideHTTPRequest - setHttpTimeout\(int timeout\)

Sets the HTTP timeout value in milliseconds.

<table id="table_rjp_1ly_cfb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

timeout

</td><td>

Integer

</td><td>

Timeout value to set.Unit: Milliseconds

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

This example shows how to set the time out value for an endpoint call using the setTimeout\(\) method.

```
var instance = 'dev12345';
var username = 'admin';
var password = 'yourpassword';

// Instantiate request with ServiceNow API incidents table endpoint
var request = new GlideHTTPRequest('https://'+instance+'.service-now.com/api/now/table/incident');

// Add authentication data
request.setBasicAuth(username, password);

// Add the Accept header to get JSON response
request.addHeader('Accept', 'application/json');

// Set the time out value
request.setHttpTimeOut(1000);

// Execute the GET request
var response = request.get();

// Print the results: status code and number of records returned
gs.print(response.getStatusCode());
```

Output

```
200
```

## GlideHTTPRequest - setLogLevel\(String logLevel\)

Sets the log level for an HTTP request.

<table id="table_ijx_myy_cfb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

logLevel

</td><td>

String

</td><td>

The level of logging available. **Note:** For performance reasons, in production it is advisable to leave HTTP request logging at **basic**.

 Valid values:

 -   basic: Covers many of the attributes of the HTTP transaction including host, path, response status, and so on.
-   elevated: Includes all of **basic**, as well as all request headers, the query string, and all response headers.
-   all: Includes all of **elevated**, as well as the request body and the response body.

 Default: basic

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

This example shows how to set the log level for an endpoint call using the setLogLevel\(\) method.

```
var instance = 'dev12345';
var username = 'admin';
var password = 'yourpassword';

// Instantiate request with ServiceNow API incidents table endpoint
var request = new GlideHTTPRequest('https://'+instance+'.service-now.com/api/now/table/incident');

// Add authentication data
request.setBasicAuth(username, password);

// Add the Accept header to get JSON response
request.addHeader('Accept', 'application/json');

// Set the time out value
request.setLogLevel(elevated);

// Execute the GET request
var response = request.get();

// Print the results: status code and number of records returned
gs.print(response.getStatusCode());
```

Output

```
200
```

## GlideHTTPRequest - setupProxy\(String host, String port\)

Sets the proxy host and port for the associated REST call.

|Name|Type|Description|
|----|----|-----------|
|host|String|Proxy host|
|port|String|Proxy port|

|Type|Description|
|----|-----------|
|void| |

