---
title: Customize team approval settings in SRM
description: Customize how team approvals work when non-admin users create or add a team in Service Reliability Management \(SRM\). This feature, also known as team governance, helps you control access and align with internal policies.
locale: en-US
release: australia
product: Service Reliability Management
classification: service-reliability-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring Service Reliability Management, Service Reliability Management, ITOM AIOps, IT Operations Management]
---

# Customize team approval settings in SRM

Customize how team approvals work when non-admin users create or add a team in Service Reliability Management \(SRM\). This feature, also known as team governance, helps you control access and align with internal policies.

## Before you begin

Role required: srm\_admin oradmin

## About this task

By default, team governance is active in SRM. When non-admin users request a team, SRM creates two records: a parent request and a requested item. The approval team is notified, and any member can approve the request from My approvals. Once approved, the team is created or added, the parent request is set to `Approved`, and the requested item is set to `Closed Complete`.

You can customize team governance by turning off approvals or changing the approval team.

**Note:** Non-admin users are SRM managers and SRM responders. When team governance is active, admins and SRM admins can still create and add teams without approval.

## Procedure

1.  Navigate to **All** &gt; **Service Operations Workspace Admin Center** &gt; **Configurations**.

2.  Under **Service Reliability Management**, select **Governance and autonomy** and then select **Team governance**.

3.  Review or update the approval options.

    |Option|Description|
    |------|-----------|
    |**Approval required when creating a new team**|Clear this option to let non-admin users create teams in SRM without approval.|
    |**Approval required when associating an existing team**|Clear this option to let non-admin users add existing teams to SRM without approval.|

4.  Review or update the approval team for one or both options.

    By default, the approval team is set to `SRM Team approvers`. You can view its members in `sys_user_group.list`.

    **Note:** Any member of the approval team can approve requests, but they need the `sn_request_read` role to view request details. Without that role, they only see the approval task.

5.  Select **Save** to update your team governance settings.


**Parent Topic:**[Configuring Service Reliability Management](../concept/configuring-service-reliability-management.md)

**Previous topic:**[Customize service approval settings in SRM](sr-add-approval-services.md)

**Next topic:**[Configure error budget actions for breached SRM SLOs](sr-configure-error-budget.md)

