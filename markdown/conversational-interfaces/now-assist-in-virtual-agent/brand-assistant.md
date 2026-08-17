---
title: Brand and personalize an assistant
description: Decide how your ServiceNow Otto for Virtual Agent assistant should look by using the default branding or by creating a branding.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/conversational-interfaces/now-assist-in-virtual-agent/brand-assistant.html
release: australia
product: Now Assist in Virtual Agent
classification: now-assist-in-virtual-agent
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [Create a chat assistant, View assistants, Configuring assistants overview, ServiceNow Otto for Virtual Agent, Conversational Interfaces]
---

# Brand and personalize an assistant

Decide how your ServiceNow Otto for Virtual Agent assistant should look by using the default branding or by creating a branding.

## Before you begin

See [Display your assistant on a portal, channel, or mobile app](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/now-assist-in-virtual-agent/display-assistant-portal-channel.md) for ServiceNow Otto for Virtual Agent assistants.

See [Display your assistant on Platform or ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/now-assist-in-virtual-agent/display-nap-assistant.md) for ServiceNow Otto panel assistants.

Role required: virtual\_agent\_admin or admin

## About this task

If you haven’t selected a display experience, branding options aren’t shown.

-   For ServiceNow Otto for Virtual Agent, branding is available for standard chat, enhanced chat, and premium chat.
-   For ServiceNow Otto panel - Platform assistant, branding is available for premium chat but does not include chat menu items.
-   For the default Employee Slate assistant, branding is available for premium chat.
-   Branding is not available for ServiceNow Otto panel - Developer assistant.

## Procedure

1.  In the **Branding** section, select a default branding or an existing customized branding.

    **Note:** To create and edit additional settings, select the **Conversational interfaces console** link. For more information, see [Set up your Virtual Agent bot's branding](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/ac-configure-chat-branding.md).

    If your display experience has standard or enhanced chat, the **Standard chat and enhanced chat** section is shown. The branding preview is for illustration purposes only.

    \[Omitted image "sno-branding-0826.png"\] Alt text: Preview pane of a standard chat assistant.

    Standard and enhanced chat use the same branding profile configuration. Your selection is reflected on your branding settings. For the same assistant, standard and enhanced chat share the same chat header, logo, and menu items. These elements are connected by default.

    The shared chat header logo is determined by the selected standard chat branding profile. You can't configure a separate chat header logo for each experience. Updating the chat header logo in one experience updates it for the other.

    To create and edit additional brand settings, navigate to **Conversational Interfaces** &gt; **Settings** &gt; **Branding**.

    Learn more about customizing the look-and-feel of enhanced chat by navigating to [Theming for Now Assist in Virtual Agent enhanced chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/now-assist-in-virtual-agent/theming-na-full-page-experience.md).

    If your display experience has premium chat, the **Premium chat** section is shown.

    \[Omitted image "sno-branding-premium-0826.png"\] Alt text: Choose a chat header, chat logo, and chat menu items for premium chat.

    1.  Choose your chat header and update the chat logo. The default chat header name is the name of the assistant. The size of the chat logo should be 144 x 144 pixels. Image file types include: .jpg, .png, .bmp, .gif, .jpeg, .ico, and .svg.
    2.  Add chat menu items to ServiceNow Otto for Virtual Agent assistant or the default Employee Slate assistant.

        **Note:** Chat menu items aren't available for ServiceNow Otto panel - Platform assistant.

        By default, chat, phone, and email are listed. Select the ellipsis to edit or remove a chat menu item.

        When editing the chat \(live agent\) option, you can select the check box so that users can see the estimated wait time for the next live agent.

        \[Omitted image "sno-estimated-wait-time-0826.png"\] Alt text: Check box that allows users to see estimated wait time for the next live agent.

    3.  To add other items, select **Add chat menu item**.

        -   Phone: Enter a valid phone number. Accepted formats include digits, spaces, hyphens, parentheses, and a leading + for the country code.
        -   Email: Enter a valid email address. Example format: name@domain.com
        -   Link
        -   Text
        -   Chat: Only one chat type menu item is allowed per assistant.
        For each chat menu item type that you add, fill out the label and value fields. Decide whether you want to use the default icon or select a custom icon. Accepted file format for the icon is .svg only. Suggested size is 40 pixels x 40 pixels.

        \[Omitted image "sno-chat-menu-0826.png"\] Alt text: Chat menu item fields to be filled out.

        Enter a valid phone number. Accepted formats include digits, spaces, hyphens, parentheses, and a leading + for a country code. Enter a valid email address. Example format: `name@domain.com`

    4.  Select **Add**.

        A warning will display if a mandatory field is left empty, or the value format is incorrect.

    5.  To reorder the menu items, drag the rows into your preferred order in the table.
    For branding Microsoft Teams or Slack channels, refer to the documentation.

    A **Channels** section is shown for ServiceNow Otto for Virtual Agent assistants and the default Employee Slate assistant if a channel is configured in the display experience.

    -   [Configure branding for your ServiceNow Virtual Agent bot in Microsoft Teams](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/virtual-agent/configure-msteams-branding.md)
    -   [Configure branding for your Virtual Agent bot in Slack](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/virtual-agent/slack-branding-overview.md)
    **Note:** Branding selections must happen in the channel, and not in the platform.

2.  In the **Personalization** section, customize the assistant's tone, response length, and personal details.

    **Note:** The **Personalization** section is viewable by default. To hide personalization or its different settings, use the **sn\_nowassist\_va.assistant\_personalization** system property. For more information, see [ServiceNow Otto for Virtual Agent system properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/now-assist-in-virtual-agent/nava-sys-props.md).

    \[Omitted image "sno-personalization-tone-0826.png"\] Alt text: Select your assistant's tone, response length, and persona.

    Each assistant can have its own tone, response length, and persona.

    1.  Select a tone for your assistant.
        -   **Direct \(default\)**: Responses feel fact-based and are straightforward.
        -   **Empathetic, clear**: Responses feel warm, genuinely helpful, and approachable.
        -   **Professional, informative**: Responses feel thoughtful, informative, and easy to follow.
    2.  Choose a response length for your assistant.

        \[Omitted image "sno-personalization-response-0826.png"\] Alt text: Select a response length for your assistant.

        -   **Succinct \(default\)**: Focused answers that are as succinct as possible.
        -   **Balanced**: Focused answers with added practical guidance.
        -   **Detailed**: Comprehensive, in-depth answers with full context.
        Responses prioritize clarity and completeness, using the selected response length as a guide. Results may vary based on the complexity of the user query.

    3.  Add persona details to your assistant.

        \[Omitted image "sno-personalization-persona-0826.png"\] Alt text: Add persona details.

        -   Assistant nickname \(160 character limit\): If this assistant persona is referenced in text, voice, or chat conversations, it will go by this name. For example, if a user asks this assistant its name, it might say “Hi I’m Henry, your HR assistant.”
        -   What subject matter does this assistant specialize in? \(200 character limit\): If this assistant persona is asked what it can do, it might say “I can help with any tasks or questions related to HR or employee relations.”
    **Note:** The preview pane changes depending on the tone and length selected. It is used for illustrative purposes only and doesn’t reflect the actual conversation that the LLM would generate.

3.  Select **Save and continue**.


## What to do next

See [Enable additional chat features](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/now-assist-in-virtual-agent/additional-chat-features.md).

