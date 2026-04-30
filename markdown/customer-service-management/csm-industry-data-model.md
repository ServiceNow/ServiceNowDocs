---
title: Service Model Foundation overview
description: Service Model Foundation provide a framework that customers can use to configure structured and flexible data models that represent their business needs.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Configure Service Model Foundation, Data models, Set up your environment, Configure, Customer Service Management]
---

# Service Model Foundation overview

Service Model Foundation provide a framework that customers can use to configure structured and flexible data models that represent their business needs.

The Service Model Foundation framework expands the Customer Service Management data model, including the install base model. It provides the flexibility and security needed to support business organizations with internal and external locations, households, customers and consumers, and the relationships that exist between these entities.

Video overview explaining key components and functionality of the Service Model Foundation. 

Use the Service Model Foundation framework to model the service organization structure that is involved in supporting your end customers. With this framework, you can:

-   Create a service organization structure that includes both internal and external business locations.
-   Assign customer service agents to business locations and provide access to the cases and customer information in their business location hierarchy.
-   Establish relationships between agents and specific customers that enable agents to manage cases and information for those customers.
-   Establish relationships between consumers, including consumers who are members of the same household.

## Entities included with Service Model Foundation

The Service Model Foundation feature includes the following entities.

<table id="table_ky1_wy4_dmb"><thead><tr><th>

Entity

</th><th>

Definition

</th><th>

Examples

</th></tr></thead><tbody><tr><td>

Service organizations

</td><td>

The internal and external entities that are involved in providing a service to customers.

 A service organization provides the base framework that supports the customer service value chain. This includes internal and external service organizations.

 You can extend the service organization to create new entities as needed.

</td><td>

-   Financial service organizations with multiple branches
-   Automobile manufacturers with multiple dealerships
-   Government agencies with multiple office locations

</td></tr><tr><td>

Internal business locations

</td><td>

The internal entities that belong to a service organization and are involved in providing goods and services.

</td><td>

-   Stores
-   Branches
-   Centers

</td></tr><tr><td>

External business locations

</td><td>

The external entities that belong to a service organization and are involved in providing goods and services.

</td><td>

-   Franchises
-   Dealerships

</td></tr><tr><td>

Customers \(B2B\)

</td><td>

The external customers in the business-to-business model who use goods and services.

</td><td>

-   Accounts
-   Contacts

</td></tr><tr><td>

[Configuring households](configure-households.md)

</td><td>

The external customers in the business-to-consumer model who use goods and services.

</td><td>

-   Consumers
-   Households

</td></tr><tr><td>

Employees and staff members

</td><td>

The people who work at internal and external service organizations and assist customers.

</td><td>

-   Internal employees
-   External agents
-   External staff

</td></tr><tr><td>

[Roles](../reference/csm-data-model-roles.md)

</td><td>

Job functions that are performed by various users in the service organization.

</td><td>

-   Location managers
-   Location agents
-   Location consumer agents
-   Location relationship managers
-   Location manager contributors

</td></tr><tr><td>

[Responsibility definitions](../reference/csm-data-model-responsibilities.md)

</td><td>

Definitions of the responsibilities that an agent can perform for a customer or that a consumer can perform for another consumer. Use these responsibilities to create relationships between agents and customers or between consumers.

</td><td>

-   Location agents
-   Location consumer agents
-   Location contributors
-   Location manager contributors
-   Location manager fulfiller
-   Location relationship manager

</td></tr><tr><td>

[Relationships](../reference/csm-data-model-relationships.md)

</td><td>

Relationships that are created between agents and customers or between two consumers, are based on specific responsibilities. Use these relationships to provide additional access to data.

</td><td>

-   Relationships between an employee or staff member and a customer
-   Relationships between two consumers

</td></tr></tbody>
</table>## Plugins for Service Model Foundation

Users with the system administrator role can activate the following plugins to enable Service Model Foundation features.

-   **Business Location**

    Activate the Business Location plugin \(com.snc.business\_location\) to enable support for businesses that interact with customers through physical channels such as stores, branches, franchises, and dealerships. This plugin automatically activates the Service Organization plugin \(com.snc.service\_organization\).

-   **Customer Service Household**

    Activate the Customer Service Household plugin \(com.snc.household\) to manage customer service for households. This plugin enables you to create households, define the members of a household, and identify relationships between household members. This plugin automatically activates the Customer Service Base Extension Entities plugin \(com.snc.cs\_base\_extension\).


**Related topics**  


[Configure Service Model Foundation](../task/configure-industry-data-model.md)

