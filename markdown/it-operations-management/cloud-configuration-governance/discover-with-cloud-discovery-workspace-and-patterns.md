---
title: Discover using Cloud Operations Workspace and Patterns
description: You can now schedule and perform discovery using Cloud Discovery Workspace and Discovery and Service Mapping Patterns.
locale: en-US
release: australia
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Additional Cloud Provisioning and Governance setup on day 2, Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Discover using Cloud Operations Workspace and Patterns

You can now schedule and perform discovery using Cloud Discovery Workspace and Discovery and Service Mapping Patterns.

## Before you begin

Role required: System admin

## About this task

Cloud Operations Workspace is now known as Cloud Discovery Workspace or CDW.

## About this task

## Procedure

1.  Check if **Cloud Discovery Workspace** \(CDW\) is installed.

2.  Navigate to **Cloud Admin Portal** &gt; **Manage** &gt; **Discovery Schedules** &gt; **ManageDiscovery Schedules**.

    Follow these scenarios for next steps.

<table id="choicetable_rcg_mjr_bcc"><thead><tr><th align="left" id="d65410e104">

Scenario

</th><th align="left" id="d65410e107">

Next steps

</th></tr></thead><tbody><tr><td id="d65410e113">

**Cloud Discovery schedules don't display for System Admin login**

</td><td>

-   Cloud Discovery Workspace isn't installed. The page notifying that Cloud Discovery Workspace must be installed, displays.
-   The page prompts to **Go to Applications Manager** to allow installation


</td></tr><tr><td id="d65410e139">

**Cloud Discovery schedules don't display for sn\_cmp Cloud Admin login**

</td><td>

-   Cloud Discovery Workspace isn't installed. The page notifying that Cloud Discovery Workspace must be installed, displays.
-   The page requests to contact the system admin for Cloud Discovery Workspace installation.


</td></tr><tr><td id="d65410e165">

**Cloud Discovery displays**

</td><td>

Cloud Discovery schedules display in a new tab of your browser.

</td></tr></tbody>
</table>3.  Ensure that the sn\_cmp cloud admin role contains the role 'sn\_cloud\_ops\_ws.cloud\_ops\_admin'.

4.  Navigate to **Cloud Admin Portal** &gt; **Manage** &gt; **Discovery Schedules**.

5.  Click and confirm when Discovery Schedules open in a new tab.

6.  Ensure that the sn\_cmp Cloud Admin is able to view the Discovery Schedules page by default.


## What to do next

Install and use the latest Discovery and Service Mapping Patterns, at least version 1.15, as the default mechanism for performing Discovery.

**Parent Topic:**[Additional Cloud Provisioning and Governance setup on day 2](../concept/cloud-mgt-general-setup-day-2.md)

