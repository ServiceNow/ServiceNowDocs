---
title: Perform a life-cycle operation on a stack or resource
description: Operations like Start/Stop, Deprovision, and ExecuteScript are called life-cycle operations or day-2 operations. When you request a life-cycle operation on a stack or resource, the system generates a change request. An approval policy specifies either that the change is auto-approved or that a user on the approver list must approve the change.
locale: en-US
release: xanadu
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Manage a stack, Cloud User Portal, Cloud Provisioning and Governance, ITOM Optimization, IT Operations Management]
---

# Perform a life-cycle operation on a stack or resource

Operations like Start/Stop, Deprovision, and ExecuteScript are called life-cycle operations or day-2 operations. When you request a life-cycle operation on a stack or resource, the system generates a change request. An approval policy specifies either that the change is auto-approved or that a user on the approver list must approve the change.

## Before you begin

Role required:

Life-cycle operations require the user with `sn_cmp.cloud_service_user` role who owns the resource. A user with the root\_admin, admin, or `sn_cmp.cloud_admin` role can also perform the operation.

## About this task

-   As noted in the descriptions, not all operations are supported for all providers or for all service categories \(resource types\).
-   All other configuration management providers: If a stack or resource requires login, then you must download the associated SSH key before you can access the resource. See [Download an SSH key](cloudmgt-download-ssh-key.md).

## Procedure

1.  Select a stack or resource.

2.  While viewing the **Stack Details** page, select the operation from the **Select Stack Operation** or **Select Resource Operation** list.

    For for full descriptions of the operations, see [Life-cycle operations in Cloud Provisioning and Governance](../reference/life-cycle-operation-cloudmgt.md).

    Some operations require settings \(for example, the name of a script or new schedule settings\).

3.  Enter the settings and then click **OK**.

    The system submits a change request and the **Activities** &gt; **Change Requests** page displays the progress and status of the request.


