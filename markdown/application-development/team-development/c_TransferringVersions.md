---
title: Versions transferring
description: Administrators transfer version records between instances by moving customizations with Update Sets or the Team Development application.
locale: en-US
release: yokohama
product: Team Development
classification: team-development
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Versions, Using Team Development, Team Development, Planning your application, Building applications]
---

# Versions transferring

Administrators transfer version records between instances by moving customizations with Update Sets or the Team Development application.

-   Update sets: committing an Update Set adds versions. For each update in the Update Set, the version that corresponds to the update is added on the local instance.
-   Team Development:
    -   Pulling retrieves from the parent instance all versions of customized records that have not already been pulled and then adds them on the local instance.
    -   Pushing adds to the parent instance only the current local version, not all the local versions.
    -   Loading changes from peer instances adds selected versions to the local instance.

**Parent Topic:**[Versions](c_Versions.md)

