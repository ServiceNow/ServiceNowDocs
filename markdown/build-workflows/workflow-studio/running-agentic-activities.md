---
title: Using Agentic Playbooks
description: Monitor and complete agentic activities as needed.
locale: en-US
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Agentic Playbooks, Workflow Studio, Build workflows]
---

# Using Agentic Playbooks

Monitor and complete agentic activities as needed.

## Before you begin

Role required: playbook.agent\_user, playbook.agentic\_workflow\_user

## About this task

Leverage AI agents in Agentic Playbooks to automate work and increase efficiency. Make sure to review the AI generated data for accuracy. If AI agents run into any issues with collecting data, some information may be missing or not 100% complete.

Activities that are configured to be completed independently by AI agents are automatically processed and marked complete. You can view the generated output and the process followed by the AI agents in the Now Assist panel. For activities that require manual intervention, you must review the AI-generated output and complete the activity.

## Procedure

1.  Launch your playbook.

2.  To monitor an activity that is being performed by an AI agent, select **View progress**.

    Activities performed by AI agents display a Now Assist status at the top of the activity card.

3.  If you encounter inaccurate information, correct the suggested input from the AI agent before completing the activity.

    Similarly, if you encounter incomplete information, add the information before completing the activity.


## Using Agentic Playbooks in contract renewal process

In the following example, Beth Anglin, a CSM / FSM Workspaces user, is creating a contract record for renewal. Traditionally, this process involves manually reviewing records, calculating discount percentages, verifying compliance, and drafting an email to the customer. With Agentic Playbooks, the process is streamlined as AI agents perform these tasks upon saving the contract record.

1.  As soon as Beth saves the new contract record, the **Playbook** tab appears, and the AI agents start calculating the discount percentage. ![On the Playbook tab of the contract record, NowAssist agents are calculating discount.](../images/agentic-playbook-contracts-save.png)
2.  Beth selects **View progress** to monitor the activities performed by the AI agents. ![The Now Assist panel displays the progress of the agents.](../images/agentic-playbook-view-progress.png)

    The Now Assist panel displays the activities performed by the AI agents.

    ![Now Assist panel displaying the AI activities.](../images/agentic-playbook-progress.png)

3.  Beth reviews the AI generated discount percentage and can update it if necessary. ![Beth reviews the AI generates discount percentage and submits.](../images/agentic-playbook-edit-discount.png)

    **Note:** If the activity is configured to be completed independently by AI agents, the agents calculate the offered discount percentage, populate the discount details, complete the activity, and automatically move to the next activity in the playbook. See [Configuring Agentic Playbooks](configure-agentic-playbooks.md).

4.  By selecting the **How** button, Beth can view a summary of the AI agents' calculation process. ![Beth clicks How button to view the process the AI agents took to calculate the discount.](../images/agentic-playbook-agent-how.png)
5.  After submitting the discount, AI agents start drafting an email for Beth, ensuring a seamless experience.
6.  Beth reviews the drafted email and selects to send it to the customer. ![Beth review the email draft and selects Send.](../images/agentic-playbook-send-email.png)

By leveraging Agentic Playbooks, Beth efficiently manages the contract renewal process, reducing manual effort and enhancing customer communication.

