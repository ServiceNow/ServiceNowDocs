---
title: HR service configuration
description: HR services are the requests and assistance an HR organization provides its employees. You can configure an HR service to define the request to fulfillment process for that case type.
locale: en-US
release: yokohama
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [HR services, HR Administration, Case and Knowledge Management, HR Service Delivery, Employee Service Management]
---

# HR service configuration

HR services are the requests and assistance an HR organization provides its employees. You can configure an HR service to define the request to fulfillment process for that case type.

You can configure an HR case template to automatically populate fields on the HR case form when a request for that service is made. And if you need to make an existing HR service available for employee self-service, you can configure a record producer to make the service available as an HR catalog item in the HR service catalog.

For best results, do not configure multiple record producers to invoke a single HR service.

**Note:** The COEs available to you may differ depending on the HR package you have.

-   The categorization of HR catalog items are employee-facing only, and have no relation to the categorization of HR services under the HR Centers of Excellence \(COEs\) data model.
-   If you are creating a new HR service and plan to make it available for employee self-service, see [HR catalog item configuration](hr-catalog-item-configuration.md) instead. Creating a new HR catalog item automatically creates a corresponding HR service, and you can avoid creating duplicate services.
-   If you have an existing HR service that you want to make available for employee self-service, do not create an HR catalog item. \(Creating a HR catalog item automatically creates a corresponding HR service.\) Instead, see [Configure a record producer for an HR service](../task/configure-hr-record-producer.md) to add the existing service as an HR catalog item in the HR service catalog.
-   The Agent Workspace for HR Case Management is highly configurable for HR agents. It supports the same functionality in the Classic HR Service Delivery Agent Workspace.

1.  [Configure an HR service](../task/configure-hr-service.md)  
Create or modify an HR service to define the request to fulfillment process for that case type. Examples of HR services include benefits enrollment, direct deposit setup, and background check requests by third-party providers.
2.  [Configure an HR case template](../task/configure-hr-case-template.md)  
Create or modify an HR case template for an HR service to automatically populate fields on the HR case form when a request for that service is made.
3.  [Configure a record producer for an HR service](../task/configure-hr-record-producer.md)  
Make an existing HR service available for employee self-service by adding it to the HR service catalog.

**Parent Topic:**[HR services](hr-service-administration.md)

