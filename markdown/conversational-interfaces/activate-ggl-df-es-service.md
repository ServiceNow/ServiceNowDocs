---
title: \(Legacy\) Activate the Google Dialogflow ES service and enable it in your instance
description: When you activate the Google Dialogflow ES service in the Open NLU Drivers \[open\_nlu\_driver\] table, the service becomes available as an option in Virtual Agent NLU settings.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/conversational-interfaces/activate-ggl-df-es-service.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Configure Google Dialogflow ES, Configure NLU in Virtual Agent, Configure NLU, \(Legacy\) Virtual Agent for NLU, Conversational Interfaces]
---

# \(Legacy\) Activate the Google Dialogflow ES service and enable it in your instance

When you activate the Google Dialogflow ES service in the Open NLU Drivers \[open\_nlu\_driver\] table, the service becomes available as an option in Virtual Agent NLU settings.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All**, and then enter `open_nlu_driver.list` in the filter.

2.  In the Open NLU Drivers table, locate the Google Dialogflow ES Script record.

3.  In the Active column, set the value to **true**.

    \[Omitted image "open-nlu-drivers-ggl-df.png"\] Alt text: Open NLU Drivers portal, with the Active column for Google Dialogflow set to true.

4.  To enable NLU in your instance, navigate to **Conversational Interfaces** &gt; **Settings**, and then do the following:

    1.  Click **Virtual Agent**.

    2.  Under Natural Language Understanding \(NLU\), click **View Settings**.

    3.  Slide the **Activate** toggle switch to enable Natural Language Understanding.

    4.  In the NLU service provider list, select **Google Dialogflow ES - Script**.

    5.  If you plan to use language-specific NLU models, enable the languages in the Supported NLU Languages list.

        A language is enabled if the Enabled column displays **true**. For more information, see [\(Legacy\) Enable NLU languages in Virtual Agent settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/enable-langs-va-gen-settings.md).

    6.  Click **Save**.


## Result

Google Dialogflow ES is the NLU service provider for your instance.

