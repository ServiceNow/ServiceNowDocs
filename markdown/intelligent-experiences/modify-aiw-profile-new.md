---
title: Edit the profile of an AI specialist in AI Agent Studio
description: Modify the profile of an AI specialist in AI Agent Studio to set its name, description, roles, and assignment groups.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/modify-aiw-profile-new.html
release: zurich
topic_type: task
last_updated: "2026-05-26"
reading_time_minutes: 2
breadcrumb: [Configure in AI Agent Studio, Configure, Autonomous Workforce, AI Agent Studio, Enable AI experiences]
---

# Edit the profile of an AI specialist in AI Agent Studio

Modify the profile of an AI specialist in AI Agent Studio to set its name, description, roles, and assignment groups.

## Before you begin

Role required: sn\_aia.admin

## About this task

AI specialists profiles determine the unique specialties of the AI specialist. Choosing the right roles helps give your AI specialist the context necessary to accomplish its tasks.

To learn how to modify the tasks that an AI specialist is capable of, see [Edit the tasks of an AI specialist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/modify-aiw-tasks-new.md).

## Procedure

1.  Navigate to the **All** &gt; **AI Agent Studio** &gt; **Agentic solutions**.

2.  Select the AI specialist you want to modify.

3.  In the node view, select the first node of the AI specialist.

    The first node contains the main configuration settings for the AI specialist. The other nodes represent the individual agents that comprise the underlying architecture and don't require modification to change the profile of the AI specialist.

4.  Update the name, profile icon, title, and description of your AI specialist.

    The user ID must match the ID of an existing record on the User table with the AI user type.

5.  Choose your AI specialist's assignment groups.

    The assignment groups determine what work the AI specialist can pick up. Multiple teams can use the same AI specialist, but you can create copies of a AI specialist if you want to fine-tune an AI specialist for different teams. See [Create a copy of an AI specialist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/copy-aiw.md) for more information.

    If you remove your team from the list of assignment groups, the AI specialist won't handle your team's tickets.

6.  Select your AI specialist's role\(s\).

    Roles determine what data access your AI specialist has. For example, if the AI specialist has a role that grants it access to the Incident table, it can work on incidents. If the role\(s\) don't grant access to a necessary table, the AI specialist can't pick up work on that table, even if it's within the assignment group's domain.

    Review the full list of roles granted to the AI specialist to check your AI specialist has access only to what it needs to accomplish tasks.

    \[Omitted image "aiw-aias-2-profile.png"\] Alt text: Fill in the profile section of the AI specialist guided setup in AI Agent Studio

7.  Select **Save** to save your changes.

    You can make additional changes to your AI specialist before selecting save.

    If you don't select **Save** before navigating to a new page or closing the browser, your changes are lost.


