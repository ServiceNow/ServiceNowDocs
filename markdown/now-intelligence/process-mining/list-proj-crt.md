---
title: Create a Process Mining project from a workspace list
description: Create a Process Mining project directly from a list of records from any ServiceNow workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/process-mining/list-proj-crt.html
release: brazil
product: Process Mining
classification: process-mining
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [process mining, workspace, list action, guided setup]
breadcrumb: [Use, Process Mining, Platform Analytics]
---

# Create a Process Mining project from a workspace list

Create a Process Mining project directly from a list of records from any ServiceNow workspace.

## Before you begin

This feature is available only when:

-   The table in the list is audit-enabled.
-   The user has the sn\_process\_mining\_analyst role.

Role required: sn\_process\_mining\_analyst

## Procedure

1.  Open a workspace from your ServiceNow instance, and select the list icon.

2.  Select a list.

3.  Select **Launch Process Mining** from the list's actions.

    **Note:** If you want to hide this button, see [Hide a global form or list action from a table or view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-user-interface/hide-global-action-from-a-table-or-view.md).

    If the list already has several other actions, **Launch Process Mining** is available in the menu \(...\).

    \[Omitted image "wksp-pm-proj.png"\] Alt text: Create a project from any Workspace

    The project opens in the guided set up of Process Mining Workspace.

4.  Continue to edit the project as required.

    Note that:

    -   If the list has a filter condition, the project inherits the filter conditions.
    -   If a template exists for the table, the project is created using that template.
    -   If a list has filter condition, and the table has a template, the project is created using the template and the filter.
    -   If no template exists for the table, a new project is created and you're taken directly to the Scope your analysis step of the guided setup.
    For information on templates and how to manage them, see [Process Mining templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/process-mining/pm_templates.md).


## Result

The project is created and you're redirected to the project's Overview page.

**Parent Topic:**[Using Process Mining](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/process-mining/use-process-mining.md)

