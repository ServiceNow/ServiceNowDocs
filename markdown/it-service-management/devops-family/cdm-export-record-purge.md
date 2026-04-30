---
title: Set the purge period for records of exporter executions
description: Change the default deletion period. By default, records of exporter executions are deleted after a period of three years.
locale: en-US
release: xanadu
product: DevOps \(Family\)
classification: devops-family
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Export a snapshot, Use, DevOps Config, IT Service Management]
---

# Set the purge period for records of exporter executions

Change the default deletion period. By default, records of exporter executions are deleted after a period of three years.

## Before you begin

**Important:** Starting with the Washington DC release, DevOps Config is being prepared for future deprecation. It will be hidden and no longer installed on new instances but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

Role required: CDM Admin \[sn\_cdm.cdm\_admin\]

## Procedure

1.  Navigate to **All** &gt; **System Maintenance** &gt; **Table Cleanup**.

2.  In the **Tablename** column, select **sn\_cdm\_exporter\_execution**.

3.  Change the **Age** setting to the retention period in seconds and then save the record.

    Minimum: 1 year. For example:

    -   1 year = 31 536 000
    -   2 years = 63 072 000
    -   3 years = 94 608 000

