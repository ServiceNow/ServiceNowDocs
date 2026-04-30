---
title: Visibility domains and Contains domains
description: Visibility domains control what a specific user or group of users can see. "Contains" domains control what an entire domain of users can see.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Exploring domain separation, Domain separation for service providers, Access Management]
---

# Visibility domains and Contains domains

Visibility domains control what a specific user or group of users can see. "Contains" domains control what an entire domain of users can see.

## Visibility domains

The "Visibility domains" element determines whether users from one domain can access records from another domain. Associate this element with User \[sys\_user\] and Group \[sys\_user\_group\] records in related lists on those records. Groups grant their members the visibility domains of the group. When a user leaves a group, they lose the group's visibility domains. Granting users a visibility domain grants all the rights to the records in that domain based on ACL \(access control list\) rules.

A visibility domain:

-   Is a user-to-domain relationship and is explicitly granted.
-   Is not a child domain.
-   Is not controlled by the selection in the domain picker. Users with access to a visibility domain always see data in that domain and its child domains.

**Note:** Using visibility domains excessively is not recommended. Although visibility is one method to allow users to access records, it's best to use contains domains for more robust control.

## Contains domains

Normally parent-child relationships define the domain hierarchy. A contains domain lets you relate domains on an as-needed basis, independent of parent-child relationships. However, contains domains grant visibility only to domain data. Processes remain unaffected by contains relationships.

A contains domain:

-   Is a many-to-many, domain-to-domain relationship.
-   May have child domains. When a domain is selected, you can see the data from that domain and its children.
-   Is controlled by the selection in the domain picker.

**Note:** When you open the domain record, the scope is set to that record's domain, so you can see only child domains. Choose **Toggle Domain Scope** from the menu to populate the related list.

## Contains domain example

When a user's home domain is A, and the A domain contains domains B and C, they all become peer domains. That means the user sees data from domains A, B, and C while in their home domain A. If users change domains with the domain picker to Domain B, they see only data in Domain B. When users interact with a record from Domain B or Domain C directly, they see only data for that domain.

## Visibility domain example

Using domain visibility, if Don Goodliffe is in the Database domain, and Bow Ruggeri is in the Network domain, and no incidents are in the global domain, then Don cannot access Bow's incidents because of data separation.

## Inheriting visibility domains based on group membership

If you set the domain table to the Group \[sys\_user\_group\] table, users can inherit visibility domains based on their group membership.

**Parent Topic:**[Exploring domain separation](c_DomainSeparation.md)

**Related topics**  


[Configuration that can be delegated to internal or external customers](ds-before-you-begin.md)

[Domain assignment](c_DomainAssignment.md)

[Domain scope](c_DomainScope.md)

[Concepts for service providers](sp-concepts.md)

[Installed with domain separation](../reference/r_InstalledWithDomainSeparation.md)

[Contains queries and domain access](bp-contains-domain-visibility.md)

[Domain separation recommended practices for service providers](../reference/bp-domain-sep-recommended.md)

