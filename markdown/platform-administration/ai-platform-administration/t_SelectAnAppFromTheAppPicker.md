---
title: Select an application from the application picker
description: Use the application picker to select the application scope to which any new records and updates apply.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/ai-platform-administration/t\_SelectAnAppFromTheAppPicker.html
release: australia
product: AI Platform Administration
classification: ai-platform-administration
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Use, Legacy Application Manager, Administering applications, Get started, Administer the ServiceNow AI Platform]
---

# Select an application from the application picker

Use the application picker to select the application scope to which any new records and updates apply.

## Before you begin

Role required: delegated\_developer or admin.

## About this task

Application developers must select an application as their current scope context. Any new records become part of this application. The ServiceNow AI Platform also uses the current application scope to determine if the developer can view or make changes to records in other scope contexts.

## Procedure

1.  In the Unified Navigation menu, select the picker icon\(\[Omitted image "icon-scope.png"\] Alt text: Picker icon.\).

    When your application scope is set to a non-Global scope, the picker icon displays with a red ring \(\[Omitted image "icon-scope-changed.png"\] Alt text: Picker icon with red ring.\).

2.  Select **Application scope** to open a list of scopes available to you.

    \[Omitted image "application-scope-picker-unif-nav.png"\] Alt text: In Unified Navigation, the application scope picker icon is highlighted.

3.  When admins change the application scope, the system automatically switches the current update set to be the application's default update set.

    Admins can modify this by selecting **Update set** and choosing a different one from the list.


## What to do next

The application picker is part of the Next Experience picker. For more information, see .

For more information about application scoping, see .

For more information about selecting update sets, see .

**Parent Topic:**[Using Legacy Application Manager](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-platform-administration/using-legacy-application-manager.md)

