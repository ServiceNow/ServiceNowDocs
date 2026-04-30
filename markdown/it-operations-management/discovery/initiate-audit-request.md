---
title: Initiate audit request
description: Initiate audits against a specified firewall manager or device to ensure proper configuration in alignment with the security policies of your organization.
locale: en-US
release: yokohama
product: Discovery
classification: discovery
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Firewall audits, Configuring Firewall Audits and Reporting, Firewall Audits and Reporting, Discovery, ITOM Visibility, IT Operations Management]
---

# Initiate audit request

Initiate audits against a specified firewall manager or device to ensure proper configuration in alignment with the security policies of your organization.

## Before you begin

Role required: firewall\_admin

## Procedure

1.  To list all of the discovered firewall managers in your network, navigate to **All** &gt; **Firewall Audits and Reporting** &gt; **Records** &gt; **Devices or Managers**.

2.  Select a firewall manager CI record or device record from the list.

3.  Select **Initiate Audit Request**.

4.  Fill in the mandatory fields on the form.

5.  Select **Submit**.


## What to do next

The procedure initiates an audit for the firewall manager, validates it, and submits the audit task. Firewall audit tasks are generated based on the assigned user for the firewall security policy. If the policy lacks a designated user, no audit task is created for that security policy, and it is placed in the **Excluded Policy List** for audit requests.

This requests an audit for the firewall manager, validates, and submits. Firewall audit task are created on the basis of an assigned user for the firewall security policy. If the policy is not assigned to a user, then no audit task is created for that security policy and it is added into the **Excluded Policy List** of audit requests.

-   If **Assigned To** is provided, the audit task is created and grouped by the assigned user.
-   If **Assigned To** is not provided, and the **sn\_disco\_firewall.default.rule.task.policy.owner.group** discovery property is not set, the policy is added to **Excluded Policies** list, and no audit task is generated.
-   If **Assigned To** is not provided, but the **sn\_disco\_firewall.default.rule.task.policy.owner.group** discovery property is configured, the audit task is created and grouped by the **Assignment Group**.

To verify if the audit task was requested, navigate to **Audits** &gt; **Audits Request**. You should see your task in the list. Creation of audit tasks is a background job using sub-flows. You may need to wait for audit tasks to get created depending on the number of policies.

The **Assigned To** person audits each policy in the related list. They choose the action for each policy and mark the task as **Close Complete**.

