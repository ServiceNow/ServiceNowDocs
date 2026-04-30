---
title: Working with update sets
description: These procedures help you manage your customizations and resolve potential collisions before you move them to another instance.
locale: en-US
release: zurich
product: System Update Sets
classification: system-update-sets
topic_type: concept
last_updated: "2025-08-07"
reading_time_minutes: 2
breadcrumb: [System update sets, Deploying applications, Building applications]
---

# Working with update sets

These procedures help you manage your customizations and resolve potential collisions before you move them to another instance.

## Overview of System update sets

Before using update sets, review [Get started with update sets](../reference/get-started-update-sets.md) to learn when to use and when not to use update sets, and how to plan the update process and avoid common mistakes. Then, create an update set and use it to change a development instance. You can report on updates, merge update sets, and compare update sets to ensure that the desired changes are ready to move.

When the update set is completed, you can transfer the update set to another instance according to your test process. See [Update set transfers](../reference/update-set-transfers.md).

-   [Create and select an update set as the current set](../task/create-select-update-set.md)

    Create an update set to store customization changes and select it as the current set.

-   [Select the current update set in Unified Navigation](../task/select-update-set-system-settings.md)

    You can change the current update set at any time, using the update set picker in Unified Navigation.

-   [View customizations and compare with current version](../task/view-customer-update-records.md)

    View the customizations that make up an update set and compare the update to the current version.

-   [Navigation between records](../reference/navigation-between-records.md)

    You can navigate between a customer update record and the customized object or the application file for the object.

-   [Merge update sets](../task/t_MergeUpdateSets.md)

    You can merge multiple update sets into a single update set. This capability is supported for backward compatibility with earlier releases of the ServiceNow AI Platform®. The newer batch update sets feature accomplishes the same outcome with a more predictable and robust solution.

-   [Compare local update sets](../task/t_CompareLocalUpdateSets.md#)

    Administrators can preview local and remote \(retrieved\) update sets and compare the sets with one another to resolve conflicting changes.

-   [Mark an update set complete](../task/t_CompleteUpdateSets.md)

    When you have completed the customizations and compared local update sets to resolve conflicts, mark the update set as Complete.

-   [Save an update set as a local XML file](../task/t_SaveAnUpdateSetAsAnXMLFile.md#)

    Administrators can export an update set as an XML file to save a specific version of an application or set of changes.


