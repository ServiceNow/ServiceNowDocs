---
title: Configure a table for escalation trigger rules
description: Configure escalation trigger rules for the tables that do not extend tasks.
locale: en-US
release: australia
product: On-Call Scheduling
classification: on-call-scheduling
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Designing an escalation process, Escalations in On-Call Scheduling, Defining On-Call Scheduling escalation process, On-Call Scheduling, IT Service Management]
---

# Configure a table for escalation trigger rules

Configure escalation trigger rules for the tables that do not extend tasks.

## Before you begin

Role required: admin

## About this task

Tables that are configured in the Trigger Rule Table Configuration \[trigger\_rule\_table\_cfg\] table appear in the **Table** field in the Trigger Rule form for creating an escalation trigger rule.

## Procedure

1.  Navigate to **All** &gt; **On-Call Administration** &gt; **Administration** &gt; **Trigger Rule Table Configuration**.

    In Service Operations Workspace \(SOW\), you can access On-call trigger rule table configuration by navigating to **All** &gt; **Service Operations Workspace Admin Center** &gt; **Overview** &gt; **Configuration**. On the **Configurations** tab, from the **SOW configurations** section, navigate to the **On-call Scheduling** tile and select **Configure** and then select **Table configuration for trigger rules**. For more information, see [Manage configurations in Service Operations Workspace for ITSM](../../../product/service-operations-workspace/task/manage-admin-console-sow-itsm.md)

2.  Select **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Table|Name of the table that will be enabled for creating escalation trigger rules.|
    |Trigger group field|Group field value in the table based on which trigger rule processes.|
    |Trigger user field|User field value in the table based on which trigger rule processes.|
    |Trigger condition fields|List of table fields that are displayed as a choice list in the **Trigger fields** field when creating or editing the trigger rules.|
    |Journal field|The ongoing escalation activity.|

4.  Click **Submit**.

    The Trigger Rules related list shows the escalation trigger rules that are configured for the table.


**Parent Topic:**[Designing an escalation process](../concept/designing-escalation-process-oncall.md)

