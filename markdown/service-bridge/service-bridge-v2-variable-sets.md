---
title: Using variable sets with Remote Record Producers
description: Use single and multi-row variable sets with remote record producers.
locale: en-US
release: zurich
product: Service Bridge
classification: service-bridge
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Remote record producers, Create remote catalogs, Install and configure for provider, Service Exchange for Providers, Service Exchange]
---

# Using variable sets with Remote Record Producers

Use single and multi-row variable sets with remote record producers.

Variable sets allow you to create a collection of variables that can be reused across multiple catalog items and order guides. Using variable sets saves time because you do not have to create the same variables individually for many catalog items. Also, when variables should be modified, you can modify the variable set and the changes are reflected across all the remote record producers that are associated with the variable set.

As a provider, you can create and associate variable sets with remote record producers. Any changes made to these variable sets are automatically synced to the remote record producers that the consumers are entitled to. You can create the following types of variable sets:

-   Single-row variable set: Use a single-row variable set to capture data from variables that are grouped together.
-   Multi-row variable set: Use a multi-row variable set to capture variable data in a grid layout for a group of entities. For example, for HR during the reorganization of employees, a single remote record producer should be able to capture the relevant information such as the department and manager for a group of employees.

**Note:**

-   Variable sets containing variables with unsupported variable types \(Custom, Custom with Label, and UIPage\) will not be synced until the invalid variables are removed.
-   Remote record producers containing invalid variable sets cannot be published. To publish the remote record producer, you must either resolve the validation issues or unassign the invalid variable set from the remote record producer.

For more details on variable sets and how they are used, see [Service catalog variable sets](https://www.servicenow.com/docs/access?context=c_ServiceCatalogVariableSets&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

