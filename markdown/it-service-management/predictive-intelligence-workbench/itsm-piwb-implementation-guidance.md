---
title: ITSM Predictive Intelligence Workbench implementation
description: Use machine learning to optimize your business processes. You can train and implement ITSM Predictive Intelligence Workbench use case models to augment your existing application workflows.
locale: en-US
release: yokohama
product: Predictive Intelligence Workbench
classification: predictive-intelligence-workbench
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [ITSM Predictive Intelligence Workbench, IT Service Management]
---

# ITSM Predictive Intelligence Workbench implementation

Use machine learning to optimize your business processes. You can train and implement ITSM Predictive Intelligence Workbench use case models to augment your existing application workflows.

**Important:**

Starting with the yokohama release, the ITSM Predictive Intelligence Workbench will reach its end of life \(EOL\) as part of its deprecation process. It will be completely deprecated and no longer deployed, enhanced, or supported from the yokohama release. To get the latest experience for this functionality, you must install the Task Intelligence for ITSM application \(com.snc.itsm\_ml\_task\) plugin. For more information, see [Task Intelligence for ITSM](../../task-intelligence-for-itsm/concept/c-itsm-task-intelligence.md)

For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184) article in the Now Support Knowledge Base.

## Explore use case templates

Users with the piwb\_admin or piwb\_manager role can explore the prebuilt use case templates and create predictive machine learning models. To create a machine learning model, you first select a prebuilt use case template. Some of the prebuilt templates are guided and display the **Guided Setup** flag. These templates include a comprehensive setup process to help ease you through implementation. Non-guided templates display the **Classic Setup** flag.

![ITSM Predictive Intelligence Workbench guided use case template](../image/ITSMPIWBUseCaseTemplateGuidedSetup.png "ITSM Predictive Intelligence Workbench guided use case template")

![ITSM Predictive Intelligence Workbench classic setup use case template](../image/ITSMPIWBUseCaseTemplateClassicSetup.png "ITSM Predictive Intelligence Workbench classic setup use case template")

Templates with available pretrained models accelerate your setup process, by providing a pre-generated model based on your data. When a template indicates **Pretrained**, this means you can go directly to the evaluation phase of the use case setup. If the pretrained model is acceptable, you can directly integrate it with your business processes. Otherwise, you can tune this model or create another model. You may change the name and description of the use case later. Pretrained models display the estimated percentage of your correctly predicted incidents.

Templates with available pretrained models also display the estimated percentage of the correctly predicted incidents. If the pretrained model is acceptable, you can directly integrate it with your business processes. Otherwise, you can tune this model or create another model. You may change the name and description of the use case later. Pretrained models display the estimated percentage of your correctly predicted incidents.

![ITSM Predictive Intelligence Workbench pretrained model use case template](../image/ITSMPIWBPretrainedModel.png "ITSM Predictive Intelligence Workbench pretrained model use case template")

Non-guided, **Classic Setup** templates provide links to relevant Predictive Intelligence Workbench product documentation or link to the ServiceNow platform Predictive Intelligence application with the **Take me there**button.

![ITSM Predictive Intelligence Workbench links to product documentation and Predictive Intelligence product documentation](../image/ITSMPIWBLinksProductDoc.png "ITSM Predictive Intelligence Workbench links to product documentation and Predictive Intelligence product documentation")

## Use case creation phases

Creating a predictive machine learning model involves several phases. After you create and train your model you need to evaluate and tune it, test its prediction results, and then integrate it with your business process. Use case model creation phases include:

-   Create and train models: Define parameters to create a model that you will train based on your unique data. It is common to create multiple models in this phase. You will tune and refine your models by defining the right combination of coverage and precision to use.
-   Test your models: Get prediction results from your models to decide which one is best to integrate with your business process. To see if a model returns a correct result, you can use either the single or batch testing process.
-   Integrate the best model: Deploy the best model into your business process. After you determine which model returns the best, correct result, integrate it into production.

    **Note:** For details regarding trained use case integration implementation, refer to [Predictive Intelligence Workbench integration and customization](itsm-piwb-integ-implem-custom.md).


