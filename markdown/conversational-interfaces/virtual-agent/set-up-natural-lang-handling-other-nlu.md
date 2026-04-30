---
title: Configure enhanced natural language user input handling
description: Add enhanced natural language handling for boolean user responses to your Virtual Agent environment. If you're using additional languages or third-party NLU providers, specify the model and intents that define variations in yes/no utterances for your bot.
locale: en-US
release: yokohama
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Enhanced natural language handling of user inputs in NLU topic discovery, Configure Natural Language Understanding in Virtual Agent, Configuring Virtual Agent, Virtual Agent, Conversational Interfaces]
---

# Configure enhanced natural language user input handling

Add enhanced natural language handling for boolean user responses to your Virtual Agent environment. If you're using additional languages or third-party NLU providers, specify the model and intents that define variations in yes/no utterances for your bot.

## Before you begin

In your NLU provider, create a model with two intents, or add two intents to an existing model. One intent should contain affirmative or "yes" utterances. The other intent should contain negative or "no" utterances.

If your environment supports multiple languages, create models and intents for each language.

Role required: virtual\_agent\_admin or admin

## About this task

The default entries in this table apply to ServiceNow NLU for English only. If you want to implement natural language handling in other languages, add new entries to the table for each language.

## Procedure

1.  Navigate to **All**, and then enter `sys_cs_nlu_dispatch.list` in the filter.

2.  Select **New** or an existing entry that you want to modify.

    Alternatively, select **New** to add an entry for another language or third-party NLU provider.

3.  On the form, fill in the fields.

<table id="table_yz1_1kp_m5b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

NLU Model ID

</td><td>

Name of the model that contains the defining intents for the boolean responses.

</td></tr><tr><td>

Name

</td><td>

Value name that represents the type of user input being configured. The following values are valid:-   **BOOLEAN\_NO**: Maps to utterances that express a "no" response to a yes/no question.
-   **BOOLEAN\_YES**: Maps to utterances that express a "yes" response to a yes/no question.


</td></tr><tr><td>

Active

</td><td>

Option that enables enhanced natural language user responses on your instance.

</td></tr><tr><td>

NLU Intent ID

</td><td>

Name of the corresponding intent for the boolean option.By default, the intent for BOOLEAN\_NO is Negative. The intent for BOOLEAN\_YES is Affirmative. If you need to make changes, create a new model with these intents, and then specify the new intent in this field.

</td></tr><tr><td>

Language

</td><td>

Language of the intent. English for ServiceNow NLU is configured by default.If you need to support other languages,you can add a row in the table for each supported language.

</td></tr></tbody>
</table>4.  Select **Submit** or **Update**.


## Result

Depending on your environment, your configuration may contain entries for other languages \(such as French or German in the example below\) or for other NLU providers, such as IBM Watson.

![VA NLU Dispatches table displaying the configurations for French, German, and IBM Watson in English.](../images/va-nlu-dispatches-full-config.png)

**Parent Topic:**[Enhanced natural language handling of user inputs in NLU topic discovery](../concept/natural-language-user-response-handling.md)

