---
title: Playbook for Automated Phishing
description: The Automated Phishing playbook provides step-by-step guidance for your analysts on how they could resolve specific types of security threats in your Automated Phishing activities.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Process-based Playbooks, Security Incident Response playbooks, Playbook Resources, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Playbook for Automated Phishing

The Automated Phishing playbook provides step-by-step guidance for your analysts on how they could resolve specific types of security threats in your Automated Phishing activities.

## Overview

The Automated Phishing playbook template is designed to automate the phishing response tasks and contains a sequence of actions that includes trigger conditions. You can use the playbook templates in Workflow Studio to automate the steps in the phishing response playbook and resolve these incidents efficiently. This playbook template contains a sequence of reusable actions designed to respond to phishing attacks. Each flow has a trigger \(condition\), a sequence of actions, and subflows that you can annotate.

In this playbook, there won't be any user interaction when a security incident's category is set to phishing. This playbook can be used if a security incident is created or updated. You need to activate the Automated Phishing Playbook in Workflow Studio, and this playbook automatically performs all the tasks, such as analysis, contain, eradicate, and review.

The following are the stages of the process definition and corresponds to the security incident state:

-   Analysis
-   Contain
-   Eradicate
-   Review

Each stage has activities within it.

![Automated phishing playbook overview](../image/automated-phishing.gif "Automated Phishing playbook")

Once you mark a task complete in a stage, you can move to the next task. You can save a task at any point in time and return to the playbook at a later date and time. After you complete all the tasks in a stage, you can move to the next stage. The status is reflected in the left-hand panel as you keep completing tasks and stages. An Activity log on the right-hand side of the playbook shows all the data that you have entered for each task.

After you complete all the tasks, you’re asked to review the details you entered in all the stages. You can choose to edit any field or click Finish to complete the process of creating the entitlement.

-   **[Create processes for Automated Phishing in PAD](../task/create-process-automated-phishing.md)**  
Use these steps to create processes for Automated Phishing in the Process Automation Designer \(PAD\).
-   **[Using the Automated Phishing playbook](../task/using-automated-phishing-playbook.md)**  
Use these steps to learn how you can use the Automated Phishing playbook in the SIR Analyst Workspace and its capabilities.

**Parent Topic:**[Process-based Playbooks](../../security-incident-response/concept/playbooks-process-based.md)

