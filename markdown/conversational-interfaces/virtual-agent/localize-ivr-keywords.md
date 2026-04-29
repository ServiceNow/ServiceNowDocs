---
title: Customize keywords in Conversational IVR
description: Customize the IVR integration-specific keywords that are provided by default for better conversation in another language with the Virtual Agent.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configure AWS account, Configuring Conversational IVR with Amazon Connect, Conversational IVR with Amazon Connect, Integrating Virtual Agent with Voice channels, Integrate VA with other channels, Virtual Agent, Conversational Interfaces]
---

# Customize keywords in Conversational IVR

Customize the IVR integration-specific keywords that are provided by default for better conversation in another language with the Virtual Agent.

## Before you begin

Role required: admin

Ensure that you have completed the IVR setup on both AWS Console and ServiceNow instance.

**Note:** Any customizations done to the Lex bot must be redone in case of any updates to the Lex bot resource in the future versions of the application.

## Procedure

1.  Log in to the AWS Admin Console and open the **Amazon Lex** bot named **SN\_CI\_CC\_LexBot**.

2.  If you want to customize the default keywords, you can edit the **amz\_ivr\_keywords** slot type and give preferred values, and here's how you can do that.

    1.  Under the Conversation structure section in Slot types, select **View slot types**.

    2.  On the Slot types page, select **AMZ\_IVR\_KEYWORDS** slot type.

        The slot type is used for customizing the IVR integration-specific keywords namely **next**, **repeat**, **back**, and **skip**. These keywords can be used when talking to the Virtual Agent to navigate the paginated options/list of choices to skip a control.

        **Important:** Ensure that you are editing the values only on the right column. Do not edit the values on the left column as they should not be changed regardless of the language.

        By default the slot type values \(on the right column\) are in English. If the values on the right are not suitable for the another, change them to equivalent appropriate values, which shall be spoken by you when talking to the Virtual Agent.![Edit the slot type values in the column on the right.](../images/ivr-slot-type-values.png)

        If you have edited the slot type values on the right column, you must also ensure that you edit their respective bot messages on your instance to reflect these changes. For more information, see [Manage bot messages for Conversational IVR](edit-va-ivr-messages.md).

    3.  Click **Save Slot type** and click **Build** on the top right of the page.

        **Note:** You must build the Slot types for any new changes you made.

        The language is successfully built and on the All languages page, you can notice the **Successfully built** status against the language you have customized.

3.  Create a new version of the bot to include both the languages.

    1.  On the left navigation, select **Bot versions**.

    2.  On the Versions page, select **Create version** on the top-right.

        **Note:** Ensure that all the languages that you need in this bot have the **Successfully built** status before creating the version as only the built languages will be included in the version.

    3.  On the Create version page, provide a **Description** for the version and click **Create**.

        A version gets created with the next number. For example, Version 2 when there is only the default version 1 on your AWS instance.

4.  Associate the version that you created with the production alias.

    1.  One left pane, navigate to **Deployment** &gt; **Aliases** and select **SN\_CI\_CC\_LexBot\_Prod\_Alias**, the default production Alias associated with Version 1 for a newly set up integration.

    2.  On the Alias page, select **Associate version with alias** and select the version you created for the language being customized.

        **Note:** Ensure to always have the production alias to point to the latest version number.

    3.  On the Associate alias to version pop-up, select the version and select **Associate**.![The Associated version list displays available versions and an option for None.](../images/ivr-associate-alias.png)

        At this step, the bot is available for use in the language that you customized.


**Parent Topic:**[Configuring your AWS account for use with Conversational IVR](../concept/configure-aws-account.md)

