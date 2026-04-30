---
title: Workspace Playbook summary
description: The following describes the process summary.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Playbook for Manual Phishing, Process-based Playbooks, Security Incident Response playbooks, Playbook Resources, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Workspace Playbook summary

The following describes the process summary.

-   Understand legacy flow-based playbook.
-   List down possible activities, stages after analyzing the flow. Look for the steps where true Orchestration can be created.
-   Take each activity and check if base system provided activity definition can fulfill the use case or not.
-   List down activity use cases, which need new activity definitions to be implemented. Classify them - Interactive, non-interactive or automated. To create an activity definition:
    -   Create a subflow or an action for the use case.
    -   Decide whether the associated data must be captured in flow data table or a custom table.
    -   If using flow data table, create flow data definition in **sys\_flow\_data\_definition**. While creating a flow data record in the subflow, select the flow data definition created.
    -   Create an **activity definition**.
    -   Map the automation plan.
    -   Fill in the **Activity Experience** properties.
    -   Create an Action under Playbook Actions. There should be an existing activity action to assign it to the activity definition.
    -   To override the default card experience based on the experience type selected, add playbook override by using Activity UI concept.
-   Some activities can be made to handle both automatic and interactive using wait for user input flag in the subflow. This input can be passed while configuring the activity in the process definition.
-   After you have all the activity definition required for your process, start building the process definition using Workflow Studio.

**Parent Topic:**[Playbook for Manual Phishing](playbook-manual-phishing.md)

