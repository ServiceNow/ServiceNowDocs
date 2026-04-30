---
title: Configure a table for escalation trigger rules
description: Configure escalation trigger rules for the tables that do not extend tasks.
locale: en-US
release: yokohama
product: On-Call Scheduling
classification: on-call-scheduling
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Designing an escalation process, Escalations in On-Call Scheduling, Define escalation process, On-Call Scheduling, IT Service Management]
---

# Configure a table for escalation trigger rules

Configure escalation trigger rules for the tables that do not extend tasks.

## Before you begin

Role required: admin

## About this task

Tables that are configured in the Trigger Rule Table Configuration \[trigger\_rule\_table\_cfg\] table do appear in the **Table** field in the Trigger Rule form for creating an escalation trigger rule.

## Procedure

1.  Navigate to **All** &gt; **On-Call Administration** &gt; **Administration** &gt; **Trigger Rule Table Configuration**.

2.  Click **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Table|Name of the table that will be enabled for creating escalation trigger rules.|
    |Trigger group field|Group field value in the table based on which trigger rule processes.|
    |Trigger user field|User field value in the table based on which trigger rule processes.|
    |Journal field|The ongoing escalation activity.|

4.  Click **Submit**.

    The Trigger Rules related list shows the escalation trigger rules that are configured for the table.


**Parent Topic:**[Designing an escalation process](../concept/designing-escalation-process-oncall.md)

