---
title: Inactive LDAP user accounts
description: Detect that an existing, current, user account is inactive or has been disabled or deleted from an Active Directory \(AD\) LDAP.
locale: en-US
release: xanadu
product: LDAP integration
classification: ldap-integration
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [LDAP record synchronization, LDAP integration, Authentication, Access Management]
---

# Inactive LDAP user accounts

Detect that an existing, current, user account is inactive or has been disabled or deleted from an Active Directory \(AD\) LDAP.

A common LDAP integration issue is how to detect disabled or deleted users in an Active Directory \(AD\) and then deactivate them in the instance. In an Active Directory LDAP, a filter is usually set to exclude inactive users when refreshing, so the instance is not aware of users that are disabled or deleted in AD. The issue is how to detect that an existing, current user is inactive or has been deleted from AD.

For more information on locating inactive accounts, see [Find inactive LDAP accounts by using the userAccountControl field](https://servicenow.com/docs/bundle/xanadu-platform-security/page/integrate/ldap/task/t_FindInactLDAPAcctsWUsrAcctCtrlFld.html).

**Note:** The recommended approach is to deactivate user records and all other types of records, not delete them. Each record is linked to other records, and deleting a record destroys all the relationships to those other records. Deactivating records keeps those relationships in place.

