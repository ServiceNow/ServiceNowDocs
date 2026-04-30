---
title: Migrate software installations
description: If you are using Discovery, run this script after installing the Software Asset Management application to copy previously discovered software installation records from the \[cmdb\_software\_instance\] table to the \[cmdb\_sam\_sw\_install\] table, which is used by the Software Asset Management application to store software installation records.
locale: en-US
release: yokohama
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Software Asset Management administration, Software Asset Management, IT Asset Management]
---

# Migrate software installations

If you are using Discovery, run this script after installing the Software Asset Management application to copy previously discovered software installation records from the \[cmdb\_software\_instance\] table to the \[cmdb\_sam\_sw\_install\] table, which is used by the Software Asset Management application to store software installation records.

## Before you begin

Role required: sam\_admin

## About this task

If you are running Discovery and have used a version of Software Asset Management previously, there is no need to run this script.

When running the Migrate Software Installs script, allow enough time for the process to complete.

## Procedure

1.  Navigate to **All** &gt; **Software Asset** &gt; **Administration** &gt; **Migrate Software Installs** and select **Proceed**.

    The Software Installations list is shown. If the data has already been migrated, a message is shown.


**Parent Topic:**[Software Asset Management administration](../concept/c_SAMAdministration.md)

