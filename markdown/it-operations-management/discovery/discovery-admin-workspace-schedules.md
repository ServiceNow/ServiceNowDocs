---
title: Discovery Admin Workspace Schedules
description: The Discovery Admin Workspace Schedules page provides a unified workspace to gain insights into the performance of all of your discoveries. The workspace provides quick access to managing Discovery schedules and Discovery statuses.Use the Discovery Admin Workspace dashboard to create IP-based Discovery schedules from the Schedules table.
locale: en-US
release: xanadu
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Discovery Admin Workspace, Exploring Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Discovery Admin Workspace Schedules

The Discovery Admin Workspace Schedules page provides a unified workspace to gain insights into the performance of all of your discoveries. The workspace provides quick access to managing Discovery schedules and Discovery statuses.

The Discovery Admin Workspace Schedules page gives Discovery administrators immediate access to all day-to-day Discovery activities.

To access the Discovery Admin Workspace Schedules page, navigate to **Workspaces** &gt; **Discovery Admin Workspace** &gt; **Schedules**.

## Key features

-   **Overview**

    The Discovery Admin Workspace Overview page enables you to make data-driven decisions through powerful visualizations.

<table id="table_cb2_yjv_fsb"><thead><tr><th>

Report title

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Schedules by location

</td><td>

Map

</td><td>

This report displays Discovery schedules by location.Select an area of the map to see Discovery schedules in the region selected.

</td></tr><tr><td>

Total schedules

</td><td>

Line chart

</td><td>

This report displays the total number of Discovery schedules run in the last 24 hours.Select the chart to view Discovery schedules.

</td></tr><tr><td>

Errors by category

</td><td>

Donut chart

</td><td>

This report displays the count of all Discovery errors by category.Select a category to add or remove it from the chart.

</td></tr><tr><td>

Total discovery attempts

</td><td>

Line and area chart

</td><td>

This report displays the count of all Discovery attempts completed and canceled.

</td></tr></tbody>
</table>-   **Discovery schedules**

    The Discovery Admin Workspace Discovery schedules tab gives you quick access to all of your Discovery schedules. You can select a Discovery schedule to view extensive details and update schedule field parameters. For more details, see [Schedule a horizontal discovery](../task/t_CreateADiscoverySchedule.md).

-   **Discovery status**

    The Discovery Admin Workspace Discovery status page shows the current status of scheduled discoveries. You can select a Discovery status number to view detailed information. For more details, see [Discovery status](c_DiscoveryStatus.md).


## Prerequisites

Confirm that you’ve installed the latest version of the CMDB Workspace.

## Roles

The following roles have access to the Discovery Admin Workspace:

-   admin
-   discovery\_admin

## Create new IP-Based Discovery schedule

Use the Discovery Admin Workspace dashboard to create IP-based Discovery schedules from the Schedules table.

**Prerequisites:** Store App version 1.5.0

In the **Discovery schedules** tab, create a new schedule by selecting **New** on the Discovery schedules table. This schedule is only for IP based Discovery. For other options, see [Schedule a horizontal discovery](../task/t_CreateADiscoverySchedule.md).

### Discovery details

**Name:** Enter a name for the Discovery schedule

**Location:** Choose from available Discovery locations. This field is not required.

**Select IP ranges:**

-   **Use existing IP range set:** Select from existing IP range sets. See [Discovery IP address configuration](../reference/discovery-ip-address-configuration.md#) for more information on IP range sets.

-   **Enter new IP ranges:** Enter comma-separated IPv4 address ranges, IPv4 networks, or individual IPs describing the ranges you would like to add. You can enter a name to save the IP range set.


### Choose your MID Server

**Auto-select MID server:** An available MID Server is automatically selected when the Discovery schedule runs. See [Automatic MID Server selection](../../agent-client-collector/concept/acc-auto-mid-selection.md) for more information.

**Cluster of MID servers:** Choose an existing MID Server cluster or create a new one. Clusters provide fail-over protection and load-balancing between MID Servers. See [Configure a MID Server cluster](https://www.servicenow.com/docs/access?context=t_ConfigureAMIDServerCluster&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US) for more information.

**MID server:** Choose a specific MID Server to run the Discovery schedule. All MID Servers are shown, but only ones that are up and validated can successfully run a Discovery schedule.

### Schedule details

**Run at a scheduled time:** Use the fields to define when the schedule runs.

**Run after series:** Choose to run the schedule after another existing Discovery schedule. Selecting an existing schedule displays a relationship map of all the other associated schedules.

**Run on demand:** The schedule only runs when triggered manually. The schedule can be triggered by selecting **Finish and run** at the end of this set-up, or navigating to the schedule in the Schedules table and selecting **Discover Now**.

**Maximum run time:** Sets a limit on how long a schedule can run, after which the schedule is cancelled. Limits can improve MID Server performance and prevent problems.

**Finish:** Once selected, all the information provided is validated. A Discovery schedule is created and you are redirected to its entry in the Schedules table. You can edit the schedule's information or run it by selecting **Discover Now**.

**Finish and run:** Once selected, all the information provided is validated. Then a Discovery schedule is created in the background, and a Discovery status is created and the schedule is run.

