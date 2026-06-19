---
title: Run a mass upgrade via the scheduled Agent Client Collector upgrade job
description: Activate the built-in scheduled job to upgrade all eligible Agent Client Collector agents automatically in rate-limited batches.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/agent-client-collector/enable-agent-upgrade-scheduled-job.html
release: australia
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2026-05-28"
reading_time_minutes: 1
keywords: [ACC scheduled upgrade, Upgrade agents incrementally, mass upgrade]
breadcrumb: [Agent Client Collector upgrade overview, ACC deployment - servers, Configuring Agent Client Collector, Agent Client Collector, IT Operations Management]
---

# Run a mass upgrade via the scheduled Agent Client Collector upgrade job

Activate the built-in scheduled job to upgrade all eligible Agent Client Collector agents automatically in rate-limited batches.

## Before you begin

Configure the required upgrade properties before enabling the scheduled job. For details, see [Agent Client Collector upgrade properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/agent-client-collector/acc-agent-upgrade-properties.md).

Role required: agent\_client\_collector\_admin

## About this task

The **Upgrade agents incrementally** scheduled job upgrades all eligible agents on a recurring schedule. The job respects the rate limits set in the upgrade properties, upgrading agents in batches to avoid overloading MID Servers. Agents that have never failed an upgrade are prioritized over agents with prior failures.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.

2.  Search for **Upgrade agents incrementally** and select record.

3.  Set **Active** to **true**.

4.  Adjust the **Run** schedule to match your maintenance window.

    The default schedule runs every hour.

5.  Select **Update**.

    The job runs on the configured schedule, upgrading agents in batches that adhere to the configured rate limits.


**Parent Topic:**[Agent Client Collector upgrade overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/agent-client-collector/acc-agent-upgrade-overview.md)

