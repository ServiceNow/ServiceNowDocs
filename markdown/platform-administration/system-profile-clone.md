---
title: Create a custom clone profile \(legacy\)
description: Clone profiles enable you to set up exclusions, preservers, and cleanup scripts for specific clone scenarios.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create a custom clone profile, Configure, Instance Clone, Configure core features, Administer the ServiceNow AI Platform]
---

# Create a custom clone profile \(legacy\)

Clone profiles enable you to set up exclusions, preservers, and cleanup scripts for specific clone scenarios.

## Before you begin

Role required: admin

## About this task

If you leave the clone profile field empty when requesting a clone, the system uses the exclude tables, data preservers, and cleanup scripts configured under **Instance Clone** &gt; **Clone Definition**.

## Procedure

1.  Navigate to **All** &gt; **Instance Clone** &gt; **Clone profiles**.

2.  Select **New**.

3.  Fill in the form.

    For field information, see [Clone options](clone-options.md).

4.  Select **Submit**.

    If you create a data preserver, exclusion, or cleanup script, it isn't automatically added to your clone profiles.

5.  To add a preserver, exclusion, or cleanup script to a clone profile.

    1.  Navigate to **Additional actions** &gt; **Configure** &gt; **Form Layout**.

    2.  Add the preserver, exclusion, or cleanup script to the selected list.


