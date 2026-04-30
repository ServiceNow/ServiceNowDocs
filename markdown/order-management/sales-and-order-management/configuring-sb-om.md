---
title: Configuring Service Exchange Order Management for Providers
description: Configure the Service Exchange Order Management for Providers application, which enables providers to use Order Management to create and fulfill product orders over Service Exchange. Providers publish the product offerings and service specifications as remote catalog items so that consumers can order from the Service Catalog on their own instance.
locale: en-US
release: xanadu
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2024-09-06"
reading_time_minutes: 3
breadcrumb: [Order Management for providers with Service Exchange, Extending Order Management with ServiceNow applications and integrations, Sales Customer Relationship Management]
---

# Configuring Service Exchange Order Management for Providers

Configure the Service Exchange Order Management for Providers application, which enables providers to use Order Management to create and fulfill product orders over Service Exchange. Providers publish the product offerings and service specifications as remote catalog items so that consumers can order from the Service Catalog on their own instance.

## Configuration overview

Follow these tasks to set up the Service Exchange Order Management for Providers application, which uses Order Management to create product offerings and service specifications and publish them in your ServiceNow provider instance as remote record producers. Service Bridge admins can then activate these remote record producers to make the products and services available from the Service Catalog on consumer instances.

|Configuration step|Description|Role|
|------------------|-----------|----|
|[Install Service Exchange for Providers](https://www.servicenow.com/docs/access?context=install-service-bridge-v2-provider&version=xanadu&pubname=xanadu-service-bridge&ft:locale=en-US)|Install the Service Exchange for Providers application from the ServiceNow Store. For more information on configuring this application, see [Installing and configuring Service Exchange for Providers](https://www.servicenow.com/docs/access?context=service-bridge-v2-configure-provider&version=xanadu&pubname=xanadu-service-bridge&ft:locale=en-US).|Admin|
|[Install Service Exchange for Consumers](https://www.servicenow.com/docs/access?context=install-service-bridge-v2-customer&version=xanadu&pubname=xanadu-service-bridge&ft:locale=en-US)|Install theService Exchange for Consumers application from the ServiceNow Store. For details on configuring this application, see [Installing and configuring Service Exchange for Consumers](https://www.servicenow.com/docs/access?context=service-bridge-v2-install&version=xanadu&pubname=xanadu-service-bridge&ft:locale=en-US).|Admin|
|[Install Service Exchange Order Management for Providers](../task/install-service-bridge-om-providers.md)|Install the Service Exchange Order Management for Providers application from the ServiceNow Store.|Admin|
|[Create a product offering for a remote catalog item](../task/create-sb-product-offerings.md)|In the provider instance, create the product offerings to be added as remote catalog items to the service catalog for your consumers.|Product catalog admin or manager|
|[Create a service specification for a remote catalog item](../task/create-sb-service-specs.md)|In the provider instance, create the service specification for a service to be added as a remote catalog item to the service catalog for your consumers.|Product catalog admin or manager|
|[Associate consumer criteria to a remote record producer](../task/associate-criteria-remote-catalog.md)|In the provider instance, review the remote record producer and associate the customer criteria that entitles the catalog item for eligible Service Exchange consumers.|Service Exchange provider admin|
|[Activate the remote record producer](../task/activate-entitlements-sb-consumer.md)|In the consumer instance, activate entitlements for the remote record producers.|Service Exchange consumer admin|
|[Retire a remote catalog item](../task/retire-product-offer.md)|Retire a product offering or service specification used in a remote catalog, which automatically retires the corresponding remote record producer and removes the item from the service catalog on the consumer instance.|Product catalog admin or manager|

