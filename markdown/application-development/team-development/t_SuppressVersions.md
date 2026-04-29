---
title: Suppress versions
description: Administrators can configure a table so that it does not track customizations in the Versions \[sys\_update\_version\] table.
locale: en-US
release: australia
product: Team Development
classification: team-development
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Versions, Administer, Team Development, Planning your application, Building applications]
---

# Suppress versions

Administrators can configure a table so that it does not track customizations in the Versions `[sys_update_version]` table.

## Before you begin

Role required: none.

## About this task

**Warning:** If you suppress versions for tables, Team Development may work incorrectly, and you may be unable to compare and revert versions of records on the tables.

## Procedure

1.  Navigate to **sys\_properties.list**.

2.  Create a new property:

    -   Name: glide.update.suppress\_update\_version
    -   Type: string
    -   Value: a comma-separated list of tables. The default value is sys\_user,sys\_import\_set\_row.

**Parent Topic:**[Versions](../concept/c_Versions.md)

