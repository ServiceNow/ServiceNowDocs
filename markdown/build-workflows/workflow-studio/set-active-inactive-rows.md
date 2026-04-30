---
title: Set rows active or inactive
description: Activating a row in a Decision Tables includes its conditions and rules when executing the Decision Tables, while deactivating rows excludes the logic while executing the Decision Tables. This feature lets you use or skip conditions in the rows when executing the Decision Tables without deleting them.
locale: en-US
release: yokohama
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Using decision tables, Using Workflow Studio, Workflow Studio, Build workflows]
---

# Set rows active or inactive

Activating a row in a Decision Tables includes its conditions and rules when executing the Decision Tables, while deactivating rows excludes the logic while executing the Decision Tables. This feature lets you use or skip conditions in the rows when executing the Decision Tables without deleting them.

This feature helps you to mark Decision Tables row as either active or inactive. Here's how it works:

-   Mark Rows as inactive- If you mark a row as inactive, the system excludes the rules and logic in the rows while executing the conditions given in the Decision Tables. This feature enables you to disable certain rules temporarily without deleting them, making it easier to test changes or troubleshoot issues.

    **Note:** .

    -   By default, the rows are set to active state.
    -   You can activate or deactivate multiple rows. You can select the ![ellipses](../image/ellipses.png)**Inactive row** &gt; **Active row**.
    ![Setting rows as inactive](../image/inactive-rows.png)

-   Mark Rows as active- If you mark a row as active, the system includes the rules and logic in the rows while executing the conditions given in the Decision Tables. It’s useful for verifying that conditions in the rows are met while executing the Decision Table.

    **Note:** Inactive rows can be identified with a Grey color band appearing in the beginning of the row as in the screenshot.

    ![Setting rows as active](../image/active-rows.png)


**Parent Topic:**[Using decision tables](using-decision-builder.md)

