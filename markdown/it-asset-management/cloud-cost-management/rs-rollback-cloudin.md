---
title: AWS only – Rollback on failed Rightsizing attempts
description: AWS only: If a Rightsizing action fails, the system immediately performs a rollback to return the resource to its original size, restarts the resource if needed, updates the change request with full details, and updates Rightsizing report data.
locale: en-US
release: yokohama
product: Cloud Cost Management
classification: cloud-cost-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Rightsizing analysis for AWS, Rightsizing resources, Exploring Cloud Cost Management, Cloud Cost Management, IT Asset Management]
---

# AWS only – Rollback on failed Rightsizing attempts

AWS only: If a Rightsizing action fails, the system immediately performs a rollback to return the resource to its original size, restarts the resource if needed, updates the change request with full details, and updates Rightsizing report data.

**Note:**

This description of rollback operations applies only to AWS environments. Cloud Cost Management performs rollback operations for AWS environments.

Cloud Cost Management doesn’t perform rollback for Microsoft Azure environments. Instead, the Azure Update service performs rollback.

## Rollback operations \(AWS only\)

In a successful Rightsizing job, the system resizes each resource that has an approved change request. If a resource is in the ON state, the process stops the resource, resizes \(modifies\) it, and then restarts it. If a resource is in the OFF state, the process resizes the resource but doesn’t start it.

A resource might fail to restart, for example, when the new size would exceed the quota limit for a resource type or for a constrained availability zone.

A Rightsizing job proceeds in batches of resources, grouped by provider/service account/region. If any modified resource in a batch fails to restart, then each resource in the batch is rolled back to its original size and then restarted. The system then updates the change requests for the resources and sets the **Rightsizing recommendation** status on Rightsizing reports to **Failed**.

Resources in a batch that were in the OFF state aren’t rolled back or marked as failed.

