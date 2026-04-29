---
title: Create approval chains
description: Optionally create approval chains that control the sequence in which two or more approval rules \(steps\) are run.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Advanced Approval Management, Configure, price, quote apps, Configure, Sales and Order Management]
---

# Create approval chains

Optionally create approval chains that control the sequence in which two or more approval rules \(steps\) are run.

## Before you begin

Role required: sn\_adv\_appr\_mgmt.approval\_rule\_admin, sn\_adv\_appr\_mgmt.approval\_rule\_writer

## About this task

Use chains to control the execution of approval steps that are run based on the approval rule order:

-   Within a chain, steps run sequentially.
-   Across chains, chains can run sequentially or in parallel, based on the chain order value. Chains with the same order value run in parallel.
-   If you don't define chains, approval rules run in parallel.

## Procedure

1.  Navigate to **Workspaces** &gt; **CSM/FSM Configurable Workspace**.

2.  Select the List icon ![](../../../reuse/icons/product-icons/list-outline-24.svg).

3.  Navigate to **Advanced Approvals** &gt; **Approval Chain**.

4.  Select **New**.

5.  Enter the **Name** of the approval chain.

6.  Enter the **Order** in which the approval chain is to be run.

    For example, entering 1 as the **Order** indicates that this chain is run first in the approval workflow sequence.

7.  Select the **Approval configuration** that identifies the Sales and Order Management entity for the approval workflows, such as Quote.


