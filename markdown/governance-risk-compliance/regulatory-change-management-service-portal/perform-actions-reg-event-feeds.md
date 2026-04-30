---
title: Perform actions on regulatory alerts
description: Perform various actions on unassigned and other types of regulatory alerts. For example, you can assign an unassigned alert, initiate impact assessment on an alert, and mark an alert as applicable, among other actions.
locale: en-US
release: zurich
product: Regulatory Change Management Service Portal
classification: regulatory-change-management-service-portal
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Regulatory alerts, Regulatory Change Management Core UI, Use, Regulatory Change Management, Governance, Risk, and Compliance]
---

# Perform actions on regulatory alerts

Perform various actions on unassigned and other types of regulatory alerts. For example, you can assign an unassigned alert, initiate impact assessment on an alert, and mark an alert as applicable, among other actions.

## Before you begin

Role required: sn\_grc\_reg\_change.manager or sn\_grc\_reg\_change.user

## About this task

A regulatory alert can be either a regulatory event alert or a source document alert. Some actions can be done on either type of alert, but some actions can only be done on regulatory event alerts. Users and managers can do many of the same actions, but there are some actions that can only be done by managers.

Managers can assign fields to the appropriate user. The appropriate user can then assess the applicability of the alert, initiate impact assessments, and complete the assigned regulatory tasks.

In the following procedure, steps 3 and after describe the various actions that you can take as a manager or user.

## Procedure

1.  Navigate to **All** &gt; **Application** &gt; **Regulatory Change Management** &gt; **Regulatory Alerts**.

2.  To assign an unassigned alert, select an alert in the Unassigned Alerts module.

    With the sn\_grc\_reg\_change.manager role, you can set the **Coordinator** field to an appropriate user who has the sn\_grc\_reg\_change.user role.

    This action moves the alert to the All Assigned Alerts module.

3.  To save and update the changes to the alert record, select **Update**.

    |Field|Description|
    |-----|-----------|
    |**Select __Applicable__**|Impact of the alert is applicable to your organization. If the alert is of a regulatory event type, then this action creates a regulatory change task. You can define and complete the regulatory actions that are associated with the change. If the alert is of a regulatory event type, then this action creates a regulatory change task. The state of the alert is updated to In Progress for both types of alerts.|

4.  To defer an alert to a later date, do the following:

    1.  Select **Defer**.

    2.  Select a future reminder date and add a reason for the deferral.

    3.  Select **Submit**.

    The alert is moved to the **Deferred** state in the application. Assigned users receive an email on the selected deferral date as a reminder to work on the alert. They can also cancel the alert.

5.  To initiate an impact assessment on the alert, select **Initiate Impact Assessment**.

    This action is available only to managers and users of regulatory event alerts. This action is not available for source document alerts.

6.  If the impact of the alert is not applicable to the organization, select **Not Applicable**.

    Specify a reason for marking the field as not applicable.

    The alert moves to the **Closed** state.

7.  To cancel the alert, select **Cancel Regulatory Alert**.

    This action is available to managers and users of regulatory event alerts, and to managers of source document alerts; but it is not available to the users of source document alerts.

    This action moves the alert to the **Cancelled** state. The alert is moved to the Closed Alerts module.

8.  To reassign an assigned alert to another user with the sn\_grc\_reg\_change.user role, select **Reassign**.

9.  To delete an alert, select **Delete**.


**Parent Topic:**[Regulatory alerts](../concept/regulatory-feeds.md)

**Related topics**  


[Add an AI-recommended citation to a regulatory alert](add-recommended-citations-to-a-regulatory-alert.md)

[Manage and assign regulatory event alerts](manage-regulatory-feeds.md)

[Train and use the similarity solution to recommend citations on regulatory alerts](retrain-ml-reg-compliance-mapping.md)

[Manage and assign source document alerts](manage-source-document-feeds.md)

