---
title: Configure UI Builder Agent
description: The UI Builder Agent is a Now Assist AI agent that assists low-code developers working in UI Builder by responding to questions, information requests, and page editing instructions.Install Now Assist for Creator, UI Generation, and Conversational Studio from Application Manager before configuring the UI Builder Agent.Follow the UI Builder Agent setup wizard in AI Agent Studio to review and confirm your agent configuration.Enable the Now Assist panel in Now Assist Admin.Activate the AI Search.Add a display experience to the Now Assist Panel- Platform \(default\) assistant, request AI Search activation, and activate the assistant in Assistant Designer.
locale: en-US
release: australia
product: Now Assist for Creator
classification: now-assist-for-creator
topic_type: task
last_updated: "2026-05-08"
reading_time_minutes: 6
breadcrumb: [Configure, UI generation, Use generative AI, Now Assist for Creator, Vibe coding and AI app development on the ServiceNow AI Platform, Building applications]
---

# Configure UI Builder Agent

The UI Builder Agent is a Now Assist AI agent that assists low-code developers working in UI Builder by responding to questions, information requests, and page editing instructions.

## Before you begin

Role required: ui\_builder\_admin

## About this task

Administrators must install the required applications, configure the agent in AI Agent Studio, enable the Now Assist panel, and activate the default Now Assist Panel- Platform assistant before developers can interact with the agent.

## Procedure

1.  [Install required applications for UI Builder Agent](configure-ui-builder-agent.md#)

2.  [Enable UI Builder Agent in AI Agent Studio](configure-ui-builder-agent.md#)

3.  [Enable the Now Assist panel](configure-ui-builder-agent.md#)

4.  [Activate the Now Assist Panel- Platform \(default\) assistant](configure-ui-builder-agent.md#)


**Parent Topic:**[Configuring UI generation](../concept/configuring-ui-generation.md)

## Install required applications for UI Builder Agent

Install Now Assist for Creator, UI Generation, and Conversational Studio from Application Manager before configuring the UI Builder Agent.

### Before you begin

You must have administrator access to Application Manager on your ServiceNow instance.

Role required: ui\_builder\_admin

### About this task

Install and update three applications to support the UI Builder Agent before configuring it in AI Agent Studio.

### Procedure

1.  Navigate to **All** &gt; **Application Manager**.

    Application Manager opens and displays the search interface for licensed applications and plugins.

2.  In the search field, type `now assist for creator` and press Enter.

3.  Select the **Installed** tab and verify that Now Assist for Creator \(`sn_now_creator`\) is listed and shows **Up to date**.

    If the application is not installed, locate it under the **Available for you** tab and install it.

4.  Clear the search field, type `ui generation`, and press Enter.

5.  Select the **Installed** tab and verify that UI Generation \(`sn_ui_generation`\) is installed and shows **Up to date**.

    The UI Generation application must be the Zurich version or later.

6.  Clear the search field, type `Conversational Studio`, and press Enter.

7.  Select the **Installed** tab and verify that Conversational Studio \(`sn_convo_studio`\) is installed and shows **Up to date**.

    If the application is not installed, locate it under the **Available for you** tab and install it.


### Result

All three applications — Now Assist for Creator, UI Generation, and Conversational Studio — are installed and up to date on your instance.

## Enable UI Builder Agent in AI Agent Studio

Follow the UI Builder Agent setup wizard in AI Agent Studio to review and confirm your agent configuration.

### Before you begin

Verify that you have installed all the required applications. See [Install required applications for UI Builder Agent](configure-ui-builder-agent.md#).

Role required: ui\_builder\_admin

### About this task

The UI Builder Agent comes pre-configured with the UI Generation application. The setup wizard in AI Agent Studio guides you through the process of defining the agent, covering aspects such as its specialty, tools, security controls, triggers, and channels.

**Important:** The UI Builder Agent record is read-only in the Global application scope. When viewing the agent in AI Agent Studio, you will see a banner indicating that the record belongs to the UI Generation application. You can proceed through the wizard without switching scope.

### Procedure

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Overview**.

    The AI Agent Studio overview page opens, showing available AI agents and recent agentic workflow activity.

2.  Locate the **UI Builder Agent** card and select it.

    The UI Builder Agent setup wizard opens on the **Define the specialty** step.

3.  Review the agent specialty definition and select **Continue**.

    You don't need to modify the specialty or subsequent configuration steps. The agent comes fully configured.

4.  On the **Add tools and information** step, select **Continue**.

5.  On the **Define user access** step, select **Continue**.

6.  On the **Define data access** step, review the user identity settings and select **Continue**.

    The agent is pre-configured with a **Dynamic user** identity type and the `ui_builder_admin` approved role. The dynamic user setting means the agent derives its data access permissions from the user who initiates the interaction.

7.  On the **Add triggers** step, select **Continue**.

8.  On the **Select channels and status** step, scroll down to **Activation status**, enable **This AI agent is active**, and then select**Test**.

    The system navigates to the Testing tab in AI Agent Studio. An alert banner appears indicating that you must enable the Now Assist panel before testing.


### Result

The UI Builder Agent setup wizard is complete. The agent configuration is confirmed, and you can enable the Now Assist panel to proceed with testing and activation.

## Enable the Now Assist panel

Enable the Now Assist panel in Now Assist Admin.

### Before you begin

Role required: ui\_builder\_admin

### About this task

Enable the panel before testing or using the UI Builder Agent.

### Procedure

1.  On the AI Agent Studio Testing tab alert banner, select the **Edit this setting** link.

    Alternatively, navigate directly to **All** &gt; **Now Assist Admin** &gt; **Experiences**.

    The Now Assist panel page opens in Now Assist Admin, showing a summary of the panel and a **Turn on** button.

2.  In the **Turn on** section, select **Turn on**.

    A success dialog appears confirming that the Now Assist panel is turned on. The dialog shows that generative AI skills in the Now Assist panel are available. It also provides a link to the Assistants page in CI Admin console for further configuration.

3.  In the success dialog, select the **Assistants page in CI Admin console** link.

    The CI Admin Experience Assistants page opens.


### Result

The Now Assist panel is enabled on your instance and is available to users based on their designated permissions.

## Activate AI search

Activate the AI Search.

### Before you begin

Role required: ui\_builder\_admin

### About this task

Activating AI Search turns on Now Assist in Virtual Agent.

### Procedure

1.  Go to **All** &gt; **AI Search** &gt; **AI Search Status**.

2.  Select **Request AI Search**.

    AI Search activation is a background process that takes about 15 minutes to complete. A confirmation page titled **AI Search is requested** appears when the request is submitted successfully.

    A message confirms that the AI Search is activated.


### Result

You can now access AI-powered search capabilities in Virtual Agent.

## Activate the Now Assist Panel- Platform \(default\) assistant

Add a display experience to the Now Assist Panel- Platform \(default\) assistant, request AI Search activation, and activate the assistant in Assistant Designer.

### Before you begin

Role required: ui\_builder\_admin

### About this task

The Now Assist Panel - Platform \(default\) assistant is the main system assistant in the Unified Navigation app shell. To use the UI Builder Agent through the Now Assist panel, you must assign at least one display experience to the assistant and turn it on.

### Procedure

1.  On the CI Admin Experience Assistants page, select **Manage assistants**.

    Assistant Designer opens, showing all available assistants including Now Assist Panel- Developer \(default\), Now Assist in Catalog Builder, and Now Assist Panel- Platform \(default\).

2.  On the Now Assist Panel- Platform \(default\) card, select **Edit**.

    A banner on the assistant overview page shows that the assistant is inactive and requires at least one display experience to be activated.

    The Now Assist Panel- Platform \(default\) assistant opens in Assistant Designer.

3.  Select **Go to display experiences**.

    The **Display experiences** settings page opens.

4.  Select **Add ServiceNow platform** and select **Unified Navigation app shell**.

5.  Select **Add**.

    The Unified Navigation app shell entry appears in the ServiceNow AI Platform® list with the **Enhanced chat** experience type.

6.  Select **Save**.

    A success banner confirms that the Now Assist Panel- Platform \(default\) assistant is saved successfully.

    The **Activate** button is enabled.

7.  Select **Activate**.

    If you haven’t activated AI Search, an alert banner appears indicating that AI Search must be activated to turn on Now Assist in Virtual Agent. To activate AI Search, see [Activate AI search](configure-ui-builder-agent.md#).

    A success banner confirms that the Now Assist Panel- Platform \(default\) assistant is activated.

    The status of Now Assist Panel- Platform \(default\) assistant in Assistant Designer changes from **Inactive** to **Active**.


### Result

The Now Assist Panel- Platform \(default\) assistant is active.

The UI Builder Agent is available to users through the Now Assist panel in UI Builder and across the platform.

