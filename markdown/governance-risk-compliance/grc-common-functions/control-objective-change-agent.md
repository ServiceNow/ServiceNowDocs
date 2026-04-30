---
title: Control objective change agent
description: Learn how the control objective change agent automates and streamlines updates to control objectives, confirming that compliance data remains accurate and consistent with user oversight.
locale: en-US
release: zurich
product: GRC Common Functions
classification: grc-common-functions
topic_type: concept
last_updated: "2025-11-19"
reading_time_minutes: 1
breadcrumb: [Explore, Now Assist, Common GRC features, Governance, Risk, and Compliance]
---

# Control objective change agent

Learn how the control objective change agent automates and streamlines updates to control objectives, confirming that compliance data remains accurate and consistent with user oversight.

When a citation is updated, such as changes in security guidelines or regulatory requirements, associated control objectives must also reflect those changes to maintain compliance accuracy.

The control objective change agent is an AI agent that automates this process. It works with the control objective impact analyzer skill to identify impacted control objectives and uses the Now Assist panel to analyze citation changes, suggest updates, accepts feedback from the user, and finalize changes.

This agent supports multiple large language model \(LLM\) providers, such as Azure OpenAI, Google Gemini, Claude, and LTS.

## How the AI agent works

The control objective change agent refines control objective details through the following process:

1.  Impact detection: The process begins when the control objective impact analyzer skill identifies control objectives that are affected by the citation changes.

    After reviewing the impacted control objectives, users can trigger the control objective change agent to update descriptions and guidance as required.

2.  Control objective details updater skill: The AI agent monitors these impacted objectives and validates whether updates are truly required. Using the control objective details updater skill, the agent fetches and applies updated descriptions and supplemental guidance to the relevant control objectives. It intelligently considers all associated citations while filtering out irrelevant details to verify precise updates.
3.  User feedback and refinement: An interactive Now Assist panel provides a feedback loop. Users can review the AI-generated suggestions and:
    -   Accept the proposed updates.
    -   Add or remove specific details.

## Benefits

The control objective change agent refines control objective updates through the following process, offering the following benefits:

-   Automates the process of updating control objective descriptions and supplemental guidance based on changes detected in related citations.
-   Significantly reduces manual effort and enhances accuracy through AI-driven suggestions combined with user feedback loops.

