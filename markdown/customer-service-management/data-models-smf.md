---
title: Service Model Foundation data model
description: The Service Model Foundation data model defines the underlying structure that supports data consistency and relationships across Service Model Foundation. The data model explains its purpose, including how entities such as services, locations, and accounts are organized and connected through the entity-relationship Diagram \(ERD\) and reference architecture. It provides a unified view of data design, confirming scalability, integrity, and seamless integration across Service Model Foundation components.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Overview, Configure Service Model Foundation, Data models, Set up your environment, Configure, Customer Service Management]
---

# Service Model Foundation data model

The Service Model Foundation data model defines the underlying structure that supports data consistency and relationships across Service Model Foundation. The data model explains its purpose, including how entities such as services, locations, and accounts are organized and connected through the entity-relationship Diagram \(ERD\) and reference architecture. It provides a unified view of data design, confirming scalability, integrity, and seamless integration across Service Model Foundation components.

Service Model Foundation provides a framework that your customers can use to create structured yet flexible data models that represent their business structure. Central support represents the supporting entity within the main organization. Service organizations represent additional entities providing customer support.

There are three types of service organizations:

-   Internal Business Locations \(IBL\)
-   External Business Locations \(EBL\)
-   Outsourced Service Providers \(OSP\)

Note: These business locations can also be logical entities and not necessarily physical locations.

## Entity relationship model

The following entity-relationship diagram \(ERD\) shows the tables and their relationships that comprise the Service Model Foundation data model.

![Entity relationship diagram showing how service organizations connect to internal and external business locations and outsourced service providers, each linked to employees or staff.](../image/smf-data-model.png "Service Model Foundation entity-relationship diagram (ERD)")

This ERD illustrates the structural relationships among service organizations, business locations, and staff or employees within the Service Model Foundation. A service organization manages multiple internal \(IBL\), external \(EBL\), and outsourced \(OSP\) locations, each associated with its own workforce, that is employees or external staff, who perform service activities.

The model differentiates internal versus external service delivery contexts while maintaining a unified link through the sys\_user and service organization staff tables. It provides the foundation for access control, visibility, and data consistency across all Service Model Foundation entities.

## Reference architecture and data flow model

The following reference architecture diagram illustrates the technical framework and data flow within the Service Model Foundation \(SMF\) system.

![Reference diagram highlighting how various system components, tables, and services interact to deliver and manage service operations.](../image/smf-reference-architecture.png "Service Model Foundation reference architecture")

This reference architecture highlights how various system components, tables, and services interact to deliver and manage service operations. It shows the flow of data between primary data tables, transaction tables, and custom tables, emphasizing the integration points between internal and external business locations, service offerings, and case management processes.

The reference architecture ensures a clear understanding of how information is processed, routed, and stored across the Service Model Foundation system.

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

 A service organization provides the base framework that supports the customer service value chain. This framework includes internal and external service organizations.

 You can extend the service organization to create entities as needed.

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
</table>