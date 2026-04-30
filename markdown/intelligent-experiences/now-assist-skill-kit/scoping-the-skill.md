---
title: Scoping the skill
description: Scoping the skill before you build it helps determine the requirements needed for the skill and the expected outcomes.
locale: en-US
release: zurich
product: Now Assist Skill Kit
classification: now-assist-skill-kit
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [General guidelines for Now Assist Skill Kit, Exploring Now Assist Skill Kit, Now Assist Skill Kit, Enable AI experiences]
---

# Scoping the skill

Scoping the skill before you build it helps determine the requirements needed for the skill and the expected outcomes.

## Before you begin

Before you start to build a custom skill with Now Assist Skill Kit, you should first review the base system skills that are available in the Now Assist Admin console. Use these pre-existing skills whenever possible.

## User prerequisites

Now Assist Skill Kit is meant to be used by a developer or someone with experience using generative AI. Because you must write the initial prompt template, you should:

1.  Be knowledgeable about prompt engineering, including:
    -   Having familiarity with the development and testing of machine learning systems.
    -   Having informed expectations about the behavior and capabilities of a prompted large language model \(LLM\). You should understand:
        -   The fundamentally probabilistic nature of LLMs.
        -   That performance can vary greatly across different LLMs and different target tasks.
    -   Having experience or training with writing and evaluating prompts for LLMs.
2.  Have an in-depth understanding of the use case that they’re trying to solve and the persona that they’re building the skill for.

## Design

Before you begin building a custom skill, you must think about the overall design and document the requirements. Consider the following:

1.  What precisely do you want the skill to do?
    -   What will be the inputs to the model?
    -   What should be the outputs of the model? \(Both content and format\)
    -   Who will be using the skill?
    -   How can you characterize success?
2.  What don't you want the model to do?
    -   It’s useful to think about the possible risks and downsides of using generative AI outputs so that you can try to guard against them during development and testing.
    -   It’s worth listing any specific model behaviors \(LLM outputs\) that would be detrimental or harmful in your specific use case.

