---
title: Edit translations for Virtual Agent topics
description: A Virtual Agent admin user can edit and publish translations directly in Virtual Agent Designer.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/conversational-interfaces/virtual-agent/edit-translations-va-topics.html
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2024-10-23"
reading_time_minutes: 1
breadcrumb: [Localizing Virtual Agent conversations, Localization options for Virtual Agent, Building and deploying Virtual Agent, Virtual Agent, Conversational Interfaces]
---

# Edit translations for Virtual Agent topics

A Virtual Agent admin user can edit and publish translations directly in Virtual Agent Designer.

## Before you begin

Role required: virtual\_agent\_admin or admin

## Procedure

1.  Do one of the following:

    -   Navigate to **All** &gt; **Conversational Interfaces** &gt; **Virtual Agent** &gt; **Designer**, open a published topic, and then select the **Languages** tab.
    -   \(NLU only\) Navigate to **All** &gt; **Conversational Interfaces** &gt; **Virtual Agent** &gt; **Designer**, and slide the discovery type toggle switch to **NLU/keyword**. Select **Manage languages** from Resources, and then choose a model, language, and topic.
2.  In the **Topic translations** column, select **Edit**.

    The Edit Translations form opens.

    \[Omitted image "edit-languages-va-topic-new.png"\] Alt text: Virtual Agent Designer Languages page Translations tab. Lock/unlock and Machine Translate controls, highlighted here, are visible when configured.

3.  On the Edit Translations form, you can do any of the following:

    -   Unlock fields and enter translations directly on the form.
    -   If it is configured in the Localization Framework, use machine translation to fill in the fields.

        To set up machine translation, see Create a translator configuration.

    -   Export files to send to a third party for translation.

        Select **Export Source File**, and then choose the file type. Select **Export File** to begin the download.

    -   Import translated files received from a translation service.

        From the Export Source file list, select **Import Translated File**.

4.  When translations are ready to publish, select **Publish Translations**.


## Result

Once translations are published, they are made available to Virtual Agent topics that use keywords dynamically.

If your topic uses Natural Language Understanding \(NLU\), train your localized models. You may also need to map them to the topic. Then test and publish your localized models to ensure that native speakers can access localized intents. For more information, see [Map a topic to a secondary NLU model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/conversational-interfaces/virtual-agent/map-nlu-language-model.md) and [Test topic and NLU model translations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/conversational-interfaces/virtual-agent/test-nlu-language-model.md).

**Parent Topic:**[Localizing Virtual Agent conversations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/conversational-interfaces/virtual-agent/localize-va-topic.md)

