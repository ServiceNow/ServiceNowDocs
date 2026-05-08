---
title: Developer Sandboxes and metadata
description: Each sandbox provisioned with Developer Sandboxes is an isolated environment within an instance, allowing developers to build and test in parallel without impacting other work.
locale: en-US
release: australia
product: Developer Sandboxes
classification: developer-sandboxes
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Explore, Developer Sandboxes, Developing your application, Building applications]
---

# Developer Sandboxes and metadata

Each sandbox provisioned with Developer Sandboxes is an isolated environment within an instance, allowing developers to build and test in parallel without impacting other work.

Sandboxes can be allocated to specific stories, developers, test plans, or any custom criteria.

## Developer Sandboxes and metadata configuration

Each sandbox is initialized with the full metadata of the base instance. For example, scripts and business rules.

Any changes made to metadata configuration in the sandbox do not affect the base instance until changes are merged. For example, you can install a plugin on a sandbox and it won't be installed on the base instance. Developers can use sandboxes to make risky changes without worrying about affecting the base instance or other sandboxes.

User credentials and roles are isolated to each sandbox. Changing a user's role in a sandbox doesn't affect other sandboxes or the base instance.

Any changes to metadata configuration must first be committed from the sandbox into the base instance. The Developer Sandboxes administrator must then merge the changes back into the base instance. The changes are then available for the next provisioned sandbox, but not for existing sandboxes.

## Developer Sandboxes and table data

Any records created in a sandbox are immediately available on the base instance. For example, adding a column to a table is isolated in the sandbox, but if you create an incident in a sandbox, that new record is also created in the incident table in the base instance.

Table data is shared in the following ways:

-   Unless a table is configured to be isolated to the base instance or copied without data, the table will be shared across all sandboxes.
-   Records created in a sandbox on a shared data table are available on the base instance and any other sandbox that shares that table. Making a schema change isolates the table, and any records added after that are also isolated.

## Developer Sandboxes and data templates

When a sandbox is allocated, it inherits the baseline data configuration of scoped apps, unless there is data that can't be copied. For more information on templates, see [Using sandbox templates](../task/create-sandbox-template.md).

## Developer Sandboxes and business rules

Business rules are metadata inherited from the base instance. You can see business rules on a sandbox by navigating to **All** &gt; **Administration** &gt; **Business rules**.

Business rules are copied, but isolated. They are inherited, but changes and additions are isolated on each sandbox. For more information on Business rules, see Classic Business rules.

