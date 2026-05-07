---
title: Configure domain-separated Discovery schedules
description: Configuring the "Run as" user in a Discovery schedule directs discovered Configuration Items \(CIs\) to the correct domain and maintains data isolation.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: task
last_updated: "2026-05-06"
reading_time_minutes: 1
breadcrumb: [Domain Separation and Discovery, Configuring Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Configure domain-separated Discovery schedules

Configuring the "Run as" user in a Discovery schedule directs discovered Configuration Items \(CIs\) to the correct domain and maintains data isolation.

## Before you begin

Role required: discovery\_admin

## About this task

In domain-separated environments, the domain of the user who creates a Discovery schedule typically determines where the discovered data is stored. Assigning a "Run as" user enables the discovery process to run under a different user’s domain and permissions, enabling administrators to control which domain stores the data and what resources the discovery process can access, regardless of who created the schedule.

**Note:** This procedure applies only to existing Discovery schedules. For information about creating a Discovery schedule, see [Schedule a horizontal discovery](t_CreateADiscoverySchedule.md#).

## Procedure

1.  Navigate to **All** &gt; **Discovery** &gt; **Discovery Schedules**.

2.  In the **Name** field, enter the name of the schedule you want to configure.

3.  Double-click the **Run as** field to perform inline editing.

    By default, the **Run as** column doesn’t display in the Discovery Schedules \[discovery\_schedule\] table. For information about customizing columns in tables, see [Personalize a list](https://www.servicenow.com/docs/access?context=c_PersonalLists&version=australia&pubname=australia-platform-user-interface&section=t_PersonalizeAList&ft:locale=en-US).

4.  Enter the name of the user that you want the schedule to run as.

5.  Select the check mark \(![check mark icon](../../cloud-management-v2/image/icon-check-mark.png)\) icon.


**Parent Topic:**[Domain Separation and Discovery](../concept/c_DiscoveryDomainSeparation.md)

