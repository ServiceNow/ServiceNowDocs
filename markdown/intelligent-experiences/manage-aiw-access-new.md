---
title: Manage access to an AI specialist in AI Agent Studio
description: Control workspace access, user roles, and publishing settings for your AI specialist and its copies configured for specific teams.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/manage-aiw-access-new.html
release: australia
topic_type: task
last_updated: "2026-01-31"
reading_time_minutes: 2
keywords: [AI specialist, access management, workspace access, role configuration, AI workforce]
breadcrumb: [Use in AI Agent Studio, Use, Autonomous Workforce, Enable AI experiences]
---

# Manage access to an AI specialist in AI Agent Studio

Control workspace access, user roles, and publishing settings for your AI specialist and its copies configured for specific teams.

## Before you begin

Verify that you have an AI specialist created and configured.

Role required: sn\_aia.admin

## About this task

Configure access settings to control which workspaces and users can interact with your AI specialist. You can also manage different copies of AI specialists configured for specific assignment groups or teams with varying access requirements.

Access management includes workspace permissions, role-based security, publishing status, and copy creation privileges. These settings determine the operational scope and security boundaries for your AI specialist.

## Procedure

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Agentic solutions**.

2.  Select the AI specialist you want to configure from the available list.

3.  In the node view, select the first node representing the AI specialist.

    The first node contains the main configuration settings for the AI specialist. The other nodes represent the individual agents that comprise the underlying architecture and do not require modification for access management.

4.  Scroll down to the **Management** section in the AI specialist guided setup.

    The Management section contains all access control and operational settings for the AI specialist.

5.  Configure workspace access by defining the workspaces where the AI specialist can operate.

    Workspace access determines where agents can monitor the progress and activity of the AI specialist. Users can only interact with the AI specialist within the specified workspaces.

6.  Configure role-based access by selecting which roles have permission to use the AI specialist.

    Users without the specified roles cannot invoke the AI specialist or review its work. Role configuration ensures that only authorized users can interact with the AI specialist.

7.  Set the publishing status by selecting whether to publish the AI specialist.

    Publishing controls whether the AI specialist can perform work on records. An unpublished AI specialist remains inactive even if it meets all other access requirements.

8.  Configure copy creation permissions by selecting whether users with the defined roles can create copies of the AI specialist.

    Copy creation allows teams to customize AI specialist behavior for specific assignment groups or use cases. Different copies can have varying configurations while maintaining the same core functionality.

    For example, you can configure an AI specialist copy for one assignment group to perform specific tasks that differ from those assigned to another group. For more information, see [Create a copy of an AI specialist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/copy-aiw-new.md).

9.  Select **Save** to apply your access configuration changes.

    You can modify additional AI specialist settings before saving. All changes are applied when you select **Save**.

    **Warning:** If you navigate to a different page or close the browser without selecting **Save**, your changes are lost and must be reconfigured.


## Result

Your AI specialist now has configured workspace access, role-based security, publishing status, and copy creation permissions. Users can interact with the AI specialist according to the access settings you defined.

## What to do next

Verify that the access configuration works as expected by testing the AI specialist with users who have the required roles in the specified workspaces. Monitor AI specialist activity to confirm that access restrictions are properly enforced.

