---
title: Creating a source definition
description: Create a source definition to capture information about which identity source a resource is provisioned from.
locale: en-US
release: australia
product: Identity
classification: identity
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [SCIM Provider, System for Cross-domain Identity Management \(SCIM\), Identity]
---

# Creating a source definition

Create a source definition to capture information about which identity source a resource is provisioned from.

## Before you begin

Role required: scim\_config\_admin

**Warning:** Grant this role carefully. The scim\_config\_admin role is equivalent to giving the user the admin role, where the scim\_config\_admin can add or update Personally Identifiable Information \(PII\).

## About this task

Using a source definition, the provisioning identity source can be mapped to an OAuth entity using which it authenticates while provisioning.

After a source definition is created, all resources getting provisioned from that identity source is mapped to its corresponding source definition ID.

The source definition captures the required source information, such as by doing the following:

-   Identifies the SCIM Client from which the resource is provisioned.
-   Resolves duplicate information provided by the external ID:
    -   If multiple identity sources are provisioning resources, there can be two or more resources have the same external ID value because the external Id is only unique to the identity source.
    -   If multiple resources are returned with an external ID SCIM filter then the resources can be resolved based on the source definition of the requesting identity source.

**Note:** A source definition can be created only for the identity source, which, uses an OAuth authentication method.

## Procedure

1.  Navigate to **All** &gt; **SCIM** &gt; **Source Definition**.

2.  On the SCIM Source Definitions page, click **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the source definition.|
    |Application|Application scope for this record.|
    |OAuth Entity|The OAuth entity of the integration user. The entity is used for provisioning the user by the identity source provider.|
    |Identity Source|The name of the identity source provider. For example, Azure AD, Okta, and so on|

    **Note:** Enable the **com.snc.integration.scim2.resolve.externalid.conflict** property to return only SCIM resources created by the requesting identity source. By default, all the matching resources with an external ID filter are returned.

    ![SCIM Source Definition](../images/create-source-definition.png)

4.  Click **Submit**.


## Result

The SCIM source definition is created. Use the SCIM ETL Definitions to map the resources based on the extension schema on the sys\_user and sys\_user\_group table. For more information, see [Create a SCIM ETL definition](create-scim-etl-definitions.md).

