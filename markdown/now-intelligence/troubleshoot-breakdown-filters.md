---
title: Troubleshoot breakdown filters
description: In Platform Analytics experience, it's not possible to do extend the functionality of a migrated breakdown filter that doesn't have an associated indicator.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-10-09"
reading_time_minutes: 1
breadcrumb: [Edit filters on dashboards, Filters, Platform Analytics experience, Platform Analytics]
---

# Troubleshoot breakdown filters

In Platform Analytics experience, it's not possible to do extend the functionality of a migrated breakdown filter that doesn't have an associated indicator.

## Before you begin

Role required: Dashboard owner

This task describes how to address the error `This option is not available for the specified filter source` when you try to update a breakdown without an associated indicator.

## Procedure

1.  Navigate to **All** &gt; **Library** &gt; **Dashboards**.

2.  Open the dashboard with the problem.

3.  Select **Edit**.

4.  Select the filter to view its configuration.

5.  Choose the **Data to filter** option.

    The error `This option is not available for the specified filter source` appears.

6.  Identify the name of the indicator breakdown under **Filter source**.

7.  Navigate to `pa_breakdowns.list` and open the breakdown.

8.  On the breakdown record, open the **Indicators** tab under **Related links**.

9.  Select **Edit** and choose one or more indicators that the breakdown applies to.

10. Select **Update**.


## Result

You can edit the **Data to filter** section of the filter configuration.

