---
title: Playbook recommendations
description: Get AI-generated recommendations for placeholder activities. The system generates recommendations based on an activity’s name and description.Select the activity definition for a placeholder activity from a list of AI-generated recommendations. The system generates recommendations based on an activity’s name and description.
locale: en-US
release: yokohama
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Playbook Assist, Exploring playbooks, Exploring Workflow Studio, Workflow Studio, Build workflows]
---

# Playbook recommendations

Get AI-generated recommendations for placeholder activities. The system generates recommendations based on an activity’s name and description.

Generate a playbook outline and get recommendations for placeholder activities 

## Activation

Now Assist Recommendations is a skill installed with the Now Assist for Creator \(sn\_now\_creator\) application. You can install this application from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Benefits

Activating the Now Assist Recommendations skill helps to search through all available activity definitions, flows, subflows, and actions on the instance, which enables quicker configuration of placeholder activities in your playbook outline, which then reduces the total time to playbook activation.

## Supported user interfaces

Access the Now Assist Recommendations skill from the Playbooks user interface.

![Five sample playbook recommendations for a placeholder activity](../images/playbook-recommendations.png "Example Now Assist recommendations")

The Now Assist Recommendations skill uses the name and description of the activity to generate one to five recommendations for the activity definition to use for a placeholder activity. If there are no recommendations listed, then no activity definitions are considered relevant to the activity name and description.

## Generative AI model training

This Generative AI large language model was pre-trained with internal ServiceNow playbooks to learn playbook creation patterns. The goal was to understand what playbook activities are most relevant for a certain position in a playbook given the trigger and previous activities.

## AI limitations

This application uses artificial intelligence \(AI\) and machine learning, which are rapidly evolving fields of study that generate predictions based on patterns in data. As a result, this application may not always produce accurate, complete, or appropriate information. Furthermore, there is no guarantee that this application has been fully trained or tested for your use case. To mitigate these issues, it is your responsibility to test and evaluate your use of this application for accuracy, harm, and appropriateness for your use case, employ human oversight of output, and refrain from relying solely on AI-generated outputs for decision-making purposes. This is especially important if you choose to deploy this application in areas with consequential impacts such as healthcare, finance, legal, employment, security, or infrastructure. You agree to abide by [ServiceNow’s AI Acceptable Use Policy](https://www.servicenow.com/ai-acceptable-use-policy.html), which may be updated by ServiceNow.

**Parent Topic:**[Playbook Assist](playbook-assist-landing.md)

## Generate playbook recommendations

Select the activity definition for a placeholder activity from a list of AI-generated recommendations. The system generates recommendations based on an activity’s name and description.

### Before you begin

-   Make sure the playbook recommendations skill is turned on. To learn how to turn on the recommendations skill for playbooks, see [Turn on playbook recommendations](../task/turn-on-playbook-recommendations.md).
-   You can only generate recommendations for placeholder activities in a generated playbook outline. To learn how to generate a playbook outline, see [Generate a playbook](../task/generate-a-playbook-outline.md).
-   Role required:
    -   admin, playbook.admin, pd\_author, or a delegated developer permission
    -   now.assist.creator

### Procedure

1.  In your playbook outline, hover over the placeholder activity and select the recommendations icon \(![Now Recommendations icon](../images/recommendations-icon.png)\) in the mini-picker.

2.  Select one of the recommended activity definitions, if appropriate.

    **Note:** If there are no recommendations listed, then no activity definitions are considered relevant to the activity name and description.

3.  Try updating the **Label** and **Description** to improve results.

    1.  Open the placeholder activity.

    2.  Update the **Label** and **Description**.

    3.  Under the **Activity definition** field, select the recommendations button \(![Recommendations button](../images/now-recommendations-button.png)\) to try to generate recommendations again.

    4.  Select one of the recommended activity definitions, if appropriate.

4.  Continue on with activity configuration from Step [11.e](../task/generate-a-playbook-outline.md#configure-activity-inputs) of the [Generate a playbook](../task/generate-a-playbook-outline.md) procedure.


### Result

When your playbook's trigger conditions are met, your playbook runs. As a result, the system creates a Process Execution record and renders user-facing configurations for Playbook Experience. For an example of how to digitize a manual business process that renders as a playbook, see [Design an automated process](../task/design-automated-process.md).

### What to do next

Design the Playbook Experience for your agents and fulfillers in UI Builder. To learn how to design and customize the runtime playbook experience in UI Builder, see [Customize the Playbook Experience](../../workspace/concept/playbook-customize-playbook.md).

