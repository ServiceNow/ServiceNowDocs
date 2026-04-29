---
title: Regulatory change tasks
description: When a manager or user marks an unassigned regulatory alert as applicable, a regulatory change task is created to analyze the impact of the regulatory change and coordinate the required compliance activities.
locale: en-US
release: australia
product: Regulatory Change Management Service Portal
classification: regulatory-change-management-service-portal
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Regulatory Change Management Core UI, Use, Regulatory Change Management, Governance, Risk, and Compliance]
---

# Regulatory change tasks

When a manager or user marks an unassigned regulatory alert as applicable, a regulatory change task is created to analyze the impact of the regulatory change and coordinate the required compliance activities.

A regulatory change task serves as the parent record for all action tasks created to address an applicable regulatory alert. Action tasks represent the specific activities required to implement regulatory changes, such as updating policies, controls, or risk statements in the regulatory library.

A manager with the `sn_grc_reg_change.manager` role assigns a regulatory change task to a user with the `sn_grc_reg_change.user` role. The task captures key information such as the assignment group, approver, assignee, and related regulatory alert to support visibility and accountability throughout the change process.

Starting with version 21.0.1, regulatory change tasks support earlier execution of compliance activities. Tasks can enter the **Implementation** state before approval is requested, allowing teams to begin work while approvals proceed based on workflow configuration.

A regulatory alert can be closed after all required regulatory change tasks and their associated action tasks are completed, and any required approvals are finalized, in accordance with the configured workflow.

-   **[Users and associated actions for the regulatory change tasks](../reference/views-and-actions.md)**  
Managers with the sn\_grc\_reg\_change.manager role and the users with the sn\_grc\_reg\_change.user role can view and perform certain tasks in the Regulatory Change Tasks module.
-   **[Manage the regulatory change tasks](../task/manage-regulatory-change-tasks.md)**  
Manage the regulatory action tasks in the Regulatory Change Tasks module so that you can use these tasks to identify and comply with the regulatory changes.

**Parent Topic:**[Regulatory Change Management Core UI](using-rcm-classic-ui.md)

