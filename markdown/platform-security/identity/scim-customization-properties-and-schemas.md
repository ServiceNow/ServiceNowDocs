---
title: SCIM customization properties and schemas
description: The SCIM customization includes the following properties, supported schemas, and unsupported schemas.
locale: en-US
release: zurich
product: Identity
classification: identity
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [SCIM customization, SCIM Provider, System for Cross-domain Identity Management \(SCIM\), Identity]
---

# SCIM customization properties and schemas

The SCIM customization includes the following properties, supported schemas, and unsupported schemas.

## Properties

SCIM customization adds the following system properties.

<table id="table_zyl_dyx_ctb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**com.snc.integration.scim2.max.member.count**

</td><td>

The SCIM maximum member count.

</td></tr><tr><td>

**com.snc.integration.scim2.resolve.externalid.conflict**

</td><td>

Resolve SCIM resources based on the source definition of the requesting client if multiple resources are found with an external ID SCIM filter.**Note:** As a prerequisite, if provisioning is done from multiple sources, then the sources must be defined in the SCIM Source Definition table. If sources are not defined or if this property is inactive, then all matching resources are returned with an external Id filter response.

</td></tr><tr><td>

**com.snc.integration.scim2.user.etl.definition.id**

</td><td>

The SCIM User ETL Definition ID.

</td></tr><tr><td>

**com.snc.integration.scim2.group.etl.definition.id**

</td><td>

The SCIM Group ETL Definition ID.

</td></tr><tr><td>

**com.snc.integration.scim2.rte.verbose.logging.enabled**

</td><td>

Enables verbose logging for SCIM User and Group RTE definitions.

</td></tr><tr><td>

**com.snc.integration.scim2.string.field.length.validation.enabled**

</td><td>

The length validation for fields. This property enables validation instead of truncating and saving the field.

</td></tr><tr><td>

**com.snc.integration.scim2.provider.customization.script.id**

</td><td>

The ID of the script include for customizing the SCIM responses.

</td></tr></tbody>
</table>## Supported schemas

SCIM customization adds the following supported schemas.

|Schemas|Description|Prefix|Example|
|-------|-----------|------|-------|
|**urn:ietf:params:scim:schemas:core:2.0:User**|Includes core attributes for the resources.|none|name.middleName|
|**urn:ietf:params:scim:schemas:extension:servicenow:2.0:User**|Includes attributes that are related to ServiceNow.|servicenow|servicenow.manager.value|
|**urn:ietf:params:scim:schemas:extension:servicenow:custom:2.0:User**|Includes custom attributes that are not mapped as part of the core extension or  the ServiceNow extension schema.|custom|custom.socialId|

## Unsupported schema

**urn:ietf:params:scim:schemas:extension:enterprise:2.0:User**: Includes attributes commonly used in representing users that belong to or act on behalf of a business or an enterprise.

**Note:** Enterprise schema is a valid schema but its attributes are mapped to any table. Because database persistence is not supported, there will be no error displayed if an enterprise schema is included in the request body.

