---
title: Deploy a scenario
description: After publishing a scenario plan, deploy the scenario on your production.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/workplace-central/deploy-neighborhood-scenario.html
release: australia
product: Workplace Central
classification: workplace-central
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Working with Space Optimization, Use, Workplace Central, Workplace Service Delivery, Employee Service Management]
---

# Deploy a scenario

After publishing a scenario plan, deploy the scenario on your production.

## Before you begin

-   Make sure that you have created and published a scenario. For more information, see the following topics.
    -   [Create a scenario](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown)
    -   [Publish a scenario](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-central/publish-a-scenario.md)
-   Make sure that the scenario is assigned to you. You can only deploy scenarios that you own.

**Important:** If allocation changes in your instance impact the scenario, the system displays a warning on the Space Details panel. You must review the changes, edit the scenario accordingly, then select **Move to valid** before continuing. For more information about allocation changes, see [Reviewing allocation changes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-space-management/reviewing-allocation-changes.md).

\[Omitted image "wsd-central-review-changes.png"\] Alt text: Space details panel displaying a warning about reviewing allocation changes.

Role required: sn\_wsd\_spcmgmt.space\_planner

## About this task

After you publish a scenario, you must deploy the scenario to implement the changes in the production or main building data.

**Note:**

-   From Workplace Space Management version 1.15.0, deploying a scenario replaces existing allocations for a space with the allocations specified based on the **Group by** value.
-   For Workplace Space Management 1.14.0 or earlier versions, deploying a scenario replaces all allocations for the space with new allocations, regardless of the **Group by** value.

During deployment, you can collate all move requests raised for the scenario deployment into a single move project. Using a move project, you can track move requests and also schedule based on availability. For more information about move projects, see [Move project views, actions, and states](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-central/move-project-schedule-view.md).

**Note:** The option to create a move project appears only if there is at least one workplace user movement in the published scenario.

## Procedure

1.  Navigate to any one of the following locations:

    -   **All** &gt; **Workplace Central** &gt; **Workplace Central**.
    -   **All** &gt; **Scenario Planning** &gt; **My Scenario Plans**
2.  Select the **Space Optimization** icon \(\[Omitted image "space-optimization-icon.png"\] Alt text: Space optimization icon.\).

    The Space optimization dashboard opens.

3.  Select the scenario that you want to deploy.

    The scenario must be owned by you. To verify the owner of a scenario, you can check the **Owned by** field in the **Details** tab of the scenario.

4.  Select **Deploy**.

    The scenario is deployed and workplace cases are created for all the allocation and assignment changes you did on a scenario.

    **Important:** Your production data is updated with the scenario plan changes. Review the updated changes before proceeding with deployment.

    **Note:** You can't edit it a scenario after it’s deployed. You can only view the scenario by using the **View Options**.

5.  Navigate to **Space Deployment plan** and the **User Deployment** tab.

    The details of all the changes that you performed in the scenario are displayed. You can view details for building and floor where the change was applied, space, the type of changes, the current and the scenario value.

    \[Omitted image "wsd-space-deployment-plan-use.png"\] Alt text: Space deployment plan showing changes made to a scenario.

    For more information about the space deployment plan and user deployment plan, see the following topics:

    -   [Space Deployment Plan](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-central/space-deployment-plan.md)
    -   [User Deployment Plan](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-central/user-deployment-plan.md)
6.  In the dialog box that appears, if you want to create a move project for all the moves of the scenario, select the **Create move project** option.

    You can view all the move requests created after deploying the scenario in the move project. You can track and schedule a move request if necessary. For more information, refer to [Move Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-central/move-mgmt.md).

    **Warning:** The option appears only if there is at least one workplace user move in the published scenario.

7.  In the dialog box that appears, select **Yes** to deploy.


## Result

The scenario is deployed. After the scenario is deployed, the state of the scenario changes to **Deployed**. Each change triggers a workplace case in the Workplace Case Management application.

Depending on the type of change, the following workplace services types are created:

-   **Workplace User Assignment and Move Service via Scenario Planning**: Workplace service to update the user assignment and perform move activities related to the user.
-   **Workplace Assignment Type Service**: Workplace service to change the assignment type of a space.
-   **Workplace Allocation Change Service**: Workplace service to change the allocation of a space.

If you want to work on a move project for all the move requests in a deployed scenario, track the move project in the Move management workspace. To work on the move project, see [Work on a move project](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-central/work-on-a-move-project.md).

**Parent Topic:**[Working with Space Optimization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-central/working-with-space-optimization.md)

**Related topics**  


[Create a scenario]()

[Viewing or editing a scenario]()

[Review a scenario]()

[Publish a scenario]()

[Send a scenario for approval]()

[Change owner of a scenario]()

[View scenario change details]()

[Create a copy of an existing scenario]()

[View or edit space allocations of a building]()

[Work on a space assist request]()

[Map based space administration]()

