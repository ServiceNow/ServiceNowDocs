---
title: Exporting files
description: The Discovery Console for OT exports data as a JSON export files.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/operational-technology/export-data-json.html
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Settings page, Using the Discovery Console, Discovery Console for OT, Operational Technology Native Discovery components, Operational Technology Discovery, Operational Technology]
---

# Exporting files

The Discovery Console for OT exports data as a JSON export files.

## Before you begin

Role required: admin

## Procedure

1.  In the main menu, select the **Settings** page.

2.  On the **Settings** page, select the **Exports** tab.

3.  Select and export data into JSON files.

    The available data includes the following.

    -   Assets
    -   Sites
    -   Softwares
    -   Sensors
    -   Network Zones
    -   Notifications
    -   Images
    -   All
    Selecting **All** downloads all JSON exports to one zip file.

4.  Select the **Download** button next to the desired data.

5.  Under the **Schedule** heading, select the export frequency by number of days and time of day \(UTC\).

    The default frequency is 1 day. The time-of-day defaults to 00:00 AM UTC. The scheduled exports are saved to `/apiexports`.

    \[Omitted image "export-api-endpoints-console.png"\] Alt text: Schedule download


