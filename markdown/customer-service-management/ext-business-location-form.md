---
title: External Business Location form
description: In the Customer Service Management \(CSM\) application, the Service Model Foundation uses the External Business Location \(EBL\) form to store information about an external business location. This information includes the staff members assigned to that location, cases, sold products, and install base items created for customers.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 6
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

Automatically generated number of the external business location. By default, location numbers start with the prefix EBL.

</td></tr><tr><td>

Name

</td><td>

Name of the external business location.

</td></tr><tr><td>

Manager

</td><td>

Manager of the external business location.**Note:** Both internal and external users can be added as managers for external business locations.

</td></tr><tr><td>

Parent Business Location

</td><td>

Parent of the business location. Use this field to create a parent-child hierarchy.

</td></tr><tr><td>

Street

</td><td>

Street address of the external business location.

</td></tr><tr><td>

City

</td><td>

City where the external business location is located.

</td></tr><tr><td>

State/Province

</td><td>

State or province where the external business location is located.

</td></tr><tr><td>

Zip/Postal code

</td><td>

ZIP code or postal code for the external business location.

</td></tr><tr><td>

Customers served

</td><td>

Types of customers who are served at a business location. Customers served can be defined using two options:-   **All Customers**: Allows service organization staff to create and resolve issues for all the customers.
-   **Criteria-based**: Allows service organization staff to create and resolve issues only for customers associated with the service organization using a criteria.

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

</td></tr><tr><td>

Open date

</td><td>

Date on which the business location becomes operational and available for customers.

</td></tr><tr><td>

Close date

</td><td>

Date on which the business location becomes non-operational and unavailable for customers.**Note:** The closed date must not be earlier than the open date.

</td></tr><tr><td>

Status

</td><td>

Current status of the business location whether In progress, Operational, non-operational, or closed.

</td></tr><tr><td>

Description

</td><td>

Description of the business location.

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

Child External Business Locations

</td><td>

List of external business location records.For more information about creating external business locations, see [Create an external business location](../task/create-external-business-location.md).

</td></tr><tr><td>

Assignment Groups

</td><td>

List of all associated assigned groups of the internal business location.For more information, see [Setting up assignment groups](../concept/setting-up-assignment-groups.md).

</td></tr><tr><td>

Available Services

</td><td>

List of services supported by the business location.For more information, see [Setting up products and available services at a business location](../concept/products-services-at-bus-loc.md).

</td></tr><tr><td>

Customer Projects

</td><td>

List of all projects assigned to the business location. Select a project to see **Project Tasks**, **Sub Projects** and **Cases** assigned to the project.

 **Note:**

-   A location manager can see projects of their respective and child business locations. To learn more about roles, see [Service Model Foundation roles](csm-data-model-roles.md).
-   List of project tasks under customer project tab is visible only if the **Visible to Customer** is selected during project task creation.

 To learn more about project creation, see[Create customer projects](../task/create-customer-projects.md).

 To learn more about project task creation, see [Create a project task from a project](https://www.servicenow.com/docs/access?context=t_CreateATaskFromAProject&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US).

</td></tr><tr><td>

Service Organization Customer Criteria

</td><td>

List of customers supported by an external business location.For more information about associating customer criteria to an external business location, see [Define the configuration type for customers or business locations](../task/associate-customer-criteria-to-service-organization.md).

</td></tr><tr><td>

Cases Requested by Location

</td><td>

Cases that have been created and requested by this location.For more information about assigning cases to an external business location, see [Create and manage cases for a business location](../task/manage-business-location-cases.md).

</td></tr><tr><td>

Cases Assigned to Location

</td><td>

Cases that have been created and assigned to this location. For more information about creating and managing cases, see [Create and manage cases for a business location](../task/manage-business-location-cases.md).

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

Sold products that have been created for customers at this location.To learn more about creating and managing sold products for an external business location, see [Create and manage sold products for a business location](../task/create-sp-for-business-location.md).

</td></tr><tr><td>

Install Base Items

</td><td>

Install base items that have been created for customers at this location.For more information about creating and managing install base items for an external business location, see [Create and manage install base items for a business location](../task/create-ib-items-for-business-locations.md).

</td></tr></tbody>
</table>**Related topics**  


[Create an internal business location](../task/create-internal-business-location.md)

[Service Model Foundation relationships](csm-data-model-relationships.md)

