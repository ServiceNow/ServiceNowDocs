---
title: Work with alerts in ITOM mobile
description: Manage alerts on the go. Learn how to assign, reassign, and close alerts in ITOM Mobile Agent. You can also add work notes to alerts and create incidents from alerts.
locale: en-US
release: zurich
product: Service Reliability Management
classification: service-reliability-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Using ITOM Mobile Agent, ITOM Mobile Agent, Service Reliability Management, ITOM AIOps, IT Operations Management]
---

# Work with alerts in ITOM mobile

Manage alerts on the go. Learn how to assign, reassign, and close alerts in ITOM Mobile Agent. You can also add work notes to alerts and create incidents from alerts.

## Add work notes to an alert

Add work notes to an alert to update your team, share important information, and document your actions.

Role required: srm\_manager, srm\_responder, or srm\_admin

1.  On your device, tap the ServiceNow Agent icon \(![Mobile Agent app icon](../../service-reliability/image/sr-mobile-agent-app.png)\).
2.  Tap the **Notifications** tab and select the relevant alert.
3.  Tap the More options icon \(![More options icon](../../event-management/image/more-actions-icon-horizontal.png)\).
4.  Select **Add work notes** and enter your notes.
5.  Save and add your notes to the alert by tapping **Submit**.

ITOM Mobile Agent displays `Success! Comments added`. The assigned team member also receives a push notification that the alert has had comments added.

To view an alert's work notes on mobile, navigate to the alert and select the **Activity** tab.

## Assign an alert

Assign an alert to make sure the correct team member acts on it. You can assign an alert to yourself.

Role required: srm\_manager, srm\_responder, or srm\_admin

1.  On your device, tap the ServiceNow Agent icon \(![Mobile Agent app icon](../../service-reliability/image/sr-mobile-agent-app.png)\).
2.  Tap the **Notifications** tab and select the relevant alert.
3.  Tap the More options icon \(![More options icon](../../event-management/image/more-actions-icon-horizontal.png)\) and select **Assign alert**.
4.  Tap **Assigned to** and select a team member to assign the alert to.
5.  Implement your changes by tapping **Submit**.

The assigned team member receives a push notification that the alert has been assigned to them. The alert also appears in their **My work** tab.

## Close an alert

Close an alert to show that the issue is resolved or that no further action is needed.

Role required: srm\_manager, srm\_responder, or srm\_admin

1.  On your device, tap the ServiceNow Agent icon \(![Mobile Agent app icon](../../service-reliability/image/sr-mobile-agent-app.png)\).
2.  Tap the **Notifications** tab and select the relevant alert.
3.  Tap the **More options** icon \(![More options icon](../../event-management/image/more-actions-icon-horizontal.png)\) and select **Close alert**.

ITOM Mobile Agent displays Alert closed successfully. The alert no longer appears in the assigned team member's **My work** tab.

To view closed alerts that were assigned to you, tap **My work** and then tap **See all** in the My Alerts section. The **Closed** tab shows your closed alerts.

## Create an incident from an alert

Create an incident when an alert signifies a critical issue that disrupts or could disrupt your system.

When you create an incident from an alert, ITOM Mobile Agent assigns the incident to the same team but not the same responder. For example, if the alert is assigned to the Network Ops team and responder Alex, the incident is assigned to the Network Ops team.

Role required: srm\_manager, srm\_responder, or srm\_admin

1.  On your device, tap the ServiceNow Agent icon \(![Mobile Agent app icon](../../service-reliability/image/sr-mobile-agent-app.png)\).
2.  Tap the **Notifications** tab and select the relevant alert.
3.  Tap the **More options** icon \(![More options icon](../../event-management/image/more-actions-icon-horizontal.png)\) and select **Create incident**.

ITOM Mobile Agent displays a notification similar to `INC0013579 was created from Alert0002468`. You can view the incident in the **My team** tab. For more information about managing incidents in ITOM Mobile Agent, see [Managing incidents and major incidents on mobile](../reference/itom-mobile-incidents.md).

**Note:** If you don't see the option to create an incident from an alert, make sure that the alert is assigned to a team. To assign the alert to a team, see [Assign alerts in Express List](../../service-operations-workspace-itom/task/assign-alerts.md). In the Express List, teams are also known as assignment groups.

## Reassign an alert

Reassign an alert to make sure the correct team member or an available team member acts on it. You can reassign an alert to yourself.

Role required: srm\_manager, srm\_responder, or srm\_admin

1.  On your device, tap the ServiceNow Agent icon \(![Mobile Agent app icon](../../service-reliability/image/sr-mobile-agent-app.png)\).
2.  Tap the **Notifications** tab and select the relevant alert.
3.  Tap the **More options** icon \(![More options icon](../../event-management/image/more-actions-icon-horizontal.png)\) and select **Reassign alert**.
4.  Tap **Assigned to** and select a team member to reassign the alert to.
5.  Implement your changes by tapping **Submit**.

ITOM Mobile Agent displays Alert reassigned successfully. The assigned team member receives a push notification and the alert appears in their **My work** tab.

**Parent Topic:**[Using ITOM Mobile Agent](use-itom-mobile.md)

**Previous topic:**[Using ITOM Mobile Agent](use-itom-mobile.md)

**Next topic:**[Managing incidents and major incidents on mobile](../reference/itom-mobile-incidents.md)

