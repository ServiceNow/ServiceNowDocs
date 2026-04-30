---
title: Application file protection policy
description: A read-only protection policy prevents anyone from modifying an application file or its related record.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Application files, Anatomy of an application, Learning about developing on the ServiceNow AI Platform, Building applications]
---

# Application file protection policy

A read-only protection policy prevents anyone from modifying an application file or its related record.

Some application code shipped with the ServiceNow system requires special protection. Only a ServiceNow employee can alter the protection policy and then modify the application file or its related record. A ServiceNow employee cannot edit protected files without changing the policy designation first.

To prevent customizations from being overwritten by system upgrades, the upgrade process automatically skips changes to customer-updated records. If you modify an application file or related record that is later designated as Read-only in an upgrade, the application file maintains the default protection policy of Write. You keep the existing modifications and can continue modifying the records.

**Note:** Reverting a customized file to its baseline state causes the record to inherit the new protection policy as well. For example, a record going from a Write protection policy to a Read-only protection policy.

