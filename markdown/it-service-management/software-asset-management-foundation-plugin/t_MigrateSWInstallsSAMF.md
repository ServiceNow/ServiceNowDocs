---
title: Migrate Basic Software Asset Management software installations
description: If you are using Discovery, run this script after installing Basic Software Asset Management to copy previously discovered software installation records from the \[cmdb\_software\_instance\] table to the \[cmdb\_sam\_sw\_install\] table, which is used by Basic Software Asset Management to store software installation records.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/software-asset-management-foundation-plugin/t\_MigrateSWInstallsSAMF.html
release: brazil
product: Software Asset Management Foundation plugin
classification: software-asset-management-foundation-plugin
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Basic Software Asset Management Administration, Basic Software Asset Management, ITSM Software Asset Management, Asset Management common applications, IT Service Management]
---

# Migrate Basic Software Asset Management software installations

If you are using Discovery, run this script after installing Basic Software Asset Management to copy previously discovered software installation records from the \[cmdb\_software\_instance\] table to the \[cmdb\_sam\_sw\_install\] table, which is used by Basic Software Asset Management to store software installation records.

## Before you begin

Role required: sam\_admin

## About this task

If you are running Discovery and have used a version of [ITSM Software Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/itsm-sam.md) previously, there is no need to run this script. Additionally, if the \[cmdb\_sam\_sw\_install\] table is already populated with software installation records, this script is disabled. You can run Discovery again to repopulate the table.

When running the Migrate Software Installs script, allow enough time for the process to complete.

## Procedure

1.  Navigate to **All** &gt; **Software Asset** &gt; **Administration** &gt; **Migrate Software Installs** and click **Procced**.

    The Software Installations list is shown. If the data has already been migrated, a message is shown.


**Parent Topic:**[Basic Software Asset Management Administration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/software-asset-management-foundation-plugin/c_SAMAdministrationSAMF.md)

