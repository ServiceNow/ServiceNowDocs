---
title: Service definitions for Public Sector Digital Services
description: Service definitions are records used to store the details about a service provided to end users. By using a service definition, you can connect a public service with a case type to extend the types of services that can be requested, and the types of cases that can be created to support those services.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Case Management, Configure agent workspaces, Configure, Public Sector Digital Services \(PSDS\)]
---

# Service definitions for Public Sector Digital Services

Service definitions are records used to store the details about a service provided to end users. By using a service definition, you can connect a public service with a case type to extend the types of services that can be requested, and the types of cases that can be created to support those services.

You can also configure the support types for those services.

## Overview of a service definition

In addition to case types, you can use a service definition to create a customized process for connecting a requester with the service needed to resolve their claim. A service definition enables you to map a public service, information service, or license and permit service to the list of services your agency offers for resolving that request. When you create a service definition, you can configure the case management processes, such as the case types, for executing those services.

In addition to case types, you can also use service definitions to create a customized process. Service definitions are configurations that sit on top of a specific case type that provide a unique request and fulfillment process. Use service definitions when adding a new use case within a domain that already has a case type and is for an existing persona. In this case, service definitions allow for faster development of new use cases.

Service definitions enable you to do the following tasks:

-   Configure the support types for services so that applicable services are displayed based on the service requested by the constituent or business.
-   Create the case types that support the requested services.
-   Automatically select a case type that is based on the service or information type that a constituent or business is requesting.

With a service definition, you establish connections between the public services that are requested and those that are offered. By associating the relevant public services that are offered for the services requested, you can use a service definition to simply the service requests that are based on the constituent's context.

Service definitions are available with the Customer Service Case Types plugin \(com.snc.csm\_case\_types\) that is automatically activated when you enable the Public Sector Digital Services Core plugin.

For more information on how to create a service definition, see [Configure a service definition for Playbooks in Public Sector Digital Services](../task/psds-create-new-service-definition.md).

## Service definition tasks for administrators

The following main components are needed to create a service definition:

-   Service definition record created for the new service.
-   New view and view rule created for the new service on the case type table.
-   New flow created for the new service which is triggered on the creation of the new record on the case type table. Flows are only needed for more complex use cases, such as ones with multiple tasks or sub-tasks.
-   New record producer for requester to create via service catalog. Only use record producers if you want an end-user to create the request.

## Service definitions

The following are the main components needed to create a service definition: For additional more information on Service definitions, see [Service definitions for Public Sector Digital Services](psds-service-definitions.md).

You can do the following tasks:

-   Define the available services.
    -   Define the details for each public service that is offered.
    -   Associate a playbook with a service.
    -   Associate a service catalog item with a service definition so that constituents or businesses can request this service directly.
-   Associate the relevant public services that are offered with each request.
-   Associate different services with different case types \(This task automates the case type selection for the agents by the service that they select\).

