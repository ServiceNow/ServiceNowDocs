---
title: Scripted REST APIs
description: The scripted REST API feature allows application developers to build custom web service APIs.
locale: en-US
release: australia
product: REST API Explorer
classification: rest-api-explorer
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [REST APIs, Web services, API implementation, API implementation and reference]
---

# Scripted REST APIs

The scripted REST API feature allows application developers to build custom web service APIs.

You can define service endpoints, query parameters, schemas,and headers for a scripted REST API, as well as scripts to manage the request and response.

Scripted REST APIs generally follow the REST architecture, but you can customize them to use different conventions. You define scripted REST APIs using the Scripted REST Service form found under **Scripted Web Services** → **Scripted REST APIs**.

![Scripted REST service form](../image/scripted-REST-service-form-new.png "Scripted REST Service form")

The following videos offer additional information about scripted REST APIs:

-   [Scripted REST APIs – Design](https://www.youtube.com/watch?v=Tw70sHgDc-w)
-   [Scripted REST APIs – Implementation](https://www.youtube.com/watch?v=LFHV-Qk1-Yk)

## Scripted REST API URIs

Scripted REST API URIs have the following format:

`https://<instance.service-now.com>/api/<name_space>/<version>/<api_id>/<relative_path>`

In this URI:

-   **&lt;instance.service-now.com&gt;**: Path to the ServiceNow instance where users access the scripted REST API.
-   **&lt;name\_space&gt;**: For web services in the global scope, the name space is the value of the property **glide.appcreator.company.code**. For web services in a scoped application, the name space is the scope name, such as x\_company\_appname. For additional information on name spaces, see Application scope.
-   **&lt;version&gt;**: Optional. Version of the endpoint to access if the API uses versioning, such as **v1**. You can access the default version of a versioned API by specifying the URI without a version number.
-   **&lt;api\_id&gt;**: Value of the **API ID** field on the Scripted REST Service form. By default this value is based on the service name.
-   **&lt;relative\_path&gt;**: Relative path defined for the resource in the Scripted REST Service form. Specifying a relative resource path allows you to have multiple resources using the same HTTP method, such as GET, in one web service. For example, a resource may specify the path `/{id}` when the web service has only one GET resource, or `/user/{id}` and `/message/{id}` when the web service has different resources for requesting user and message records.

## Scripted REST API versioning

Scripted REST API URIs may include a version number, such as `/api/management/v1/table/{tableName}`. Version numbers identify the endpoint version that a URI accesses. By specifying a version number in your URIs, you can test and deploy changes without impacting existing integrations.

## Default API version

A version may be marked as default. Specifying a default version allows users to access that version using a scripted REST endpoint without a version number. If no version is marked as default, the latest version is used as the default.

## Scripted REST API resources

A scripted REST API resource is equivalent to a REST endpoint. It defines the HTTP method to execute, the processing script, and any override settings from the parent API. You can define one ore more resources per API.

## Scripted REST API query parameters

Query parameters define values that requesting users can pass in a request. When creating a scripted REST API, you can specify which parameters are available and which are mandatory for each request. You can also associate a query parameter with multiple resources.

Access request parameters in scripts using the request object queryParams field.

## Scripted REST schemas

Schemas define a structure that can be used for API requests and responses, including data type, expected fields, and formats. You can define multiple schemas within a scripted REST API, which can be used to specify request and response contents of the resources within that API.

Schemas must be defined using [OpenAPI version 3.0.1 format](https://spec.openapis.org/oas/v3.0.1.html).

## Scripted REST API roles

To work with scripted REST APIs, you must have the web service administrator \[web\_service\_admin\] role. Users with this role can read, create, modify, and delete scripted REST APIs and web service resources.

**Note:** These roles are not required to access a scripted REST API endpoint.

## Request and response formats

By default, all resources in an API support the following request and response formats: application/json, application/xml, and text/xml. You can overrride the default formats at the API level. The new formats apply to all resources belonging to the API, unless an individual resource overrides the defaults.

## Scripted REST API security

You can configure your scripted REST APIs with the necessary level of security. From public APIs/endpoints that don't require any security to highly secure APIs/endpoints that require user authentication with tight access control to all resources.

Use the API access policy feature to control the authentication method for the APIs. For more information, see API access policy.

## Scripted REST API access controls

Access control lists \(ACLs\) define criteria, such as the roles needed and conditions that a user must meet to access a scripted REST API or endpoint. A requesting user must satisfy at least one of the ACLs. It is not necessary to satisfy all selected ACLs. You can define a single ACL for an entire REST API or for an individual endpoint.

When defining a scripted REST API ACL, it must have the **Type** value **REST\_Endpoint**.

For additional information on ACLs, see Access control list rules and [Configure a scripted REST API resource to require an ACL](../task/t_WbSvcOpRqACL.md).

## Scripted REST API security matrix

There are multiple possible security configurations for scripted REST APIs. Use this table to identify the scripted REST API security configuration that best suits your needs, and the field values to implement that configuration.

|Configuration|Scripted REST API|Scripted REST Resource|
| |Default ACLs|Requires authentication|Requires ACL authorization|ACLs|
|-------------|-----------------|----------------------|
|---|------------|-----------------------|--------------------------|----|
|The resource is public. No authentication or ACL is required.|Any value|False|Any value|Any value|
|The resource requires basic authentication only. No ACL is required.|Any value|True|False|Any value|
|The resource requires basic authentication only. ACL is required.|No ACL selected|True|True|No ACL selected|
|An ACL selected in the resource record is required.|Any value|True|True|One or more ACLs selected|
|An ACL selected in the scripted REST API record is required.|One or more ACLs selected|True|True|No ACL selected|

## Scripted REST API error objects

Scripted REST APIs include error objects that allow you to respond to a request with a standard HTTP error message when an error occurs during request processing. You can use error objects in scripted REST API resources to alert requesting clients of errors. Use error objects to respond to incoming requests, not to catch errors within your server-side code.

## Error response format

The content type of the response depends on the request Accept header. If the Accept header specifies an unsupported format, such as image/jpeg, the error response uses JSON.

Error responses follow this format:

```
{
  "error": {
    "message": "My error message",
    "detail": "My details"  
  },  
  "status": "failure"
}
```

The numeric status code, such as 404, is included in the response Status code header, not in the response body.

## Automated Test Framework support

The Automated Test Framework \(ATF\) supports Inbound REST test steps. You can create automated tests for custom Inbound REST APIs that you create. Creating tests for your custom REST APIs simplifies upgrade testing, and makes it possible to verify that modifications to a REST API are backward compatible. See Administering REST test step configurations and ATF REST test step configurations.

## Developer training

In the ServiceNow® Developer Site, you can find training for [Scripted REST APIs](https://developer.servicenow.com/app.do#!/training/article/app_store_learnv2_rest_paris_scripted_rest_apis/app_store_learnv2_rest_paris_scripted_rest_api_objectives?v=paris).

-   **[Create a scripted REST API](../task/t_CreateAScriptedRESTService.md)**  
Create a scripted REST API to define web service endpoints.
-   **[Scripted REST APIs good practices](../../../app-store/good_practices/scripted-rest/concept/scripted-rest-good-practices.md)**  
Follow these guidelines when designing and implementing scripted REST APIs.
-   **[Scripted REST API examples](c_ScriptedRESTAPIExamples.md)**  
Mutliple examples are available demonstrating how to create and use scripted REST APIs.

**Parent Topic:**[REST APIs](../../inbound-rest/concept/c_RESTAPI.md)

