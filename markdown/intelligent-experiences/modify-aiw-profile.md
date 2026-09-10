---
title: Edit the profile of an AI specialist in the legacy AI Agent Studio
description: Modify the profile of an AI specialist in the legacy AI Agent Studio to set its name, description, roles, and assignment groups.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/modify-aiw-profile.html
release: australia
topic_type: task
last_updated: "2026-08-11"
reading_time_minutes: 1
keywords: [AI specialist, AI specialist profile]
breadcrumb: [Configure in the legacy AI Agent Studio, Configure, Autonomous Workforce, Enable AI experiences]
---

# Edit the profile of an AI specialist inthe legacy AI Agent Studio

Modify the profile of an AI specialist inthe legacy AI Agent Studio to set its name, description, roles, and assignment groups.

## Before you begin

Role required: sn\_aia.admin

## About this task

AI specialists profiles determine the unique specialties of the AI specialist. Choosing the right roles helps give your AI specialist the context necessary to accomplish its tasks.

To learn how to modify the tasks that an AI specialist is capable of, see [Edit the tasks of an AI specialist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/modify-aiw-tasks.md).

## Procedure

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage**.

2.  In the **AI specialists** tab, select the AI specialist you want to edit.

3.  In the **Profile** tab, select the edit icon next to the name of the AI specialist.

4.  Choose your AI specialist's assignment groups.

    The assignment groups determine what work the AI specialist can pick up. Multiple teams can use the same AI specialist. If you remove your team from the list of assignment groups, the AI specialist won't handle your team's tickets.

5.  Select your AI specialist's role\(s\).

    Roles determine what data access your AI specialist has. For example, if the AI specialist has a role that grants it access to the Incident table, it can work on incidents. If the role\(s\) don't grant access to a specific table, the AI specialist can't pick up work on that table, even if it is within the domain of its capabilities and assignment group.

    Review the full list of roles granted to the AI specialist to check your AI specialist has access only to what it needs to accomplish tasks.

    \[Omitted image "aiw-aias-profile.png"\] Alt text: Fill in the profile section of the AI specialist guided setup in AI Agent Studio

6.  Select **Save** to save your changes.

    You can make additional changes to your AI specialist before selecting save. Changing tabs in the AI specialist guided setup won't lose your changes.

    If you don't select **Save** before navigating to a new page or closing the browser, your changes are lost.


## Result

Your AI specialist profile is updated. Your AI specialist has the updated context for understanding its role when accomplishing tasks.

