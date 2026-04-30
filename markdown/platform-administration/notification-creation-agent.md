---
title: Notification agent
description: Use the Notification agent to create and modify email notifications, templates, and layouts through conversation, reducing the need of navigating complex forms and scripts.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2026-03-16"
reading_time_minutes: 1
breadcrumb: [Now Assist in Notifications, Configure core features, Administer]
---

# Notification agent

Use the Notification agent to create and modify email notifications, templates, and layouts through conversation, reducing the need of navigating complex forms and scripts.

## Notification agent capabilities

The Notification agent is an agentic AI feature within Now Assist. It simplifies the process of creating and modifying email notifications, template, and layouts using natural language prompts.

Describe your notification requirement, and the agent handles configuration, templates, layouts, and duplicate detection.

**Note:**

The Notification agent may produce inconsistent results when used with the Now LLM model.

## End to end notification creation using the Notification agent

The following table shows how a platform administrator creates, applies email templates, tests, and activates a P1 incident notification using the agent chat interface.

|Example|Scenario|Action|Agent output|
|-------|--------|------|------------|
|Creating a notification from a natural language prompt.|A platform administrator needs to notify users when a P1 incident is assigned to them without navigating the Notifications module.|Create a notification whenever a P1 incident is assigned to a user from the sys\_user \[sys\_user\] table.|The agent checks for duplicates and generates a notification record with the name, table, trigger, and recipients populated for review.|
|Modifying preview content.|After previewing the generated notification, the administrator wants to adjust the email template content.|Add the incident priority to the email body.|The agent updates the email template to include the incident priority field and presents it for review.|

