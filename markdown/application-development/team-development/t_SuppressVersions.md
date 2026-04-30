---
title: Suppress versions
description: Administrators can configure a table so that it doesn’t track customizations in the Versions \[sys\_update\_version\] table.
locale: en-US
release: zurich
product: Team Development
classification: team-development
topic_type: task
last_updated: "2025-10-02"
reading_time_minutes: 1
breadcrumb: [Working with version records, Team Development, Planning your application, Building applications]
---

# Suppress versions

Administrators can configure a table so that it doesn’t track customizations in the Versions `[sys_update_version]` table.

## Before you begin

Role required: admin

## About this task

**Warning:** Suppressing versions for tables can create an error, making you unable to compare and revert versions of records on the tables.

## Procedure

1.  Navigate to **sys\_properties.list**.

2.  Create a property:

    1.  Name: `glide.update.suppress_update_version`

    2.  Type: string

    3.  Value: a comma-separated list of tables.

        The default value is sys\_user, sys\_import\_set\_row.


**Parent Topic:**[Working with version records](../concept/c_Versions.md)

