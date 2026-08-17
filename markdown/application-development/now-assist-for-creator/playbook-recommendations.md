---
title: Playbook recommendations for placeholder activity
description: Get AI-generated recommendations for placeholder activities. The system generates recommendations based on an activity’s name and description.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/now-assist-for-creator/playbook-recommendations.html
release: australia
product: Now Assist for Creator
classification: now-assist-for-creator
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Playbook recommendations, Use generative AI, ServiceNow Otto for Creator, Agentic development on the ServiceNow AI Platform, Building applications]
---

# Playbook recommendations for placeholder activity

Get AI-generated recommendations for placeholder activities. The system generates recommendations based on an activity’s name and description.

\[Omitted video\] Description: Generate a outline and get recommendations for placeholder activities

## Activation

Playbook recommendations is a skill installed with the ServiceNow Otto for Creator \(sn\_now\_creator\) application. You can install this application from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Benefits

The AI recommendations skill searched through all available activity definitions, flows, subflows, and actions on the instance. That enables quicker configuration of placeholder activities in your playbook outline, which then reduces the total time to playbook activation.

## Supported user interfaces

Access the Playbook Recommendations skill from the Playbooks user interface.

\[Omitted image "playbook-recommendation-otto.png"\] Alt text: Sample AI recommendation for placeholder activity.

The AI recommendations skill uses the name and description of the activity to generate one to five recommendations for the activity definition to use for a placeholder activity. If there are no recommendations listed, then no activity definitions are considered relevant to the activity name and description.

The system can only recommend activity definitions, flows, subflows, and actions that are available from ServiceNow. Recommendations can’t include user-created activity definitions, flows, subflows, or actions.

## Generative AI model training

This Generative AI large language model was pre-trained with internal ServiceNow playbooks to learn playbook creation patterns. The goal was to understand what playbook activities are most relevant for a certain position in a playbook given the trigger and previous activities.

## Playbook preference

By default, Workflow Studio shows Playbook recommendations as you configure placeholder activities in a playbook outline. You can hide these recommendations on playbook by playbook basis by turning off the Show recommendations playbook preference. See [User preferences for flows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/flow-preferences.md) for more information.

**Parent Topic:**[Playbook recommendations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/now-assist-for-creator/playbook-recommendations-landing.md)

**Related topics**  


[Generate recommendations for placeholder activities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/now-assist-for-creator/generate-playbook-recommendations.md)

