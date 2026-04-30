---
title: Team Development roles
description: Team Development is installed with these roles.Configures a managed instance for use in Team Development.Performs operations, such as pushing, pulling, comparing, and reconciling changes.Review, approve, and reject a pushed code change.
locale: en-US
release: zurich
product: Team Development
classification: team-development
topic_type: reference
last_updated: "2025-09-30"
reading_time_minutes: 1
keywords: [\[teamdev\_configure\_instance\], teamdev\_configure\_instance, teamdev\_user, teamdev\_code\_reviewer]
breadcrumb: [Team Development Reference, Team Development, Planning your application, Building applications]
---

# Team Development roles

Team Development is installed with these roles.

**Parent Topic:**[Team Development Reference](../reference/team-development-reference.md)

## Configure instance \[teamdev\_configure\_instance\]

Configures a managed instance for use in Team Development.

### Contains Roles

teamdev\_configure\_instance

### Groups

Team development.

### Special considerations

This role shouldn’t be granted on the managing instance.

## User \[teamdev\_user\]

Performs operations, such as pushing, pulling, comparing, and reconciling changes.

### Contains Roles

-   soap\_create
-   soap\_update
-   soap\_query

### Groups

Team development.

### Special considerations

None.

## Code reviewer \[teamdev\_code\_reviewer\]

Review, approve, and reject a pushed code change.

Is able to read records from

-   sys\_sync\_history
-   sys\_sync\_history\_version
-   sys\_update\_version
-   sys\_update\_set\_source

### Contains Roles

None.

### Groups

Team development.

### Special considerations

None.

