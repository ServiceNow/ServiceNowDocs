---
title: Configuring Instance Clone
description: Register your instance for cloning and create a custom clone profile.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-09-12"
reading_time_minutes: 1
breadcrumb: [Instance Clone, Configure core features, Administer]
---

# Configuring Instance Clone

Register your instance for cloning and create a custom clone profile.

## Configuration overview

1.  Register your target instance through the [Clone Admin Console](configure-target-instance.md) or [the legacy experience](t_CreateACloneTarget.md) before requesting your clone.

    A clone target record specifies the instance URL and credentials used for cloning.

2.  Create a custom clone profile in the [Clone Admin Console](configure-clone-profile.md) or [the legacy experience](../reference/system-profile-clone.md).

    Clone profiles enable you to select the correct exclusions and preservers for your clone.

3.  Create a clone preserver in the [Clone Admin Console](create-new-clone-preserver.md) or [the legacy experience](t_CreateADataPreserver.md).

    Create clone preservers to protect data on the target instance from being overwritten.

4.  Exclude a table from cloning in the [Clone Admin Console](exclude-a-table-from-cloning.md) or [the legacy experience](t_ExcludeATableFromCloning.md).

    Exclude a table to create an empty but usable table on the target instance.

5.  Create cleanup scripts in the [Clone Admin Console](create-cleanup-script.md) or [the legacy experience](../concept/post-clone-cleanup-scripts.md).

    Use cleanup scripts to automate post-clone steps or to modify data after your clone.


