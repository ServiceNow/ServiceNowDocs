---
title: Digital Experience Score​ properties
description: Configure the system properties to enable DEX Score application and set the company level target for the digital experience score.
locale: en-US
release: australia
product: Digital Experience Score
classification: digital-experience-score
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reference, Digital Experience Score, Digital End-User Experience, IT Service Management]
---

# Digital Experience Score​ properties

Configure the system properties to enable DEX Score application and set the company level target for the digital experience score.

These properties are available for Digital Experience Score​.

**Note:** To open the System Properties \[sys\_properties\] table, enter `sys_properties.list` in the navigation filter.

<table id="table_cfk_tl1_jzb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_dex\_score.active

</td><td>

Controls the availability of the Digital Experience Score​ application on the instance. When true, the application's calculations, dashboard, and configurations are available for use.

When false, the application is unavailable.

-   Type: true\|false
-   Default value: true
-   Other possible values: false

</td></tr><tr><td>

sn\_dex\_score.company\_target\_score

</td><td>

Organization's target for DEX score that you can see on the DEX Score dashboard.-   Type: integer
-   Default value: 75
-   Other possible values: Any whole number from 0 to 100.

</td></tr></tbody>
</table>**Parent Topic:**[Digital Experience Score​ reference](../concept/dexscr-dex-score-reference.md)

