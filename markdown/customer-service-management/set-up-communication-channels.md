---
title: Configure communication channels
description: Configure communication channels to provide users with options to email, call, or chat with your teams for help. You can also integrate with social media.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Enable communication channels, Configuring Customer Service Management, Customer Service Management]
---

# Configure communication channels

Configure communication channels to provide users with options to email, call, or chat with your teams for help. You can also integrate with social media.

## Before you begin

Role required: admin

## About this task

You have the following options for setting up communication channels:

## Procedure

-   Set up the [Customer Service email channel](../concept/c_CustomerServiceEmailCommunication.md).

    Customers can send emails to create new cases and update current cases as well as receive email updates from agents as cases progress. Customer Service Management uses the ServiceNow [email accounts](https://www.servicenow.com/docs/access?context=c_EmailAccounts&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US) feature to create and maintain email accounts.

    -   [Configure one or more email addresses](https://www.servicenow.com/docs/access?context=t_ConfigureAnEmailAccount&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).
    -   [Configure an email address for a product](t_ConfigureEmailCommunication.md).
    -   [Configure an email subject line prefix](t_ConfigureAnEmailSubjectLinePrefix.md)
    -   [Set email communication channel properties](../reference/r_CustomerServiceEmailProperties.md)
    -   [Create an email client template](https://www.servicenow.com/docs/access?context=t_CreateAnEmailClientTemplate&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).
    -   [Create quick messages](https://www.servicenow.com/docs/access?context=t_QuickMessages&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).
    -   [Create rules for incoming emails and create and assign cases](../concept/create-rules-incoming-emails-create-assign-cases.md).
-   Set up the [Customer Service phone channel](../concept/c_PhoneCommunication.md).

    External customers can reach out to customer service agents using the phone communication channel. Customer Service Management uses both Computer Telephony Integration \(CTI\) and OpenFrame to provide phone support for customers, as well as the Notify application and the Twilio Voice product.

    OpenFrame is included with Customer Service Management. The CTI Softphone plugin \(com.snc.cti\) and the Customer Service CTI Demo Data \(com.snc.customerservice\_cti\_demo\) plugin must be activated separately. The Notify plugin \(com.snc.notify\) is activated as part of the CTI Softphone plugin.

    -   [Set up the phone communication channel](t_PhoneInstallationAndConfiguration.md#).
    -   [Associate a phone number with a workflow](t_AssociateNumberWithWorkflow.md).
    -   [Create an OpenFrame configuration](t_CreateAnOpenFrameConfiguration.md).
-   Set up the [Customer Service chat channel](../concept/c_ChatFeature.md).

    The chat communication channel uses the Connect Support feature to provide chat capability from the Customer Service Portal and Consumer Service Portal. You can also enable Virtual Agent to create or use predefined chatbot topics \(conversations\) for your users.

    -   [Configure the customer service chat queue](t_ConfCustServChatQueue.md).
    -   [Add an agent to the chat support assignment group](t_AddAgentToChatSupAssignGroup.md).
    -   [Activate Virtual Agent for CSM](activate-virtual-agent-csm.md)
    -   [Activate Customer Service Virtual Agent conversations](../concept/csm-virtual-agent-chatbot.md).
    -   [Integrate Customer Service Virtual Agent with Facebook Messenger](update-authentication-facebook-va-integration.md).
-   Set up the [social media integration](../concept/social-media-integration.md) feature to support case resolution through social media channels.

    -   [Create a social media profile](create-social-profile.md) for an account, contact, or consumer.
    -   [Create a social media log entry](create-social-log.md) for a case.

