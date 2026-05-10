---
title: Create a voice assistant
description: Create an AI voice assistant to enable natural, conversational voice interactions between users and AI voice agents.
locale: en-US
release: australia
product: Now Assist in Virtual Agent
classification: now-assist-in-virtual-agent
topic_type: task
last_updated: "2025-04-21"
reading_time_minutes: 7
breadcrumb: [View assistants, Configuring assistants overview, Now Assist in Virtual Agent, Conversational Interfaces]
---

# Create a voice assistant

Create an AI voice assistant to enable natural, conversational voice interactions between users and AI voice agents.

## Before you begin

Role required: virtual\_agent\_admin or admin

Set up your preferred user identification and authentication methods to allow access to AI voice agents. See [Authentication factors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/authentication/authentication-factors.md) for more information.

## About this task

An AI voice assistant enables natural, conversational voice interactions between users and AI voice agents. It uses speech-to-text \(STT\), large language model \(LLM\), and text-to-speech \(TTS\) to understand and respond to callers in real time. You can configure a voice assistant with personalized voice and welcome message, fallback options, and assign AI voice agents with specific AI instructions. The fallback options include live agent transfer and ticket creation, based on the origin of the call.

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Assistant Designer** &gt; **Assistants** and select **Create assistant**.

2.  Select **Voice-only** option in the Create an assistant window and select **Continue**.

    ![image.ai-voice-assistant-voice-only-option]

3.  Add basic details of the assistant.

    ![image.ai-voice-assistant-basic-details]

    1.  On the form, fill in the fields.

<table id="table_mp3_4nj_zcc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the voice assistant. Provide a name according to the business outcome that the voice assistant targets.

 For example: HR Service Desk

</td></tr><tr><td>

Description

</td><td>

Brief summary of the business outcomes that your voice assistant targets.

 Example for the HR Service Desk: HR service desk to help resolve employee requests and inquiries.

</td></tr><tr><td>

Tags

</td><td>

Add tags to track analytics for the voice assistant. For example: HR Business UnitTags do not affect the functionality of the AI voice agent or the end user experience.

</td></tr></tbody>
</table>    2.  Select **Save and continue**.

        You’re directed to the AI Agents page.

4.  Add one or more AI voice agents to the voice assistant by selecting **Add from library** and select **Save and continue**.

    **Note:** Add at least one AI voice agent to the voice assistant. The voice assistant uses the AI voice agents to execute AI instructions. You can select an existing agent or select **Create** to create one. See [Create an AI voice agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/create-a-voice-enabled-ai-agent.md) for more information.

5.  Select a voice personality.

    ![image.ai-voice-assistant-voice-personality]

    1.  Select the language your assistant will use as the default speaking language for interacting with the callers.

        You can select from the following languages

        -   English
        -   German
        -   Spanish
        -   Japanese
        See [Multilingual support for voice assistants](../reference/multi-lingual-support-for-voice-assistants.md) for more information.

    2.  Add a personalized welcome message to greet the callers calling into the voice assistant.

    3.  Select a voice persona that best suits the conversational experience that you want to deliver through the voice assistant.

        Preview the voice samples to determine the appropriate voice and tone. All AI voice agents connected to the voice assistants share the same voice.

    4.  Select **Save and continue**.

        You’re directed to the Authentication page.

6.  Set up communication channels for the user to interact with the assistant.

    You can set up telephony provider, mobile app, or both as communication channels. At least one communication channel needs to be set up to activate the voice assistant.

    1.  Integrate a telephony provider to connect to the voice assistant.

        For more information, see [Integrating voice assistant with CCaaS provider](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/integrating-voice-service-with-ccaas-providers.md).

    2.  Configure your voice assistant to be accessible through mobile app voice launcher function.

        For more information, see [Integrate voice assistant with mobile app voice launcher](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/integrate-voice-assistant-with-mobile-app-voice-launcher.md)

7.  Identify and authenticate the caller.

    Authentication settings apply only to telephony provider communication channel. If you have selected only mobile communication channel, skip this step.

    ![image.ai-voice-assistant-authentication]

    Identification and authentication factors must be configured at the platform level, where you define which tables and columns the system should use for both identification and authentication. After the factors are defined, they appear here as selectable options for your voice agent configuration. For more information, see [Authentication factors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/authentication/authentication-factors.md).

    1.  Select the method used to identify the caller when the call begins.

        Caller identification determines who the caller is before any authentication occurs. The information provided by the caller is matched with system records to identify the caller. If you select phone number as the primary identification method, enable the checkbox to allow the system to automatically match the caller’s phone number to the incoming caller Id received from the telephony system.

    2.  Select the fallback method to identify the caller.

        If the caller can't be uniquely identified through the primary method, the system automatically retries using the fallback method.

    3.  Enable the caller access to AI voice agents by selecting the authentication type and methods used.

        Caller authentication verifies the caller’s identity before allowing access to AI voice agents that require authentication.

        Select from the following authentication types.

        -   Multi-factor authentication \(MFA\) requires callers to successfully complete more than one verification method configured before the system grants access. MFA is required by default.
        -   Single factor authentication requires the user to complete the configured verification method. To enable single factor authentication, you must set the `glide.voice.authenticate.mfa_mandatory` system property to `false`.
        Select from the following authentication methods.

        -   Knowledge-based authentication \(KBA\)
        -   Okta Verify push notification
        -   SMS verification code
        -   Authenticator app time-based One Time Password \(TOTP\)
        -   Soft PIN
        **Note:** KBA authentication, for example, employee security questions, requires you to configure the questions and response fields at platform level and explicitly map them to the voice assistant before they can be selected here. To ensure secure and consistent verification, KBA authentication factor must use numeric data only, for example, date of birth, Social Security Number, or employee Id. Additionally, the source table used must reference the `sys_user` table so that caller identity can be validated reliably across the platform. See [Knowledge-based authentication \(Security Questions\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/authentication/knowledge-based-authentication.md) for more information.

    4.  Select **Save and continue**.

        You’re directed to the Safeguards page.

8.  Set up safeguards to create a secure and seamless experience for users interacting with the assistant.

    ![image.ai-voice-assistant-safeguards]

    1.  Set fallback options to route the call to a live agent or create a ticket.

        When a voice agent cannot complete a user's request, the system determines the appropriate fallback behavior based on the call origin, for example, telephony provider or mobile channel.

        -   Telephony provider requires either connect to live agent or a record producer as fallback option.
        -   Mobile channel requires a record producer as fallback option.
        -   **Connect to live agent** option. When selected, this option redirects the caller to a live agent. You must set up live agent transfer for your telephony provider separately.

            **Note:** You can enable the **Capture details before live agent handoff** option, in which the voice agent prompts the caller to provide details in order to triage the call to the appropriate live agent.

        -   **Generate a ticket with record producer** option. When selected, this option creates a ticket for further tracking.

            **Note:** If you choose to use generating a ticket with record producer as the fallback option, you must keep the fields in the record producer simple and short to optimize the user experience for both the communication channels. For example, a short description, description, and an optional field for the callback number should suffice. You can also enable the **Require authentication** option which ensures only confirmed employees are able to generate tickets.

    2.  Set the time limits for call duration and reprompting users after inactivity.

        -   Set Max call duration to trigger fallback behavior when the call reaches this limit.
        -   Set the duration of inactivity after which the user is reprompted for a response. If there's still no response, the call is disconnected. You can set upto 60 seconds.
9.  Review your voice assistant configuration.

    You can change the configuration later.

    ![image.ai-voice-assistant-review]

10. Select **Save and activate** to complete the configuration steps or review a previous step by selecting **Back**.

    Activating the assistant also activates any inactive AI agents associated with it. The following conditions must be met in order to activate the assistant. If any of these conditions are not met, select **Save and close** to come back to it later.

    -   At least one communication channel is selected \(telephony provider or mobile channel\)
    -   At least one AI agent is associated with the assistant
    -   If a telephony provider is enabled, authentication is set up and fallback is configured to either connect to a live agent or create a record producer.
    -   If a mobile channel is enabled, fallback is configured to create a record producer.

## What to do next

Test the execution of your AI voice agent by manually calling in the telephony number to see if the AI voice agent functions the way you defined it. Review the transcript and logs for troubleshooting and improving the conversational experience of users. See [AI voice agent reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/voice-agent-reference.md) for information on the tables containing transcript and logs.

