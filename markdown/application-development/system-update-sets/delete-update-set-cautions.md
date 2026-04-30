---
title: Cautions about deleting update sets
description: Deleting an update set is a bad practice. To revert a customization, back out the update set rather than deleting it.
locale: en-US
release: xanadu
product: System Update Sets
classification: system-update-sets
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Update set transfers, System update sets, Deploying applications, Building applications]
---

# Cautions about deleting update sets

Deleting an update set is a bad practice. To revert a customization, back out the update set rather than deleting it.

Administrators can delete an update set only when it is not the current update set and it is empty \(no `sys_update_xml` entries are associated with it\). For example, after merging update sets, you might want to delete the original sets. This function is restricted by an access control rule \(ACL\) on the Update Set \[sys\_update\_set\] table.

Do not delete `sys_update_xml` entries, because this action:

-   Does not undo the updates.
-   Removes any record of who applied the customizations.
-   Removes the `sys_update_xml` entries associated with the update set, so customizations are overwritten when the instance is upgraded.

When you try to delete an update entry, a warning message appears. Click **OK** to confirm the deletion.

