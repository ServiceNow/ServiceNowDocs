---
title: Verify agent functionality
description: Verify that an agent is running properly by performing a self-test on the agent. If one or more of the tests fail, you can diagnose the agent problem and view a potential resolution.
locale: en-US
release: australia
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Collect data from your system devices, ACC deployment - shared between servers and endpoints, Configuring Agent Client Collector, Agent Client Collector, IT Operations Management]
---

# Verify agent functionality

Verify that an agent is running properly by performing a self-test on the agent. If one or more of the tests fail, you can diagnose the agent problem and view a potential resolution.

## Before you begin

Role required: agent\_client\_collector\_admin

## Procedure

1.  Navigate to **All** &gt; **Agent Client Collector** &gt; **Agents**.

2.  Select an agent that is running \(**Status = Up**\).

3.  In the **Related Links** section, select **Run self-test**.

4.  The **Agent Self Test Runs** page appears, displaying the previous self-tests run on the agent.

    If the current test doesn’t appear, refresh the page.

5.  Hover next to the entry for the current test and select the info icon ![](../../health-log-analytics-operator/image/icon-info.png).

    The **Agent Self Test Run** pop-up window appears.

6.  Select **Open Record**.

    The Agent Self Test Run page appears, displaying information on the self test.

7.  In the **Agent Self Test Results** table at the bottom of the page, locate a test with **Status = Fail**.

8.  Hover next to the entry for the failed test and select the info icon ![](../../health-log-analytics-operator/image/icon-info.png).

    The **Agent Self Test Results** pop-up window appears.

9.  Select **Open Record**.

    The Agent Self Test Results page appears, displaying information on the failed test.


## Result

In the **Agent Self Test Logs** table on the bottom of the page, you can view the level of the failed test \(ERROR or WARNING\), and a resolution for the failed test.

