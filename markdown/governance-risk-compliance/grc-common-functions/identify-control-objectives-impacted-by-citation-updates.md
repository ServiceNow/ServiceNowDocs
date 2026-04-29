---
title: Use Control Objective Impact Analyzer skill to identify control objectives
description: Identify and manage control objectives impacted by latest citation updates by using the Control Objective Impact Analyzer generative AI skill.
locale: en-US
release: australia
product: GRC Common Functions
classification: grc-common-functions
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [Control Objective Impact Analyzer skill, Gen AI skill, Impacted control objectives]
breadcrumb: [Use generative AI skills, Now Assist, Common GRC features, Governance, Risk, and Compliance]
---

# Use Control Objective Impact Analyzer skill to identify control objectives

Identify and manage control objectives impacted by latest citation updates by using the Control Objective Impact Analyzer generative AI skill.

## Before you begin

Role required: sn\_grc\_sharegenai.compliance\_library\_gen\_ai\_user

Verify that the Control Objective Impact Analyzer skill is activated.

**Important:** This Now Assist skill is turned on by default. The skill will be automatically available to appropriate role users for the application. For more information, see [Now Assist skills, agents, and agentic workflows on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

## Procedure

1.  Navigate to **Workspaces** &gt; **Compliance Workspace**.

2.  Select the List icon.

3.  Select **Compliance library** &gt; **Citations**.

4.  Select the citation for which you want to identify impacted control objectives.

5.  On the citation page, select **Analyze Impact**.

    Gen AI evaluates the latest citation details to determine their impact on control objectives. Impacted objectives appear in the Change impacts tab. If no control objectives are found, the tab remains empty.

6.  Review the impacted control objectives in the Change impacts tab.

    Each entry provides the current state and additional information regarding how the impact was determined.

    The impacted control objectives have the following states:

    -   New: This state is assigned when an impacted control objective is first identified, indicating that no action has yet been taken.
    -   In progress: This state is assigned when the Control Objective Change Agent is triggered from the NAP panel, indicating active review or update of the control objective.
    -   Completed: This state is assigned after the update process is completed and the control objective’s description and supplemental guidance have been successfully updated, marking the end of the workflow for that item.
    -   Canceled: This state is assigned when a user manually removes a control objective from the impacted list, the system marks the record as 'Canceled' in the background for audit purposes. This state isn't displayed in the UI.
7.  In the Change impacts tab, the user can also manually add or remove control objectives.

    For manually added control objectives, the Additional info column displays 'Manually added'.


