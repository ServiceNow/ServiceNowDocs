---
title: SCIM2Client - Scoped
description: The SCIM2Client API provides methods that call the System for Cross-domain Identity Management \(SCIM\) Provider \(server role\) to create, update, or delete data in a service provider \(SP\).Deletes a specified resource from an external service provider system.Returns all resources from a specified external provider system that match the passed criteria.Returns a resource from the external provider system with the specified unique resource ID.Creates or updates a resource in an external service provider system for a specified sys\_id.Creates a new resource in an external service provider system for a specified sys\_id.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 9
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# SCIM2Client- Scoped

The SCIM2Client API provides methods that call the System for Cross-domain Identity Management \(SCIM\) Provider \(server role\) to create, update, or delete data in a service provider \(SP\).

SCIM is a REST and JSON-based protocol that defines a client and server role. A client is usually an identity provider \(IDP\), such Okta, that contains a robust directory of user identities. An SP is typically a SaaS application, such as Box or Slack, that needs a subset of information from those identities. When changes to identities are made in the IDP, including create, update, and delete, they are automatically synchronized to the SP according to the SCIM protocol.

The following image illustrates typical API call flows for manipulating service provider data.

![SCMI Client API call flow](../images/SCIMClient_call_flow.png)

This API runs in the `sn_auth` namespace and requires the SCIM v2 - ServiceNow Cross-domain Identity Management Client \(com.snc.integration.scim2.client\) plugin to be installed to access the API.

You can locate the results of each SCIM method call in the SCIM Client Logs \[sys\_scim\_client\_logs\] table.

For additional information on SCIM, see System for Cross-domain Identity Management \(SCIM\).

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## SCIM2Client - executeDelete \(String provider, String resourceName, String providerResourceId\)

Deletes a specified resource from an external service provider system.

<table id="table_yhc_r5k_btb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

provider

</td><td>

String

</td><td>

Required. Name of the configured SCIM service provider. The service provider name is defined in the name field of the SCIM Provider \[sys\_scim\_provider\] table.

</td></tr><tr><td>

resourceName

</td><td>

String

</td><td>

Required. Name of the resource type, such as User or Group.Table: In the resource\_name field of the SCIM Provider Resource Mapping \[sys\_scim\_provider\_resource\_mapping\] table.

</td></tr><tr><td>

providerResourceId

</td><td>

String

</td><td>

Required. Unique identifier of the associated resource on the external service provider system.

</td></tr></tbody>
</table><table id="id_hqb_vfl_btb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

message

</td><td>

If the **status** is SUCCESS, the endpoint returns the response body as defined by the REST [SCIM](../../../../../integrate/inbound-rest/concept/scim-api.md#) API.Data type: String

</td></tr><tr><td>

status

</td><td>

Status of the request.Possible values:

-   FAILURE
-   SUCCESS

Data type: String

</td></tr></tbody>
</table>The following example shows how to delete a user resource in the SNOW Provider system.

```
var scimClient = new sn_auth.SCIM2Client(); 
var response = scimClient.executeDelete('SNOW Provider','User','f282abf03710200044e0bfc8bcbe5d12'); 
gs.info('response: ' + response);
```

Output:

```
// Example of a successful response
{
  "status":"SUCCESS",
  "message":null
}

// Example of a failed response
{
  "status":"FAILURE",
  "message":"{
    \"schemas\":[
      \"urn:ietf:params:scim:api:messages:2.0:Error\"
    ],
    \"status\":\"404\",
    \"detail\":\"Invalid user id 3985e598876989103fa711f83cbb35ae1\"
  }"
}
```

## SCIM2Client - executeGet \(String provider, String resourceName, String queryParams\)

Returns all resources from a specified external provider system that match the passed criteria.

This information is used to call the corresponding SCIM service provider API.

<table id="table_smr_cpk_btb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

provider

</td><td>

String

</td><td>

Required. Name of the configured SCIM service provider. The service provider name is defined in the name field of the SCIM Provider \[sys\_scim\_provider\] table.

</td></tr><tr><td>

resourceName

</td><td>

String

</td><td>

Required. Name of the resource type, such as User or Group.Table: In the resource\_name field of the SCIM Provider Resource Mapping \[sys\_scim\_provider\_resource\_mapping\] table.

</td></tr><tr><td>

queryParams

</td><td>

String

</td><td>

Required. SCIM compliant query parameters passed to the external SCIM service provider endpoint.For additional information on the available query parameters and their associated format, refer to the following sections in the Internet Engineering Task Force document: System for Cross-domain Identity Management: Protocol

-   [https://datatracker.ietf.org/doc/html/rfc7644\#section-3.4.2.2](https://datatracker.ietf.org/doc/html/rfc7644#section-3.4.2.2)
-   [https://datatracker.ietf.org/doc/html/rfc7644\#section-3.4.2.4](https://datatracker.ietf.org/doc/html/rfc7644#section-3.4.2.4)
-   [https://datatracker.ietf.org/doc/html/rfc7644\#section-3.4.2.3](https://datatracker.ietf.org/doc/html/rfc7644#section-3.4.2.3)
-   [https://datatracker.ietf.org/doc/html/rfc7644\#section-3.4.2.5](https://datatracker.ietf.org/doc/html/rfc7644#section-3.4.2.5)

</td></tr></tbody>
</table><table id="id_orm_vrt_ctb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

message

</td><td>

If the **status** is SUCCESS, the endpoint returns the response body as defined by the REST [SCIM](../../../../../integrate/inbound-rest/concept/scim-api.md#) API.Data type: String

</td></tr><tr><td>

status

</td><td>

Status of the request.Possible values:

-   FAILURE
-   SUCCESS

Data type: String

</td></tr></tbody>
</table>The following example shows how to retrieve all of the available users from the snow test service provider whose work email contains lucius.bagnoli.

```
var scimClient = new sn_auth.SCIM2Client(); 
var queryParams = {}; 
queryParams['filter'] = 'emails[type eq \"work\" and value co \"lucius.bagnoli\"]'; 
var response = scimClient.executeGet('SCIM Provider Demo','User', queryParams); 
gs.info('response for get with filter: ' + response);
```

Response:

```
//Example of a successful response
{
  "status":"SUCCESS",
  "message":"{
    \"schemas\":[
      \"urn:ietf:params:scim:api:messages:2.0:ListResponse\"
    ],
  \"totalResults\":647,
  \"Resources\":[
    {
      \"schemas\":[
        \"urn:ietf:params:scim:schemas:extension:servicenow:2.0:User\",
        \"urn:ietf:params:scim:schemas:core:2.0:User\"
      ],
    \"id\":\"005d500b536073005e0addeeff7b12f4\",
    \"meta\":{
      \"resourceType\":\"User\",
      \"created\":\"2019-04-05T21:09:12Z\",
      \"lastModified\":\"2021-10-10T19:38:36Z\",
      \"location\":\"https://empiamsd1.service-now.com/api/now/scim/Users/005d500b536073005e0addeeff7b12f4\"
    },
    \"userName\":\"survey.user\",
    \"name\":{
      \"familyName\":\"user\",
      \"givenName\":\"survey\"
    },
    \"displayName\":\"survey user\",
    \"active\":true,
    \"emails\":[
      {
        \"value\":\"survey.user@email.com\",
        \"type\":\"work\"
      }
    ]
  },
  {
    \"schemas\":[
      \"urn:ietf:params:scim:schemas:extension:servicenow:2.0:User\",
      \"urn:ietf:params:scim:schemas:core:2.0:User\"
    ],
    \"id\":\"02826bf03710200044e0bfc8bcbe5d3f\",
    \"meta\":{
      \"resourceType\":\"User\",
      \"created\":\"2012-02-18T03:04:49Z\",
      \"lastModified\":\"2021-10-10T19:38:36Z\",
      \"location\":\"https://empiamsd1.service-now.com/api/now/scim/Users/02826bf03710200044e0bfc8bcbe5d3f\"
    },
    \"userName\":\"lucius.bagnoli\",
    \"name\":{
      \"familyName\":\"Bagnoli\",
      \"givenName\":\"Lucius\"
    },
    \"displayName\":\"Lucius Bagnoli\",
    \"active\":true,
    \"emails\":[
      {
        \"value\":\"lucius.bagnoli@example.com\",
        \"type\":\"work\"
      }
    ],
    \"urn:ietf:params:scim:schemas:extension:servicenow:2.0:User\":{
      \"gender\":\"Male\",
      \"costCenter\":{
        \"value\":\"91e8bbf43710200044e0bfc8bcbe5daa\",
        \"name\":\"Customer Support\",
        \"$ref\":\"https://empiamsd1.service-now.com/api/now/scim/CostCenters/91e8bbf43710200044e0bfc8bcbe5daa\"
      },
      \"company\":{
        \"value\":\"81fd65ecac1d55eb42a426568fc87a63\",
        \"name\":\"ACME Japan\",
        \"$ref\":\"https://empiamsd1.service-now.com/api/now/scim/Companies/81fd65ecac1d55eb42a426568fc87a63\"
      },
      \"department\":{
        \"value\":\"5d7f17f03710200044e0bfc8bcbe5d43\",
        \"name\":\"Customer Support\",
        \"$ref\":\"https://empiamsd1.service-now.com/api/now/scim/Departments/5d7f17f03710200044e0bfc8bcbe5d43\"
      },
      \"manager\":{
        \"value\":\"02826bf03710200044e0bfc8bcbe5d88\",
        \"displayName\":\"Billie Cowley\",
        \"$ref\":\"https://empiamsd1.service-now.com/api/now/scim/Users/02826bf03710200044e0bfc8bcbe5d88\"
      },
      \"location\":{
        \"value\":\"0002c0a93790200044e0bfc8bcbe5df5\",
        \"name\":\"2-10-1 Yurakucho, Chiyoda-ku, Tokyo\",
        \"$ref\":\"https://empiamsd1.service-now.com/api/now/scim/Locations/0002c0a93790200044e0bfc8bcbe5df5\"
      }
    }
  }
],
\"startIndex\":1,
\"itemsPerPage\":2}"}


// Example of a failure response
{
  "status":"FAILURE",
  "message":"SCIM Provider rest message is not configured properly"
}
```

## SCIM2Client - executeGetById \(String provider, String resourceName, String providerResourceId, Map&lt;String, String&gt; queryParams\)

Returns a resource from the external provider system with the specified unique resource ID.

This information is used to call the corresponding SCIM service provider API.

<table id="id_xsc_lmk_btb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

provider

</td><td>

String

</td><td>

Required. Name of the configured SCIM service provider. The service provider name is defined in the name field of the SCIM Provider \[sys\_scim\_provider\] table.

</td></tr><tr><td>

providerResourceId

</td><td>

String

</td><td>

Required. Unique identifier of the associated resource on the external service provider system.

</td></tr><tr><td>

queryParams

</td><td>

String

</td><td>

Required. SCIM compliant query parameters passed to the external SCIM service provider endpoint.For additional information on the available query parameters and their associated format, refer to the following sections in the Internet Engineering Task Force document: System for Cross-domain Identity Management: Protocol

-   [https://datatracker.ietf.org/doc/html/rfc7644\#section-3.4.2.2](https://datatracker.ietf.org/doc/html/rfc7644#section-3.4.2.2)
-   [https://datatracker.ietf.org/doc/html/rfc7644\#section-3.4.2.4](https://datatracker.ietf.org/doc/html/rfc7644#section-3.4.2.4)
-   [https://datatracker.ietf.org/doc/html/rfc7644\#section-3.4.2.3](https://datatracker.ietf.org/doc/html/rfc7644#section-3.4.2.3)
-   [https://datatracker.ietf.org/doc/html/rfc7644\#section-3.4.2.5](https://datatracker.ietf.org/doc/html/rfc7644#section-3.4.2.5)

</td></tr></tbody>
</table><table id="id_sz2_wrt_ctb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

message

</td><td>

If the **status** is SUCCESS, the endpoint returns the response body as defined by the REST [SCIM](../../../../../integrate/inbound-rest/concept/scim-api.md#) API.Data type: String

</td></tr><tr><td>

status

</td><td>

Status of the request.Possible values:

-   FAILURE
-   SUCCESS

Data type: String

</td></tr></tbody>
</table>This example shows how to obtain the specified resource from the external provider system "snow test".

```
var scimClient = new sn_auth.SCIM2Client(); 
var queryParams = {}; 
var response = scimClient.executeGetById('snow test','User', 'f282abf03710200044e0bfc8bcbe5d12', queryParams); 
gs.info('response for simple getById: ' + response); 
```

Output:

```
// Example of a successful response
{
  "status":"SUCCESS",
  "message":"{
    \"schemas\":[
      \"urn:ietf:params:scim:schemas:extension:servicenow:2.0:User\",
      \"urn:ietf:params:scim:schemas:core:2.0:User\"
    ],
    \"id\":\"f282abf03710200044e0bfc8bcbe5d12\",
    \"meta\":{
      \"resourceType\":\"User\",
      \"created\":\"2012-02-18T03:04:53Z\",
      \"lastModified\":\"2021-10-10T19:38:37Z\",
      \"location\":\"https://empiamsd1.service-now.com/api/now/scim/Users/f282abf03710200044e0bfc8bcbe5d12\"
    },
    \"userName\":\"tia.neumaier\",
    \"name\":{
      \"givenName\":\"Tia\"
    },
    \"displayName\":\"Tia Neumaier\",
    \"active\":true,
    \"emails\":[
      {
        \"value\":\"tia.neumaier@example.com\",
        \"type\":\"work\"
      }
    ],
    \"urn:ietf:params:scim:schemas:extension:servicenow:2.0:User\":{
      \"costCenter\":{
        \"value\":\"7fb1cc99c0a80a6d30c04574d14c0acf\",
        \"name\":\"Sales\",
        \"$ref\":\"https://empiamsd1.service-now.com/api/now/scim/CostCenters/7fb1cc99c0a80a6d30c04574d14c0acf\"
      },
      \"company\":{
        \"value\":\"227cdfb03710200044e0bfc8bcbe5d6b\",
        \"name\":\"ACME South America\",
        \"$ref\":\"https://empiamsd1.service-now.com/api/now/scim/Companies/227cdfb03710200044e0bfc8bcbe5d6b\"
      },
      \"department\":{
        \"value\":\"221db0edc611228401760aec06c9d929\",
        \"name\":\"Sales\",
        \"$ref\":\"https://empiamsd1.service-now.com/api/now/scim/Departments/221db0edc611228401760aec06c9d929\"
      },
      \"location\":{
        \"value\":\"25b4c23b0a0a0bb30054836629537509\",
        \"name\":\"Carretera Cancun-Chetumal KM 22, Cancun\",
        \"$ref\":\"https://empiamsd1.service-now.com/api/now/scim/Locations/25b4c23b0a0a0bb30054836629537509\"
      }
    }
  }"
}

// Example of a failed response
{
  "status":"FAILURE",
  "message":"{
    \"schemas\":[
      \"urn:ietf:params:scim:api:messages:2.0:Error\"
    ],
    \"status\":\"404\",
    \"detail\":\"User not found f282abf03710200044e0bfc8bcbe5d121\"
  }"
}
```

## SCIM2Client - provision \(String provider, String resourceName, String resourceId\)

Creates or updates a resource in an external service provider system for a specified sys\_id.

For example, if you create or update a user in a ServiceNow instance, you can use this method to create or update the same resource on an external service provider system. Only those fields which are mapped in the SCIM Provider Resource Mapping \[sys\_scim\_provider\_resource\_mapping \] table can be created or updated in the corresponding resource.

For additional information on provider resource mapping, see Create a SCIM Provider Resource Mapping.

<table id="table_urc_kcl_btb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

provider

</td><td>

String

</td><td>

Required. Name of the configured SCIM service provider. The service provider name is defined in the name field of the SCIM Provider \[sys\_scim\_provider\] table.

</td></tr><tr><td>

resourceName

</td><td>

String

</td><td>

Required. Name of the resource type, such as User or Group.Table: In the resource\_name field of the SCIM Provider Resource Mapping \[sys\_scim\_provider\_resource\_mapping\] table.

</td></tr><tr><td>

resourceId

</td><td>

String

</td><td>

Required. Sys\_id of the resource saved in the ServiceNow instance \(the client\).Table: In the primary\_table field of the SCIM Provider Resource Mapping \[sys\_scim\_provider\_resource\_mapping\] table.

</td></tr></tbody>
</table><table id="id_wc2_2fl_btb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

message

</td><td>

If the **status** is SUCCESS, the endpoint returns the response body as defined by the REST [SCIM](../../../../../integrate/inbound-rest/concept/scim-api.md#) API.Data type: String

</td></tr><tr><td>

status

</td><td>

Status of the request.Possible values:

-   FAILURE
-   SUCCESS

Data type: String

</td></tr></tbody>
</table>The following example shows how to provision a user on the Snow Provider.

```
var scimClient = new sn_auth.SCIM2Client(); 
var response = scimClient.provision('SNOW Provider','User','f282abf03710200044e0bfc8bcbe5d12'); 
gs.info('response: ' + response);
```

Output:

```
// Example of successful response
{
  "status":"SUCCESS",
  "message":"{
    \"schemas\":[
      \"urn:ietf:params:scim:schemas:extension:servicenow:2.0:User\",
      \"urn:ietf:params:scim:schemas:core:2.0:User\"
    ],
    \"id\":\"f282abf03710200044e0bfc8bcbe5d12\",
    \"meta\":{
      \"resourceType\":\"User\",
      \"created\":\"2012-02-18T03:04:53Z\",
      \"lastModified\":\"2021-10-10T19:38:37Z\",
      \"location\":\"https://empiamsd1.service-now.com/api/now/scim/Users/f282abf03710200044e0bfc8bcbe5d12\"
    },
    \"userName\":\"tia.neumaier\",
    \"name\":{
      \"familyName\":\"Neumaier\",
      \"givenName\":\"Tia\"
    },
    \"displayName\":\"Tia Neumaier\",
    \"active\":true,
    \"emails\":[
      {
        \"value\":\"tia.neumaier@example.com\",
        \"type\":\"work\"
      }
    ],
    \"urn:ietf:params:scim:schemas:extension:servicenow:2.0:User\":{
      \"gender\":\"Female\",
      \"costCenter\":{
        \"value\":\"7fb1cc99c0a80a6d30c04574d14c0acf\",
        \"name\":\"Sales\",
        \"$ref\":\"https://empiamsd1.service-now.com/api/now/scim/CostCenters/7fb1cc99c0a80a6d30c04574d14c0acf\"
      },
      \"company\":{
        \"value\":\"227cdfb03710200044e0bfc8bcbe5d6b\",
        \"name\":\"ACME South America\",
        \"$ref\":\"https://empiamsd1.service-now.com/api/now/scim/Companies/227cdfb03710200044e0bfc8bcbe5d6b\"
      },
      \"department\":{
        \"value\":\"221db0edc611228401760aec06c9d929\",
        \"name\":\"Sales\",
        \"$ref\":\"https://empiamsd1.service-now.com/api/now/scim/Departments/221db0edc611228401760aec06c9d929\"
      },
      \"location\":{
        \"value\":\"25b4c23b0a0a0bb30054836629537509\",
        \"name\":\"Carretera Cancun-Chetumal KM 22, Cancun\",
        \"$ref\":\"https://empiamsd1.service-now.com/api/now/scim/Locations/25b4c23b0a0a0bb30054836629537509\"
      }
    }
  }"
}

// Example of failure response
{
  "status":"FAILURE",
  "message":"SCIM client attribute or provider resource mapping is not configured properly , 
  No provider resource mapping id found for provider name: SNOW Provider and resource name: User"
}
```

## SCIM2Client - provisionNew \(String provider, String resourceName, String resourceId\)

Creates a new resource in an external service provider system for a specified sys\_id.

For example, if you create a new user in a ServiceNow instance, you can use this method to create the same resource on an external service provider system. Only those fields which are mapped in the SCIM Provider Resource Mapping \[sys\_scim\_provider\_resource\_mapping\] table can be created in the corresponding external service provider system. If the resource is already present in the external service provider system, an error response is returned.

For additional information on provider resource mapping, see Create a SCIM Provider Resource Mapping.

<table id="table_csg_wxp_btb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

provider

</td><td>

String

</td><td>

Required. Name of the configured SCIM service provider. The service provider name is defined in the name field of the SCIM Provider \[sys\_scim\_provider\] table.

</td></tr><tr><td>

resourceName

</td><td>

String

</td><td>

Required. Name of the resource type, such as User or Group.Table: In the resource\_name field of the SCIM Provider Resource Mapping \[sys\_scim\_provider\_resource\_mapping\] table.

</td></tr><tr><td>

resourceId

</td><td>

String

</td><td>

Required. Sys\_id of the resource saved in the ServiceNow instance \(the client\).Table: In the primary\_table field of the SCIM Provider Resource Mapping \[sys\_scim\_provider\_resource\_mapping\] table.

</td></tr></tbody>
</table><table id="id_wc2_2fl_btb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

message

</td><td>

If the **status** is SUCCESS, the endpoint returns the response body as defined by the REST [SCIM](../../../../../integrate/inbound-rest/concept/scim-api.md#) API.Data type: String

</td></tr><tr><td>

status

</td><td>

Status of the request.Possible values:

-   FAILURE
-   SUCCESS

Data type: String

</td></tr></tbody>
</table>The following example shows how to create a new user in the external service provider SNOW Provider.

```
var scimClient = new sn_auth.SCIM2Client(); 
var response = scimClient.provisionNew('SNOW Provider','User','f282abf03710200044e0bfc8bcbe5d12'); 
gs.info('response: ' + response);
```

Output:

```
// Example of successful response
{
  "status":"SUCCESS",
  "message":"{
    \"schemas\":[
      \"urn:ietf:params:scim:schemas:extension:servicenow:2.0:User\",
      \"urn:ietf:params:scim:schemas:core:2.0:User\"
    ],
    \"id\":\"f282abf03710200044e0bfc8bcbe5d12\",
    \"meta\":{
      \"resourceType\":\"User\",
      \"created\":\"2012-02-18T03:04:53Z\",
      \"lastModified\":\"2021-10-10T19:38:37Z\",
      \"location\":\"https://empiamsd1.service-now.com/api/now/scim/Users/f282abf03710200044e0bfc8bcbe5d12\"
    },
    \"userName\":\"tia.neumaier\",
    \"name\":{
      \"familyName\":\"Neumaier\",
      \"givenName\":\"Tia\"
    },
    \"displayName\":\"Tia Neumaier\",
    \"active\":true,
    \"emails\":[
      {
        \"value\":\"tia.neumaier@example.com\",
        \"type\":\"work\"
      }
    ],
    \"urn:ietf:params:scim:schemas:extension:servicenow:2.0:User\":{
      \"gender\":\"Female\",
      \"costCenter\":{
        \"value\":\"7fb1cc99c0a80a6d30c04574d14c0acf\",
        \"name\":\"Sales\",
        \"$ref\":\"https://empiamsd1.service-now.com/api/now/scim/CostCenters/7fb1cc99c0a80a6d30c04574d14c0acf\"
      },
      \"company\":{
        \"value\":\"227cdfb03710200044e0bfc8bcbe5d6b\",
        \"name\":\"ACME South America\",
        \"$ref\":\"https://empiamsd1.service-now.com/api/now/scim/Companies/227cdfb03710200044e0bfc8bcbe5d6b\"
      },
      \"department\":{
        \"value\":\"221db0edc611228401760aec06c9d929\",
        \"name\":\"Sales\",
        \"$ref\":\"https://empiamsd1.service-now.com/api/now/scim/Departments/221db0edc611228401760aec06c9d929\"
      },
      \"location\":{
        \"value\":\"25b4c23b0a0a0bb30054836629537509\",
        \"name\":\"Carretera Cancun-Chetumal KM 22, Cancun\",
        \"$ref\":\"https://empiamsd1.service-now.com/api/now/scim/Locations/25b4c23b0a0a0bb30054836629537509\"
      }
    }
  }"
}

// Example of failure response
{
  "status":"FAILURE",
  "message":"SCIM client attribute or provider resource mapping is not configured properly , 
  No provider resource mapping id found for provider name: SNOW Provider and resource name: User"
}
```

