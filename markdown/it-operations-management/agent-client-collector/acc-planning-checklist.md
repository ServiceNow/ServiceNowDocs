---
title: Agent Client Collector planning checklist
description: Successful Agent Client Collector \(ACC\) implementations, especially involving large numbers of endpoints or servers, require careful planning. Before proceeding with a large-scale ACC deployment, follow the steps described in the planning checklist.
locale: en-US
release: zurich
product: Agent Client Collector
classification: agent-client-collector
topic_type: concept
last_updated: "2025-10-26"
reading_time_minutes: 2
breadcrumb: [Preparing for ACC implementation, Agent Client Collector, IT Operations Management]
---

# Agent Client Collector planning checklist

Successful Agent Client Collector \(ACC\) implementations, especially involving large numbers of endpoints or servers, require careful planning. Before proceeding with a large-scale ACC deployment, follow the steps described in the planning checklist.

<table id="table_rnf_xjd_dhc"><thead><tr><th>

Step number

</th><th>

Action

</th><th>

Description

</th></tr></thead><tbody><tr><td align="center">

1

</td><td>

Define use cases, targeted devices, and success metrics

</td><td>

Typical ACC use cases include ITOM Visibility, ITAM \(SAM/HAM\), ITSM \(DEX\), ITOM Health \(HLA/Metric Intelligence\). Many customers have success metrics targeting a percentage of devices with successful data collection for a use case over a 7 to 14-day window \(for example, “95% of endpoints report software usage over a 14-day period”\).

</td></tr><tr><td align="center">

2

</td><td>

Identify Key Stakeholders

</td><td>

Involve network, security, and device/software management teams \(such as jamf/Intune experts\) as early as possible during planning.

</td></tr><tr><td align="center">

3

</td><td>

Assess ServiceNow License, Store App and Instance Requirements

</td><td>

Ensure that you have all license entitlements for your use cases. Determine which software updates or configuration changes to your production and sub-production instances are needed to support your targeted number of devices.

</td></tr><tr><td align="center">

4

</td><td>

Assess Software Requirements

</td><td>

1.  Ensure that all CPU architectures and operating systems for your use cases are supported. If not, determine whether non-ACC solutions such as Service Graph Connector or Discovery Patterns can be used.
2.  Determine whether your use cases require elevated system privileges on endpoints or servers \(for example, root access on Linux for device serial number tracking\).

</td></tr><tr><td align="center">

5

</td><td>

Assess Network Requirements

</td><td>

Verify whether there are VPN, firewall, or proxy restrictions that prevent ACC from sending data to your ServiceNow instance.

</td></tr><tr><td align="center">

6

</td><td>

Assess Device Management Requirements

</td><td>

Verify which internal solutions are available for deploying software within your organization on all targeted devices. For example, Intune and Jamf for endpoints; Chef, Puppet, or Ansible for servers.

</td></tr><tr><td align="center">

7

</td><td>

Draft ACC Solution Architecture

</td><td>

Work with your ServiceNow account team to define how ACC agents send data to the ServiceNow instance, based on your use cases and differences in server and endpoint deployment techniques. Verify whether direct connections are made using ITOM Cloud Services or MID Servers.

</td></tr><tr><td align="center">

8

</td><td>

Define and Segment your ACC Deployment Plan

</td><td>

Define evaluation, pilot, and broad rollout stages and the number of devices targeted in each phase. Align each segment with risk tolerance and business goals. ACC must be rolled out gradually, with no more than 5,000 agents per hour.

</td></tr><tr><td align="center">

9

</td><td>

Internal Compliance and Security Review

</td><td>

Work with internal teams and your stakeholders to review your deployment plan, solution architecture, and to obtain approvals.

</td></tr></tbody>
</table>**Parent Topic:**[Preparing for Agent Client Collector implementation](acc-preparation.md)

