---
title: Set up agents for Impact
description: Configure the ServiceNow Auto Panel and assistant settings to enable AI agents in Impact. Completing this setup allows agents such as Success Path, Value Story Builder, and the Health Agent to display in the context panel on Impact pages.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/impact/set-up-agents-for-impact.html
release: brazil
topic_type: task
last_updated: "2026-09-15"
reading_time_minutes: 2
keywords: [agents, ServiceNow Auto Panel, assistant, Premium Chart, agent orchestration]
breadcrumb: [Impact Guided Setup, Configuring Impact, Impact]
---

# Set up agents for Impact

Configure the ServiceNow Auto Panel and assistant settings to enable AI agents in Impact. Completing this setup allows agents such as Success Path, Value Story Builder, and the Health Agent to display in the context panel on Impact pages.

For agents to display in Impact, the admin must complete four configuration steps in sequence. Customers with ProPlus entitlements or NOSIS credits can access agents after this setup is complete.

Complete the following steps to set up agents:

-   Enable ServiceNow Auto Panel
-   Activate the default platform assistant
-   Set the display experience to Premium Chart
-   Enable the agent orchestration property

**Important:** Complete each step in the order listed. Agents will not display correctly if any step is skipped or completed out of sequence.

## Before you begin

Complete the Register your instance category in Impact Guided Setup before beginning this task.

Role required: admin

## Procedure

1.  Enable ServiceNow Auto Panel.

    1.  Navigate to **All** &gt; **AI Admin Hub** &gt; **Experiences**.

        The Experiences page loads.

    2.  Select **Turn on**.

        The ServiceNow Auto Panel is enabled. The button label updates to confirm the panel is active.

2.  Activate the default platform assistant.

    1.  Navigate to **All** &gt; **Conversational Interface** &gt; **Assistant Designer**.

        The Assistant Designer page loads.

    2.  Select the **ServiceNow Auto Panel - Platform Default** assistant.

    3.  Select **Edit**.

    4.  Select **Activate**.

        The assistant status updates. The button label changes from **Activate** to **Deactivate**, confirming the assistant is active.

3.  Set the display experience to Premium Chart.

    1.  In the **ServiceNow Auto Panel - Platform Default** assistant, select **Review Display Experiences**.

    2.  Select the edit icon next to the default display experience.

    3.  Change the chart type from **Enhanced Chart** to **Premium Chart**.

    4.  Select **Save**.

    5.  Select **Save** again on the assistant record to apply the changes.

4.  Enable the agent orchestration property.

    1.  Navigate to **All** &gt; **System Properties**.

    2.  Search for the agent orchestration property.

        **Note:** Confirm the exact property name with your Impact Squad. By default, the value is set to false.

    3.  Set the value to true.

    4.  Select **Save**.

5.  Select **Mark as complete** in the Setup Hub to confirm the configuration is finished.


## What to do next

After completing the Set up agents category, agents are available in the Impact context panel for customers with ProPlus entitlements or NOSIS credits. The following agents are available:

-   Success Path
-   Value Story Builder
-   Health Agent

**Parent Topic:**[Impact Guided Setup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/guided-setup-impact-in-app.md)

