---
title: Exploring Flow recommendations
description: Select the next component in your flow from a list of AI-generated recommendations. The system generates recommendations based on the current position in the flow and the flow component names listed before.
locale: en-US
release: yokohama
product: Now Assist for Creator
classification: now-assist-for-creator
topic_type: concept
last_updated: "2025-08-07"
reading_time_minutes: 2
breadcrumb: [Flow recommendations, Now Assist for Creator, Build workflows]
---

# Exploring Flow recommendations

Select the next component in your flow from a list of AI-generated recommendations. The system generates recommendations based on the current position in the flow and the flow component names listed before.

![Five sample Flow recommendations for an empty flow](../images/flow-recommendations-01.png "Example flow recommendations")

The model uses the name of the flow components that come before to generate one to five recommendations for the next step of the flow. If there are no recommendations listed, then there are no flow components that meet the required relevance threshold.

The system can only recommend actions, flow logic, and subflows that are available from ServiceNow. Recommendations can’t include user-generated flow components such as custom actions, nor can recommendations include actions from ServiceNow Store spokes.

## Generative AI model training

This Generative AI large language model was pre-trained with internal ServiceNow flows to learn flow creation patterns. The goal was to understand what flow components are most relevant for a certain position in a flow given the content before.

## Flow preference

![Flow preference to show recommendations](../images/flow-recommendations-preference.png "Flow preferences")

By default, Workflow Studio shows flow recommendations as you build a flow. You can hide these recommendations on a flow by flow basis by turning off the Show recommendations flow preference. See [User preferences for flows](../reference/flow-preferences.md) for more information.

## Recommendations in diagramming view

![image.flow-recommendations-diagramming-view]

Workflow Studio shows recommendations from the flow diagramming view while you're editing a flow. In diagramming view, the last node of the flow always shows a list of recommendations. This experience matches the behavior of the text view, which also always shows a list of recommendations at the end of the flow.

## AI limitations

This application uses artificial intelligence \(AI\) and machine learning, which are rapidly evolving fields of study that generate predictions based on patterns in data. As a result, this application may not always produce accurate, complete, or appropriate information. Furthermore, there is no guarantee that this application has been fully trained or tested for your use case. To mitigate these issues, it is your responsibility to test and evaluate your use of this application for accuracy, harm, and appropriateness for your use case, employ human oversight of output, and refrain from relying solely on AI-generated outputs for decision-making purposes. This is especially important if you choose to deploy this application in areas with consequential impacts such as healthcare, finance, legal, employment, security, or infrastructure. You agree to abide by [ServiceNow’s AI Acceptable Use Policy](https://www.servicenow.com/ai-acceptable-use-policy.html), which may be updated by ServiceNow.

