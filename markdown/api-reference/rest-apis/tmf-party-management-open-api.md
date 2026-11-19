---
title: Party Management Open API
description: The Party Management Open API provides endpoints for managing parties with a relationship to the enterprise, like a consumer, account, or contact. Use this API to create, update, and retrieve data from the Consumer \[csm\_consumer\], Account \[customer\_account\], and Contact \[customer\_contact\] tables.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/api-reference/rest-apis/tmf-party-management-open-api.html
release: brazil
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# Party Management Open API

The Party Management Open API provides endpoints for managing parties with a relationship to the enterprise, like a consumer, account, or contact. Use this API to create, update, and retrieve data from the Consumer \[csm\_consumer\], Account \[customer\_account\], and Contact \[customer\_contact\] tables.

The Party Management Open API is a ServiceNow® implementation of the TM Forum Party Management API REST specification. This implementation is based on the [TMF632 Party Management API Conformance Profile v5.0.0 – TM Forum](https://www.tmforum.org/resources/reference/tmf632b-party-management-api-conformance-profile-v5-0-0/), June 2025. The Party Management Open API is conformance certified by TM Forum.

## Accessing the API

This API is provided within the sn\_tmf\_api namespace. The calling user must have the sn\_tmf\_api.party\_integrator role. The Customer Service Base Entities \(com.snc.cs\_base\) plugin is required, particularly for all GET operations.

## API versions

ServiceNow® supports two versions of Party Management Open API. See related method documentation based on the version you are working with:

-   [Party Management Open API v1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/rest-apis/tmf-party-mgmt-API-v1.md)
-   [Party Management Open API v2](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/rest-apis/tmf-party-mgmt-API-v2.md)

The following table summarizes the changes to the Party Management API between v1 and v2. Quickly review how the record type is determined and which values are accepted for contact medium types.

<table><thead><tr><th>

Change

</th><th>

v1

</th><th>

v2

</th></tr></thead><tbody><tr><td>

Party type

</td><td>

The root-level `partyOrPartyRole` object determines whether the request creates an Account, Consumer, or Contact record. The root-level `@type` field is optional.

</td><td>

The `partyOrPartyRole` object is removed from the root level of requests and responses. The root-level `@type` field is required and determines the record type. Valid values:

 -   Account: Creates an Account record.
-   Consumer: Creates a Consumer record.
-   Contact: Creates a Contact record.

</td></tr><tr><td>

Contact medium type

</td><td>

`contactMedium.mediumType`

</td><td>

`contactMedium.contactType` The accepted values are the same as in v1: email, mobilePhone, businessPhone, homePhone, and postalAddress.

</td></tr></tbody>
</table>## Migrating requests from v1 to v2

1.  If your integration specifies v1 in the endpoint path, change it to v2, or remove the version to use the default.
2.  Remove the root-level **partyOrPartyRole** object from the request body.
3.  In POST requests, add the root-level **@type** field and set it to `Account`, `Consumer`, or `Contact`. This field is optional in v1 but required in v2.
4.  In each **contactMedium** object, rename **mediumType** to **contactType**. Keep the existing values.

-   **[Party Management Open API v1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/rest-apis/tmf-party-mgmt-API-v1.md)**  
The Party Management Open API v1 provides endpoints for managing parties with a relationship to the enterprise, such as accounts, consumers, and contacts. Use this API to create, update, retrieve, and inactivate records in the Consumer \[csm\_consumer\], Account \[customer\_account\], and Contact \[customer\_contact\] tables.
-   **[Party Management Open API v2](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/rest-apis/tmf-party-mgmt-API-v2.md)**  
The Party Management Open API v2 provides endpoints for managing parties with a relationship to the enterprise, such as accounts, consumers, and contacts. Use this API to create, update, retrieve, and inactivate records in the Consumer \[csm\_consumer\], Account \[customer\_account\], and Contact \[customer\_contact\] tables.

**Parent Topic:**[REST API reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/rest-apis/api-rest.md)

