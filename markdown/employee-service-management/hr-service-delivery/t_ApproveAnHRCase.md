---
title: Resubmit an HR case for approval
description: HR cases that are rejected can be resubmitted for approval. Resubmitting a rejected case alleviates having to recreate a new case.
locale: en-US
release: australia
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Use HR Case Management, Case and Knowledge Management, HR Service Delivery, Employee Service Management]
---

# Resubmit an HR case for approval

HR cases that are rejected can be resubmitted for approval. Resubmitting a rejected case alleviates having to recreate a new case.

## Before you begin

Role required: sn\_hr\_core.case\_writer

After a new case is submitted, an email notification is sent to all approvers. Approvals for HR cases are assigned to individual users or to members of a specified group. Approvers can reject or approve from the HR Service Portal or HR Ticket Page.

When a service activity for an HR service has **Allow resubmit of approvals** for **On rejection**, the Assigned to person can resubmit an approval request after rejection. See [Configure an approval](configure-approval-to-fulfill-hr-service.md).

You can view a list of approvers at the bottom of the HR case form under the **Approvers** tab.

HR cases: Approvals for HR cases use workflows. Do the following to resubmit a rejected HR case.

## Procedure

1.  Open the HR case that has a rejected approval.

    A message appears at the top of the form.![HR case form - reject message](../image/hr-case-reject.png)

2.  Select the **here** link.

    The **Enter the reason for resubmitting approval requests** pop-up appears. You can enter work notes \(not visible to employee\) or comments \(visible to employee\). Work notes or comments are required.![HR case form - reject comments](../image/hr-case-reject-comments.png)

3.  Select **OK**.

    Lifecycle Events cases:

    Approvals for HR activities under a lifecycle event are configured differently than an HR case. There are more options for approvals. See [For an approval](configure-hr-lifecycle-event-activity.md#).

    **Note:** Approvers that do not have the sn\_hr\_core.manager role cannot access the HR case after the state changes to **Closed Complete**.


**Parent Topic:**[Use HR Case Management](../concept/c_HRCaseManagement.md)

