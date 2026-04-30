---
title: Configure the default behavior to request items for other users
description: Define the default behavior when no roles are specified in the glide.sc.req\_for.roles property.
locale: en-US
release: xanadu
product: Service Catalog
classification: service-catalog
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Delegated request experience, Configuring Service Catalog, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Configure the default behavior to request items for other users

Define the default behavior when no roles are specified in the **glide.sc.req\_for.roles** property.

## Before you begin

Role required: admin

## About this task

The **glide.sc.req\_for.roles** property specifies the list of roles who can request items for other users. When no roles are specified, then the default behavior is defined by the **glide.sc.req\_for.roles.default** property. For information about the **glide.sc.req\_for.roles** property, see [Service Catalog properties](../reference/r_ServiceCatalogProperties.md).

Following are the possible values for the **glide.sc.req\_for.roles.default** property.

-   When the property is set to `allow`, then any user can request items for other users.
-   When the property is set to `deny`, then no user can request items for other users.

The value of the **glide.sc.req\_for.roles.default** property is considered as `allow` in any of the following scenarios and any user can request an item for other users:

-   The **glide.sc.req\_for.roles.default** property is not defined.
-   The value of the **glide.sc.req\_for.roles.default** property is empty, `allow`, or any string other than `deny`.


A user with the admin role can request an item for other users. In this case, values of both the properties, glide.sc.req\_for.roles and glide.sc.req\_for.roles.default, are not considered.

For zBoot customers, the **glide.sc.req\_for.roles.default** property is available in the base system with the default value as `deny`. Upgrade customers can add and modify the property if required.

## Procedure

1.  Navigate to sys\_properties.list.

2.  Select the **glide.sc.req\_for.roles.default** property.

3.  On the System Property form, in the **Value** field, specify the value.

4.  Click **Update**.


**Parent Topic:**[Delegated request experience](../concept/delegated-request-exp.md)

