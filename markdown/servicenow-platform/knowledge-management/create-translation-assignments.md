---
title: Create translation assignments for knowledge articles
description: Assign knowledge articles to language experts to ensure accurate translations. Identify the language experts and create assignment rules so that translation tasks are automatically assigned to language experts and groups.
locale: en-US
release: zurich
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Use translation management, Using Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Create translation assignments for knowledge articles

Assign knowledge articles to language experts to ensure accurate translations. Identify the language experts and create assignment rules so that translation tasks are automatically assigned to language experts and groups.

## Before you begin

Role required: knowledge\_admin or admin

## About this task

Translation tasks are automatically assigned once the assignment rules are created. Assignment rules are applied only if a task is not already assigned to another user or group.

## Procedure

1.  Navigate to **All** &gt; **Knowledge** &gt; **Translation Management** &gt; **Translator Mapping**.

2.  Click **New** to create a new assignment rule.

3.  Enter a name for the assignment rule in the **Name** field.

4.  In the **Applies To** tab, choose the task type you want to assign by setting a condition.

    1.  Select the **Knowledge Translation Task \[kb\_translation\_task\]** table from the **Table** drop-down list.

    2.  Set a condition for assigning tasks in the **Conditions** field.

        For example, to assign tasks for translation into English, you would set the condition to**\[Translated language\]\[is\]\[English\].**

5.  In the **Assign To** tab, select the user or group you want to assign the task to.

6.  Click the **Script** tab to enter a script to further customize the assignment rule.

7.  Click **Submit**.


## Result

An email notification is sent to the user or group that has been assigned the task with a link to the translation task and source article.

**Parent Topic:**[Use translation management](../concept/use-translation-management.md)

