---
title: Configure Managed Instances
description: Implement the following steps to configure the Managed Instances in Multi-Instance Management.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Cross-instance application trust configuration, Multi-instance Management, Get started, Administer the ServiceNow AI Platform]
---

# Configure Managed Instances

Implement the following steps to configure the Managed Instances in Multi-Instance Management.

## Before you begin

Role required: admin or sn\_mif.mif\_admin.

## Procedure

1.  Go to **Multi-Instance Management** &gt; **Managed Instances**.

2.  Select **Add managed instances**.

    The Add managed instances modal shows up. The managed instances allow the managing instance to remotely distribute trust profile configurations. The modal shows a list of instances where the approval request is sent.

    **Note:** The instances that show up on the list are pulled from the instance table. The instances that belong to the same account and customer are only shown in the list for the request to be sent.

3.  Select **Send Requests** to send the request to the selected instances to allow to be managed.

    A message informs you that managing instance requests were successfully sent and are pending approvals.

4.  Refresh the managed instance and you will see the list of instances you have sent the request to with pending approval.

    The Managing instance needs to approve them.

5.  Go to the Managed By Instances instance and refresh it.

    You will see the approvals requested.

6.  Select the information icon next to the application name on the Managed By Instances instance.

    The Manager Instances record pops up.

7.  Select **Open Record** in the pop up to open the record.

8.  Select one of the following actions Manager Instances record.

    -   Approve Manager Instance
    -   Reject Manager Instance
    **Note:** If you are an Multi-instance Management admin, you will also be notified by an email about the approval requests.

9.  Once approved, review the Managed Instances instance and the status updates.

    **Note:** The status shows as Revoked in the Managed Instances instance if its been deleted from the Managed By Instances instance. If a request is approved by the system, the status shows as Auto-Approved.


