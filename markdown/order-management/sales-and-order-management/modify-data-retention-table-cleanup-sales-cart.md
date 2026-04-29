---
title: Modifying the data retention and table cleanup policy for the Sales Cart application
description: A default data retention and table cleanup policy automatically deletes records from the Sales Cart application based on predefined conditions. You can modify these conditions to match your organization's policies.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Business Portal, Configure, Sales and Order Management]
---

# Modifying the data retention and table cleanup policy for the Sales Cart application

A default data retention and table cleanup policy automatically deletes records from the Sales Cart application based on predefined conditions. You can modify these conditions to match your organization's policies.

By default, records in the complete state are deleted from the Sales Cart \[sn\_sales\_cart\] table if they meet either of the following conditions:

-   Records older than six months
-   Records that haven't been updated for more than six months

Modify the data retention and table cleanup frequency depending on your expected load and volume. For more information, see [Modify data retention policy for ATF test results](https://www.servicenow.com/docs/access?context=atf-edit-table-cleanup&version=australia&pubname=australia-application-development&ft:locale=en-US).

**Related topics**  


[Table cleanup](https://www.servicenow.com/docs/access?context=table-cleanup&version=australia&pubname=australia-application-development&ft:locale=en-US)

[Autoflush form](https://www.servicenow.com/docs/access?context=atf-auto-flush&version=australia&pubname=australia-application-development&ft:locale=en-US)

