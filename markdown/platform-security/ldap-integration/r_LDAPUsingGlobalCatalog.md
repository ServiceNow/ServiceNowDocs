---
title: LDAP global catalog usage
description: A DC can be granted the Global Catalog \(GC\) role. Global Catalog \(GC\) role is an LDAP-compliant directory consisting of a partial representation of every object from every domain within a forest.
locale: en-US
release: xanadu
product: LDAP integration
classification: ldap-integration
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [LDAP integration, Authentication, Access Management]
---

# LDAP global catalog usage

A DC can be granted the Global Catalog \(GC\) role. Global Catalog \(GC\) role is an LDAP-compliant directory consisting of a partial representation of every object from every domain within a forest.

Administrators configure Active Directory to host Lightweight Directory Access Protocol \(LDAP\) directory information using one of the following hosting methods.

-   The common method of hosting LDAP directory information is to use the default LDAP or LDAPS \(secure LDAP\) on ports 389 or 636. These standard LDAP ports always exist on a Domain Controller \(DC\) and are rarely changed. Accessing this directory partition provides access to all of the objects within the domain that is hosted on the DC. There is no way to access objects from other domains using this method.
-   A DC can also be granted the Global Catalog \(GC\) role. Global Catalog \(GC\) role is an LDAP-compliant directory consisting of a partial representation of every object from every domain within the forest. This LDAP directory can be accessed on port 3268, with LDAPS on port 3269. LDAPS and the default LDAP ports' certificate requirements are the same.

## Global Catalog LDAP dependencies

-   The domain controller that your instance connects to must have the Global Catalog role enabled.
-   Firewall rules must allow inbound traffic to the domain controller on port 3268 \(LDAP\) or 3269 \(LDAPS\).

## Special notes

-   Not all attributes are replicated to the GC partition. Common attributes such as first name, last name, email, phone number, description, and address are included. Additional attributes can be added to the GC but should be limited to minimize the impact to forest replication traffic.
-   Standard LDAP integrations usually use sAMAccountName as the instance's UserID and as the coalesce key in the LDAP import map since this is guaranteed to be unique within a domain. This attribute is no longer unique when viewing an entire forest of domains. A new unique attribute needs to be identified and as the UserID and the coalesce key. These do not need to be the same attribute and may vary based on your forest design. Consult your Active Directory administrator. Typically, the userPrinicpalName is a unique attribute across domains but this may not be a user-friendly name to login with, but it could be used for the unique identifier on imports. A common attribute that is used for the UserID is email address. These decisions impact the LDAP Properties and LDAP Mapping.
-   The value used for the coalesce key on the LDAP import map must be unique and exist on every object being imported. If it is not unique or does not exist, incorrect records are updated with changes.
-   If you already have an LDAP integration and wish to change it to a GC, change the import coalesce key. The new key values must be imported before you can change the coalesce key.
-   If you make any changes to your LDAP integration that break your integration, your first step should be to revert those changes. After that, contact Customer Service and Support with complete information about what you're attempting.

