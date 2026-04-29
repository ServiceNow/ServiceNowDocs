---
title: OpenAPI support in the REST step
description: Populate REST step fields and action inputs with information imported from an OpenAPI Specification. Import specifications by providing a URL to the YAML or JSON, or copying and pasting content.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Integration steps, Build integrations, Integration Hub, Workflow Data Fabric]
---

# OpenAPI support in the REST step

Populate REST step fields and action inputs with information imported from an OpenAPI Specification. Import specifications by providing a URL to the YAML or JSON, or copying and pasting content.

## Benefits

OpenAPI support in the REST step offers these benefits.

-   Use information imported from an OpenAPI Specification to configure REST step operations, HTTP methods, parameters, request body, path, and headers.
-   Review available API operations without leaving the Flow Designer interface.
-   Generate inputs required for the REST step to send valid requests to an OpenAPI service and add them to the REST step in the correct location.

**Note:** Always review REST step values imported from an OpenAPI Specification before sending a request. Remove parameters, headers, and inputs that the API does not require.

## Generated inputs

When you import an OpenAPI Specification, the system creates any required inputs and adds them to the REST step form where appropriate. At runtime, the system sends a REST request that contains input values provided to the action. For example, if an API requires a name parameter passed in the request, the system creates a **name** input and adds it to the REST step. When you add the action to the flow, name becomes an input to the action.

The system maps OpenAPI data types to Workflow Studio data types. For example, if the OpenAPI Specification requires a user object, then the system creates a complex data object as input. For more information, see [Complex data](https://www.servicenow.com/docs/access?context=complex-data&version=australia&pubname=australia-build-workflows&ft:locale=en-US).

## Specification size limit

By default, the system can import OpenAPI Specifications up to 10 MB. To increase the import size, update the **glide.rest.openapi.max\_request\_size** system property. The maximum value is 100 MB.

## Specification management

Import an OpenAPI Specification by selecting options in the REST step. For more information, see [REST step](../../flow-designer/reference/rest-request-action-designer.md). Importing an OpenAPI Specification creates a record in the OpenAPIs \[sys\_openapi\] table. You can view or delete specification records directly from this table. To update a specification, delete it and import it again.

## Design considerations

Create a REST step from an OpenAPI Specification with these considerations in mind.

-   **Remove unnecessary REST step parameters**

    When importing an OpenAPI Specification, the system adds all parameters and headers present in the specification to the REST step. Review the final REST step values and remove parameters you do not want to send in the request. For example, if the API accepts content type headers for both JSON and XML, the system adds both headers to the REST step. Remove one of the headers depending on the content type you want to receive in the response.

-   **Make input labels user-friendly**

    Ensure that input labels required for the REST step are clear and understandable. Clear labels enable flow designers to easily understand the required inputs when using the action in a flow.

-   **Remove inputs that do not require flow designer configuration**

    When importing an OpenAPI Specification, the system adds all inputs present in the specification to the action input section. Remove any inputs that do not require a flow designer to configure. For example, if a REST step variable receives a value from another step in the action, an action input is not required.

-   **Avoid changing the API operation**

    Changing the value of the **API Operation** field removes all values dependent on that operation. If you configure the OpenAPI Specification values in the REST step form, then change the operation, the system does not save your configuration. Values that are entered manually by a user are not affected.


## Limitations

Create a REST step from an OpenAPI Specification with these limitations.

-   **Request body media types**

    The request body only supports JSON and XML-based media types. If the selected operation from the imported OpenAPI Specification contains a request body with a different media type, the system adds a data pill of type String to the **Request body** field.

-   **OpenAPI 3.0 components**

    OpenAPI 3.0 adds new components to Swagger 2.0 to describe an API in further detail. OpenAPI support in the REST step supports some, but not all of these components. The REST step does not currently support these components.

    -   Schema Object: oneOf, anyOf properties
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


