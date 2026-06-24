---
title: Create an AI voice assistant
description: Create an AI voice assistant to enable natural, conversational voice interactions between users and AI voice agents.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/create-an-ai-voice-service.html
release: zurich
topic_type: task
last_updated: "2026-06-08"
reading_time_minutes: 11
breadcrumb: [Deploy AI voice agents, Now Assist AI agents, Enable AI experiences]
---

# Create an AI voice assistant

Create an AI voice assistant to enable natural, conversational voice interactions between users and AI voice agents.

## Before you begin

Role required: virtual\_agent\_admin or admin

Set up your preferred user identification and authentication methods to allow access to AI voice agents. See [Authentication factors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-security/authentication/authentication-factors.md) for more information.

## About this task

An AI voice assistant enables natural, conversational voice interactions between users and AI voice agents. It uses speech-to-text \(STT\), large language model \(LLM\), and text-to-speech \(TTS\) to understand and respond to callers in real time. You can configure a voice assistant with personalized voice and welcome message, fallback options, and assign AI voice agents with specific AI instructions. The fallback options include live agent transfer and ticket creation, based on the origin of the call.

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Assistant Designer** &gt; **Assistants** and select **Create assistant**.

2.  Select **Voice-only** option in the Create an assistant window and select **Continue**.

    \[Omitted image "ai-voice-assistant-voice-only-option.png"\] Alt text: Voice-only option selected in the Create an assistant dialog, showing voice mode as the channel type for the new assistant.

3.  Add basic details of the assistant.

    \[Omitted image "ai-voice-assistant-basic-details.png"\] Alt text: Basic details form with Name, Description, and Tags fields for configuring the voice assistant identity and analytics tracking.

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

Add tags to track analytics for the voice assistant. For example, HR.Adding or removing tags will apply the changes immediately. These will be tracked in analytics.

</td></tr></tbody>
</table>    2.  Select **Save and continue**.

        You’re directed to the AI agents page.

4.  Add one or more AI voice agents to the voice assistant by selecting **Add from library** and select **Save and continue**.

    **Note:** Adding AI agents is optional. If no AI agents are added, you can add them later by editing this assistant. The assistant will be inactive. Select **Add from library** to add an existing agent, or select **Create** to create a new one. See [Create an AI voice agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/create-a-voice-enabled-ai-agent.md) for more information.

5.  Select a voice personality.

    \[Omitted image "ai-voice-assistant-voice-personality.png"\] Alt text: Voice personality step showing primary language selection, welcome message, secondary languages, and voice persona options in a two-panel layout.

    1.  Select the primary language your assistant will use for interacting with callers.

        You can configure a primary language and up to three secondary languages. You can select from the following languages:

        -   English
        -   German
        -   Spanish
        -   Japanese
        -   Korean
        -   Dutch
        -   Brazilian Portuguese
        -   Italian
        -   Mandarin Simplified
        -   French
        -   Canadian French
        -   British English
        -   Mexican Spanish
        -   Thai
        -   Hindi
        -   Danish
        -   Russian
        -   Turkish
        See  for more information.

    2.  Add a personalized welcome message to greet the callers calling into the voice assistant.

    3.  On the **Voice persona** tab, select a voice persona that best suits the conversational experience that you want to deliver through the voice assistant.

        Preview the voice samples to determine the appropriate voice and tone. All AI voice agents connected to the voice assistants share the same voice.

    4.  Select **+ Add language** to add secondary languages.

        For each secondary language, select the corresponding voice persona. The order of secondary languages reflects the caller experience during language selection.

    5.  On the **Pronunciation dictionary** tab, add custom pronunciations for domain-specific or company-specific terms.

        \[Omitted image "ai-voice-assistant-pronunciation-dictionary.png"\] Alt text: Pronunciation dictionary tab showing dictionary entries with Word and Phoneme columns, and an Add entry button.

        Select **Add entry** and provide the word or phrase and its pronunciation in either phonetic spelling or phoneme format. Pronunciation entries are specific to the selected language and are applied during voice interactions.

    6.  Select **Save and continue**.

        You’re directed to the Communication channels page.

6.  Set up communication channels for the user to interact with the assistant.

    Select a **Provider application** to deploy this voice assistant to. This field is required for all communication channel types.

    Configure at least one communication channel to activate the voice assistant.

    \[Omitted image "ai-voice-assistant-telephony-provider.png"\] Alt text: Communication channels step with Telephony provider tab selected, showing SIP channel type, Genesys provider, Transfer number, Transfer method, SIP Trunk information, and x-snc-param fields.

    1.  Select the **Telephony provider** tab to connect the voice assistant to a phone network.

        Select a communication channel type from the **Communication channel** dropdown, then select a CCaaS provider and configure the required fields. For more information, see [Integrating voice assistant with CCaaS provider](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/integrating-voice-service-with-ccaas-providers.md).

    2.  Select the **Web Real-Time Communication \(WebRTC\)** tab to connect the voice assistant to mobile and external applications.

        Select **Mobile applications** to configure ServiceNow applications such as chat launcher functions, voice launcher functions, and prominent action button overrides. You can also configure external applications. For more information, see [Integrate voice assistant with mobile app voice launcher](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/integrate-voice-assistant-with-mobile-app-voice-launcher.md).

    3.  Select **Save and continue**.

        You're directed to the Caller verification page.

7.  Identify and authenticate the caller.

    Authentication settings apply only to telephony provider communication channel. If you have selected only mobile communication channel, skip this step.

    \[Omitted image "ai-voice-assistant-authentication.png"\] Alt text: Caller verification step with Identification methods, Authentication methods with First and Second factor options, and Advanced options section.

    Identification and authentication factors must be configured at the platform level, where you define which tables and columns the system should use for both identification and authentication. After the factors are defined, they appear here as selectable options for your voice agent configuration. For more information, see [Authentication factors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-security/authentication/authentication-factors.md).

    1.  Select the method used to identify the caller when the call begins.

        Caller identification determines who the caller is before any authentication occurs. The information provided by the caller is matched with system records to identify the caller. If you select phone number as the primary identification method, enable the checkbox to allow the system to automatically match the caller’s phone number to the incoming caller Id received from the telephony system.

    2.  Select the fallback method to identify the caller.

        If the caller can't be uniquely identified through the primary method, the system automatically retries using the fallback method.

    3.  Enable caller access to AI voice agents by selecting the authentication type, First factor, and Second factor methods.

        Caller authentication verifies the caller’s identity before allowing access to AI voice agents that require authentication.

        Select from the following authentication types.

        -   Multi-factor authentication \(MFA\) requires callers to successfully complete more than one verification method configured before the system grants access. MFA is required by default.
        -   Single factor authentication requires the user to complete the configured verification method. To enable single factor authentication, you must set the `glide.voice.authenticate.mfa_mandatory` system property to `false`.
        Select from the following **First factor** authentication methods.

        -   Knowledge-based authentication \(KBA\)
        -   Okta Verify push notification
        -   SMS verification code
        -   Authenticator app time-based One Time Password \(TOTP\)
        -   Soft PIN
        -   Email one-time password \(OTP\)
        Select from the following **Second factor** authentication methods.

        Numeric authentication factors such as SMS verification code, Authenticator app time-based One Time Password \(TOTP\), and Soft PIN support voice input. Callers can respond verbally instead of using the keypad. Voice input for each factor can be configured at platform level and scoped per voice service. See [Authentication factors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-security/authentication/authentication-factors.md) for more information.

        **Note:** The option selected as the First factor is not available in the Second factor dropdown. KBA authentication, for example, employee security questions, requires questions to be configured at platform level with the **Channel** field set to **Voice** and the **Type** field set to **Identification**, **Authentication**, or both. Questions configured this way automatically appear in Assistant Designer for selection. Explicit service mapping is not required.

        Base system questions are available out of the box for the voice channel at both the identification and authentication levels and are ready to use without additional configuration.

        For secure and consistent verification, KBA authentication factor must use numeric data only, for example, date of birth, Social Security Number, or employee Id. Additionally, the source table used must reference the `sys_user` table so that caller identity can be validated reliably across the platform. See [Knowledge-based authentication \(Security Questions\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-security/authentication/knowledge-based-authentication.md) for more information.

        KBA now also supports external authentication. The caller's system ID and their spoken response are passed to a verification script, which checks the answer against an external system and returns a true or false result. Optionally, context from earlier responses in the same session can be passed to the script. Configure external authentication scripts at platform level.

        Email OTP authentication requires platform-level configuration before it can be selected here. Configure the email field and source table in the Email OTP configuration screen. By default, the email address is sourced from the sys\_user table. The source table must reference the sys\_user table, and the selected column must be an email field. Email OTP configuration can be scoped to a specific voice service. See [Email One-time passwords \(OTP\) authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-security/authentication/email-otp-authentication.md) for more information.

    4.  Enable the **Authenticate at the start of the call** option to prompt callers for authentication or identification details before the voice assistant responds to any request.

        When enabled, every caller is prompted to complete authentication or identification at the start of the call, regardless of which AI voice agent handles the interaction.

    5.  Select **Save and continue**.

        You’re directed to the Safeguards page.

8.  Set up safeguards to create a secure and seamless experience for users interacting with the assistant.

    \[Omitted image "ai-voice-assistant-safeguards.png"\] Alt text: Safeguards step with Fallback behavior options for telephony and Call constraints showing Max call duration and Inactivity timeout fields.

    1.  Set fallback options to route the call to a live agent or create a ticket.

        When a voice agent cannot complete a user's request, the system determines the appropriate fallback behavior based on the call origin, for example, telephony provider or mobile channel.

        -   Telephony provider requires either connect to live agent or a record producer as fallback option.
        -   Mobile channel requires a record producer as fallback option.
        -   **Connect to live agent** option. When selected, this option redirects the caller to a live agent. You must set up live agent transfer for your telephony provider separately.

            **Note:** You can enable the **Capture details before live agent handoff** option, in which the voice agent prompts the caller to provide details in order to triage the call to the appropriate live agent.

        -   **Generate a ticket with record producer** option. When selected, this option creates a ticket for further tracking.

            **Note:** If you choose to use generating a ticket with record producer as the fallback option, you must keep the fields in the record producer simple and short to optimize the user experience for both the communication channels. For example, a short description, description, and an optional field for the callback number should suffice. You can also enable the **Require authentication** option, which restricts ticket creation to authenticated employees.

    2.  Set the time limits for call duration and reprompting users after inactivity.

        -   Set Max call duration to trigger fallback behavior when the call reaches this limit. You can set up to 10 minutes.
        -   Set the duration of inactivity after which the user is reprompted for a response. If there's still no response, the call is disconnected. You can set up to 300 seconds.
    3.  Select **Save and continue**.

        You're directed to the Advanced settings page.

9.  Configure advanced settings for the voice assistant.

    Advanced settings let you configure supplementary features for the voice assistant.

    1.  In the **Noise cancellation** section, select the level of background noise cancellation intensity.

        Noise cancellation reduces background noise from the caller's side so the voice agent can better hear them. Select from the following levels:

        -   **Low**: Picks up even the quietest background noises. Use in quiet environments where background sounds such as TV or music may be present.
        -   **Medium** \(default\): Picks up somewhat quiet background noises. Use in environments with moderate background noise, such as public places or areas with normal talking.
        -   **High**: Picks up only the loudest background noises. Use in very noisy environments such as construction sites or areas with loud background speech.
    2.  Select **Save and continue**.

        You're directed to the Review page.

10. Review your voice assistant configuration.

    You can change the configuration later.

11. Select **Save and activate** to complete the configuration steps or review a previous step by selecting **Back**.

    Activating the assistant also activates any inactive AI agents associated with it.The following conditions must be met in order to activate the assistant. If any of these conditions are not met, select **Save and close** to return later.

    -   At least one communication channel is selected \(telephony provider or mobile channel\)
    -   At least one AI agent is associated with the assistant
    -   If a telephony provider is enabled, authentication is set up and fallback is configured to either connect to a live agent or create a record producer.
    -   If a mobile channel is enabled, fallback is configured to create a record producer.

## What to do next

Test the execution of your AI voice agent by manually calling in the telephony number to see if the AI voice agent functions the way you defined it. Review the transcript and logs for troubleshooting and improving the conversational experience of users. See [AI voice agent transcript and logs tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/voice-agent-reference.md) for information on the tables containing transcript and logs.

