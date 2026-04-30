---
title: Pull exceptions
description: A reference topic that covers versions that are ignored during pulling when certain conditions occur.
locale: en-US
release: zurich
product: Team Development
classification: team-development
topic_type: reference
last_updated: "2025-10-02"
reading_time_minutes: 1
breadcrumb: [Team Development Reference, Team Development, Planning your application, Building applications]
---

# Pull exceptions

A reference topic that covers versions that are ignored during pulling when certain conditions occur.

|Scenario|Description|
|--------|-----------|
|Matched an exclusion policy|An exclusion policy helps prevent pulling changes for records matching the policy conditions. The pull identifies the changes but doesn’t include versions for these records.|
|Private properties|A private property is excluded from all update sets and pulls.|
|Collisions|A collision is detected when the pulled version and the current local version both include modifications to the same record. You must resolve all collisions before you can pull.|
|Previously resolved collisions|When you resolved a collision by accepting either the pulled version or local version of a record, the pull remembers your decision and accepts the version that you indicated as a previously resolved collision.|
|Skipped version|Pulls skip versions where there’s a problem with the version record such as a corrupt or missing version.|

**Parent Topic:**[Team Development Reference](team-development-reference.md)

