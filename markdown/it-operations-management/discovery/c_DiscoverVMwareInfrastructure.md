---
title: Discovery for VMware virtualization
description: A Discovery schedule for VMware virtualization discovers vCenter and ESX hosts and individual ESXi hosts that manage VMs and related components without a vCenter.
locale: en-US
release: zurich
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2026-12-30"
reading_time_minutes: 1
keywords: [VMware virtualization, VMware infrastructure, VMware Discovery]
breadcrumb: [Discovery for data-center virtualization, Discovery, ITOM Visibility, IT Operations Management]
---

# Discovery for VMware virtualization

A Discovery schedule for VMware virtualization discovers vCenter and ESX hosts and individual ESXi hosts that manage VMs and related components without a vCenter.

The following options are available for discovering VMware vCenter data:

-   Discovery runs the [VMware - vCenter Datacenters](../reference/r_ListOfDiscoveryProbes.md) probe when it identifies a VMware vCenter process running on a Windows machine or detects activity with the vmapp port probe.
-   [Classic Orchestration](https://www.servicenow.com/docs/access?context=r-orchestration&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US) runs any of the vCenter probes from a workflow.

Use standalone ESXi discovery to discover VMware data without a vCenter.

**Note:** See the knowledge article [KB0687582](https://support.servicenow.com/kb_view.do?sysparm_article=KB0687582) for information on model\_id and manufacturer.

