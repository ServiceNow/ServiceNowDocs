---
title: Use case: Configure an event handler with Now Assist
description: Automate event handler configuration without writing manual binding expressions.
locale: en-US
release: australia
product: Now Assist for Creator
classification: now-assist-for-creator
topic_type: concept
last_updated: "2026-05-09"
reading_time_minutes: 3
breadcrumb: [Use case, Use, UI generation, Use generative AI, Now Assist for Creator, Vibe coding and AI app development on the ServiceNow AI Platform, Building applications]
---

# Use case: Configure an event handler with Now Assist

Automate event handler configuration without writing manual binding expressions.

## Scenario

A UI developer is creating a Service Operations Workspace homepage for a service desk team. The homepage features two components: a button that directs agents to a list of open incidents, and a task list that displays open change requests. For the task list, when an agent selects a reference link in any row, the developer wants the associated change request record to open in a new tab, without requiring any additional navigation steps.

## Problem

Without Now Assist, the developer must manually add an Open page or URL handler to the button component and configure both the destination page and the associated table parameter. For the task list, they need to add a second Open page or URL handler to the Reference link clicked event. Additionally, they must write binding expressions to map the event payload fields table and sys\_id to the record page parameters. This process requires familiarity with the names of the payload fields, the binding syntax, and the parameter names expected by the record page, making it a complex configuration task for each handler.

## Solution

With Event handler generation, the developer uses natural language prompts in the Now Assist panel to configure an event handler. Now Assist identifies the correct destination page, selects the appropriate event payload fields, and generates accurate binding expressions. The developer then reviews the preview and accepts the configuration without needing to look up payload field names or manually write any binding expressions.

## Before you begin

Make sure that you install UI generation and that you have the ui\_builder\_admin role. For more information, see [Install UI generation](../task/install-ui-generation.md) and [Grant UI Builder admin role](../task/grant-ui-builder-admin-role.md).

## Configuration steps

Perform the following steps to use the Event handler generation skill:

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.
2.  Open the Service Operations Workspace experience and navigate to the home page.
3.  Select the button component and open the Button clicked event.
4.  Add an Open page or URL handler. In the Now Assist input panel, enter the prompt: `Open simple list page with table from state parameter.`

    **Tip:** When writing prompts for Event handler generation, reference the specific destination page type and the fields you want to map by name. For reference link events, Now Assist displays the available payload fields in the panel — use these field names in your prompt for the most accurate results.

    Now Assist identifies the simple list page, selects it as the destination, and binds the table parameter to the appropriate state parameter.

5.  Review the preview, select **Accept and edit**, and save the handler.
6.  Select the task list component and open the Reference link clicked event.
7.  Add a Open page or URL handler. Now Assist displays the available event payload fields. Enter the prompt: `Open record page in a new tab with fields table and sysid from event payload`.

    Now Assist sets the destination to the record page, binds the table parameter to the payload’s table field, binds sysid to the payload’s sys\_id field, and enables the Open in new tab option.

8.  Review the preview, confirm the bindings are correct, and accept the configuration.

## Outcome

Both event handlers can be configured with natural language prompts. The developer could set them up quickly without looking up payload field names or writing binding expressions manually. During runtime, selecting the button navigates the agent to the incident list, with the table parameter automatically populated from the workspace's state. Additionally, selecting any reference link in the task list opens the corresponding change request record in a new tab, pulling the table name and sys\_id directly from the selected row. The generated configurations are ready for immediate use. The developer retains full control and can edit any field using standard form controls before saving.

**Parent Topic:**[UI Generation use cases](../task/ui-generation-use-cases.md)

**Related topics**  


[Event handler generation](concept-event-handler-generation.md)

[Configure an event handler with Now Assist](../task/configure-an-event-handler-with-now-assist.md)

