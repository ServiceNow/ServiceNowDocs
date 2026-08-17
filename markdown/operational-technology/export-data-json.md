---
title: Export data
description: The Discovery Console for OT exports data as a JSON export file.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/operational-technology/export-data-json.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Settings page, Use the Console pages, Discovery Console for OT, Operational Technology Native Discovery components, Operational Technology Discovery, Operational Technology]
---

# Export data

The Discovery Console for OT exports data as a JSON export file.

## Before you begin

Role required: admin

## Procedure

1.  In the main menu, select the **Settings** option.

2.  On the Settings page, select the **Exports** tab.

    \[Omitted image "settings-export-connections.png"\] Alt text: Export connections

    **Note:** For information, see .

3.  Select and export data into JSON files.

    The available data includes the following.

    -   Assets
    -   Sites
    -   Connections[^1]
    -   Softwares
    -   Sensors
    -   Network Zones
    -   Notifications
    -   Images
    -   All
    **Note:** Selecting **All** downloads all JSON exports to one zip file.

4.  Select the **Download** button next to the desired data.

    The scheduled exports are saved to `/apiexports`.

5.  Under the **Schedule** heading, select the export frequency by number of days and time of day \(UTC\).

    The default frequency is 1 day. The time-of-day defaults to 00:00 AM UTC.


**Parent Topic:**[Settings page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/settings-page-console.md)

[^1]: There are two version of Connections API. They provide the same information in two different formats.
