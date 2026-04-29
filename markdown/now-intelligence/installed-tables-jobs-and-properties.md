---
title: Installed jobs, tables, and properties for Platform Analytics library recommendations
description: Several types of components are installed with activation of the plugin, including tables, properties, and scheduled jobs.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Library recommendations, Platform Analytics experience, Platform Analytics]
---

# Installed jobs, tables, and properties for Platform Analytics library recommendations

Several types of components are installed with activation of the  plugin, including tables, properties, and scheduled jobs.

## Scheduled jobs installed

<table id="table_bhh_jzb_h3c"><thead><tr><th>

Scheduled job

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Analytics library management job

</td><td>

Generates recommendations for all supported libraries. Runs weekly by default.

</td></tr></tbody>
</table>## Tables installed

<table id="table_dhh_jzb_h3c"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Analytics Library Scan Items

 \[analytics\_library\_scan\_item\]

</td><td>

Stores the results of the scheduled library management jobs

</td></tr><tr><td>

Analytics Library Scan Executions

 \[analytics\_library\_scan\_execution\]

</td><td>

Stores the logs of the scheduled library management jobs

</td></tr></tbody>
</table>## System properties installed

<table id="table_i3z_w1c_h3c"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_analytics\_rcmnd.recommendation\_metrics\_time\_period

</td><td>

Sets the period on which usage is calculated. Add it to the System Properties \[sys\_properties\] table. The value is an integer that defines a number of days. If the property is not specified, the default is 180 days.

</td></tr></tbody>
</table>**Parent Topic:**[Platform Analytics library recommendations](../concept/pa-library-recommendations.md)

