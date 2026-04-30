---
title: SCIM customization
description: Customize SCIM protocols for your identity management.
locale: en-US
release: yokohama
product: Identity
classification: identity
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [SCIM Provider, System for Cross-domain Identity Management \(SCIM\), Identity]
---

# SCIM customization

Customize SCIM protocols for your identity management.

SCIM customization enables you to do the following:

-   Support custom fields on the sys\_user and sys\_user\_group tables through dynamic extension schema generation.
-   Provide an ability to override the default SCIM mappings.

A SCIM admin can define custom extension schemas for user and group resources. The attributes defined in the custom extension schema can be mapped to fields in the sys\_user or sys\_user\_group tables.

## Configurations for SCIM customization

For SCIM customization, you should perform the following tasks:

-   Define a custom extension schema for users and groups in the SCIM Extension schema table.  For more information see, [Create a SCIM Extension schema](../task/create-scim-extension-schemas.md).
-   Create entities in an ETL definition for custom schema attributes. The entities are created for the target table that is mapped with either the sys\_user or sys\_user\_group attributes. For more information see, [Create a SCIM ETL definition](../task/create-scim-etl-definitions.md).
-   Create an RTE mapping between these two entities.  For more information see, step [5](../task/create-scim-etl-definitions.md#RTEMapping) in the [Create a SCIM ETL definition](../task/create-scim-etl-definitions.md).
-   Send custom schema attributes with data in the SCIM API request payload.

The SCIM API calls the RTE engine with the defined mapping. The data is stored in the respective fields in the target table as defined in the mapping.

