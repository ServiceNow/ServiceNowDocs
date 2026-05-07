---
title: Playbook for Failed Login Manual
description: The Failed Login Manual playbook provides guidance and helps optimize the investigation of failed login security incidents.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Process-based Playbooks, Security Incident Response playbooks, Playbook Resources, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Playbook for Failed Login Manual

The Failed Login Manual playbook provides guidance and helps optimize the investigation of failed login security incidents.

When a user makes certain unsuccessful login attempts \(as per the SIM configuration\), a security incident is created. These unsuccessful login attempts may either be false positives or attempts made by attackers to obtain access to user email accounts.

You can use the playbook templates in Workflow Studio to perform the steps in the Failed Login playbook and resolve failed login security incidents efficiently. This playbook includes trigger conditions, a sequence of actions, and subflows that you can annotate. This playbook contains a sequence of reusable actions designed to respond to failed login security incidents. Each flow has a trigger \(condition\), a sequence of actions, and subflows for annotation.

This playbook can be used if a failed login security incident is created or updated. You need to activate the Failed Login Manual Playbook in Workflow Studio and create all the tasks, such as analysis, contain, eradicate, and review.

The following are the stages of the process definition and corresponds to the security incident state:

-   Analysis
-   Contain
-   Eradicate
-   Review

Each stage has activities within it.

Once you mark a task complete in a stage, you can move to the next task. You can save a task at any point in time and return to the playbook at a later date and time. After you complete all the tasks in a stage, you can move to the next stage. The status is reflected in the left-hand panel as you keep completing tasks and stages. An Activity log on the right-hand side of the playbook shows all the data that you have entered for each task.

After you complete all the tasks, you’re asked to review the details you entered in all the stages. You can choose to edit any field or click Finish to complete the process of creating the entitlement.

-   **[Create processes for Failed Login Manual in PAD](../task/create-process-failed-login-manual.md)**  
Use these steps to create processes for Failed Login Manual in the Process Automation Designer \(PAD\).
-   **[Using the Failed Login Manual playbook](../task/using-failed-login-manual-playbook.md)**  
Use these steps to learn how you can use the Failed Login Manual playbook in the SIR Analyst Workspace and its capabilities.

**Parent Topic:**[Process-based Playbooks](../../security-incident-response/concept/playbooks-process-based.md)

