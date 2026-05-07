---
title: Check for conversational compatible subflows
description: Run a compatibility check on new or all subflows to determine if they are conversation compatible. Review the inputs of a subflow to determine if their data types are compatible.
locale: en-US
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Conversational subflows, Explore subflows, Flows, Flows, subflows, and actions, Workflow Studio, Build workflows]
---

# Check for conversational compatible subflows

Run a compatibility check on new or all subflows to determine if they are conversation compatible. Review the inputs of a subflow to determine if their data types are compatible.

## Before you begin

Role required:

-   admin or flow\_designer
-   now.assist.creator

## About this task

You can only configure conversational settings for subflows that are marked as conversational compatible. Run a compatibility check to update the list of conversational compatible subflows. After you create or update a subflow, run a compatibility check to determine if you can make it conversational.

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  On the homepage, select **Subflows**.

3.  Go to the **Conversational compatible** tab and select **Run compatibility check**.

    ![Screen showing the conversational compatible tab on the subflows page.](../images/conv-compatible-subflows.png)

    By default, the system only checks new subflows that were created since the last compatibility check. If you want to check all subflows, select **Complete scan**. You can use a complete scan to verify that updated subflows remain conversationally compatible.

    The system runs a compatibility check in the background. The more subflows there are to check, the longer the compatibility check takes.


## Result

The system updates the list of conversational compatible subflows.

## What to do next

To make a subflow conversational, configure its conversational settings. See [Configure subflow conversational settings](configure-subflow-conversation-settings.md).

