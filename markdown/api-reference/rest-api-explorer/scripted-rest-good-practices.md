---
title: Scripted REST APIs good practices
description: Follow these guidelines when designing and implementing scripted REST APIs.
locale: en-US
release: xanadu
product: REST API Explorer
classification: rest-api-explorer
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Scripted REST APIs, REST APIs, Web services, API implementation, API implementation and reference]
---

# Scripted REST APIs good practices

Follow these guidelines when designing and implementing scripted REST APIs.

## Follow REST API conventions

Use REST API standards to provide a consistent and easy to use interface for clients. REST API conventions define specific behavior for each type of method. Use the following guidelines as a starting point for designing your API.

-   **GET** operations only query data. A GET request should never modify data.
-   **POST** operations create new records but do not modify existing records.
-   **PUT** and **PATCH** operations modify existing records.
-   **DELETE** operations destroy records.

## Use versioning to control changes to your API

Use versioning to implement new functionality and avoid breaking existing integrations. When you introduce significant functionality changes to your API, create a new version of the API first. Do not introduce behavior that will break existing integrations in a published version.

Using versioning allows you to implement significant changes to your API without breaking existing clients. You can then release the new version of the API for new clients while allowing existing clients to upgrade at their own pace.

Encourage clients to use a version-specific API, or configure the API without a default version to force clients to specify a version. You can also make new, optional behavior available by adding an optional parameter to an existing version.

## Return an informative HTTP status code

Return a status code that informs the requestor of the success or failure of the request. Return an HTTP status code that helps the client understand the result of the request. Use the following guidelines for common status codes.

|Status code|Description|
|-----------|-----------|
|200|Indicates that the request was completed successfully.|
|201|Indicates that a record was created successfully.|
|204|Indicates that a record was deleted successfully.|
|40X \(401, 404\)|Status codes in the 400 range indicate a client error, such as 400 for invalid request syntax.|
|50X \(500, 503\)|Status codes in the 500 range indicate that a server error occurred. The client request may have been valid or invalid, but a problem occurred on the server that prevented it from processing the request.|

## Return useful error information

Provide the client with enough information in error messages to allow them to understand the problem without having to refer to your API documentation. An error response should include a helpful error message, as well as an error status code.

For example, when a client queries a record that does not exist, you can return the error message "The specified record does not exist. Ensure that a record with the ID of &lt;id value&gt; exists in the application." along with a 404 status code.

The scripted REST API feature includes several preconfigured error objects you can use for commonly-encountered errors, and a customizable ServiceRequest error object you can use when the preconfigured error objects do not meet your needs.

## Enforce and test access controls

Enforce existing access controls and require additional access to modify data. In addition to requiring authentication to access the API, require authorization to access data. Use the GlideRecordSecure API in your scripted REST API scripts. This API ensures that access controls defined on the underlying data are applied for the requesting user.

Require additional access controls for operations that modify data. Requests such as PUT, POST, and DELETE should require a higher level of access than GET. Configure these API resources to require a more strict ACL.

Test your access controls, both authentication and authorization, before releasing the API.

## Build tests to verify functionality

Build tests that verify your scripted REST web services functionality as part of your development process. Use repeatable tests to ensure that your API functions the way you expect it to. Testing also helps ensure that changes you make do not affect the expected API behavior after you release a version. You can use a REST client application that supports automated testing, such as Postman, to facilitate testing.

Tests should validate the response code, headers, and body content as appropriate for each resource you implement. You can also use tests to validate authentication requirements, and to confirm that errors return useful responses.

**Parent Topic:**[Scripted REST APIs](../../../../integrate/custom-web-services/concept/c_CustomWebServices.md)

