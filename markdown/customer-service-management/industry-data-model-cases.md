---
title: Service Model Foundation cases
description: Location agents and location consumer agents at a business location can create cases for accounts, contacts, consumers, and households.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Service Model Foundation overview, Configure Service Model Foundation, Data models, Set up your environment, Configuring Customer Service Management, Customer Service Management]
---

# Service Model Foundation cases

Location agents and location consumer agents at a business location can create cases for accounts, contacts, consumers, and households.

Staff members with the location agent or location consumer agent role can do the following:

-   View information for the customers at their location.
-   Create cases for accounts, contacts, households, and consumers.
-   Update cases created at their location.
-   Create consumers.

## Case location

A case belongs to a business location. When a case is created by a location agent or manager, the **Service Organization** field on the Case form is automatically updated with the business location to which the agent or manager belongs. If the case is reassigned, this field is updated to that of the new agent or manager.

If the location agent or manager belongs to multiple locations, the **Service Organization** field can be kept empty. When you fill in this field, select carefully as the service organization controls a location agent's access to cases.

**Note:** A case can belong to only one business location.

The **Service Organization** can be set manually for a new case or changed for an existing case. Changing the **Service Organization** doesn’t change the assigned agent.

## Case access

Case access is controlled by the business location in the **Service Organization** field on the Case form. The following users can access cases:

-   Staff members at the business location with the location agent or location consumer agent role.
-   Managers at the business location with the location manager role.

Cases for a business location are added to the Cases related list on the internal or external business location form.

-   When a case is created, the service organization on the case is the service organization of the user who creates the case.
-   When a case is assigned to an agent, the service organization on the case is updated to the service organization of the assigned agent.

**Note:** Only external staff with the location agent can act as fulfillers. For more information, see [External business location \(EBL\) as a fulfiller](../concept/ebl-as-a-fulfiller.md).

|Consumer type|Case access|
|-------------|-----------|
|Consumer|Can manage their own cases.|
|Head of household|Can manage cases for all household members.​|
|Authorized representative, regardless of household|Can manage cases for the consumer they represent​.|
|Authorized representative, inside of household|Can manage cases for the consumer they represent as long as both are current members of the household.​|

<table id="table_ltw_2mw_gmb"><thead><tr><th>

User

</th><th>

Required role

</th><th>

Case access

</th></tr></thead><tbody><tr><td>

Location manager

</td><td>

Location manager

</td><td>

Can manage the cases in their location hierarchy.​

</td></tr><tr><td>

Location staff member

</td><td>

Location agent

 Location consumer agent

</td><td>

Can manage the cases in their locations.

</td></tr><tr><td>

Account manager

</td><td>

Relationship agent

</td><td>

Can manage cases for their accounts.

</td></tr><tr><td>

Consumer relationship manager

</td><td>

Relationship agent

</td><td>

Can manage cases for their consumers.

</td></tr><tr><td>

Household relationship manager

</td><td>

Relationship agent

</td><td>

Can manage cases for their households.

</td></tr></tbody>
</table>