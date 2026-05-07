---
title: Notify stakeholders and initiate response workflows
description: Notify the stakeholders and initiate multiple workflows for the recovery teams across your organization and help them respond to the threat and take necessary actions.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Crisis Management map, Using BCM Classic Workspace, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Notify stakeholders and initiate response workflows

Notify the stakeholders and initiate multiple workflows for the recovery teams across your organization and help them respond to the threat and take necessary actions.

## Before you begin

Role required: BCM admin or BCM Program Manager

## Procedure

1.  Navigate to **Business Continuity** &gt; **Business Continuity Workspace**.

2.  Click the map icon \(![Crisis map icon](../image/CrisisMapIcon.png)\).

3.  Click an alert record.

    As a crisis manager, while viewing the alerts and their severity, you can initiate appropriate actions and trigger Crisis Management workflows for the respective stakeholders to respond and act on the crisis. The **Suggested Actions** section lists various responses that you can initiate.

    -   **Notify Stakeholders**

        Notify important stakeholders of the assets that are at risk because of the alert.

    -   **Declare a Crisis Event**

        Start an event to activate the recovery tasks to recover the assets with a recovery team.

4.  To notify a stakeholder of the impending crisis by an email, click the **Notify** button in the Notify Stakeholders card.

    In the modal window that opens, identify the concerned person or persons and communicate the information to them. It is a two-step process, where you identify the audience and draft an email to send it to them.

    1.  Select an audience from the list in the Notify Stakeholders pop-up.

        You can select an additional audience from the list whom you think must be notified too.

    2.  Click **Next**.

    3.  In the Step 2 of the process, verify the alert details and draft an email appropriately in the **Email Body** field.

    4.  Click the **Send Notification** button.

        You get a message that the action is executed.

5.  To activate a business continuity or disaster recovery plan for the locations that are impacted, click **Declare Crisis** in the Declare a Crisis Event card.

    1.  Enter a brief description of the crisis event in the Declare a Crisis Event modal window that opens.

    2.  Click **Next**.

    3.  Select the assets at risk that are within the radius of the threat alert.

    4.  Click **Start Crisis Event** button.

    When you trigger these actions, separate scripts run to trigger the alert notify action and the declaration of the crisis event. A message appears to confirm that your actions are executed. You can navigate to the **Response Tasks** tab to view the action and recovery event details.

    All the assets at risk are copied over to the Event Assets table \[sn\_recovery\_event\_asset\] related to the event \[sn\_recovery\_event\].

    ![Event details of a crisis event.](../image/DeclareCrisis.png "Declare a crisis event")


## What to do next

1.  If it is a recovery event, click anywhere on the Response Tasks card to take you to the event details.
2.  In the **Details** tab of the event, update the details if required.
3.  Click the **Start Event** button. The event for the crisis is then activated. All the associated plans for this recovery event and the tasks associated with it are set into action. The Crisis Management workflow begins to recover the impacted assets. For more information, see [Manage a crisis event](manage-crisis-event.md).

    All the assets at risk are copied over to the Event Assets table \[sn\_recovery\_event\_asset\] related to the event \[sn\_recovery\_event\].


