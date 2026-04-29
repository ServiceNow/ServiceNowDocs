---
title: Initiate the response actions
description: Initiate the response workflows for your recovery teams in BCM UIB Workspace. You can then notify the stakeholders and help them respond to the threat and take the necessary actions.
locale: en-US
release: australia
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Structured workflows for Crisis map, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Initiate the response actions

Initiate the response workflows for your recovery teams in BCM UIB Workspace. You can then notify the stakeholders and help them respond to the threat and take the necessary actions.

## Before you begin

Role required: sn\_bcm.admin or sn\_bcm.program\_manager

## Procedure

1.  Navigate to **Workspaces** &gt; **Business Continuity Workspace** and select **Crisis map** in the list view.

2.  Select an alert record.

    While viewing the alerts and their severity, you can initiate appropriate actions and trigger Crisis Management workflows for the respective stakeholders to respond and act on the crisis. The **Suggested Actions** section lists various responses that you can initiate.

    -   **Notify Stakeholders**

        Notify important stakeholders of the assets that are at risk because of the alert.

    -   **Declare a Crisis Event**

        Start an event to activate the recovery tasks to recover the assets with a recovery team.

3.  Notify stakeholders of the impending crisis by email using the **Notify** button in the 'Notify Stakeholders' card.

    In the modal window that opens, identify the concerned person or persons and communicate the information to them. It’s a two-step process, where you identify the audience and draft an email to send it to them.

    1.  Select an audience from the list in the Notify Stakeholders pop-up.

        You can select an additional audience from the list whom you think must be notified too.

    2.  Select **Next**.

    3.  Verify the alert details as described in step 2 of the process and draft an appropriate email in the **Email Body** field.

    4.  Select the **Send Notification** button.

        You get a message that the action is executed.

4.  Activate a business continuity or disaster recovery plan for impacted locations by selecting **Declare Crisis** in the 'Declare a Crisis Event' card.

    1.  Enter a brief description of the crisis event in the Declare a Crisis Event form that opens and select **Next**.

    2.  Select the assets at risk that are within the radius of the threat alert.

    3.  Select the **Start Crisis Event** button.

    When you trigger these actions, separate scripts run to trigger the alert notify action and the declaration of the crisis event. A message appears to confirm that your actions are executed. You can navigate to the **Response Tasks** tab to view the action and recovery event details.

    All the assets at risk are copied over to the Event Assets table \[sn\_recovery\_event\_asset\] that is related to the event \[sn\_recovery\_event\].


## What to do next

1.  If it’s a recovery event, select anywhere on the **Response Tasks** card to take you to the event details.
2.  In the **Details** tab of the event, update the details if necessary.
3.  Select the **Start Event** button. The event for the crisis is then activated. All the associated plans for this recovery event and the tasks associated with it are set into action. The Crisis Management workflow begins to recover the impacted assets. For more information, see [Crisis events](../concept/crisis-management-uib.md).

    All the assets at risk are copied over to the Event Assets table \[sn\_recovery\_event\_asset\] that is related to the event \[sn\_recovery\_event\].


**Parent Topic:**[Structured workflows for Crisis map](../concept/crisis-map-collective-tasks.md)

