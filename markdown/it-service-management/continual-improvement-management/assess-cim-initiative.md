---
title: Assess an improvement for approval
description: Once accepted and set to assess, Approver group members evaluate the improvement for approval before implementation can begin.
locale: en-US
release: australia
product: Continual Improvement Management
classification: continual-improvement-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Managing improvements, Continual Improvement Management, IT Service Management]
---

# Assess an improvement for approval

Once accepted and set to assess, Approver group members evaluate the improvement for approval before implementation can begin.

## Before you begin

Role required: None \(must be a member of the Approver group\)

## About this task

**Note:** Only one Approver group member needs to approve the improvement before moving to the next state. To require additional approvers, configure the CIM Approval workflow in [Flow Designer](https://www.servicenow.com/docs/access?context=flow-designer&version=australia&pubname=australia-application-development&ft:locale=en-US).

The default expiration period for approval requests is seven business days. Pending approval requests are automatically canceled after seven days but can be resubmitted for approval.

Preconditions:

-   Incident manager created an improvement request.
-   Improvement Manager accepted and assigned the improvement request.

By default, an improvement requires approval before it can progress to the Implement state. You can disable the approval requirement using the **sn\_cim.need\_approval** [property](../reference/cim-reference.md). When disabled, the **Approver group** field and the **Approvers** related list on the Improvement Initiative form are not shown.

## Procedure

1.  Navigate to **All** &gt; **Self Service** &gt; **My Approvals**.

2.  On the Approval form, scroll down to the **Summary of Item being approved** section and assess the details of the improvement, including alignment with strategic objectives \(strategies\), business service, business process, priority, effort estimate, benefits, and why this improvement is important.

3.  Click **Approve** in the header bar to approve the improvement.

    The improvement is ready for implementation by the Improvement Manager and Improvement Coordinator.

    A default CIM phase \(CIMT number\) is automatically created.


## Approve an improvement

In the process of reviewing KPI performance in the Performance Analytics application, the incident manager noticed the **Average time to resolve an incident** KPI scorecard was too high \(24 hours\).

As part of the approval process, an Approver group member assessed the details of the improvement and approved it to begin implementation.

|Field|Value|
|-----|-----|
|Approver|Howard Johnson|
|State|Approved|
|Approving|CIM0000135|
|Comments|--|

**Parent Topic:**[Managing improvements](../concept/cim-improvement-initiative-mgmt.md)

**Related topics**  


[Improvement field descriptions](../reference/cim-field-descriptions.md)

