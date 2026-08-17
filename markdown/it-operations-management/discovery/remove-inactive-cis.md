---
title: Enable automatic retirement for inactive Kubernetes cluster CIs
description: Enable automatic retirement to update the status of inactive Kubernetes cluster configuration items \(CIs\) and all associated resources during full discovery cycles, so your CMDB reflects only active infrastructure.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/discovery/remove-inactive-cis.html
release: australia
product: Discovery
classification: discovery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Install Kubernetes Visibility Agent \(KVA\) Informer, Configure, Kubernetes discovery using Kubernetes Visibility Agent, Discovery for containerized resources, Discovery, ITOM Visibility, IT Operations Management]
---

# Enable automatic retirement for inactive Kubernetes cluster CIs

Enable automatic retirement to update the status of inactive Kubernetes cluster configuration items \(CIs\) and all associated resources during full discovery cycles, so your CMDB reflects only active infrastructure.

## Before you begin

Confirm you have the following setup:

-   Kubernetes Visibility Agent \(KVA\) Plugin application release 3.15.0
-   Informer version 2.6.0

Role required: discovery\_admin

## About this task

Enable automatic retirement to update the status of inactive Kubernetes cluster CIs and all associated resources \(pods, namespaces, deployments, containers, and other resources\) during full discovery cycles. This feature is disabled by default.

## Procedure

1.  Enable automatic retirement for inactive cluster CIs by performing the following substeps.

    1.  Navigate to **All &gt; System Properties &gt; All Properties**.

    2.  In the **Name** field, enter `sn_acc_visibility.auto_retire_k8s_clusters`.

        -   If the property is available, double-click the **Value** field to perform inline editing, enter `true`.
        -   If the property doesn't exist on your instance, select **New** and create the `sn_acc_visibility.auto_retire_k8s_clusters` property with Type set to True/False, then double-click the **Value** field to perform inline editing, and enter `true`.
        Auto-retirement is enabled. By default, clusters are retired after 60 days of inactivity with the *install\_status* set to Retired \(value 7\).

    3.  Customize the inactivity period by setting the **sn\_acc\_visibility.auto\_retire\_period\_days** property to the number of days after which inactive clusters should be retired.

        The default value is 60 days.

    4.  Customize the install status value by setting the **sn\_acc\_visibility.auto\_retire\_install\_status** property to the numerical value of the desired install status.

        The default value is 7 \(Retired\). Other possible values include 100 \(Absent\).

        **Warning:** If you set the value to 100 \(Absent\), the cluster CI and all associated CIs are deleted by a table cleanup job. This action is irreversible.

    5.  Configure the install status for Linux server CIs associated with Kubernetes nodes by setting the **sn\_acc\_visibility.node\_deletion\_set\_server\_install\_status** property to the numerical value of the desired install status.

        If this property does not exist or the value is empty, no action is taken on Linux server CIs when nodes are retired.

2.  To manage the lifecycle of retired CIs, see [https://www.servicenow.com/docs/r/servicenow-platform/configuration-management-database-cmdb/cmdb-data-management.html](https://www.servicenow.com/docs/r/servicenow-platform/configuration-management-database-cmdb/cmdb-data-management.html).


**Parent Topic:**[Install Kubernetes Visibility Agent \(KVA\) Informer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/cnov-deploy-install.md)

