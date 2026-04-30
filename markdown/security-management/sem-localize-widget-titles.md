---
title: Localize widget titles
description: Update the widget title in the Messages \[sys\_ui\_message\_list\] table whenever you create a custom widget or rename an existing one to ensure it displays correctly in localized interfaces.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-10-28"
reading_time_minutes: 1
breadcrumb: [Configure Visualization library, Implement, Unified Security Exposure Management, Security Operations]
---

# Localize widget titles

Update the widget title in the Messages \[sys\_ui\_message\_list\] table whenever you create a custom widget or rename an existing one to ensure it displays correctly in localized interfaces.

## Before you begin

Role required: admin

## About this task

Follow these steps to add the widget title for translation in the Messages table.

## Procedure

1.  Navigate to the Messages table \[sys\_ui\_message\_list\].

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_orj_sky_chc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Key

</td><td>

Widget title as it appears in the visualization library.

</td></tr><tr><td>

Language

</td><td>

Target language \(for example, Japanese\).

</td></tr><tr><td>

Message

</td><td>

Widget title that must be translated.

</td></tr><tr><td>

Application

</td><td>

Application for the widget. Select **Security Exposure Management**.**Note:** Cross-scope access isn’t supported.

</td></tr></tbody>
</table>4.  Select **Submit**.

    **Important:** If you later rename a widget, search for its existing record in the Messages \[sys\_ui\_message\_list\] table, and update the **Key** and **Message** fields with the new widget title.


