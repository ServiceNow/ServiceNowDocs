---
title: Expand domain scope
description: By default, when a user in the global domain views a table containing a sys\_overrides column, the user sees records from only the global domain. When an admin in the global domain views a process table, that admin sees only records that are in that process table.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [View domain relationships, Domain separation setup and administration, Domain separation for service providers, Access Management]
---

# Expand domain scope

By default, when a user in the global domain views a table containing a **sys\_overrides** column, the user sees records from only the global domain. When an admin in the global domain views a process table, that admin sees only records that are in that process table.

## Before you begin

Role required: admin

## Procedure

1.  Change the **glide.sys.restrict\_global\_domain\_processes** property to **true**.

2.  To view records from all domains, click **Expand Domain Scope** under Related Links.

3.  To return to viewing records from the global domain only, click **Collapse Domain Scope**.


