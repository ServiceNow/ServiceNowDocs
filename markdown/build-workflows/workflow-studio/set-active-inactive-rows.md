---
title: Set rows active or inactive
description: Set rows in a Decision Tables as active or inactive to include or exclude their conditions and rules during execution without deleting them.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/build-workflows/workflow-studio/set-active-inactive-rows.html
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2026-07-22"
reading_time_minutes: 1
breadcrumb: [Decision tables, Decision tables, Workflow Studio, Build workflows]
---

# Set rows active or inactive

Set rows in a Decision Tables as active or inactive to include or exclude their conditions and rules during execution without deleting them.

Mark a Decision Tables row as active or inactive:

-   Inactive rows: If you mark a row as inactive, the system excludes the rules and logic in the rows while executing the conditions in the Decision Tables. You can disable certain rules temporarily without deleting them, which helps when testing changes or troubleshooting issues.

    **Note:**

    -   By default, the rows are set to active state.
    -   You can activate or deactivate multiple rows. You can select the \[Omitted image "ellipses.png"\] Alt text: ellipses**Inactive row** &gt; **Active row**.
    \[Omitted image "inactive-rows.png"\] Alt text: Setting rows as inactive

-   Active rows: If you mark a row as active, the system includes the rules and logic in the rows while executing the conditions in the Decision Tables. Use active rows to verify that conditions in the rows are met during execution.

    **Note:** Inactive rows are identified by a gray color band at the beginning of the row.

    \[Omitted image "active-rows.png"\] Alt text: Setting rows as active


**Parent Topic:**[Decision tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/using-decision-builder.md)

