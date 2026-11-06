---
title: Create a style guide in the Knowledge Center
description: Create a style guide that defines the tone, voice, and terminology AI applies when it generates knowledge articles. Assign the style guide to a knowledge base so that authors can select it during article generation.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/servicenow-platform/create-style-guides-for-articles.html
release: australia
topic_type: task
last_updated: "2026-10-23"
reading_time_minutes: 1
breadcrumb: [Using style guides in the Knowledge Center, Using Knowledge Center, Knowledge Center, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Create a style guide in the Knowledge Center

Create a style guide that defines the tone, voice, and terminology AI applies when it generates knowledge articles. Assign the style guide to a knowledge base so that authors can select it during article generation.

## Before you begin

Role required: knowledge admin

## About this task

A style guide contains the rules for language, tone, voice, and terminology that Now Assist follows when it generates a knowledge article. Each style guide is a separate record that you assign at the knowledge base level, in the same way as article templates.

When an author submits a prompt with a style guide selected, the style guide body is sent as part of the prompt to the Large Language Model \(LLM\). A style guide doesn't define the structure of an article. The article template controls structure.

## Procedure

1.  Navigate to **Lists** &gt; **Administration** &gt; **Style Guides**.

    The list of style guides on the instance appears.

2.  Select **New**.

3.  On the Style Guide form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the style guide. Authors see this name in the style guide list when they generate an article.|
    |Short description|Brief description of the purpose of the style guide.|
    |Style guide body|Plain-text instructions for the language, tone, voice, and terminology to use in generated articles. You can enter the text directly or paste it from another document.|
    |Active|Option that makes the style guide available for assignment to a knowledge base. Clear this option for a style guide that is in progress or retired.|

    **Note:**

    The **Style guide body** field accepts plain text only, because its content is sent to the LLM as part of the prompt.

    For example, the style guide body might include an instruction such as `Don't use the term users. Refer to them as employees.`

4.  Select **Save**.

    The style guide appears in the list of style guides.


