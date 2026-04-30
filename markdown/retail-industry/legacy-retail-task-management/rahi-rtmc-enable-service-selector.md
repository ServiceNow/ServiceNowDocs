---
title: Enable service selector for Retail Task Management Core
description: Activate the service selector to set up multi-store case capabilities.
locale: en-US
release: zurich
product: \[Legacy\] Retail Task Management
classification: legacy-retail-task-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, Retail Task Management, Retail]
---

# Enable service selector for Retail Task Management Core

Activate the service selector to set up multi-store case capabilities.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **Declarative Actions** &gt; **List Actions**.

2.  Search for **Case Type Selector** under the **Specify Client Action** attribute.

3.  Set **Active** to **true**.

4.  Select **Update**.

5.  **Note:** For users on releases prior to Utah only, the following additional steps must occur:

    Navigate to **All** &gt; **System Properties** &gt; **All Properties**.

6.  Search for the **sn\_csm\_case\_types.service\_definition\_select** property.

7.  Set **Value** to **true** to enable the 'Product Service Select' version of the Case Type Selector.

8.  Select **Update**.


## Result

The service selector is now active within the CSM/FSM Configurable Workspace for use with Retail Task Management Core.

