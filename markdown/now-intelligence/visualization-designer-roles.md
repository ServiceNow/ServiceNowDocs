---
title: Data Visualization roles
description: There are several roles associated with the Visualization Designer and Visualization Library. Roles limit what users can do with visualizations.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Reference, Data visualizations, Platform Analytics experience, Platform Analytics]
---

# Data Visualization roles

There are several roles associated with the Visualization Designer and Visualization Library. Roles limit what users can do with visualizations.

## Roles

-   **Any role**

    Users with any role can create visualizations in dashboards that they have editing rights to. They need access to the data that they wish to display. They can also add visualizations from the library to their dashboards if those visualizations have been shared with them. They can also bookmark or export visualizations that have been shared with them from the Visualization Designer. They can share a visualization with other users and groups if it was shared with them with sharing rights. Specific roles are needed to create or edit visualizations in the Visualization Designer.

-   **viz\_creator, itil, report\_user**

    Creates visualizations in the Visualization Designer that are then available throughout the organization in the Data Visualizations library. Cannot delete visualizations that have been shared with them. Can edit visualizations in the library only if they created them or if the visualization was shared with them with editing rights. Can share visualizations only with groups and users.

-   **viz\_admin, platform\_analytics\_admin**

    Creates visualizations in the Visualization Designer that are then available throughout the organization in the Data Visualizations library. Edits, deletes, shares, exports, and schedules the export of any visualization. Can share visualizations with roles, not only users or groups. Can schedule export and email of any data visualization on the instance.

-   **report\_admin, admin**

    Has the rights of a viz\_admin and can also manage all Core UI reports, including reports on the Service Portal.

-   **par\_scheduler**

    Schedules export and email distribution of any visualizations that they can access. Users with this role must also have another role that grants permission to create, edit, and share visualizations.

-   **sn\_par\_sche\_export.par\_scheduler\_admin**

    Schedules export and email of any data visualization on the instance.


<table id="table_c3f_kwc_k2c"><thead><tr><th>

Use case

</th><th>

Required role

</th></tr></thead><tbody><tr><td>

Create a data visualization

</td><td>

Anyone with access to data can create a visualization of that data on a dashboard that they own. Users with the viz\_creator role can create a visualization in the Visualization Designer. If you create a visualization in the Visualization Designer, it is saved to the library.

</td></tr><tr><td>

Edit a data visualization

</td><td>

You can edit any visualization that you created or that was shared with you with editing rights, if it is not in the library. If it is in the library, you also need the viz\_creator role.Edit any visualization on the instance with viz\_admin or higher.

</td></tr><tr><td>

Add a visualization from the library to a dashboard

</td><td>

Any role, if the visualization has been shared with you.viz\_creator to add any visualization from the library.

</td></tr><tr><td>

Add a visualization that was created in a dashboard to the library

</td><td>

viz\_creator or higher and the right to edit the dashboard

</td></tr><tr><td>

Unlink a data visualization on a dashboard from the library, creating a version that is local to that dashboard.

</td><td>

Any role, if you can edit the dashboard containing the visualization

</td></tr><tr><td>

Duplicate a visualization in the Visualization Designer

</td><td>

viz\_creator or higher

</td></tr><tr><td>

Share a visualization with users or groups

</td><td>

Any role to share a data visualization that you created or that was shared with you with sharing rights. With the viz\_admin role or higher, you can share any data visualization on the instance. When you share a data visualization, you can pass along the rights to share that visualization further. You also decide whether to share with editing rights or only viewing rights. If a data visualization has been shared with you with sharing and editing rights, you can also pass along editing rights.

</td></tr><tr><td>

Share a data visualization with roles

</td><td>

viz\_admin or higher

</td></tr><tr><td>

Export a visualization

</td><td>

Any role, if you can view the visualization in the Visualization Designer.

</td></tr><tr><td>

Schedule the export of a data visualization

</td><td>

par\_scheduler or higher to schedule the export of a data visualization that you can edit. viz\_admin or higher to schedule the export of any data visualization on the instance.

</td></tr><tr><td>

Delete the scheduled export of a data visualization

</td><td>

sn\_par\_sche\_export.par\_scheduler\_admin \(contained in viz\_admin\)

</td></tr><tr><td>

Delete a visualization

</td><td>

Any role, to delete a data visualization that you created. viz\_admin or higher to delete any data visualization on the instance.

</td></tr><tr><td>

[Control data source availability by role](../task/dv-use-data-source-acl.md)

</td><td>

admin

</td></tr><tr><td>

[Configure chart interactions](../../reporting/task/configure-go-data.md)

</td><td>

Any role if you have the right to edit the data visualization. The viewer needs the right to view any data they drill down to.

</td></tr><tr><td>

[Use service catalog variables in data visualizations](../../reporting/concept/dv-rep-sc-variables.md#)

</td><td>

viz\_creator or higher

</td></tr><tr><td>

[Create coloring rules for data visualizations](../../performance-analytics/concept/colors-dv.md#)

</td><td>

Any role if you have the right to edit the data visualization.

</td></tr></tbody>
</table>**Parent Topic:**[Data visualization reference](data-visualization-reference.md)

