---
title: DEX policies for non-persistent VDIs
description: Policy reference for DEX monitoring on Windows non-persistent \(NP\) Virtual Desktop Infrastructures \(VDI\). Use this reference to understand available check instances, frequencies, and parameters for application, network, and device monitoring.
locale: en-US
release: australia
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: reference
last_updated: "2026-04-02"
reading_time_minutes: 1
breadcrumb: [DEX Content Playbook reference, Reference, Digital End-User Experience, IT Service Management]
---

# DEX policies for non-persistent VDIs

Policy reference for DEX monitoring on Windows non-persistent \(NP\) Virtual Desktop Infrastructures \(VDI\). Use this reference to understand available check instances, frequencies, and parameters for application, network, and device monitoring.

## Policies for Windows — Application

DEX provides the following policies for applications.

<table id="table_cyl_3cq_53c"><thead><tr><th>

Check instance

</th><th>

Description

</th><th>

Frequency

</th><th>

Historical or latest

</th><th>

Check instance parameters\*

</th></tr></thead><tbody><tr><td>

os.win.check-app-historical

</td><td>

Collects apps metrics from nonpersistent VDI Windows machine and sends metric data to Metric Base and ServiceNow® Instance.

</td><td>

5 mins

</td><td>

Historical

</td><td>

cpu\_usage, memory\_usage, uptime, last\_access\_time, crashes, is\_running, freezes

</td></tr><tr><td>

os.win.check-app-sccm-latest

</td><td>

Collect application-specific metrics for the Microsoft System Center Configuration Manager app on theWindows device

</td><td>

24 hours

</td><td>

Latest

</td><td>

Not applicable

</td></tr><tr><td colspan="5">

**Important:** \* DEX Windows Apps Metrics with the uptime check instance parameter only runs with the Local System account.

</td></tr></tbody>
</table>## Policies for Windows — Device

DEX provides the following policies for non-persistent VDI devices.

| | | | | |
|---|---|---|---|---|
|os.win.check-system-metrics-historical|Collects all historical metrics.|5 mins|Historical|memory\_details, io\_usage\_write, io\_usage\_read, cpu\_usage|
|os.win.check-system-metrics-latest|Collects all latest metrics.|24 hours|Latest|cpu\_usage|

**Parent Topic:**[DEX Content Playbook reference](dex-content-playbook-reference.md)

