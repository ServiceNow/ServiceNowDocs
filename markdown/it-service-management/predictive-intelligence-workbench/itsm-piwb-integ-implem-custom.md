---
title: Predictive Intelligence Workbench integration and customization
description: Predictive Intelligence Workbench uses scripted extension points to integrate a trained use case model for prediction.
locale: en-US
release: xanadu
product: Predictive Intelligence Workbench
classification: predictive-intelligence-workbench
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [ITSM Predictive Intelligence Workbench, IT Service Management]
---

# Predictive Intelligence Workbench integration and customization

Predictive Intelligence Workbench uses scripted extension points to integrate a trained use case model for prediction.

**Important:**

Starting with the Xanadu release, ITSM Predictive Intelligence Workbench is being prepared for future deprecation. It will be completed deprecated and will no longer be supported from the **Yokohama** release. To get the latest experience for this functionality, you must install the Task Intelligence for ITSM application \(com.snc.itsm\_ml\_task\) plugin. For more information, see [Task Intelligence for ITSM](../../task-intelligence-for-itsm/concept/c-itsm-task-intelligence.md)

For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184) article in the Now Support Knowledge Base.

## Scripted extension points for trained use case integration implementation

The scripted extension point is PIWBPredictionProcessor​ and PIWBPredictionProcessor\_incident​ is the default implementation of PIWBPredictionProcessor​​ for the Incident \[incident\] table. PIWBPredictionProcessor\_incident​ runs all the predictions for integrated incident-related use case models.

## Customizing default implementation

If you want to customize the default implementation, you can modify the PIWBPredictionProcessor\_incident​ script. The business rule **PIWB Prediction – Incident** on the Incident table calls the PIWBPredictionProcessor\_incident​ script for predictions. For details about scripted extension points, refer to [Using extension points to extend application functionality](https://www.servicenow.com/docs/access?context=extension-points&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US).

