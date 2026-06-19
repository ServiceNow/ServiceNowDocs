---
title: Developer Sandboxes and metadata
description: Each sandbox provisioned with Developer Sandboxes is an isolated environment within an instance. Developers can build and test in parallel without affecting other work.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/developer-sandboxes/dev-sbx-metadata.html
release: australia
product: Developer Sandboxes
classification: developer-sandboxes
topic_type: concept
last_updated: "2026-06-09"
reading_time_minutes: 2
breadcrumb: [Explore, Developer Sandboxes, Developing your application, Building applications]
---

# Developer Sandboxes and metadata

Each sandbox provisioned with Developer Sandboxes is an isolated environment within an instance. Developers can build and test in parallel without affecting other work.

Sandboxes can be allocated to specific stories, developers, test plans, or any custom criteria.

## Developer Sandboxes and metadata configuration

Each sandbox is initialized with the full metadata of the base instance. For example, the metadata includes scripts and business rules.

Any changes made to metadata configuration in the sandbox don't affect the base instance until changes are merged. For example, you can activate a plugin on a sandbox, and it isn't activated on the base instance. Sandboxes isolate risky changes from the base instance and other sandboxes.

User credentials and roles are isolated to each sandbox. Changing a user's role in a sandbox doesn't affect other sandboxes or the base instance.

Any changes to metadata configuration must first be committed from the sandbox into the base instance. The Developer Sandboxes administrator must then merge the changes back into the base instance. The changes are then available for the next provisioned sandbox, but not for existing sandboxes.

## Developer Sandboxes and table data

Table data behavior in sandboxes depends on how each table is configured. By default, tables use the Shared configuration. Tables that extend sys\_metadata are configured as Full Copy.

Each table in a sandbox instance can be configured with one of the following data modes:

-   **Shared**

    The default configuration \(introduced in the Zurich release\). Table data is shared across the base instance and all sandboxes. All changes, additions, and deletions to records are visible across all sandboxes.

-   **Full Copy**

    Table data is copied in full from the base instance to each sandbox at the time the sandbox is created. Sandboxes receive a snapshot of the data. All subsequent record changes are isolated to the sandbox.

-   **Zero Copy**

    The table is isolated, but no data is copied from the base instance. Sandboxes start with no records in that table. All record changes are isolated to the sandbox.

-   **Partial Copy**

    Data is copied from the base instance based on a filter condition. This option has limited usability due to cross-table references.


**Note:** To change the Task or CMDB tables, contact Now Support.

To view the current table configurations, view `sys_dsb_table_config`. Table configuration is set at the base or parent table for all inherited tables.

Records created in a sandbox on a Shared table are immediately available on the base instance and any other sandbox that shares that table. For isolated tables \(Full Copy, Zero Copy, or Partial Copy\), record changes remain isolated to that sandbox. Making a schema change also isolates the table, and any records added after that point are isolated.

To generate synthetic test data, use Now Assist Data Kit. For more information, see .

## Developer Sandboxes and business rules

Business rules are metadata inherited from the base instance. You can see business rules on a sandbox by navigating to **All** &gt; **Administration** &gt; **Business rules**.

Business rules are copied, but isolated. For more information on Business rules, see .

