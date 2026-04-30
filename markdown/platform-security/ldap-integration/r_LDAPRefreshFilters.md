---
title: LDAP refresh filters
description: Filters on the LDAP refresh process can be used to specify processing that ignores inserts of disabled users.
locale: en-US
release: xanadu
product: LDAP integration
classification: ldap-integration
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [LDAP record synchronization, LDAP integration, Authentication, Access Management]
---

# LDAP refresh filters

Filters on the LDAP refresh process can be used to specify processing that ignores inserts of disabled users.

You can loosen the LDAP OU filter to bring all of the data in to your import set table \(including inactive users\) and then specify processing that ignores inserts of disabled users. The sample ‘Users’ OU definition that the instance provides in its out-of-box LDAP sample contains a filter.

This filter is important because it defines which user records are brought into the import set table to be evaluated. While achieving a smaller data load, a limitation of this filter is that it filters out inactive users, so the inactive user records are not imported into the import set temporary tables. Since there is not visibility of the inactive user records, there is no ability to evaluate the record indicators.

![](../image/LDAPOUdefinition.png)

To use filtering within the main LDAP refresh process, change the filter to bring in all of the user records. The result is that all the records will be loaded into the import set temporary table where they can be evaluated and transformed.

**Note:** There is a precaution here: because the filtering brings in all the records, you may end up with a vast amount of older inactive LDAP accounts that should not be inserted into the instance. A user record should never be created for a disabled user.

