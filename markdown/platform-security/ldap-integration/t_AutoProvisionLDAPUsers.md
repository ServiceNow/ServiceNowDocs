---
title: Auto provision LDAP users
description: You automatically provision users who are in the LDAP server but not yet in your instance.
locale: en-US
release: xanadu
product: LDAP integration
classification: ldap-integration
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [LDAP integration setup, LDAP integration, Authentication, Access Management]
---

# Auto provision LDAP users

You automatically provision users who are in the LDAP server but not yet in your instance.

## Before you begin

Role required: admin

## Procedure

-   Create the following properties in the System Properties \[sys\_properties\] table:

    |LDAP property|Description|
    |-------------|-----------|
    |glide.ldap.authentication|Enables LDAP authentication by using LDAP to authenticate users. Set this property to **true** \(the default value\).|
    |glide.ldap.user.autoprovision|Enables LDAP the system to automatically create users in the User \[sys\_user\] table when the user exists in LDAP but is not yet in the instance. Set this property to **true** \(the default value\).|

    Both of these properties must be set to **true** for auto-provisioning to work.


