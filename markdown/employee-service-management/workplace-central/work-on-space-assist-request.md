---
title: Work on a space assist request
description: As a space planner, fulfill workplace space assistance requests. View the selected space plan of the request and deploy accordingly. You can also assign the request to another assignment group or a user.
locale: en-US
release: yokohama
product: Workplace Central
classification: workplace-central
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 7
breadcrumb: [Working with Space Optimization, Use, Workplace Central, Workplace Service Delivery, Employee Service Management]
---

# Work on a space assist request

As a space planner, fulfill workplace space assistance requests. View the selected space plan of the request and deploy accordingly. You can also assign the request to another assignment group or a user.

## Before you begin

Ensure that you have the following:

-   Workplace Central
-   Workplace Case Management
-   Workplace Space Management
-   For Floor map view, the floor maps must be created using Workplace Indoor Mapping Map studio.

Role required: sn\_wsd\_spcmgmt.space\_planner

## About this task

When a space request is submitted, a workplace case is created in the application. The Workplace Central Space Optimization dashboard enables you to view all the space request-related workplace cases at one place. As a space planner you can perform the following actions on a request:

-   View space requests submitted by users. You can view a request even if the user has not selected any option. Such workplace cases are set with the Work in progress state.
-   Track the total number of space requests created in the organization using the Space Optimization metrics board. You can also view the detailed list of the space requests.
-   Monitor the state of a space request and work on it accordingly.
-   View the selected space plan of a space request and deploy it.
-   Assign the space request to another assignment group or a user.
-   View the space plan on a floor map and visualize the seating before deployment.
-   Add work notes on the request. Work notes are displayed only to the space planner who is working on that request.
-   Add comments on the request so that the user can view. You can inform the progress or notify them with any information that they must know.

For a detailed information about the functionality, views, and states, refer to [Space request approvals, states, actions, and key features](../reference/space-request-states-and-view.md).

**Note:** You can deploy only a space request that is in the Approved state.

## Procedure

1.  Navigate to any one of the following locations:

    -   **All** &gt; **Workplace Central** &gt; **Workplace Central**.
    -   **All** &gt; **Scenario Planning** &gt; **My Scenario Plans**
    You can also open Workplace Central from the Employee Center directly. Navigate to **Workspaces** &gt; **Workplace Central**.

    The Workplace Analytics dashboard opens.

2.  On the left pane, select **Space Optimization** icon \(![Space optimization.](../images/space-optimization-icon.png)\).

    The Space optimization dashboard opens.

3.  To open a space request, do one of the following:

    -   In the **Scenarios** metrics section, select **All space requests**.
    -   In the **Space requests** section, select **View all**.
    Space Requests tab opens.

4.  Apply filters and sort options on the list to filter out the request.

5.  Select the workplace case of the space request that you want to work on.

    The workplace case opens in a separate tab and displays various details of the request. For detailed information of the various options displayed on the request, refer to [Space request approvals, states, actions, and key features](../reference/space-request-states-and-view.md).

6.  In the **Workplace Case** panel, you can perform any of the following:

    -   To assign the space request to another assignment group, edit the **Assignment group** field.
    -   To assign the space request to another user directly, specify the user in the **Assigned to** field.
    -   Scroll to view the request details and the variables provided by the requester.
7.  In the **Activity** panel, you can perform any of the following:

    -   Add comments in the **Comments** section and select **Post comments** to notify users with any information.
    -   Add work notes in the **Work notes** section and select **Post Work notes \(Private\)** to notify other space planners who are working on the request. Work notes are not displayed to the requester.
8.  Select the **Space plan** tab to view the space plan that is selected by the requester.

    You can also view the space on the map by selecting the **View spaces on map.**

    **Warning:** You can view the space plan only if the requester selects an option. If the requester has not selected any option, the **Space plan** tab doesn’t display any information.

9.  Select the **Approvals** tab to view the approver details of the space request.

10. Select the **Space Deployment plan** to view the space allocation details such as the type of change, current value, and the scenario value.

11. Select the **Floor map** tab to view the space plan on a floor map.

    The legend of the color related with each department is displayed on the right panel.

    **Note:** You can view the floor map only if the floor on which the space plan is made has a floor map configured. Ensure that you have configured Indoor Mapping as your map provider to view maps and have the Indoor Mapping components plugin. For more information, see [Customize the map properties](../../workplace-space-mapping/task/wsm-configure-map-properties.md).

12. After making changes, select **Save**.

13. To deploy the space plan, do the following:

    1.  Select the **Space Deployment plan** tab.

    2.  Review the space plan and allocations if required.

    3.  Click **Deploy**.

    The space plan selected in the request is deployed.


## Result

The space plan is deployed for the space request. The state of the request is changed to Deployment in progress until all the space allocations are implemented. For every allocation, a workplace case is created for it. When deployment is in progress, the following actions are performed:

-   If any one workplace case associated with an allocation is unsuccessful, that is, if the state is changed to Closed incomplete. In such cases, the deployment fails and the state of the space request is set to Closed incomplete. You can add comments if you want to notify the user with the failure details.
-   If all the workplace cases associated with allocations are successfully implemented, that is, they all have the state set to Closed complete, then the deployment is successful. When the deployment is successful, the space request is set to Closed complete.

**Parent Topic:**[Working with Space Optimization](../concept/working-with-space-optimization.md)

**Related topics**  


[Create a scenario](create-a-scenario.md)

[Viewing or editing a scenario](../concept/viewing-editing-scenario.md)

[Review a scenario](review-a-scenario.md)

[Publish a scenario](publish-a-scenario.md)

[Send a scenario for approval](send-a-scenario-for-approval.md)

[Change owner of a scenario](change-owner-of-a-scenario.md)

[Deploy a scenario](deploy-a-scenoria.md)

[View scenario change details](view-scenario-change-details.md)

[Create a copy of an existing scenario](create-copy-of-scenario.md)

[View or edit space allocations of a building](view-or-edit-space-alloctions-of-a-building.md)

[Map based space administration](../concept/map-based-space-administration.md)

