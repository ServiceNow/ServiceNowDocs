---
title: Brand and personalize an assistant
description: Decide how your Now Assist in Virtual Agent assistant should look by using the default branding or by creating a branding.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/conversational-interfaces/now-assist-in-virtual-agent/brand-assistant.html
release: zurich
product: Now Assist in Virtual Agent
classification: now-assist-in-virtual-agent
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Create a chat assistant, View assistants, Configuring assistants overview, Now Assist in Virtual Agent, Conversational Interfaces]
---

# Brand and personalize an assistant

Decide how your Now Assist in Virtual Agent assistant should look by using the default branding or by creating a branding.

## Before you begin

See [Display your chat assistant on a portal, channel, or mobile app](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/now-assist-in-virtual-agent/display-assistant-portal-channel.md) for Now Assist in Virtual Agent assistants.

See [Display your assistant on Platform or ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/now-assist-in-virtual-agent/display-nap-assistant.md) for Now Assist panel assistants.

Role required: virtual\_agent\_admin or admin

## About this task

If you haven’t selected a display experience, branding options aren’t shown.

-   For Now Assist in Virtual Agent, branding is available for standard chat, enhanced chat, and premium chat.
-   For Now Assist panel - Platform assistant, branding is available for premium chat but does not include chat menu items.
-   For the default Employee Slate assistant, branding is available for premium chat.
-   Branding is not available for Now Assist panel - Developer assistant.

**Note:** For Now Assist panel – Platform assistant, branding is available for premium chat. Branding is not available for Now Assist panel – Developer assistant.

## Procedure

1.  In the **Branding** section, select a default branding or an existing customized branding.

    **Note:** To create and edit additional settings, select the **Conversational interfaces console** link. For more information, see [Set up your Virtual Agent bot's branding](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/ac-configure-chat-branding.md).

    If your display experience only has standard chat, the **Standard chat** section and branding preview are shown.

    \[Omitted image "NAinVA-branding-122025.png"\] Alt text: Preview pane of a standard chat assistant.

    If your display experience only has enhanced chat, both **Standard chat** and **Enhanced chat** sections are shown.

    \[Omitted image "NAinVA-branding-0426.png"\] Alt text: Enhanced chat section.

    The chat header logo is shared between standard and enhanced chat, and it's determined by the selected standard chat branding profile. You can't configure a separate chat header logo for each experience. Updating the chat header logo in one experience updates it for the other.

    Learn more about customizing the look-and-feel of enhanced chat by navigating to [Theming for Now Assist in Virtual Agent enhanced chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/now-assist-in-virtual-agent/theming-na-full-page-experience.md).

    If your display experience has premium chat, the **Premium chat** section is shown.

    \[Omitted image "NAinVA-premium-branding-052026.png"\] Alt text: Choose a chat header, chat logo, and chat menu items for premium chat.

    1.  Choose your chat header and update the chat logo. The default chat header name is the name of the assistant. The size of the chat logo should be 144 x 144 pixels. Image file types include: .jpg, .png, .bmp, .gif, .jpeg, .ico, and .svg.
    2.  Add chat menu items to Now Assist in Virtual Agent assistant or the default Employee Slate assistant. Chat menu items aren't available for Now Assist panel - Platform assistant.

        By default, chat, phone, and email are listed. Select the ellipsis to edit or remove a chat menu item. Select **Add chat menu item** to add other items.

        -   Type: Select the menu item type from the drop-down menu. Options include email, link, chat, text, phone, and icon.
        -   Label: A text box type in a label, such as Contact Live Agent, Call Support, etc.
        -   Value: A value field that is dependent on the menu item type.
        -   Icon: Accepted file format for the chat menu icon is .svg only. Suggested size is 40 pixels x 40 pixels.
        \[Omitted image "NAinVA-premium-branding-chat-menu-052026.png"\] Alt text: Chat menu item fields to be filled out.

        Enter a valid phone number. Accepted formats include digits, spaces, hyphens, parentheses, and a leading + for a country code. Enter a valid email address. Example format: `name@domain.com`

    3.  Select **Save**.

        A warning will display if a mandatory field is left empty, or the value format is incorrect.

    4.  To reorder the menu items, drag the rows into your preferred order in the table.
    For branding Microsoft Teams or Slack channels, refer to the documentation.

    A **Channels** section is shown for Now Assist in Virtual Agent assistants and the default Employee Slate assistant if a channel is configured in the display experience.

    -   [Configure branding for your ServiceNow Virtual Agent bot in Microsoft Teams](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/virtual-agent/configure-msteams-branding.md)
    -   [Configure branding for your Virtual Agent bot in Slack](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/virtual-agent/slack-branding-overview.md)
    **Note:** Branding selections must happen in the channel, and not in the platform.

2.  In the **Personalization** section, customize the assistant's tone, response length, and personal details.

    **Note:** The **Personalization** section is viewable when the **sn\_nowassist\_va.assistant\_personalization** system property is active. For more information, see [Now Assist in Virtual Agent system properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/now-assist-in-virtual-agent/nava-sys-props.md).

    \[Omitted image "NAinVA-personalization-062026.png"\] Alt text: Select your assistant's tone, response length, and persona.

    Each assistant can have its own tone, response length, and persona.

    1.  Select a tone for your assistant.
        -   **Direct \(default\)**: Responses feel fact-based and are straightforward.
        -   **Empathetic, clear**: Responses feel warm, genuinely helpful, and approachable.
        -   **Professional, informative**: Responses feel thoughtful, informative, and easy to follow.
    2.  Choose a response length for your assistant.

        -   **Succinct \(default\)**: Focused answers that are as succinct as possible.
        -   **Balanced**: Focused answers with added practical guidance.
        -   **Detailed**: Comprehensive, in-depth answers with full context.
        Responses prioritize clarity and completeness, using the selected response length as a guide. Results may vary based on the complexity of the user query.

    3.  Add persona details to your assistant.
        -   Assistant nickname \(160 character limit\): If this assistant persona is referenced in text, voice, or chat conversations, it will go by this name. For example, if a user asks this assistant its name, it might say “Hi I’m Henry, your HR assistant.”
        -   What subject matter does this assistant specialize in? \(200 character limit\): If this assistant persona is asked what it can do, it might say “I can help with any tasks or questions related to HR or employee relations.”
    **Note:** The preview pane changes depending on the tone and length selected. It is used for illustrative purposes only and doesn’t reflect the actual conversation that the LLM would generate.

3.  Select **Save and continue**.


## What to do next

See [Enable additional chat features](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/now-assist-in-virtual-agent/additional-chat-features.md).

