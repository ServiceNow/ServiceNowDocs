---
title: Local changes
description: The Local Changes table tracks which customized records have current versions that exist on the development instance but not on the parent instance.
locale: en-US
release: yokohama
product: Team Development
classification: team-development
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Team Development, Exploring Team Development, Team Development, Planning your application, Building applications]
---

# Local changes

The Local Changes table tracks which customized records have current versions that exist on the development instance but not on the parent instance.

Use local changes to collect changes in preparation for a push.

You queue local changes that are ready to push. Each development instance maintains a single queue, regardless of who develops or queues the changes. You ignore local changes that you do not want to push. For example, you may want to ignore changes to the color scheme that visually distinguish a development instance from the production instance. You can remove a change from the queue or stop ignoring a change.

Changing the parent instance or reconciling recreates the list of local changes that have not been queued or ignored. If you had previously queued or ignored a local change, that designation is maintained.

**Parent Topic:**[Team Development](c_TeamDevelopment.md)

