---
title: On-call support for an incident in Service Operations Workspace
description: You can identify available on-call members of a support group and contact them to resolve an issue.View the relevant shift details and contact on-call members for issue resolution and dynamically track the on-call escalation.
locale: en-US
release: australia
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [On-Call Scheduling in Service Operations Workspace, Managing IT services in your organization, Service Operations Workspace for ITSM, IT Service Management]
---

# On-call support for an incident in Service Operations Workspace

You can identify available on-call members of a support group and contact them to resolve an issue.

## On-call support for an incident

Based on support groups associated with all services and CIs of the incident, the **Experts on-call** panel displays three on-call recommendations in the following order:

-   Support group associated with the primary service, that is, the **Service** field.
-   Top support group of impacted services from the Impacted Services/CIs related list.
-   Support group associated with the primary configuration item, that is, the **Configuration item** field.
-   Top support group of affected CIs from the Affected CIs related list.
-   Assignment group of an agent, that is, the **Assignment group** field.

For each of these fields, on-call information such as shift names and on-call members is displayed. For each on-call member, you can view the contact information.

![Experts on-call panel](../image/on-call-section-sow.png "Experts on-call panel")

For information about On-Call Scheduling, see [On-Call Scheduling](../../../administer/on-call-scheduling/concept/c_OnCallScheduling.md).

**Parent Topic:**[On-Call Scheduling in Service Operations Workspace](on-call-scheduling-in-sow.md)

## Experts on-call in Service Operations Workspace

View the relevant shift details and contact on-call members for issue resolution and dynamically track the on-call escalation.

### Before you begin

Role required: itil, admin, sn\_incident\_read, sn\_change\_read

Ensure that the escalation logging, that is, the **com.snc.on\_call\_rotation.log\_escalations** property is enabled to view the on-call escalation tracking page. For information about this property, see [System properties for On-Call Scheduling](../../../administer/on-call-scheduling/reference/on-call-properties.md).

### Procedure

1.  Open an incident.

2.  To view the relevant shift details, contact on-call members, and do other relevant tasks, perform the following steps.

    1.  From the contextual side panel, click the experts on-call icon \(![experts on-call icon](../image/experts-on-call.png)\).

        For information about how on-call recommendations can be configured, see [Customize the on-call support group recommendations](../task/configure-supportgroup-oncall-sow.md).

        Three on-call recommendations are displayed based on support groups associated with all services and CIs of the incident in the following order:

        -   Support group associated with the primary service, that is, the **Service** field.
        -   Top support group of impacted services from the Impacted Services/CIs related list.
        -   Support group associated with the primary configuration item, that is, the **Configuration item** field.
        -   Top support group of affected CIs from the Affected CIs related list.
        -   Assignment group of the agent, that is, the **Assignment group** field.
    2.  To view detailed shift information such as all on-call members and start time and end time and, click **Shift details**.

        When no on-call member is available for a support group in that shift, you can view the next shift with on-call members.

    3.  To start a Microsoft Teams chat conversation with an on-call member, click **Contact** next to the member details and click **Start Teams chat**.

        **Note:** You can view the user presence before contacting the on-call member.

        For information about Microsoft Teams chat, see [Collaborate on a task record using Microsoft Teams in Service Operations Workspace](../task/start-msteams-chat-sow.md).

    4.  To configure display preferences in the **Experts on-call** panel, click the preferences icon \(![preferences icon](../image/preferences-icon.png)\) and perform any of the following actions.

        -   To hide shifts with no on-call members, use the **Hide shifts with no on-call** toggle switch. If no on-call members are available for all support groups, you can search for other groups and view its on-call members.
        -   To use the default date and time format configured for the current user, use the **Use default date and time formats** toggle switch.
3.  To view dynamic tracking of an on-call escalation, click the on-call escalations icon \(![on-call escalations icon](../image/on-call-escalation.png)\)

    ![Escalation tracking in SOW](../image/escalation-tracking-SOW.png)

4.  To view detailed escalation tracking information, click **View escalation details**.

    ![View escalation tracking details](../image/escalation_tracking_details_SOWOncall.png)


