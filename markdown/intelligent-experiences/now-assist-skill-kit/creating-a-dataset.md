---
title: Creating a dataset using Now Assist Skill Kit
description: Use these guidelines to create an effective dataset. Having an effective dataset provides better results for your prompt.
locale: en-US
release: xanadu
product: Now Assist Skill Kit
classification: now-assist-skill-kit
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [General guidelines for Now Assist Skill Kit, Exploring Now Assist Skill Kit, Now Assist Skill Kit, Enable AI experiences]
---

# Creating a dataset using Now Assist Skill Kit

Use these guidelines to create an effective dataset. Having an effective dataset provides better results for your prompt.

## Now Assist Skill Kit dataset creation overview

A data-driven approach to skill development relies on the collection of a high-quality dataset to develop and test the skill. When you use Now Assist Skill Kit, you can also leverage the existing capabilities of the ServiceNow AI Platform to create a high-quality dataset.

When collecting data for this purpose, you should aim to create datasets that are:

1.  Representative of the skill’s intended deployment environment. The data should:
    -   Seek to reflect the expected distribution of inputs in the deployment environment.
    -   Capture variance along several identified axes, for example, input length, urgency.
    -   Include any examples of inputs that are known to be important to the use case.
    -   Consider edge cases \(which may be rare\) but that are suspected to cause problems, for example, long examples.
2.  Sized appropriately for the team’s risk appetite.
    -   It’s possible to develop and deploy a skill with little data. However, a lack of data creates more uncertainty about how the skill performs in deployment.
    -   You should think like statisticians and produce confidence intervals for any associated performance scores and prompt comparisons.
3.  Isolated from the data used for developing and writing the prompts.
    -   You should split the data collected into development and testing sets. By splitting the data, you are protecting some data solely for evaluation purposes.
    -   If you use all the data during the process of developing the prompt, your final evaluation of the skill is biased, meaning that it over-reports performance. This bias is because of a phenomenon known as prompt overfitting.

