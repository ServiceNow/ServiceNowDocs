---
title: Use Recommendation of similar control objectives skill to generate suggestions
description: The "Recommendation of similar control objectives" skill generates recommendations by identifying, deduplicating, and rationalizing similar control objectives within the compliance library. This enables identification of redundant control objectives, making it easier to maintain a clean and efficient compliance library.
locale: en-US
release: zurich
product: Privacy Workspace
classification: privacy-workspace
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Now Assist for Privacy Management, Privacy Management, Governance, Risk, and Compliance]
---

# Use Recommendation of similar control objectives skill to generate suggestions

The "Recommendation of similar control objectives" skill generates recommendations by identifying, deduplicating, and rationalizing similar control objectives within the compliance library. This enables identification of redundant control objectives, making it easier to maintain a clean and efficient compliance library.

## Before you begin

Role required: sn\_reco\_template.rationalization\_process\_writer and sn\_grc\_shared\_genai.compliance\_gen\_ai\_user

## About this task

**Important:** This Now Assist skill is turned on by default. The skill will be automatically available to appropriate role users for the application. For more information, see [Now Assist skills, agents, and agentic workflows on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

The "Recommendation of similar control objectives" skill generates recommendations based on the similarity parameters configured \(names and description\). The Gen AI searches for similar names and descriptions, which serve as inputs for providing recommendations.

**Important:** Be sure to check AI-generated recommendations for accuracy.

## Procedure

1.  Navigate to **Workspaces** &gt; **Privacy Workspace**.

2.  Select the List icon.

3.  Navigate to **Library** &gt; **Control Objectives**.

4.  Open the control objective which you want to rationalize.

5.  In the Overview tab of the control objective, select **Rationalize**.

    **Note:** If a rationalization process is already available for a control objective, the user is directed to the Rationalize tab for that specific control objective.

    -   A new Rationalization process page is automatically created.
    -   The Activity section shows the progress of the rationalization creation process:
        -   The rationalization process first moves to Initiate state, with Generating Recommendations as the substate.
        -   After the recommendations are ready, a new Rationalize tab appears.
        -   The state next moves to Analyze, with Identify Duplicates as the substate.

## What to do next

Accept or dismiss the generated recommendations. For more information, see Act on the Recommendations topic.

**Note:**

You can configure UI form actions in addition to "Accept as duplicate", "Dismiss" and "Retain as primary" as declarative actions for recommendations. For more information about creating declarative actions and how to use them, see [Customizing Configurable Workspace with declarative actions](https://www.servicenow.com/docs/access?context=declarative-actions-landing&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US).

