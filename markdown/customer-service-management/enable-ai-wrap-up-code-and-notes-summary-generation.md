---
title: Enable Now Assist to generate wrap up code and notes summary
description: Configure Now Assist in your ServiceNow instance to enable the feature to automatically analyze interaction transcripts and recommend wrap up codes and generate notes summaries. This configuration allows agents to use AI-generated suggestions during the wrap up process or manually invoke the skill.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Enable communication channels, Configure, Customer Service Management]
---

# Enable Now Assist to generate wrap up code and notes summary

Configure Now Assist in your ServiceNow instance to enable the feature to automatically analyze interaction transcripts and recommend wrap up codes and generate notes summaries. This configuration allows agents to use AI-generated suggestions during the wrap up process or manually invoke the skill.

## Before you begin

After an Interaction ends or is transferred to a new agent, the interaction may enter a wrap up state. During this state, agents must select a wrap up code and enter notes to document the interaction. Now Assist can analyze the interaction transcript and recommend an appropriate wrap up code based on the conversation and available wrap up code options. The skill also generates a summary of the interaction to populate the notes field. You can configure the system to automatically generate these recommendations when wrap up begins, or you can enable manual generation where agents click a button to invoke the skill when needed. Manual generation gives customers control over token usage by calling the LLM only when requested.

See [Use AI to generate wrap up code and notes summary](../concept/ai-generated-wrap-up-codes-and-notes-summary.md) and [AI interaction wrap-up](../concept/interaction-wrapup-ai-generated.md).

Role required: admin

Review the following dependencies to ensure access to configuration:

-   Now Assist for Customer Service Management plugins are installed and activated
-   The Now Assist for Wrap Up skill is activated in your instance
-   Wrap up codes are present in the Interaction Wrap Up Codes table with detailed description

## Procedure

1.  Verify the Now Assist for **Wrap Up** skill is activated:

    ![Activate the Wrap Up Completion skill](../image/int-wrap-up-completion-skill.jpg)

    1.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Skills**

    2.  In the left panel, navigate to **Customer** &gt; **CSM** to view available Now Assist skills.

    3.  Locate the **Wrap Up Completion** skill and verify it is activated.

        If the skill is not activated, click the **Activate** button on the skill card.

2.  Create wrap up codes with detailed description:

    ![Create Wrap Up Codes with detailed description](../image/int-configure-wrap-up-code-description.jpg)

    1.  Navigate to **All** &gt; **Interaction** &gt; **Wrap up Codes**.

    2.  Create or update wrap up code records with detailed description.

        The skill uses wrap up code description to determine the most appropriate recommendation. Detailed description improves the accuracy for the recommendations.

3.  Configure wrap up codes for your interaction type:

    ![Interaction Wrap Up configuration](../image/int-wrap-up-configuration.jpg)

    1.  Navigate to **All** &gt; **Interaction** &gt; **Wrap Up Configuration** and open the wrap up configuration record for your interaction type.

    2.  In the **Codes** tab, select the **Enable wrap up codes** checkbox.

    3.  Select and add the wrap up codes you want to make available for this configuration.

    4.  In the **Default wrap up code** field, select the code to use if the wrap up timer expires before an agent selects a code.

4.  Enable AI capabilities for wrap up configuration:

    1.  Select the **AI** tab.

    2.  Select the AI capabilities you want to enable:

        -   Select **Enable AI code** to auto-populate wrap up codes: Enables AI-generated wrap up code recommendations.
        -   Select **Enable AI notes** to auto-populate notes: Enables AI-generated notes summaries.
        You can enable one or both options based on your requirements.

    3.  Select Use AI code as default to automatically submit the AI-recommended wrap up code if the wrap up timer expires.

    4.  Click **Update** to save the configuration.

5.  Configure steps to enable the AI-generated method for automatic or manual recommendations:

    1.  Navigate to **All** &gt; **System Properties** &gt; **All Properties** and search for: **sn\_csm\_workspace.auto\_generate\_ai\_wrap\_up**

    2.  Set the value as required.

        Setting the value to true automatically generates AI recommendations when wrap up begins. Setting the value to false displays a **Run Now Assist** button that agents click to generate recommendations.

    3.  Click **Update**.

    Setting the property to false allows agents to manage when the skill is invoked and helps manage token usage.


## Result

When an interaction enters wrap up state, the system creates an **Interaction Wrap Up Segment** record that maps the interaction, transcript, and wrap up configuration. If automatic generation is enabled, the AI recommendations appear immediately in the wrap up fields. If manual generation is enabled, agents select the **Generate Wrap Up** button to generate recommendations.

Agents can accept the AI recommendations or enter their own values. The **Insert AI notes** button allows agents to restore AI-generated notes if they modify the field and want to return to the original suggestion.

**Note:** The system never overwrites agent input when displaying AI recommendations.

