---
title: Exploring Playbook recommendations
description: Get AI-generated recommendations for placeholder activities. The system generates recommendations based on an activity’s name and description.
locale: en-US
release: zurich
product: Now Assist for Creator
classification: now-assist-for-creator
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Playbook recommendations, Now Assist for Creator, Build workflows]
---

# Exploring Playbook recommendations

Get AI-generated recommendations for placeholder activities. The system generates recommendations based on an activity’s name and description.

Generate a outline and get recommendations for placeholder activities 

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

