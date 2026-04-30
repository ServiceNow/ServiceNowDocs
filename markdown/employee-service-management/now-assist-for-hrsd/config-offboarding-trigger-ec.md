---
title: Configure the AI agent triggers for offboarding to use Employee Center
description: Add the Employee Center portal to the AI agent trigger configuration used in the offboarding knowledge transfer plan generation agentic workflow. This configuration change enables managers and employees to interact with AI agents through Now Assist in Virtual Agent.
locale: en-US
release: zurich
product: Now Assist for HRSD
classification: now-assist-for-hrsd
topic_type: task
last_updated: "2026-02-25"
reading_time_minutes: 1
breadcrumb: [Offboarding knowledge transfer plan generation agentic workflow, Use agentic workflows, Now Assist for HR Service Delivery \(HRSD\), HR Service Delivery, Employee Service Management]
---

# Configure the AI agent triggers for offboarding to use Employee Center

Add the Employee Center portal to the AI agent trigger configuration used in the offboarding knowledge transfer plan generation agentic workflow. This configuration change enables managers and employees to interact with AI agents through Now Assist in Virtual Agent.

## Before you begin

Role required: admin \[virtual\_agent\_admin\]

## About this task

This task applies to the following triggers associated with the offboarding knowledge transfer plan generation agentic workflow:

-   Offboarding knowledge transfer trigger
-   Knowledge transfer record created

## Procedure

1.  Navigate to the **All** menu, and enter `sn_aia_trigger_configuration.list` in the navigation filter.

    The AIA Trigger Configuration \[sn\_aia\_trigger\_configuration\] table appears.

2.  Select **Offboarding knowledge transfer trigger** from the list of AI agent triggers.

3.  Add the **Active** and **Portal** fields to the form if they aren’t available.

    1.  Select and hold \(or right-click\) the form header and select **Configure** &gt; **Form layout**.

    2.  Select **Active** and **Portal** from the Available list, and then select the **Add** icon to move the fields to the Selected list.

    3.  Select **Save**.

4.  Select the **Active** check box.

5.  Set the **Portal** field to **Employee Center**.

6.  Select **Update**.

7.  Repeat this task to configure the following trigger: Knowledge transfer record created.


