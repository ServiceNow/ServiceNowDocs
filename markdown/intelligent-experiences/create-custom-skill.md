---
title: Create a custom skill in ServiceNow Cowork
description: Create a skill for Cowork to do a specific task, customizing it to fit your needs. After running the same type of task a few times, turn it into a skill so future runs require just one prompt instead of detailed instructions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/create-custom-skill.html
release: brazil
topic_type: task
last_updated: "2026-09-27"
reading_time_minutes: 1
keywords: [custom skills, skill creator, slash commands]
breadcrumb: [Extend ServiceNow Cowork, Use, ServiceNow Cowork, Extending AI with external systems and providers, Enable AI Experiences]
---

# Create a custom skill in ServiceNow Cowork

Create a skill for Cowork to do a specific task, customizing it to fit your needs. After running the same type of task a few times, turn it into a skill so future runs require just one prompt instead of detailed instructions.

## Before you begin

Role required: sn\_app\_cowork.user

## About this task

Cowork includes a default skill, that builds new skills for you. You describe the task, and Cowork creates the skill with a name, a description that the agent uses to determine when to apply it, and instructions.

## Procedure

1.  In the message box, ask Cowork to create a skill and describe what it should do.

    For example: Create a skill that turns my weekly incident notes into a status summary for my manager, using the same headings every time.

2.  Select the send icon.

3.  Answer any questions Cowork asks about the steps, format, or sources.

4.  Review the skill in the chat, and ask for changes if needed.

5.  Navigate to **Settings** &gt; **Skills**.

6.  Select the refresh icon to view the skill.

    The skill appears in the list.

7.  Filter the list by selecting **Custom** under **Filters**.


## Result

Cowork uses the skill automatically when a request matches its description. If the skill is user invoked, enter its name as a slash command \(/\) in the message box.

## What to do next

Be specific about the output you need. A skill that names its format and sources gives more consistent results. To edit a skill's files, navigate to the Skills page.

**Parent Topic:**[Extend ServiceNow Cowork](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/extending-cowork.md)

