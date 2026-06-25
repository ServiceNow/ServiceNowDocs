---
title: Configure product model and catalog item relationships
description: Enable customers to request services for the products that they own. Create definitions for the services that support your products and then configure service definitions to associate them with the appropriate products and catalog items.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/create-csm-product-model-items.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Product models, Configure product data, Product data, Set up your environment, Configure, Customer Service Management]
---

# Configure product model and catalog item relationships

Enable customers to request services for the products that they own. Create definitions for the services that support your products and then configure service definitions to associate them with the appropriate products and catalog items.

## Before you begin

Role required: sn\_csm\_case\_types.service\_definition\_manager, sn\_csm\_case\_types.service\_definition\_admin, or admin

## About this task

Use the [Service definitions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/csm-service-definitions.md) feature to create definitions for the services that are offered to support your products. This feature is available with the [Customer service case types](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/customer-service-case-types.md) plugin.

From the Customer and Consumer Portals, end users can select available services from the [Services portal widget](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/csm-service-definitions.md). Selecting a service displays the record producer associated with the service definition. Submitting the record producer creates a case of the correct case type.

## Procedure

1.  [Create a service definition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/create-csm-service-definition.md).

2.  [Associate a product with a service definition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/service-def-associate-products.md).

3.  [Associate one or more catalog items with a service definition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/service-def-config-catalog-items.md).


**Related topics**  


[View product information from the Customer Service Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/view-product-info-csp.md)

