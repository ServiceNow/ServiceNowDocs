---
title: Create a SCIM Extension schema
description: Create custom attributes to map to fields that are not mapped as part of either the core schema or the ServiceNow extension schema.
locale: en-US
release: yokohama
product: Identity
classification: identity
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [SCIM customization, SCIM Provider, System for Cross-domain Identity Management \(SCIM\), Identity]
---

# Create a SCIM Extension schema

Create custom attributes to map to fields that are not mapped as part of either the core schema or the ServiceNow extension schema.

## Before you begin

Role required: scim\_admin

**Warning:** Grant this role carefully. The scim\_admin role is equivalent to giving the user the admin role, where the scmin\_admin role can insert new records into the tables that can bypass business logic or ACL protection.

## Procedure

1.  Navigate to **All** &gt; **SCIM** &gt; **SCIM Extension schemas**.

2.  Click **New**.

3.  On the form, fill in the fields.

    **Note:** Only one extension schema can be mapped to the **Resource Type** field. For example, User as a resource type can be mapped to a user extension schema.

<table id="table_z3g_llg_btb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the extension schema.

</td></tr><tr><td>

Active

</td><td>

Option to activate the schema. Select this field if the record must be considered as custom extension schema. Only one custom extension schema record can be active at a time for a specific resource type, whether for the User or Group type.

</td></tr><tr><td>

Resource Type

</td><td>

Resource type that has to be mapped to the extension schema. The following are the options:-   **User**
-   **Group**


</td></tr><tr><td>

Application

</td><td>

Application scope for this record.

</td></tr><tr><td>

Schema JSON

</td><td>

Details within the JSON schemas. For more information about defining the extension schema with attributes, see [Datatracker](https://datatracker.ietf.org/doc/html/rfc7643#section-7).

</td></tr></tbody>
</table>    ![SCIM Extension schema](../images/scim-extension-schemas.png)

4.  Validate the attributes by clicking **Validate**.

5.  Click **Submit**.


## Result

The extension schema with custom attributes related to User or Group resource type is created. Use the SCIM ETL Definitions to map the resources based on the extension schema on the sys\_user and sys\_user\_group table. For more information, see [Create a SCIM ETL definition](create-scim-etl-definitions.md).

