---
title: Configure proactive case flows
description: Automate workflows for proactive case creation to improve your operational efficiency and respond to customer issues faster.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure Proactive Customer Service, Extend capabilities, Configure, Customer Service Management]
---

# Configure proactive case flows

Automate workflows for proactive case creation to improve your operational efficiency and respond to customer issues faster.

## Before you begin

Role required: admin

## About this task

**Note:** This task is only applicable if you are using the integration with Event Management.

Configure the flow designer to automate the next steps in processing a proactive case. You can automate that a proactive case is proposed to a major case or is directly promoted to a major case. If promoted directly to a major case, child cases are automatically created when multiple customers are impacted.

If a single account is affected, you can also automate that an account and primary contact are associated to a case.

## Procedure

1.  Navigate to **All** &gt; **Customer Service** &gt; **Administration** &gt; **Proactive Case Flows**.

2.  Click the **Process Proactive Cases Created from Alerts** flow.

3.  Click the **Process Proactive Cases for Single and Multiple Accounts** subflow.

4.  In the **Major Case Status** field, set the initial status of the major case for multiple accounts.

    By default, this field is set to **None**. Based on your selection, the proactive case is either **Proposed**, **Accepted**, or **None**. If you set the status to **Accepted**, child cases are created automatically.

5.  In the **Affected Account Threshold** field, enter the number of affected accounts required for a proactive case to be eligible for major case processing.

    The default is two.

6.  Select the **Process Case for Single Account** check box to associate an account and primary contact to the case if a single account is affected.

    This also applies if multiple install base items from the same account are affected.

7.  Click **Done**.


