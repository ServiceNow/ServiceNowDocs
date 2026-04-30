---
title: Configure Microsoft LUIS as the NLU provider for Virtual Agent
description: Use the intents, entities, and utterances defined in a Microsoft Language Understanding Intelligent Service \(LUIS\) application and apply them as an NLU model for your Virtual Agent conversations.
locale: en-US
release: zurich
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
keywords: [Microsoft, Virtual Agent, Language Understanding Intelligent Service, LUIS, NLU, Provider]
breadcrumb: [Configure NLU in Virtual Agent, Configure, Virtual Agent, Conversational Interfaces]
---

# Configure Microsoft LUIS as the NLU provider for Virtual Agent

Use the intents, entities, and utterances defined in a Microsoft Language Understanding Intelligent Service \(LUIS\) application and apply them as an NLU model for your Virtual Agent conversations.

## Before you begin

**Important:** Microsoft Language Understanding Intelligent Service \(LUIS\) will be fully retired on March 31, 2026. Beginning on October 31, 2025, the LUIS portal will no longer be available. Consider migrating your LUIS applications to Now Assist in Virtual Agent to benefit from continued product support and multilingual capabilities.

In Microsoft LUIS, do the following:

-   [Sign in to the LUIS portal and create an application to be used as an NLU model](https://docs.microsoft.com/en-us/azure/cognitive-services/LUIS/how-to/sign-in) \(requires a Microsoft Azure account.\)
-   Locate and copy these Microsoft LUIS keys:
    -   Authoring key that was automatically generated when you created your Microsoft LUIS account. The authoring key provides the authentication needed for your LUIS applications and for creating, training, and publishing them. You can find the authoring key by signing into LUIS, selecting your user account, and opening Account Settings.
    -   Prediction endpoint runtime key that you assigned to the resource for your Microsoft LUIS application. Virtual Agent accesses the LUIS runtime query prediction endpoint through this key.

        **Note:** If you are using more than one LUIS application \(NLU model\), you must provide the prediction endpoint runtime key for each application that you create.


In your ServiceNow instance, do the following:

-   Make sure that the Glide Virtual Agent plugin is activated, as it installs the Proxy Agent to the Microsoft LUIS Natural Language Understanding server plugin \(com.glide.nlu.msluis.intent.discovery\) needed for this integration. If you upgraded from a previous release, the upgrade process automatically retains the LUIS keys that you provided.
-   Role required: admin

## About this task

You can set only one NLU service provider for your instance.

## Procedure

1.  To set the credential passwords for the LUIS NLU model, entities, intents, and prediction information, do the following:

    1.  Navigate to **All**, and then enter `http_connection.list` in the filter.

    2.  In the HTTP\(s\) Connections page, select **MSLuisNLUModels** in the Connection alias column to open the record.

        ![HTTPS Connections table, with Connection alias key and MSLuisNLUModels value highlighted.](../images/va-luis-model-connalias.png)

    3.  In the Connection &amp; Credential Aliases for MSLuisNLUModels page, go to the Connection Attributes related list.

    4.  Find the Credential Password attribute, and then double-select in the **Default value** column to edit the value.

        ![Connection & Credential Credential Aliases form for MSLuisNLUModels. Credential Password attribute and the Default value field in which you enter the Microsoft Luis authoring key are highlighted.](../images/va-luis-model-attribute.png)

    5.  Enter the MS LUIS authoring key in the **Default value** field, and then select the save icon.

    6.  Return to the HTTP\(s\) Connections page and repeat these steps to add the MS LUIS authoring key as the default value in the following Connection aliases:

        -   MSLuisNLUCustomEntities
        -   MSLuisNLUPrebuiltEntities
        -   MSLuisNLUIntents
        -   MSLuisNLUPrediction
        ![HTTPS connections table, with Connection alias values for Microsoft Luis NLU values highlighted.](../images/va-luis-connection-aliases.png)

        **Note:** Repeat these steps for each Microsoft LUIS application that you use as an NLU model. Each application has its own prediction endpoint runtime key that you must provide.

2.  Make the LUIS NLU service active.

    1.  Navigate to **All**, and then enter `open_nlu_driver.list` in the filter.

    2.  In the Open NLU Drivers table, set the **Active** field value for the **MS Luis Script** record to **true**.

        ![Open NLU Drivers table, with MS Luis-Script service Active field value set to true.](../images/open-nlu-drivers-luis.png)

        **Note:** Activating this setting adds **MS Luis - Script** to the list of available NLU services in Virtual Agent settings.

3.  To enable NLU in your instance, navigate to **Conversational Interfaces** &gt; **Settings**, and then do the following:

    1.  Select **Virtual Agent**.

    2.  Under Natural Language Understanding \(NLU\), select **View Settings**.

    3.  Slide the **Activate** toggle switch to enable Natural Language Understanding.

    4.  In the **NLU Service Provider** list, select **MS Luis - Script**.

    5.  If you plan to use language-specific NLU models, enable the languages in the Supported NLU Languages list.

        A language is enabled if the Enabled column displays **true**. For more information, see [Enable NLU languages in Virtual Agent settings](enable-langs-va-gen-settings.md).

    6.  Select **Save**.

    Microsoft LUIS is now the NLU service provider for your instance.


**Parent Topic:**[Configure Natural Language Understanding in Virtual Agent](configure-nlu-settings.md)

