---
title: Basic trust configuration for data sync applications
description: Certain ServiceNow applications have the ability to provide data visibility across instances within a customer’s account.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure, Multi-instance Management, Get started, Administer]
---

# Basic trust configuration for data sync applications

Certain ServiceNow applications have the ability to provide data visibility across instances within a customer’s account.

Data visibility is protected by a trust configuration per instance, per application. You can configure the data sharing for production and non-production instances for the applicable applications by navigating to **All** &gt; **Multi-Instance Management** &gt; **Trust Configuration**.

**Note:**

By default, non-production instances allow application data sharing with production only. Production instances do not allow application data sharing with any other instance. However, these can be updated by the admin for each instance based on business needs.

If you demote a production instance to non-production, or promote a non-production instance to production, all previous customizations to data sharing settings are reset to the default configuration.

The **Grant access** column indicates the permission granted by the instance that you’re currently logged in to for the instance named in the same row’s instance column. The **Is granting access** column displays whether or not the instance mentioned in the Instance column has granted access to the instance you’re currently logged in to; it can’t be edited.

The following are some examples for data sharing restrictions between instances.

## Logged in to Prod1

In the following example, you’re logged in to Prod1. Prod1 has granted access to the instance Prod2 for the application Subscription Management, as indicated by the `True` value in the **Grant access** column.

Prod2 hasn’t granted access to Prod1, as indicated by the `False` value in the **Is granting access** column.

![The configurations in the MIF table.](../image/eg-1.png)

To revoke access for the Subscription Management app from Prod1 to Prod2, update the value in the **Grant access** column to `False` while logged in to Prod1.

## Logged in to Prod2

In the following example, you’re logged in to Prod2. Prod1 has granted access to the instance Prod2 for the application Subscription Management, as indicated by the `True` value in the **Is granting access** column.

Prod2 hasn’t granted access to Prod1, as indicated by the `False` value in the **Grant access** column.

![The configurations in the MIF table.](../image/eg-2.png)

To grant access from Prod2 to Prod1 for the Subscription Management application, update the value in the **Grant access** column to `True` while logged in to Prod2.

## Logged in to Sub-prod2

In the following example, you’re logged in to Sub-prod2. Prod1 hasn’t granted access to the instance Sub-prod2 for the application Subscription Management, as indicated by the `False` value in the **Is granting access** column.

Sub-prod2 has granted access to Prod1, as indicated by the `True` value in the **Grant access** column.

![The configurations in the MIF table.](../image/eg-3.png)

To revoke access from Sub-prod2 to Prod1 for the Subscription Management application, update the value in the **Grant access** column to `True` while logged in to Sub-prod2.

## Logged in to Sub-prod3

In the following example, you’re logged in to Sub-prod3. Sub-prod4 has granted access to the instance Sub-prod3 for the application Subscription Management, as indicated by the `True` value in the **Is granting access** column. Sub-prod3 has also granted access to Sub-prod4, as indicated by the `True` value in the **Grant access** column.

![The configurations in the MIF table.](../image/eg-4.png)

**Parent Topic:**[Configuring Multi-instance Management](data-sync-configure.md)

