---
title: Conflicts between changeset commits
description: Service delivery can include multiple teams working at the same time on config data with potentially hundreds of configuration changes every day. Because changes can be in conflict with earlier changes by a different user, CDM manages commits and snapshots to block commits that conflict. You are notified of changeset conflicts to help you to resolve them.
locale: en-US
release: xanadu
product: DevOps \(Family\)
classification: devops-family
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Changesets and version control in CDM, Use, DevOps Config, IT Service Management]
---

# Conflicts between changeset commits

Service delivery can include multiple teams working at the same time on config data with potentially hundreds of configuration changes every day. Because changes can be in conflict with earlier changes by a different user, CDM manages commits and snapshots to block commits that conflict. You are notified of changeset conflicts to help you to resolve them.

**Important:** Starting with the Washington DC release, DevOps Config is being prepared for future deprecation. It will be hidden and no longer installed on new instances but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

## When a conflict happens

Every time you attempt to commit a changeset, the system determines whether there are conflicts with other earlier commits. If the system reports a conflict, you can choose to attempt to keep some of the changes or discard all conflicted changes and start from a new changeset. For this reason, to ease the task of recreating your work, you might copy-paste larger changes to a text editor before closing a conflicted changeset.

## How to avoid conflicts

Follow these suggestions to avoid conflicts:

-   Try to keep a changeset open for a brief period. If you need to do research, close the changeset and start a new changeset after you have the information.
-   Coordinate your code editing tasks with coworkers. This enables you to avoid updating the same configuration item at the same time.

## Types of conflicts

In each of the following examples of an identified conflict, the "item" being described is the configuration data item \(CDI\) in your changeset. Another user committed changes that your changes conflict with.

-   **Stale data in your working changeset**
    -   The value of the item was changed in another changeset.
    -   The item is no longer included in a collection or deployable in another changeset.
    -   Data corruption caused by an incorrect change in the data table: The newly added item in your open changeset was modified in the data table to incorrectly refer to a previous version. The item in your open changeset was superseded by a change in the data table. The updated or deleted item in your open changeset was incorrectly modified in the data table to not refer to the previous version.
-   **Changed parent**

    The item is an orphan because its parent was deleted or renamed in another changeset.

-   **Changed parent/child relationship**

    New items were added in another changeset while you made changes to the parent data item.

-   **Changed references**
    -   The Item was included in a collection or deployable in another changeset.
    -   The item cannot be deleted because it is included in a collection or deployable in another changeset.
-   **Duplicate**

    An item with the same name already exists.

-   **Invalid includes**
    -   The component or collection to which the include referred was deleted in another changeset.
    -   The component or collection to which the include referred was renamed in another changeset.
    -   A descendent of the component to be included is already included in the collection in another changeset.

