---
title: Activate the Google Dialogflow ES service and enable it in your instance
description: When you activate the Google Dialogflow ES service in the Open NLU Drivers \[open\_nlu\_driver\] table, the service becomes available as an option in Virtual Agent NLU settings.
locale: en-US
release: yokohama
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configure Google Dialogflow ES as the NLU provider for Virtual Agent, Configure Natural Language Understanding in Virtual Agent, Configuring Virtual Agent, Virtual Agent, Conversational Interfaces]
---

# Activate the Google Dialogflow ES service and enable it in your instance

When you activate the Google Dialogflow ES service in the Open NLU Drivers \[open\_nlu\_driver\] table, the service becomes available as an option in Virtual Agent NLU settings.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All**, and then enter `open_nlu_driver.list` in the filter.

2.  In the Open NLU Drivers table, locate the Google Dialogflow ES Script record.

3.  In the Active column, set the value to **true**.

    ![Open NLU Drivers portal, with the Active column for Google Dialogflow set to true.](../images/open-nlu-drivers-ggl-df.png)

4.  To enable NLU in your instance, navigate to **Conversational Interfaces** &gt; **Settings**, and then do the following:

    1.  Click **Virtual Agent**.

    2.  Under Natural Language Understanding \(NLU\), click **View Settings**.

    3.  Slide the **Activate** toggle switch to enable Natural Language Understanding.

    4.  In the NLU service provider list, select **Google Dialogflow ES - Script**.

    5.  If you plan to use language-specific NLU models, enable the languages in the Supported NLU Languages list.

        A language is enabled if the Enabled column displays **true**. For more information, see [Enable NLU languages in Virtual Agent settings](enable-langs-va-gen-settings.md).

    6.  Click **Save**.


## Result

Google Dialogflow ES is the NLU service provider for your instance.

**Parent Topic:**[Configure Google Dialogflow ES as the NLU provider for Virtual Agent](../concept/configure-dialogflow-es-integration.md)

**Previous topic:**[Generate a Java Keystore \(JKS\) file and configure security on your ServiceNow instance](vad-configure-dialogflow-security.md)

**Next topic:**[Test Virtual Agent with Google Dialogflow ES NLU in Virtual Agent Designer](test-va-nlu-dialogflow.md)

