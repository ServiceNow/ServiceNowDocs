---
title: LDAP extraction
description: An LDAP extraction process can be implemented to detect disabled users.
locale: en-US
release: zurich
product: LDAP integration
classification: ldap-integration
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [LDAP record synchronization, LDAP integration, Authentication, Access Management]
---

# LDAP extraction

An LDAP extraction process can be implemented to detect disabled users.

An extract from your LDAP source can filtered for disabled users using an active flag that can be set for every record in the import to ‘false’. Specify \(‘target.active=false’\) and copy into the **Script** field directly on the Table Transform Map record.

## Benefits

Benefits to this method include:

-   Simple scripting
-   Existing user records are not involved in processing
-   Inactive users are not loaded into a temporary import table
-   No performance impact

## Drawbacks

Drawbacks to this method include:

-   An additional process is created
-   The extract set must be placed in a location where your data source can access it

## Alternative method

[LDAP refresh filters](r_LDAPRefreshFilters.md) use multiple import jobs to divide different types of user records, segregating records for separate processing.

