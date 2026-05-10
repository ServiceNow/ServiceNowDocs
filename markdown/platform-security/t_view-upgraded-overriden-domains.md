---
title: View upgraded processes or records in the global domain
description: You can track and review base system records or processes in the global domain that were overridden across one or multiple domains prior to an upgrade and were subsequently updated during a platform or app upgrade.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-05-09"
reading_time_minutes: 1
breadcrumb: [Setup and administration, Domain separation for service providers, Access Management]
---

# View upgraded processes or records in the global domain

You can track and review base system records or processes in the global domain that were overridden across one or multiple domains prior to an upgrade and were subsequently updated during a platform or app upgrade.

## Before you begin

Role required: domain\_admin

## Procedure

1.  Navigate to **ALL &gt; Domain Admin &gt; Upgraded Overridden Processes**.

2.  Review the information in the dashboard's **Summary** tab.

    **Note:** You can sort the dashboard by either admin reviewed or non-reviewed records with the **Reviewed** drop-down menu.

    |Dashboard metric|Description|
    |----------------|-----------|
    |Overridden Records by Table Name|A graphical list of all overridden records, sorted by table name.|
    |Overridden Record Count|The total number of overridden records.|
    |Overridden Records List|Shows information for all overridden records.|

3.  Select the **Upgraded Overridden Domain Records** tab to view the Summary information in more detail:

    **Note:** The information for this dashboard view is compiled from the **Overridden Record Count** \(`upgraded_overridden_process`\) table. In addition, the columns you select for view in this table will be the columns that display in this dashboard. You can view this table by selecting the number displayed in the **Overridden Record Count** metric display on the Summary view of the dashboard.

    |Metric|Description|
    |------|-----------|
    |File Name|Name of the upgraded file.|
    |Process Name|Name of the process that is changed post upgrade.|
    |Table|Name of the table that the upgraded process belongs to.|
    |Upgrade Date|The time when the record was upgraded.|
    |Change Type|Whether the record was changed or updated.|
    |Reviewed|Whether the override record has been reviewed by an admin.|
    |Release Version|Indicates the version or release name where the record was updated.|
    |Review Notes|Brief notes or closing comments added by the admin after global record changes are reviewed|
    |Updated By|The account that last updated the record.|
    |Updates|The total number of updates that have been made to the record.|
    |Upgrade History|Select the link to view the complete upgrade history for the record.|

    You can filter this table with Boolean operators.


## What to do next

Select a file name to review its associated overridden record.

