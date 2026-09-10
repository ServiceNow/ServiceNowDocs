---
title: Discover only the latest operating system patch versions
description: Collect only the current operating system patch level by configuring the sn\_itom\_pattern.discover\_latest\_os\_patches MID Server property. Collecting only the current patch is supported only for AIX Server discovery.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/itom-visibility/enable-latest-patch-discovery.html
release: australia
product: ITOM Visibility
classification: itom-visibility
topic_type: task
last_updated: "2026-08-18"
reading_time_minutes: 1
keywords: [Unix discovery, AIX discovery, HP-UX discovery, Solaris discovery, patch discovery, cmdb\_ci\_patches]
breadcrumb: [Operating systems discovery, Data collected by ITOM Visibility, ITOM Visibility reference, ITOM Visibility, IT Operations Management]
---

# Discover only the latest operating system patch versions

Collect only the current operating system patch level by configuring the **sn\_itom\_pattern.discover\_latest\_os\_patches** MID Server property. Collecting only the current patch is supported only for AIX Server discovery.

## Before you begin

Verify that you have at least version 6.35.0 of Visibility Content.

Role required: discovery\_admin

## About this task

By default, Discovery adds a record to the Patches \[cmdb\_ci\_patches\] table for every patch reported by the server, including older patch versions. The **sn\_itom\_pattern.discover\_latest\_os\_patches** MID Server property controls this behavior; the default value is false. When set to true, Discovery evaluates all patches reported by the server and identifies the latest patch level. Only that patch is populated as active in the CMDB.

## Procedure

1.  Navigate to **All** &gt; **MID Server** &gt; **Properties**.

2.  In the **Name** column, search for `sn_itom_pattern.discover_latest_os_patches`.

3.  Select the **sn\_itom\_pattern.discover\_latest\_os\_patches** MID Server property.

4.  In the **Value** field, enter `true`.

    To revert to the default behavior and collect all patch versions on each run, set the value to `false`.

5.  Select **Submit**.


## What to do next

Run Discovery again to apply the change.

**Parent Topic:**[Operating systems discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-visibility/c_Computers.md)

**Related topics**  


[AIX server discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-visibility/r_DataCollDiscoAIXComputers.md)

