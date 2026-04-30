---
title: Retain inactive namespace CIs for audits
description: If required by your corporate standards, retain inactive namespace configuration items \(CIs\) for reference and auditing purposes with the option to delete them manually later.
locale: en-US
release: zurich
product: Discovery
classification: discovery
topic_type: task
last_updated: "2026-01-15"
reading_time_minutes: 1
breadcrumb: [Install Kubernetes Visibility Agent \(KVA\), Configuring Kubernetes Visibility Agent, Kubernetes discovery using Kubernetes Visibility Agent, Discovery for containerized resources, Discovery, ITOM Visibility, IT Operations Management]
---

# Retain inactive namespace CIs for audits

If required by your corporate standards, retain inactive namespace configuration items \(CIs\) for reference and auditing purposes with the option to delete them manually later.

## Before you begin

Confirm you have the following setup:

-   Kubernetes Visibility Agent \(KVA\) Plugin application release 3.11.0
-   Informer version 2.5.0

Role required: admin

## About this task

To keep Namespace CIs for viewing or auditing required by your corporate standards instead of deleting them automatically, which is the default behavior, enable a system property that ensures that the **table cleaner** scheduled job doesn't remove them but instead updates their *install\_status* value to retired.

You can later delete inactive CIs manually.

## Procedure

1.  Navigate to **All &gt; System Properties &gt; All Properties**.

2.  In the **Name** field, enter `sn_acc_visibility.retired_deletion_strategy_enabled`.

    -   If the property is available, double-click the **Value** field to perform inline editing, enter `true`.
    -   If the property doesn't exist on your instance, select **New** and create the `sn_acc_visibility` property, then double-click the **Value** field to perform inline editing, and enter `true`.
3.  Refer to [https://www.servicenow.com/docs/r/servicenow-platform/configuration-management-database-cmdb/cmdb-data-management.html](https://www.servicenow.com/docs/r/servicenow-platform/configuration-management-database-cmdb/cmdb-data-management.html) to manage the lilfecycle of retired CIs.


**Parent Topic:**[Install Kubernetes Visibility Agent \(KVA\)](cnov-deploy-install.md)

