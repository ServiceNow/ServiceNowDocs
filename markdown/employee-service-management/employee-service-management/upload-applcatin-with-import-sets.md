---
title: Upload job applications using import sets
description: Upload job application data from your ATS to your ServiceNow instance at regular intervals using import sets.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
---

# Upload job applications using import sets

Upload job application data from your ATS to your ServiceNow instance at regular intervals using import sets.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Import Sets** &gt; **Load data**.

2.  On the form, fill in the fields.

    For a description of the field values, see [Load data form](../reference/import-set-table.md).

    **Note:** In the **Import set table** field, select **Existing table** and add Job Application Staging \[sn\_ta\_connector\_job\_application\_staging\] table.

    The table is available with the base system.

3.  Select **Submit**.

    You can download the import set template too. For more information, see [Download an import template](https://www.servicenow.com/docs/access?context=t_DownloadAnImportTemplate&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US).

4.  In the Next steps section, select **Run Transform** related link.

5.  In the specify Import set and Transform map, select **Transform**.

6.  Select **Transform history** related link to check for errors in the **Import set Row Errors** tab.


## Result

The job application list is updated with the imported data.

**Parent Topic:**[Integrate with your ATS](../concept/integrate-ats.md)

