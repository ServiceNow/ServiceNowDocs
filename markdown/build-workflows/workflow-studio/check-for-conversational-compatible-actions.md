---
title: Check for conversational compatible actions
description: Run a compatibility check on new or all actions to determine if they are conversational compatible. Review the inputs of an action to determine if their data types are compatible.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/build-workflows/workflow-studio/check-for-conversational-compatible-actions.html
release: zurich
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Conversational actions, Actions, Explore, Workflow Studio, Build workflows]
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

3.  Goo to the **Conversational compatible** tab and select **Run compatibility check**.

    \[Omitted image "conv-compatible-action.png"\] Alt text: Image of the conversational compatible tab on the actions page.

    By default, the system only checks new actions that were created since the last compatibility check. If you want to check all actions, select **Complete scan**. You can use a complete scan to verify that updated actions remain conversationally compatible.

    The system runs a compatibility check in the background. The more actions there are to check, the longer the compatibility check takes.


## Result

The system updates the list of conversational compatible actions.

## What to do next

To make an action conversational, configure its conversational settings. See [Configure action conversational settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/build-workflows/workflow-studio/configure-action-conversation-settings.md).

**Parent Topic:**[Conversational actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/build-workflows/workflow-studio/conversational-actions.md)

