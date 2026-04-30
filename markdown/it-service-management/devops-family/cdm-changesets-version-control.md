---
title: Changesets and version control in CDM
description: A changeset is a draft copy of an application that you can update and save as often as needed. When you are satisfied with your changes, you can commit the changeset to apply the changes to the application. Committing
locale: en-US
release: zurich
product: DevOps \(Family\)
classification: devops-family
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Use, DevOps Config, IT Service Management]
---

# Changesets and version control in CDM

A changeset is a draft copy of an application that you can update and save as often as needed. When you are satisfied with your changes, you can commit the changeset to apply the changes to the application. Committing

**Important:** DevOps Config is now deprecated and no longer supported or available for new activation.

## About changesets

To edit config data, you create a changeset and make changes in the changeset. You can perform the following actions:

-   Create a new changeset: The changeset includes the full config dataset of the application.
-   Save a changeset: The Editor panel, List view, and Preview panel refreshes to reflect the resolved state of the changeset. The system updates the changeset but does not update the application. Changes appear on the **Activity** tab. You must commit a changeset to update the config data for the application. After saving, you can move on to other activities and return later to edit the changeset.
-   Update an existing changeset: Edit a changeset that had been saved but not committed.
-   Commit a saved changeset:  The system generates a snapshot of each deployable that is affected by the changes.

## About conflicts with other changesets of the application that you are working on

Sometimes, UserA and UserB are working at the same time on two different changesets of the same application. If UserA commits a changeset that sets *variableX* to `A` and later, UserB tries to commit a changeset with *variableX* set to `B`, a conflict results.

An open changeset with conflicts is blocked—it cannot be committed. The system notifies you of conflicts with a warning message on the page. In addition, the **State** value in the header changes from **Open** to **Blocked**.

See [Conflicts between changeset commits](cdm-changeset-conflicts.md) for descriptions of the types of conflicts that the system identifies.

