---
title: Phase 2 - Prepare for the development instance upgrade
description: For a better understanding of your production upgrade duration, request a full clone of your production instance \(including large tables and attachments\) onto a non-production instance. Confirm your current and target release versions, because you will later use this information when scheduling your upgrade in Now Support.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Upgrade to the Zurich release, Zurich release notes]
---

# Phase 2 - Prepare for the development instance upgrade

For a better understanding of your production upgrade duration, request a full clone of your production instance \(including large tables and attachments\) onto a non-production instance. Confirm your current and target release versions, because you will later use this information when scheduling your upgrade in Now Support.

## Before you begin

Role required: admin.

## About this task

![Upgrade progress bar](../image/progress-bar-phase-2.png)

## Procedure

1.  On your production instance, create a system clone and select your development instance as the **Target instance**.

    The clone provides you with an exact copy of production. Performing an upgrade on your clone allows you to simulate an upgrade on your production configuration in a non-production environment. Refer to System clone for details.

    **Important:**

    For effective upgrade testing, use this clone to test on a system that reflects the production instance as closely as possible. If your non-production and production instances are the same size, include the production audit log and the attachment data on your production clone. To ensure that all production data is included with the clone, make sure that you clear all the **Exclude** check boxes on the Request Clone form. On your non-production instance, replicate typical user behaviors that occur on your production instance to enhance an estimate of your upgrade duration.

2.  Set expectations for performance during upgrades.

    During an upgrade, your performance may be impacted because your nodes initiate the distribution upgrade. All nodes are restarted during an upgrade, but your multi-node instances are available during an upgrade because ServiceNow instances operate on a multi-node system. This multi-node system staggers node distribution upgrades, ensuring that there is at least one active pair of nodes for multi-node instances during an upgrade.

    To help you set accurate expectations for performance during upgrades, be aware of the differences between the nodes on your non-production and production instances. Instances with one node experience a short period of downtime during the upgrade, but multi-node instances do not have UI downtime. For details on your nodes and their status, see the Upgrade Progress screen.


