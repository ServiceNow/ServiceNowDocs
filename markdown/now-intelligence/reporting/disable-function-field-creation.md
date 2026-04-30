---
title: Disable function field creation
description: Configure a system property to remove the ability to create function fields in the Report Designer.
locale: en-US
release: xanadu
product: Reporting
classification: reporting
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Report on function fields, Advanced reporting topics, Reporting, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Disable function field creation

Configure a system property to remove the ability to create function fields in the Report Designer.

## Before you begin

Role required: admin.

## Procedure

1.  Navigate to **All** &gt; **sys\_properties.list**.

2.  Search for the property **glide.report.enable\_function\_field\_ui**.

3.  Select the property's name to open its form.

4.  Set the property's value to `false`.

5.  Select **Update**.


## Result

The option to configure function fields does not appear in the Report Designer for any user.

**Parent Topic:**[Report on function fields](../concept/function-fields-reporting.md)

