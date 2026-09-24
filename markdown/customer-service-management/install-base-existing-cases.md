---
title: Migrating the install base information for existing cases
description: Your customer service agents can use the case form on the CSM Agent Workspace to add an install base item to an existing case.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/install-base-existing-cases.html
release: brazil
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Create a case for install base items, Case form, Customer Service forms, Reference, Customer Service Management]
---

# Migrating the install base information for existing cases

Your customer service agents can use the case form on the CSM Agent Workspace to add an install base item to an existing case.

To populate existing cases with the install base information, agents can use the following sample script:

```
var installBaseMigrationUtil = new sn_install_base.InstallBaseMigrationUtils();​ 
installBaseMigrationUtil.populateInstallBaseOnCases(); 
```

The migration script populates cases with the install base information, only if the case is associated with the install base item. To associate a case to an install base item, see [Associate multiple install base items to a case](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/associate-multiple-install-base-items-case.md).

