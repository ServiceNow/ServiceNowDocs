---
title: Omnichannels for communicating with customers
description: Meet customers where they feel most comfortable by providing omnichannel support. Customers can use chat on the Customer Service Management portal, chat via consumer messaging apps, use email, or place a phone call.From the Customer Service Portal and Consumer Service Portal, customers can start a chat with a virtual or live agent for help.Email queries from customers can be managed either as interactions or cases. Interactions handle simple queries that can be resolved promptly, while cases are for more complex issues requiring investigation. Use interactions for simple questions and as a staging object for case categorization. Use cases for complex issues requiring investigation by the back office to facilitate proper resolution.External customers can reach out to customer service agents by phone. The Customer Service Management application uses both Computer Telephony Integration \(CTI\) and OpenFrame to provide phone support for customers.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 6
keywords: [Email Interaction for CSM]
breadcrumb: [Exploring Customer Service Management, Customer Service Management]
---

# Omnichannels for communicating with customers

Meet customers where they feel most comfortable by providing omnichannel support. Customers can use chat on the Customer Service Management portal, chat via consumer messaging apps, use email, or place a phone call.

Provides an overview of omnichannel support capabilities within the ServiceNow AI Platform.

Customers can use the following consumer messaging apps to message you.

-   WhatsApp
-   LINE
-   Facebook Messenger
-   Apple Messages for Business

To learn more, see [Integrating with consumer messaging apps](../task/messg-integrate-channels.md).

**Parent Topic:**[Exploring Customer Service Management](exploring-csm.md)

## Chat channel

From the Customer Service Portal and Consumer Service Portal, customers can start a chat with a virtual or live agent for help.

![Infographic displaying the process for users to chat with a virtual or live agent to get help submitting a case and resolving an issue.](../image/chat_image_1.png "Chatting with an agent")

The chat communication channel uses the ServiceNow® Connect Support feature to provide chat capability. You can also enable the ServiceNow® Virtual Agent application to create or use predefined chatbot topics \(conversations\) for your users.

The chat request from the customer is either routed to a virtual agent or to an available agent with the required skill set. The agent can respond to the customer and, if necessary, create a new case or link the discussion to an existing case.

An agent can also initiate a Zoom meeting from a chat to resolve issues faster. For more information, see [Chat Zoom Connector](chat-zoom-connector.md).

If a case is created as the result of a chat, the customer can later find and view the case from the portal for updates. The customer service agent can also link a chat discussion to an existing case. Details from the chat discussion are copied to the case form.

For more information, see [Connect Support](https://www.servicenow.com/docs/access?context=c_ConnectSupport&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US) and [Configuring the chat channel](c_ChatFeature.md).

When a support agent of the assignment group associated with the chat queue ends a chat with a user, a survey is available in the chat window for the users. Users can take the survey to give feedback about the interaction with an agent. The survey is not captured in the transcript in the agent's interactions page.

## Email channel

Email queries from customers can be managed either as interactions or cases. Interactions handle simple queries that can be resolved promptly, while cases are for more complex issues requiring investigation. Use interactions for simple questions and as a staging object for case categorization. Use cases for complex issues requiring investigation by the back office to facilitate proper resolution.

### Email Interaction

Enables you to create interactions to manage email engagement with customers. Agents can review these interactions and take appropriate actions. The customer query can be resolved by an email response over the interaction, or a case can be created for further investigation.![Customers can email support to get help from an agent.](../image/Email_as_an_Interaction.png)

-   **Streamlining case management from intake to resolution**

    When a customer sends an email, it’s automatically created as an interaction in the system. This interaction captures all email communication between agent and customer, providing agents with context for the query. The agent reviews the interaction to determine whether the issue requires further investigation. If the customer’s request is clear and needs resolution, a case is created based on the interaction.

    Once the case is created, the interaction is marked as closed. This helps prevent unnecessary duplication and keeps the system organized. When the agent replies to the customer's email through the case, an outbound interaction is automatically created. This confirms that all communication is tracked, maintaining a complete record of the conversation.


### Email to case

With email to case, customers can send emails to create cases and update current cases. They can also receive email updates from customer service agents as cases progress.

![Customers can email support to submit a case and get help from an agent.](../image/Email_to_case.png)

-   **Creating, viewing, and updating cases**

    Customers can create a new case by sending an email to a designated address. They can also create a case for a specific product by sending an email to a designated address and including the product name in the subject line. Or, if a channel configuration has been created, customers can send an email to a designated address regardless of the information included in the subject line.

    After submitting a case, the customer receives a confirmation email with the assigned case number and a link to the Case form. When an agent updates a case, the customer receives an email with the details.

    Customers can update an existing case in the following ways:

    -   By replying directly to an email from a customer service agent.
    -   By creating an email and including the Case: prefix followed by the case number in the subject line. For example, `Case:CS0000011`.
-   **Accepting and rejecting solutions**

    When an agent proposes a solution to a case, the customer receives an email with instructions for accepting or rejecting the solution. The customer can reply and include **Accept** or **Reject** in the first line of the email, or the customer can select the **Accept** or **Reject** link in the email.

    When an agent closes a case, two emails are sent to the customer. The first email states that the case has been closed. The second email provides a link to a customer satisfaction survey.

    **Note:** If a customer accepts a solution or closes a case from the Customer Service Portal, they’re automatically routed to the survey. They don’t receive the survey email.

    To get started with the email channel, see [Configuring the email channel](c_CustomerServiceEmailCommunication.md).


## Phone channel

External customers can reach out to customer service agents by phone. The Customer Service Management application uses both Computer Telephony Integration \(CTI\) and OpenFrame to provide phone support for customers.

![nfographic displaying the process when a customer calls support to get an agent to submit a case and resolve an issue.](../image/phone_image.png)

-   **Computer Telephony Integration \(CTI\)**

    CTI provides a way to integrate the ServiceNow AI Platform with telephony providers to support inbound and outbound calls. With this integration, customer service agents can place and accept calls from customers, quickly identify customers and account information, and capture case-related information.

    **Note:** The CTI integration with the Twilio Voice product requires activation of the Notify plugin.

-   **OpenFrame**

    OpenFrame is a tool that enables CTI capability with telephony service providers. OpenFrame provides a communication frame that agents use to place and receive customer calls.

-   **Interaction Controls Component \(ICC\)**

    Integrate ICC with contact centers to embed a native call control interface within the Agent Workspace. This streamlines the management of all inbound and outbound phone interactions by providing contextual assistance in a single interface.

    **Note:** The Interaction Controls Component \(ICC\) is a framework that includes voice call features. However, these features will not function unless they are implemented by a CCaaS \(Contact Center as a Service\) solution.

    For more information, see: [Integrating contact centers with Interaction Controls Component \(ICC\) for voice calls](contact-center-integration-with-icc.md)


To get started with the phone channel, see [Configuring the phone channel](c_PhoneCommunication.md).

