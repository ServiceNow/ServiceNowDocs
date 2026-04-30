---
title: GlideHTTPResponse - Global
description: The GlideHTTPResponse API provides utility methods to perform common functions with Glide HTTP responses.Returns a list of all headers.Returns a string containing the body for the HTTP response.Returns the list of cookies associated with an endpoint call.Returns the current error code returned by an endpoint.Returns the last error encountered.Returns the header specified in the passed-in parameter.Returns all headers associated with the endpoint response.Returns the HTTP method associated with the specified endpoint call.Returns the last status code for an endpoint call.Returns a flag that indicates whether there were any errors while processing the endpoint call.
locale: en-US
release: xanadu
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 8
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# GlideHTTPResponse- Global

The GlideHTTPResponse API provides utility methods to perform common functions with Glide HTTP responses.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## GlideHTTPResponse - getAllHeaders\(\)

Returns a list of all headers.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Array|List of all the headers associated with the endpoint call.|

This example shows how to delete a specified incident from the Incident table using the del\(\) method.

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

// Print all headers associated with the endpoint call
gs.print(response.getAllHeaders());
```

Output

```
[
  X-Is-Logged-In: true, 
  X-Transaction-ID: 21a9223f1b13, 
  X-Total-Count: 69,
  X-Content-Type-Options: nosniff,
  Pragma: no-store,no-cache,
  Cache-Control: no-cache,no-store,must-revalidate,
  max-age=-1,
  Expires: 0,
  Content-Type: application/json;charset=UTF-8,
  Transfer-Encoding: chunked,
  Date: Tue, 26 Oct 2021 16:54:24 GMT,
  Server: ServiceNow,
  Set-Cookie: JSESSIONID=36B9B3E86C31E244A50AF38106376F9B; Path=/; HttpOnly; SameSite=None; Secure,
  Set-Cookie: glide_user=; Max-Age=0; Expires=Thu, 01-Jan-1970 00:00:10 GMT; Path=/; HttpOnly; SameSite=None; Secure,
  Set-Cookie: glide_user_session=; Max-Age=0; Expires=Thu, 01-Jan-1970 00:00:10 GMT; Path=/; HttpOnly; SameSite=None; Secure,
  Set-Cookie: glide_user_route=glide.455981d2bb48a9658f44c18e5f56313d; Max-Age=2147483647; Expires=Sun, 13-Nov-2089 20:08:31 GMT; Path=/; HttpOnly; SameSite=None; Secure,
  Set-Cookie: glide_session_store=E9A9223F1B1370107CF30D03CD4BCB8D; Max-Age=1800; Expires=Tue, 26-Oct-2021 17:24:24 GMT; Path=/; HttpOnly; SameSite=None; Secure,
  Set-Cookie: BIGipServerpool_jsmith=428037898.31808.0000; path=/; Httponly; Secure; SameSite=None; Secure, Strict-Transport-Security: max-age=63072000; includeSubDomains
]

```

## GlideHTTPResponse - getBody\(\)

Returns a string containing the body for the HTTP response.

**Note:** If the stream has already been accessed, it cannot be accessed again. In this case the method will return null.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|HTTP response body.|

This example shows how to use the getBody\(\) method to display the contents of the return results of an endpoint call.

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
request.addHeader('Content-Type','application/json');
 
var response = request.post('{"short_description":"Test me"}');
 
gs.print(response.getStatusCode());
gs.print(response.getBody());
```

Output

```
201
{
  "result":{
    "parent":"",
    "made_sla":"true",
    "caused_by":"",
    "watch_list":"",
    "upon_reject":"cancel",
    "sys_updated_on":"2021-10-26 14:59:22",
    "child_incidents":"0",
    "hold_reason":"",
    "task_effective_number":"INC0010003",
    "approval_history":"",
    "skills":"",
    "number":"INC0010003",
    "resolved_by":"",
    "sys_updated_by":"admin",
    "opened_by":{
      "link":"https://instanceName.servicenow.com/api/now/table/sys_user/6816f79cc0a8016401c5a33be04be441",
      "value":"6816f79cc0a8016401c5a33be04be441"
    },
    "user_input":"",
    "sys_created_on":"2021-10-26 14:59:22",
    "sys_domain":{
      "link":"https://instanceName.servicenow.com/api/now/table/sys_user_group/global",
      "value":"global"
    },
    "state":"1",
    "route_reason":"",
    "sys_created_by":"admin",
    "knowledge":"false",
    "order":"",
    "calendar_stc":"",
    "closed_at":"",
    "cmdb_ci":"",
    "delivery_plan":"",
    "contract":"",
    "impact":"3",
    "active":"true",
    "work_notes_list":"",
    "business_service":"",
    "priority":"5",
    "sys_domain_path":"/",
    "rfc":"",
    "time_worked":"",
    "expected_start":"",
    "opened_at":"2021-10-26 14:59:22",
    "business_duration":"",
    "group_list":"",
    "work_end":"",
    "caller_id":"",
    "reopened_time":"",
    "resolved_at":"",
    "approval_set":"",
    "subcategory":"",
    "work_notes":"",
    "universal_request":"",
    "short_description":"Test me",
    "close_code":"",
    "correlation_display":"",
    "delivery_task":"",
    "work_start":"",
    "assignment_group":"",
    "additional_assignee_list":"",
    "business_stc":"",
    "description":"",
    "calendar_duration":"",
    "close_notes":"",
    "notify":"1",
    "service_offering":"",
    "sys_class_name":"incident",
    "closed_by":"",
    "follow_up":"",
    "parent_incident":"",
    "sys_id":"a85f82ffdb5f30103dd9c39d13961916",
    "contact_type":"",
    "reopened_by":"",
    "incident_state":"1",
    "urgency":"3",
    "problem_id":"",
    "company":"",
    "reassignment_count":"0",
    "activity_due":"",
    "assigned_to":"",
    "severity":"3",
    "comments":"",
    "approval":"not requested",
    "sla_due":"",
    "comments_and_work_notes":"",
    "due_date":"",
    "sys_mod_count":"0",
    "reopen_count":"0",
    "sys_tags":"",
    "escalation":"0",
    "upon_approval":"proceed",
    "correlation_id":"",
    "location":"",
    "category":"inquiry"
  }
}
```

## GlideHTTPResponse - getCookies\(\)

Returns the list of cookies associated with an endpoint call.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Array|List containing the name and value of each cookie as a string.|

This example shows how to use the getCookies\(\) method to display the cookies associated with a endpoint response.

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
gs.print(response.getCookies());
```

Output

```
200
[
  JSESSIONID=B8E5C1C0E43FEA35EC0FCB323A9DF8D1; 
  Path=/; HttpOnly; SameSite=None; Secure, glide_user=; Max-Age=0; Expires=Thu, 01-Jan-1970 00:00:10 GMT;
  Path=/; HttpOnly; SameSite=None; Secure, glide_user_session=; Max-Age=0; Expires=Thu, 01-Jan-1970 00:00:10 GMT;
  Path=/; HttpOnly; SameSite=None; Secure, glide_user_route=glide.f1aa2015b3fa5fa8dfe567386cde8fd5; Max-Age=2147483647; Expires=Sun, 13-Nov-2089 21:02:31 GMT;
  Path=/; HttpOnly; SameSite=None; Secure, glide_session_store=7406BAB7DBDF30103DD9C39D13961966; Max-Age=1800; Expires=Tue, 26-Oct-2021 18:18:24 GMT;
  Path=/; HttpOnly; SameSite=None; Secure, BIGipServerpool_jsmith=2643023626.45630.0000; path=/; Httponly; Secure; SameSite=None; Secure
]
```

## GlideHTTPResponse - getErrorCode\(\)

Returns the current error code returned by an endpoint.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Integer|The error code. 0 is returned if there are no errors.|

This example shows how to view the error code of the last error message thrown by the instance for the associated REST call using the getErrorCode\(\) method.

```
var instance = 'dev12345'; // Instance name
var username = 'admin';
var password = 'yourpassword';
var sysId = '0123456789abcdef0123456789abcdef';  // Sys_id of the incident to get

// Instantiate request with the ServiceNow API incident table endpoint for deletion of an incident
var endpoint = 'https://' + instance + '.service-now.com/api/now/table/incident/' + sysId;
var request = new GlideHTTPRequest(endpoint);

// Add authentication data
request.setBasicAuth(username, password);

// Delete the incident
response = request.get();

// Print the results: status code and response body
gs.print(response.getStatusCode());

// Get the last error message
gs.print(response.getErrorCode());
```

Output

```
404
1
```

## GlideHTTPResponse - getErrorMessage\(\)

Returns the last error encountered.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Text string that describes the last error encountered.|

This example shows how to view the last error message thrown by the instance for the associated REST call using the getErrorMessage\(\) method.

```
var instance = 'dev12345'; // Instance name
var username = 'admin';
var password = 'yourpassword';
var sysId = '0123456789abcdef0123456789abcdef';  // Sys_id of the incident to get

// Instantiate request with the ServiceNow API incident table endpoint for deletion of an incident
var endpoint = 'https://' + instance + '.service-now.com/api/now/table/incident/' + sysId;
var request = new GlideHTTPRequest(endpoint);

// Add authentication data
request.setBasicAuth(username, password);

// Try to get the non-existent incident
response = request.get();

// Print the results: status code and response body
gs.print(response.getStatusCode());

// Get the last error message
gs.print(response.getErrorMessage());
```

Output

```
404
Method failed: (/api/now/table/incident/0123456789abcdef0123456789abcdef) with code: 404
```

## GlideHTTPResponse - getHeader\(String name\)

Returns the header specified in the passed-in parameter.

|Name|Type|Description|
|----|----|-----------|
|name|String|Name of the response header to return, such as **Content-Type**.|

|Type|Description|
|----|-----------|
|String|Value of the specified header for the current response.|

This example shows how to display the contents of the **Content-Type** header.

```
var instance = 'dev12345'; // Instance name
var username = 'admin';
var password = 'yourpassword';
var sysId = '0123456789abcdef0123456789abcdef';  // Sys_id of the incident to get

// Instantiate request with the ServiceNow API incident table endpoint for deletion of an incident
var endpoint = 'https://' + instance + '.service-now.com/api/now/table/incident/' + sysId;
var request = new GlideHTTPRequest(endpoint);

// Add authentication data
request.setBasicAuth(username, password);

// Execute the GET request
var response = request.get();

// Print the results
gs.print(response.getStatusCode());
gs.print(response.getHeader("Content-Type"));
```

Output

```
200
application/json
```

## GlideHTTPResponse - getHeaders\(\)

Returns all headers associated with the endpoint response.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Object|Object containing all associated headers.|

This example shows how to display all of the headers associated with an endpoint call using the getHeaders\(\) method.

```
var instance = 'dev12345'; // Instance name
var username = 'admin';
var password = 'yourpassword';
var sysId = '0123456789abcdef0123456789abcdef';  // Sys_id of the incident to get

// Instantiate request with the ServiceNow API incident table endpoint for deletion of an incident
var endpoint = 'https://' + instance + '.service-now.com/api/now/table/incident/' + sysId;
var request = new GlideHTTPRequest(endpoint);

// Add authentication data
request.setBasicAuth(username, password);

// Execute the GET request
var response = request.get();

// Print the results
gs.print(response.getStatusCode());
gs.print(response.getHeaders());
```

Output

```
200
{
  Transfer-Encoding=chunked, 
  Strict-Transport-Security=max-age=63072000; includeSubDomains,
  Cache-Control=no-cache, no-store, must-revalidate,
  max-age=-1,
  Server=ServiceNow,
  X-Content-Type-Options=nosniff,
  X-Transaction-ID=399f8f73db13,
  X-Is-Logged-In=true,
  Set-Cookie=BIGipServerpool_jsmith=2643023626.45630.0000; path=/; Httponly; Secure; SameSite=None; Secure,
  Pragma=no-store,no-cache, Expires=0, Date=Tue, 26 Oct 2021 19:40:10 GMT, 
  Content-Type=application/json;charset=UTF-8
}

```

## GlideHTTPResponse - getHttpMethod\(\)

Returns the HTTP method associated with the specified endpoint call.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

HTTP method associated with the endpoint call, such as `org.apache.commons.httpclient.methods.GetMethod@f83e63`. Format: org.apache.commons.httpclient.methods.&lt;Method&gt;

</td></tr></tbody>
</table>This example shows how to display the HTTP method used when calling the associated endpoint using the getMethod\(\) method.

```
var instance = 'dev12345'; // Instance name
var username = 'admin';
var password = 'yourpassword';
var sysId = '0123456789abcdef0123456789abcdef';  // Sys_id of the incident to get

// Instantiate request with the ServiceNow API incident table endpoint for deletion of an incident
var endpoint = 'https://' + instance + '.service-now.com/api/now/table/incident/' + sysId;
var request = new GlideHTTPRequest(endpoint);

// Add authentication data
request.setBasicAuth(username, password);

// Execute the GET request
var response = request.get();

// Print the results
gs.print(response.getStatusCode());
gs.print(response.getHttpMethod());
```

Output

```
200
org.apache.commons.httpclient.methods.GetMethod@f83e63
```

## GlideHTTPResponse - getStatusCode\(\)

Returns the last status code for an endpoint call.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|int|HTTP response status code.|

This example shows how to get the status code of a REST call after it executes using the getStatusCode\(\) method.

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

// Print the results: status code
gs.print(response.getStatusCode());
```

Output:

```
200
```

## GlideHTTPResponse - haveError\(\)

Returns a flag that indicates whether there were any errors while processing the endpoint call.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_zpm_g52_dfb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether there were any errors when processing the endpoint call.Valid values:

-   true: Error occurred during the processing of the endpoint.
-   false: No errors during the processing of the endpoint.

Returns true if an error has occurred, or false if there are no errors

</td></tr></tbody>
</table>This example shows how no error is flagged when the sys\_id for an incident is valid using the haveError\(\) method.

```
var instance = 'dev12345';
var username = 'admin';
var password = 'yourpassword';

// Valid sys_id of an incident record
var sysId = 'a85f82ffdb5f30103dd9c39d13961916';  // Sys_id of the incident to get

// Instantiate request with the ServiceNow API incident table endpoint for deletion of an incident
var endpoint = 'https://' + instance + '.service-now.com/api/now/table/incident/' + sysId;
var request = new GlideHTTPRequest(endpoint);

// Add authentication data
request.setBasicAuth(username, password);

// Execute the GET request
var response = request.get();

// Print the results
gs.print(response.getStatusCode());
gs.print(response.haveError());
```

Output

```
200
false
```

This example shows how an error is flagged when the sys\_id for an incident is not valid \(not found\) using the haveError\(\) method.

```
var instance = 'dev12345';
var username = 'admin';
var password = 'yourpassword';

// Invalid sys_id
var sysId = 'a85f82ffdb5f30103dd9c39d13961832';  // Sys_id of the incident to get

// Instantiate request with the ServiceNow API incident table endpoint for deletion of an incident
var endpoint = 'https://' + instance + '.service-now.com/api/now/table/incident/' + sysId;
var request = new GlideHTTPRequest(endpoint);

// Add authentication data
request.setBasicAuth(username, password);

// Execute the GET request
var response = request.get();

// Print the results
gs.print(response.getStatusCode());
gs.print(response.haveError());
```

Output

```
404
true
```

