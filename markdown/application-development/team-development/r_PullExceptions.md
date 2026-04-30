---
title: Pull exceptions
description: Pulling ignores versions when certain conditions occur.
locale: en-US
release: yokohama
product: Team Development
classification: team-development
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Team Development, Exploring Team Development, Team Development, Planning your application, Building applications]
---

# Pull exceptions

Pulling ignores versions when certain conditions occur.

|Issue|Description|
|-----|-----------|
|Matched an exclusion policy|An exclusion policy prevents pulling changes for records matching the policy conditions. The pull identifies the changes but does not include versions for these records.|
|Private properties|A private property is excluded from all Update Sets and pulls.|
|Collisions|A collision is detected when the pulled version and the current local version both include modifications to the same record. You must resolve all collisions before you can pull.|
|Previously resolved collisions|When you resolved a collision by accepting either the pulled version or local version of a record, the pull remembers your decision and accepts the version that you indicated as a "previously resolved collision".|
|Skipped|Pulls skip versions where there is a problem with the version record such as a corrupt or missing version.|

**Parent Topic:**[Team Development](../concept/c_TeamDevelopment.md)

