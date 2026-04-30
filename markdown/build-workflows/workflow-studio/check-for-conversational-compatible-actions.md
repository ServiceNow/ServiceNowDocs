---
title: Check for conversational compatible actions
description: Run a compatibility check on new or all actions to determine if they are conversational compatible. Review the inputs of an action to determine if their data types are compatible.
locale: en-US
release: yokohama
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2025-04-10"
reading_time_minutes: 1
breadcrumb: [Conversational actions, Exploring actions, Exploring Workflow Studio, Workflow Studio, Build workflows]
---

# Check for conversational compatible actions

Run a compatibility check on new or all actions to determine if they are conversational compatible. Review the inputs of an action to determine if their data types are compatible.

## Before you begin

Role required:

-   admin, flow\_designer, or action\_designer
-   now.assist.creator

## About this task

You can only configure conversational settings for actions that are marked as conversational compatible. Run a compatibility check to update the list of conversational compatible actions. After you create or update an action, run a compatibility check to determine if you can make it conversational.

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  On the homepage, select **Actions**.

3.  Go to the **Conversational compatible** tab and select **Run compatibility check**.

    ![Image of the Conversational compatible tab on the Actions page.](../images/conv-compatible-action.png)

    By default, the system only checks new actions that were created since the last compatibility check. If you want to check all actions, select **Complete scan**. You can use a complete scan to verify that updated actions remain conversationally compatible.

    The system runs a compatibility check in the background. The more actions there are to check, the longer the compatibility check takes.


## Result

The system updates the list of conversational compatible actions.

## What to do next

To make an action conversational, configure its conversational settings. See [Configure action conversational settings](configure-action-conversation-settings.md).

**Parent Topic:**[Conversational actions](../concept/conversational-actions.md)

