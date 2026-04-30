---
title: Internal Business Location form
description: In the Customer Service Management \(CSM\) application, the Service Model Foundation uses the Internal Business Location \(IBL\) form to store information about an internal business location. This information includes the staff members assigned to that location, cases, sold products, and install base items created for customers.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Customer Service forms, Customer Service Management reference, Customer Service Management]
---

# Internal Business Location form

In the Customer Service Management \(CSM\) application, the Service Model Foundation uses the Internal Business Location \(IBL\) form to store information about an internal business location. This information includes the staff members assigned to that location, cases, sold products, and install base items created for customers.

<table id="table_fyv_dtr_bs"><thead><tr><th>

Field

</th><th>

Definition

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Automatically generated number of the internal business location. By default, the location numbers start with the prefix IBL.

</td></tr><tr><td>

Name

</td><td>

Name of the internal business location.

</td></tr><tr><td>

Manager

</td><td>

Manager of the internal business location.**Note:** Only internal users can be added as managers for the internal business locations.

</td></tr><tr><td>

Parent Internal Business Location

</td><td>

Business location that can have a parent internal business location. Use this field to create a parent-child hierarchy.

</td></tr><tr><td>

Street

</td><td>

Street address of the internal business location.

</td></tr><tr><td>

City

</td><td>

City in which the internal business location lives.

</td></tr><tr><td>

State/Province

</td><td>

State or province in which the internal business location lives.

</td></tr><tr><td>

Zip/Postal code

</td><td>

ZIP code or postal code for the internal business location.

</td></tr><tr><td>

Customers served

</td><td>

Customers that are served at a business location. The customers served can be defined with two options:-   **All Customers**: Allows service organization staff to create and resolve issues for all the customers.
-   **Criteria-based**: Allows service organization staff to create and resolve issues only for customers associated to the service organization using a criteria.

</td></tr><tr><td>

Website

</td><td>

Web address for the internal business location.

</td></tr><tr><td>

Email

</td><td>

Email ID used by the internal business location.

</td></tr><tr><td>

Phone

</td><td>

Phone number for the internal business location.

</td></tr></tbody>
</table>## Internal business location related lists

The Internal Business Location form includes the following related lists.

<table id="table_wts_433_gmb"><thead><tr><th>

Related list

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Members

</td><td>

Internal users \(users with the snc\_internal role\) who have been added as staff members at this business location. -   Staff members can create cases for customers at their business locations.
-   Staff members can access customer cases and information where the **Service Organization** field on the Case form matches their business locations.

For more information, see [Add staff members to a business location](../concept/add-staff-members-biz-loc.md).

</td></tr><tr><td>

Internal Business Locations

</td><td>

List of internal business location records.For more information, see [Create an internal business location](../task/create-internal-business-location.md).

</td></tr><tr><td>

Service Organization Customer Criteria

</td><td>

List of customers that are supported by an internal business location.For more information, see [Define the configuration type for customers or business locations](../task/associate-customer-criteria-to-service-organization.md).

</td></tr><tr><td>

Cases Assigned to Location

</td><td>

Cases that have been created and assigned to this location. For more information, see[Create and manage cases for a business location](../task/manage-business-location-cases.md).

</td></tr><tr><td>

Account Staff Relationships

</td><td>

Relationships that have been created between staff members and accounts at this location. Create account staff relationships by using the Account Manager responsibility.

For more information, see [Create an account staff relationship](../task/create-staff-account-relationship.md).

</td></tr><tr><td>

Consumer Staff Relationships

</td><td>

Relationships that have been created between staff members and consumers at this location. Create consumer staff relationships by using the Relationship Manager responsibility.

For more information, see [Create a consumer staff relationship](../task/create-staff-consumer-relationship.md).

</td></tr><tr><td>

Household Staff Relationships

</td><td>

Relationships that have been created between staff members and households at this location. Create household staff relationships by using the Relationship Manager responsibility.

For more information, see [Create a household staff relationship](../task/create-staff-household-relationship.md).

</td></tr><tr><td>

Sold Products

</td><td>

Sold products that have been created for customers at this location.For more information, see [Create and manage sold products for a business location](../task/create-sp-for-business-location.md).

</td></tr><tr><td>

Install Base Items

</td><td>

Install base items that have been created for customers at this location.For more information, see [Create and manage install base items for a business location](../task/create-ib-items-for-business-locations.md).

</td></tr></tbody>
</table>**Related topics**  


[Create an internal business location](../task/create-internal-business-location.md)

[Service Model Foundation relationships](csm-data-model-relationships.md)

