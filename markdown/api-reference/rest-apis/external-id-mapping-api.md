---
title: External ID Mapping API
description: Enables external Contact Center as a Service \(CCaaS\) platforms to store and retrieve routing identifiers for ServiceNow records.Retrieves the external routing ID mapping for a specific record.Creates or updates an external routing ID mapping for a ServiceNow record.
locale: en-US
release: zurich
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2026-01-12"
reading_time_minutes: 7
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# External ID Mapping API

Enables external Contact Center as a Service \(CCaaS\) platforms to store and retrieve routing identifiers for ServiceNow records.

As part of the Contact Center Integration Core \(sn\_ct\_ctr\_it\_core\) store application, this API enables CCaaS providers to get or set external IDs in the CCaaS External ID Mappings \[sn\_ct\_ctr\_it\_core\_ccaas\_external\_id\_mapping\] table. This API is in the sn\_ct\_ctr\_it\_core namespace and requires the sn\_ct\_ctr\_it\_core.admin role.

This API supports multi-provider environments, enabling organizations to integrate with multiple CCaaS platforms simultaneously while maintaining separate routing ID namespaces for each provider.

When a CCaaS platform \(such as Genesys Cloud, Five9, or Amazon Connect\) routes a case, task, or interaction to an external agent, it generates a unique routing ID. This API provides a centralized mechanism to map those external routing IDs to records, enabling bidirectional tracking and correlation between the CCaaS platform and ServiceNow.

-   **External routing correlation**

    The CCaaS platform generates a routing ID when it routes a case to an external agent. must store this ID to correlate future events, callbacks, or status updates from the CCaaS platform.

    This API stores the external routing ID in a mapping table, associating it with the record and the provider that generated it.

-   **Bidirectional tracking**

    You might have to track which external routing session corresponds to which case for reporting, analytics, and troubleshooting.

    You can use this API to retrieve external routing IDs for any record, enabling dashboards and reports to show the complete routing history.

-   **Integration flexibility**

    Different CCaaS platforms might require storing routing IDs for different tables, such as cases, tasks, interactions, or custom tables.

    This API accepts any valid table name, making it extensible for future use cases. The endpoints can be called independently depending on the workflow.


For more information about integrating with CCaaS systems, see [Integrating with contact centers](https://www.servicenow.com/docs/access?context=contactcenter-integration&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US).

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## External ID Mapping - GET /sn\_ct\_ctr\_it\_core/external\_id\_mapping/table/\{tableName\}/documentId/\{documentId\}

Retrieves the external routing ID mapping for a specific record.

This endpoint queries the mapping table to find the external routing ID that has been stored for a given record and provider. Use this endpoint to retrieve the external routing ID that was assigned to a record by a CCaaS platform.

### URL format

Default URL: `/api/sn_ct_ctr_it_core/external_id_mapping/table/{tableName}/documentId/{documentId}`

### Supported request parameters

<table id="table_b4p_1vg_yhc" class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

tableName

</td><td>

Required. The ServiceNow table name containing the record. Can be any valid table name. For example, sn\_customerservice\_case, sn\_customerservice\_task, interaction, or custom tables.Data type: String

</td></tr><tr><td>

documentId

</td><td>

Required. The sys\_id of the ServiceNow record for which to retrieve the external ID mapping.Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table id="table_f4p_1vg_yhc" class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-entry-RESTAPI">

Data format of the response body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|400|Bad Request. A bad request type or malformed request was detected.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|403|Forbidden. The user doesn't have access rights to the specified record.|
|404|Not found. The requested item wasn't found.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON\)

<table id="table_k4p_1vg_yhc"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

Result object containing information about the request.Data type: Object

```
"result": { 
   "data": "String",
   "message": "String"
}
```

</td></tr><tr><td>

result.data

</td><td>

Data for the mapping.Data type: Object

```
"data": { 
  "document_id": "String", 
  "document_table": "String",
  "external_id": "String",
  "external_provider": "String"
}
```

</td></tr><tr><td>

result.data.document\_id

</td><td>

The sys\_id of the ServiceNow AI Platform record for which to retrieve the external ID mapping.Data type: String

</td></tr><tr><td>

result.data.document\_table

</td><td>

The ServiceNow AI Platform table name containing the record.Data type: String

</td></tr><tr><td>

result.data.external\_id

</td><td>

The external routing ID from the CCaaS platform.Max characters: 200

Data type: String

</td></tr><tr><td>

result.data.external\_provider

</td><td>

The sys\_id of the provider from the External Provider \[awa\_external\_provider\] table.Data type: String

</td></tr><tr><td>

result.error.message

</td><td>

If the request fails, message explaining why the request failed.Data type: String

</td></tr><tr><td>

result.error

</td><td>

If the request fails, message explaining why the request failed.Data type: String

</td></tr><tr><td>

result.error.message

</td><td>

If the request fails, message explaining why the request failed.Data type: String

</td></tr><tr><td>

result.message

</td><td id="message">

Message that describes the outcome of the API request.Data type: String

</td></tr><tr><td>

result.status

</td><td id="omni-response-result.status-entry">

Success or failure status of the request.Valid values:

-   success
-   failure

Data type: String

</td></tr></tbody>
</table>This example queries the mapping for case with sys\_id `f584a7b23b3d3e10c524c59a04e45a6f` to find which external routing ID has been assigned by the CCaaS platform.

```
curl "https://instance.service-now.com/api/sn_ct_ctr_it_core/external_id_mapping/table/sn_customerservice_case/documentId/f584a7b23b3d3e10c524c59a04e45a6f" \
--request GET \
--header "Accept:application/json" \
--user 'admin':'admin'
```

Response body:

```
{
  "result": {
    "data": {
      "document_table": "sn_customerservice_case",
      "document_id": "f584a7b23b3d3e10c524c59a04e45a6f",
      "external_id": "200",
      "external_provider": "8b592fb64f140210c0338ef0b1ce0b18"
    }
  }
}
```

## External ID Mapping - PUT /sn\_ct\_ctr\_it\_core/external\_id\_mapping/table/\{tableName\}/documentId/\{documentId\}

Creates or updates an external routing ID mapping for a ServiceNow record.

This endpoint is idempotent, so calling it multiple times with the same parameter updates the existing mapping rather than creating duplicate mappings. The endpoint automatically determines whether to insert a new mapping or update an existing one based on the combination of table name, document ID, and external provider.

### URL format

Default URL: `/api/sn_ct_ctr_it_core/external_id_mapping/table/{tableName}/documentId/{documentId}`

### Supported request parameters

<table id="table_fgq_r2t_c3c" class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

tableName

</td><td>

Required. The ServiceNow table name containing the record. Can be any valid table name. For example, sn\_customerservice\_case, sn\_customerservice\_task, interaction, or custom tables.Data type: String

</td></tr><tr><td>

documentId

</td><td>

Required. The sys\_id of the ServiceNow record for which to retrieve the external ID mapping.Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

<table id="table_hgq_r2t_c3c" class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

external\_id

</td><td>

Required. External agent ID from the CCaaS system.Data type: String

Maximum length: 200 characters

</td></tr><tr><td>

external\_provider

</td><td>

The sys\_id of the provider record from the External Provider \[awa\_external\_provider\] table. This identifies which CCaaS platform generated the external ID.Data type: String

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Only supports **application/json**.|
|Content-Type|Data format of the request body. Only supports **application/json**.|

|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

<table id="table_mgq_r2t_c3c"><thead><tr><th>

Status code

</th><th>

Description

</th></tr></thead><tbody><tr><td>

200

</td><td id="entry-200-status-code">

Successful. The request was successfully processed.

</td></tr><tr><td>

201

</td><td>

Created. The external ID mapping was successfully created, that is, a new mapping was inserted.

</td></tr><tr><td>

400

</td><td id="entry-400-status-code">

Bad Request. A bad request type or malformed request was detected.

</td></tr><tr><td>

401

</td><td id="entry-401-status-code">

Unauthorized. The user credentials are incorrect or have not been passed.

</td></tr><tr><td>

403

</td><td id="entry-403-status-code-awa">

Forbidden.Possible reasons:

-   The user doesn't have the awa\_integration\_user role.
-   The value of the glide.awa.enabled property isn't `true`. This property is listed in the System Property \[sys\_property\] table if the Advanced Work Assignment \(com.glide.awa\) plugin is installed. For more information, see [Components installed with Advanced Work Assignment](https://www.servicenow.com/docs/access?context=installed-with-awa&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US).

</td></tr><tr><td>

404

</td><td id="entry-404-status-code">

Not found. The requested item wasn't found.

</td></tr><tr><td>

500

</td><td id="entry-500-status-code">

Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.

</td></tr></tbody>
</table>### Response body parameters \(JSON\)

<table id="table_ogq_r2t_c3c"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

Result object containing information about the request.Data type: Object

```
"result": { 
   "data": "String",
   "message": "String"
}
```

</td></tr><tr><td>

result.error.message

</td><td>

If the request fails, message explaining why the request failed.Data type: String

</td></tr><tr><td>

result.error

</td><td>

If the request fails, message explaining why the request failed.Data type: String

</td></tr><tr><td>

result.error.message

</td><td>

If the request fails, message explaining why the request failed.Data type: String

</td></tr><tr><td>

result.message

</td><td id="message">

Message that describes the outcome of the API request.Data type: String

</td></tr><tr><td>

result.status

</td><td id="omni-response-result.status-entry">

Success or failure status of the request.Valid values:

-   success
-   failure

Data type: String

</td></tr></tbody>
</table>### cURL request

This example shows how to store an external ID from a CCaaS platform \(identified by provider sys\_id `8b592fb64f140210c0338ef0b1ce0b18`\).

```
curl "https://instance.service-now.com/api/sn_ct_ctr_it_core/external_id_mapping/table/sn_customerservice_case/documentId/f584a7b23b3d3e10c524c59a04e45a6f" \
--request PUT \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
    \"external_id\": \"200\",
    \"external_provider\": \"8b592fb64f140210c0338ef0b1ce0b18\"
}" \
--user 'admin':'admin'
```

Response body:

```
{
  "result": {
    "message": "External ID mapping record updated for sn_customerservice_case [f584a7b23b3d3e10c524c59a04e45a6f]",
    "status": "success"
  }
}
```

