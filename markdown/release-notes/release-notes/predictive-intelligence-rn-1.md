---
title: Predictive Intelligence release notes
description: The ServiceNow Predictive Intelligence application enables you to create and train machine learning models to help improve the performance, efficiency, and flexibility of your systems. Predictive Intelligence was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-07-27"
reading_time_minutes: 1
---

# Predictive Intelligence release notes

The ServiceNow® Predictive Intelligence application enables you to create and train machine learning models to help improve the performance, efficiency, and flexibility of your systems. Predictive Intelligence was enhanced and updated in the Australia release.

## Predictive Intelligence highlights for the Australia release

-   A new Predictive Intelligence Usage Analytics dashboard provides you with actionable insights into model performance, user engagement, adoption trends, and product health.
-   The sys property ML Trainer - Glide communication KAA \(glide.platform\_ml.kaa\_auth\_enabled\) implements KAA validation when mTLS is enabled.

See [Predictive Intelligence](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/predictive-intelligence-landing.md) for more information.

## New in the Australia release

-   **[Predictive Intelligence Usage Analytics dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/predictive-intel-usage-analytics.md)**

    Usage Analytics dashboard is a central location to understand the adoption, effectiveness, and overall value of all your Predictive Intelligence solutions. Dashboard widgets offer several metrics such as total monthly count of predictions per solution type.

-   **Sys property: [ML Trainer - Glide communication KAA](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/predictive-intelligence-properties.md)**

    A sys property \(glide.platform\_ml.kaa\_auth\_enabled\) implements KAA validation to the ML Trainer server. KAA validation occurs only if mTLS is enabled on the instance. If this property is enabled but mTLS isn't enabled, the KAA validation is skipped. Default value is true \(from the Australia release\).


## Activation information

Predictive Intelligence is a ServiceNow AI Platform feature that is active by default.

## Related ServiceNow applications and features

-   **[Now Assist in Document Intelligence \(Legacy\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/docintel-nowassist-landing.md)**

    With the Now Assist in Document Intelligence application, you can use generative AI to get key information from digital documents into your automation workflows.

-   **[Task Intelligence](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/task-intelligence.md)**

    Task Intelligence uses machine learning to train solutions with your data and achieve important outcomes.

-   **[ServiceNow® apps and features that use Predictive Intelligence](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/servicenow-apps-features-use-predictive-intelligence.md)**

    Prebuilt Predictive Intelligence solutions tailored to specific BUs are available in apps across the ServiceNow AI Platform.


