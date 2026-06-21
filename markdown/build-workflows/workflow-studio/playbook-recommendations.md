---
title: Playbook recommendations
description: Get AI-generated recommendations for placeholder activities. The system generates recommendations based on an activity’s name and description.Select the activity definition for a placeholder activity from a list of AI-generated recommendations. The system generates recommendations based on an activity’s name and description.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/build-workflows/workflow-studio/playbook-recommendations.html
release: yokohama
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Playbook generation, Exploring playbooks, Exploring Workflow Studio, Workflow Studio, Build workflows]
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

\[Omitted image "playbook-recommendations.png"\] Alt text: Five sample playbook recommendations for a placeholder activity

The Now Assist Recommendations skill uses the name and description of the activity to generate one to five recommendations for the activity definition to use for a placeholder activity. If there are no recommendations listed, then no activity definitions are considered relevant to the activity name and description.

The system can only recommend activity definitions, flows, subflows, and actions that are available from ServiceNow. Recommendations can’t include user-created activity definitions, flows, subflows, or actions.

## Generative AI model training

This Generative AI large language model was pre-trained with internal ServiceNow playbooks to learn playbook creation patterns. The goal was to understand what playbook activities are most relevant for a certain position in a playbook given the trigger and previous activities.

## Playbook preference

By default, Workflow Studio shows playbook recommendations as you configure placeholder activities in a playbook outline. You can hide these recommendations on playbook by playbook basis by turning off the Show recommendations playbook preference. See [User preferences for flows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/build-workflows/workflow-studio/flow-preferences.md) for more information.

## AI limitations

This application uses artificial intelligence \(AI\) and machine learning, which are rapidly evolving fields of study that generate predictions based on patterns in data. As a result, this application may not always produce accurate, complete, or appropriate information. Furthermore, there is no guarantee that this application has been fully trained or tested for your use case. To mitigate these issues, it is your responsibility to test and evaluate your use of this application for accuracy, harm, and appropriateness for your use case, employ human oversight of output, and refrain from relying solely on AI-generated outputs for decision-making purposes. This is especially important if you choose to deploy this application in areas with consequential impacts such as healthcare, finance, legal, employment, security, or infrastructure. You agree to abide by [ServiceNow’s AI Acceptable Use Policy](https://www.servicenow.com/ai-acceptable-use-policy.html), which may be updated by ServiceNow.

**Parent Topic:**[Playbook generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/build-workflows/workflow-studio/playbook-assist-landing.md)

## Generate playbook recommendations

Select the activity definition for a placeholder activity from a list of AI-generated recommendations. The system generates recommendations based on an activity’s name and description.

### Before you begin

-   Make sure the playbook recommendations skill is turned on. To learn how to turn on the recommendations skill for playbooks, see [Turn on playbook recommendations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/build-workflows/workflow-studio/turn-on-playbook-recommendations.md).
-   You can only generate recommendations for placeholder activities in a generated playbook outline. To learn how to generate a playbook outline, see [Generate a playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/build-workflows/workflow-studio/generate-a-playbook-outline.md).
-   Role required:
    -   admin, playbook.admin, pd\_author, or a delegated developer permission
    -   now.assist.creator

### Procedure

1.  In your playbook outline, hover over the placeholder activity and select the recommendations icon \(\[Omitted image "recommendations-icon.png"\] Alt text: Now Recommendations icon\) in the mini-picker.

2.  Select one of the recommended activity definitions, if appropriate.

    **Note:** If there are no recommendations listed, then no activity definitions are considered relevant to the activity name and description.

3.  Try updating the **Label** and **Description** to improve results.

    1.  Open the placeholder activity.

    2.  Update the **Label** and **Description**.

    3.  Under the **Activity definition** field, select the recommendations button \(\[Omitted image "now-recommendations-button.png"\] Alt text: Recommendations button\) to try to generate recommendations again.

    4.  Select one of the recommended activity definitions, if appropriate.

4.  Continue on with activity configuration from Step [8.e](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/build-workflows/workflow-studio/generate-a-playbook-outline.md) of the [Generate a playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/build-workflows/workflow-studio/generate-a-playbook-outline.md) procedure.


### Result

When your playbook's trigger conditions are met, your playbook runs. As a result, the system creates a Process Execution record and renders user-facing configurations for Playbook Experience. For an example of how to digitize a manual business process that renders as a playbook, see [Design an automated process](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/build-workflows/workflow-studio/design-automated-process.md).

### What to do next

Design the Playbook Experience for your agents and fulfillers in UI Builder. To learn how to design and customize the runtime playbook experience in UI Builder, see [Customize the Playbook Experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/build-workflows/workflow-studio/playbook-customize-playbook.md).

