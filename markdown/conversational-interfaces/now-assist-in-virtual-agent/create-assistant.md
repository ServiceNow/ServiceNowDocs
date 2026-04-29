---
title: Create a chat assistant
description: Create a chat assistant on your instance. Add basic details and set your assistant as a primary assistant.
locale: en-US
release: australia
product: Now Assist in Virtual Agent
classification: now-assist-in-virtual-agent
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [View assistants, Configuring assistants overview, Now Assist in Virtual Agent, Conversational Interfaces]
---

# Create a chat assistant

Create a chat assistant on your instance. Add basic details and set your assistant as a primary assistant.

## Before you begin

See [View assistants](view-assistants.md).

When configuring a chat assistant, notes throughout the procedures show where there are variations between the setup for Now Assist in Virtual Agent assistants and the setup for Now Assist panel \(Platform and Developer\) assistants.

Now Assist in Virtual Agent assistants and Now Assist panel - Platform \(default\) assistant can be linked to other assistants.

Additional Now Assist panel assistants can't be created.

Role required: virtual\_agent\_admin or admin

## About this task

Set up basic details for your assistant and set it as a primary assistant. Primary assistants can be linked to secondary assistants. For general information about primary and secondary assistants, see [LLM assistants](../concept/llm-assistants.md).

## Procedure

1.  Provide a name and description for the assistant.

    The name of the assistant in this example is Now Assist in Virtual Agent - TEST. An alert is shown if you attempt to create an assistant with the same name as another assistant.

    **Note:** The **Name** and **Description** fields for Now Assist panel assistants can't be modified.

    ![Provide a name and description for your assistant.](../image/NAinVA-chat-details-122025.png "Add assistant details")

2.  Select the **Set as a primary assistant** check box if you want to make the assistant a primary assistant to which you can add secondary assistants.

    **Note:** The ability to link to another assistant is not available for Now Assist panel - Developer assistant.

3.  Place your cursor within the **Select assistants to link to** field to see a list of available secondary assistants.

    Assistants that already have secondary assistants under them can't be selected. Any assistant that you select becomes a secondary assistant to the assistant that is being set as a primary assistant. The primary assistant will contain a combination of search profiles and assets from the secondary assistants.

    One or more secondary assistants must be selected. All assistants within the same instance and domain are shown in the drop-down list, enabling you to link your primary assistant with one or more secondary assistants. Two primary assistants can’t be linked to each other, and other primary assistants are unavailable in the list.

    If one or more secondary assistants selected are inactive, an alert shows **The following secondary assistants are off and will be inaccessible.** A list of inactive assistants is shown.

4.  Select **Save and continue**.


## What to do next

See [Use agentic support for a chat assistant](use-agentic-support.md).

