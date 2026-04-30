---
title: Predictive Intelligence Workbench pretrained use cases
description: The pretrain functionality mechanism for use cases enables and trains the machine learning solution definition when you activate the Predictive Intelligence Workbench application.
locale: en-US
release: yokohama
product: Predictive Intelligence Workbench
classification: predictive-intelligence-workbench
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [ITSM Predictive Intelligence Workbench, IT Service Management]
---

# Predictive Intelligence Workbench pretrained use cases

The pretrain functionality mechanism for use cases enables and trains the machine learning solution definition when you activate the Predictive Intelligence Workbench application.

**Important:**

Starting with the yokohama release, the ITSM Predictive Intelligence Workbench will reach its end of life \(EOL\) as part of its deprecation process. It will be completely deprecated and no longer deployed, enhanced, or supported from the yokohama release. To get the latest experience for this functionality, you must install the Task Intelligence for ITSM application \(com.snc.itsm\_ml\_task\) plugin. For more information, see [Task Intelligence for ITSM](../../task-intelligence-for-itsm/concept/c-itsm-task-intelligence.md)

For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184) article in the Now Support Knowledge Base.

When a pretrained machine learning solution exists in the system, Predictive Intelligence Workbench highlights the use case templates with the **Pretrained** flag.

![ITSM Predictive Intelligence Workbench pretrained model use case template](../image/ITSMPIWBPretrainedModel.png "ITSM Predictive Intelligence Workbench pretrained model use case template")

The **Pretrained** flag for use case templates displays when the following criteria are met.

-   The Predictive Intelligence Workbench **piwb.instance\_eligible\_auto\_train** system property for pretraining is enabled \(true\) on the your instance. This property is disabled by default. Requires the piwb\_admin role to enable.
-   The instance has to be one of the following types:
    -   ded-prod
    -   shared-prod
    -   ded-subprod
    -   shared-subprod
-   The associated machine learning solution is active and ready for deployment.
-   The use case template does not contain an existing pretrained use case.
-   The machine learning solution net automation is greater than the threshold value.

    **Note:** The default base-system threshold value is 30. You can configure this value via the Predictive Intelligence Workbench **piwb.auto\_train\_threshold** system property for. Requires the piwb\_admin role to modify the default value.

-   The machine learning solution is a pretrained base-system solution with an associated record for its definition in the ML Auto Train Solution \[ml\_autotrain\_solution\] table.

