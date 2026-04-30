---
title: Recall event-driven questionnaires and doc requests
description: You can recall third-party risk assessments \(questionnaires and document requests\) that were sent by an event-driven management rule. The items are removed from the Third-party portal for all third parties or engagements that haven’t yet responded.
locale: en-US
release: zurich
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Event-driven management rules, Classic assessments, Configure, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Recall event-driven questionnaires and doc requests

You can recall third-party risk assessments \(questionnaires and document requests\) that were sent by an event-driven management rule. The items are removed from the Third-party portal for all third parties or engagements that haven’t yet responded.

## Before you begin

Role required: sn\_vdr\_risk\_asmt.vendor\_risk\_manager

## About this task

**Important:** The questionnaires and document requests are removed from the Third-party portal only for third parties where no item had yet been returned.

## Procedure

1.  Use either of the following methods to start the process:

    -   Workspace: Select **Workspaces** &gt; **Vendor Management Workspace** and on the **Risk** tab, select the list icon ![](../image/icon-tprm-ws-list.png). In the **Event-driven management** list, select any option: **Active**, **Inactive**, or **All**.
    -   Legacy: Navigate to **All** &gt; **Third-party Risk Management** &gt; **Event-driven management** and then select any option: **Active**, **Inactive**, or **All**.
2.  Enter text that explains the reason for recalling the items in the **Recall justification** field and then select **Recall**.

    The third-party risk assessments are removed from the affected Third-party portals and the **State** value of the rule is set to **Recalled**.


