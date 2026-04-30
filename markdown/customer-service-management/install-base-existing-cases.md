---
title: Migrating the install base information for existing cases
description: Your customer service agents can use the case form on the CSM Agent Workspace to add an install base item to an existing case.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Create a case for a new install base item, Case form, Customer Service forms, Customer Service Management reference, Customer Service Management]
---

# Migrating the install base information for existing cases

Your customer service agents can use the case form on the CSM Agent Workspace to add an install base item to an existing case.

To populate existing cases with the install base information, agents can use the following sample script:

```
var installBaseMigrationUtil = new sn_install_base.InstallBaseMigrationUtils();​ 
installBaseMigrationUtil.populateInstallBaseOnCases(); 
```

The migration script populates cases with the install base information, only if the case is associated with the install base item. To associate a case to an install base item, see [Associate multiple install base items to a case](../task/associate-multiple-install-base-items-case.md).

