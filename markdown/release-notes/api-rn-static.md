---
title: API release notes
description: The ServiceNow APIs enable organizations to programmatically integrate ServiceNow with other systems, automate business processes, and extend platform capabilities to create seamless, end-to-end workflows across their entire IT and business ecosystem. See the following sections for release notes by family and store release.ServiceNow APIs enable you to build custom applications and experiences. APIs were enhanced and updated in the Brazil release.ServiceNow APIs enable you to build custom applications and experiences. APIs were enhanced and updated in the ServiceNow Store release.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/api-rn-static.html
release: brazil
topic_type: topic
last_updated: "2026-09-10"
reading_time_minutes: 5
breadcrumb: [Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# API release notes

The ServiceNow® APIs enable organizations to programmatically integrate ServiceNow® with other systems, automate business processes, and extend platform capabilities to create seamless, end-to-end workflows across their entire IT and business ecosystem. See the following sections for release notes by family and store release.

## About ServiceNow® APIs

-   Use server-side JavaScript APIs in scripts to change the application functionality.
-   Run client APIs whenever a client-based event occurs, such as when a form loads, a form is submitted, or a field value changes.
-   Use inbound REST APIs to interact with various ServiceNow functionalities within your application.
-   Client Next Experience APIs include client APIs compatible with the Next Experience UI.

See [API implementation and reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/api-implementation-reference.md) for more information.

## Activation and other requirements

-   **Activation information**

    API activation is dependent on the specific product or application where the API is required. Consult your product documentation or contact your ServiceNow® administrator to determine activation steps for your use case.


**Parent Topic:**[Features and changes by product](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/new-features-changes.md)

## Brazil Early Availability

ServiceNow® APIs enable you to build custom applications and experiences. APIs were enhanced and updated in the Brazil release.

### What's new

-   ****

<table id="table_djq_2qv_bkc"><thead><tr><th>

Application

</th><th>

API type

</th><th>

API

</th><th>

Endpoints

</th></tr></thead><tbody><tr><td>

Developer Sandboxes

</td><td>

REST

</td><td>

[Developer Sandbox Management API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/developer-sandbox-management-api.md)

</td><td>

Programmatically create, list, retrieve, and destroy isolated development environments within a ServiceNow® instance.-   DELETE /dsbName
-   GET /operationId
-   GET /sandboxes
-   GET /sysId
-   POST /sandboxes


</td></tr><tr><td>

Stream Connect

</td><td>

REST

</td><td>

[Schema Registry API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/schema_registry-api.md)

</td><td>

Retrieve Avro schemas along with their subject and version history.-   GET /schemas
-   GET /schemas/ids/\{id\}
-   GET /schemas/ids/\{id\}/schema
-   GET /schemas/ids/\{id\}/subjects
-   GET /schemas/ids/\{id\}/versions
-   GET /subjects
-   GET /subjects/\{subject\}/versions
-   GET /subjects/\{subject\}/versions/\{version\}
-   GET /subjects/\{subject\}/versions/\{version\}/schema


</td></tr><tr><td>

Sales Cart

</td><td>

REST

</td><td>

[Sales Cart REST API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/sales-cart-api.md)

</td><td>

Programmatically create, read, update, and submit a sales cart and its line items, or remove a cart or line item entirely.-   POST /sales\_cart
-   PATCH /v1/sales\_cart
-   GET /v1/sales\_cart
-   GET /sales\_cart/\{cart\_id\}
-   GET /sales\_cart/\{cartId\}/line-item/\{lineItemId\}
-   POST /sales\_cart/\{cart\_id\}/submitorder
-   DELETE /sales\_cart/\{cart\_id\}
-   DELETE /sales\_cart/\{cartId\}/line-item/\{lineItemId\}


</td></tr><tr><td>

Platform \(Glide\)

</td><td>

Mobile Scripting

</td><td>

-   [MobileGlideDate - Scoped](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/MobileGlideDateScopedAPI.md)
-   [MobileGlideDateTime - Scoped](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/MobileGlideDateTimeScopedAPI.md)
-   [MobileGlideElement - Scoped](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/MobileGlideElementScopedAPI.md)
-   [MobileGlideRecord - Scoped](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/MobileGlideRecordScopedAPI.md)
-   [MobileGlideSystem - Scoped](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/MobileGlideSystemScopedAPI.md)
-   [MobileGlideTime - Scoped](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/MobileGlideTimeScopedAPI.md)
-   [MobileGlideUser - Scoped](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/MobileGlideUserScopedAPI.md)
-   [MobileScripts - Scoped](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/MobileScriptsScopedAPI.md)


</td><td>

The Mobile Offline Scripting APIs introduce a set of scripting classes in the `sn_mobile_scripting` namespace that can run against data stored on a user's device. These classes query and modify records, read and write field values, and evaluate dates and times, so button conditions and write-back actions continue to work while the mobile app is offline. Because mobile scripts are a subset of the scripting capabilities available in the browser, the same script runs on the instance without modification when connectivity is available.

</td></tr></tbody>
</table>
### What's changed

-   ****

    |Application|API type|API|Endpoints|
    |-----------|--------|---|---------|
    |Virtual Agent and Live Agent|REST|[Virtual Agent Bot Integration API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/bot-api.md)|POST /bot/integration: The `history` parameter of the Virtual Agent Bot Integration API now supports an `attachment` type, letting the primary bot include files that were shared earlier in the conversation when it passes chat history to Virtual Agent or Live Agent.|


## September 2026

ServiceNow® APIs enable you to build custom applications and experiences. APIs were enhanced and updated in the ServiceNow Store release.

### What's new

-   ****

<table id="table_djq_2qv_bkc"><thead><tr><th>

Application

</th><th>

App Version

</th><th>

API type

</th><th>

API

</th><th>

Endpoints

</th></tr></thead><tbody><tr><td>

Telecommunications Open APIs, Order Management for Telecommunications, Media, and Technology

</td><td>

8.0.1, 15.0.0

</td><td>

REST

</td><td>

[Product Offering Qualification API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/product-offering-qualification-api.md)

</td><td>

-   POST /queryProductOfferingQualification
-   POST /checkProductOfferingQualification


</td></tr></tbody>
</table>
### What's changed

-   ****

<table id="table_rgg_kz3_sjc"><thead><tr><th>

Application

</th><th>

App Version

</th><th>

API type

</th><th>

API

</th><th>

Methods/endpoints

</th></tr></thead><tbody><tr><td>

Workplace Calendar Synchronization

</td><td>

3.4.16

</td><td>

REST

</td><td>

[WSD Recurring Reservation API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/wsd_recur_reserv-api.md)

</td><td>

POST /create\_series: The recurringPattern parameter now uses RFC 5545 iCalendar format \(freq, dtstart, interval, byweekday, tzid, etc.\) for better timezone handling and standards compliance. **Note:** Legacy format patterns \(using repeats, options.\*, and startDate\) remain supported and continue to work without changes.

</td></tr><tr><td>

Interaction Controls Component

</td><td>

3.0.1

</td><td>

Client

</td><td>

[openFrameAPI - Client](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/c_openFrameAPI.md)

</td><td>

-   setICContext\(\): Supports supervisor monitoring controls \(coaching, monitoring, barging\), callback transfer enhancements with directTarget support, and clarified conditional logic for callback context timing.
-   subscribe\(\): Supports five new callback-related sub-actions \(callbackLeaveAndTransfer, getSearchTarget, getMoreInfo, callbackTransferInitiated, cancelCallbackTransfer\) and the openframe\_icc\_record\_opened event for manager role interaction tracking.

</td></tr><tr><td>

Product Catalog Management Core application

</td><td>

20.0.2

</td><td>

REST

</td><td>

[Product Catalog Search API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/product-catalog-search-api.md)

</td><td>

The POST /search endpoint now returns the **productOfferingFamily** field, which identifies the product offering family that each offering belongs to.

</td></tr><tr><td>

Product Catalog Management Core application

</td><td>

20.0.2

</td><td>

Server

</td><td>

[CatalogSearchAPI - Scoped, Global](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/server-api-reference/CatalogSearchAPI-scoped_global.md)

</td><td>

The getCatalogData\(\) now returns the `productOfferingFamily` field, which identifies the product offering family that each offering belongs to.

</td></tr><tr><td>

Telecommunications Open APIs, Order Management for Telecommunications, Media, and Technology

</td><td>

8.0.1, 15.0.0

</td><td>

REST

</td><td>

[Product Order Open API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/tmf622_product_ordering-api.md)

</td><td>

PATCH /productOrder/\{id\}: -   Now supports a `changeType=nonProduct` parameter to update order and line item administrative details without triggering product change workflows or state transitions.
-   Now accepts either the system ID \(`sys_id`\) or external ID \(`external_id`\) in the `productOrderItem.id` field, reducing the need for additional lookups when updating line items.
-   Supports associating payment profiles, billing accounts, and related parties \(Account, Contact, Location, and Consumer\) with product orders. This allows clients to link existing records or create new ones inline during order placement for streamlined end-to-end order workflows.
GET/LIST endpoints now support the following query parameters: `Account`, `Contact and Consumer(Related Party)`, `externalID`.

</td></tr><tr><td>

Telecommunications Open APIs, Order Management for Telecommunications, Media, and Technology

</td><td>

8.0.1, 15.0.0

</td><td>

REST

</td><td>

[Service Order Open API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/service-order-open-api.md)

</td><td>

GET/LIST endpoints now support the following query parameters: `Account`, `Contact and Consumer(Related Party)`, `externalID`, `expectedStartDate`, `CompletionDate`, `requestedStartDate`, `requestedCompletionDate`, `expectedCompletionDate`.

</td></tr><tr><td>

Telecommunications Open APIs, Order Management for Telecommunications, Media, and Technology

</td><td>

8.0.1, 15.0.0

</td><td>

REST

</td><td>

[Product Inventory Open API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/product-inventory-open-api.md)

</td><td>

GET/LIST endpoints now support the following query parameters: `Account`, `Contact` and `Consumer`\(Related Party\), `billingAccount`.

</td></tr><tr><td>

Telecommunications Open APIs, Order Management for Telecommunications, Media, and Technology

</td><td>

8.0.1, 15.0.0

</td><td>

REST

</td><td>

[Product Catalog Open API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/product-catalog-open-api.md)

</td><td>

GET/LIST endpoints now support the following query parameters: `externalID`, `isSellable`

</td></tr><tr><td>

Telecommunications Open APIs, Order Management for Telecommunications, Media, and Technology

</td><td>

8.0.1, 15.0.0

</td><td>

REST

</td><td>

[Service Test Management Open API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/service-test-management-api.md)

</td><td>

All GET and POST endpoints responses return `id` and `externalId` as distinct fields on ServiceTest and ServiceTestSpecification resources. The `id` field returns the record's `sys_id`, and `externalId` returns the value of the `external_id` column when one is set. Existing query resolution behavior is unchanged, so requests that filter on an external identifier continue to work.

</td></tr><tr><td>

Telecommunications Open APIs, Order Management for Telecommunications, Media, and Technology

</td><td>

8.0.1, 15.0.0

</td><td>

REST

</td><td>

[Product Catalog Open API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/product-catalog-open-api.md)

</td><td>

GET/LIST endpoints: Supports the Accept-Language request header on GET and LIST operations for retrieving translated field values, and filtering by translated name on LIST operations.

</td></tr></tbody>
</table>
