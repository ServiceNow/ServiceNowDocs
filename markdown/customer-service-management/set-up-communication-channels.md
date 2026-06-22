---
title: Configure communication channels
description: Configure communication channels to provide users with options to email, call, or chat with your teams for help. You can also integrate with social media.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/customer-service-management/set-up-communication-channels.html
release: zurich
product: Customer Service Management
classification: customer-service-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Enable communication channels, Configure, Customer Service Management]
---

# Configure communication channels

Configure communication channels to provide users with options to email, call, or chat with your teams for help. You can also integrate with social media.

## Before you begin

Role required: admin

## About this task

You have the following options for setting up communication channels:

## Procedure

-   Set up the [Customer Service email channel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/c_CustomerServiceEmailCommunication.md).

    Customers can send emails to create new cases and update current cases as well as receive email updates from agents as cases progress. Customer Service Management uses the ServiceNow [email accounts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/ai-platform-administration/c_EmailAccounts.md) feature to create and maintain email accounts.

    -   [Configure one or more email addresses](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/ai-platform-administration/t_ConfigureAnEmailAccount.md).
    -   [Configure an email address for a product](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/t_ConfigureEmailCommunication.md).
    -   [Configure an email subject line prefix](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/t_ConfigureAnEmailSubjectLinePrefix.md)
    -   [Set email communication channel properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/r_CustomerServiceEmailProperties.md)
    -   [Create an email client template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/ai-platform-administration/t_CreateAnEmailClientTemplate.md).
    -   [Create quick messages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/ai-platform-administration/t_QuickMessages.md).
    -   [Create rules for incoming emails and create and assign cases](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/create-rules-incoming-emails-create-assign-cases.md).
-   Set up the [Customer Service phone channel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/c_PhoneCommunication.md).

    External customers can reach out to customer service agents using the phone communication channel. Customer Service Management uses both Computer Telephony Integration \(CTI\) and OpenFrame to provide phone support for customers, as well as the Notify application and the Twilio Voice product.

    OpenFrame is included with Customer Service Management. The CTI Softphone plugin \(com.snc.cti\) and the Customer Service CTI Demo Data \(com.snc.customerservice\_cti\_demo\) plugin must be activated separately. The Notify plugin \(com.snc.notify\) is activated as part of the CTI Softphone plugin.

    -   [Set up the phone communication channel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/t_PhoneInstallationAndConfiguration.md).
    -   [Associate a phone number with a workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/t_AssociateNumberWithWorkflow.md).
    -   [Create an OpenFrame configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/t_CreateAnOpenFrameConfiguration.md).
-   Set up the [Customer Service chat channel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/c_ChatFeature.md).

    The chat communication channel uses the Connect Support feature to provide chat capability from the Customer Service Portal and Consumer Service Portal. You can also enable Virtual Agent to create or use predefined chatbot topics \(conversations\) for your users.

    -   [Configure the customer service chat queue](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/t_ConfCustServChatQueue.md).
    -   [Add an agent to the chat support assignment group](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/t_AddAgentToChatSupAssignGroup.md).
    -   [Activate Virtual Agent for Customer Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/activate-virtual-agent-csm.md)
    -   [Activate Customer Service Virtual Agent conversations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/csm-virtual-agent-chatbot.md).
    -   [Integrate Customer Service Virtual Agent with Facebook Messenger](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/update-authentication-facebook-va-integration.md).
-   Set up the [social media integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/social-media-integration.md) feature to support case resolution through social media channels.

    -   [Create a social media profile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/create-social-profile.md) for an account, contact, or consumer.
    -   [Create a social media log entry](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/create-social-log.md) for a case.

