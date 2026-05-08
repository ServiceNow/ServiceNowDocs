---
title: Planned Work Management system properties
description: Planned Work Management uses the following system properties, which are located in the System Properties \[sys\_properties\] table.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-05-07"
reading_time_minutes: 1
breadcrumb: [Planned Work Management components, Components installed with additional plugins, Reference, Field Service Management]
---

# Planned Work Management system properties

Planned Work Management uses the following system properties, which are located in the System Properties \[sys\_properties\] table.

<table id="table_zwf_nnc_zxb"><thead><tr><th>

Properties

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_fsm\_planned\_wm.consider\_initial\_meter\_reading

</td><td>

Enables the system to take the initial meter reading into account when generating the first maintenance schedule.-   Type: True/false
-   Default value: true

</td></tr><tr><td>

create\_and\_cancel\_suppressed\_workorders

</td><td>

Enables the system to log the work order if the schedule is suppressed.-   Type: True/false
-   Default value: false

</td></tr><tr><td>

sn\_fsm\_planned\_wm.valid\_order\_states\_for\_update

</td><td>

Maintains a list of work order states that can be selected to reflect the appropriate state of work orders.

 -   Type: choice list
-   Default value: 1, 10, 15

</td></tr><tr><td>

sn\_fsm\_planned\_wm.tolerance\_span

</td><td>

Maintains the configurable time window for applying schedule suppression. It offers the options of going forward, backward, or in both directions from the current date for selecting the span in which the suppression will be active.-   Type: choice list
-   Default value: Both

</td></tr><tr><td>

sn\_fsm\_planned\_wm.auto\_task\_generation\_enabled

</td><td>

Enables the system to automatically generate tasks for work orders upon their creation. If this property isn’t enabled, the state of the work order remains in the draft state.-   Type: True/false
-   Default value: true

</td></tr><tr><td>

sn\_fsm\_planned\_wm.supported\_effectivity\_calculation\_type

</td><td>

Enables the effective date of a work plan to be set in the past. Support for past dates is enabled when this property is set to advanced.-   Type: Choice list
-   Default value: Advanced

</td></tr></tbody>
</table>**Parent Topic:**[Planned Work Management components](planned-work-components.md)

