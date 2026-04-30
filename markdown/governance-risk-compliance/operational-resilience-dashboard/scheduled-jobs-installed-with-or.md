---
title: Scheduled jobs installed with Operational Resilience
description: When you install the Operational Resilience application, the Update CSDM and other dependencies, Calculate red flags for CSDM and dependencies, Update other dependencies scheduled jobs are added to your instance. As a user with the sn\_oper\_res.admin role, you may find this information useful.
locale: en-US
release: xanadu
product: Operational Resilience Dashboard
classification: operational-resilience-dashboard
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reference, Operational Resilience, Governance, Risk, and Compliance]
---

# Scheduled jobs installed with Operational Resilience

When you install the Operational Resilience application, the **Update CSDM and other dependencies**, **Calculate red flags for CSDM and dependencies**, **Update other dependencies** scheduled jobs are added to your instance. As a user with the sn\_oper\_res.admin role, you may find this information useful.

## Scheduled jobs installed with the Operational Resilience application

The following scheduled jobs are installed with the Operational Resilience application:

<table id="table_v4k_1wv_4zb"><thead><tr><th>

Scheduled job

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Update CSDM and other dependencies**

</td><td>

Scheduled job that gathers data from different applications including such as GRC: Advanced Risk, GRC: Risk Management, and GRC: Policy and Compliance Management, BCM, CMDB, and Vulnerability Response to calculate supporting data for various reports.

 The scheduled job runs once a day and removes all the data from the previous day before creating new supporting data for the reports. The job uses different conditions to retrieve the data from different sources and saves it to the Operational Resilience staging tables.

 Updates CSDM and other dependencies. It is configured to run weekly at midnight local time.

</td></tr><tr><td>

**Calculate red flags for CSDM and dependencies**

</td><td>

Calculates the red flags for the CSDM and its dependencies. It is configured to run daily at 3:00 AM local time to refresh the red flags.

</td></tr></tbody>
</table>