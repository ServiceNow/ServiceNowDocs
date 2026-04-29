---
title: Modifying data retention and table cleanup policy for Lead-to-Cash Process Management
description: Modify the default data retention and table cleanup policy for Lead-to-Cash Process Management to match your organizations requirements.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Lead-to-Cash Process Management, Order operations apps, Configure, Sales and Order Management]
---

# Modifying data retention and table cleanup policy for Lead-to-Cash Process Management

Modify the default data retention and table cleanup policy for Lead-to-Cash Process Management to match your organizations requirements.

By default, records are deleted from the Business Process Record \[sn\_bo\_core\_process\_record\] and Sales Process Record \[sn\_l2c\_cockpit\_sales\_process\_record\] tables and child records in the Business Process Task \[sn\_bo\_core\_process\_task\] and Business Process Resource \[sn\_bo\_core\_process\_resource\] tables if they meet either of the following conditions:

-   In an inactive state and not updated in the past six months
-   In an active state but not updated in the past year

You can modify the data retention and table cleanup policy depending on your expected load and volume.

To find out how to modify the data retention and table cleanup frequency for Lead-to-Cash Process Management, see [Modify data retention policy for ATF test results](https://www.servicenow.com/docs/access?context=atf-edit-table-cleanup&version=australia&pubname=australia-application-development&ft:locale=en-US).

**Related topics**  


[Table cleanup](https://www.servicenow.com/docs/access?context=table-cleanup&version=australia&pubname=australia-application-development&ft:locale=en-US)

[Autoflush form](https://www.servicenow.com/docs/access?context=atf-auto-flush&version=australia&pubname=australia-application-development&ft:locale=en-US)

