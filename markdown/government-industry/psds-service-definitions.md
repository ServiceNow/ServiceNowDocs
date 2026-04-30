---
title: Service definitions for Public Sector Digital Services
description: Service definitions are records used to store the details about a service provided to end users. By using a service definition, you can connect a public service with a case type to extend the types of services that can be requested, and the types of cases that can be created to support those services.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Configuring Public Sector Digital Services, Public Sector Digital Services \(PSDS\)]
---

# Service definitions for Public Sector Digital Services

Service definitions are records used to store the details about a service provided to end users. By using a service definition, you can connect a public service with a case type to extend the types of services that can be requested, and the types of cases that can be created to support those services.

You can also configure the support types for those services.

## Overview of a service definition

In addition to case types, you can use a service definition to create a customized process for connecting a requester with the service needed to resolve their claim. A service definition enables you to map a public service, information service, or license and permit service to the list of services your agency offers for resolving that request. When you create a service definition, you can configure the case management processes, such as the case types, for executing those services.

Service definitions enable you to do the following tasks:

-   Configure the support types for services so that applicable services are displayed based on the service requested by the constituent or business.
-   Create the case types that support the requested services.
-   Automatically select a case type that is based on the service or information type that a constituent or business is requesting.

With a service definition, you establish connections between the public services that are requested and those that are offered. By associating the relevant public services that are offered for the services requested, you can use a service definition to simply the service requests that are based on the constituent's context.

Service definitions are available with the Customer Service Case Types plugin \(com.snc.csm\_case\_types\) that is automatically activated when you enable the Public Sector Digital Services Core plugin.

**Important:**

After upgrade to Public Sector Digital Services v8.0, Services Offered, an extension of Product Model, will no longer be used to model government services. Services Received, an extension of Sold Product, will no longer be used to model the government services that have been granted/delivered to constituents. The Service Definition table will be used to model all public services offered by governments. The following fields from the Service Offered table will be removed and replaced with Service Model fields:

-   Type
-   Status
-   Number
-   Period Start Date
-   Period End Date
-   Jurisdiction
-   Category
-   Subcategory
-   Payment source

For more information on how to create a service definition, see [Configure a service definition for Playbooks in Public Sector Digital Services](../task/psds-create-new-service-definition.md).

## Service definition tasks for administrators

The following main components are needed to create a service definition:

-   Service definition record that you create for the new service.
-   New view and view rule that you create for the new service on the case type table.
-   New flow that you create for the new service. This flow is triggered when a new record is created on the case type table. Flows are only needed for more complex use cases, such as the cases that have multiple tasks or subtasks.
-   New record producer for an end-user requester to create through the service catalog.

You can do the following tasks:

-   Define the available services.
    -   Define the details for each public service that is offered.
    -   Associate a playbook with a service.
    -   Associate a service catalog item with a service definition so that constituents or businesses can request this service directly.
-   Associate the relevant public services that are offered with each request.
-   Associate different services with different case types \(This task automates the case type selection for the agents by the service that they select\).

