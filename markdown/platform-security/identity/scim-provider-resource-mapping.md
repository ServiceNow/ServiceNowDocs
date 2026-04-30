---
title: Create a SCIM Provider Resource Mapping
description: Define the mappings of SCIM attributes to ServiceNow attributes for a particular resource type and SCIM Provider.
locale: en-US
release: yokohama
product: Identity
classification: identity
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [SCIM Client, System for Cross-domain Identity Management \(SCIM\), Identity]
---

# Create a SCIM Provider Resource Mapping

Define the mappings of SCIM attributes to ServiceNow attributes for a particular resource type and SCIM Provider.

## Before you begin

Roles required: admin

## Procedure

1.  Navigate to **All** &gt; **SCIM Client** &gt; **SCIM Provider Resource Mapping**.

    The SCIM Provider Resource Mapping is shipped with the User and Group mapping by default.

    **Note:** The User or Group mappings contains sample mappings, which you can use as a reference. You can also create mapping based on the user or group resources.

    ![SCIM Provider Resource Mapping](../images/scim-provider-resource-mapping.png)

2.  Create a resource mapping by clicking **New**.

3.  On the form, fill in the fields.

    |Fields|Description|
    |------|-----------|
    |Provider|Name of the SCIM Provider. Refer to the configured Provider name when creating a SCIM Provider.|
    |Resource Name|Resource for which the mapping must be defined.|
    |Primary Table|The table that contains the sys\_id of the resource being mapped.|

    ![SCIM Provider Resource Mapping - New record](../images/resource-mapping-group.png)

4.  Click **Submit**.


## Result

The record is created and displayed in the SCIM Provider Resource Mapping page. Use the SCIM Attribute Mappings to further map the attributes from schemas. For more information, see [Create a SCIM attribute mapping](create-scim-attribute-mappings.md).

