---
title: Customize Firewall Audits and Reporting
description: Change Discovery properties to customize some of the aspects of Firewall Audits and Reporting.
locale: en-US
release: xanadu
product: Discovery
classification: discovery
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Visibility to Firewall inventory, Configuring Firewall Audits and Reporting, Firewall Audits and Reporting, Discovery, ITOM Visibility, IT Operations Management]
---

# Customize Firewall Audits and Reporting

Change Discovery properties to customize some of the aspects of Firewall Audits and Reporting.

## Before you begin

Role required: discovery\_admin or admin

## About this task

[Discovery properties](../reference/r_DiscoveryProperties.md) manage various aspects of the horizontal discovery process. This procedure explains how to assign default policy owner group and approval group names for approving firewall rule tasks.

## Procedure

1.  To edit [Discovery properties](../reference/r_DiscoveryProperties.md), navigate to **All** &gt; **Discovery Definition** &gt; **Properties**.

    For more information on properties, see [Discovery properties](../reference/r_DiscoveryProperties.md).

    -   sn\_disco\_firewall.default.rule.task.policy.owner.group: Your default task owner group name
    -   sn\_disco\_firewall.default.rule.task.approval.group: Your default approval group name
2.  Edit the properties as required.

    -   sn\_disco\_firewall.default.rule.task.policy.owner.group: Your default task owner group name
    -   sn\_disco\_firewall.default.rule.task.approval.group: Your default approval group name
    These feature saves time by automatically filling in your default owner group and approval group in requests.


**Parent Topic:**[Visibility to Firewall inventory](../concept/use-firewall-audit-rep.md)

