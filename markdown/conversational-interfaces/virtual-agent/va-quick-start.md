---
title: Quick start for Virtual Agent
description: Using the Conversational Interfaces console, you can quickly add Virtual Agent to a portal, configure branding, personalize the greeting, and begin to use pre-built ITSM Virtual Agent conversations.
locale: en-US
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2024-11-05"
reading_time_minutes: 7
keywords: [Virtual Agent, Conversational Interfaces, Now Assist, quick start]
breadcrumb: [Exploring Virtual Agent, Virtual Agent, Conversational Interfaces]
---

# Quick start for Virtual Agent

Using the Conversational Interfaces console, you can quickly add Virtual Agent to a portal, configure branding, personalize the greeting, and begin to use pre-built ITSM Virtual Agent conversations.

If you have a license for a Now Assist product, you can also quickly deploy Now Assist skills in Virtual Agent in a matter of minutes. For details, see [Configuring Now Assist in Virtual Agent](../../now-assist-in-va/task/configure-now-assist-va.md).

## Before you begin

If you have a license for Virtual Agent, the following sections will help you get started and create conversations for your organization quickly.

If you do not have a license for Virtual Agent, you can try Virtual Agent Lite, which comes preinstalled. For information about getting started with Virtual Agent Lite, see [Quick start for Virtual Agent Lite](../task/quick-start-va-lite.md).

Use the Conversational Interfaces console application to activate and configure Virtual Agent quickly. For more information about the Conversational Interfaces console, see [Conversational Interfaces Console](../../conversational-interfaces/concept/ci-console.md).

## Step 1: Activate Virtual Agent and recommended store plugins

If Virtual Agent has not been activated on your instance, you will need to install it.

![Conversational Interfaces console when Virtual Agent is not installed.](../images/vaqs-home-activate-va.png "Conversational Interfaces console page when Virtual Agent is not installed")

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Home**.
2.  If Virtual Agent is not installed, select **Get Virtual Agent plugin** on the home page.
3.  When prompted, select **Start install**.

    The Applications page opens with Virtual Agent \(com.glide.cs.chatbot\) selected.

    ![Select Install/Update to install the Virtual Agent plugin.](../images/vaqs-install-va-plugin.png "Install the Virtual Agent plugin")

    1.  If you have a Virtual Agent license, select **Install/Update All**.
    2.  In the dialog box, select **Install** to begin.
4.  Under Choose what type of requests you want your bot to support, select **Get ITSM plugin**.

    ![Select Get ITSM plugin to install it from the ServiceNow Store.](../images/vaqs-get-itsm-plugin.png "Install the ITSM Virtual Agent Conversations plugin")

5.  Follow the directions in the ServiceNow Store and select **Opt-in** when prompted.
6.  Repeat steps 3 and 4 to install additional plugins. Otherwise, continue to the next section.

## Step 2: Make Virtual Agent available to users

Add a chat entry to the menu of your web portal. You can add Virtual Agent to additional portals later.

For conversations based on generative AI large language models \(LLMs\), you can quickly set up Now Assist in Virtual Agent and add it to a portal. For information about adding Now Assist in Virtual Agent to a portal, see [Configuring Now Assist in Virtual Agent](../../now-assist-in-va/task/configure-now-assist-va.md).

**Note:** You cannot use both Now Assist in Virtual Agent and Virtual Agent using NLU discovery in the same portal.

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Home**.
2.  Under Add your bot to a portal, select **Add to portal**.

    ![Add your bot to a portal tile on the Conversational Interfaces console page.](../images/vaqs-home-integrate-portal.png "Add your bot to a portal tile on the Conversational Interfaces console page")

3.  Fill in the form for Service Portal Agent Chat Configuration.

    Type a name and unlock the **Portal\(s\)** field to specify one or more portals for your virtual agent. Type a number in the **Order** field to specify where to include Virtual Agent on the menu.

    1.  In the **Name** field, type a name for the configuration.
    2.  Select the **Portal** lock icon to open it.
    3.  Select the search icon, and then select a portal.
    4.  In the **Order** field, type a number to indicate the order that the configurations should run.

        Only one configuration applies per portal. If there are multiple configurations on a portal, the system runs the first configuration found from lowest to highest.

4.  Select **Submit**.

For more detailed information, see [Add your bot to a portal](../../conversational-interfaces/task/ac-configure-bot-portal.md).

## Step 3: Customize the look and feel of Virtual Agent

You can change the way Virtual Agent looks to the end user. You can change the colors, add your company logo, and change the icon that represents your bot.

If you're using Now Assist in Virtual Agent, you can customize the look and feel during the configuration process. For more information, see [Configuring Now Assist in Virtual Agent](../../now-assist-in-va/task/configure-now-assist-va.md).

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Home**.
2.  Under Edit your bot's look and feel, select **Set up branding**.

    ![Edit your bot's look and feel tile on the Conversational Interfaces page.](../images/vaqs-home-brand-bot.png "Edit your bot's look and feel tile on the Conversational Interfaces console page")

    The Branding settings page opens.

3.  Select **New** or the name of an existing branding record.
4.  On the form, fill in the fields.
5.  Select **Save**.
6.  Apply the branding configuration as described in [Set up your Virtual Agent bot's branding](../../conversational-interfaces/task/ac-configure-chat-branding.md).

## Step 4: Get recommended topics

The Topic Recommendations app lets you evaluate the common use cases that Virtual Agent can help resolve or deflect. You can use Topic Recommendations with Virtual Agent topics that use either keyword or NLU topic discovery.

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Home**.
2.  Under Set up Topic Recommendations, select **Get Recommendations**.

    ![Set up topic recommendations.](../../conversational-interfaces/image/ci-home-set-up-tr.png "Set up topic recommendations")

    The Topic Recommendations page opens.

3.  Use the [Quick start for Topic Recommendations](getting-started-topic-recommendations.md) to configure and get topic recommendations based on your company's data.

## Explore further

As you work with Virtual Agent, you can expand its capabilities by implementing other features. For example, you can do the following:

-   [Configure Now Assist in Virtual Agent](../../now-assist-in-va/task/configure-now-assist-va.md)
-   [Set up chat experiences for Virtual Agent users](va-conversation-settings.md)
-   [Create new Virtual Agent topics](../task/create-virtual-agent-topic.md)
-   [Change Virtual Agent and Agent Chat system messages](../../conversational-interfaces/task/ac-change-system-messages.md)
-   [Enable AI Search](va-ai-search.md)
-   [Implement Natural Language Understanding \(NLU\)](advantages-nlu.md)
-   [Use Virtual Agent with a live agent](using-va-agent-chat.md)
-   [Using language detection and dynamic machine translation in Virtual Agent enhanced chat conversations](dynamic-lang-detection-translation-enhanced-chat.md)
-   [Localize Virtual Agent topics](localize-va-topic.md)

