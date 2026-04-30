---
title: API reference
description: Use ServiceNow APIs to change functionality and add features on the ServiceNow AI Platform.
locale: en-US
release: zurich
product: API Reference
classification: api-reference
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [API implementation and reference]
---

# API reference

Use ServiceNow APIs to change functionality and add features on the ServiceNow AI Platform.

<table id="table_iwv_lpv_klb" class="nav-card"><tbody><tr><td>

[Client ![](../../../reuse/icons/brand-icons/bus-monitor.svg) Control how the ServiceNow AI Platform functions and is displayed within the web browser.](api-client.md)

</td><td>

[Client Next Experience ![](../../../reuse/icons/brand-icons/bus-laptop.svg) Control how the ServiceNow AI Platform functions and is displayed within the web browser in the Next Experience UI Framework.](api-client-next.md)

</td><td>

[Client mobile ![](../../../reuse/icons/brand-icons/bus-mobile-native.svg) Build custom mobile experiences inside of ServiceNow AI Platform native mobile apps.](api-client-mobile.md)

</td><td>

[Mobile SDK ![](../../../reuse/icons/brand-icons/bus-mobile-phone.svg) Leverage the ServiceNow AI Platform within standalone Android and iOS apps.](api-mobile_sdk.md)

</td></tr><tr><td>

[Server ![](../../../reuse/icons/brand-icons/bus-server.svg) Build and update applications.](api-server.md)

</td><td>

[REST ![](../../../reuse/icons/brand-icons/bus-cloud.svg) Access and update data.](api-rest.md)

</td><td>

[UI Builder ![](../../../reuse/icons/brand-icons/bus-service-map.svg) Build client scripts in UI Builder.](api-uib.md)

</td><td>

[Browse APIs by product ![](../../../reuse/icons/brand-icons/bus-find-an-app.svg) Find APIs to use with your ServiceNow products.](api-product-type.md)

</td></tr></tbody>
</table>## Client

Use client-side JavaScript APIs to control how the ServiceNow AI Platform functions and displays within the web browser. Client-side APIs provide common functionality that you can add to your instance by calling the APIs from client-side scripts such as client scripts and UI policy scripts.

Common use cases:

-   Use the [GlideAjax](../../../app-store/dev_portal/API_reference/GlideAjax/concept/c_GlideAjaxAPI.md#) API to call server-side code from a client script.
-   Use the [GlideForm](../../../app-store/dev_portal/API_reference/GlideForm/concept/c_GlideFormAPI.md#) API to customize forms.

## Client mobile

Cabrillo JS is a client-side JavaScript API for accessing capabilities inside ServiceNow AI Platform native mobile applications. Cabrillo JS provides methods to use native device capabilities, native mobile UI, and other ServiceNow AI Platform mobile functionality.

## Mobile SDK

Use the ServiceNow Mobile SDK to leverage the functionality and resources of the ServiceNow AI Platform within your standalone mobile Android and iOS applications.

Using the Mobile SDK, you can perform the following within your applications:

-   Access data on your ServiceNow instance through its public REST APIs or custom scripted REST APIs that you develop.
-   Embed and enable Virtual Agent within your application interface.
-   Gather and track custom analytics events for analysis.
-   Attach documents \(attachments\) to a record within your ServiceNow instance.
-   Load web pages hosted on your ServiceNow instance in a native web view or Cabrillo.
-   Provide simple authentication flows using JSON Web Tokens for third-party applications to authenticate users.
-   Send push notifications.

## Server

Use server-side JavaScript APIs to change the functionality of existing applications or to build new applications. Server-side APIs provide common functionality that you can add to your instance by calling the APIs from server-side scripts such as business rules and script includes. Scoped APIs are intended for use with scoped applications, and global APIs are intended for use with applications in the global scope. New applications are typically scoped. Applications in the global scope are typically legacy applications.

Common use cases:

-   Use the [GlideRecord](../../../app-store/dev_portal/API_reference/glideRecordScoped/concept/c_GlideRecordScopedAPI.md#) or [GlideQuery](../../../app-store/dev_portal/API_reference/GlideQuery/concept/GlideQueryGlobalAPI.md#) APIs to perform create, read, update, and delete operations on record data from server-side scripts.
-   Use the [GlideSystem](../../../app-store/dev_portal/API_reference/glideSystemScoped/concept/c_GlideSystemScopedAPI.md#) API to access information about the instance or the current user session and to write informational or error messages.
-   Use [FlowAPI](../../../app-store/dev_portal/API_reference/ScriptableFlowAPI/concept/ScriptableFlowAPI.md#) methods to trigger flows, subflows, and actions from server-side scripts.

## REST

Use REST APIs to access and update data on the ServiceNow AI Platform. You can discover these APIs from within your instance by using the REST API Explorer. If you don't find an API that meets your needs, you can create custom REST APIs using the Scripted REST API feature. ServiceNow REST APIs support Basic Authentication and OAuth 2.0 to authenticate requests.

Common use cases:

-   Use the [Attachment API](../../../integrate/inbound-rest/concept/c_AttachmentAPI.md#) to upload and query file attachments.
-   Use the [Email API](../../../integrate/inbound-rest/concept/email-api.md#) to send and receive email messages.
-   Use the [Table API](../../../integrate/inbound-rest/concept/c_TableAPI.md#) to create, read, update, and delete records in a table.

## UI Builder

Use UI Builder APIs when developing client scripts in the [UI Builder](https://www.servicenow.com/docs/access?context=ui-builder-overview&version=zurich&pubname=zurich-application-development&ft:locale=en-US). Client scripts are executed in response to something happening on a page, such as:

-   User interaction events/actions, such as a button click.
-   Lifecycle events, such as a data broker execution started.

