---
title: Tracking CI Relationships
description: Changes to a CI relationship \(CI Relations, CI/User Relations, or CI/Group Relations\) appear in the history of the items on both sides of the changed relationship regardless of whether the change was manual or a result of Discovery.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Knowing about History sets, Auditing, Platform Security]
---

# Tracking CI Relationships

Changes to a CI relationship \(CI Relations, CI/User Relations, or CI/Group Relations\) appear in the history of the items on both sides of the changed relationship regardless of whether the change was manual or a result of Discovery.

For example, if the computer alpha has a used by CI Relation with the computer beta, then the history for alpha has a record of when the relationship with beta was established, and likewise, the history for beta has a record of when the relationship with alpha was established. This example illustrates the history displayed when some CI Relations are established, and then one of the relations is removed:

![](../image/CIRelationshipHistory.png "CI Relationship History")

The created bullet indicates the date that the CI, user, or group was created. The last activity bullet refers to when the relationships were last changed. If you don't want to show CI relationship history for any or all CI relationship types, you can turn it off by disabling auditing on the CI relationship tables \(CI Relationship \[`cmdb_rel_ci`\], CI/User Relationship Type \[`cmdb_rel_user_type`\], or Group Relationship \[`cmdb_rel_group`\]\).

