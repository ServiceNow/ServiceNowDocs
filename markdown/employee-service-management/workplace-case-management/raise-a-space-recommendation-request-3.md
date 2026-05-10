---
title: Raise a space assistance request
description: Submit a workplace service request to get space allocation recommendations using the Workplace Service Portal. The Workplace Service Delivery space assistance provides you with the best space allocation plan options based on the space quantity and the department that you specify. You can select the most suitable allocation or none. Depending on your selection, the Space planner deploys the plan to use.
locale: en-US
release: australia
product: Workplace Case Management
classification: workplace-case-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 9
breadcrumb: [Requesting a workplace service, Workplace Case Management, Workplace Service Delivery, Employee Service Management]
---

# Raise a space assistance request

Submit a workplace service request to get space allocation recommendations using the Workplace Service Portal. The Workplace Service Delivery space assistance provides you with the best space allocation plan options based on the space quantity and the department that you specify. You can select the most suitable allocation or none. Depending on your selection, the Space planner deploys the plan to use.

## Before you begin

Ensure the following:

-   Workplace Central plugin is installed.
-   Workplace Case Management plugin is installed.
-   To view the space recommendations on the map, the floor map must be configured using Workplace Indoor Mapping.

Role required: sn\_wsd\_core.workplace\_user

## About this task

Specify the department and number of spaces that you want to assign to that department on a floor. Specify the location where you want to see the allocation recommendation. Depending on the specification submitted on the form, the system provides you with options containing the most suitable space allocation plans in that building. If the selected department exists on the floor that you selected, then the spaces are recommended nearby to that department.

You can select the best option and submit the selection. If an approval is configured, then the plan is sent for an approval to your manager. The selected space plan is directed to the space planner. The space planner reviews the plan and deploys it accordingly.

## Procedure

1.  Navigate to **All** &gt; **Workplace Core** &gt; **Workplace service portal**.

    The Workplace Service Portal opens.

2.  Open the General category.

    1.  Select **Catalog**.

    2.  Select **Browse by Categories**.

    3.  In the Workplace Services Catalog, select **General**.

        **Note:** If there are multiple catalogs configured on the portal, go to the Catalogs list and select **Workplace Services Catalog** &gt; **General**.

3.  Select **Space assist request**.

4.  On the form, fill in the fields.

<table id="table_ctm_hmd_cwb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Request name

</td><td>

Descriptive name for the request.

</td></tr><tr><td>

Allocate space by

</td><td>

The allocation type is set with the default allocation type set by your administrator.**Note:** If there is no allocation type specified, then you cannot proceed with the request.

</td></tr><tr><td>

Requested for

</td><td>

Option to specify the user for whom you are raising the space assistance request.

</td></tr><tr><td>

Select a department

</td><td>

Department based on which you want to allocate spaces. This option appears if **Department** is set in the **Allocate space by** field.

</td></tr><tr><td>

Select a Cost center

</td><td>

Cost center based on which you want to allocate spaces. This option appears only appears if **Cost center** is set in the **Allocate space by** field.

</td></tr><tr><td>

Select a workplace entity type

</td><td>

Workplace entity type based on which you want to allocate spaces. This option appears if **Workplace Entity** is set in the **Allocate space by** field.

</td></tr><tr><td>

Select a workplace entity

</td><td>

Workplace entity based on which you want to allocate spaces. This option appears if **Workplace Entity** is set in the **Allocate space by** field.

</td></tr><tr><td>

Reason for request

</td><td>

Option to select the reason for the request.

</td></tr><tr><td>

Space type

</td><td>

Option to specify what type of spaces you want.

</td></tr><tr><td>

Exact match \(Space type\)

</td><td>

Option to confirm that you want to see only the spaces that are an exact match to the selected space type.

</td></tr><tr><td>

Assignment type

</td><td>

Option to specify if you want flexible or permanent spaces.

</td></tr><tr><td>

Quantity/Capacity

</td><td>

Number of spaces that you want to allocate.

</td></tr><tr><td>

Region

</td><td>

Region where you want to make space allocation.

</td></tr><tr><td>

Campus

</td><td>

Campus where you want to make space allocation.

</td></tr><tr><td>

Site

</td><td>

Site where you want to make space allocation.

</td></tr><tr><td>

Building

</td><td>

Building where you want to make space allocation.

</td></tr><tr><td>

Exact match \(Building\)

</td><td>

Option to confirm that you want see only the spaces that are an exact match to the selected building.

</td></tr><tr><td>

Move-in date

</td><td>

Option to specify the date from when you want to implement the space allocation.

</td></tr><tr><td>

Exact match \(Move-in date\)

</td><td>

Option to confirm that you want see only the spaces that are available on the selected move-in date.This option is not available from Workplace Space Management version 1.12.0.

</td></tr><tr><td>

Move-out date

</td><td>

Option to specify the date until when you want to allocate the spaces.

</td></tr><tr><td>

Exact match \(Move-out date\)

</td><td>

Option to confirm that you want see only the spaces that are available until the selected move-out date.This option is not available from Workplace Space Management version 1.12.0.

</td></tr><tr><td>

Add attachments

</td><td>

Option to attach any supporting files if necessary.

</td></tr></tbody>
</table>5.  Select **Submit**.

    The request is submitted. After the submission, the request details page is opened.

6.  In the My request page, select **Space plans**.

    Refresh the page to view space plan options.

    The page displays options that have the most suitable space allocations for the select cost center or department on the selected floor, along with the match percentage.

7.  Review the options that are displayed.

    The match percentage is displayed under each option.

8.  View the space allocations on the map by selecting **View spaces on map**.

    **Note:** You can view the space allocations on the map only if the floor has a floor map configured.

9.  Select an option from the provided options.

    1.  In the My request page, select **Tasks/To-dos**.

    2.  In the **Select a space plan option**, select **View task**.

        A page with all the options that are displayed in the **Space plan** is displayed for selection.

    3.  Select **Select** next to the option that you want to proceed with.

    4.  If you do not want to select any option for any reason, select **None of the above**.

        **Note:** If you select **None of the above**, the request is closed and the state will be set to **Closed complete**

    5.  After selection, select **Submit**.


## Result

The option that you selected is submitted. At any time, you can view your selected option in the **Space plans** tab. After you submit the selection, the following actions are performed based on the approval process configured by your organization:

-   If an approval process is configured for your user profile, then the space request is sent to your manager for approval. The state of the space request changes to Awaiting approval.
    -   If your manager approves, the space request is sent for deployment and the state changes to Approved.
    -   If your manager rejects, then the space request is rejected and the state changes to Closed incomplete.
-   If your user profile doesn’t require an approval, then the space request is transferred to your organization's space planner and the state changes to **Approved.**

**Parent Topic:**[Requesting a workplace service](../../workplace-case-mgmt/concept/request-workplace-services.md)

**Parent Topic:**[Managing workplace locations](../concept/Creating-workplace-location-records-using-spce-mgmt.md)

**Parent Topic:**[Manage Workplace Central](../../workplace-central/concept/manage-workplace-central.md)

**Related topics**  


[Reconfigure an office space](../../workplace-case-mgmt/task/Reconfig-office-space-1.md)

[Raise help request for a workplace inquiry](../../workplace-case-mgmt/task/submit-gen-workplace-serv-req.md)

[Raise a move request for a space change](../../workplace-move-mgmt/task/request-desk-change.md)

[Request furniture for a space](../../workplace-case-mgmt/task/request-furniture.md)

[Submit a maintenance request](../../workplace-case-mgmt/task/submit-a-maintenance-request.md)

[Submit a catering request](../../workplace-case-mgmt/task/submit-a-catering-request.md)

[Submit heating and cooling request](../../workplace-case-mgmt/task/submit-heating-and-cooling-request.md)

[Submit a badge request](../../workplace-case-mgmt/task/submit-a-badge-request.md)

[Submit a tech support request](../../workplace-case-mgmt/task/submit-a-tech-support-request.md)

[Submit a cleaning request](../../workplace-case-mgmt/task/submit-a-cleaning-request.md)

[Submit an equipment request](../../workplace-case-mgmt/task/submit-a-equipment-request.md)

[Edit a workplace request](../../workplace-case-mgmt/task/edit-workplace-request.md)

[Submit an emergency maintenance request](../../workplace-case-mgmt/task/submit-emergency-maint-request.md)

[Submit a change event request for a reservation](../../workplace-case-mgmt/task/submit-change-event-reservation.md)

[Add a campus](add-a-campus.md)

[Add a building using Workplace Space Management](add-new-building-1.md)

[Add a floor using Workplace Space Management](add-a-floor-1.md)

[Add an area using Workplace Space Management](add-an-area.md)

[Add a room using Workplace Space Management](add-a-room.md)

[Add a space using Workplace Space Management](add-a-space.md)

[Allocate a cost center, department, or workplace entity](add-cost-center-department-floor.md)

[Configure a workspace or desk as flexible or permanent](assign-a-flex-perm-space.md)

[Update the measurement details of a workplace location](update-measurement-details-of-workplace-location.md)

[Change the status of a workplace location](change-active-status-of-workplace-location.md)

[Configure a BOMA type](configure-a-boma-type.md)

[Map a space type with BOMA type](map-a-space-type-with-boma-type.md)

[Create a Space Recommender rule](create-a-space-recommender-rule.md)

[Create a view-by configuration](create-view-by-config.md)

[Reviewing allocation changes](../concept/reviewing-allocation-changes.md)

[Approve a scenario](../../workplace-central/task/approve-a-scenario.md)

[View workplace scenarios](../../workplace-central/task/view-space-optimization-board.md)

[Approve a space assist request](../../workplace-central/task/approve-a-space-assist-request.md)

