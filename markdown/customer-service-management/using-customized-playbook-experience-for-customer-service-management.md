---
title: Add an optional activity
description: Add optional activities to different stages in a playbook. Although customer processes follow a certain structure, optional tasks may be necessary in some instances. For example, a customer may want to schedule an appointment to visit a location.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Using playbooks, Automate and optimize, Use, Customer Service Management]
---

# Add an optional activity

Add optional activities to different stages in a playbook. Although customer processes follow a certain structure, optional tasks may be necessary in some instances. For example, a customer may want to schedule an appointment to visit a location.

## Before you begin

This feature must be configured by an administrator. If optional activities aren’t configured for a playbook, the **Add Activity** menu item isn’t available. For more information, see [Configure playbook stage and activity visibility](../task/playbook-config-activity-visibility.md).

Role required: agent

## About this task

You can add some optional activities to any stage while you can add others only to a single stage. You can't insert an optional activity as the first activity in a stage or between two completed activities. An approval request optional activity is supported only for a business-to-business \(B2B\) use case.

An agent or a fulfiller can insert an approval request optional activity during a  playbook  run in process-based page variants for complaint case type \(in the triage and research stage\) or onboarding case type \(in the due diligence stage\).

## Procedure

1.  Open a playbook in **CSM Configurable Workspace**.

2.  Find a stage by selecting the More actions menu.

3.  Select **Add Activity**.

    **Add Activity** isn’t displayed if no optional activities are available in this stage.

4.  In the location that you want to add the activity to the playbook, select  **+ Add activity here **.

    In the modal that opens, you can see the placeholders where you can insert an activity.

5.  Select the activity that you want to add to the playbook.

6.  Select **Done**.


