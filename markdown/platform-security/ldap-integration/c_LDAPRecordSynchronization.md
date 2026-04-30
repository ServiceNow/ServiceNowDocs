---
title: LDAP record synchronization
description: Administrators can synchronize inactive, disabled, or deleted LDAP records with their LDAP records.
locale: en-US
release: yokohama
product: LDAP integration
classification: ldap-integration
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [LDAP integration, Authentication, Access Management]
---

# LDAP record synchronization

Administrators can synchronize inactive, disabled, or deleted LDAP records with their LDAP records.

LDAP record synchronization is the process of detecting inactive records on the LDAP server and updating the corresponding LDAP records. Detecting inactive LDAP records involves defining consistent data indicators for each user object, importing LDAP data, and evaluating the data indicators.

A data indicator can be:

-   A date field
-   Membership in a specific OU \(identify by parsing the **dn** attribute\), using the **useraccountcontrol** attribute
-   A combination of these indicators

Imported data comes into the instance through import set tables where the data can be evaluated and processed.

The import process can use [LDAP refresh filters](../reference/r_LDAPRefreshFilters.md)on multiple import jobs to divide different types of user records and segregarte records for separate processing.

