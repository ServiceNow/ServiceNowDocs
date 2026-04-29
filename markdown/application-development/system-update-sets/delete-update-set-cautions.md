---
title: Important considerations before deleting update sets
description: Revert a customization, back out the update set rather than deleting it.
locale: en-US
release: australia
product: System Update Sets
classification: system-update-sets
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reference, System update sets, Deploying applications, Building applications]
---

# Important considerations before deleting update sets

Revert a customization, back out the update set rather than deleting it.

Administrators can delete an update set only when it isn’t the current update set and contains no sys\_update\_xml entries. For example, after merging update sets, you might want to remove the original sets. This capability is governed by an access control rule \(ACL\) applied to the sys\_update\_set table.

Don’t delete sys\_update\_xml entries, because this action:

-   Doesn’t undo the updates.
-   Removes any record of who applied the customizations.
-   Removes the sys\_update\_xml entries associated with the update set, so customizations are overwritten when the instance is upgraded.

When you try to delete an update entry, a warning message appears. Select **OK** to confirm the deletion.

**Parent Topic:**[Update sets reference](update-sets-reference.md)

