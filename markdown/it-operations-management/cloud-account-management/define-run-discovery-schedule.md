---
title: Define and run discovery schedule
description: The discovery schedule is the control point for running discoveries. The schedule controls when discovery runs, defines the MID Server to use, the type of discovery that should run, and the IP addresses to query.
locale: en-US
release: australia
product: Cloud Account Management
classification: cloud-account-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Populate Cloud Account Management dependent tables, Setting up Cloud Account Management in Cloud Workspace, Configuring Cloud Account Management, Cloud Account Management, ITOM Cloud Accelerate, IT Operations Management]
---

# Define and run discovery schedule

The discovery schedule is the control point for running discoveries. The schedule controls when discovery runs, defines the MID Server to use, the type of discovery that should run, and the IP addresses to query.

## Before you begin

Role required: discovery\_admin

## Procedure

1.  Navigate to **All** &gt; **Cloud Provisioning and Governance** &gt; **Cloud Admin Portal**.

    The Cloud Admin Portal opens in a new browser tab.

2.  On the Cloud Admin Portal, navigate to **Manage** &gt; **Discovery Schedules**.

3.  Select **Add New Schedule**.

4.  Fill in the details \(by selecting the provider\).

    For more information on the field details, see [Create a new discovery schedule form reference](../../discovery/reference/create-a-new-discovery-schedule-form.md).

    If the system can’t detect an appropriate MID Server, you’re prompted to configure a MID Server.

5.  Select **Next**.

    After the schedule runs, the system discovers resources from the org and org units linked to the AWS account or Azure tenant and management groups. The details are populated in the following tables:

    -   cmdb\_ci\_cloud\_org\_list.do
    -   For AWS: cmdb\_ci\_aws\_org\_unit\_list.do
    -   For Azure: cmdb\_ci\_azure\_management\_group

