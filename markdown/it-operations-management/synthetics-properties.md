---
title: Synthetic monitoring properties
description: Synthetic monitoring includes the following properties.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Synthetic monitoring reference, Synthetic monitoring, ITOM AIOps, IT Operations Management]
---

# Synthetic monitoring properties

Synthetic monitoring includes the following properties.

These properties are available for synthetic monitoring.

**Note:** To open the System Properties \[sys\_properties\] table, enter `sys_properties.list` in the navigation filter.

<table id="table_dzn_y33_n2c"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_sow\_synthetics.logger

</td><td>

Controls logging output. Valid values are:-   debug
-   info
-   notice \(default\)
-   warning
-   err
-   crit

</td></tr><tr><td>

sn\_sow\_synthetics.auto\_mid\_selection.skip\_phases

</td><td>

Determines the number of comma-separated phases to skip in selection cascade. Default value is empty.

</td></tr><tr><td>

sow.recommendation.enabled

</td><td>

Feature flag to enable recommendation tile on incidents and by default it is set to 'false'.

</td></tr><tr><td>

sow.recommendation.max\_endpoints

</td><td>

Determines the max endpoints to be shown in recommendation panel. The default value is 50.

</td></tr><tr><td>

sn\_sow\_synthetics.default\_mid\_location

</td><td>

Displays default location sys\_id for auto MID selection phase 5. The default value is 'null'.

</td></tr><tr><td>

sn\_sow\_synthetics.auto\_mid\_selection.enabled

</td><td>

Flag to enable/disable auto MID selection and be default it is set to 'true'.

</td></tr><tr><td>

sn\_sow\_synthetics.auto\_mid\_selection.dns\_cache\_ttl

</td><td>

Determines the DNS cache time for IP affinity phase. The default value is 300 seconds.

</td></tr></tbody>
</table>**Parent Topic:**[Synthetic monitoring reference](synthetic-monitoring-reference.md)

