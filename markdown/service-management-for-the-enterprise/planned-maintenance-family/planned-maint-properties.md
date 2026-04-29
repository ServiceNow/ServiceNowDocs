---
title: Property settings for Planned Maintenance
description: You configure Planned Maintenance properties at Planned Maintenance Properties .
locale: en-US
release: australia
product: Planned Maintenance \(Family\)
classification: planned-maintenance-family
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Managing maintenance plans, Planned Maintenance, Service Management]
---

# Property settings for Planned Maintenance

You configure Planned Maintenance properties at **Planned Maintenance** &gt; **Properties**.

## Trigger properties

<table id="table_aw1_jgm_pbb"><tbody><tr><td>

Use this property to maintain the planned maintenance intervals in fixed meter\[planned\_maintenance.fixed\_meter\]

</td><td>

Preserve the calculated meter trigger. See the illustration.

 -   Select the check box to perform the next planned maintenance at the meter value that was originally calculated even if the most recent work order was completed at a later meter value.
-   Clear the check box to restart the meter calculation using the reading when the work order was completed.

</td></tr><tr><td>

Use this property to maintain the planned maintenance intervals in fixed intervals\[planned\_maintenance.fixed\_interval\]

</td><td>

Preserve the calculated interval trigger. See the illustration.

 -   Select the check box to perform the next planned maintenance at the time/date that was originally calculated based on the configured interval even if the most recent work order was completed late.
-   Clear the check box to restart the interval calculation when the work order is completed.

</td></tr></tbody>
</table>![Properties controlling trigger calculation](../image/property-preserve-calc.png)

**Parent Topic:**[Managing maintenance plans](../concept/c_MaintPlanMgmt.md)

