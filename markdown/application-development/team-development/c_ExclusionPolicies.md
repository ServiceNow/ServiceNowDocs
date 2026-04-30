---
title: Exclusion policies
description: You can exclude certain files from change tracking by creating an exclusion policy.
locale: en-US
release: yokohama
product: Team Development
classification: team-development
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Using Team Development, Team Development, Planning your application, Building applications]
---

# Exclusion policies

You can exclude certain files from change tracking by creating an exclusion policy.

When a change matches an exclusion policy, the change does not generate records in the local changes list. The change still generates local version records and Update Set records as normal. See [Creating an Exclusion Policy](../task/t_CreateAnExclusionPolicy.md).

**Note:** The exclusion policy applies to changes identified during a reconciliation operation. If you create an exclusion policy after a reconciliation, Team Development still tracks the changes until the next reconciliation.

