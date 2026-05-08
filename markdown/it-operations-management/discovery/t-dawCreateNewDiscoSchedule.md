---
title: Create an IP-based Discovery schedule in Discovery Admin Workspace
description: Use the Discovery Admin Workspace dashboard to create IP-based Discovery schedules.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [Discovery, Admin, Workspace]
breadcrumb: [Running discoveries in your network, Using Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Create an IP-based Discovery schedule in Discovery Admin Workspace

Use the Discovery Admin Workspace dashboard to create IP-based Discovery schedules.

## Before you begin

Store version: 1.8.0.

Role required: discovery\_admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Discovery Admin Workspace** &gt; **Schedules**.

2.  Select **New Discovery** from the header of any tab on the Schedules page.

3.  Select **IP-based discovery** and select **Continue**.

    **Note:** This schedule is only for IP-based Discovery. For Cloud Discovery, see [Create a discovery schedule in Cloud Discovery Workspace](cloud-operations-disco-create-schedule.md).

4.  Enter a name for the Discovery schedule.

5.  Choose from available Discovery locations.

6.  Choose IP ranges by either selecting from existing sets or by manually entering the ranges.

    -   To select from existing IP range sets, select **Use existing IP range set \(recommended\)**. See [Discovery IP address configuration](../reference/discovery-ip-address-configuration.md#) for more information on IP range sets.
    -   To manually enter comma-separated IPv4 address ranges, IPv4 networks, or individual IPs that describe the ranges you want to add, select **Enter new IP ranges** and enter the IP ranges.
7.  Select **next**.

8.  Choose your MID Server.

    |Option|Description|
    |------|-----------|
    |**Cluster of MID servers**|Select an existing MID Server or create one. Clusters provide failover protection and load balancing between MID Servers. See Configure a MID Server cluster for more information.|
    |**Auto-select MID server**|An available MID Server is automatically selected when the Discovery schedule runs. See [Automatic MID Server selection](../../agent-client-collector/concept/acc-auto-mid-selection.md) for more information.|
    |**MID server**|Choose a MID Server to run the Discovery schedule. All MID Server are shown, but only ones that are up and validated can successfully run a Discovery schedule.|

9.  Select **next**.

10. Configure the Discovery schedule.

    |Option|Description|
    |------|-----------|
    |**Run on demand**|The schedule only runs when triggered manually. Trigger the schedule by selecting **Finish and run** at the end of this setup, or by navigating to the schedule in the Schedules table and selecting **Discover Now**.|
    |**Run at a scheduled time**|The schedule runs at a scheduled date and time. Use the fields to define when the schedule runs.|
    |**Run after series**|The schedule runs after another existing Discovery schedule completes, staggering or chaining them together. Selecting an existing schedule displays a relationship map of all the other associated schedules.|
    |**Cancel discovery if longer than maximum runtime**|If the schedule exceeds the maximum runtime, it's canceled. After toggled, configure the runtime threshold.|
    |**Finish and run**|After being selected, all the information provided is validated. Then, a Discovery schedule is created in the background, a Discovery status is created, and the schedule is run. You're redirected to the Status Details page for the schedule.|
    |**Finish**|After being selected, all the information provided is validated. A Discovery schedule is created and you're redirected to its entry in the Discovery Schedules \[discovery\_schedule\] table. You can edit the schedule information or run it by selecting **Discover Now**.|


## What to do next

After you create and save a Discovery schedule, you can optionally configure the following settings:

-   Define IP addresses or ranges to exclude from all Discovery schedules. See [Use Global Excludes List for IP addresses and ranges](../reference/discovery-ip-address-configuration.md#).
-   Define Discovery schedule attributes to automatically set CI field values such as location or asset tag on discovered CIs. You can define attributes at the schedule, range set, or IP address range level. See [Define CI field attributes](define-ci-attributes.md).

