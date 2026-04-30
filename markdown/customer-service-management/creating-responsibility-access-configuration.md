---
title: Creating a responsibility access configuration
description: Create responsibility access configurations to add or modify access for various user relationships using different association types.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Configuring customer access management, User management, Set up your environment, Configure, Customer Service Management]
---

# Creating a responsibility access configuration

Create responsibility access configurations to add or modify access for various user relationships using different association types.

Administrators can use these configurations to define the roles required to access specific table records, including the level of access. With new filters and table mappings, you can model granular relationships that represent a wide range of responsibilities within your organization.

For example, starting with the Zurich release, account manager responsibility access configuration is introduced out of the base system. Using this responsibility, you can assign the account manager responsibility to a specific account. This configuration grants access to account information, along with related entities such as cases, sold products, and more.

## Association types

As an administrator, you can use this flexible framework to either create a responsibility with customized access rules or modify existing configurations as needed. You can create responsibility access configurations for various relationship patterns using appropriate association types.

-   Simple association
-   Dependent association
-   Advanced association

## Simple association

You can use this association when there’s a direct relationship between the user and the target record. This association type uses direct field matching and doesn’t require intermediate tables or custom logic.

![A screenshot displaying how access to case records is granted using a simple relationship association.](../image/simple-association.png "Simple association workflow")

**Simple association workflow**

This scenario explains how access to case records is granted based on a user’s direct relationship to the associated account. For example, Anna is an account manager for the customer account XYZ company. They need access to case records that are directly linked to XYZ company. As the case record includes a field for the associated account, the system can easily validate Anna’s access based on the role and the account ID.

The system determines Alex’s access using the following logic:

-   Anna opens a case record.
-   The system identifies the account associated with the case.
-   It checks the account team member table to find a record where:
    -   The user is Anna
    -   The responsibility is the account manager
    -   The account matches the account listed on the case
-   If a matching record is found, access to the case is automatically granted.

This approach confirms that access is granted efficiently when there’s a clear, one-to-one relationship between the user and the account associated with the case.

## Dependent association

You can use this association when access must be determined through an intermediate relationship, often involving a many-to-many \(M2M\) table. This setup is common when a requester’s connection to a record is established indirectly through related items.

![A screenshot displaying how access to case records is granted using a dependent relationship association.](../image/dependent-association.png "Dependent association workflow")

**Dependent association workflow**

This scenario explains how access to case records is granted based on a requester’s relationship to install base items associated through an intermediate table. For example, Alex is a team member with authorized account responsibility and require access to specific case records that are tied to install base items. Alex’s access depends on whether these case records are listed as an authorized party for any of those items. However, the relationship between the case and the install base item isn’t direct, but it’s maintained through a separate affected install base table.

The system determines Alex’s access using the following logic:

-   Alex opens a case record.
-   The system checks if the case is linked to any install base items using the affected install base table.
-   It retrieves the install base items associated with the case.
-   The system checks if Alex is listed with the authorized account role for any of the install base items in the related party table.
-   If Alex holds the required role for any matching item, access to the case record is automatically granted.

This approach confirms that access is granted only when a valid relationship exists between the requester and install base items, enforcing secure access even through indirect associations.

## Advanced association

You can use this association in complex scenarios where simple relationship-based access is insufficient. This association type relies on custom script logic to validate requester's access across multiple related records.

![A screenshot displaying how access to case records is granted using an advanced relationship association.](../image/advanced-association.png "Advanced association workflow")

**Advanced association workflow**

This scenario explains how access to escalation records is determined based on the requester’s relationship to the associated account.

For example, Anna is an account manager who needs access to specific escalation records. Some of these escalation records are tied to cases, which are in turn associated with accounts Anna manages. A custom script identifies the related accounts and verifies Anna’s role before granting access to the escalation records.

The system determines Alex’s access using the following logic:

1.  Anna opens an escalation record.
2.  The system checks the escalation’s source:
    -   If the escalation is linked to a customer case, the system identifies the account associated with that case.
    -   If the escalation is directly linked to an account, the system uses the account record.
3.  The system verifies if Anna is assigned as the account manager for the identified account.
4.  If Anna is assigned to the account, access to the escalation record is automatically granted.

This approach confirms that access is granted only when a clear relationship exists between the user and account, whether the link is direct or through a related case.

