---
title: Activate SLO-based change approval decisions
description: Activate Service Level Objective \(SLO\) change approval decisions to evaluate change requests based on SLO performance.
locale: en-US
release: australia
product: Service Level Objective Management
classification: service-level-objective-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Using SLO Management, Service Level Objective Management, ITOM AIOps, IT Operations Management]
---

# Activate SLO-based change approval decisions

Activate Service Level Objective \(SLO\) change approval decisions to evaluate change requests based on SLO performance.

## Before you begin

Review change approval policies and their terminology, including policy inputs, decisions, and approval definitions. For more information, see Change approval policies.

Role required: admin

## About this task

Activate the Service Level Objective Change policy's decisions to include SLO performance in your change management process. The policy is active by default, however, its decisions are inactive.

When you activate the policy's decisions, the policy evaluates SLOs as inputs and implements the following:

-   Require group manager approval if these conditions are true:
    -   The lowest SLO error budget is less than 25%.
    -   The highest SLO burn rate is greater than 1%.
-   Auto-approve change requests if these conditions are true:
    -   The lowest SLO error budget is greater than 25%.
    -   The highest SLO burn rate is less than 1%.

## Procedure

1.  Navigate to **All** &gt; **Change** &gt; **Change Policy** &gt; **Change Approval Policies**.

2.  Select the **Service Level Objective Change policy**.

3.  In the **Decisions** tab, set **Active** to true for these decisions:

    -   **Budget &lt; 25% and Burn Rate &gt; 1**
    -   **Budget &gt; 25% and Burn rate &lt; 1**
4.  Select **Update** to save your changes.

    The decisions are active and part of your change management process.


## What to do next

Use a test change request to verify that change requests are either auto-approved or routed to a manager as expected.

You can also customize the Service Level Objective Change policy, including its name and conditions, as needed.

For more advanced setups, use Flow Designer to customize the SLOs and services included as policy inputs:

**Important:** Customizing the flow prevents it from receiving future release updates. That behavior is intentional to avoid overwriting your customizations.

1.  Navigate to **Process Automation** &gt; **Flow Designer**.
2.  In the list of flows, select **Change - SLO – Authorize** and then select **SLO - Get worst performing SLOs**.
3.  Customize the **Action Inputs** section.
4.  Select **Done** to implement your changes.

**Parent Topic:**[Using SLO Management](../../slo-management/task/using-service-level-objective-management.md)

