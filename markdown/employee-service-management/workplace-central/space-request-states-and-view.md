---
title: Space request approvals, states, actions, and key features
description: As a space planner, execute the space allocation requests raised in the organization using the Workplace Central Space Optimization dashboard. Using the Workplace Central Space Optimization dashboard to avoid multiple tasks about checking the availability, allocating spaces manually, and other process involved while space planning.
locale: en-US
release: zurich
product: Workplace Central
classification: workplace-central
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 8
breadcrumb: [Reference, Workplace Central, Workplace Service Delivery, Employee Service Management]
---

# Space request approvals, states, actions, and key features

As a space planner, execute the space allocation requests raised in the organization using the Workplace Central Space Optimization dashboard. Using the Workplace Central Space Optimization dashboard to avoid multiple tasks about checking the availability, allocating spaces manually, and other process involved while space planning.

## Functionality

The Workplace Service Portal enables workplace managers and other workplace users to raise a space recommendation request by specifying their requirements. The application generates various space plan options based on their specifications. When a space request is submitted, a workplace case is created in the application. The Workplace Central Space Optimization makes it easy for you, as a space planner to view only those workplace cases specifically generated from a space request.

As a space planner, you only have a few actions to perform to deploy a space plan. The application applies various algorithms on the location specified by the requester and generates multiple space plan options. The requester is provided with these space plan options to make a selection and submit. This pre-planning of space allocation makes it easier for you, as a space planner to deploy the space plan.

The Space Optimization dashboard provides you the metrics of the total number space requests raised and also view details of each space request. You can also view the details applying various filters and also based on the building for which it is requested for.

On the Space Optimization dashboard, you can view space requests using any one of the following options:

-   In the **Scenarios** metrics board, select **All space requests**.
-   In the **Space requests** section, select **View all** to view all the space requests.

## Approvals

If a space assist request requires approval, you can approve them using the Workplace Core approval configuration. You can approve a space assist request of only those users to whom you are assigned as a manager.

## Space request views

When you open a space request workplace case, a separate tab is opened with various details. You can view the details in different views.

-   **Request details**

    The space request opens in the Request details view by default. In the Request details, the details are split in three different panels as follows:

    1.  **Workplace case and Variables**: In the first panel, the Workplace case details and the variables provided by the requester is detailed.
        -   In the Workplace Case section, you can view the description of the request. You can also assign the space request to another assignment group or a user using the **Assignment group** and **Assigned to** field.
        -   In the Variables, section, you can view all the details specified on the form by the requester.
    2.  **Compose and Activity**: In the second panel, you can add comments and activities performed on the space request since its creation.
        -   In the Compose section, you can add comments and work notes in the request. Comments are also displayed to the requester whereas work notes are displayed only to the space planners working on the space request.
        -   In the Activity section, you can view all the details related to the actions performed on the space request, such as state changes, approvals, work notes and all.
    3.  **Attachments and Templates**: In the third panel, you can select two different views, that is, view or add attachments or view workplace case templates. You can select these options using the extreme right panel.
-   **Space plan**

    In the **Space plan** tab you can view the space plan option that is selected by the requester. You can also see the space plan on the floor map. The floor map is visible only if the floor has a floor map configured using the Workplace Indoor Mapping application and if you have installed the Indoor mapping component.

    -   The space plan also displays high-level information of the floor, building, and campus involved in the form of pills.
    -   The space plan provides detailed information of the spaces, floor, building, campus, site, and the region which is used for the allocation.
    **Important:** If the requester has not made any option selection, the **Space plan** tab does not display any details.

-   **Approvals**

    In the **Approvals** tab, you can view the approver details of the space request.

-   **Space Deployment plan**

    The **Space Deployment plan** displays the detailed information related to the allocation, the floor where the space is allocated, the type of change made in the plan, the current value and the scenario value. When you deploy the space plan, a workplace case is created and executed for each allocation. Until all the workplace cases are in progress, the deployment is not considered as done.

-   **User Deployment plan**

    The **User Deployment plan** displays the detailed information related to the neighbourhood user assignment-related changes if the scenario is grouped by neighbourhood.

-   **Floor map**

    In the Floor map view, you can view the floor map of the floor where the space plan is planned. The floor map is visible only if the floor has a floor map configured using Workplace Indoor Mapping and if you have installed the Indoor mapping component. You can perform the following actions on a floor map:

    -   Switch the locations using floor, building, and campus filters.
    -   Zoom in and out on the map. You can also double-click to zoom in.
    -   View the legend associated with each department on the right panel.

## Space request states

A space request since its creation undergoes several state changes. Based on the state of the request, you can perform actions and deployment.

A space request has the following states:

-   **Draft**: When a space request is created using the Workplace Service Portal, it is initially set to the Draft state for a few seconds and then changes to the Ready state.
-   **Ready**: After the request is created and the space plan options are still under generation, the status is set to the Ready.
-   **Work in progress**: After the options are generated and available to the requesters for selection, the status is set to Work in progress. The status is set as Work in progress until the requester selects an option.
    -   If the requester selects an option, then the request changes to the next state.
    -   If the requester selects the None option from the list of options provided, then the request is closed and the state is set to Closed complete.
-   **Awaiting approval**: If the requester selects an option and submits the request, one of the following actions is performed:
    -   If the requester's profile requires a manager approval, then the request is sent for an approval and the state is set to Awaiting approval.
    -   If the requester's profile does not require any approval, then the state is automatically changed to Approved.
-   **Closed incomplete**: When the request is sent for approval and if the approver rejects the request, that is, if the approver rejects the selected space plan, then the state changes to Closed incomplete.
-   **Approved**: If the approver approves the space request, then the state is changed to Approved. You can only deploy space requests that are in the Approved state. Also, the **Space Deployment plan** and the **User Deployment plan** displays the space selected in the space request if the request is Approved.
-   **Deployment in progress**: When you deploy the space plan selected in the space request, the state of the request changes to Deployment in progress. The following actions are performed when a request is in the Deployment in progress state:
    -   For every allocation, a workplace case is created and implemented.
    -   The deployment process is successful only if all the workplace cases are implemented successfully, that is, if all the cases are closed with the Closed complete state.
    -   The deployment process is unsuccessful if any one workplace case is not implemented successfully, that is, if any one case is closed with the Closed incomplete state.
-   **Closed complete**: If the deployment is successfully implemented, then the space request is closed and the state is set to Closed complete. If the deployment fails, then the space request is closed and the state is set to Closed incomplete.

**Parent Topic:**[Workplace Central reference](../concept/workplace-central-references.md)

**Related topics**  


[Components installed with Workplace Central](components-installed-with-workplace-central.md)

[Space Optimization - Key features and actions](space-optmization-features-and-actions-.md)

[Workplace Central Event planner](event-planner-key-features-actions-views.md)

[Scenario and Building - Views, states, settings, and key features](scenario-planning-views-actions-keyfeatures-.md)

[Move management key features and actions](move-mgmt-views-states-actions.md)

[Case Management - Key features, Actions &amp; Case details](case-management-key-features-actions-case-details.md)

[Schedule Plan details form](schedule-plan-details-form.md)

[Scenario details form](scenario-details-form.md)

[Space Deployment Plan](space-deployment-plan.md)

[User Deployment Plan](user-deployment-plan.md)

[Excel column lengths for move projects](move-excel-char-limit.md)

[Move conflicts for projects created via Excel upload](excel-upload-conflicts.md)

[Workplace Central troubleshooting](workplace-central-troubleshooting.md)

[Workplace Task form - Space Assignment task](workplace-task-space-assignment.md)

[Neighborhood User Assignment Rule form](user-assignment-rule-form.md)

[User Workplace Profile form](user-workplace-profile-form.md)

