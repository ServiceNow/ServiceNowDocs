---
title: Block event creation for non-existent entities
description: Invoke the skip\_events\_for\_nonexistent parameter to block event creation when specific process, service, or log does not exist. Invoke this parameter if you do not want to be notified about these non-existent entities.
locale: en-US
release: australia
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [ACC deployment - shared between servers and endpoints, Configuring Agent Client Collector, Agent Client Collector, IT Operations Management]
---

# Block event creation for non-existent entities

Invoke the **skip\_events\_for\_nonexistent** parameter to block event creation when specific process, service, or log does not exist. Invoke this parameter if you do not want to be notified about these non-existent entities.

## Before you begin

Role required: agent\_client\_collector\_admin

## About this task

A process, service, or log does not exist when the following checks do not contain valid values for the indicated parameters:

|Check|Parameter|
|-----|---------|
|os.linux.check-process|**file\_pid**, **daemon\_name**|
|util.check-windows-service|**service**|
|os.windows-check-log|**file**|
|util.checks-logs|**file**|
|util.checks-logs-sudo|**file**|

## Procedure

1.  Navigate to **All** &gt; **Agent Client Collector** &gt; **Configuration** &gt; **Check Definitions**.

2.  Locate the check definition for which you want to block events.

3.  On the **Check Parameter Definitions** tab, select **skip\_events\_for\_nonexistent**.

4.  Select the **Active** check box to enable the parameter and prevent alert creation when the process, service, or log isn’t located for the specified check.

    If you want to receive notification about the missing process or service, leave the **skip\_events\_for\_nonexistent** parameter with its default value of **false**.


**Parent Topic:**[Deploying Agent Client Collector on both servers and endpoints](../concept/acc-shared-deployment.md)

