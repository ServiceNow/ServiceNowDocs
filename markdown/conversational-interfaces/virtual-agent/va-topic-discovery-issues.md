---
title: Resolve Natural Language Understanding \(NLU\) topic discovery issues
description: If an intent is not being chosen when expected, you can troubleshoot NLU prediction errors.
locale: en-US
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: reference
last_updated: "2024-10-23"
reading_time_minutes: 12
breadcrumb: [Debug a Virtual Agent topic, Getting started with Virtual Agent Designer, Building and deploying Virtual Agent, Virtual Agent, Conversational Interfaces]
---

# Resolve Natural Language Understanding \(NLU\) topic discovery issues

If an intent is not being chosen when expected, you can troubleshoot NLU prediction errors.

## Quick troubleshooting tips

If a Virtual Agent is not being discovered, check the following:

-   **Is NLU enabled for the session language?**

    Enable the language in Natural Language Understanding \(NLU\) settings for Virtual Agent. For details, see [Enable NLU languages in Virtual Agent settings](../task/enable-langs-va-gen-settings.md).

-   **Is the NLU Model trained and published for the session language?**

    Your topic may not be using the latest changes to your model. For ServiceNow® NLU, see [Train and try your NLU model](https://www.servicenow.com/docs/access?context=test-train-nlu-model&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US) and [Publish a Virtual Agent topic](../task/publish-virtual-agent-topic.md).

-   **Is the Virtual Agent topic published, discoverable, and bound to a published NLU Model and Intent for the session language?**

    The topic should be bound to a single model and intent for a given language. Ensure there are no duplicate intents bound to other topics. Make sure that the topic, model, and intent are in the same domain. For more information, see [Publish a Virtual Agent topic](../task/publish-virtual-agent-topic.md).

-   **Are any roles or conditions specified for the Virtual Agent topic on the Properties tab in Virtual Agent Designer?**

    If the topic is shown only for certain roles or for certain conditions, this can impede topic discovery. For details, see [Topic Properties tab](vad-topic-properties-tab.md).

-   **Why did Virtual Agent discover my topic in Spanish but not in French?**

    There are several possibilities:

    -   Not all languages are supported by all NLU providers. For details, see [Language support for NLU services](language-support-nlu-services.md).
    -   Not all topics are bound to a language-specific NLU model and intent.

        For example, Topic A may be mapped as follows:

        -   Bound to Model A and Intent A for English
        -   Bound to Model A and Intent A for Spanish
        -   NOT bound to a model or intent for French
        In this scenario, create a French model and intent for the topic. For more information, see [Multilingual model management](https://www.servicenow.com/docs/access?context=multilingual-model-managent&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).

-   **Why did a topic variable NOT slot fill?**

    Check the following:

    -   The topic's user input node was not configured with an associated entity. Use the **NLU entity** property for the node in Virtual Agent Designer.

        ![Specify an existing entity in the NLU entity list.](../images/input-node-nlu-entity-field.png)

    -   The prediction result contained an NLU entity with a confidence score that was less than the configured confidence threshold.
    -   The NLU entity value for the node was invalid. For example, you can't apply the word "red" to a Date/Time entity type.
-   **Test discovery from the topic.**

    Do one of the following:

    -   From the home page, slide the discovery type toggle switch to **NLU/Keyword**, then select **Test NLU/Keyword Topics**. Enter your utterance, and watch the **Analyze test phrases** tab.
    -   Open the topic in Virtual Agent Designer, then select **Test**. In the Test window, select the **Include topic discovery** check box. Enter your utterance, and watch the **Analyze test phrases** tab.
    For details, see [Testing NLU/Keyword topics](va-designer-testing.md). For an understanding of how topic discovery works, see [Natural Language Understanding topic discovery logic in Virtual Agent](../concept/how-topic-discovery-works.md).

-   **Is "Setup Topic" the topic in question?**

    If so, it needs to be configured in Conversational Interfaces Chat Settings for it to be discovered. For details, see [Configure a Virtual Agent chat experience](../task/configure-default-chat-experience.md).

-   **Questions or issues with mid-topic switching.**
    -   **Why did the conversation return to Topic A after Virtual Agent switched to Topic B?**

        The **Resume topic flow after topic switching** attribute is enabled on the topic. You can find this toggle switch on the **Properties** tab under **Advanced properties** &gt; **Additional**.

    -   **Why did the conversation NOT return to Topic A after Virtual Agent switched to Topic B?**

        The **Resume topic flow after topic switching** attribute is disabled on the topic. You can find this toggle switch on the **Properties** tab under **Advanced properties** &gt; **Additional**.

    -   **If Virtual Agent doesn't find an intent, will it use a keyword search in mid-topic?**

        No.

    -   **Are Topic A's variables available to Topic B after switching?**

        No.

    -   **Are Topic B's variables available to Topic A when Topic A resumes?**

        No.


For additional troubleshooting, check the information in the following tables.

## Check NLU prediction information in the Open NLU tables

When reviewing or debugging topics that use Natural Language Understanding \(NLU\), you can use various Open NLU tables to view the NLU prediction results for your topics. For example, the Open NLU Predict Intent Feedbacks and Open NLU Predict Entity Feedbacks tables provide detailed information on the NLU processing performed by applications \(such as Virtual Agent\) to determine topic intent and entities \(slot filling\).

-   **Open NLU Predict Intent Feedbacks table**

    The Open NLU Predict Intent Feedbacks \[open\_nlu\_predict\_intent\_feedback\] table shows the intent processing that an application \(in this case Virtual Agent\) performs in response to an NLU intent prediction result. The goal for Virtual Agent is to map a predicted NLU intent to a Virtual Agent topic. Whenever Virtual Agent suggests a topic, a record of the prediction result is added to this table. If Virtual Agent doesn't find a topic, no prediction occurs, and a record marked **Skipped** is added to this table.

    To view the table, navigate to **All**, and then enter `open_nlu_predict_intent_feedback.list` in the navigation filter.

<table id="table_ojs_j3y_vjb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

App

</td><td>

Application using NLU. For example: **VA** \(Virtual Agent\).

</td></tr><tr><td>

App Document

</td><td>

sys\_id of the application record. For example: **sys\_cs\_topic.sys\_id**.

</td></tr><tr><td>

App document table

</td><td>

Table of the application record. For example: **sys\_cs\_topic** \(Topics table\).

</td></tr><tr><td>

Auto-Selected

</td><td>

Boolean indicating whether the system detected only one intent above the prediction threshold, and therefore the application chose to run the topic that matched the same intent: **true** or **false**.

</td></tr><tr><td>

Current Intent

</td><td>

NLU intent that was used by the application when the NLU prediction was submitted. This field can be empty \(blank\). For example, an intent used in the Virtual Agent application could be **Change password**.

</td></tr><tr><td>

Domain

</td><td>

The intent's domain. For example, Global or ITSM.

</td></tr><tr><td>

External Model Display Name

</td><td>

Name of the external NLU model. For example, the name of the IBM Watson Assistant NLU application.

</td></tr><tr><td>

Intent Switch Causer

</td><td>

Name of the originating topic that prompts the user for confirmation. There are two possible scenarios for values in this column:-   The user is prompted for confirmation on the initial intent match for their utterance \(**Ask user if topic VA chose is correct** toggle switch is enabled in [NLU Settings](../task/configure-nlu-settings.md)\).

If the user is prompted for an initial utterance, this value may be the Greetings topic. If the value is **empty**, the user either was not prompted for the initial match, or the user rejected the initially matched topic intent.

-   The user is prompted for confirmation for an intent switch in mid-topic \(**Ask user if switched topic is correct** toggle switch is enabled in [NLU Settings](../task/configure-nlu-settings.md)\).

If the user is prompted for a switch in mid-topic, this value is the name of the topic they were viewing at the time of the switch.

 **Note:** System tasks may also display here, which you can ignore. For example: **\_\_silent\_TerminateGoal\_a3817a5f7ca7439b8**.

</td></tr><tr><td>

Intent Switch Causer current Task

</td><td>

Name of the task \(node\) that the user switches from.**Note:** System tasks may also display here, which you can ignore. For example: **\_\_silent\_TerminateGoal\_a3817a5f7ca7439b8**.

</td></tr><tr><td>

Mapped

</td><td>

Boolean indicating whether the application \(Virtual Agent\) considered the prediction to be usable by matching the intent to an available topic: **true** or **false**.

</td></tr><tr><td>

Model Display Name

</td><td>

Name of the ServiceNow NLU model.

</td></tr><tr><td>

Model ID

</td><td>

ID of the NLU model that the prediction was submitted for.

</td></tr><tr><td>

Model Name

</td><td>

Name of the NLU model that the prediction was submitted for.

</td></tr><tr><td>

NLU Topic Discovery Outcome

</td><td>

Prediction result for initial utterance in a conversation as part of topic discovery:-   **AI Search Fallback**: No prediction was made. AI Search was used as the fallback.
-   **Correct**: A single prediction was made. The user confirmed the topic was correct.
-   **Correct Among Multiple**: Multiple predictions were made. This result indicates that the user selected this prediction. Other prediction records are marked as Uncategorized.
-   **Exited with no confirmation**: The user exits with no confirmation.
-   **Incorrect**: A single prediction was made. The user confirmed the topic was incorrect.
-   **Incorrect Among Multiple**: Multiple predictions were made, but the user did not select any of the suggested topics. This result indicates that this prediction had the highest Prediction Confidence value. The other prediction records are marked as Uncategorized.
-   **Setup Topic Prediction**: Setup topic related prediction was made without using AI Search.
-   **Skipped**: No prediction was made.
-   **Skipped with New Utterance**: When the Topic menu displayed, the user typed a new utterance.
-   **Uncategorized**: None of the above conditions were met, or the user abandoned the conversation.


</td></tr><tr><td>

NLU Model Language

</td><td>

Language of the NLU model used for the prediction.

</td></tr><tr><td>

Prediction

</td><td>

Name of the predicted intent.

</td></tr><tr><td>

Prediction Audit Log

</td><td>

Reference to the Open NLU Predict Logs \[open\_nlu\_predict\_log\] table.

</td></tr><tr><td>

Prediction Confidence

</td><td>

Confidence value of the prediction.

</td></tr><tr><td>

Requester Session Language

</td><td>

Language code of the requester session language when Dynamic Translation is enabled.For example, if the user types in French, the code **fr** is stored. If language detection is enabled and the user enters text in a language that is not the default, Virtual Agent asks the user to confirm their language. If confirmed, the detected language becomes the default value for the session.

</td></tr><tr><td>

Selected

</td><td>

Boolean indicating whether the multiple predicted intents shown to end users as matched topics were actually selected by the end users: **true** or **false**.

</td></tr><tr><td>

Shown

</td><td>

Boolean indicating whether the application \(Virtual Agent\) displayed the predicted intent as a choice for the end user to select: **true** or **false**.

</td></tr><tr><td>

Topic Switched

</td><td>

Name of the topic, if the user was prompted for confirmation \(regardless of their choice, yes or no\).

</td></tr><tr><td>

Utterance

</td><td>

Phrase entered by the end user in the chat client window.

</td></tr></tbody>
</table>-   **Open NLU Predict Entity Feedbacks table**

    The Open NLU Predict Entity Feedbacks \[open\_nlu\_predict\_entity\_feedback\] table shows the entity \(slot-filling\) processing that an application \(in this case Virtual Agent\) performs in response to an NLU entity prediction result. For example, the goal of Virtual Agent is to map a predicted NLU entity to a Virtual Agent topic input variable.

    To view the table, enter `open_nlu_predict_entity_feedback.list` in the navigation filter.

<table id="table_u1p_kyx_vjb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

App

</td><td>

Application using NLU. For example, VA \(Virtual Agent\).

</td></tr><tr><td>

App Document

</td><td>

sys\_id of the application record. For example: **sys\_cs\_topic.sys\_id**.

</td></tr><tr><td>

App Document Table

</td><td>

Table of the application record. For example: **sys\_cs\_topic**.

</td></tr><tr><td>

Auto Selected

</td><td>

Boolean indicating whether the application automatically chose to use the entity without notifying the user: **true** or **false**.

</td></tr><tr><td>

External Model Display Name

</td><td>

Name of the external NLU model. For example, the name of the IBM Watson Assistant NLU application.

</td></tr><tr><td>

Mapped

</td><td>

Boolean indicating whether the application \(Virtual Agent\) considered the prediction to be usable: **true** or **false**.

</td></tr><tr><td>

Mapped to

</td><td>

Item in the application that the entity was mapped to.

</td></tr><tr><td>

Model Display Name

</td><td>

Name of the ServiceNow NLU model.

</td></tr><tr><td>

Model ID

</td><td>

ID of the NLU model that the prediction was submitted for.

</td></tr><tr><td>

Model Name

</td><td>

Name of the NLU model that the prediction was submitted for.

</td></tr><tr><td>

Prediction

</td><td>

Name of the predicted entity.

</td></tr><tr><td>

Prediction Audit Log

</td><td>

Reference to the Open NLU Predict Logs \[open\_nlu\_predict\_log\] table.

</td></tr><tr><td>

Prediction Confidence

</td><td>

Confidence value for the prediction.

</td></tr><tr><td>

Selected

</td><td>

Boolean indicating whether the application selected to use the entity: **true** or **false**.

</td></tr><tr><td>

Shown

</td><td>

Boolean indicating whether the application displayed the predicted entity to the end user as a choice to select: **true** or **false**.

</td></tr><tr><td>

Utterance

</td><td>

User phrase entered in the chat client window.

</td></tr><tr><td>

Value

</td><td>

Value of the predicted entity.

</td></tr></tbody>
</table>-   **Open NLU Predict Logs**

    The Open NLU Predict Logs \[open\_nlu\_predict\_log\] table provides a consolidated overview of the NLU prediction records for topics. Each record in the log identifies the utterance and corresponding intents \(topics\) and entities determined by the NLU service. Each record also includes the NLU prediction scores calculated during topic discovery \(intent matching\) and entity extraction.

    **Note:** NLU prediction node logs are generated automatically. If you're using node logs for debugging but you want to suppress the automatic generation of NLU prediction node logs, add the **com.glide.opennlu.predict.node\_logging\_enabled** system property and set the value to false.

    To view the Open NLU Predict Logs, enter `open_nlu_predict_log.list` in the navigation filter.

<table id="table_ns3_fmg_yhb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Async

</td><td>

Indicator for asynchronous prediction processing: **true** or **false**. True indicates that the prediction was performed asynchronously, allowing Virtual Agent worker threads to continue.

</td></tr><tr><td>

Created

</td><td>

Date and time the NLU prediction record was created.

</td></tr><tr><td>

Duration

</td><td>

Length of processing time for the prediction to return intent and entity values.

</td></tr><tr><td>

Language

</td><td>

The language of the NLU prediction request.

</td></tr><tr><td>

Level

</td><td>

Type of message: Information level.

</td></tr><tr><td>

Message

</td><td>

Prediction results returned: number of intents and entities.

</td></tr><tr><td>

Request

</td><td>

NLU prediction parameter that contains the utterance and NLU model for the recognized intent.

</td></tr><tr><td>

Response

</td><td>

NLU prediction results, which contain 0 \(none\) or more scored intents and scored entities.

</td></tr><tr><td>

Source

</td><td>

Process or area: **OpenNLU - Predict**.

</td></tr><tr><td>

Utterance

</td><td>

User statement recognized by the bot, which maps to an intent defined in an NLU model.

</td></tr></tbody>
</table>    **Note:** You can view the detailed intent and entity results in the Open NLU Predict Intent Feedbacks and Open NLU Predict Entity Feedbacks tables.


## Review HTTP connection information for Open NLU integrations

Use the Open NLU Driver HTTP Connection \[open\_nlu\_driver\_http\_connection\] table to quickly check the HTTP credentials, connection details, and methods for the intents, entities, NLU models, and predictions for your NLU service provider.

To view the table, enter `open_nlu_driver_http_connection.list` in the navigation filter.

**Parent Topic:**[Debug a Virtual Agent topic](virtual-agent-troubleshooting-guide.md)

