---
title: Select an application from the application picker
description: Use the application picker to select the application scope to which any new records and updates apply.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Use, Legacy Application Manager, Administering applications, Get started, Administer]
---

# Select an application from the application picker

Use the application picker to select the application scope to which any new records and updates apply.

## Before you begin

Role required: delegated\_developer or admin.

## About this task

Application developers must select an application as their current scope context. Any new records become part of this application. The ServiceNow AI Platform also uses the current application scope to determine if the developer can view or make changes to records in other scope contexts.

## Procedure

1.  In the Unified Navigation menu, select the picker icon\(![Picker icon.](../image/icon-scope.png)\).

    When your application scope is set to a non-Global scope, the picker icon displays with a red ring \(![Picker icon with red ring.](../image/icon-scope-changed.png)\).

2.  Select **Application scope** to open a list of scopes available to you.

    ![In Unified Navigation, the application scope picker icon is highlighted.](../image/application-scope-picker-unif-nav.png "Application scope picker in Unified Navigation")

3.  When admins change the application scope, the system automatically switches the current update set to be the application's default update set.

    Admins can modify this by selecting **Update set** and choosing a different one from the list.


## What to do next

The application picker is part of the Next Experience picker. For more information, see [Exploring Next Experience pickers](https://www.servicenow.com/docs/access?context=next-experience-pickers&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US).

For more information about application scoping, see [Application scope](https://www.servicenow.com/docs/access?context=c_ApplicationScope&version=zurich&pubname=zurich-application-development&ft:locale=en-US).

For more information about selecting update sets, see [Select the current update set in Unified Navigation](https://www.servicenow.com/docs/access?context=select-update-set-system-settings&version=zurich&pubname=zurich-application-development&ft:locale=en-US).

**Parent Topic:**[Using Legacy Application Manager](using-legacy-application-manager.md)

