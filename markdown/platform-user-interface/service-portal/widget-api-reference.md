---
title: Widget API reference
description: Service Portal includes client and server side APIs to use in widget client and server scripts.Global variable and functions available in widget client and server scripts.
locale: en-US
release: australia
product: Service Portal
classification: service-portal
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Developing custom widgets, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Widget API reference

Service Portal includes client and server side APIs to use in widget client and server scripts.

## Service Portal client-side APIs

These are Service Portal APIs that you can use in a widget client controller.

See the API reference for detailed class and method information.

<table id="table_skq_rjp_h1b"><thead><tr><th>

Class

</th><th>

Description

</th></tr></thead><tbody><tr><td>

[spAriaUtil](https://www.servicenow.com/docs/access?context=spAriaUtil-API&version=australia&pubname=australia-api-reference&ft:locale=en-US)

</td><td>

Shows messages on a screen reader.

</td></tr><tr><td>

[spContextManager](https://www.servicenow.com/docs/access?context=spContextManagerAPI&version=australia&pubname=australia-api-reference&ft:locale=en-US)

</td><td>

Makes data from a Service Portal widget available to other applications and services in a Service Portal page. For example, pass widget data to Agent Chat when it opens in a Service Portal page.

</td></tr><tr><td>

[spUtil](https://www.servicenow.com/docs/access?context=spUtilAPI&version=australia&pubname=australia-api-reference&ft:locale=en-US)

</td><td>

Utility methods to perform common functions in a Service Portal widget client script.

</td></tr><tr><td>

[spModal](https://www.servicenow.com/docs/access?context=SPModal-API&version=australia&pubname=australia-api-reference&ft:locale=en-US)

</td><td>

Shows alerts, prompts, and confirmation dialogs in Service Portal widgets. The spModal class is available in Service Portal client scripts.

</td></tr></tbody>
</table>**Note:** g\_form as a global object cannot be used in a widget client controller or in a UI script.

## Service Portal server-side APIs

These are Service Portal APIs that you can use in a widget server script.

<table id="table_sfm_vjp_h1b"><thead><tr><th>

Class

</th><th>

Description

</th></tr></thead><tbody><tr><td>

[GlideSPScriptable](https://www.servicenow.com/docs/access?context=c_GlideSPScriptableScopedAPI&version=australia&pubname=australia-api-reference&ft:locale=en-US)

</td><td>

The GlideSPScriptable API provides methods to interact with data and perform record operations in Service Portal widgets.

</td></tr><tr><td>

[GlideSPSearchAnalytics](https://www.servicenow.com/docs/access?context=GlideSPSearchAnalyticsAPI&version=australia&pubname=australia-api-reference&ft:locale=en-US)

</td><td>

The GlideSPSearchAnalytics API provides methods to generate search analytics from custom ServiceNow search widgets.

</td></tr><tr><td>

[SPScriptedFacet - Scoped](https://www.servicenow.com/docs/access?context=SPScriptedFacetScopedAPI&version=australia&pubname=australia-api-reference&ft:locale=en-US)

</td><td>

Defines facet items, filters, or mapped queries for a facets object.

</td></tr><tr><td>

[SPScriptedFacetService - Scoped](https://www.servicenow.com/docs/access?context=SPScriptedFacetServiceScopedAPI&version=australia&pubname=australia-api-reference&ft:locale=en-US)

</td><td>

Generates a multi-choice or single-choice facets object for an advanced search source.

</td></tr><tr><td>

[SPSEOUtilsSNC - Global](https://www.servicenow.com/docs/access?context=SPSEOUtilsSNCAPI&version=australia&pubname=australia-api-reference&ft:locale=en-US)

</td><td>

Return human-readable URLs for a specific page, or for the current page, based on the transaction request.

</td></tr><tr><td>

[SPWidgetAccessControl - Global](https://www.servicenow.com/docs/access?context=SPWidgetAccessControlGlobalAPI&version=australia&pubname=australia-api-reference&ft:locale=en-US)

</td><td>

Check whether a provided table is granted access to a widget to ensure that a widget is securely accessed by an intended audience.

</td></tr></tbody>
</table>**Parent Topic:**[Developing custom widgets](../concept/widget-dev-guide.md)

## Widget properties

Global variable and functions available in widget client and server scripts.

### Server script global objects

|Property|Description|
|--------|-----------|
|`input`|An object containing client-side properties set under `c.data`. The value is `undefined` until the client controller calls `c.server.update()`.|
|`data`|An object containing properties set during server-side execution.|
|`options`|An object containing the schema option properties.|

### Client script global functions

|Property|Description|
|--------|-----------|
|`this.server.get([Object])`|Calls the server and sends custom `input`. Returns `Promise`.|
|`this.server.update()`|Calls the server and posts `this.data` to the server script. Returns `Promise`.|
|`this.server.refresh()`|Calls the server and automatically replaces the current options and data from the server response. Returns `Promise`.|

A `promise` represents the eventual result of an asynchronous operation. For more information on promises, see [https://promisesaplus.com/](https://promisesaplus.com/) or [AngularJS documentation](https://docs.angularjs.org/api/ng/service/$q).

