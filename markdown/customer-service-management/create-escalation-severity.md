---
title: Create a case or account escalation severity
description: The escalation severity defines the type of escalation and the color used to represent the cases and accounts of this escalation severity in the user interface.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure escalation management, Configure case management, Case management, Organize agent workspaces, Configure, Customer Service Management]
---

# Create a case or account escalation severity

The escalation severity defines the type of escalation and the color used to represent the cases and accounts of this escalation severity in the user interface.

## Before you begin

Role required: sn\_crm\_foundation\_admin or sn\_crm\_escalation\_admin oradmin

## About this task

The assigned severity allows agents to easily identify escalated cases and accounts on lists and forms. The escalation feature provides two escalation severity definitions:

-   **High Severity**: escalated records are highlighted in red.
-   **Medium Severity**: escalated records are highlighted in orange.

The user interface determines which fields are highlighted for escalated cases and accounts:

-   **Agent Workspace**: Field indicators and field highlights appear on the **Short description** field for escalated cases and on the **Name** field for escalated accounts.

    **Note:** You can move indicators and highlights to any field that is not a hyperlinked field.

-   **Platform interface**: Escalated case and account numbers are indicated with a colored dot on a list and a colored background on a form.

## Procedure

1.  Navigate to **All** &gt; **Customer Service** &gt; **Escalation Severity**.

2.  Click **New**.

3.  Enter a **Name** for the severity.

4.  In the **Style** field, enter a color.

    To configure additional escalation severity records, the system administrator must configure a new style with the desired color. For more information, see [Highlight list fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/highlight-list-fields-platform.md).

5.  Click **Submit**.


