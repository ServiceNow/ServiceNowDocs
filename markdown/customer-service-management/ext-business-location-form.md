---
title: External Business Location form
description: In the Customer Service Management \(CSM\) application, the Service Model Foundation uses the External Business Location \(EBL\) form to store information about an external business location. This information includes the staff members assigned to that location, cases, sold products, and install base items created for customers.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Customer Service forms, Customer Service Management reference, Customer Service Management]
---

# External Business Location form

In the Customer Service Management \(CSM\) application, the Service Model Foundation uses the External Business Location \(EBL\) form to store information about an external business location. This information includes the staff members assigned to that location, cases, sold products, and install base items created for customers.

<table id="table_oxs_s2g_qtb"><thead><tr><th>

Field

</th><th>

Definition

</th></tr></thead><tbody><tr><td>

Number

</td><td>

The automatically generated number of the external business location. By default, location numbers start with the prefix EBL.

</td></tr><tr><td>

Name

</td><td>

The name of the external business location.

</td></tr><tr><td>

Manager

</td><td>

The manager of the external business location.**Note:** Both internal and external users can be added as managers for external business locations.

</td></tr><tr><td>

Parent Business Location

</td><td>

A business location can have a parent external business location. Use this field to create a parent-child hierarchy.

</td></tr><tr><td>

Street

</td><td>

The street address of the external business location.

</td></tr><tr><td>

City

</td><td>

The city in which the external business location resides.

</td></tr><tr><td>

State/Province

</td><td>

The state or province in which the external business location resides.

</td></tr><tr><td>

Zip/Postal code

</td><td>

The ZIP code or postal code for the external business location.

</td></tr><tr><td>

Customers served

</td><td>

Customers served at a business location. Customers served can be defined using two options:-   **All Customers**: Allows service organization staff to create and resolve issues for all the customers.
-   **Criteria-based**: Allows service organization staff to create and resolve issues only for customers associated to the service organization using a criteria.

</td></tr><tr><td>

Website

</td><td>

The web address for the internal business location.

</td></tr><tr><td>

Email

</td><td>

The email ID used by the internal business location.

</td></tr><tr><td>

Phone

</td><td>

The phone number for the internal business location.

</td></tr></tbody>
</table>## External business location related lists

The External Business Location form includes the following related lists.

<table id="table_wts_433_gmb"><thead><tr><th>

Related list

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Members

</td><td>

Internal and external users who have been added as staff members at this business location. -   Staff members can create cases for customers at their business locations.
-   Staff members can access customer cases and information where the **Service Organization** field on the Case form matches their business locations.

For more information about adding staff members to an external business location, see [Add staff members to a business location](../concept/add-staff-members-biz-loc.md).

</td></tr><tr><td>

External Business Locations

</td><td>

List of external business location records.For more information about creating external business locations, see [Create an external business location](../task/create-external-business-location.md).

</td></tr><tr><td>

Service Organization Customer Criteria

</td><td>

The list of customers supported by an external business location.For more information about associating customer criteria to an external business location, see [Define the configuration type for customers or business locations](../task/associate-customer-criteria-to-service-organization.md).

</td></tr><tr><td>

Cases Requested by Location

</td><td>

Cases that have been created and requested by this location.For more information about assigning cases to an external business location, see[Create and manage cases for a business location](../task/manage-business-location-cases.md).

</td></tr><tr><td>

Account Staff Relationships

</td><td>

Relationships that have been created between staff members and accounts at this location. Account staff relationships are created using the Account Manager responsibility.

For more information about creating an account staff relationship, see [Create an account staff relationship](../task/create-staff-account-relationship.md).

</td></tr><tr><td>

Consumer Staff Relationships

</td><td>

Relationships that have been created between staff members and consumers at this location. Consumer staff relationships are created using the Relationship Manager responsibility.

For more information about creating a consumer staff relationship, see [Create a consumer staff relationship](../task/create-staff-consumer-relationship.md).

</td></tr><tr><td>

Household Staff Relationships

</td><td>

Relationships that have been created between staff members and households at this location. Household staff relationships are created using the Relationship Manager responsibility.

For more information about creating a household staff relationship, see [Create a household staff relationship](../task/create-staff-household-relationship.md).

</td></tr><tr><td>

Sold Products

</td><td>

Sold products that have been created for customers at this location.For more information about creating and managing sold products for an external business location, see [Create and manage sold products for a business location](../task/create-sp-for-business-location.md).

</td></tr><tr><td>

Install Base Items

</td><td>

Install base items that have been created for customers at this location.For more information about creating and managing install base items for an external business location, see [Create and manage install base items for a business location](../task/create-ib-items-for-business-locations.md).

</td></tr></tbody>
</table>**Related topics**  


[Create an internal business location](../task/create-internal-business-location.md)

[Service Model Foundation relationships](csm-data-model-relationships.md)

