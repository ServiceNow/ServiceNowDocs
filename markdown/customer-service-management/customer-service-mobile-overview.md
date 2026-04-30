---
title: Customer Service mobile application overview
description: Customer service agents and managers can use the applet launcher and applets in the Customer Service mobile application to view notifications and manage customer service cases.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Mobile experience for Customer Service Management, Manage schedules and sites, Using Customer Service Management, Customer Service Management]
---

# Customer Service mobile application overview

Customer service agents and managers can use the applet launcher and applets in the Customer Service mobile application to view notifications and manage customer service cases.

## Applet launchers

Applet launchers serve as landing pages or home pages. When you log in to your instance, you see an applet launcher and the applets configured to display on that launcher. The system administrator configures the applet launcher and applets for the Customer Service Management mobile application.

## Navigation bar

The navigation bar appears at the bottom of the mobile application screen. This bar includes the following tabs that you can use to access different applets and application launch pages:

-   **Cases**: displays the main case page. Use this applet launcher to access case management functionality.
-   **Notifications**: view a list of the notifications that have been pushed to the agent. Tap a notification in the list to see the details, then tap the details open the case.
-   **Settings**: manage settings for the mobile application.

## Applets and cards

Select an applet from the applet launcher screen. Each applet contains one or more screens used to display records that correspond to the applet function. The Active Cases applet, for example, displays a list of all active case records.

The cases in the list are displayed as cards, with the case status displayed at the top of the card. To use the cards:

-   Swipe a card left or right to see the available actions, then tap the desired action.
-   Tap a card to see the record details such as activity, related list, and escalations if any.
-   In the detail view:
    -   Tap the top menu to see additional actions, then tap the desired action.
    -   Select the back button to return to the list.

Applets provide a filter option if there is more than one case in the list. When you tap the applet, you see a list of filters that you can use to narrow down the list of cases.

## Agent applets

Customer service agents have access to the following set of applets.

|Applet|Description|
|------|-----------|
|My Cases|
|Needs Attention Cases|Cases that are waiting for the agent to take action. Includes cases in the Open, Awaiting Info, and Resolved states.|
|Active Cases|Cases that are assigned to the agent. Includes cases Open, Awaiting Info, and Resolved states.|
|New Cases|Cases in the New state.|
|Active Critical Cases|Priority 1 cases in the Open, Awaiting Info, and Resolved states.|

**Note:** Cases in these lists are sorted by the last updated date in descending order, with the most recent updated case displayed first.

## Customer service card layout

In a list view, case cards display the following information:

-   Case state
-   Case number
-   Short description
-   Contact
-   Account

In the major case list view, case cards display the following information:

-   Major case state
-   Case number
-   Short description
-   Account

## Case form related lists

Customer service agents can access the following Case form related lists.

<table id="table_ylq_rb5_dhb"><thead><tr><th>

Related list

</th><th>

Description

</th></tr></thead><tbody><tr><td>

SLAs

</td><td>

Displays a list of SLAs for a case. View the following information for SLAs included in this list: -   Task
-   SLA Stage
-   SLA Definition
-   Actual Elapsed Percentage
-   Actual Elapsed Time

 **Note:** Detail view is not available from the SLA related list.

</td></tr><tr><td>

Tasks

</td><td>

Displays a list of case tasks. View the following information for case tasks included in this list: -   State
-   Number
-   Subject
-   Assigned to
-   Priority

 **Note:** Detail view is not available from the Tasks related list.

</td></tr><tr><td>

Child Cases

</td><td>

Displays a list of child cases for a case. View the following information for child cases included in this list: -   Case number
-   State
-   Short description
-   Account
-   Contact

Click a child case to view additional details on the Case form.

</td></tr></tbody>
</table>## Notifications

Agents can receive notifications in the Customer Service mobile application when cases are assigned, are commented, or need attention. The following table lists the available notifications:

|Notification|Description|
|------------|-----------|
|Case assignment|When a case is assigned to an agent by someone else, a notification is sent to the agent selected in the **Assigned to** field. The notification includes the case number, state, priority, and short description.|
|Case comments|When information is added to a case in the **Additional comments** or **Work notes** fields by someone other than the assigned agent, a notification is sent to the user selected in the **Assigned to** field. The notification includes the case number, priority, and short description.|
|Needs attention flag is checked|When the **Needs attention** flag is checked on the Case form, a notification is sent to the agent in the **Assigned to** field. The notification includes the case number, state, priority, and short description.|
|Case escalation|When an escalation is raised, users who are part of the group that has permissions to approve are notified. The approvers review and approve them.|
|Change requests|When a change request is raised, users who are part of the group that has permissions to approve are notified. The approvers review and approve them.|

**Parent Topic:**[Mobile experience for Customer Service Management](../concept/customer-service-mobile-interface.md)

**Related topics**  


[Get started with the Customer Service mobile application](../task/install-customer-service-mobile-app.md)

[Applet launcher](https://www.servicenow.com/docs/access?context=sg-mobile-applet-launcher&version=yokohama&pubname=yokohama-mobile&ft:locale=en-US)

[Navigation bar](https://www.servicenow.com/docs/access?context=sg-mobile-tab-bar&version=yokohama&pubname=yokohama-mobile&ft:locale=en-US)

[Mobile push notifications](https://www.servicenow.com/docs/access?context=sg-mobile-push-notifications&version=yokohama&pubname=yokohama-mobile&ft:locale=en-US)

