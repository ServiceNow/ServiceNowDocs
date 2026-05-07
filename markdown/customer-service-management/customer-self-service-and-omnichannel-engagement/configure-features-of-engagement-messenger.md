---
title: Feature configuration for Engagement Messenger
description: Configure the features of Engagement Messenger so that you can change the default settings to suit your customer needs.
locale: en-US
release: australia
product: Customer Self-service and Omnichannel Engagement
classification: customer-self-service-and-omnichannel-engagement
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Engagement Messenger, Set up self-service, Configure, Customer Service Management]
---

# Feature configuration for Engagement Messenger

Configure the features of Engagement Messenger so that you can change the default settings to suit your customer needs.

## Before you begin

Role required: sn\_csm\_ec.ec\_admin

You must configure Engagement Messenger before configuring its features. For more information, see [Configure Engagement Messenger](create-engagement-messenger-module.md).

## About this task

Configure how the features of Engagement Messenger appear to your customers, their display arrangement, and their behavior.

Use the Features section of the guided configuration to customize the messenger configuration. View a live preview of how the Engagement Messenger would look like in your third-party website. You can also watch the [academy video](https://www.youtube.com/watch?v=uViv-3bcg3k&list=PLkGSnjw5y2U79gjQuQW-2GBqzEccwFkWH&index=20) to understand the overall functionality of Engagement Messenger.

## Procedure

1.  Navigate to **All** &gt; **Engagement Messenger** &gt; **Modules**.

2.  In the Edit module column of the messenger module that you want to configure, select **Edit**.

    The guided configuration view is displayed.

3.  From the Features section of the guided configuration, enable or disable a feature by using the toggle \(![Toggle icon.](../image/toggle-icon.png)\) on the feature card.

4.  Open one of the following features and modify the values:

    -   Greeting: See [Greeting feature configuration](../reference/greeting-feature-configuration-fields.md).
    -   Knowledge: See [Knowledge feature configuration](../reference/knowledge-feature-configuration-fields.md).
    -   Search: See [Search feature configuration](../reference/search-feature-configuration-fields.md).
    -   Case: See [Case management feature configuration](../reference/case-management-feature-configuration-fields.md).
    -   Catalog: See [Catalog feature configuration](../reference/catalog-feature-configuration.md).
    -   Field service: See [Field service feature configuration](../reference/field-service-feature-configuration.md).
    -   Walk-up: See [Walk-up feature configuration](../reference/walk-up-feature-configuration.md).
    -   Chat with an agent: See [Chat feature configuration form fields](../reference/agent-chat-feature-configuration-fields.md).

        **Note:**

        -   The knowledge article, catalog item, and case links sent by an agent can be opened within Engagement Messenger. You can configure how links should be open in a messenger. For more information, see [Create a smart link preference](https://www.servicenow.com/docs/access?context=create-smart-link-preference&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US).
        -   You can also enable the Now Assist in Virtual Agent in Engagement Messenger by [Configuring assistants overview](https://www.servicenow.com/docs/access?context=configure-now-assist-va&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US) and then [Display your assistant](https://www.servicenow.com/docs/access?context=display-assistant-portal-channel&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US) in Engagement Messenger.
    -   Configurable Cards: See [Configurable Cards feature configuration](../reference/configurable-card.md).
    -   Callback: See [Callback feature configuration form](../reference/em-callback.md).
5.  You can also add a feature in the **Features** section using Configurable Cards.

    1.  Select **Add custom feature**.

    2.  Enter the feature name and select the feature type.

    3.  Select **Add**.

    For more information, see [Configurable Cards feature configuration](../reference/configurable-card.md).

6.  Select **Update**.

7.  Change the display order of the features by reordering the feature cards.

    You can see the modified home page layout of your Engagement Messenger in the live preview of the module.

    ![View of the Configure Engagement Messenger form with a list of features like Greeting, Search, Knowledge and so on that can be used for configuration.](../image/em-config-feature.gif "Engagement Messenger features")

    **Note:** Engagement Messenger extends service portal capabilities that don't support domain separation. For more information, see \([Domain separation and Service Portal](https://www.servicenow.com/docs/access?context=domain-separation-service-portal&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US)\). However, other tables that are used in Engagement Messenger may support domain separation according to the configurations with which they're created.


## What to do next

[Create an identity provider \(IdP\) for Engagement Messenger](../concept/create-identity-providers-for-engagement-messenger.md)

