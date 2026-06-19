---
title: Run the Agent Client Collector \(ACC\) health instance scan as a scheduled job
description: Run the Run \(ACC\) health instance scan scheduled job to monitor the overall health of the instance receiving data from the Agent Client Collector.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/agent-client-collector/acc-instance-scan-run.html
release: zurich
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2026-05-07"
reading_time_minutes: 1
breadcrumb: [ACC health instance scan suite, ACC deployment - shared between servers and endpoints, Agent Client Collector, IT Operations Management]
---

# Run the Agent Client Collector \(ACC\) health instance scan as a scheduled job

Run the **Run \(ACC\) health instance scan** scheduled job to monitor the overall health of the instance receiving data from the Agent Client Collector.

## Before you begin

Role required: agent\_client\_collector\_admin

## About this task

This procedure describes how to schedule an ACC health instance scan. Alternatively, you can run the ACC health instance scan on demand, as follows:

1.  Navigate to **All** &gt; **Instance Scan** &gt; **Suites**.
2.  Select **ACC Health Instance Scan**.
3.  Select **Execute Suite Scan**.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.

2.  Select the **Run ACC Health Instance Scan** entry.

3.  Select the **Active** check box.

4.  Set the frequency by which the job is to repeat in the **Repeat Interval** field.

    The default is 7 days.

5.  Select **Execute Now** to run the **Run ACC Health Instance Scan** job.


## Result

The results of the job are compiled in the Scan Results \(scan\_result\) table. Errors are compiled in the Agents issue \(sn\_agent\_acc\_error\_msg\) table.

For details on the ACC health instance scan suite checks, see [Agent Client Collector health instance scan checks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/agent-client-collector/acc-instance-scan-checks.md).

**Parent Topic:**[Agent Client Collector health instance scan suite](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/agent-client-collector/acc-instance-scan-suite.md)

