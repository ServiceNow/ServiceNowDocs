---
title: Service definitions
description: Use service definitions to create connections between products, services, and case types. Customers can use these definitions to quickly discover and request the services they need. Agents can use these definitions to create cases of the correct type to support those service requests.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 11
breadcrumb: [Case management, Organize agent workspaces, Configure, Customer Service Management]
---

# Service definitions

Use service definitions to create connections between products, services, and case types. Customers can use these definitions to quickly discover and request the services they need. Agents can use these definitions to create cases of the correct type to support those service requests.

## Overview of service definitions

The service definitions feature is available with the Customer Service Case Types plugin \(com.snc.csm\_case\_types\). [Case types](customer-service-case-types.md) enable you to address specific types of customer requests. A case type extends the base customer service case and includes the processes, attributes, and data required to resolve a specific type of case, such as onboarding a customer or resolving a complaint.

**Note:** Ensure that you are assigned to the service\_definition\_admin role

A service definition describes a service that a business or organization offers to support a product or service that they sell. Service definitions work with case types to provide different types of service requests.

-   You can create connections between products and services and the case types that support those services. These connections streamline the case management process for requesting and executing services and simplify service requests based on the customer's context.
-   You can also create service definitions for case task types and then create parent-child relationships between case type definitions and case task type definitions. This enables agents to easily create case tasks of the correct type.
-   You can create categories of services and then organize service definitions into logical groupings. Agents can use these categories to quickly find the services they need.

## Service definition benefits

When you create service definitions for each of the services that you offer, agents can use the defined services to create cases and cases tasks of the correct type for customer issues and requests. When creating these cases and case tasks, agents can do the following:

-   Select from a list of available services.
-   Select a category and view the available services within that category.
-   Filter the applicable services based on the products owned by a customer.
-   Create a case of the correct type based on the service requested or for the products owned by a customer.

Customers can use service definitions to discover and request services to support their products from the Customer and Consumer Service Portals.

## Service definition categories

Service definition categories enable you to organize service definitions into logical groupings. A category can have multiple service definitions and a service definition can belong to one or more categories.

These categories appear on the case service selector and case task service selector. When an agent is creating a case or case task, the agent can select a category and then view and select from the available services within that category to create a case or case task.

## Filtering service definitions

The service definitions filtering feature enables you to filter or narrow the services that are available to agents when they are creating cases.

You can filter service definitions by creating configurations that are based on two types of criteria: user and customer.

-   [User criteria](../task/configure-user-criteria-for-a-service-definition.md): Filter service definitions by user criteria such as role, assignment group, or specific user. For example, in a retail organization, different services are created for various roles. Only users with specific roles, such as regional managers or operational managers, can view and use service definitions like Product Recall or New Product Launch in Store. These services are hidden from other agents who are not authorized to create such cases.
-   [Customer criteria](../task/configure-customer-criteria-for-a-service-definition.md): Filter service definitions by customer criteria such as location, customer level, or related entities. For example, for customers with a loyalty membership, service definitions like Free Delivery or Free Installation are made available. Customers who do not meet these criteria will not see or have access to these services.

## The service definition ID field

Starting with the Washington DC release, the **ID** field replaces the **Number** field.

-   For upgrade customers, the **Number** field is relabeled to show that it is deprecated.
-   For new customers, the **Number** field is not present.

For customers upgrading from Utah or Vancouver, a fix script runs automatically that adds the ID field to records in the Service Definition \[sn\_case\_type\_selection\] table. The fix script copies the value from the **Name** field and adds it to the **ID** field, replacing white space characters with underscores. This field has a maximum length of 40 characters.

## System administrator experience

The system administrator defines the services that are offered to customers for the products and services in the product catalog. For each service definition, the admin can complete the following configuration tasks.

|Task|Description|
|----|-----------|
|[Create a service definition](../task/create-csm-service-definition.md)|The service definition record stores details about a service that is provided to customers. This information includes a name for the service definition, the target table, and the service category.|
|[Associate one or more products](../task/service-def-associate-products.md)|Services can be product-specific or general services can be created and made available for all products.|
|[Associate a case type](../task/service-def-associate-case-type.md)|A case type provides the processes and data that an agent needs to resolve a case for a specific type of service.|
|[Associate a playbook](../task/service-def-associate-playbook.md)|A playbook provides agents with step-by-step guidance for resolving a specific type of case.|
|[Configure default field values](../task/service-def-default-field-values.md)|Configure default values for fields in a service definition's target table. When a record is created for this table, the system uses these values to auto-populate record fields.|
|[Associate a record producer](../task/service-def-config-catalog-items.md)|Record producers enable end users to request services from the Customer and Consumer Portals.|
|[Configure related services for a service definition](../task/service-def-config-related-services.md)|Associate one or more related services with a service definition to create parent-child relationships between service definitions. For example, you can create service definitions for case tasks and associate them with a service definition for a case type.|
|[Create a service definition category](../task/create-csm-service-def-category.md)|Create a category for service definitions. You can use these categories to create logical groupings of service definitions.|
|[Associate service definitions with a category](../task/service-def-category-associate-service.md)|Add service definitions to a category. A category can have one or more associated service definitions and a service definition can belong to multiple categories.|
|[Add a case type to the Case interceptor](../task/service-def-config-case-interceptor.md)|Add case types to the Case interceptor, to configure this feature for use in the Core UI.|
|[Configure user criteria for a service definition](../task/configure-user-criteria-for-a-service-definition.md)|Add user criteria to a service definition that restricts a user's access to the service. Associate user-specific criteria such as role, assignment group, or specific user with a service definition to determine which users can access and use that service to create a case.|
|[Configure customer criteria for a service definition](../task/configure-customer-criteria-for-a-service-definition.md)|Add entity criteria to a service definition that restricts access to the service. Associate customer-specific criteria such as location, customer level, or verified status with a service definition to determine which customers are eligible for that service.|

## Agent experience

Associating a case type with a service definition automates the case type selection process for agents. From CSM Configurable Workspace, agents can quickly [create cases of the right case type](../task/create-case-of-specific-case-type.md) based on customer context.

When creating cases, agents can select the appropriate service for a customer based on the products that the customer owns. The Product Service Select version of the [case type selector](csm-case-type-select-modals.md) enables agents to do the following:

-   Create cases from case and case type list views.
-   Create cases from several [types of records](csm-case-type-select-modals.md):
-   Select a product. The case type selector includes a **This case is for an owned product** check box.
    -   If checked: Lists services relevant to the selected product.
    -   If cleared: Lists all available services.
-   Select a category of services and view the services within that category.
-   Select a service from the list of available services.
-   Select **Create Case** to create a case of the case type associated with the service.

The system automatically determines the case type based on the selected service and creates a case of that type. If the service definition has an associated playbook, the agent can use the playbook in a tab on the case record.

**Note:** From the Core UI, the Case interceptor enables agents to select a service definition for case type creation.

Associating a case task type with a service definition enables agents to create case tasks of the right type based on the case context. The Product Service Select version of the [case task type selector](csm-case-task-type-select-modal.md) enables agents to create tasks from case task lists, case records, playbook stages, and the Dynamic Related Records tab in the contextual side panel.

## Customer experience

End users can use the service definitions feature to request available services from the Customer and Consumer Service Portals based on the products they have purchased.

-   Use the portal to view the sold products or the install base items that they own.
-   Select a product or an install base item and see the available services in the Services portal widget. This widget can display product-specific services, requests for new products, and general services.
-   Select a service and launch a record producer to create a service request. When submitted, the system automatically creates a case of the correct type.
-   View a case that was created for a service request and see the **Service definition** field on the case record.

## Services portal widget

End users can view a list of available services for their sold products and install base items from the Customer and Consumer Service Portals.

From the portal, an end user can navigate to a list of their sold products or install base items. After selecting a product, the Services portal widget lists the available services. These can include:

-   Services based on a sold product or install base item
-   General services
-   Services for requesting new products

Selecting a service from the widget displays the record producer associated with the service definition. Depending on the record producer configuration, some of the fields are auto-filled such as the product model or install base item and the selected service. Submitting the record producer creates a case of the correct case type.

**Note:** Cases that have been created from a case type associated with a service definition display the service definition in the **Service definition** field. End users can see this information on the case records that they can access from the portal.

**Related topics**  


[Configuring service definitions](csm-service-definitions-configure.md)

[Customer service case types](customer-service-case-types.md)

[Manage customer service case types](manage-csm-case-types.md)

[Create a customer service case of a specific type](../task/create-case-of-specific-case-type.md)

