---
title: Create a copy of an AI specialist in AI Agent Studio
description: Create a new copy of an AI specialist to configure different settings for different assignment groups
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/copy-aiw-new.html
release: australia
topic_type: task
last_updated: "2026-05-26"
reading_time_minutes: 1
breadcrumb: [Use in AI Agent Studio, Use, Autonomous Workforce, Enable AI experiences]
---

# Create a copy of an AI specialist in AI Agent Studio

Create a new copy of an AI specialist to configure different settings for different assignment groups

## Before you begin

Role required: sn\_aia.admin

## About this task

The base AI specialist can be configured to cover general or the most likely situations. Creating a copy of an AI specialist allows you to make specific changes for different assignment groups, such as different capabilities. You can also specify exactly which roles have access to the copy.

You can't change the tasks of an AI specialist at the copy level. Tasks must be configured for the base AI specialist.

## Procedure

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Agentic solutions**.

2.  Select the AI specialist you want to copy.

3.  In the node view, select the first node of the AI specialist.

    The first node contains the main configuration settings for the AI specialist. The other nodes represent the individual agents that comprise the underlying architecture and do not require access or modification to create a copy of an AI specialist.

4.  Scroll down to the **Management** section in the AI specialist guided setup to configure the different access settings.

5.  In the Copies section, select **Add copy**.

6.  Review the basic details and profile of the base AI specialist, then make changes for the specific copy.

    For example, you may want to change the name of the AI specialist or its department or description.

7.  Assign the copy of the AI specialist to an assignment group.

8.  Select a manager for the AI specialist.

    A manager might be the Service Desk Manager whose team the AI specialist will be a part of.

9.  Select the roles to access this copy of the AI specialist.


## Result

A new instance of an AI specialist is configured for a new assignment group.

## What to do next

The copy of the AI specialist can be made available to users by publishing and activating the base AI specialist.

