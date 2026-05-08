---
title: Configure for VMware Discovery
description: Configure for VMware Discovery by setting up alternate port for vCenter and configuring your ESXi resource pools.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Configure for VMware Discovery

Configure for VMware Discovery by setting up alternate port for vCenter and configuring your ESXi resource pools.

Alternative ports and resource pools aren't managed by ServiceNow ServiceNow directly. They're set up and managed by your security teams and VMware admins. Discovery captures information related to VMware use.

In many environments, security teams block the standard ports, and vCenter/ESXi services run on custom ports. You must configure Discovery for these alternate ports, or it will fail. For more information, see [Configure an alternate port for vCenter](../task/t_ConfigureAlternatePortForVCenter.md) and [Configure ESXi resource pools](../task/t_ConfigureESXResourcePools.md)

**Note:** Applications that access VMware cloud resources need access to VMware credentials. For more infomration, see VMware credentials.

