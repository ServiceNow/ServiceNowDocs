---
title: Configure SLA retroactive start and pause
description: You can use retroactive start to retain timing information for an SLA when a task record changes. Retroactive pause prevents immediate breaches and notifications when retroactive start is enabled for SLA definitions.
locale: en-US
release: xanadu
product: Service Level Management
classification: service-level-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configuring Service Level Management, Service Level Management, IT Service Management]
---

# Configure SLA retroactive start and pause

You can use retroactive start to retain timing information for an SLA when a task record changes. Retroactive pause prevents immediate breaches and notifications when retroactive start is enabled for SLA definitions.

## Before you begin

Role required: admin

## About this task

When a task record changes, typically a new SLA may be attached, with a new set of timing information. This is useful if you are re-assigning an incident to another group and want to attach a new SLA record with new timing information.

However, you may want to retain time information for the task in specific situations. For example, an incident is raised with a priority of **3 - Moderate** and the priority changes to **1 - Critical** after 3 hours. A priority 1 SLA is attached to the incident at that time. You can use retroactive start to ensure this SLA timing is adjusted retroactively to count from when the incident was first created, rather than from when the incident's priority changed. This reflects the actual time the user contacted you.

You can use the retroactive pause property to apply pause times to the new SLA.

## Procedure

1.  Navigate to **All** &gt; **Service Level Management** &gt; **SLA** &gt; **SLA Definitions**.

2.  Open the relevant SLA definition record.

3.  In the **Start Condition** section, select the **Retroactive start** check box.

4.  From the **Set start to**, select the event from which the SLA starts.

    This option determines the start time used for every task SLA record created from this SLA definition.

    For example, you can select **Opened** to start the SLA from when the task form was initially opened to create the record, which accurately reflects the time the end user contacts the service desk. Alternatively, you can select **Created** to start the SLA from when the task form was initially saved.

5.  To enable the retroactive pause property, select the **Retroactive pause** check box.

    Enabling this property ensures that the new task SLA record gets any pause time that would have been accumulated during the period between the retroactive start time and now. This pause time increases the breach time with the appropriate amount.

6.  Click **Update**.


## What to do next

When retroactive start is enabled, it may result in task SLAs being breached as soon they attach, which will trigger multiple notifications. To prevent the workflow from being processed for these breached SLAs, set the **com.snc.sla.workflow.run\_for\_breached** property to false.

**Parent Topic:**[Configuring Service Level Management](../concept/configuring-service-level-management.md)

