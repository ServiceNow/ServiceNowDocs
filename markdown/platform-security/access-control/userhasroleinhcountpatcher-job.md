---
title: UserHasRoleInhCountPatcher job for Role Management V2
description: UserHasRoleInhCountPatcher job for resolving role inheritance discrepancies.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-security/access-control/userhasroleinhcountpatcher-job.html
release: zurich
product: Access Control
classification: access-control
topic_type: concept
last_updated: "2026-08-05"
reading_time_minutes: 1
breadcrumb: [Contextual Security Manager, Access Control List Rules, Access Management]
---

# UserHasRoleInhCountPatcher job for Role Management V2

UserHasRoleInhCountPatcher job for resolving role inheritance discrepancies.

## About the UserHasRoleInhCountPatcher job

When group or role assignments occur simultaneously, users can end up with role inheritance discrepancies — either missing roles they should have or holding roles they shouldn't. The UserHasRoleInhCountPatcher job periodically checks for these discrepancies in the `sys_user_has_role` table and corrects them, keeping each user's assigned roles accurate.

**Note:** The **UserHasRoleInhCountPatcher** job applies only to Role management V2.

To enable this feature, add the `glide.security.inh_count_patcher.enabled` system property and set its value to `true`.

