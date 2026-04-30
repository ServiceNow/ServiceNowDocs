---
title: Configuring service definitions
description: Create service definitions for the types of services required to support your products. Associate different features such as case types, playbooks, and record producers with service definitions so that customers can request the services they need and agents can create cases of the right type to support those services.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Service definitions, Case management, Organize agent workspaces, Configuring Customer Service Management, Customer Service Management]
---

# Configuring service definitions

Create service definitions for the types of services required to support your products. Associate different features such as case types, playbooks, and record producers with service definitions so that customers can request the services they need and agents can create cases of the right type to support those services.

System administrators can use the service definitions feature to define the services that are offered to customers and connect those services to products, case types, playbooks, and catalog items.

|Task|Description|
|----|-----------|
|[Create a service definition](../task/create-csm-service-definition.md)|Create a definition for a service that's offered to support a product.|
|[Associate a product with a service definition](../task/service-def-associate-products.md)|Configure the relationship between a product and service.|
|[Associate a case type with a service definition](../task/service-def-associate-case-type.md)|A case type defines the case resolution process for a service definition.|
|[Associate a playbook with a service definition](../task/service-def-associate-playbook.md)|A playbook provides step-by-step guidance for resolving a specific type of case. Defining a playbook record generator view enables case creation for a requested service.|
|[Configure default field values for a service definition](../task/service-def-default-field-values.md)|Configure default values for fields in a service definition's target table. When a record is created for this table, the system uses these values to auto populate record fields.|
|[Configure catalog items for a service definition](../task/service-def-config-catalog-items.md)|End users can select a catalog item from the service portal and use the record producer to create the service request.|
|[Configure related services for a service definition](../task/service-def-config-related-services.md)|Associate one or more related services with a service definition to create parent-child relationships between service definitions. For example, you can create service definitions for case tasks and associate them with a service definition for a case type.|
|[Associate service organizations with a service](../task/associate-services-to-service-organization.md)|After creating a service definition, you can associate service organizations offering service with a service organization.|
|[Create a service definition category](../task/create-csm-service-def-category.md)|Create a category for service definitions. You can use these categories to create logical groupings of service definitions.|
|[Associate service definitions with a category](../task/service-def-category-associate-service.md)|Add service definitions to a category. A category can have one or more associated service definitions and a service definition can belong to multiple categories.|
|[Add a case type to the Case interceptor](../task/service-def-config-case-interceptor.md)|In the Core UI, the Case interceptor lists the types of customer service cases that an agent can create. If you create a case type and you want that case type to appear in the Case interceptor, you need to add it to the Case interceptor configuration.|

