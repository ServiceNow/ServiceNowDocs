---
title: Using the Overview tab to view the bot processes in RPA Hub
description: By using the Overview tab in RPA Hub, you can quickly view the bot process details in one place.
locale: en-US
release: yokohama
product: RPA Hub
classification: rpa-hub
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Configuring a bot process record in RPA Hub, Using RPA Hub, RPA Hub, Robotic Process Automation \(RPA\) Hub, Data and Automation]
---

# Using the Overview tab to view the bot processes in RPA Hub

By using the **Overview** tab in RPA Hub, you can quickly view the bot process details in one place.

## Introduction of the Overview tab

The **Overview** tab appears after a bot process is in published, in maintenance, or a retired stage. You can see the status of all life-cycle stages \(but not for the Build stage\) for both the attended and unattended bot processes.

## Sections of the Overview tab

The **Overview** tab is divided into the following six sections:

-   Process information
-   Happening now
-   Upcoming changes
-   Performance
-   Work queues
-   Contacts

**Note:** The descriptions of these sections are in a table later in this topic.

## Roles required

To access the **Overview** tab, you must have one of the following roles:

-   RPA developer
-   RPA release manager
-   RPA business manager
-   RPA support user
-   RPA admin

## Examples

The **Overview** tab for an unattended bot process is shown in the following example.

![Overview tab for a published unattended bot process.](../image/overview-unattended-trigger-mode-removed.jpg "Overview tab for an unattended bot process")

The **Overview** tab for an attended bot process is shown in the following example.

![Overview tab for a published attended bot process.](../image/overview-attended.jpg "Overview tab for an attended bot process")

## Details of the sections in the Overview tab

For more information about the **Overview** tab, see [Get a snapshot of a bot process](../task/open-overview-page-rpa.md).

**Note:** If you don't have access to a particular table, you can't see that table in the **Overview** tab.

The following table shows the detailed descriptions of the sections and actions that are available.

<table id="table_g5q_2x5_wtb"><thead><tr><th>

Visualization

</th><th>

Descriptions and action

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Process details

</td></tr><tr><td>

Life cycle stage status

</td><td>

Status of the life-cycle stage of the bot process:-   **Published**
-   **In Maintenance**
-   **Retired**

</td></tr><tr><td>

Process details

</td><td>

Snapshot of the bot process details:-   Bot process type
-   Job Purging days
-   Run Time Threshold
-   Order
-   Managed By Group
-   Description of the bot process

</td></tr><tr><td>

Package

</td><td>

Snapshot of the associated package details:-   Package name
-   Version
-   Created on
-   Created by

 To update the package details, select **Manage package**.

 You can't update the package details when the bot process is published.

</td></tr><tr><td>

Business applications

</td><td>

Associated business applications.For example, Ariba, Microsoft Excel, or Google Chrome.

 To view more business applications, select **View all**.

 To add a business application, select **Add business application**. For more information about adding a business application, see [Assign a business application with a bot process](../task/associate-business-apps.md).

 You can't add a business application when the bot process is published.

</td></tr><tr><td>

Shared parameters

</td><td>

Associated shared parameters.To view more shared parameters, select **View all**.

 To add a shared parameter, select **Add parameters**. For more information about adding a shared parameter, see [Create a shared parameter in RPA Hub](../task/create-shared-parameter.md).

 You can't add a shared parameter when the bot process is published.

</td></tr><tr><td class="sub-head" colspan="2">

Happening nowThis label appears only when the life-cycle stage of the bot process is **In Maintenance**.

</td></tr><tr><td>

Process

</td><td>

State of the process job along with the time stamp and duration:-   **Running**: When at least one process job is in the running state.
-   **Idle**: No process jobs are in the running state.

 This state also shows the contact details of the last update.

</td></tr><tr><td>

Robots

</td><td>

Total number of robots:-   **Total**: Total number of non-retired robots that are associated with the bot process.
-   **In-Maintenance**: Total number of robots that are associated with the in-maintenance life-cycle stage status.

 The summary includes a donut report of robot states.

</td></tr><tr><td>

Currently running robots

</td><td>

Information about the unattended bot process.This state is only for a published bot process when the process job is in the running state.

 Information about the attended bot process.

</td></tr><tr><td>

Last run robots

</td><td>

Information about the last completed process job for the current bot process.This state is for both the published and in-maintenance bot process, when the process job is in the idle state.

</td></tr><tr class="sub-head"><td>

Upcoming changes

</td><td>

Upcoming changes to the associated robots, business applications, and bot processes.This state is only for a published bot process.

</td></tr><tr class="sub-head"><td>

Changes

</td><td>

Changes to the associated robots, business applications,and bot processes.This state is only for an in-maintenance bot process.

</td></tr><tr class="sub-head"><td>

Performance

</td><td>

Performance of the associated process jobs.

</td></tr><tr class="sub-head"><td>

Work queues

</td><td>

Associated work queues for both published and in-maintenance bot processes.To view additional details about the queue, select **View details**.

</td></tr><tr class="sub-head"><td>

Contacts

</td><td>

Contact card details of the IT Owner, Business Owner, Release Manager, and Support User.

</td></tr><tr><td class="sub-head" colspan="2">

Compose

</td></tr><tr><td>

Additional Comments or Work notes \(Private\)

</td><td>

Additional comments or work notes that you can add.

</td></tr><tr><td>

Activity

</td><td>

Activity of the form, work notes, and additional comments that you can view.Configure the related system property to view the activity stream. For more information, see [Display an activity stream for bot processes and robots in RPA Hub](../task/display-activity-stream-sys-property-rpahub.md).

</td></tr></tbody>
</table>