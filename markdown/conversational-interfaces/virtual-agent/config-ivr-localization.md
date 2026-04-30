---
title: Configure localization in Conversational IVR with Amazon Connect
description: Configure localization in Conversational IVR to use localization with Virtual Agent in other supported languages.
locale: en-US
release: zurich
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
keywords: [Virtual Agent, localization, Amazon Connect, Conversational IVR, AWS Console]
breadcrumb: [Configure AWS account, Configuring Conversational IVR with Amazon Connect, Conversational IVR with Amazon Connect, Integrating Virtual Agent with Voice channels, Integrate VA with other channels, Virtual Agent, Conversational Interfaces]
---

# Configure localization in Conversational IVR with Amazon Connect

Configure localization in Conversational IVR to use localization with Virtual Agent in other supported languages.

## Before you begin

Role required: admin

Ensure that you have completed the IVR setup on both AWS Console and ServiceNow instance.

## Procedure

1.  Log in to the AWS Management Console and open the **Amazon Lex** bot named **SN\_CI\_CC\_LexBot**.

2.  Change the language of the amazon IVR Contact.

    1.  Navigate to Amazon Connect from the AWS Console.

    2.  On the instance page, open the connect instance.

    3.  Hover over the Routing icon ![Routing icon.](../images/routing-icon.png) on the left navigation bar and select **Contact flows**.

    4.  Select the **SN\_CI\_CC\_Inbound\_Contact\_Flow**.

        SN\_CI\_CC\_Inbound\_Contact\_Flow is the default contact that is shipped to the user for use with Conversation IVR.

    5.  On the Contact flow, select the **Set voice** flow.

    6.  On the Set voice pop-up, select the language that you added from the **Language** drop-down and select the **Set language attribute** check box.

        English \(US\) is the default voice language and the English \(US\) language code is sent to the LexBot. The LexBot then collects the intents from the English \(US\) language.

        **Note:** There are different dialects available for a language. Therefore, ensure that you select the correct language with its dialect that you have added previously.

    7.  Select **Save**.

    8.  Select **Publish** to publish the Contact flow with the new language.

    The entire process of setting up the language attribute in **Set voice** block works only if you use Virtual Agent integration with one language.

    If you wish to select the language dynamically for every conversation, you must manually add a list of language choices to get the input from the user and use **Set voice** block to set the appropriate language code.

    The following image illustrates the flow:

    ![Illustration to set up language attributes for the new language added.](../images/ivr-set-lang-flow.png "Workflow to set language attribute")


**Parent Topic:**[Configuring your AWS account for use with Conversational IVR](../concept/configure-aws-account.md)

