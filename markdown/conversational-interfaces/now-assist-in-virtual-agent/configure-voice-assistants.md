---
title: Create a voice assistant
description: Create an AI voice assistant to enable natural, conversational voice interactions between users and AI voice agents.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/conversational-interfaces/now-assist-in-virtual-agent/configure-voice-assistants.html
release: australia
product: Now Assist in Virtual Agent
classification: now-assist-in-virtual-agent
topic_type: task
last_updated: "2025-04-21"
reading_time_minutes: 13
breadcrumb: [View assistants, Configuring assistants overview, ServiceNow Otto for Virtual Agent, Conversational Interfaces]
---

# Create a voice assistant

Create an AI voice assistant to enable natural, conversational voice interactions between users and AI voice agents.

## Before you begin

Role required: virtual\_agent\_admin or admin

Set up your preferred user identification and authentication methods to allow access to AI voice agents. See [Authentication factors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/authentication-factors.md) for more information.

## About this task

An AI voice assistant enables natural, conversational voice interactions between users and AI voice agents. It uses speech-to-text \(STT\), large language model \(LLM\), and text-to-speech \(TTS\) to understand and respond to callers in real time. You can configure a voice assistant with personalized voice and welcome message, fallback options, and assign AI voice agents with specific AI instructions. The fallback options include live agent transfer and ticket creation, based on the origin of the call.

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Assistant Designer** &gt; **Assistants** and select **Create assistant**.

2.  Select **Voice-only** option in the Create an assistant window and select **Continue**.

    \[Omitted image "ai-voice-assistant-voice-only-option.png"\] Alt text: Voice-only option selected in the Create an assistant dialog, showing voice mode as the channel type for the new assistant.

3.  Add basic details of the assistant.

    \[Omitted image "ai-voice-assistant-basic-details.png"\] Alt text: Basic details form with Name and Assistant instructions fields, and the How to write instructions guidance panel.

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

Assistant instructions

</td><td>

Instructions that tell the assistant how to handle specific situations and topics during a call. These instructions apply to all AI voice agents within the assistant. AI turns your instructions into rules that the assistant follows.

 For example: "You are an HR assistant for ServiceNow. Your job is to help callers with PTO balance, timeoff requests, payroll queries."

</td></tr></tbody>
</table>        Follow these guidelines for writing effective assistant instructions:

        -   Define the role:

            -   State the assistant's role and department, and the topics it should help callers with.
            -   Example: You are a \[role\] for \[company/department\]. Your job is to help callers with \[topic/task\].
        -   Set the voice pacing:

            -   Describe how the assistant should pace its spoken responses.
            -   Example: Speak in short, clear sentences. Pause between key points and avoid long strings of information.
        -   Define conditional scenarios:

            -   Describe how the assistant should respond to specific situations.
            -   Example: If a caller mentions a specific situation, for example, asks about a missing payment, describe what the assistant should do.
    2.  Select **Save and continue**.

        You’re directed to the Voice AI agents page.

4.  Add one or more AI voice agents to the voice assistant by selecting **Add from library** and select **Save and continue**.

    **Note:** Adding AI agents is optional. If no AI agents are added, you can add them later by editing this assistant. The assistant will be inactive. Select **Add from library** to add an existing agent, or select **Create** to create a new one. See  for more information.

5.  Select language and voice persona.

    \[Omitted image "ai-voice-assistant-language-voice-step.png"\] Alt text: Language and voice step showing the Opening message field, primary and secondary language selection, and the Welcome message, Voice persona, Pronunciation dictionary, and Key term dictionary tabs.

    1.  Select the primary language your assistant will use for interacting with callers.

        You can configure a primary language and any number of secondary languages. You can select from the following languages:

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
        -   Polish
        -   Swedish
        -   Norwegian
        -   Australian English
        -   Irish English
        -   Finnish
        -   Czech
        -   Slovakian
        -   Ukrainian
        -   Malay
        -   Canadian English
        See [Multilingual support for voice assistants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/now-assist-in-virtual-agent/multi-lingual-support-for-voice-assistants.md) for more information.

    2.  Enter an **Opening message** for callers to hear when the call starts.

        The opening message always plays first, before any language selection. If you configure only one language, end the opening message with an intent question, for example, "Thank you for calling. How may I help you today?" because it's the only greeting callers hear. If you configure secondary languages, keep the opening message general instead, for example, "Thank you for calling. This call may be recorded for quality purposes."

    3.  On the **Welcome message** tab, add the message that plays immediately after the caller selects a language.

        This tab only applies if you configure at least one secondary language. With a single language, no language selection occurs, and no welcome message plays. After secondary languages are configured, add a separate welcome message for each language. End each welcome message with an intent question, for example, "How may I help you today?"

    4.  In the **Language input selections** section, select how callers can choose a language during the call.

        \[Omitted image "image.ai-voice-assistant-language-input-selections"\] Alt text: Language input selections section showing the DTMF option selected with a Recommended label, and the Voice option alongside it, with the Advanced settings hyperlink below the section description.

        Select **DTMF** \(dual-tone multi-frequency\) to allow callers to press a keypad number to select a language. Select **Voice** to allow callers to speak a language name. DTMF is the recommended option. You can only enable one option.

        This section is available only when secondary languages are added. For additional settings such as defining retry and goodbye messages, select the **Advanced settings** hyperlink in this section.

    5.  On the **Voice persona** tab, select a voice persona that best suits the conversational experience that you want to deliver through the voice assistant.

        \[Omitted image "ai-voice-assistant-voice-personality.png"\] Alt text: Voice persona tab showing voice persona options with audio preview controls.

        Preview the voice samples to determine the appropriate voice and tone. All AI voice agents connected to the voice assistants share the same voice.

    6.  Select **+ Add language** to add secondary languages.

        For each secondary language, select the corresponding voice persona on the **Voice persona** tab and add a welcome message on the **Welcome message** tab. When secondary languages are configured, callers are presented with a language selection prompt at the start of the call. The order of secondary languages determines the sequence in which options are presented to the caller during language selection.

    7.  On the **Pronunciation dictionary** tab, add custom pronunciations for domain-specific or company-specific terms.

        \[Omitted image "ai-voice-assistant-pronunciation-dictionary.png"\] Alt text: Pronunciation dictionary tab showing dictionary entries with Word and Phoneme columns, and an Add phoneme button.

        Select **Add phoneme** and provide the word or phrase and its pronunciation in either phonetic spelling or phoneme format. Pronunciation entries are specific to the selected language and are applied during voice interactions.

    8.  On the **Key term dictionary** tab, select **Add key term** and add a term that the STT engine might misinterpret, to help it transcribe more accurately.

        \[Omitted image "ai-voice-assistant-key-term-dictionary.png"\] Alt text: Key term dictionary tab showing key term entries that map misheard terms to their correct term, and the Add key term button.

        Key terms improve STT accuracy for domain-specific vocabulary, such as product names or acronyms that the STT engine might otherwise mishear as a similar-sounding common word or phrase.

        Results can vary based on audio quality, caller accent, and context.

        Key term entries are specific to the selected language. You can add up to 30 key terms for each language.

        **Note:** The key term dictionary is separate from the **Pronunciation dictionary**. Key terms improve STT recognition accuracy; pronunciation entries control TTS playback.

    9.  Select **Save and continue**.

        You’re directed to the Communication channels page.

6.  Set up communication channels for the user to interact with the assistant.

    Select a **Provider application** to deploy this voice assistant to. This field is required for all communication channel types.

    Configure at least one communication channel to activate the voice assistant.

    \[Omitted image "ai-voice-assistant-telephony-provider.png"\] Alt text: Communication channels step with Telephony provider tab selected, showing SIP channel type, Genesys provider, Transfer number, Transfer method, SIP Trunk information, and x-snc-param fields.

    1.  Select the **Telephony provider** tab to connect the voice assistant to a phone network.

        Select a communication channel type from the **Communication channel** dropdown, then select a CCaaS provider and configure the required fields. For more information, see [Integrating voice assistant with CCaaS provider](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/integrating-voice-service-with-ccaas-providers.md).

    2.  Select the **Web Real-Time Communication \(WebRTC\)** tab to connect the voice assistant to mobile, web, and external applications.

        Select **Mobile applications** to configure ServiceNow applications such as chat launcher functions, voice launcher functions, and prominent action button overrides. You can also configure external applications. For more information, see [Integrate voice assistant with mobile app voice launcher](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/integrate-voice-assistant-with-mobile-app-voice-launcher.md).

        Select **Web applications** to configure the voice call widget on your ServiceNow Portal or Engagement Messenger. For more information, see .

    3.  Select **Save and continue**.

        You're directed to the Caller verification page.

7.  Identify and authenticate the caller.

    Authentication settings apply only to telephony provider communication channel. If you have selected only mobile communication channel, skip this step.

    \[Omitted image "ai-voice-assistant-authentication.png"\] Alt text: Caller identification and authentication method selection, showing identification method cards, first and second authentication factor cards, and advanced options.

    Ensure the identification and authentication factors are configured at the platform level before you select them here. For more information, see [Authentication factors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/authentication-factors.md).

    To reload available factors from the platform-level configuration without leaving this page, select **Refresh configuration** at the top of the screen. If you have unsaved changes, a confirmation dialog appears before the refresh proceeds. Use this option when authentication factors or system properties have been updated outside Assistant Designer, as those changes are not reflected automatically.

    1.  Select the method used to identify the caller when the call begins.

        Caller identification determines who the caller is before any authentication occurs. The information provided by the caller is matched with system records to identify the caller. If you select the default phone number question, the system automatically matches the caller’s registered phone number to the incoming caller ID from the telephony provider.

        To change or remove an identification method, select **Remove** on the method card.

    2.  Select the fallback method to identify the caller.

        If the caller can't be uniquely identified through the primary method, the system automatically retries using the fallback method.

    3.  Select the **First factor** and **Second factor** authentication methods to enable caller access to AI voice agents.

        Caller authentication verifies the caller’s identity before allowing access to AI voice agents that require authentication. Select a **First factor** and, when MFA is enabled, a **Second factor**. The option selected as the **First factor** is not available in the **Second factor** dropdown. To change or remove an authentication factor, select **Remove** on the factor card. The first and second factor can each be independently cleared.

<table id="table_auth_factors_qry"><thead><tr><th>

Factor

</th><th>

Description

</th><th>

Input method

</th></tr></thead><tbody><tr><td>

Knowledge-based authentication \(KBA\)

</td><td>

Verifies the caller by asking security questions configured at the platform level. Supports both internal records and external sources. See [Knowledge-based authentication \(Security Questions\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/knowledge-based-authentication.md) for more information.

</td><td>

Voice or DTMF

</td></tr><tr><td>

Okta Verify push notification

</td><td>

Sends a push notification to the caller’s registered Okta Verify app for approval. See [Push notification - Okta Verify](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/push-notification-okta-verify.md) for more information.

</td><td>

Approve on device

</td></tr><tr><td>

SMS verification code

</td><td>

Sends a one-time numeric code via SMS to the caller’s registered phone number. See [SMS One-time passcode \(OTP\) authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/sms-otp-authentication.md) for more information.

</td><td>

Voice or DTMF

</td></tr><tr><td>

Authenticator app time-based One Time Password \(TOTP\)

</td><td>

The caller provides a time-based one-time password generated by an authenticator app. See [Time-based one-time password \(TOTP\) authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/totp-authenticator-apps.md) for more information.

</td><td>

Voice or DTMF

</td></tr><tr><td>

Soft PIN

</td><td>

The caller provides a numeric PIN enrolled through ServiceNow. See [Soft PIN authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/softpin-authentication.md) for more information.

</td><td>

Voice or DTMF

</td></tr><tr><td>

Email one-time password \(OTP\)

</td><td>

Sends a one-time code to the caller’s configured email address. See [Email One-time passwords \(OTP\) authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/email-otp-authentication.md) for more information.

</td><td>

Voice or DTMF

</td></tr></tbody>
</table>    4.  Enable the **Authenticate at the start of the call** option to prompt callers for authentication or identification details before the voice assistant responds to any request.

        When enabled, every caller is prompted to complete authentication or identification at the start of the call, regardless of which AI voice agent handles the interaction.

    5.  In the **Advanced options** section, configure the authentication type and retry attempts.

        -   **Authentication type**: Select **Multi-factor authentication \(MFA\)** to require callers to complete both a first and second factor before the system grants access. MFA is enabled by default. Select **Single factor** to require one verification method only. To enable single factor, set the `glide.voice.authenticate.mfa_mandatory` system property to `false`.
        -   **Retry**: Set the number of authentication attempts callers get before the system routes them to a live agent. The default is 3 attempts.
    6.  Select **Save and continue**.

        If the configuration is incomplete or inconsistent, inline messages appear next to the relevant field.

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
        -   Set the duration of inactivity after which the user is reprompted for a response. If there's still no response, the call is disconnected. You can set up to 300 seconds. The default is 30 seconds.
    3.  Select **Save and continue**.

        You're directed to the Advanced settings page.

9.  Configure advanced settings for the voice assistant.

    Advanced settings let you configure supplementary features for the voice assistant.

    1.  In the **Noise cancellation** section, select the level of background noise cancellation intensity.

        Noise cancellation reduces background noise from the caller's side so the voice agent can better hear them. Select from the following levels:

        -   **Low**: Picks up even the quietest background noises. Use in quiet environments where background sounds such as TV or music may be present.
        -   **Medium** \(default\): Picks up somewhat quiet background noises. Use in environments with moderate background noise, such as public places or areas with normal talking.
        -   **High**: Picks up only the loudest background noises. Use in very noisy environments such as construction sites or areas with loud background speech.
    2.  On the **Language and voice** tab, configure the messages played during language selection.

        |Field|Description|
        |-----|-----------|
        |Retry message|Message played before each replay of the language selection prompt, up to three times.|
        |Goodbye message|Message played after the maximum number of retry attempts is reached without a valid selection.|

    3.  Select **Save and continue**.

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

Test the execution of your AI voice agent by manually calling in the telephony number to see if the AI voice agent functions the way you defined it. Review the transcript and logs for troubleshooting and improving the conversational experience of users. See  for information on the tables containing transcript and logs.

