---
title: Create a change request in Service Operations Workspace
description: Track modifications to a supported configuration item \(CI\). Use a change request form to record information such as the reason for the change, type, priority, and risk.
locale: en-US
release: xanadu
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 8
breadcrumb: [Change Management in Service Operations Workspace, Use, Service Operations Workspace for ITSM, IT Service Management]
---

# Create a change request in Service Operations Workspace

Track modifications to a supported configuration item \(CI\). Use a change request form to record information such as the reason for the change, type, priority, and risk.

## Before you begin

Role required: itil or admin

**Note:** You must have the sn\_devops.viewer role to view or add DevOps data to a change request.

## Procedure

1.  Perform one of the following actions to start creating a change request.

<table id="choicetable_vrd_rrt_tsb"><thead><tr><th align="left" id="d303338e55">

Option

</th><th align="left" id="d303338e58">

Description

</th></tr></thead><tbody><tr><td id="d303338e64">

**From any change list**

</td><td>

1.  Navigate to a list of changes.

**Note:** Following lists are available for change:

    -   Open
    -   Closed
    -   All
2.  Select **New**.


</td></tr><tr><td id="d303338e98">

**From an incident**

</td><td>

1.  Open an incident.
2.  From the record page, select **Create change request**.


</td></tr><tr><td id="d303338e119">

**From an interaction**

</td><td>

1.  Open an interaction.
2.  From the record page, select the drop-down beside **Create incident** and select **Create change**.


</td></tr><tr><td id="d303338e143">

**From a problem**

</td><td>

1.  Open a problem.
2.  Perform any of the following actions:
    -   From the record page, select the drop-down beside **Create problem task** and select **Create change request**.
    -   From the **Fix Tasks** tab, navigate to Change Requests list and select **New**.


</td></tr></tbody>
</table>2.  Select the change model that you want to create, and select **Next**.

    For information about change models, see [Change models](../../change-management/concept/change-models.md).

<table id="choicetable_ty1_knn_n3b"><tbody><tr><td id="d303338e206">

**Normal**

</td><td>

Any service change that is not a pre-approved change or an emergency change.

</td></tr><tr><td id="d303338e215">

**Pre-approved**

</td><td>

A pre-authorized change that is low risk, relatively common, and follows a specified procedure or work instruction.

</td></tr><tr><td id="d303338e224">

**Emergency**

</td><td>

An emergency change that bypasses group and peer review and approval, and goes straight to the authorization state for approval by the CAB approval group.

</td></tr><tr><td id="d303338e233">

**DevOps or DevOps Simplified**

</td><td>

Change model used for DevOps change requests. For more information on the DevOps model change, see [DevOps change models](../../enterprise-dev-ops/concept/devops-change-multimodel.md).**Note:** You must activate the DevOps Change Velocity application to use the DevOps models.

</td></tr></tbody>
</table>    **Note:**

    -   You can filter and search for the change type.
    -   When you create a change request from an interaction, only pre-approved change types are available.
3.  In the Overview tab, fill in the fields.

    You must provide the initial details of the change in the Overview tab.

    |Field|Description|
    |-----|-----------|
    |Short description|Brief description of the change.|
    |Description|Detailed description of the change.|
    |Justification|Reason for the planned change request, which helps approvers determine their decision.|

4.  Select **Save**.

    The change request is created along with **Scope and impact**, **Assignment**, **Schedule**, **Risk evaluation**, and **Change task** sections.

5.  Select **Add scope** in **Scope and impact** section.

    1.  On the form, fill in the fields.

<table id="table_v3g_jqy_2wb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration item

</td><td>

Configuration item \(CI\) that the change applies to. You can associate any type of CI with a change request, including service offerings. It also provides detailed access to SLA and availability requirements.

</td></tr><tr><td>

Service offering

</td><td>

Consists of one or more service commitments that uniquely define the level of service in terms of availability, scope, pricing, and packaging options. Service offering enables you to receive different features and their levels of performance for a given service.

</td></tr><tr><td>

Service

</td><td>

The business service that you want to make available for the change request.

</td></tr><tr><td>

Category

</td><td>

The category of the change, for example, **Hardware**,  **Network**, **Software**, **Other**, **DevOps**, and so on.**Note:** The section to **Add DevOps data** \(step 8 in this procedure\) is enabled only when the category is selected as **DevOps**. For DevOps models, the category is automatically set to DevOps.

</td></tr><tr><td>

Affected CIs

</td><td>

Associate CIs with a single change request.

</td></tr><tr><td>

Propose mass CI update

</td><td>

Apply the same update to a set of CIs for a specific CI class.

</td></tr><tr><td>

Propose single change

</td><td>

Propose a change to one CI from your list of affected CIs.

</td></tr><tr><td>

Refresh impact services

</td><td>

When you refresh impacted services, the Impacted Services/CIs, Business Applications, and Service Offerings related lists get updated based on the affected CIs. The records in each of the related list are unique even though the impact can be from a single affected CI.

</td></tr></tbody>
</table>    2.  Select **Save**.

6.  Select **Assign** in the **Assignment** section.

    1.  On the form, fill the fields.

<table id="table_u1d_ssf_2xb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Assignment group

</td><td>

Group assigned to the change.You can populate the **Assignment group** field automatically based on the support group available for the respective configuration item \(CI\). If the CI does not have any change group, then the field gets populated with the change group available for service offerings. The business rule **Populate Assignment Group based on CI/SO** triggers the functionality when an incident, problem, or change request is created or updated and when the **Assignment group** and the **Assigned to** field is empty. The following properties identify the field whose value populates the **Assignment group** field:

-   **com.snc.change\_request.ci\_assignment\_group.field\_name**: This change property identifies which CI field populates the **Assignment group** field.
-   **com.snc.change\_request.service\_offering\_assignment\_group.field\_name**: This change property identifies which service offering field populates the **Assignment group** field.
**Note:** The default value for the properties is support group for incident or problem and change group for change request respectively. The business rule **Populate Assignment Group based on CI/SO** is shipped as part of the development plugin ITSM CSDM Best Practice – Quebec plugin \(com.snc.best\_practice.itsm\_csdm.quebec\) and is available only for the new customers.

</td></tr><tr><td>

Assigned to

</td><td>

User assigned to the change request. If an assignment rule applies, the change is automatically assigned to the appropriate user or group.

</td></tr><tr><td>

Work notes

</td><td>

Information about how to resolve the change or steps taken to resolve it, if applicable. This note is for internal use. The work notes information is not visible to your customer.

</td></tr></tbody>
</table>    2.  Select **Save**.

7.  Select **Schedule** to schedule the implementation for the change.

    1.  On the form, fill in the fields.

<table id="table_esz_lry_2wb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Planned start date

</td><td>

Date to begin working on the change.

</td></tr><tr><td>

Planned end date

</td><td>

Date the change is planned to be completed.

 If the task type is  **Implementation**, the **Planned start date**  and **Planned end date**  values must fall within the planned start and end dates specified in the change request.

</td></tr><tr><td>

Actual start date

</td><td>

Start date of the implementation.

</td></tr><tr><td>

Conflict status

</td><td>

Status of the conflict.

</td></tr><tr><td>

Actual end date

</td><td>

Date when the change was implemented.

</td></tr><tr><td>

Conflict last run

</td><td>

Date when the conflict was last run.

</td></tr></tbody>
</table>    2.  Select **Schedule**.

        Select **Schedule** under **Next conflict-free card** to re-schedule the implementation of the change if there is any conflict.

        ![Change schedule](../image/change-schedule.png)

    3.  Select **Details** tab to view the Change details.

8.  Select **Add data** in the **DevOps data** section to add DevOps data to the change request.

    **Note:** You must have the sn\_devops.viewer role to add DevOps data to a change request or view DevOps data in an already created change record.

    1.  Specify the following values on the **Select associations** step: ![Select DevOps data type and its associations step](../image/select-assoc-sow.png)

<table id="table_ss2_yzz_vbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Data type

</td><td>

The type of data to associate with the change request.

 -   Artifact version
-   Release version
-   Build number
-   Work item


</td></tr><tr><td>

Data associations

</td><td>

The specific data to associate with the change request. You can select multiple artifact versions, build numbers, and work items.

 If you select Build number as the **Data type**, then you must also specify the application name and corresponding pipelines and build numbers. If you select Work item as the **Data type**, then you can filter the list of work items available for selection by applications and plans.

 You can search for build numbers by the branch name as well.

</td></tr></tbody>
</table>    2.  Select **Next** to open the **Review data** step. ![Review DevOps data step](../image/review-data-sow.png)

    3.  Navigate the tabs to verify that the associated data is mapped accurately.

        Update settings as needed.

        -   Work Items
        -   Commits
        -   Pull Requests
        -   Test Summaries
        -   Artifact Versions
        -   Software Quality Summaries
        -   Security Scan Summaries
    4.  Select **Submit**.

        **Note:** Once the commits are added in the DevOps data section, you can select **View source** corresponding to the Commits tile to view the source details of the commit like pipeline execution, branch, repository, and so on.

    5.  To modify the data that is associated with the change request, select **Edit DevOps data**.

        1.  Edit the data type and its associations from which DevOps data has been added in the **Select associations** step.
        2.  Review the DevOps data that’ll be associated to or removed from this change request in **Review data** step.
        3.  Select **Submit**.
9.  Select **Risk evaluation** to evaluate the risk for the change.

    The risk is calculated and is shown in Record information.

    The last evaluated risk value is displayed along with the timestamp.

10. Select **New** in **Change task** section.

    For more information to create a change task, refer [Create a change task in Service Operations Workspace](create-change-task-sow.md).

11. Select  **Request Approval** when the change request is ready to move to the next state.

    The state is moved forward based on the type of change request:

    -   Assess state: Group level approval for a normal change request. Approval records are automatically generated based on the  Change approval policies. You can conduct peer and technical reviews of the proposed change.
    -   Authorize state: Approval required by the business stakeholders, or by the Change Advisory Board.
    -   Scheduled state: Pre-approved standard changes.
    **Note:** To mail the change record, select the more options icon \(![More options icon.](../../change-management/image/more-options.png)\) in the content frame and select **Email**. Both the user who requested the change and the user who is assigned to the change are automatically populated in the list of recipients.

    To view the calendar, select **View Calendar** in the title bar of the Change Request form.

12. Select **Save**.


**Parent Topic:**[Change Management in Service Operations Workspace](../concept/change-sow.md)

**Related topics**  


[Work on a change request in Service Operations Workspace](work-on-change-sow.md)

[Standard change catalog](../concept/standard-change-catalog-sow.md)

[Create a change task in Service Operations Workspace](create-change-task-sow.md)

[Work on a change task in Service Operations Workspace](work-on-change-task-sow.md)

