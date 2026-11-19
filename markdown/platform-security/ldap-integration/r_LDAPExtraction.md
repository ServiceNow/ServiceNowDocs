---
title: LDAP extraction
description: Implement an LDAP extraction process to detect inactive users.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-security/ldap-integration/r\_LDAPExtraction.html
release: zurich
product: LDAP integration
classification: ldap-integration
topic_type: reference
last_updated: "2026-05-20"
reading_time_minutes: 1
breadcrumb: [LDAP record synchronization, LDAP integration, Authentication, Access Management]
---

# LDAP extraction

Implement an LDAP extraction process to detect inactive users.

To detect inactive users using LDAP extraction, create a separate LDAP data source scoped specifically to inactive user accounts. For example, target a inactive users organizational unit \(OU\) or apply a query filter that matches inactive account flags. In the Table Transform Map for that data source, add a transform script that sets `target.active = false` for each record. Because the data source returns only inactive users, the script deactivates only those accounts in ServiceNow.

## Benefits

Benefits to this method include:

-   Simple scripting
-   Existing user records aren't involved in processing
-   Inactive users aren't loaded into a temporary import table
-   No performance impact

## Drawbacks

Drawbacks to this method include:

-   An additional process is created
-   The extract set must be placed in a location where your data source can access it

## Alternative method

[LDAP refresh filters](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/ldap-integration/r_LDAPRefreshFilters.md) use multiple import jobs to divide different types of user records, segregating records for separate processing.

