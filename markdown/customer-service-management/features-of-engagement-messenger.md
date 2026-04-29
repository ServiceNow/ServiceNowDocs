---
title: Features of Engagement Messenger
description: Understand what the Engagement Messenger application can provide to your customers.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 11
breadcrumb: [Engagement Messenger, Set up Engagement Messenger, Enable communication channels, Configure, Customer Service Management]
---

# Features of Engagement Messenger

Understand what the Engagement Messenger application can provide to your customers.

After you create and configure the Engagement Messenger module, you can customize it for your customers. For example, you can change the display order of any of these features on the home page of the messenger. Also, you can enable or disable any of these features to suit your customer's needs.

![Engagement messenger application showing all options for a customer to interact with a company. Refer to the following list for all available options.](../image/em-home-page-v3.png "Engagement Messenger features")

-   **Greeting**

    You can display the user greeting, which also includes a greeting message, on the header of the messenger. You can customize the way you want to greet your guest users and the users who sign in to your website.

-   **Knowledge**

    You can select a knowledge base for your search results or choose to display featured articles on the home page of the messenger. You can also add multiple knowledge bases to suit your customer base.

    **Note:** To add knowledge bases to the Engagement Messenger module, you must manually assign the knowledge\_admin role to the Engagement Messenger admin \[sn\_csm\_ec.ec\_admin\] user.

-   **Search**

    The ServiceNow® AI Search capability that is used in the Engagement Messenger application uses the knowledge bases that you selected for your messenger.

    When a customer searches for information using the Search widget on the messenger, the displayed results are from the articles in the knowledge bases that are associated to your messenger module.

    Customers can open the articles from the search results to get the information they need. They can also provide feedback to the article directly from the messenger to indicate whether the article was helpful or not. This feedback helps you to understand which articles are the most helpful so that you can improve those articles that weren’t helpful.

    **Note:**

    -   If the Service Portal - Restricted Pages plugin \(com.glide.service-portal.pages.restricted\) is activated in your ServiceNow instance, AI Search functionality will not work in Engagement Messenger for unauthenticated users.

        If this plugin is not activated, then the AI Search functionality works for both unauthenticated and authenticated users.

    -   You must configure AI Search in your ServiceNow instance and then enable Typeahead Search and AI Search Assist widgets so that the unauthenticated users can use the AI search feature from Engagement Messenger.

        For more information on enabling Typeahead Search and AI Search Assist widgets for Engagement Messenger, see [Enabling AI search in the Customer and Consumer Service Portals for unauthenticated users](../task/configure_search_csp_guestuser.md).

        For more information of AI Search configuration, see [Configuring AI Search](https://www.servicenow.com/docs/access?context=configuring-ais&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

-   **Case management**

    You can manage your customer cases on the messenger. This feature is available only for authenticated users of your website.

    By using the Cases widget on the messenger, your customers can submit a case to request help with something or to report an issue. Submitted cases can be assigned to a customer service agent and tracked to a resolution.

    ![Case management chat windows that customers can see on the customer portal. For the text description, refer to the text that follows.](../image/em-case-flow.png "Case management")

    Whenever your customers return to the customer portal and log in, they are notified of any updates to the cases that they created. They can also view the details of all the cases and requests that they have previously submitted and track their status.

    Some cases would require action from the submitted user, asking them to provide more information about the help they need or to review a solution that the support team has provided. Customers can perform all these actions directly from within the messenger.

-   **Catalogs**

    You can associate pre-defined catalogs with your Engagement Messenger. Customers can browse through the list of available catalog items. From this list of catalog items, they can choose to request a service or create a ticket. The requests that the customer makes can be tracked to a resolution using the case management feature.

    Whenever your customers return to the customer portal and log in, they are notified of any updates to the requests that they have previously submitted.

    ![Catalog view with the Request things you need feature highlighted.](../image/catalog-feature.png "Catalog feature")

-   **Field service management**

    The field service feature enables your customer to request a technician visit to service their issue. By selecting a product or service that they need help with and their location, customers can submit a request for a technician visit. While submitting the request, customers can also add any supporting attachments that they think might help the support team understand the issue before a technician is allotted for the visit.

    All technician requests are stored as work orders in your ServiceNow instance so that they can be tracked to completion.

    The Work Order will have the location where the customer has raised a request. Geo-location services must be enabled for the technicians so that customers can track the live location and know the estimated time of arrival \(ETA\) of their technician. For more information, see [Field service feature configuration](../reference/field-service-feature-configuration.md).

    **Note:**

    -   Verify that the Field Service Management - Customer Experience plugin \(com.snc.fsm\_customer\_experience\) is active in your ServiceNow instance.
    -   The field service feature is available only for users who log in to the Engagement Messenger and not for guest users.
-   **Walk-up appointments**

    The walk-up feature enables your customers to book an appointment to visit one of your stores, service centers, and the like. Customers can view the support centers near them and select one to schedule an appointment to visit. Once an appointment is scheduled, customers receive a confirmation email.

    Customers who log in into your website can view a list of scheduled appointments directly from this widget on the Engagement Messenger home page. They can modify or cancel existing appointments. They also receive notification emails on the following status of their walk-up appointment:

    -   They're ready to be assisted by an associate of the support center
    -   A walk-up interaction is assigned to an associate of the support center
    -   A walk-up interaction is closed
    Customers who don’t log in can use the confirmation email to view and modify their appointments.

    **Note:** To enable a walk-up feature for your customers, verify that you activate the following plugins in your ServiceNow instance:

    -   Walk-up for CSM plugin \(com.snc.walkup\_for\_csm\) for authenticated users
    -   Guest Walk-up Experience for Customer Service plugin \(sn\_guest\_walkup\_cs\) for unauthenticated users
-   **Virtual and live agent chat**

    The chat feature enables support agents to interact with customers to resolve their issue by creating incident or case records or to transfer chats to another agent or queue if needed. Chat feature support is enabled for both authenticated and guest \(unauthenticated\) users.

    -   **Virtual and live agent chat**

        Customers can use the Chat widget on the messenger to interact with a virtual or live customer support agents in your organization. This way, your customers can get immediate responses to their queries or issues.

        ![Chat window showing a customer's dissatisfied response to a field service agent's suggested steps to resolve an issue.](../image/em-chat-live-agent.png "Live agent chat")

        Engagement Messenger also provides contextual chat functionality. From any case details page, your customers can directly start a chat that opens with the context of that specific case.

        **Note:** Chat is available when you activate the Glide Virtual Agent plugin \(com.glide.cs.chatbot\) and set the **com.glide.cs.embed.csp\_frame\_ancestors** system property value to **'self' &lt;your website URL&gt;**.

    -   **Now Assist in Virtual Agent with Engagement Messenger**

        Now Assist in Virtual Agent offers a conversational support experience that improves the chat experience in Engagement Messenger by delivering prompt answers to user questions. When enabled, Now Assist in Virtual Agent provides your users with an interactive generative AI experience. A friendly, natural language conversation that is easier to understand and helps users to be more comfortable with chatting to a bot.

        By integrating generative AI chat capabilities, Now Assist in Virtual Agent enhances the user experience in Engagement Messenger. It improves asynchronous messaging, enabling users to resolve issues more quickly and efficiently. These capabilities help speed up issue resolution and increase efficiency by reducing the number of incoming queries that must be diverted to a live agent. To know more about Now Assist in Virtual Agent, see [Exploring Now Assist in Virtual Agent](https://www.servicenow.com/docs/access?context=exploring-now-assist-va&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US).

        Getting started with Now Assist in Virtual Agent in Engagement Messenger:

        -   To enable Now Assist in Virtual Agent chat support in Engagement Messenger, verify that the Now Assist in Virtual Agent experience is configured by virtual\_agent\_admin or admin. For more information, see [Configuring assistants overview](https://www.servicenow.com/docs/access?context=configure-now-assist-va&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US).
        -   You can create or use an existing assistant by navigating to **All** &gt; **Conversational Interfaces** &gt; **Assistants**. For more information, see [Create a chat assistant](https://www.servicenow.com/docs/access?context=create-assistant&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US).
        -   Once you select an assistant navigate to the **Display experience** tab to configure the Engagement Messenger module. In the **Portals** tab, select the Engagement Messenger module from the **Add portal** list and select the **Standard chat** as the experience. For more information, see [Display your chat assistant on a portal, channel, or mobile app](https://www.servicenow.com/docs/access?context=display-assistant-portal-channel&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US).
        **Note:** Each assistant comes with its own search configuration. For a smooth experience, if the assistant appears on a portal or mobile app that already has AI search configured, consider duplicating that setup to maintain consistency.

        ![Engagement Messenger displaying a conversational interface with Now Assist in Virtual Agent enabled.](../image/nava_in_em.png)

    -   **Asynchronous chat**

        Engagement Messenger supports communication at different time intervals, enabling your support agents and end users to participate in long-running conversations without having to be online at the same time. For more information about asynchronous conversation, see [Asynchronous Chat](https://www.servicenow.com/docs/access?context=async-chat&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US).

        Configure asynchronous chat on Engagement Messenger by setting the web client as a messaging channel. For more information, see [Configure asynchronous chat for the web channel](https://www.servicenow.com/docs/access?context=configure-async-web&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US).

        -   **Message preview**

            -   Enable preview to see previews of unread chat message text, tables, links, HTML content, cases, knowledge cards, and images shared by the support agent without opening a message. The complete HTML content or video, and multiple unread messages, can be seen only when the user accesses the message.
            -   Asynchronous chat supports emojis sent by an agent in the message preview for a more interactive conversation. For more information on how to use emojis in Agent chat, see [Using emojis in Agent Chat](https://www.servicenow.com/docs/access?context=ci-agent-chat-using&version=australia&pubname=australia-conversational-interfaces&section=ac-using-emojis-agent-chat&ft:locale=en-US).
            ![Unread message previews shared by support agents. For the text description, refer to the preceding text in the Message preview section.](../image/async-preview.png "Previews")

        -   **Offline message support**

            Offline chat support enables users to view messages sent by the support agent while they were offline. The chat widget notification shows the total number of unread messages in real-time when the user revisits the website.

            ![Pop-up window displaying the number of messages received when the user was offline.](../image/async-notif.png "Offline message support")

        -   **Chat messages history**

            Users can close and reopen the chat window as needed without losing context or progress so an accidental messenger closure doesn’t reset the chat session.

        **Note:** You can set a specific timeout to manage the idle conversation. By default, if the requester doesn’t respond to an agent message within two days, the conversation status changes to Closed Abandoned and the chat session is ended. As an admin, you can override the conversation idle timeout period for a web channel by setting the value in the Conversation Idle Timeout field in the Messaging Channels \[sys\_cs\_channel\] table. For details, see [Closing Virtual Agent and Live Agent conversations](https://www.servicenow.com/docs/access?context=va-open-conversations&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US).

-   **Configurable Cards**

    The Configurable Cards enables you to add custom features to Engagement Messenger. It enables Engagement Messenger to serve as a one-stop solution for accessing all the information. You can embed portal page, featured links, and data from any table on the messenger using the Configurable Cards.

    -   **Portal page feature card**

        Allows you to embed any portal page or catalog item on Engagement Messenger. The embedded page opens within the messenger when the user selects the feature card.

        ![Portal configuration showing feature cards including a clickable image as a display card, and title and subtitle text as a display card.](../image/em-portal.png "Portal configuration")

    -   **Featured links**

        Enables you to add a list of links to website on Engagement Messenger. The link opens in a new browser tab when accessed using the feature card on messenger's home page.

        ![Featured links shown as Top Links in a display card.](../image/em-links.png "Featured links")

    -   **Data from any table feature card**

        The feature card enables you to embed data from any table on Engagement Messenger. The added records appear as a card with a title or links on a messenger's home page.

        ![Engagement messenger view of open orders and their details, displayed in a table record view or list view when accessed through Card or Links.](../image/em-data-from-table.png "Data from any table")

-   **Proactive updates and reminders**

    Engagement Messenger provides your customers updates and reminders in the following scenarios so that you can keep your customers updated even if they are not accessing the messenger directly.

    -   Reminder for an upcoming walk-up appointment, according to the walk-up feature configuration
    -   Reminder for an upcoming technician visit
    -   Updates on a case
    -   Update on a chat
    According to the configuration of Engagement Messenger behavior, the count of the updates is displayed on the messenger widget on your customer support webpage. If the customer navigates away from your website, the count of updates is also displayed on the browser tab.


To learn how to start configuring Engagement Messenger for your third-party website, see [Set up Engagement Messenger](setting-up-engagement-messenger.md).

**Related topics**  


[Exploring AI Search](https://www.servicenow.com/docs/access?context=explore-ais&version=australia&pubname=australia-platform-administration&ft:locale=en-US)

[Case management for Customer Service Management](csm-case-management.md)

[Virtual Agent](https://www.servicenow.com/docs/access?context=virtual-agent-landing-page&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US)

[Using Walk-up Experience](use-walkup-experiencce.md)

[Knowledge Management](https://www.servicenow.com/docs/access?context=knowledge-management&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US)

[Field Service Management](https://www.servicenow.com/docs/access?context=fsm-application-landing-page&version=australia&pubname=australia-field-service-management&ft:locale=en-US)

