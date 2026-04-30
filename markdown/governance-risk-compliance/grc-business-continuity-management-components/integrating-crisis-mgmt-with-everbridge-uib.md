---
title: Emergency notifications in Everbridge
description: You can integrate Crisis Management in the BCM application with Everbridge notifications system. You can then send an emergency notification to an individual or a group of people alerting them of an impending emergency. It provides a one-way notification and two-way communication through properly established delivery channels.
locale: en-US
release: xanadu
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Explore, Business Continuity Management, Governance, Risk, and Compliance]
---

# Emergency notifications in Everbridge

You can integrate Crisis Management in the BCM application with Everbridge notifications system. You can then send an emergency notification to an individual or a group of people alerting them of an impending emergency. It provides a one-way notification and two-way communication through properly established delivery channels.

Crisis Management in Business Continuity Management application uses Everbridge to direct certain crisis response activities. This integration helps to send notifications about critical events to stakeholders and coordinates responses from them in an effective two-way delivery channel.

To send a notification, you need correct contacts, groups, and delivery channels. Delivery channels are created and stored in Everbridge and you have to import those delivery channels for your particular organization ID. These delivery channels are used for sending notifications and contact creation.

## Process for sending the emergency notifications

You can send an event notification that triggers a complete workflow of the activities from the **Draft** to the **Complete** state in Everbridge. You can monitor all activities from Business Continuity Workspace.

When you send an emergency notification from the Business Continuity Workspace, the action creates an incident and a notification for the incident in Everbridge to be sent to the right contacts and groups.

The emergency notifications for an event are displayed on the **Emergency notifications** tab for the event. You can view the details of the emergency notification such as the notification state, start date, end date, and so on as shown in the following example.

![Emergency notifications tab.](../image/emergency-notification.png)

The emergency notification form is shown in the following example.

![Emergency notification form.](../image/notification-form.png)

## Summary of the notification sent to contacts

The **Summary** section in the notification form displays a list of the contacts and groups to whom the notification was sent and their responses are also recorded. It also displays the number of contacts who could not be reached, the number of contacts who acknowledged the notification, and the number of pending acknowledgments. This information is retrieved from Everbridge and it is displayed in your Business Continuity Workspace as shown in the following example.

![Summary of the notification sent to the contacts.](../image/SummaryEmergNotif.png "Summary of the notification sent to the contacts")

The Summary section in the notification form contains the following information:

-   **Sent to**

    Number of contacts to whom the notification was sent.

-   **Unreachable**

    Number of contacts to whom notification was not sent.

-   **Acknowledged**

    Number of contacts who acknowledged the receipt of notification.

-   **Pending acknowledgment**

    Number of contacts who did not acknowledge the receipt of notification.

-   **Late acknowledgment**

    Number of contacts who confirmed the receipt of notification after the notification duration had elapsed.


If there are many contacts to whom the notification could not be delivered, then you can create another notification for the same crisis event. This time, you can send it to a team of managers, as the previous notification did not reach many contacts.

## Administrative tasks for integrating Crisis Management with Everbridge

For information on the administrative tasks for integrating Crisis Management with Everbridge notifications system, see [Setup for Everbridge notifications](setup-steps-for-emergency-notification-uib-ws.md).

**Parent Topic:**[Exploring Business Continuity Management](exploring-bcm.md)

