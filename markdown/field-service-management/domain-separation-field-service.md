---
title: Domain separation and Field Service Management
description: Domain separation provides a structured and efficient way to manage complex, multi-tiered organizational environments. It allows for tailored access and control, ensuring that users see only the data relevant to their domain, enhancing security and efficiency.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Plan implementation, Configure, Field Service Management]
---

# Domain separation and Field Service Management

Domain separation provides a structured and efficient way to manage complex, multi-tiered organizational environments. It allows for tailored access and control, ensuring that users see only the data relevant to their domain, enhancing security and efficiency.

## Support level: Basic



-   Business logic: Ensure that data goes into the proper domain for the application’s service provider use cases.
-   The application supports domain separation at run time. The domain separation includes separation from the user interface, cache keys, reporting, rollups, and aggregations.
-   The owner of the instance must set up the application to function across multiple tenants.

Sample use case: When a service provider \(SP\) uses chat to respond to a tenant-customer’s message, the customer must be able to see the SP's response.

For more information on support levels, see [Application support for domain separation](https://www.servicenow.com/docs/access?context=domain-separated-apps&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

## Field Service Management domain separation overview

Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data. In the Field Service Management application, you can use the Company entity to drive domain separation. Assign a domain to each company and then any work orders and tasks created for a company are created within the company domain. Other entities and tasks related to work orders, such as dispatcher and assignment groups, part requirements, and transfer orders, are driven by the company and work order domains.

## How domain separation works in Field Service Management

Domain separation for Field Service Management uses the Company entity to drive the domain structure. To use domain separation, all companies must be assigned to a domain.

When using Field Service Management in a domain separated instance, the **Company** field is a mandatory field on the Work Order form. When you create a work order for a company, the work order is created in the company domain. Any tasks created for the work order are also created in the company domain.

When using Field Service Management integrated with Customer Service Management in a domain separated instance, the **Account** field is a mandatory field on the Work Order form. When you create a work order for an account through a customer service case, the work order is created in the account domain. Any tasks created for the work order are created in the same domain as the work order. In the event that the domain of the work order changes, the domain of the work order tasks is also updated.

Modifying the company or account on a work order also modifies the domain of the work order and work order tasks. The domains of other related entities are not automatically updated. The company or account can be changed until the work order is qualified.

**Note:** Field Service Management is configured at the application level and does not support domain-specific configuration. For example, if you select **use dynamic scheduling** as your task assignment method, this method is used to assign tasks in all domains.

## Setting up domain separation in Field Service Management

To set up domain separation for Field Service Management, contact ServiceNow, Inc.

## Work orders created from Incident, Problem, or Change

For work orders created from an incident, problem, or change request the following will occur:

-   The company on the work order is inherited from the original record.
-   The domain of the work order is inherited from the company.
-   If the original record does not include a company, the **Company** field is still a required field on the Work Order form.

## Groups

Qualification, dispatcher, and assignment groups are filtered based on the domain of the work order and work order tasks. The group domain must match the work order or work order task domain.

## Parts process

The parts process, which includes sourcing and using assets, is also domain separated.

-   Part requirements are created in the work order domain.
-   Transfer orders and transfer order lines created for a part requirement are created in the part requirement’s domain.
-   When sourcing a part, the following are available:
    -   Assets are available for a work order or work order task based on the part requirement domain.
    -   Assets are available based on the part requirement domain.
    -   Stockrooms are available based on available assets.

**Related topics**  


[Domain separation for service providers](https://www.servicenow.com/docs/access?context=domain-sep-landing-page&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)

