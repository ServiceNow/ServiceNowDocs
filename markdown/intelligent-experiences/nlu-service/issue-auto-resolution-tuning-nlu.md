---
title: Issue Auto Resolution Tuning in NLU
description: Use the NLU Workbench homepage to support Issue Auto Resolution \(IAR\) tuning in NLU.
locale: en-US
release: yokohama
product: NLU Service
classification: nlu-service
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [NLU Workbench - Advanced Features, Natural Language Understanding, Enable AI experiences]
---

# Issue Auto Resolution Tuning in NLU

Use the NLU Workbench homepage to support Issue Auto Resolution \(IAR\) tuning in NLU.

A video introducing Issue Auto Resolution tuning in the NLU Workbench

## Summary usage and roles

Use the nlu\_admin or admin role to access IAR Tuning in the NLU Workbench. IAR Tuning in the NLU Workbench requires at least the nlu\_feedback\_admin role. Note that the nlu\_admin role contains the nlu\_feedback\_admin role. Also, the virtual\_agent\_admin role contains the nlu\_admin role.

If you click on the IAR model name, you will be taken straight to tuning, in the product. You will not be taken to a model overview page, so this behavior differs from Virtual Agent or AI Search models in the NLU Workbench.

## The IAR Tuning workflow

IAR admins begin their model tuning journey in the IAR Admin Console, and then land in the NLU Workbench to tune their ITSM model. If they haven't trained the ITSM model in the console yet, the workflow sends them to the Expert Feedback Loop documentation under the **Boost your model performance** section of the NLU Workbench.

## How IAR models differ from NLU models

Unlike the Virtual Agent and AI Search tabs, the IAR tab doesn't use a Create new model button. The IAR-ITSM model that IAR admins use is a prebuilt model. IAR models can't be moved using update sets.

## Exploring the NLU Workbench

![The NLU Workbench homepage opens in the Virtual Agent tab by default.](../images/issue-auto-resolution-tuning-nlu2.png)

At the top of the NLU Workbench page are three tabs that group Virtual Agent, Issue Auto Resolution, and AI Search models separately. Below those tabs are a list of models colored grey. In the Model column of the list, if you click the caret to the left of the model name, the model changes color from grey to white and opens to show the model's languages; status; usage; model type; number of enabled intents and mapped intents and the date when the model was last modified or last published.

-   **[Issue Auto Resolution tuning options](issue-auto-resolution-tuning-options.md)**  
When you are tuning your Issue Auto Resolution model in NLU Workbench, you can adjust the output for several goals: precision, automation, or a balance of the two. Compare how your choice of tuning options affect match rate and coverage, before committing.

**Parent Topic:**[NLU Workbench - Advanced Features](nlu-workbench-advanced-features.md)

