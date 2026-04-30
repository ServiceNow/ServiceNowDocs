---
title: Create a voice assistant
description: Create an AI voice assistant to enable natural, conversational voice interactions between users and AI voice agents.
locale: en-US
release: yokohama
product: Now Assist in Virtual Agent
classification: now-assist-in-virtual-agent
topic_type: task
last_updated: "2025-04-21"
reading_time_minutes: 5
breadcrumb: [View assistants, Configuring assistants overview, Now Assist in Virtual Agent, Conversational Interfaces]
---

# Create a voice assistant

Create an AI voice assistant to enable natural, conversational voice interactions between users and AI voice agents.

## Before you begin

Role required: virtual\_agent\_admin or admin

Set up your preferred user identification and authentication methods to allow access to AI voice agents. See [Authentication factors](https://www.servicenow.com/docs/access?context=authentication-factors&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US) for more information.

## About this task

An AI voice assistant enables natural, conversational voice interactions between users and AI voice agents. It uses speech-to-text \(STT\), large language model \(LLM\), and text-to-speech \(TTS\) to understand and respond to callers in real time. You can configure a voice assistant with personalized voice and welcome message, fallback options, and assign AI voice agents with specific AI instructions. The fallback options include live agent transfer and ticket creation.

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Assistant Designer** &gt; **Assistants** and select **Create assistant**.

2.  Select **Voice-only** option in the Create an assistant window and select **Continue**.

    ![Voice-only option for creating voice assistant](../image/ai-voice-assistant-voice-only-option.png "Voice-only option in Create assistant")

3.  Add basic details of the assistant.

    ![Basic details form for creating voice assistant](../image/ai-voice-assistant-basic-details.png "Basic details form")

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

    **Note:** The voice assistant uses the AI voice agents to execute AI instructions. You can also create an AI voice agent on the fly by selecting **Create**. See [Create an AI voice agent](https://www.servicenow.com/docs/access?context=create-a-voice-enabled-ai-agent&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US) for more information.

5.  Choose a voice personality.

    ![Voice personality selection for creating voice assistant](../image/ai-voice-assistant-voice-personality.png "Voice personality selection")

    1.  Select the language your assistant will use as the default speaking language for interacting with the callers.

        You can select from the following languages

        -   English
        -   German
        -   Spanish
    2.  Add a personalized welcome message to greet the callers calling into the voice assistant.

    3.  Select a voice persona that best suits the conversational experience that you want to deliver through the voice assistant.

        Preview the voice samples to determine the appropriate voice and tone. All AI voice agents connected to the voice assistants share the same voice.

    4.  Select **Save and continue**.

        You’re directed to the Authentication page.

6.  Identify and authenticate the caller.

    ![Authentication method selection for creating voice assistant](../image/ai-voice-assistant-authentication.png "Authentication method selection")

    Identification and authentication factors must be configured at the platform level, where you define which tables and columns the system should use for both identification and authentication. After the factors are defined, they appear here as selectable options for your voice agent configuration. For more information, see [Authentication factors](https://www.servicenow.com/docs/access?context=authentication-factors&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

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
        **Note:** KBA authentication, for example, employee security questions, requires you to configure the questions and response fields at platform level and explicitly map them to the voice assistant before they can be selected here. To ensure secure and consistent verification, KBA authentication factor must use numeric data only, for example, date of birth, Social Security Number, or employee Id. Additionally, the source table used must reference the `sys_user` table so that caller identity can be validated reliably across the platform. See [Knowledge-based authentication \(Security Questions\)](https://www.servicenow.com/docs/access?context=knowledge-based-authentication&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US) for more information.

    4.  Select **Save and continue**.

        You’re directed to the Safeguards page.

7.  Set up safeguards to create a secure and seamless experience for users interacting with the assistant.

    ![Safeguards selection for creating voice assistants](../image/ai-voice-assistant-safeguards.png "Safeguards selection")

    1.  Set fallback options to route the call to a live agent or create a ticket.

        -   **Connect to live agent** option. When selected, this option redirects the caller to a live agent. You must set up live agent transfer for your Contact Center as a Service \(CCaaS\) provider separately.

            **Note:** You can enable the **Capture details before live agent handoff** option, in which the voice agent prompts the caller to provide details in order to triage the call to the appropriate live agent.

        -   **Generate a ticket with record producer** option. When selected, this option creates a ticket for further tracking.

            **Note:** If you choose to use generating a ticket with record producer as the fallback option, you must keep the fields in the record producer simple and short to optimize the user experience for the phone channel. For example, a short description, description, and an optional field for the callback number should suffice. You can also enable the **Require authentication** option which ensures only confirmed employees are able to generate tickets.

    2.  Set the time limits for call duration and reprompting users after inactivity.

        -   Set Max call duration to trigger fallback behavior when the call reaches this limit.
        -   Set the duration of inactivity after which the user is reprompted for a response. If there's still no response, the call is disconnected. You can set upto 60 seconds.
8.  Integrate a telephony provider to power the voice assistant.

    For more information, see [Integrating voice assistant with CCaaS provider](https://www.servicenow.com/docs/access?context=integrating-voice-service-with-ccaas-providers&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

9.  Review your voice assistant configuration.

    You can change the configuration later.

    ![Review configuration page for voice assistants](../image/ai-voice-assistant-review.png "Review configuration")

10. Select **Save and close** to complete the configuration steps or review a previous step by selecting **Back**.


## What to do next

Test the execution of your AI voice agent by manually calling in the telephony number to see if the AI voice agent functions the way you defined it. Review the transcript and logs for troubleshooting and improving the conversational experience of users. See [AI voice agent reference](https://www.servicenow.com/docs/access?context=voice-agent-reference&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US) for information on the tables containing transcript and logs.

