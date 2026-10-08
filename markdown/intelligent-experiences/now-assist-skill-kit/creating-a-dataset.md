---
title: Dataset guidelines for AI Skill Kit
description: A representative, appropriately sized, and isolated dataset gives you a reliable measure of how your skill prompt performs.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/now-assist-skill-kit/creating-a-dataset.html
release: brazil
product: Now Assist Skill Kit
classification: now-assist-skill-kit
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [General guidelines for AI Skill Kit, Exploring AI Skill Kit, AI Skill Kit, Generative AI skills, Enable AI Experiences]
---

# Dataset guidelines for AI Skill Kit

A representative, appropriately sized, and isolated dataset gives you a reliable measure of how your skill prompt performs.

## AI Skill Kit dataset creation

A data-driven approach to skill development relies on the collection of a high-quality dataset to develop and test the skill. When you use AI Skill Kit, you can also use the existing capabilities of the ServiceNow AI Platform to create a high-quality dataset.

When collecting data for this purpose, create datasets that are:

1.  Representative of the skill’s intended deployment environment. The data should:
    -   Seek to reflect the expected distribution of inputs in the deployment environment.
    -   Capture variance along several identified axes, for example, input length, urgency.
    -   Include any examples of inputs that are known to be important to the use case.
    -   Consider edge cases that might be rare but are suspected to cause problems, for example, long inputs.
2.  Sized appropriately for the team’s risk appetite.
    -   It’s possible to develop and deploy a skill with little data. However, a lack of data creates more uncertainty about how the skill performs in deployment.
    -   Produce confidence intervals for any associated performance scores and prompt comparisons.
3.  Isolated from the data used for developing and writing the prompts.
    -   Split the collected data into development and testing sets so that some data is reserved for evaluation.
    -   If you use all the data during the process of developing the prompt, your final evaluation of the skill is biased, meaning that it over-reports performance. This bias is because of a phenomenon known as prompt overfitting.

