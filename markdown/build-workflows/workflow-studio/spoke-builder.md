---
title: Building spokes using Spoke Generator
description: Automate integration tasks by creating a sequence of reusable actions to develop custom integrations called spokes.
locale: en-US
release: zurich
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2025-09-02"
reading_time_minutes: 3
breadcrumb: [Use, Workflow Studio, Build workflows]
---

# Building spokes using Spoke Generator

Automate integration tasks by creating a sequence of reusable actions to develop custom integrations called spokes.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps, for information about submitting requests to the store, and to download and install Spoke Generator \(sn\_spoke\_builder\). For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## App dependencies

If you’re having trouble installing the app, ensure that the dependent plugin, ServiceNow IntegrationHub Starter Pack Installer \(com.glide.hub.integrations.starter\) is installed. You need ServiceNow IntegrationHub Professional Pack Installer license in your prod and sub-prod environments for creating spokes using OpenAPI specification, Postman collection, or Now Assist.

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation.

## Capabilities

An Integration Hub custom spoke provides both inbound and outbound integration with third-party applications. These integrations, referred to as spokes, are easy to configure and enable you to quickly add powerful actions without the need to write a script. This feature requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

You can build custom spokes for the required third-party application by importing an [OpenAPI Specification](../task/create-spoke-fd.md) or [Postman collection](../task/create-spoke-postman-collection.md), [documentation snippets from third-party API documentation](now-assist-in-spk-gen.md), or [creating a spoke manually](../task/create-spoke-manual.md).

## Required user roles

-   Users with the admin role can:
    -   View the **Spokes** tab.
    -   Create a new spoke.
    -   Import an OpenAPI Specification.
    -   Create connection alias.
    -   Publish actions and save actions as drafts.
    -   See spoke activity log.
-   Users with the action\_designer and fd\_read\_actions roles can:
    -   View the **Spokes** tab.
    -   See actions in a spoke.
-   Users with the action\_designer role can add actions.

    **Note:** Users with just the fd\_read\_actions role can only see actions.

-   Users with the flow\_operator or flow\_designer can view flows and subflows.

## OpenAPI Specification size limit

By default, the system can import OpenAPI Specifications up to 10 MB. To increase the import size, update the **glide.rest.openapi.max\_request\_size** system property. The maximum value is 100 MB.

## Limitations of OpenAPI Specification

Spoke actions created by importing OpenAPI specification, contain the OpenAPI step. Ensure that you are aware of these OpenAPI step limitations.

-   **Request body media types**

    The request body only supports JSON media types.

    **Note:** A string type output object is created when the OpenAPI schema has additionalProperties or no properties.

-   **OpenAPI 3.0 components**

    OpenAPI 3.0 adds new components to Swagger 2.0 to describe an API in further detail. OpenAPI support in the OpenAPI step supports some, but not all of these components. The OpenAPI step does not currently support these components.

    -   Schema Object: oneOf, anyOf, additionalProperties properties
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


## App version

Spoke Generator v4.2.0 is the latest version.

-   **[Create spoke and build actions by importing an OpenAPI Specification](../task/create-spoke-fd.md)**  
Automate an integration and generate reusable actions by importing an OpenAPI Specification.
-   **[Create spoke and build actions by importing a Postman collection](../task/create-spoke-postman-collection.md)**  
Automate an integration and generate reusable actions by importing a Postman collection.
-   **[Use Now Assist to create spokes and build actions](now-assist-in-spk-gen.md)**  
Use Now Assist in Spoke Generator to create spokes and actions by providing the required third-party API documentation snippet as an input.
-   **[Create spoke and build actions manually](../task/create-spoke-manual.md)**  
Automate an integration and generate reusable actions manually.
-   **[Add more actions to the custom spoke](../task/actions-cust-spk.md)**  
Add more reusable actions to your custom spoke to automate an integration.

**Parent Topic:**[Using Workflow Studio](../../workflow-studio/reference/building-workflow-studio-components.md)

