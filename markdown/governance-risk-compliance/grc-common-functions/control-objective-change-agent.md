---
title: Control Objective Change Agent
description: Learn how Control Objective Change Agent automates and streamlines updates to control objectives, ensuring compliance data remains accurate and consistent with user oversight.
locale: en-US
release: yokohama
product: GRC Common Functions
classification: grc-common-functions
topic_type: concept
last_updated: "2025-11-19"
reading_time_minutes: 1
breadcrumb: [Explore, Now Assist, Common GRC features, Governance, Risk, and Compliance]
---

# Control Objective Change Agent

Learn how Control Objective Change Agent automates and streamlines updates to control objectives, ensuring compliance data remains accurate and consistent with user oversight.

When a citation is updated, such as changes in security guidelines or regulatory requirements, associated control objectives must also reflect those changes to maintain compliance accuracy.

Control Objective Change Agent is an AI agent that automates this process. It works with the Control Objective Impact Analyzer skill to identify impacted control objectives and uses the Now Assist panel analyzes citation changes, suggest updates, accepts feedback from the user, and finalizes changes.

This agent supports multiple Large Language Model \(LLM\) providers, such as Azure OpenAI, Google Gemini, Claude, and LTS.

## How the AI agent works

Control Objective Change Agent refines control objective details through the following process:

1.  Impact detection: The process begins when the Control objective impact analyzer skill identifies control objectives that are affected by the citation changes.

    After reviewing the impacted control objectives, users can trigger the Control objective change agent to update descriptions and guidance as required.

2.  Control objective details update: The AI agent monitors these impacted objectives and validates whether updates are truly required. Using the Control Objective Details Updater skill, the agent fetches and applies updated descriptions and supplemental guidance to the relevant control objectives. It intelligently considers all associated citations while filtering out irrelevant details to ensure precise updates.
3.  User feedback and refinement: An interactive Now Assist panel \(NAP\) provides a feedback loop. Users can review the AI-generated suggestions and:
    -   Accept the proposed updates.
    -   Add or remove specific details.

## Benefits

The Control Objective Change Agent refines control objective updates through the following process: offers the following benefits:

-   Automates the process of updating control objective descriptions and supplemental guidance based on changes detected in related citations.
-   Significantly reduces manual effort and enhances accuracy through AI-driven suggestions combined with user feedback loops.

