---
title: Configuring Service Exchange Order Management for Providers
description: Configure the Service Exchange Order Management for Providers application, which enables providers to use Order Management to create and fulfill product orders over Service Exchange. Providers publish the product offerings and service specifications as remote catalog items so that consumers can order from the Service Catalog on their own instance.
locale: en-US
release: yokohama
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Order Management for providers with Service Exchange, Extending Order Management with ServiceNow applications and integrations, Sales Customer Relationship Management]
---

# Configuring Service Exchange Order Management for Providers

Configure the Service Exchange Order Management for Providers application, which enables providers to use Order Management to create and fulfill product orders over Service Exchange. Providers publish the product offerings and service specifications as remote catalog items so that consumers can order from the Service Catalog on their own instance.

## Configuration overview

Follow these tasks to set up the Service Exchange Order Management for Providers application, which uses Order Management to create product offerings and service specification and publish them ServiceNow in your provider instance as remote record producers. Service Exchange admins can then activate these remote record producers to make the products and services available from the Service Catalog on consumer instances.

<table id="table_n2l_dcy_qxb"><thead><tr><th>

Configuration step

</th><th>

Description

</th><th>

Role

</th></tr></thead><tbody><tr><td>

[Install Service Exchange for Providers](https://www.servicenow.com/docs/access?context=install-service-bridge-v2-provider&version=yokohama&pubname=yokohama-service-bridge&ft:locale=en-US)

</td><td>

Install the Service Exchange for Providers application from the ServiceNow Store. For more information on configuring this application, see [Installing and configuring Service Exchange for Providers](https://www.servicenow.com/docs/access?context=service-bridge-v2-configure-provider&version=yokohama&pubname=yokohama-service-bridge&ft:locale=en-US).

</td><td>

Admin

</td></tr><tr><td>

[Install Service Exchange for Consumers](https://www.servicenow.com/docs/access?context=install-service-bridge-v2-customer&version=yokohama&pubname=yokohama-service-bridge&ft:locale=en-US)

</td><td>

Install the Service Exchange for Consumers application from theServiceNow Store. For details on configuring this application, see[Install Service Exchange for Consumers](https://www.servicenow.com/docs/access?context=install-service-bridge-v2-customer&version=yokohama&pubname=yokohama-service-bridge&ft:locale=en-US) .

</td><td>

Admin

</td></tr><tr><td>

[Install Service Exchange Order Management for Providers](../task/install-service-bridge-om-providers.md)

</td><td>

Install the Service Exchange Order Management for Providers application from the ServiceNow Store.

</td><td>

Admin

</td></tr><tr><td>

[Create a product offering for a remote catalog item](../task/create-sb-product-offerings.md)

</td><td>

In the provider instance, create the product offerings to be added as remote catalog item to the service catalog for your consumers.

</td><td>

Product catalog admin or manager

</td></tr><tr><td>

[Create a service specification for a remote catalog item](../task/create-sb-service-specs.md)

</td><td>

In the provider instance, create the service specification for a service to be added as a remote catalog item to the service catalog for your consumers.

</td><td>

Product catalog admin or manager

</td></tr><tr><td>

[Associate consumer criteria to a remote record producer](../task/associate-criteria-remote-catalog.md)

</td><td>

In the provider instance, review the remote record producer and associate the customer criteria that entitles the catalog item for eligible Service Exchange consumers.

</td><td>

Service Exchange provider admin

</td></tr><tr><td>

Associate consumer criteria to the remote record producer for manage inventory.

</td><td>

Review the remote record producer for manage inventory and associate the customer criteria.

</td><td>

 

</td></tr><tr><td>

[Activate the remote record producer](../task/activate-entitlements-sb-consumer.md)

</td><td>

In the consumer instance, activate entitlements for the remote record producers.

</td><td>

Service Exchange consumer admin

</td></tr><tr><td>

[Retire a remote catalog item](../task/retire-product-offer.md)

</td><td>

Retire a product offering or service specification used in a remote catalog, which automatically retires the corresponding remote record producer and removes the item from the service catalog on the consumer instance.

</td><td>

Product catalog admin or manager

</td></tr></tbody>
</table>