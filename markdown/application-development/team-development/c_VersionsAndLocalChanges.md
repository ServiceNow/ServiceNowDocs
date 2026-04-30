---
title: Versions and local changes
description: Version records track changes to a customizable record over time so that you can compare or revert to a specific version later.
locale: en-US
release: xanadu
product: Team Development
classification: team-development
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Team Development, Planning your application, Building applications]
---

# Versions and local changes

Version records track changes to a customizable record over time so that you can compare or revert to a specific version later.

A version record is created every time a developer changes a customizable record, so a single record can have multiple version records associated with it. A local change record is created or updated to reference the current version every time a developer modifies a customizable record, so a single record can have only one local change record associated with it.

Local change records track which customized records have changes on the development instance that are not on the parent instance so that you can collect changes in preparation for a push.

![Hierarchy of development instances and the workflow](../image/TeamDevConcepts.png "Team Development concepts")

Developers can back out a local change to restore a previous version of a customizable record. The back out action sets the local customizable record to the last revision identified by a reconciliation action.

**Parent Topic:**[Team Development](c_TeamDevelopment.md)

