---
title: Legacy - Modify models
description: Test and modify the Virtual Agent models so they more accurately predict user intents.
locale: en-US
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Legacy - Natural Language Understanding of Virtual Agent responses, Legacy - Using the Conversational Analytics Dashboard, Legacy - Conversational Analytics Dashboard, Analyzing Virtual Agent performance, Virtual Agent, Conversational Interfaces]
---

# Legacy - Modify models

Test and modify the Virtual Agent models so they more accurately predict user intents.

## Before you begin

**Important:**

Conversational Analytics dashboard is being prepared for future deprecation. It will be supported until deprecation but will no longer be available for installation. A new Conversational Analytics dashboard in Platform Analytics experience, which meets the compliance requirements of Government Community Cloud \(GCC\), and thus FedRAMP authorized, is available. See [Conversational Analytics dashboard in Platform Analytics experience](../concept/VA-dashboard-landing-page-pae.md).

For details on the deprecation process, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

If you are an existing user of this dashboard and want to migrate analytics data to the new dashboard, see [Migrate data to Conversational Analytics dashboard in Platform Analytics experience \[KB1651556\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1651556).

Role required: Chat Analytics Admin

## About this task

Many ServiceNow products, such as ITSM, HRSD, and CSM include NLU models for Virtual Agent \(VA\) topics. The NLU plugin contains entities that are common across all products. You can modify those models. To learn how to train and test the models used for VA conversations, see [Natural Language Understanding](https://www.servicenow.com/docs/access?context=nlu-landing&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).

## Procedure

1.  Navigate to **All** &gt; **Conversational Analytics** &gt; **Dashboard** and select the **NLU Prediction** tab.

2.  Select **View more**.

    The Models page opens that displays the models that predict intents in your setup.

    ![NLU Workbench dashboard list of NLU models.](../images/dashboard-list-of-models-2.png)

3.  If none of the models contain intents and utterances you'd like in your setup, select **Create Model** and follow the instructions in [Create an NLU model](https://www.servicenow.com/docs/access?context=create-nlu-modelx&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).

4.  Click a model to display the intents the model predicts.

    ![NLU Workbench Model Intents tab.](../images/dashboard-model-intents.png)

5.  Click an intent to display the utterances associated with it.

    ![NLU Workbench Intent utterances tab.](../images/dashboard-intents-utterances.png)

6.  To create a new intent and add it to the model:

    1.  Select **New Intent**.

        The **Create a new intent** dialog box opens.

    2.  Enter the name of the new intent in **Intent Name**, a description of it in the **Description** field, and select **Save**.

        A page for your new intent opens.

        ![NLU Workbench intent utterances tab showing utterance added.](../images/dashboard-intent-added.png)

    3.  Enter an utterance for your new intent and select **Add**.

        You can repeat this step multiple times to add multiple utterances.

7.  Import one or more intents by selecting **Import Intents**.

    The **Import Intents** dialog box opens, which displays the intents you can import.![Import intents dialog box with SubmitRequest intent selected.](../images/dashboard-import-intents.png)

    1.  Find the intent\(s\) to import by entering a search term, or by clicking an arrowhead to display the intents in a folder, and then selecting one or more check boxes.
    2.  Select **Import**.
8.  If you added or imported intents:

    1.  Select **Train** to add the intents to the model.

    2.  Select **Train** to train the model.

        If successful, a banner at the top reads, **The model has been successfully trained.**

9.  To test all the utterances, select **Test** and enter a sentence a user might enter in a chat to see if NLU understands the intent of your sentence.

    ![NLU Workbench Intents tab and Test model tab displaying test utterance.](../images/dashboard-test-utterance.png)

10. If the models fail to predict the intent, add additional intents to the model, or utterances to the intents, as described in step 6.


**Parent Topic:**[Legacy - Natural Language Understanding of Virtual Agent responses](../concept/nlu-tab.md)

