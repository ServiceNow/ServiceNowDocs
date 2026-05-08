---
title: OpenAPI/Postman step
description: Import the OpenAPI specification or a Postman collection of a third-party outbound REST web service and build an integration to the web service. The request details for the underlying REST API operation are derived from the OpenAPI specification or Postman collection.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Integration steps, Build integrations, Integration Hub, Workflow Data Fabric]
---

# OpenAPI/Postman step

Import the OpenAPI specification or a Postman collection of a third-party outbound REST web service and build an integration to the web service. The request details for the underlying REST API operation are derived from the OpenAPI specification or Postman collection.

For JSON output response body, the system creates a complex data object output from the OpenAPI specification or [Postman collection](https://learning.postman.com/docs/collections/collections-overview/).

**Note:** OpenAPI/Postman step is not available in the base system and requires the ServiceNow® Integration Hub subscription. After the required plugin is activated, the step is visible under Integrations.

## Roles and availability

Available as an Action Designer action step. Users with the action\_designer and open\_api\_admin, or admin roles can create a custom action with one or more action steps.

## Fields

<table id="table_z5z_y5t_txb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Connection Alias

</td><td>

Connection &amp; Credential alias record that the system uses to run the action step. Users with the action\_designer and connection\_admin, or admin roles can select an associated Connection alias record. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using an action in multiple environments. Likewise, if the connection information changes, you don't need to update your custom action. To learn more about connections and credentials, see credentials, connections, and aliases.

</td></tr><tr><td>

Base URL

</td><td>

Base URL from the Connection Alias for the REST request.

</td></tr><tr><td>

Toggle Advanced View

</td><td>

Option to view or hide the request details. When enabled, you can view and configure the resource path, HTTP method, query parameters, headers, and action outputs of the request.

</td></tr><tr><td>

API Source

</td><td>

Option to select an API from the list of available imported APIs.

</td></tr><tr><td>

Import Spec

</td><td>

Option that allows you to import an OpenAPI \(v2.0 or v3.0\) specification or a Postman collection \(version 2.0.0 or 2.1.0\). You can import an OpenAPI specification or Postman collection by providing a URL and credentials to the specification or collection, or manually copying and pasting JSON content.

</td></tr><tr><td>

API Operation

</td><td>

Option to select an operation from the list. Available operations are provided by the OpenAPI Specification or Postman collection in the **API Source** field.

</td></tr><tr><td>

Save As Attachment

</td><td>

Option to specify whether to save the response as a record in the Attachment \[sys\_attachment\] table.

</td></tr><tr><td>

Resource Path

</td><td>

Path for the resource.

</td></tr><tr><td>

HTTP Method

</td><td>

HTTP method used to process the request.-   **GET**
-   **POST**
-   **PUT**
-   **PATCH**
-   **DELETE**

</td></tr><tr><td>

Query Parameters

</td><td>

Name-value pairs to pass to the REST endpoint. You can create these parameters manually, or drag input variables into the parameter fields, and then assign a value.

 Support REST step requests that contain duplicate query parameter names. If you create a REST request that contains duplicate query parameter names, Workflow Studio adds the query parameters to the request in the same order as you defined them.

 **Note:** When importing an OpenAPI Specification, the system adds all parameters and headers present in the specification to the REST step. Review the final REST step values and remove parameters you do not want to send in the request. For example, if the API accepts content type headers for both JSON and XML, the system adds both headers to the REST step. Remove one of the headers depending on the content type you want to receive in the response.

</td></tr><tr><td>

Headers

</td><td>

Headers to send with the request. You can create headers manually, or drag input variables into the parameter fields, and then assign a value.

 Support REST step requests that contain duplicate request headers. If you create a REST request that contains duplicate request headers, the headers are sent in the same order as you defined them.

 **Note:** When importing an OpenAPI Specification, the system adds all parameters and headers present in the specification to the REST step. Review the final REST step values and remove parameters you do not want to send in the request. For example, if the API accepts content type headers for both JSON and XML, the system adds both headers to the REST step. Remove one of the headers depending on the content type you want to receive in the response.

</td></tr><tr><td>

Attachment

</td><td>

Attachment record that contains the request. You can look up or create this record in a prior step and define it as an input variable. Create it by using the JSONStreamingBuilder and XMLStreamingBuilder APIs in the Script step. **Note:** This field is available when you select **Binary** from the Request Type list.

</td></tr><tr><td>

Enable Retry Policy

</td><td>

Option to enable the retry policy. For more information, see Retry policy.

</td></tr><tr><td>

Override Default Policy for Alias

</td><td>

Option to override the default retry policy. This check box is not applicable when **Define Connection Inline** is selected from the Connection list.

</td></tr><tr><td>

Retry Policy

</td><td>

Default retry policy associated with **Connection Alias**. If **Override Default Policy for Alias** is selected, you can override the default retry policy and select another existing retry policy based on your requirement.

</td></tr></tbody>
</table>## Action error evaluation

-   **If this step fails**

    Data type: **Choice**

    Option to continue running the next step or go to error evaluation. To use the step status code or message for a custom action error condition, see Action error evaluation.


![Demonstrates on how to import a Postman collection into an OpenAPI/Postman step](../images/openapi-postman-step-example.gif)

## Action error evaluation

-   **If this step fails**

    Data type: **Choice**

    Option to continue running the next step or go to error evaluation. To use the step status code or message for a custom action error condition, see Action error evaluation.


## Known limitations

Create a OpenAPI step from an OpenAPI Specification with these limitations.

-   **Request body media types**

    The request body only supports JSON media types.

    **Note:** A string type output object is created when the OpenAPI schema has additionalProperties or no properties.

-   **OpenAPI 3.0 components**

    OpenAPI 3.0 adds new components to Swagger 2.0 to describe an API in further detail. OpenAPI support in the OpenAPI step supports some, but not all of these components. The OpenAPI step does not currently support these components.

    -   Schema Object: additionalProperties properties
    -   Discriminator Object
    -   Info object: termsOfService, contact, license fields
    -   Example Object
    -   Link Object
    -   Callback Object
    -   Security Scheme Object
    -   Security Requirements Object
    -   Tag Object
    -   External Documentation Object
    -   Server Object
    -   Specification extensions
    -   Recursive references
    More information on these components is available in the OpenAPI documentation. See [OpenAPI Specification](https://swagger.io/specification/).

-   **Maximum number of operations supported**

    The number of API operations is limited to 500 by default. However, using the system property **glide.rest.openapi.max\_operation\_limit**, you can configure the number of operations from 1 through 1000.


