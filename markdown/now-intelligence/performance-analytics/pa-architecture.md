---
title: Performance Analytics architecture
description: Before using Performance Analytics, familiarize yourself with how the layers of architecture take you from raw database entries to insightful visuals on dashboards.
locale: en-US
release: australia
product: Performance Analytics
classification: performance-analytics
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Implement Performance Analytics, Explore, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Performance Analytics architecture

Before using Performance Analytics, familiarize yourself with how the layers of architecture take you from raw database entries to insightful visuals on dashboards.

<table id="table_wfx_jgw_s3b"><thead><tr><th>

Level

</th><th>

Component

</th><th>

Description

</th><th>

Creator persona

</th></tr></thead><tbody><tr><td>

0

</td><td>

ServiceNow database tables

</td><td>

Business process tables, containing the raw data that you want to analyze to evaluate performance. Examples: Incident \[incident\], Problem \[problem\]Inventory tables, containing the information you need to filter, categorize, or break down data from the business process tables. Examples: User \[sys\_user\], Choice \[sys\_choice\]

</td><td>

N/A

</td></tr><tr><td>

1

</td><td>

Indicator sources

</td><td>

Metadata objects, each one of which can serve as the data source for multiple indicators. Indicator sources contain the following:-   Reference to a business process table
-   Reference to a field on the table with unique values for every record
-   Conditions for filtering the records of the table
-   The indicator frequency for which this source is valid. An indicator frequency is the frequency for which data is collected for an indicator. The frequencies of the indicator and the indicator source must match.

</td><td>

Performance Analytics Technical Expert, with at least the pa\_data\_collector role.

</td></tr><tr><td>

1

</td><td>

Breakdown sources

</td><td>

Metadata objects, each one of which can serve as the data source for multiple breakdowns. Breakdown sources contain the following:-   Reference to an inventory table
-   Reference to a field on the table with unique values for every record
-   Conditions for filtering the records of the table

</td><td>

Performance Analytics Technical Expert, with at least the pa\_data\_collector role.

</td></tr><tr><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr></tbody>
</table>**Parent Topic:**[Implement Performance Analytics](implementing-pa.md)

