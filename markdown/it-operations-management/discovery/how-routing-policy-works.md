---
title: Routing policy details
description: Routing policies are essential for automated certificate management in TLS certificates as they define specific criteria, such as CA and environment, enabling efficient handling of different scenarios during the certificate lifecycle.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Automated certificate management for TLS certificates, Configuring Certificate Inventory and Management, Certificate Inventory and Management, ITOM Visibility, IT Operations Management]
---

# Routing policy details

Routing policies are essential for automated certificate management in TLS certificates as they define specific criteria, such as CA and environment, enabling efficient handling of different scenarios during the certificate lifecycle.

There are three different scenarios for how routing policies work for automated certificate management for TLS certificates.

-   Scenario 1: A single routing policy matches and manual approval is required. The approver can verify the task details and approve the certificate request. Once approved, this triggers the automated flow.
-   Scenario 2: No routing policy matches OR there are multiple routing policies that match. The approver can verify the task details and select Choose Routing Policy &amp; Approve. The approver needs to manually select the routing policy. The updated routing policy then displays. The approver selects the routing policy which then triggers the automated flow.
-   Scenario 3: A single routing policy matches, manual approval is not required, and Approval Required flag is inactive. This triggers the automatic flow.

**Note:**

If the approver has rejected the certificate request task, the task is marked as Failed. A single approval is enough for triggering the automated flow progress.

