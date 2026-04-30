---
title: Enhanced natural language handling of user inputs in NLU topic discovery
description: Give Virtual Agent the capability of recognizing natural variations on yes and no from the user, such as sure or nope. By defining a range of boolean responses as affirmative or negative, Virtual Agent doesn't have to prompt the user to restate their preference.
locale: en-US
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configure Natural Language Understanding in Virtual Agent, Configuring Virtual Agent, Virtual Agent, Conversational Interfaces]
---

# Enhanced natural language handling of user inputs in NLU topic discovery

Give Virtual Agent the capability of recognizing natural variations on `yes` and `no` from the user, such as `sure` or `nope`. By defining a range of boolean responses as affirmative or negative, Virtual Agent doesn't have to prompt the user to restate their preference.

When Virtual Agent doesn't understand unexpected user input, it prompts the user again for information that it can understand. Starting with the Tokyo release, Virtual Agent can understand natural variations in boolean "yes/no" responses, such as `yep` or `nah`.

## Natural language handling in ServiceNow NLU

The VA NLU Dispatches \[sys\_cs\_nlu\_dispatch\] table stores the names of the model and intents that handle utterance variations.

For ServiceNow® NLU, the Setup Topics Model is already configured to handle boolean user inputs in English. There are two records in the table, **BOOLEAN\_NO** and **BOOLEAN\_YES**, which are mapped to the **Negative** and **Affirmative** intents in the Setup Topics Model.

![The VA NLU Dispatches table displaying the names of the intent and model that handle the utterance variations.](../images/va-nlu-dispatches-list.png)

The Setup Topics Model and intents are read only, so if you need to modify the intents or add additional intents in other languages, create a new model with new intents. You can update the existing entries and add new ones to the table.

## Setting up natural language handling for third-party NLU providers

If you are using IBM Watson, Microsoft LUIS, or Google Dialogflow for NLU topic discovery, add entries for the corresponding model and intents in the VA NLU Dispatches table, as described in [Configure enhanced natural language user input handling](../task/set-up-natural-lang-handling-other-nlu.md).

## Changing the confidence threshold

The confidence threshold for boolean inputs is defined in the **com.glide.cs.dialog.boolean\_threshold** system property. The default value is **0.9**. For more information, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=xanadu&pubname=xanadu-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

-   **[Configure enhanced natural language user input handling](../task/set-up-natural-lang-handling-other-nlu.md)**  
Add enhanced natural language handling for boolean user responses to your Virtual Agent environment. If you're using additional languages or third-party NLU providers, specify the model and intents that define variations in yes/no utterances for your bot.

**Parent Topic:**[Configure Natural Language Understanding in Virtual Agent](../task/configure-nlu-settings.md)

