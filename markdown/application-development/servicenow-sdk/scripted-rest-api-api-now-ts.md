---
title: Scripted REST API - ServiceNow Fluent
description: The Scripted REST API defines the endpoints, query parameters, and headers for a scripted REST service \[sys\_ws\_definition\].Create a scripted REST API \[sys\_ws\_definition\] to define web service endpoints.Create a scripted REST resource \[sys\_ws\_operation\] to define the HTTP method, the processing script, and to override settings from the parent service.Create query parameters \[sys\_ws\_query\_parameter\] and headers \[sys\_ws\_header\] for routes in a scripted REST API. Query parameters control what values a requesting user can pass in the request URI. Headers specify what the API accepts and can respond with.Create versions for a scripted REST API \[sys\_ws\_version\] to define web service endpoints.
locale: en-US
release: australia
product: ServiceNow SDK
classification: servicenow-sdk
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 11
breadcrumb: [ServiceNow Fluent API reference, Reference, ServiceNow SDK, Building applications in source code, Building pro-code applications, Developing your application, Building applications]
---

# Scripted REST API - ServiceNow Fluent

The Scripted REST API defines the endpoints, query parameters, and headers for a scripted REST service \[sys\_ws\_definition\].

**Note:** For the latest ServiceNow Fluent API documentation and examples, see the [ServiceNow Fluent API reference](https://servicenow.github.io/sdk/) and [ServiceNow SDK examples repository](https://github.com/ServiceNow/sdk-examples) on GitHub.

For general information about scripted REST services, see [Scripted REST APIs](https://www.servicenow.com/docs/access?context=c_CustomWebServices&version=australia&pubname=australia-api-reference&ft:locale=en-US).

**Parent Topic:**[ServiceNow Fluent API reference](servicenow-fluent-api-reference.md)

**Related topics**  


[ServiceNow Fluent](../concept/servicenow-fluent.md)

## RestApi object

Create a scripted REST API \[sys\_ws\_definition\] to define web service endpoints.

<table id="table_vy2_525_jq" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

$id

</td><td>

String or Number

</td><td>

Required. A unique ID for the metadata object. When you build the application, this ID is hashed into a unique sys\_id. For more information, see [ServiceNow Fluent language constructs](fluent-constructs.md).Format: `Now.ID['String' or Number]`

</td></tr><tr><td>

name

</td><td>

String

</td><td>

Required. The name of the API, which is used in the API documentation.

</td></tr><tr><td>

serviceId

</td><td>

String

</td><td>

Required. The API identifier used to distinguish this API in URI paths. It must be unique within the API namespace.

</td></tr><tr><td>

active

</td><td>

Boolean

</td><td>

Flag that indicates whether the API can serve requests.Valid values:

-   true: The API can serve requests.
-   false: The API can't serve requests.

Default: true

</td></tr><tr><td>

shortDescription

</td><td>

String

</td><td>

A brief description of the API, which is used in the API documentation.

</td></tr><tr><td>

consumes

</td><td>

String

</td><td>

A list of media types that resources of the API can consume.Default: application/json,application/xml,text/xml

</td></tr><tr><td>

docLink

</td><td>

String

</td><td>

A URL that links to static documentation about the API.

</td></tr><tr><td>

enforceAcl

</td><td>

Array

</td><td>

A list of variable identifiers of ACL objects or sys\_ids of ACLs to enforce when accessing resources \[sys\_security\_acl\]. For more information, see [Access Control List API - ServiceNow Fluent](acl-api-now-ts.md#).To not enforce ACLs, set this property to an empty array \(`[]`\).

Default: Scripted REST External Default

</td></tr><tr><td>

produces

</td><td>

String

</td><td>

A list of media types that resources of the API can produce.Default: application/json,application/xml,text/xml

</td></tr><tr><td>

routes

</td><td>

Array

</td><td>

The resources \[sys\_ws\_operation\] for the API. For more information, see [routes object](scripted-rest-api-api-now-ts.md#).

</td></tr><tr><td>

policy

</td><td>

String

</td><td>

The policy for how application files are protected when downloaded or installed.Valid values:

-   read: Files are viewable only.
-   protected: Users with password permissions can edit the files.

</td></tr><tr><td>

versions

</td><td>

Array

</td><td>

A list of versions \[sys\_ws\_version\] for the API. For more information, see [versions object](scripted-rest-api-api-now-ts.md#).Specifying versions allows you to manage different versions of an API and their statuses, such as whether they are active, the default version, or deprecated.

</td></tr><tr><td>

$meta

</td><td>

Object

</td><td>

Metadata for the application metadata.With the installMethod property, you can map the application metadata to an output directory that loads only in specific circumstances.

```javascript
$meta: {
      installMethod: 'String'
}
```

Valid values for installMethod:

-   demo: Outputs the application metadata to the `metadata/unload.demo` directory to be installed with the application when the **Load demo data** option is selected.
-   first install: Outputs the application metadata to the `metadata/unload` directory to be installed only the first time an application is installed on an instance.

</td></tr></tbody>
</table>```javascript
import { RestApi } from '@servicenow/sdk/core'
import { process } from '../server/handler.js'

RestApi({
    $id: Now.ID['rest1'],
    name: 'customAPI',
    serviceId: 'custom_api',
    consumes: 'application/json',
    routes: [
        {
            $id: Now.ID['route1'],
            path: '/home/{id}',
            script: process,
            parameters: [{ $id: Now.ID['param1'],  name: 'n_param' }],
            headers: [{ $id: Now.ID['header1'],  name: 'n_token' }],
            enforceAcl: [acl],
            version: 1,
        },
    ],
    enforceAcl: [acl],
    versions: [
        {
            $id: Now.ID['v1'],
            version: 1,
        },
    ],
})

```

The ACL referenced is defined using the ACL object:

```javascript
import { Acl } from "@servicenow/sdk/core";

const acl = Acl({
    name: 'My random ACL',
    type: 'rest_endpoint',
    script: `answer = (Math.random() > 0.5)`,
    active: true,
    adminOverrides: false,
    operations: ['execute'],
})
```

## routes object

Create a scripted REST resource \[sys\_ws\_operation\] to define the HTTP method, the processing script, and to override settings from the parent service.

Use the routes object within the RestApi object.

<table id="table_vy2_525_jq" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

$id

</td><td>

String or Number

</td><td>

Required. A unique ID for the metadata object. When you build the application, this ID is hashed into a unique sys\_id. For more information, see [ServiceNow Fluent language constructs](fluent-constructs.md).Format: `Now.ID['String' or Number]`

</td></tr><tr><td>

name

</td><td>

String

</td><td>

The name of the API resource, which is used in the API documentation.Default: the value of the path property

</td></tr><tr><td>

script

</td><td>

Script

</td><td>

Required. The custom script defines how the operation parses and responds to requests. This property supports a function from a JavaScript module, a reference to another file in the application that contains a script, or inline JavaScript.Format:

-   For functions, use the name of a function, function expression, or default function exported from a JavaScript module and import it into the `.now.ts` file. For information about JavaScript modules, see [JavaScript modules and third-party libraries](../concept/javascript-modules-third-party-libraries.md).
-   To use text content from another file, refer to a file in the application using the following format: `Now.include('path/to/file')`. For more information, see [ServiceNow Fluent language constructs](fluent-constructs.md).
-   To provide an inline script, use string literals or template literals for multiple lines of code: `'Script' or `Script``.

</td></tr><tr><td>

parameters

</td><td>

Array

</td><td>

A list of query parameters \[sys\_ws\_query\_parameter\] for the route. For more information, see [parameters and headers objects](scripted-rest-api-api-now-ts.md#).

</td></tr><tr><td>

headers

</td><td>

Array

</td><td>

A list of headers \[sys\_ws\_header\] for the route. For more information, see [parameters and headers objects](scripted-rest-api-api-now-ts.md#).

</td></tr><tr><td>

active

</td><td>

Boolean

</td><td>

Flag that indicates whether the resource is used.Valid values:

-   true: The resource is used.
-   false: The resource isn't used.

Default: true

</td></tr><tr><td>

path

</td><td>

String

</td><td>

The path of the resource relative to the base API path. The relative URI can contain path parameters such as `'/abc/{id}'`.Default: /

</td></tr><tr><td>

shortDescription

</td><td>

String

</td><td>

A brief description of the resource, which is used in the API documentation.

</td></tr><tr><td>

consumes

</td><td>

String

</td><td>

A list of media types that the resource can consume.This property can be overridden with the PUT, PATCH, or POST methods.

Default: The value of the consumes property in the RestApi object

</td></tr><tr><td>

enforceAcl

</td><td>

Array

</td><td>

A list of variable identifiers of ACL objects or sys\_ids of ACLs to enforce when accessing resources \[sys\_security\_acl\]. For more information, see [Access Control List API - ServiceNow Fluent](acl-api-now-ts.md#).To not enforce ACLs, set this property to an empty array \(`[]`\).

Default: Scripted REST External Default

</td></tr><tr><td>

produces

</td><td>

String

</td><td>

A list of media types that the resource can produce.Default: The value of the produces property in the RestApi object

</td></tr><tr><td>

requestExample

</td><td>

String

</td><td>

A valid sample request body payload for the resource, which is used in the API documentation.

</td></tr><tr><td>

method

</td><td>

String

</td><td>

The HTTP method that the resource implements.Valid values: GET, POST, PUT, PATCH, DELETE

Default: GET

</td></tr><tr><td>

authorization

</td><td>

Boolean

</td><td>

Flag that indicates whether users must be authenticated to access the resource.Valid values:

-   true: Users must be authenticated to access the resource.
-   false: Authentication isn't required to access the resource.

Default: true

</td></tr><tr><td>

authentication

</td><td>

Boolean

</td><td>

Flag that indicates whether ACLs are enforced when accessing the resource.Valid values:

-   true: ACLs are enforced when accessing the resource.
-   false: ACLs aren't enforced when accessing the resource.

Default: true

</td></tr><tr><td>

internalRole

</td><td>

Boolean

</td><td>

Flag that indicates whether the route requires the snc\_internal role.This property is supported only if the Explicit Roles plugin \(com.glide.explicit\_roles\) is enabled.

Valid values:

-   true: The route requires the snc\_internal role.
-   false: The route doesn't require the snc\_internal role.

Default: true

</td></tr><tr><td>

policy

</td><td>

String

</td><td>

The policy for how application files are protected when downloaded or installed.Valid values:

-   read: Files are viewable only.
-   protected: Users with password permissions can edit the files.

</td></tr><tr><td>

version

</td><td>

Number

</td><td>

The version of the API.This property is required if the versions property is used in the RestApi object.

The version specified with this property is used to automatically generate a URI with a version, such as `/api/management/v1/table/{tableName}`. Version numbers identify the endpoint version that a URI accesses. By specifying a version number, you can test and deploy changes without impacting existing integrations.

</td></tr><tr><td>

$meta

</td><td>

Object

</td><td>

Metadata for the application metadata.With the installMethod property, you can map the application metadata to an output directory that loads only in specific circumstances.

```javascript
$meta: {
      installMethod: 'String'
}
```

Valid values for installMethod:

-   demo: Outputs the application metadata to the `metadata/unload.demo` directory to be installed with the application when the **Load demo data** option is selected.
-   first install: Outputs the application metadata to the `metadata/unload` directory to be installed only the first time an application is installed on an instance.

</td></tr></tbody>
</table>```javascript
routes: [
   {
      $id: Now.ID['route1'],
      path: '/home/{id}',
      script: process,
      parameters: [{ $id: Now.ID['param1'],  name: 'n_param' }],
      headers: [{ $id: Now.ID['header1'],  name: 'n_token' }],
      enforceAcl: [acl],
      version: 1,
   },
],
```

### parameters and headers objects

Create query parameters \[sys\_ws\_query\_parameter\] and headers \[sys\_ws\_header\] for routes in a scripted REST API. Query parameters control what values a requesting user can pass in the request URI. Headers specify what the API accepts and can respond with.

Use the parameters and headers objects within the routes object.

<table id="table_vy2_525_jq" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

$id

</td><td>

String or Number

</td><td>

Required. A unique ID for the metadata object. When you build the application, this ID is hashed into a unique sys\_id. For more information, see [ServiceNow Fluent language constructs](fluent-constructs.md).Format: `Now.ID['String' or Number]`

</td></tr><tr><td>

name

</td><td>

String

</td><td>

Required. The name of the parameter or header, which is used in the API documentation.

</td></tr><tr><td>

required

</td><td>

Boolean

</td><td>

Flag that indicates whether the parameter or header is required.Valid values:

-   true: The parameter or header is required.
-   false: The parameter or header isn't required.

Default: false

</td></tr><tr><td>

exampleValue

</td><td>

String

</td><td>

An example of a valid value for the parameter or header, which is used in the API documentation.

</td></tr><tr><td>

shortDescription

</td><td>

String

</td><td>

A brief description of the parameter or header, which is used in the API documentation.

</td></tr><tr><td>

$meta

</td><td>

Object

</td><td>

Metadata for the application metadata.With the installMethod property, you can map the application metadata to an output directory that loads only in specific circumstances.

```javascript
$meta: {
      installMethod: 'String'
}
```

Valid values for installMethod:

-   demo: Outputs the application metadata to the `metadata/unload.demo` directory to be installed with the application when the **Load demo data** option is selected.
-   first install: Outputs the application metadata to the `metadata/unload` directory to be installed only the first time an application is installed on an instance.

</td></tr></tbody>
</table>```javascript
parameters: [{ $id: Now.ID['param1'],  name: 'n_param' }],
headers: [{ $id: Now.ID['header1'],  name: 'n_token' }],
```

## versions object

Create versions for a scripted REST API \[sys\_ws\_version\] to define web service endpoints.

Use the versions object within the RestApi object.

<table id="table_vy2_525_jq" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

$id

</td><td>

String or Number

</td><td>

Required. A unique ID for the metadata object. When you build the application, this ID is hashed into a unique sys\_id. For more information, see [ServiceNow Fluent language constructs](fluent-constructs.md).Format: `Now.ID['String' or Number]`

</td></tr><tr><td>

version

</td><td>

Number

</td><td>

Required. A version of the REST API.

</td></tr><tr><td>

active

</td><td>

Boolean

</td><td>

Flag that indicates whether the version of the REST API can serve requests.Valid values:

-   true: The version of the API can serve requests.
-   false: The version of the API can't serve requests.

Default: true

</td></tr><tr><td>

deprecated

</td><td>

Boolean

</td><td>

Flag that indicates whether the version of the REST API is deprecated. Resources belonging to deprecated versions can serve requests, but are identified as deprecated in documentation.Valid values:

-   true: The version of the API is identified as deprecated.
-   false: The version of the API isn't identified as deprecated.

Default: false

</td></tr><tr><td>

shortDescription

</td><td>

String

</td><td>

A brief description of the version of the REST API, which appears in the API documentation.

</td></tr><tr><td>

isDefault

</td><td>

Boolean

</td><td>

Flag that indicates whether the version of the REST API is the default version. Clients can access the default version using either the versioned or non-versioned URI path.Valid values:

-   true: The version of the API is the default version.
-   false: The version of the API isn't the default version.

Default: false

</td></tr><tr><td>

$meta

</td><td>

Object

</td><td>

Metadata for the application metadata.With the installMethod property, you can map the application metadata to an output directory that loads only in specific circumstances.

```javascript
$meta: {
      installMethod: 'String'
}
```

Valid values for installMethod:

-   demo: Outputs the application metadata to the `metadata/unload.demo` directory to be installed with the application when the **Load demo data** option is selected.
-   first install: Outputs the application metadata to the `metadata/unload` directory to be installed only the first time an application is installed on an instance.

</td></tr></tbody>
</table>```javascript
versions: [
 {
   $id: Now.ID['v1'],
   version: 1,
 },
],
```

