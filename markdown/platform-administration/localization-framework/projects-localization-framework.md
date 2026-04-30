---
title: Create translation projects
description: The Localization Framework provides the means to assemble, manage, and complete localization and translation tasks, from single item assignments to large batch projects.
locale: en-US
release: zurich
product: Localization Framework
classification: localization-framework
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Localization Framework, Translation and localization, Configure core features, Administer]
---

# Create translation projects

The Localization Framework provides the means to assemble, manage, and complete localization and translation tasks, from single item assignments to large batch projects.

The **Localization Projects** feature enable users to bundle multiple localization request items \(LRITMs\) under one project. This allows bulk translation of requested items, thereby increasing the efficiency of the process. To work with Localization Projects, the feature needs to be enabled in Localization settings. A user with localization\_manager role can enable the feature in Localization settings.

Localization tasks are not created automatically. The localization manager adds the requested items to a project and starts the project. All the requested items are then bundled under the localization tasks.

You can also automatically create a localization projects by enabling the **Enable auto creation** option in the Localization Framework settings. A localization project is auto created and the corresponding LRITMs are created, bundled, and added to the localization project. For more information, see [Configure Localization Framework settings](../task/define-translation-preferences.md).

Each localization task has one or more requested items and is grouped in the following sequence:

1.  Localization Framework **settings**: All the requested items are first grouped based on LF settings.
2.  Source language: After the requested items are grouped according to the settings, then same source languages are bundled under one localization task.
3.  Group of 150 requested items: If the number of requested items for a source language is more than 150, then for every group of 150 requested items, one localization task is created.

