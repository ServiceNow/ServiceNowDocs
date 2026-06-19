---
title: Configure an action configuration record
description: Create an action configuration record for a form or list action and copy the action configuration record's sys\_id.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-user-interface/configure-user-experiences/config-da-action-configuration.html
release: zurich
product: Configure User Experiences
classification: configure-user-experiences
topic_type: task
last_updated: "2025-10-17"
reading_time_minutes: 1
breadcrumb: [Configure action buttons, Declarative actions, Administer, Configurable Workspace UI, Configure UIs and portals, Configure user experiences]
---

# Configure an action configuration record

Create an action configuration record for a form or list action and copy the action configuration record's sys\_id.

## Before you begin

Role required: admin

## About this task

An action configuration is a record that defines how and where a declarative action is used in a Configurable Workspace.

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **Declarative Actions** and select either **Form Actions** or **List Actions**.

    An Action Assignment record opens.

2.  Select the **Action Configurations** related list tab.

3.  Select **New**.

    A new UX Actions Configuration record opens.

4.  Complete the following fields:

    -   **Name**

        Enter a name for the action configuration.

    -   **Description**

        Enter a description for the action configuration.

5.  Select the Additional actions icon \(\[Omitted image "MenuIcon.png"\] Alt text:\), and select **Copy sys\_id**.

    The action configuration record’s sys\_id is copied to clipboard. You’ll need to use the sys\_id in UI Builder to display the action on a workspace page.

    For example, you can display a restricted global list action on a specified workspace page. For instructions, see [Restrict a global list action to a workspace page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-user-interface/configure-user-experiences/config-da-limit-workspace-page.md).

6.  Select **Submit**.


## Result

An action configuration record is created for the form or list action, and the action configuration record's sys\_id is copied to clipboard.

