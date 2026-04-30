---
title: Agent Client Collector deployment checklist
description: Successful Agent Client Collector \(ACC\) implementations, especially involving large numbers of endpoints or servers, require careful deployment. When proceeding with a large-scale ACC deployment, follow the steps described in the deployment checklist.
locale: en-US
release: zurich
product: Agent Client Collector
classification: agent-client-collector
topic_type: concept
last_updated: "2025-11-17"
reading_time_minutes: 1
breadcrumb: [Preparing for ACC implementation, Agent Client Collector, IT Operations Management]
---

# Agent Client Collector deployment checklist

Successful Agent Client Collector \(ACC\) implementations, especially involving large numbers of endpoints or servers, require careful deployment. When proceeding with a large-scale ACC deployment, follow the steps described in the deployment checklist.

<table id="table_hvf_bwk_3hc"><thead><tr><th>

Step number

</th><th>

Action

</th><th>

Description

</th></tr></thead><tbody><tr><td align="center">

1

</td><td>

Update production and sub-production instances

</td><td>

Ensure that all instances are updated to the most recent store applications, family releases, or both.

</td></tr><tr><td align="center">

2

</td><td>

Assess instance capacity

</td><td>

Open support tickets if additional instance capacity is needed for the projected number of ACC agents.

</td></tr><tr><td align="center">

3

</td><td>

Deploy and configure MID Servers when required

</td><td>

If connecting over 1,000 ACC agents to a single MID Server, assess performance and whether a load balancer in front of a MID Server is needed.

</td></tr><tr><td align="center">

4

</td><td>

Verify whether ITOM Cloud Services \(ICS\) is required and, if so, whether it is configured

</td><td>

Some use cases \(such as DEX\) always require ICS.

</td></tr><tr><td align="center">

5

</td><td>

Download appropriate installer files from the instance

</td><td>

Installer files may be in one of the following formats:-   .rpm
-   .msi
-   .pkg

</td></tr><tr><td align="center">

6

</td><td>

Define a deployment calendar

</td><td>

Share deployment groups and group size, assignments, start/stop, success gates, go/no-go signers, and rollback criteria with stakeholders.

</td></tr><tr><td align="center">

7

</td><td>

Package ACC in appropriate software management tools

</td><td>

Software management tools include:-   Intune
-   jamf

</td></tr><tr><td align="center">

8

</td><td>

Deploy pilot and test environments on sub-production instances using your preferred software management tool

</td><td>

In test and pilot environments, you can test multiple operating systems and hardware combinations \(such as server vs. laptop\).

</td></tr><tr><td align="center">

9

</td><td>

Monitor the ServiceNow instance and the software management solution

</td><td>

-   On the instance, monitor the performance and rate limit violations.
-   On the software management solution, monitor the deployment success rate.

</td></tr><tr><td align="center">

10

</td><td>

Assess data collection, install success rate, and instance performance over the next 2-3 business days

</td><td>

Workloads and data collection can vary significantly, depending on the time of day; therefore, monitor deployment success over several days.

</td></tr><tr><td align="center">

11

</td><td>

Update deployment calendar and continue with next install cohorts

</td><td>

After successful deployment, continue with data collection.

</td></tr></tbody>
</table>**Parent Topic:**[Preparing for Agent Client Collector implementation](acc-preparation.md)

