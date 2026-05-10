---
title: Product data
description: Product data in the CRM portfolio gives agents, customers, and sales teams a shared view of what has been sold, how it has been deployed, and what service coverage applies.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-04-28"
reading_time_minutes: 3
---

# Product data

Product data in the CRM portfolio gives agents, customers, and sales teams a shared view of what has been sold, how it has been deployed, and what service coverage applies.

## Product data overview

When an agent opens a case, the product data associated with the customer's account tells them exactly what products are in scope, how they are installed, and what the customer is entitled to. Product data is part of the shared CRM data foundation and data model and is available across Sales CRM, FSM, CSM, and industry solutions without duplication or manual synchronisation.

Product data is part of the shared data foundation of the CRM portfolio. It connects what an organization sells to cases, work orders, and service requests raised against those products. This connection is what allows agents, technicians, and sales teams to work from a consistent view of the customer's product landscape at every stage of the customer lifecycle.

## Product data entities

The following entities make up the product data model.

|Entity|What it represents|How it is used|
|------|------------------|--------------|
|Product model|A type of good or service that your organization sells and supports like hardware, software, a service, or a consumable.|Product models are the catalog of what your organization offers. They can be associated with service offerings that customers can request, and are referenced by sold products when a product is sold.|
|Sold product|A specific product or service that has been sold to an account or consumer.|Records what a customer has purchased. Supports a hierarchical structure and can be associated with contracts and entitlements. Cases can be linked directly to a sold product when an issue arises.|
|Install base item|An instance of a product that has been installed or provisioned for a customer.|Tracks the deployed state of a customer's products. Available to agents and technicians when resolving issues. For SaaS products, represents the application service configuration item.|
|Installed product|The association between a sold product and one or more install base items.|Captures how a sold product has been deployed. A single sold product can have multiple installed product records across different locations or instances.|

## Product data and service delivery

When a case is opened, an agent can identify the specific sold product or install base item affected, connecting the service request directly to the relevant product context. Install base items created by Sales CRM fulfillment flows are immediately visible in CSM, and field technicians dispatched through FSM carry the same product context on their work orders.

## Assets and service coverage

Assets, service contracts, and entitlements extend product data into service coverage. An asset is a specific product instance supported for an account or consumer. Service contracts define the type of support a customer receives, while entitlements specify the level of support, supported channels, and SLA terms, giving agents immediate visibility into what a customer is covered for when a case is opened.

## Product data across CRM and Industries

Product data is a foundational layer of the CRM portfolio. It is the mechanism through which what a customer has purchased becomes visible and actionable across every CRM product and industry solution.

|Product|How data is used|
|-------|----------------|
|CSM|Agents use sold products and install base items to identify what is affected when a case is opened. Entitlements derived from the product and contract data determine the SLA applied to the case automatically.|
|Sales CRM|Order fulfillment creates sold products and install base items that are immediately available in CSM.|
|FSM|Field technicians dispatched through FSM carry the same product context - sold products, install base items, and assets on their work orders, giving them full visibility into what is deployed at a customer site before they arrive.|
|Industry solutions|Industry solutions such as Telecommunications, Manufacturing Commercial Operations, and Financial Services Operations extend the core product data model with industry-specific structures. Telecom organizations use install base items to represent network services and configurations. Manufacturers use them to track equipment deployed at customer sites. Financial services organizations use sold products to represent financial products and accounts under service.|

**Related topics**  


[Data models](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/data-models.md)

[Product models](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/product-models.md)

[Create service contracts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/create-csm-service-contracts.md)

[Configure entitlements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/configure-csm-entitlements.md)

[Configure install base](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/configure-install-base.md)

