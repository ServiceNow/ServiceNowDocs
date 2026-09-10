---
title: Set up long-term memory
description: Make AI agents remember your preference or facts from previous interactions and use memories for more focused conversations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/long-term-memory-aia-new.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [AI Agent Studio settings, Configure AI Agent Studio, AI Agent Studio, Enable AI experiences]
---

# Set up long-term memory

Make AI agents remember your preference or facts from previous interactions and use memories for more focused conversations.

## Before you begin

Role required: sn\_aia.admin

## Procedure

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Settings** &gt; **Long-term memory**.

    **Note:** Expand the Long-term memory section to see the user facts and preferences.

2.  Configure the User facts and preferences.

<table><thead><tr><th>

Preferences

</th><th>

Value

</th></tr></thead><tbody><tr><td>

**Allow all AI agents to retain user information**

</td><td>

The default value is **Allow**.**Note:** Selecting **Do not allow** disables the rest of the preferences for the Long-term memory configuration.

</td></tr><tr><td>

**Allow all AI agents to apply their knowledge in conversations**

</td><td>

The default value is **Allow**. You can select **Do not allow**, if you don't want to allow the AI agents to apply their knowledge in conversations.

</td></tr><tr><td>

**Allow an LLM to identify categories of memories**

</td><td>

The default value is **Allow**. You can select **Do not allow** if you don't want to allow an LLM to identify the memory categories.

</td></tr></tbody>
</table>3.  To view the existing AI Agent memory categories, select **View**.

    For more information about creating long-term memory categories, see [Create long-term memory category](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/create-ltm-category-new.md).

4.  To view the AI agent category mappings select **View**.

    For more information about creating a category mapping, see . For more information about mapping a category to an AI agent, see [Map Long-term memory category](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/map-ltm-aia-new.md).

5.  Configure Past executions outcomes by turning on the **Allow all AI agents to learn from last executions** using the toggle button.


