---
title: Add parallel activities
description: If the When to Start field is set to With Previous, then parallel activities can be initiated.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create playbooks for Manual Phishing in Workflow Studio, Playbook for Manual Phishing, Process-based Playbooks, Security Incident Response playbooks, Playbook Resources, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Add parallel activities

If the **When to Start** field is set to **With Previous**, then parallel activities can be initiated.

## For moving from one stage to the next stage

If no run condition is defined, the stages and activities are executed sequentially.

You can use the run condition to skip activities or stages. In this example, **Contain stage begins when the outcome of ‘Does the email have threat indicators?’ is Yes**.

To move from one stage to another stage, you can use the platform provided **activity definition – Update Record**. This will update the state field of security incident, and resume the playbook execution to the next stage.

However, the challenge with this activity definition is that, if say that the playbook is in the Analysis stage, and if the user had manually updated the state to say review, the Update Record activity will again change the state to Contain to continue the playbook execution. This will override the manual change done.

To overcome this, in the base system an activity definition called **Update Task State** is provided. This activity won’t override the security incident state, if the current state of the state of the security is ahead of the stage in the playbook.

## Create a Process definition with dummy trigger condition

A process definition always requires a trigger condition. But, if you aren’t sure when the process should be triggered, you can still create a process definition with a dummy trigger condition. Set the trigger condition as **sys\_id is empty**. This condition will never be met.

**Parent Topic:**[Create playbooks for Manual Phishing in Workflow Studio](../task/create-process-manual-phishing.md)

