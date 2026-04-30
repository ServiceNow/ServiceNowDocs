---
title: Mobile Agent experience for Public Sector Digital Services
description: If you're a government agent, you can use the Mobile Agent app on your mobile device to create, update, and monitor the status of non-emergency service requests in the Public Sector Digital Services application. You can also get an overview of your case load, including your new and active cases.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 7
breadcrumb: [Use, Public Sector Digital Services \(PSDS\)]
---

# Mobile Agent experience for Public Sector Digital Services

If you're a government agent, you can use the Mobile Agent app on your mobile device to create, update, and monitor the status of non-emergency service requests in the Public Sector Digital Services application. You can also get an overview of your case load, including your new and active cases.

Use the Mobile Agent to review your case details and complete your case tasks. With a government service agent role, you can use the app to do the following tasks:

-   Get a quick overview of your case load.
-   Add comments or work notes to cases.
-   Review your case details, activity stream, and related information, such as the service level agreements \(SLAs\), case tasks, and related cases.
-   Edit case information.
-   Complete case tasks.

The following video highlights some of the capabilities of the ServiceNow® Mobile Agent app. Introduction to ServiceNow mobile apps.

**Note:** To use the Mobile Agent, the required plugins must be enabled by an administrator. If you're an administrator, see [Configure Mobile Agent for Service Request Playbook](psds-config-mobile-agent.md#) to get the information on configuring the Mobile Agent. For instructions on how to get started with the app after an administrator configures these settings, see [Get started with the Customer Service mobile application](https://www.servicenow.com/docs/access?context=install-customer-service-mobile-app&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US).

## Mobile Agent homepage

When you open the Mobile Agent and log in, an applet launcher is displayed with all the applets that are configured to that launcher.

The following example shows the homepage of the Mobile Agent, which displays an overview of cases.

![Homepage view of the mobile agent app showing an overview of cases and approvals.](../image/psds-agent-mobile-app-landing-page.png "Mobile Agent applet launcher for agents")

The applet launcher includes all the applets that you need to address or resolve service request cases. You have access to the following applets:

| | |
|---|---|
|New Service Request Cases|All service request cases that are assigned to you in the **New** state.|
|Active Service Request Cases|All service request cases that you have access to but haven’t been resolved or cancelled, including the cases in the **Open**, **Awaiting Info**, and **Resolved** states.|
|New Information Request Cases|All service request cases that are assigned to you in the **New** state.|
|Active Information Request Cases|All information request cases that you have access to but haven’t been resolved or cancelled, including the cases in the **Open**, **Awaiting Info**, and **Resolved** states.|

To launch an applet, select it in the app.

## Applets and cards

Each applet on the applet launcher screen displays the records that correspond to the applet function. The Active Service Requests applet, for example, when tapped, displays a list of all the active service request case records.

The following example shows a service request card view with a list of all active service request case records.

![Service request card view that shows a list of all active service request case records.](../image/psds-mobile-agent-case-card-list.png "Mobile Agent Service Request Case card list")

The cases in the list are displayed as cards, and the state of the case is displayed at the top of the card. For more information on the case states, see [Life cycle of a Public Service case](../reference/government-service-case-states.md).

Select a card to see the case record details. For example, you can see the case activity, related lists, and case escalations, if any.

You can narrow down or sort the list of cases by using the filter icon \(![Filter icon.](../image/psds-mobile-agent-filter-option.png)\).

## Service Request case cards in the Mobile Agent app

The case cards in the Mobile Agent app display information that is similar to what you would see if you were viewing a case in the CSM Configurable Workspace. For a full list of service request case fields and their descriptions, see [Service Request case form](../reference/service-request-case-form-new.md#).

The following example shows the case details card view. In this view, you can see the case number, case opened date, application type, priority, constituent, channel, primary purpose, and which agency is assigned to the case.

![Case details card view. For the text description, refer to the preceding text..](../image/psds-mobile-app-service-request-details.png "Mobile Agent service request case detail card")

As an agent, you can take several actions on service request cases in the Mobile Agent app from within the case cards. In the case detail view, you can select the More Actions icon \(![More actions icon.](../image/psds-mobile-agent-top-menu.png)\) to see a list of actions, and select the back button to return to the record list. These actions include:

-   Editing the case.
-   Closing the case.
-   Requesting more information from the constituent or contact.
-   Moving the case to review.
-   Moving the case directly to a decision.
-   Adding comments.
-   Escalating the case.

The following example shows the list of actions that you can take for a service request case. ![List of actions for a service request case.](../image/psds-mobile-app-service-request-actions.png)

For more information on the agent tasks in the Mobile Agent app, see [Using the Mobile Agent to perform agent tasks](psds-mobile-playbooks-perform-agent-manager-tasks.md).

## Information Request case cards in the Mobile Agent

The case cards in the Mobile Agent display information that is similar to what you would see if you were viewing a case in the CSM Configurable Workspace. For a full list of information request case fields and their descriptions, see [Information Request case form](../reference/information-request-case-form.md#).

The following example shows the case details card view. In this view, you can see the case number, case opened date, application type, priority, contact, channel, primary purpose, and which agency is assigned to the case.

![Case details card view. For the text description, refer to the preceding text.](../image/psds-mobile-app-information-request-details.png "Mobile Agent information request case detail card")

As an agent, you can take several actions on information request cases in the Mobile Agent from within the case cards. In the case detail view, you can select the More Actions icon \(![More actions icon.](../image/psds-mobile-agent-top-menu.png)\) to see a list of actions, and select the back button to return to the record list. These actions include:

-   Editing the case.
-   Closing the case.
-   Requesting more information from the requester.
-   Requesting fee approvals.
-   Evaluating similar information requests.
-   Moving the case directly to a decision.
-   Adding comments.
-   Escalating the case.

The following example shows a list of actions that you can take for an information request case. ![List of actions for an information request case.](../image/psds-mobile-app-info-request-actions.png)

For more information on the agent tasks in the Mobile Agent, see [Using the Mobile Agent to perform agent tasks](psds-mobile-playbooks-perform-agent-manager-tasks.md).

## Navigation bar

The navigation bar appears at the bottom of the mobile application screen. This bar includes the following tabs:

-   **Cases ![Cases icon.](../image/psds-mobile-agent-app-cases-icon.png)**

    Displays the main case page. Use this applet launcher to access the case management functionality.

-   **Saved ![Saved icon.](../image/psds-mobile-agent-app-saved-icon.png)**

    Displays the saved cases or case lists.

-   **Settings ![Settings icon.](../image/psds-mobile-agent-app-settings-icon.png)**

    Manages settings for the mobile application.


## Related lists in the Mobile Agent

You can access the related lists that are listed in the following table from within the case details.

<table id="table_ylq_rb5_dhb"><thead><tr><th>

Related list

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Work Orders

</td><td>

List of work orders that were created for this case. You must install the Field Service Management plugin \(com.snc.work\_management\) to view the work orders.

</td></tr><tr><td>

Case Tasks

</td><td>

Displays a list of case tasks. You can view the following information for the case tasks in this list: -   State
-   Number
-   Subject
-   Assigned to
-   Priority

</td></tr><tr><td>

SLAs

</td><td>

Displays a list of the service level agreements \(SLAs\) for a case. The following information for SLAs is included in this related list: -   Task
-   SLA Stage
-   SLA Definition
-   Actual Elapsed Percentage
-   Actual Elapsed Time

</td></tr><tr><td>

Blocked Tasks

</td><td>

List of blocking tasks that have been created for this case. A blocking task is something that prevents you from making progress toward a case resolution.

</td></tr><tr><td>

Related Parties

</td><td>

List of related parties, such as the contacts or constituents that were added to the case.

</td></tr><tr><td>

Related Cases

</td><td>

Displays a list of the related cases for a case. You can view the following information for the related cases that are included in this list: -   Case number
-   State
-   Short description
-   Contact

Select a related or child case to view the additional details on the Case form.

</td></tr><tr><td>

Attached Knowledge

</td><td>

Knowledge articles that were attached as a proposed solution to the case.

</td></tr><tr><td>

Documents

</td><td>

List of attached documents for the case.

</td></tr></tbody>
</table>