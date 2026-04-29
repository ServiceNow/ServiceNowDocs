---
title: Platform Analytics migration tables
description: The following tables are used in the process of migrating to Platform Analytics. Each row of the bridging tables states the migration type: bulk, owner, list, or upgrade.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Platform Analytics Migration Center, Platform Analytics experience, Platform Analytics]
---

# Platform Analytics migration tables

The following tables are used in the process of migrating to Platform Analytics. Each row of the bridging tables states the migration type: bulk, owner, list, or upgrade.

<table id="table_zw4_rrb_m2c"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

par\_coreui\_migration\_bridge\_component

</td><td>

Lists reports, PA widgets, and filters that have been migrated outside of a dashboard.-   Bulk indicates a migration from the Migration Center.
-   List and Owner indicate partial migrations.
-   Upgrade indicates a dashboard supported in a bulk migration in the context of an upgrade.

</td></tr><tr><td>

par\_coreui\_migration\_bridge\_dashboard

</td><td>

Lists the dashboard migration logs.

</td></tr><tr><td>

par\_coreui\_migration\_bridge\_sysauto

</td><td>

Lists the scheduled export logs.

</td></tr><tr><td>

par\_coreui\_migration\_bridge\_widget

</td><td>

Lists the elements of a dashboard that have been migrated.

</td></tr></tbody>
</table>