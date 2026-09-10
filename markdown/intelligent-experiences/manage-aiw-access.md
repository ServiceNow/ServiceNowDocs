---
title: Manage access to an AI specialist in the legacy AI Agent Studio
description: Control workspace access, user roles, and publishing settings for your AI specialist and its copies configured for specific teams.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/manage-aiw-access.html
release: zurich
topic_type: task
last_updated: "2026-08-11"
reading_time_minutes: 2
keywords: [AI specialist, access management, workspace access, role configuration, AI workforce]
breadcrumb: [Use in the legacy AI Agent Studio, Use, Autonomous Workforce, AI Agent Studio, Enable AI experiences]
---

# Manage access to an AI specialist inthe legacy AI Agent Studio

Control workspace access, user roles, and publishing settings for your AI specialist and its copies configured for specific teams.

## Before you begin

Verify that you have an AI specialist created and configured.

Role required: sn\_aia.admin

## About this task

Configure access settings to control which workspaces and users can interact with your AI specialist. You can also manage different copies of AI specialists configured for specific assignment groups or teams with varying access requirements.

Access management includes workspace permissions, role-based security, publishing status, and copy creation privileges. These settings determine the operational scope and security boundaries for your AI specialist.

## Procedure

1.  Navigate to **AI Agent Studio** &gt; **Create and manage**.

2.  Select the AI specialist you want to configure from the available list.

3.  Select the **Management** tab in the AI specialist guided setup.

    The Management tab contains all access control and operational settings for the AI specialist.

4.  Configure workspace access by defining the workspaces where the AI specialist can operate.

    Workspace access determines where agents can monitor the progress and activity of the AI specialist. Users can only interact with the AI specialist within the specified workspaces.

5.  Configure role-based access by selecting which roles have permission to use the AI specialist.

    Users without the specified roles cannot invoke the AI specialist or review its work. Role configuration ensures that only authorized users can interact with the AI specialist.

6.  Configure copy creation permissions by selecting whether users with the defined roles can create copies of the AI specialist.

    Copy creation allows teams to customize AI specialist behavior for specific assignment groups or use cases. Different copies can have varying configurations while maintaining the same core functionality.

    For example, you can configure an AI specialist copy for one assignment group to perform specific tasks that differ from those assigned to another group. For more information, see [Create a copy of an AI specialist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/copy-aiw.md).

    \[Omitted image "aiw-aias-manage-1.png"\] Alt text: Management tab for an AI specialist in AI agent studio with the sections described in the previous steps

7.  Set the active status of the AI specialist.

    Activation controls whether the AI specialist performs work. If an AI specialist is inactive, it won't work on any tasks, even if it is published.

8.  Set the publishing status by selecting whether to publish the AI specialist.

    Publishing controls whether the AI specialist can be seen in workspaces and be assigned to a manager. An unpublished AI specialist remains inactive even if it meets all other access requirements.

    If an AI specialist is unpublished, then it will not be visible for Service Desk Managers or other members of the assignment group, even if it is active.

    \[Omitted image "aiw-aias-manage-2.png"\] Alt text: Management tab for an AI specialist with the active and publish sections

9.  Select **Save** to apply your access configuration changes.

    You can modify additional AI specialist settings before saving. All changes are applied when you select **Save**.

    **Warning:** If you navigate to a different page or close the browser without selecting **Save**, your changes are lost and must be reconfigured.


## Result

Your AI specialist now has configured workspace access, role-based security, publishing status, and copy creation permissions. Users can interact with the AI specialist according to the access settings you defined.

## What to do next

Verify that the access configuration works as expected by testing the AI specialist with users who have the required roles in the specified workspaces. Monitor AI specialist activity to confirm that access restrictions are properly enforced.

