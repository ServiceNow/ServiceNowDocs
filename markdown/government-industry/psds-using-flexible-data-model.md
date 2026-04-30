---
title: Using the extendable data model in Public Sector Digital Services
description: The flexibility of the ServiceNow platform provides you with an opportunity to create numerous applications to interact with Public Sector Digital Services. Public Sector Digital Services provides a data model that you can extend and leverage in these applications. Product ModelsYou can use both case types and service definitions to define the processes and data needed to fulfill constituent requests. This section discusses the decision points for choosing which implementation to use in various situations.Use the Public Sector Digital Services data model to review the tables and fields installed with each Public Sector Digital Services application, and determine whether a base case table extension is necessary for your specific use case.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-12-10"
reading_time_minutes: 8
breadcrumb: [Public Sector Data Model, Public Sector Digital Services reference, Public Sector Digital Services \(PSDS\)]
---

# Using the extendable data model in Public Sector Digital Services

The flexibility of the ServiceNow platform provides you with an opportunity to create numerous applications to interact with Public Sector Digital Services. Public Sector Digital Services provides a data model that you can extend and leverage in these applications.

## Product Models

Product Models

A product model is a specific version or configuration of a product that is offered to an end user \(constituent, applicant, or business\). They represent the set of products that your organization offers to its consumers, and allow relationships between different product models. Product models provide government service agents and their end users with a common understanding of the products being offered by an agency, and those being used by constituents. A product model can be a social benefit program that an applicant applies for, or specific type of permit that is ultimately issued to the applicant. End users can view the products they have requested on the Government Service Portal.

You can associate services with product models to enable users to select services for products, and then create service definitions for the services that support your products and associate them with the appropriate products and catalog items. Enable customers to request services using that catalog. Use the Service Definition feature to create definitions for the services that are offered to support your products. This feature is available with the case types plugin.

From the Government Service Portal, end users can select available services from the portal. Selecting a service displays the record producer associated with the service definition. Submitting the record producer creates a case of the correct case type.

Implementors can create their own product models based on the services their agency provides, or add additional fields to their out-of-the-box product model, if required, to describe their product model. For a driver's license, one could add a choice field for license class with choices A, B, or C, creating one product model record per class.

Having a specific product model for each product that is offered helps support multiple aspects of the permitting process implementation, including defining the product, tying together services associated with it, delivering specific product instances, additional workflows, reporting, etc. A product model and associated fields for each playbook is provided out-of-the-box.

If you are dealing with multiple types of permits with unrelated fields, you can extend the specific product model class off the permit model base class to define different attributes on the relevant permit products.

To use product models, admins must:

-   Create a service definition. For information on service definitions, see [.](psds-using-flexible-data-model.md#)
-   Associate a product offered with a service definition
-   Associate one or more catalog items with a service definition.
-   Add additional fields to further differentiate your product model.

## Case Types and Service Definitions

You can use both case types and service definitions to define the processes and data needed to fulfill constituent requests. This section discusses the decision points for choosing which implementation to use in various situations.

### Case types

A case type represents the processes and data needed to resolve a specific type of constituent request. For example, within Public Sector, government service agents can use case types for different constituent needs such as requests for information, requests for maintenance, social benefits application processing, or managing licenses and permits. You can associate record producers with a certain type of case so that when you submit that record producer through the portal, it creates a case of the correct type.

You can extend from existing case types that are provided in Public Sector Digital Services applications out-of-the-box, or you can create and configure an entirely new case type that extends the Case table, in order to implement specific case application types, and enabling you to take advantage of prebuilt roles, business rules, and other business logic.

Creating a new case type can include creating a new table that is an extension of an existing case, or creating an entirely new case type. Typically this involves creating new roles, modules, workspaces, and other required entities. For additional information on case types, see [Customer Service Case Types](https://www.servicenow.com/docs/access?context=customer-service-case-types&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)

All Public Sector Digital Services applications have a base case type table. Use the base case type table when adding a new case type for that application. For example, if you need a new case type in License and Permit Playbook, extend the License and Permit Base Case table, which is itself an extension of the Government Service base case table and was created to capture more specific information related only to a License and Permit case. However, if there is need for a new case type for which there is no base application in PSDS that works, extend the base PSDS case \[sn\_govservice\_case\] table.For more information on the base tables installed with each Public Sector Digital Services application, see [Public Sector Digital Services data model](public-sector-digital-services-data-model.md).

When you are evaluating whether you need to create a new case type in Public Sector Digital Services, you should consider the following:

-   Should I use a service definition instead of a new case type?
-   Does an application already exist that I can use for my use case?
-   Which base PSDS case type should I extend when creating the new case type?

For more information on Case Types and how to extend them, see [Defining the processes and data for a Public Service case](government-service-case-type.md).

### Service definitions

In addition to case types, you can also use service definitions to create a customized process. Service definitions are configurations that sit on top of a specific case type that provide a unique request and fulfillment process. Use service definitions when adding a new use case within a domain that already has a case type and is for an existing persona. In this case, service definitions allow for faster development of new use cases.

The following are the main components needed to create a service definition:

-   Service definition record created for the new service.
-   New view and view rule created for the new service on the case type table.
-   New flow created for the new service which is triggered on the creation of the new record on the case type table. Flows are only needed for more complex use cases, such as ones with multiple tasks or sub-tasks.
-   New record producer for customer/requester to create via service catalog. Only use record producers if you want an end-user to create the request.

For additional more information on Service definitions, see [Service definitions for Public Sector Digital Services](psds-service-definitions.md).

## Tables and Fields

Use the Public Sector Digital Services data model to review the tables and fields installed with each Public Sector Digital Services application, and determine whether a base case table extension is necessary for your specific use case.

When an instance is first created, an admin installs and populates the Public Sector Digital Services data structures with data that is required in order to enable all Public Sector features and capabilities, including prebuilt roles, rules, and other business logic. This data is kept in tables that are considered foundational to all products on your instance, and are included with every Public Sector Digital Services application.

In each Public Sector Digital Services application, you can extend base system tables to create a case type that is more specific to cases you are handling. For example You can also create custom tables that enable you to expand the functionality of the Public Sector Digital Services platform and create custom applications. Custom tables can be used to configure and extend the base system workflows, and to add new functionality or custom applications from your Public Sector Digital Services instance.

A table that extends another table is called a child class, and the table it extends is the parent class. A table can be both a parent and child class both extending and providing extensions for other tables. A parent class that is not an extension of another table is called a base class. A child table will automatically contain the fields that belong to the parent table, but the parent table may not contain all the fields in a child table. Tables and fields are customizable, and you can add new fields to both the base and extension tables to properly capture and track specific information related to the case. Any fields added to the base table will appear in the extension table.

Extending a table:

-   Links the new table to the extending table.
-   Creates system fields in the new table.
-   Creates one or more database tables to store the parent and child classes.

Creating new fields in an extension child table does NOT edit the base table.

This data model outlines that tables and fields that are included with each Public Sector Digital Services application, allowing you to see whether the base case table can capture your information, or whether you need to extend the table to remove fields or add fields to capture your specific data. For more information on extending tables and case types, see [Table extension and classes](https://www.servicenow.com/docs/access?context=table-extension-and-classes&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

