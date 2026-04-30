---
title: Create multi topics in the LES source table
description: Consume messages for each source type independently by creating a unique topic per source type.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Create a log source configuration, Log Export Service \(LES\), Platform Security]
---

# Create multi topics in the LES source table

Consume messages for each source type independently by creating a unique topic per source type.

## Before you begin

Role required: admin

## Procedure

1.  Add the sn\_logstoanalytics.kafka.multi\_topics system property and set it to True.

    It is set to False by default.

2.  Create a new source record.

    **Note:** When you create a new source type, a unique topic is created for it.

    The topic names have the suffix as the source type. For example, sn\_logstoanalytics.node\_log has the node\_log as the source type.

3.  Create another topic for a different source as in the previous steps.

    **Note:** If the sn\_logstoanalytics.kafka.multi\_topics is set to False, the ability to create multi topics in the source table is disabled.

    **Note:** This feature is not compatible with the MID server consumer \(LES v2\). You must use your own consumer \(LES v1\).


**Parent Topic:**[Create a log source configuration](les-create-source-configuration.md)

