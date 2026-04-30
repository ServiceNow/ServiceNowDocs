---
title: Open the Cloud Orchestration Trail
description: Open the Cloud Orchestration Trail to debug and troubleshoot issues like a failed policy or failed Discovery of cloud resources.
locale: en-US
release: zurich
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [The Cloud Orchestration Trail, Troubleshooting tools for Cloud Provisioning and Governance, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Open the Cloud Orchestration Trail

Open the Cloud Orchestration Trail to debug and troubleshoot issues like a failed policy or failed Discovery of cloud resources.

## Before you begin

Role required: sn\_cmp.cloud\_operator or sn\_cmp.cloud\_admin

## Procedure

1.  In the Cloud Admin Portal, navigate to **Operate** &gt; **Trails**.

2.  On the **Cloud Orchestration Trail** tab, filter and sort the list of Orchestration API Trail records as needed.

    If you are looking for something like a failed Discovery, filter the list so the **Level** column shows only entries with **Error**.

3.  Click a link in the **Created** column to open the Orchestration API Trail record.

4.  In the CAPI Trail Logs related list, open the log record that displays the information you want.

    For example, open **route\_error** or **error\_detail** to debug a failed operation.


