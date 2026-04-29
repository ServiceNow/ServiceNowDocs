---
title: Upgrade Center properties
description: On the properties form, you can set parameters that control how the system executes.
locale: en-US
release: australia
product: Upgrade Center
classification: upgrade-center
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Upgrade Center references, Upgrade Center, Upgrade, Administer the ServiceNow AI Platform]
---

# Upgrade Center properties

On the properties form, you can set parameters that control how the system executes.

<table id="table_y3t_t15_flb"><thead><tr><th>

Field / Element

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Queries upgrade duration estimate **glide.upgrade.preview.duration.instance.id**

</td><td>

A non-production instance queries the upgrade duration estimate. If this property is absent, the system uses all remote instance records to query the upgrade duration estimate. You can also copy the sys\_id of the remote instance record you wish to query for upgrade duration estimate. The system uses the highest duration from the results.

</td></tr></tbody>
</table><table id="table_mlx_3c5_flb"><thead><tr><th>

Field / Element

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Enable an admin or user with admin role to own Upgrade VTB

 **glide.upgrade\_center.task\_board.owner**

</td><td>

Upgrade VTB owner must be an admin. If this property is absent, the system uses the first admin user from active admin users list. The active admin users list is sorted by username.

</td></tr><tr><td>

Enable admins or users with admin role to be members of Upgrade VTB

 **glide.upgrade\_center.task\_board.members**

</td><td>

Upgrade VTB members must be an admin. If this property is absent, the system adds all active admin users as members.

</td></tr></tbody>
</table><table id="table_h4b_wq2_5tb"><thead><tr><th>

Field / Element

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Queries about the type of instance the user is configured. **glide.upgrade.plan.instance\_type**

</td><td>

You must configure the instance either as a builder or a consumer. You must build the upgrade plan on a builder instance and implement it on a consumer instance.

</td></tr></tbody>
</table>**Parent Topic:**[Upgrade Center references](uc-reference.md)

**Related topics**  


[Upgrade Center VTB Labels list](uc-vtb-labels-list.md)

[Default skipped rules](../concept/uc-default-skipped-rules.md)

[Upgrade Center roles](uc-roles.md)

