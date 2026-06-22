---
title: Set up a character counter for journal fields
description: A character counter displays the number of remaining characters in a journal field.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/platform-user-interface/configure-user-experiences/set-up-character-counter-journal-fields.html
release: yokohama
product: Configure User Experiences
classification: configure-user-experiences
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Administering forms for Configurable Workspace, Administering Configurable Workspace, Configurable Workspace UI, Configure UIs and portals, Configure user experiences]
---

# Set up a character counter for journal fields

A character counter displays the number of remaining characters in a journal field.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to `sys_properties.list`.

2.  Add a system property named **glide.ui.textarea.character\_counter**.

    For more information on adding system property, see [Add a system property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/ai-platform-administration/t_AddAPropertyUsingSysPropsList.md).

3.  Set the Value to **true**.

4.  Select **Submit**.


