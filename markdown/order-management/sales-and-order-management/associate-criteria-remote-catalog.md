---
title: Associate consumer criteria to a remote record producer
description: In the provider instance, associate the appropriate consumer criteria to the remote record producer created for a remote catalog item. The consumer criteria determines which consumers are entitled to the catalog item. Service Exchange automatically generates the entitlement records that are replicated to eligible consumer instances.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configuring Service Exchange Order Management for Providers, Order Management for providers with Service Exchange, Integrate, Sales Customer Relationship Management]
---

# Associate consumer criteria to a remote record producer

In the provider instance, associate the appropriate consumer criteria to the remote record producer created for a remote catalog item. The consumer criteria determines which consumers are entitled to the catalog item. Service Exchange automatically generates the entitlement records that are replicated to eligible consumer instances.

## Before you begin

By default remote record producers are available to all consumers. If you have specific criteria for certain users, define the consumer criteria for Service Exchange those users. For more information, see [Creating entitlements in Service Exchange for Providers](https://www.servicenow.com/docs/access?context=service-bridge-v2-entitlements&version=zurich&pubname=zurich-service-bridge&ft:locale=en-US).

Role required: sn\_sb.Admin or admin

## Procedure

1.  In your provider instance, navigate to **All** &gt; **Service Bridge Provider** &gt; **Administration** &gt; **Remote Catalog Items**.

2.  Select the remote record producer for the product offering or service specification that your product catalog admin or manager created.

    Review the record to validate that it was created as expected.

    **Note:** A remote record producer, Manage Inventory, is created automatically when a product offering or service specification for a remote catalog item is published. You must associate the consumer criteria to this remote record producer so that your consumers can manage the product or service inventory from the service catalog on a consumer instance.

3.  Navigate to the **Consumer Criterias** tab.

4.  In the record for the Active criteria, under the **Remote consumer criteria** column, select and save the criteria to be associated to the catalog item.

5.  Select **Publish**.

    Service Exchange automatically generates the entitlement records that are replicated to eligible consumer instances.


## What to do next

[Activate the entitlements for the remote record producer.](activate-entitlements-sb-consumer.md)

