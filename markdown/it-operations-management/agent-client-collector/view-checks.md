---
title: Create and edit checks
description: You can select a check based on the type of entity \(such as a server or an application\) you want to monitor. You can view and edit the default checks or create new checks, as needed.
locale: en-US
release: yokohama
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Collect data from your system devices, Agent Client Collector Framework, Agent Client Collector, IT Operations Management]
---

# Create and edit checks

You can select a check based on the type of entity \(such as a server or an application\) you want to monitor. You can view and edit the default checks or create new checks, as needed.

## Before you begin

Role required: agent\_client\_collector\_admin

## Procedure

1.  Navigate to **All** &gt; **Agent Client Collector** &gt; **Check Definitions**.

2.  Click **New**.

    The **Check Definition** page appears.

    **Note:** Using Ruby scripts in a Windows environment causes high CPU consumption.

3.  Enter values in the fields on the page, as described in [Agent Client Collector check definition page](../reference/check-definition-form.md).

4.  On the **Parameters** tab, enter parameter definitions, as needed.

    Parameters are used for the **Command** field when the Simple template is used, as described in [Agent Client Collector check definition page](../reference/check-definition-form.md).

    The information you can add for parameters is described in [Check definition form parameters tab](../reference/check-definition-parameters-tab.md).


