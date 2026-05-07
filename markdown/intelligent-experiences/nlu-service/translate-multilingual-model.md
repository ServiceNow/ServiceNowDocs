---
title: Translate a multilingual model
description: Add a language to an existing NLU model by translating it. Use one of several translation options to add a secondary model in a supported language.
locale: en-US
release: australia
product: NLU Service
classification: nlu-service
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Multilingual model management, Natural Language Understanding, Enable AI experiences]
---

# Translate a multilingual model

Add a language to an existing NLU model by translating it. Use one of several translation options to add a secondary model in a supported language.

## Before you begin

-   Activate the Localization Framework \(com.glide.localization\_framework.installer\) plugin. See [Localization Framework](https://www.servicenow.com/docs/access?context=localization-framework-landing&version=australia&pubname=australia-platform-administration&ft:locale=en-US).
-   In your target application scope, create a primary language model, or use an existing primary model.
-   Multilingualism is available for Virtual Agent and AI Search models.
-   Role required: nlu\_admin or admin.

**Note:** The nlu\_editor role cannot initiate a model translation, because the nlu\_editor does not have permission to create a new model. See [Assign an NLU editor to a model](assign-nlu-editor-to-model.md).

## About this task

Translating a model creates a secondary model of the language you choose, in the same application scope as the primary model.

The secondary model contains the same content as the primary. However, the intents of the secondary model are disabled and must be reviewed prior to publishing the secondary model.

To translate a primary model and create a secondary model, you must choose a translation mode. The modes appear in the user interface as individual cards that you use in Step 4 of this procedure. Activated cards appear surrounded by a thin green border. Only activated cards can be selected as your translation mode. For the Use AI and Use a third party modes, selecting the **Add** button on an activated card starts the translation.

The No translation mode is active by default and available for all languages. However, the Use AI and Use a third party modes are activated only when the localization framework \(LF\) settings for the secondary language are in place.

**Note:** Before you add a new model in a secondary language, you must ensure that the Localization Framework \(LF\) settings for the secondary language are completed.

<table id="table_uwq_fdf_zrb"><thead><tr><th>

Translation mode

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Use AI**

</td><td>

Translate using machine-intelligence providers such as Google. Selecting the card creates a translated secondary model. Machine translations may be incorrect or too literal, so review the translated content for accuracy. For more information, see [Dynamic Translation](https://www.servicenow.com/docs/access?context=dynamic-translation-overview&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

 To activate the Use AI mode, [Localization Framework](https://www.servicenow.com/docs/access?context=localization-framework-landing&version=australia&pubname=australia-platform-administration&ft:locale=en-US) must be configured and activated.

</td></tr><tr><td>

**Use a third party**

</td><td>

Request translation by a professional translation team. When you select this mode, an LF task is created per the LF language group settings for the secondary language. When the translations are completed, the translated model is created and ready for review. For more information, see [Localization Framework](https://www.servicenow.com/docs/access?context=localization-framework-landing&version=australia&pubname=australia-platform-administration&ft:locale=en-US) and [Translation modes](https://www.servicenow.com/docs/access?context=translation-modes&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

</td></tr><tr><td>

**No translation**

</td><td>

Default. Manually translate your primary language into a secondary language. Selecting this mode creates a draft secondary model with the intent names the same as that of the primary model. These intents are disabled by default, and you must enter your utterances manually. Names of intents and names of entities imported from the primary model aren't editable. Names of entities that you create directly in the secondary model are editable. This mode is also helpful if you want to draft and save the primary model first, and then translate your utterances later.

</td></tr></tbody>
</table>Multilingual models are supported in 17 languages.

**Note:** Some of these languages support only intents, not entities. If the language is intent-only, your primary model entities will not be translated or copied. For more information, see [NLU language support](../concept/nlu-language-support.md).

In this example scenario, your primary model uses the English language and you're adding a version in the French language, without translating utterances.

## Procedure

1.  Navigate to **All** &gt; **NLU Workbench** &gt; **Models**.

    The Virtual Agent tab opens by default. If appropriate, select the AI Search tab.

2.  Identify a primary model to which you want to assign a secondary language.

3.  In the row of the primary model, select the more options menu, then select **Add a language**.

    **Note:** You may need to scroll to the right to find the more options menu.

    ![In the NLU Workbench home, the More options list is expanded, and Add a language is highlighted.](../images/translate-model001V.png)

4.  In the **Add a language to this model** window, choose the desired language for the secondary model and the translation method.

    ![The window for Add a language to this model. The No translation card is highlighted.](../images/translate-model002V.png)

5.  Select the **Add** button.

    The secondary model is created and the **Build and train your model** phase of the secondary model loads.


## What to do next

If you chose to enable the model without translation, you must manually enter training utterances for each intent. If you choose to use software or a third-party translator, you must review the translations before you can continue working on the model.

Entering training utterances and reviewing secondary models can be delegated to users who have the nlu\_editor role. For more information, see [Assign an NLU editor to a model](assign-nlu-editor-to-model.md) and [Resolve intent issues](resolve-intent-issues.md).

