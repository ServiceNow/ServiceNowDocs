---
title: Edit translations for Virtual Agent topics
description: A Virtual Agent admin user can edit and publish translations directly in Assistant Designer Asset library.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/conversational-interfaces/virtual-agent/edit-translations-va-topics.html
release: zurich
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Localizing Virtual Agent conversations, Localization options for Virtual Agent, Build and deploy, Virtual Agent, Conversational Interfaces]
---

# Edit translations for Virtual Agent topics

A Virtual Agent admin user can edit and publish translations directly in Assistant Designer Asset library.

## Before you begin

**Note:** An updated Assistant Designer Asset library user interface is available when you install ServiceNow Otto in Virtual Agent. This content assumes that you can see the list view. If ServiceNow Otto in Virtual Agent is not installed, you see the legacy UI and topics page. For more information, see [Virtual Agent Designer legacy topics page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/virtual-agent/vad-prev-topics-page.md).

Role required: virtual\_agent\_admin or admin

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Assistant Designer**, select the **Asset library** tab, and do one of the following:

    -   Set the discovery type toggle switch to **LLM**, open a published topic, and then select the **Languages** tab.
    -   Set the discovery type toggle switch to **NLU/keyword**, then select **Manage languages** from Resources, and choose a model, language, and topic.
2.  In the **Topic translations** column, select **Edit**.

    The Edit Translations form opens.

    \[Omitted image "edit-languages-va-topic.png"\] Alt text: Assistant Designer Asset library Languages page Translations tab. Lock/unlock and Machine Translate controls, highlighted here, are visible when configured.

3.  On the Edit Translations form, you can do any of the following:

    -   Unlock fields and enter translations directly on the form.
    -   If it is configured in the Localization Framework, use machine translation to fill in the fields.

        To set up machine translation, see [Create a translator configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/create-custom-translator.md).

    -   Export files to send to a third party for translation.

        Select **Export Source File**, and then choose the file type. Select **Export File** to begin the download.

    -   Import translated files received from a translation service.

        From the Export Source file list, select **Import Translated File**.

4.  When translations are ready to publish, select **Publish Translations**.


## Result

Once translations are published, they are made available to Virtual Agent topics that use keywords dynamically.

If your topic uses Natural Language Understanding \(NLU\), train your localized models. You may also need to map them to the topic. Then test and publish your localized models to ensure that native speakers can access localized intents. For more information, see [Map a topic to a secondary NLU model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/virtual-agent/map-nlu-language-model.md) and [Test topic and NLU model translations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/virtual-agent/test-nlu-language-model.md).

**Parent Topic:**[Localizing Virtual Agent conversations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/virtual-agent/localize-va-topic.md)

