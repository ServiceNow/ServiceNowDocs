---
title: Resubmit a failed stack request
description: The Cloud Provisioning and Governance application creates a remediation or a catalog task when a request for a stack fails to provision. You can resubmit the failed request or assign it to the Cloud Operator group to handle it for you.
locale: en-US
release: australia
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2026-05-08"
reading_time_minutes: 1
breadcrumb: [Launch a stack, Cloud User Portal, Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Resubmit a failed stack request

The Cloud Provisioning and Governance application creates a remediation or a catalog task when a request for a stack fails to provision. You can resubmit the failed request or assign it to the Cloud Operator group to handle it for you.

## Before you begin

Roles required: sn\_cmp.cloud\_service\_user and sn\_cmp.cloud\_operator.

## About this task

Task remediation captures every remediation applied to a failed request. You can view the remediation carried out for a failed request and all the major milestones in the **Comments/Work Notes** sub tab in the Cloud User Portal. Task remediation is available only for new provisioning of stacks and not for life cycle or any other operation.

A stack may fail to provision for many reasons. A stack may fail if you have exceeded your cloud quota, datacenter capacity, or have entered an invalid parameter in the request form \(such as a duplicate NIC\).

If a stack fails to provision, a catalog task is created and assigned to you. An error message pertaining to the failed request is displayed in the **Status** sub tab in the Cloud User Portal.

## Procedure

1.  In the Cloud User Portal, navigate to **View Activities** &gt; **Requests** &gt; **Tasks**.

2.  Click the catalog task to resubmit.

3.  Based on your preference, select an action:

    -   **Retry**: Resubmits the failed request. You can try to resubmit the failed request by resolving the error if possible. If the error is due to exceeding the quota limit, you can try to deprovision some resources that are not currently in use and then click **Retry**. When you click **Retry**, the original request is resubmitted. A new request is not created.

        **Note:** Any policy associated with a resource operation is re-executed.

    -   **Ask for Help**: Creates a new catalog task and assigns it to the Cloud Operator group to resubmit the failed request. The Cloud Operator group can look more closely into the error and try to resolve it for you. Every time the comments or work notes in the catalog task gets updated by the Cloud Operator group, the changes are reflected in the **Comments/Work Notes** sub tab in the Cloud User Portal. If necessary, the operator can cancel the failed request.
    -   **Cancel Order**: Cancels the failed request and deprovisions all partially-provisioned resources.

