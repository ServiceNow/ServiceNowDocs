---
title: Migrate Software Asset Management Foundation plugin software installations
description: If you are using Discovery, run this script after installing Software Asset Management Foundation plugin to copy previously discovered software installation records from the \[cmdb\_software\_instance\] table to the \[cmdb\_sam\_sw\_install\] table, which is used by Software Asset Management Foundation plugin to store software installation records.
locale: en-US
release: australia
product: Software Asset Management Foundation plugin
classification: software-asset-management-foundation-plugin
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Software Asset Management Foundation plugin Administration, Software Asset Management Foundation plugin, ITSM Software Asset Management, Asset Management, IT Service Management]
---

# Migrate Software Asset Management Foundation plugin software installations

If you are using Discovery, run this script after installing Software Asset Management Foundation plugin to copy previously discovered software installation records from the \[cmdb\_software\_instance\] table to the \[cmdb\_sam\_sw\_install\] table, which is used by Software Asset Management Foundation plugin to store software installation records.

## Before you begin

Role required: sam\_admin

## About this task

If you are running Discovery and have used a version of [ITSM Software Asset Management](../../asset-management/concept/itsm-sam.md) previously, there is no need to run this script. Additionally, if the \[cmdb\_sam\_sw\_install\] table is already populated with software installation records, this script is disabled. You can run Discovery again to repopulate the table.

When running the Migrate Software Installs script, allow enough time for the process to complete.

## Procedure

1.  Navigate to **All** &gt; **Software Asset** &gt; **Administration** &gt; **Migrate Software Installs** and click **Procced**.

    The Software Installations list is shown. If the data has already been migrated, a message is shown.


**Parent Topic:**[Software Asset Management Foundation plugin Administration](../concept/c_SAMAdministrationSAMF.md)

