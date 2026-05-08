---
title: Create a change request in Service Operations Workspace
description: Track modifications to a supported configuration item \(CI\) by using a change request. You can record information such as the reason for the change, and the change type, priority, and risk.
locale: en-US
release: australia
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 12
breadcrumb: [Change Management in Service Operations Workspace, Operating IT services in your organization, Service Operations Workspace for ITSM, IT Service Management]
---

# Create a change request in Service Operations Workspace

Track modifications to a supported configuration item \(CI\) by using a change request. You can record information such as the reason for the change, and the change type, priority, and risk.

## Before you begin

Role required: itil or admin

**Note:** You must have the sn\_devops.viewer role to view or add DevOps data to a change request.

## Procedure

1.  Create a new change request.

<table id="choicetable_vrd_rrt_tsb"><thead><tr><th align="left" id="d170927e55">

Source

</th><th align="left" id="d170927e58">

Description

</th></tr></thead><tbody><tr><td id="d170927e64">

**Change list**

</td><td>

1.  Navigate to a list of changes.

**Note:** The following lists are available:

    -   Open
    -   Closed
    -   All
2.  Select **New**.


</td></tr><tr><td id="d170927e100">

**From a change template**

</td><td>

1.  Navigate to a list of changes.

**Note:** The following lists are available:

    -   Open
    -   Closed
    -   All
2.  Select **New**.
3.  Select **Templates**.
4.  Search for and select the required template.
5.  View the new change request record created using the selected template by selecting **Continue**.
 **Note:** When you select an existing template, information in the predefined fields will be populated. Template fields are either read-only or mandatory depending on the template field policies configured while creating the template.

For more information on change templates, see [Create and propose a change template in Service Operations Workspace](create-change-template-sow.md).

</td></tr><tr><td id="d170927e165">

**Incident**

</td><td>

1.  Open an incident.
2.  In the incident record form, select **Create change request**.


</td></tr><tr><td id="d170927e187">

**Interaction**

</td><td>

1.  Open an interaction.
2.  In the interaction record form, from the **Create incident** drop-down list, select **Create change**.


</td></tr><tr><td id="d170927e211">

**Problem**

</td><td>

1.  Open a problem.
2.  On the problem record page, from the **Create problem task** drop-down list, select **Create change request**.


</td></tr></tbody>
</table>2.  Select the change model that you want to create, and select **Continue**.

    You can filter and search for the change type.

    The following change types are available:

<table id="table_qbj_vqx_mhc"><thead><tr><th>

Change model

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Normal

</td><td>

Any service change that is not a pre-approved change or an emergency change.

</td></tr><tr><td>

Standard

</td><td>

A pre-authorized change that is low risk, relatively common, and follows a specified procedure or work instruction.

</td></tr><tr><td>

Emergency

</td><td>

An emergency change that bypasses group and peer review and approval, and goes straight to the authorization state for approval by the CAB approval group.

</td></tr><tr><td>

DevOps or DevOps Simplified

</td><td>

Change model used for DevOps change requests.To use the DevOps models, you must activate the DevOps Change Velocity application.

</td></tr></tbody>
</table>    For more information, see [Change models](../../change-management/concept/change-models.md).

    **Note:** When you create a change request from an interaction, only pre-approved change types are available.

3.  In the Overview tab, fill in the fields.

    You must provide the initial details of the change in the Overview tab.

    |Field|Description|
    |-----|-----------|
    |Short description|Brief description of the change.|
    |Description|Detailed description of the change.|
    |Justification|Reason for the planned change request, which helps approvers determine their decision.|

4.  Select **Save**.

    The change request is created along with **Scope and impact**, **Assignment**, **Schedule**, **Risk evaluation**, and **Change task** sections.

5.  Provide the scope and impact information for the change.

    1.  Select **Add scope** in **Scope and impact** section.

    2.  On the form, fill in the fields.

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
</table>    3.  Select **Save**.

6.  Assign the change request to relevant user or assignment group.

    1.  Select **Assign** in the **Assignment** section.

    2.  On the form, fill the fields.

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
</table>    3.  Select **Save**.

7.  Schedule the implementation for the change and view conflicts detected.

    **Note:** The conflict detection feature is unavailable if the **Exclude from conflict detection** check box in the Change Request form is selected. For more information, see [.](../../change-management/task/t_RunManualConflictDetection.md#)

    1.  Select **Set schedule**.

    2.  On the Schedule page, enter the planned start and end date.

    3.  In the **Conflict** tab, the **Schedule and conflicts** section lists any detected conflicts.

        The **Conflict last run** field displays the date when the conflict detection was last run. You can view the details of the detected conflicts in the Related records tab.

        **Note:** When a conflict detection process is in progress, the **Check conflicts** button changes to **View progress**.

        The details of detected conflicts listed in the following table are displayed in the **Conflict** section.

<table id="table_esz_lry_2wb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Change

</td><td>

The current change request for which conflicts have been detected.

</td></tr><tr><td>

Type

</td><td>

The type of conflict detected. The following types of conflicts are displayed:

-   **CI Already Scheduled**
-   **Parent CI Already Scheduled**
-   **Child CI Already Scheduled**
-   **Not in Maintenance Window**
-   **Parent Not In Maintenance Window**
-   **Child Not In Maintenance Window**
-   **Blackout**


</td></tr><tr><td>

Schedule

</td><td>

The blackout or maintenance schedule the detected conflict is associated with.

</td></tr><tr><td>

Conflicting Change

</td><td>

The change that is in conflict with the current change request, if any.

</td></tr><tr><td>

Affected CI

</td><td>

The CI associated with the conflict detected.

</td></tr><tr><td>

Impacted Services

</td><td>

The services impacted by the detected conflict.

</td></tr><tr><td>

Last checked

</td><td>

Date when the conflict detection process was last run.

</td></tr></tbody>
</table>        For more information, see [Conflict detection](../../change-management/concept/c_ConflictDetection.md).

        **Note:** You can also run the conflict detection process manually by selecting **Check conflicts**.

    4.  Reschedule your current change request if there is any conflict.

        1.  Navigate to the **Schedule** page.
        2.  Select the edit icon ![pencil icon](../../configuration-data-management/image/icon-edit-pencil.png) in the **Current** card.
        3.  Select the new planned start and end dates.
        Alternatively, you can reschedule the implementation of the change to the next time and date there is no conflict by selecting **Schedule** in the **Next conflict-free** card.

        ![Change schedule Next conflict free card](../image/change-schedule.png)

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

11. Associate the change with a product or service release.

    This option is available only if you have the Digital Product Release v2.4 installed. For more information, see [Associating change requests with releases in Service Operations Workspace](../../digital-product-release/concept/dpr-sow-integration-cr.md).

    1.  Select **Assign** in the **Related release** card on the contextual side panel.

    2.  In the Assigned to release dialog box, select the release you want to associate with the change request.

    3.  If its a multi-product release, select the product within the release.

    4.  Select the phase of the selected release to which you want to link the change request.

    5.  Add work notes to provide context for the assignment.

    6.  Select **Assign**.

12. Import affected configuration items \(CIs\) from release phases to a change request.

    This option is available after the change request is associated with a release that has configuration items mapped to its release phases.

    1.  Select **Related records** tab and select the **Affected CIs** option.

    2.  Select **Add CIs from release phase**.

    3.  Select **Yes** to confirm adding CIs from the release phase into the change request.

        The available CIs from the release phase of the associated release are added as affected CIs and listed.

        The import operation runs asynchronously. A notification is displayed when the operation completes. Refresh the list manually to see the newly added CIs.

13. Select  **Request Approval** when the change request is ready to move to the next state.

    The state is moved forward based on the type of change request:

    -   Assess state: Group level approval for a normal change request. Approval records are automatically generated based on the  Change approval policies. You can conduct peer and technical reviews of the proposed change.
    -   Authorize state: Approval required by the business stakeholders, or by the Change Advisory Board.
    -   Scheduled state: Pre-approved standard changes.
    **Note:** To mail the change record, select the more options icon \(![More options icon.](../../change-management/image/more-options.png)\) in the content frame and select **Email**. Both the user who requested the change and the user who is assigned to the change are automatically populated in the list of recipients.

    To view the calendar, select **View Calendar** in the title bar of the Change Request form.

14. Select **Save**.


-   **[Create and propose a change template in Service Operations Workspace](create-change-template-sow.md)**  
Create, customize, and then propose a change template aligned to a change model.

**Parent Topic:**[Change Management in Service Operations Workspace](../concept/change-sow.md)

**Related topics**  


[Work on a change request in Service Operations Workspace](work-on-change-sow.md)

[Standard change catalog](../concept/standard-change-catalog-sow.md)

[Create a change task in Service Operations Workspace](create-change-task-sow.md)

[Work on a change task in Service Operations Workspace](work-on-change-task-sow.md)

[Create a Change Advisory Board \(CAB\) definition](cm-create-cab-definition-sow.md)

[Create a CAB meeting](cm-create-cab-meeting-sow.md)

[Conduct a CAB meeting in the CAB workbench](cm-manage-cab-meeting-workbench-sow.md)

