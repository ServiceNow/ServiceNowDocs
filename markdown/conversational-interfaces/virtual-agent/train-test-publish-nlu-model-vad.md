---
title: Train and test your NLU model in Virtual Agent Designer
description: Use the NLU Intent tab to train and try a Natural Language Understanding \(NLU\) model that is mapped to a topic without leaving Virtual Agent Designer.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Testing NLU/Keyword topics, Getting started with Virtual Agent Designer, Build and deploy, Virtual Agent, Conversational Interfaces]
---

# Train and test your NLU model in Virtual Agent Designer

Use the **NLU Intent** tab to train and try a Natural Language Understanding \(NLU\) model that is mapped to a topic without leaving Virtual Agent Designer.

## Before you begin

Role required: virtual\_agent\_admin or admin

## About this task

As you make changes to a topic's intent, train the model so that your updates are incorporated. Then try and test the model to review prediction results based on the latest changes. Continue to test and refine your model until you're satisfied with your changes.

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Virtual Agent** &gt; **Designer**.

2.  Set the discovery type toggle switch to **NLU/Keyword**.

3.  Open a topic and view the **NLU Intent** tab.

4.  Select **Train model**.

    A message indicates that the model was successfully trained.

5.  Select **Try model**.

    In the Try model panel, manually enter an utterance to test. The prediction results display in the panel.

    ![The Try model panel showing results of testing an utterance manually.](../images/nlu-publish-model.png "Example of testing an utterance in the NLU Try model panel")

    If prediction confidence score results meet or surpass the confidence threshold you established for the model, the results appear under Top prediction\(s\). In this example, the threshold value is 65%.

    The default value of the **com.glide.cs.intent\_confidence\_threshold** property is **0.7**.

    The default value of the **com.glide.cs.entity\_confidence\_threshold** property is **0.5**.

    **Note:** You can compare the draft NLU model to its most recent published version. For more information, see Compare draft and published versions of your NLU model.

6.  When you're satisfied with the prediction results, publish the model from NLU Workbench or select **Publish** in the topic Header bar and select **NLU Model**.


## What to do next

You can publish the model at the same time as the Virtual Agent topic if the model meets publication criteria. Make sure your model has passed through all phases of development and is ready to publish. For more information, see Model management.

For more information on providing feedback using thumbs icons in the results, see Test panel feedback.

**Parent Topic:**[Testing NLU/Keyword topics](../reference/va-designer-testing.md)

