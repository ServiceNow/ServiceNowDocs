---
title: Import or export assets
description: You can import or export assets, and ignored assets, to either CSV or JSON formats.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/operational-technology/import-export-assets.html
release: zurich
topic_type: task
last_updated: "2026-04-15"
reading_time_minutes: 1
breadcrumb: [Assets page, Using the Discovery Console, Discovery Console for OT, Operational Technology Native Discovery components, Operational Technology Discovery, Operational Technology]
---

# Import or export assets

You can import or export assets, and ignored assets, to either CSV or JSON formats.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **Assets &gt; Assets** page.

    The list of current assets displays on the page.

2.  You can import/export all listed assets or you can filter the list using the Filter panel, selecting the Filter tab.

    For more information, see [Assets page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/operational-technology/assets-page-console.md).

3.  Import assets
4.  Select the**Actions** button.

    \[Omitted image "image.action-button-list-new"\] Alt text: Action menu

5.  Select Import Assets and the Import Assets window opens.

    \[Omitted image "image.import-assets-prompt"\] Alt text: Import Assets

    The window lists the format you can import to the Console. You can also toggle the available settings in the window to activate them:

    -   Ignore Invalid Network Zones
    -   Keep Existing Assets
6.  When you select Import Ignore Assets, the prompt window opens and displays the additional required information needed.

    \[Omitted image "image.import-ignored-assets-prompt"\] Alt text: Import Ignored Asset

    **Note:** The assets file must be in CSV format to upload to the Console.

7.  Other actions and formats you can select from the **Actions** menu are:

    -   Export Ignore Assets \(CSV\)
    -   Export Assets \(JSON\)
    -   Export Assets \(CSV\)
8.  Export assets
9.  Select the**Actions** button.

    \[Omitted image "image.action-button-list-new"\] Alt text: Action menu

10. Select Export Assets by the format you want the output to be.

    Choose to export either .csv or json asset files. If you don't choose a specific asset or assets, all asset information is exported.

11. Use the Filters panel to sort the assets you want to export.

    In this image, the assets are filtered by the general type Purdue level and the more specific Level 2.

    \[Omitted image "image.filter-by-purdue-export"\] Alt text: Filtered assets

12. From the Actions menu, select Export Assets for the desired format, either .json or .csv.

    The filtered assets are exported.


