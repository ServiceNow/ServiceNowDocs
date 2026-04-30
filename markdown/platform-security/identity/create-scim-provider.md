---
title: Create a SCIM Provider
description: Create a SCIM Provider to fetch resource types and schemas information from the SCIM Provider with the REST message. Enable the configuration of the HTTP Method \(PUT or PATCH\) to update a resource in the SCIM Provider.
locale: en-US
release: zurich
product: Identity
classification: identity
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [SCIM Client, System for Cross-domain Identity Management \(SCIM\), Identity]
---

# Create a SCIM Provider

Create a SCIM Provider to fetch resource types and schemas information from the SCIM Provider with the REST message. Enable the configuration of the HTTP Method \(PUT or PATCH\) to update a resource in the SCIM Provider.

## Before you begin

**Note:** A sample SCIM Provider is part of the base system. You can use and configure based on your requirement, or create a new record.

Roles required: admin

## Procedure

1.  Navigate to **All** &gt; **SCIM Client** &gt; **SCIM Provider**.

2.  In the SCIM Providers page, click **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the SCIM Provider|
    |Outbound REST Message|Message that is used to call the API of the SCIM Provider. For more information, see [Create a REST message](create-a-rest-message.md).|
    |HTTP Method for Update|Type of HTTPS method that is used for updating the resource mapping. The PATCH or PUT method can be used by the Client while updating the identity resource during the provision of an already existing resource.|

    **Note:**

    -   The **Resource Definition** and **Schema Field Definition** fields are fetched from the **/ResourceTypes** and **/Schemas** public endpoints of the SCIM Provider. These fields are auto-populated after the rest message is selected.
    -   If the REST message, Schemas, or the Resource Types are updated on the SCIM Provider, then click **Refresh** and then **Update** to update the **Resource Definition** and **Schema Field Definition** fields.
    ![SCIM Provider page](../images/scim-provider-page.png)

4.  Click **Submit**.


## Result

The SCIM Provider details are created successfully. Use the SCIM Provider Resource Mapping to map the SCIM Provider details to the resources such as users or groups. For more information, see [Create a SCIM Provider Resource Mapping](scim-provider-resource-mapping.md).

