---
title: Configure AWA queues for the proxy contact role
description: Modify the Advanced Work Assignment queues and add routing conditions that support the proxy contact role and the Internal contact field on the Case form.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [AWA for CSM, Case routing and assignment, Organize agent workspaces, Configure, Customer Service Management]
---

# Configure AWA queues for the proxy contact role

Modify the Advanced Work Assignment queues and add routing conditions that support the proxy contact role and the **Internal contact** field on the Case form.

## Before you begin

Role required: admin

## About this task

Modify the following AWA queues:

-   For the Case service channel: Customer Service Cases
-   For the Chat service channel: Customer Service

## Procedure

1.  Navigate to **All** &gt; **Advanced Work Assignment** &gt; **Queues**.

2.  Select the **Customer Service Cases** queue.

3.  In the **Work item routing condition** field, add the following OR condition: **Internal Contact is not empty**.

4.  Click **Update**.

5.  Select the **Customer Service** queue.

6.  In the **Work item routing condition** field, add the following OR condition: **Roles is sn\_customerservice.proxy\_contact**.

7.  Click **Update**.


