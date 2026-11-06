---
title: Create a custom skill in ServiceNow Arc
description: Create a skill for Arc to do a specific task, customizing it to fit your needs. After running the same type of task a few times, turn it into a skill so future runs require only one prompt instead of detailed instructions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/application-development/create-custom-skill.html
release: australia
topic_type: task
last_updated: "2026-09-27"
reading_time_minutes: 1
keywords: [custom skills, skill creator, slash commands]
breadcrumb: [Extend ServiceNow Arc, Use, ServiceNow Arc, Extend, AI Workflow Factory Prime, Agentic app development, Building applications]
---

# Create a custom skill in ServiceNow Arc

Create a skill for Arc to do a specific task, customizing it to fit your needs. After running the same type of task a few times, turn it into a skill so future runs require only one prompt instead of detailed instructions.

## Before you begin

Role required: sn\_app\_arc.user

## About this task

Arc includes a default skill, that builds new skills for you. You describe the task, and Arc creates the skill with a name, a description that the agent uses to determine when to apply it, and instructions.

## Procedure

1.  In the message box, ask Arc to create a skill and describe what it should do.

    For example: Create a skill that turns my weekly incident notes into a status summary for my manager, using the same headings every time.

2.  Select the send icon.

3.  Answer any questions Arc asks about the steps, format, or sources.

4.  Review the skill in the chat, and ask for changes if needed.

5.  Navigate to **Settings** &gt; **Skills**.

6.  Select the refresh icon to view the skill.

    The skill appears in the list.

7.  Filter the list by selecting **Custom** under **Filters**.


## Result

Arc uses the skill automatically when a request matches its description. If the skill is user invoked, enter its name as a slash command \(/\) in the message box.

## What to do next

Be specific about the output you need. A skill that names its format and sources gives more consistent results. To edit a skill's files, navigate to the Skills page.

**Parent Topic:**[Extend ServiceNow Arc](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/extending-cowork.md)

