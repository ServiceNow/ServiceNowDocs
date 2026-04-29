---
title: Service Definitions in FSO
description: A service definition describes a service that a financial institution offers to support a product that they sell. Service definitions work with case types to provide different types of support inquiries and unique request and fulfillment processes. In FSO, a sample list of service definitions is preconfigured for each product and line of business.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Using case types and service definitions in FSO, Developer resources, Financial Services Operations \(FSO\)]
---

# Service Definitions in FSO

A service definition describes a service that a financial institution offers to support a product that they sell. Service definitions work with case types to provide different types of support inquiries and unique request and fulfillment processes. In FSO, a sample list of service definitions is preconfigured for each product and line of business.

A service definition is created for each of the services that a financial institution offers. Agents can quickly use the pre-defined services to create cases and case tasks of the right type for customer issues and requests.

Use service definitions when adding a new use case within a domain that already has a case type and is for an existing persona. In this case, service definitions enable faster development of new use cases.

A group of service definitions define the set of services for a given product/case type. If the fulfillers are the same, many different services can be associated with the same case.

Pre-defined service definitions in FSO have associated workflows that sit on top of each case type.

Each service definition has a unique workflow/playbook, attributes, and forms. They can be requested \(via an agent or customer\) or triggered from a backend system. Service definitions enable easy configuration of workflows and extensibility to additional services with Views, Catalog items, data attributes, flows, SLAs, and UI policies.

Service definitions can also be grouped into service categories. Service categories enable easier navigation and controls access to authorized users.

![Service Selector launched from a case list.](../image/fso-service-selector-case-list.png)

The following are the main components needed to create a service definition:

-   A service definition record for the new service.
-   A new view and view rule for the new service on the case type table.
-   A new flow for the new service, which is triggered on the creation of the new record on the case type table.
-   Flows are only needed for more complex use cases, such as ones with multiple tasks or subtasks.
-   A new record producer for customer/requester to create via service catalog. Only use record producers if you want an end user to create the request.

**Parent Topic:**[Using case types and service definitions in FSO](fso-int_guide-work_case_types.md)

**Related topics**  


[Service definitions](https://www.servicenow.com/docs/access?context=csm-service-definitions&version=australia&pubname=australia-customer-service-management&ft:locale=en-US)

[Configure service definitions](../../../../product/fso-common/task/configure-service-definitions.md)

