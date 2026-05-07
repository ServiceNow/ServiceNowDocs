---
title: Create a business continuity plan
description: Create a business continuity plan in BCM UIB Workspace.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 11
breadcrumb: [Structured workflows for BCPs, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Create a business continuity plan

Create a business continuity plan in BCM UIB Workspace.

## Before you begin

Role required: sn\_bcp.plan\_contributor or sn\_bcp.plan\_manager

The BCP Plan Manager \(sn\_bcp.plan\_manager\) now includes the Doc writer \(sn\_doc.writer\) role that provides read and write permissions to the document templates.

## Procedure

1.  Navigate to **Workspaces** &gt; **Business Continuity Workspace**.

2.  Navigate to **Planning** in the list view and select **New**.

    The **Create New Plan** form is displayed as shown in the example.

    ![Create New Plan form.](../image/create-new-plan-blank-form.png)

3.  Fill in the required fields in the **Details** tab of the **Create New Plan** form.

    For more information on the fields, see [Create New Plan form](../reference/create-new-plan-bcp-uib-ws-reference-form.md).

    The business continuity plan \(BCP\) is created in the **Draft** state and it’s displayed in the List view. The state and details of the business continuity plan are displayed in the tabs.

<table id="table_x2h_znl_hhc"><thead><tr><th>

Tab

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Overview**

</td><td>

Current state and overall state progression of the BCP.

</td></tr><tr><td>

**Details**

</td><td>

Details of the plan. Contains details such as its Name, Template, Type, Plan owner, BCM lead, Business unit, Department, Expires, Description, comments, and Activity panel.

</td></tr><tr><td>

**Scope**

</td><td>

Contains the asset types list. For the selected asset type, shows the Item, Types, Recovery time objective, Recovery point objective, Recovery tier. BIA, Status in source, Synchronized on columns for detailed info.

 **Note:**

The **source\_table\_fields** configuration applies to the **Scope** tab in the BCPs. These columns appear when you select **Add primary scope** or **Add related asset**.

 Add an asset to the scope of the plan and view the primary elements that are defined in the plan template. Beginning with the Xanadu release, the **Asset dependencies** tab now displays detailed information about the assets, replacing the Primary scope and Related asset toggles previously found in the **Scope** tab of the plan record. Additionally, the Type column in the **Scope** tab of the plan records has been renamed to Types column, enabling an asset to be categorized both as a primary scope and a related asset. The BIA column in the **Scope** tab has been updated from a document ID type to a reference type, enabling administrators to select and access the BIA record, update its information, and dot-walk to the plan record. It simplifies the process and saves time and effort. When two business impact analyses have identical asset dependencies, the most recent BIA is acknowledged as the source for these relationships.

 When creating a business continuity plan, you can enter details such as the Recovery Time Objective \(RTO\), Recovery Point Objective \(RPO\), Recovery Tier, and BIA link based on the primary asset in the plan record. Updating the dependencies refreshes the asset details in these columns with information from the latest unarchived BIA record. If the asset originates from a downstream BIA, the columns for Recovery Timeframe and Required Data Backup are revised to display the latest data for that asset.

</td></tr><tr><td>

**Add primary scope** UI action

</td><td>

**Add primary scope** and **Add related asset** UI actions: You can mark an asset as a primary scope, assign it as a related asset, or link it as a related asset to a primary scope within the plan. This approach simplifies the classification of asset types and enables you to view the relationships directly on the plan record page. It shows which assets are impacted when the primary scope is operationally down, thereby saving time and effort. You can monitor the gaps in the primary and related items.

The example shows that the IAD datacenter is added as both a related asset of a primary scope and as a primary scope itself.

![Primary scope.](../image/pri-related-assets-scope-tab.png)The **source\_table\_fields** configuration applies to the **Scope** tab in the BCPs. These columns appear when you select **Add primary scope**.

</td></tr><tr><td>

**Add related asset** UI action

</td><td>

The **Add related asset** action enables you to add a related asset and then relate it to a primary asset. For example, Abel Tuter, employed at the IAD datacenter, is added as a related asset.

![Related asset scope tab.](../image/related-asset-scope-tab.png)The **source\_table\_fields** configuration applies to the **Scope** tab in the BCPs. These columns appear when you select **Add related asset**.

</td></tr><tr><td>

**Asset dependencies**

</td><td>

Displays the Asset, BIA, Recovery time objective \(RTO\), Recovery point objective \(RPO\), Recovery tier, required Recovery Timeframe, Required Data backup, Primary source, Relationship source.

The **Asset dependencies** tab provides a Hierarchical view illustrating the relationships between parent assets and their child assets. In this example, it's shown that Abel Tuter is a related asset to the IAD data center.

![Related asset.](../image/asset-dep-tab-hierarchy-view.png)Since the user, Abel Tuter, was added manually, the Primary source column indicates it as a manual source.

You can track dependencies in the Hierarchical view and List view. You have the option to switch from the Hierarchical view to the List view, where all assets are displayed in the list format. The Hierarchical view displays all primary assets and up to 20 child assets. If a primary asset includes more than 20 assets, you can select the primary or related asset and it navigates you to the record view. Related assets are only present for the primary assets.

![List view.](../image/list-view.png)For example, the Business Application: Acrobat is considered a primary asset, while the Company: Adobe systems is identified as its related asset. The source of the asset is displayed in the Primary source column.

![Primary source.](../image/pri-source-column.png)You can add details from the dependent items in the plan as shown in the example.

![Add details from dependent items.](../image/add-details-from-dep-items-bcp.png)

</td></tr><tr><td>

**Documentation**

</td><td>

Record the recovery capabilities of the plan in the documentation sections. Contains details of the plan in the Sections panel and the **Create new section** tab. Similarly, contains informational fields on the plans such as Title, Description, Order, Contents.

</td></tr><tr><td>

**Associated plans**

</td><td>

Contains the associated plan types such as Upstream plans, Downstream plans, Related plans. For more information, see [Add associated plans and recovery teams](add-related-plans-recovery-teams-bcp-uib-ws.md).

</td></tr><tr><td>

**Recovery teams**

</td><td>

Recovery teams assigned for the business continuity plan. Contains the Name, Description, Groups, Users columns.

</td></tr><tr><td>

**Loss scenarios**

</td><td>

Loss scenarios that are applicable to the business continuity plan. Contains the Name and Description columns.

</td></tr><tr><td>

**Recovery tasks**

</td><td>

Details of the recovery tasks such as Planned order, Short description, Owner, Dependencies, Planned duration, Phase, Asset recovery level columns.

You can create a recovery task within the business continuity plan.![Recovery tasks tab.](../image/recovery-tasks-tab.png)A cyclic dependency occurs when two or more recovery tasks rely on each other, either directly or indirectly. Beginning with the Xanadu release, it’s possible to help prevent cyclic dependencies in recovery tasks, verifying that the same plan is not triggered multiple times.

![Plan record tabs.](../image/plan-record-tabs.png)For example, if the recovery task in Plan 1 triggers Plan 2, Plan 2 then triggers Plan 3, and Plan 3 subsequently triggers Plan 1, this sequence creates a cyclic dependency. An error message, similar to the example provided, is displayed to inform users that triggering the plan has resulted in a cyclic dependency and suggests selecting an alternative related plan. Choosing a different related plan in such cases helps avoid these issues during an event.

![Cyclic plan error message.](../image/cyclic-plan-error-message.png)If plans are activated beyond 10 levels or hierarchical links involving more than 10 levels of plans are established, an error message is displayed, advising the removal of the plan before the record can be saved.

![Plan levels.](../image/cyclic-plan-levels.png)Beginning with the Xanadu release, the recovery tasks are organized based on their dependencies. You have the flexibility to assign dependencies to the tasks, and the application then determines a sequence for these tasks based on the assigned dependencies. If there are tasks without any dependencies linking them, they can be handled simultaneously. You can edit the **sn\_bcp.sync\_order\_calculation\_task\_limit** property to change the count for the recovery task order so that it’s calculated synchronously.

![Order.](../image/recovery-tasks-order.png)The sequence of tasks depicted in the illustration is clarified with the example:

1.  Task 1 and Task 3 are independent of each other, enabling them to be executed at the same time, and they’re both assigned a planned order of 1.
2.  Task 5 depends on both Task 1 and Task 3 and therefore, it’s assigned a planned order of 2.
3.  Task 6 depends on Task 4, which has a planned order of 3. The planned order for Task 6 is then set at 4.
Tasks can be performed simultaneously, enabling several users to collaborate on the same plan at once. When a dependency is updated for a task and the task is saved, the planned order for the tasks is recalculated based on the removed dependency.

If you have over 500 recovery tasks and the dependencies are updated, the planned order of these recovery tasks is not updated instantly. Rather, an informational message is displayed, suggesting that the planned order of the recovery tasks be updated using the **Refresh tasks order** UI action.

![Refresh tasks UI action.](../image/refresh-tasks-order.png)The option to refresh the task order is also accessible from the menu in the plan record, as illustrated in the example.

![Refresh tasks in plan.](../image/refresh-tasks-order-in-plan-record.png)When you must reorder recovery tasks within a plan, a message is displayed that the reordering process may take some time. You can use the **Refresh tasks order** UI action to update the tasks order.

</td></tr></tbody>
</table>4.  Add a primary scope and its related assets in the **Scope** tab.

    1.  Update the dependencies by selecting the **Update dependencies** button.

    It pulls both related assets and their relationships. A message is displayed that the dependencies are being updated and you must refresh the page to view the updated dependencies.

    ![Updated dependencies.](../image/update-dependencies-plan-record.png)

    You can view dependency updates in the snapshot record.

    ![Snapshot.](../image/updated-snapshot-plan-record.png)

    The Parent item column in the **Added** tab shows the parent item of the new asset. All items that are dependent on the parent item are shown in the Item column as shown in the example. The Source column shows whether the source is from CMDB, Manual, or Downstream dependency in BIA. It’s used for BIA downstream. Selecting the BIA record link shows you that the dependencies are derived from this BIA record.

    ![Parent item.](../image/parent-item-snapshot-record.png)

5.  Review the **Finalized RTO** and **Finalized RPO** values columns in the **Scope** tab.

    With GRC: Business Impact Analysis, version 9.2.x, the **Finalized RTO** and **Finalized RPO** fields are introduced in the **Scope** tab.

    ![Finalized RPO.](../image/finalized-rpo-rto-plan.png)

    When you add a dependency in the **Scope** tab, the system retrieves the most recent Business Impact Analysis \(BIA\) and uses its "Finalized RTO" and "Finalized RPO" values for that specific dependency.

    Additionally, values for "Recovery Tier" and "BIA" are also retrieved and displayed in the plan record.

    When you add "Acrobat" as a primary scope to the plan record, the "Finalized RTO" and "Finalized RPO", "Recovery Tier", and "BIA' values are retrieved from the BIA and populated in the columns.

    ![Finalized RPO.](../image/acrobat-rto-plan.png)

    If you've already fetched a dependency and later update the BIA's RTO and RPO values and if the corresponding RTO fields for that dependency are empty, select**Update dependencies** to fetch the latest values from the BIA.

6.  To add a contributor from the list to the business continuity plan record, launch the **Contributors** panel by selecting the **Contributors** icon in the side-bar.

    The BCP contributors with the sn\_bcp.plan\_contributor role have read, write, and delete access to the business continuity plan. If you have the BCP manager, BCM lead, or plan contributor role, you can add or remove the contributors. The BCP contributors can edit the list of the contributors and edit the BCP.

7.  To revert an archived business continuity plan \(BCP\) to the **Draft** state, select the **Edit** button.

    Starting with BCM release 9.0.x, you can revert an archived business continuity plan \(BCP\) to the **Draft** state by selecting the **Edit** button on the form. It helps you to have more flexibility in managing business continuity plans and related records.

8.  To perform more actions on the BCP, select **More actions**.

    |Step|Description|
    |----|-----------|
    |**Select __Discuss__.**|Add the subject for the discussion and add participants that have access to the record. Include a brief message for the participants and select **Start discussion**.|
    |**Select __Generate MS Word__.**|Generate a report of the BIA, BCP, exercise, or crisis record in Microsoft Word format. The Microsoft Word copy of the BCP record is successfully generated that you can download.|
    |**Select __Generate PDF__.**|Generate a PDF of the BCP with the legacy or Smart Assessment. The PDF of the BCP record is successfully generated that you can download. In the Impact Assessments section of the PDF, details of the Smart assessment are covered, including questions and answers for RPO and RTO in a tabular format, along with dependencies, contributors, and attachments.|
    |**Select __Copy__.**|Create a copy of the BCP. BCP details, including its state, assessments, questions, and answers, are copied into the instance and displayed on the home page in the BCP section and BCP list. Confirm the name of the new BCP.|
    |**Select __360º view__.**|Generate 360º relationships for the BCP. A graphical presentation of the BCP and its relationships is displayed. Refresh the planned order for the recovery task|
    |**Select __Delete__.**|Delete the BCP record. A warning message is displayed that deleting the record results in an automatic deletion of related records, which may also cause a cascade of additional records to be deleted.|

9.  Select **Save**.

    The plan is saved in the **Draft** state and it’s displayed in the List view of the Planning records.

10. Select the **360º view** button to refresh the planned order for the recovery task.

11. Select the **Generate PDF** button to generate the BCP in a PDF format.

12. To create a copy of the BCP, select the **Copy** button.

13. Select **360º view** to generate the 360º relationships for the plan.

14. Select **Delete** to delete the plan.


-   **[Create New Plan form](../reference/create-new-plan-bcp-uib-ws-reference-form.md)**  
Use the Create New Plan form in BCM UIB Workspace to add the details about the business continuity plan \(BCP\).

**Parent Topic:**[Structured workflows for BCPs](../concept/bcp-tasks-performed-by-bcp-owner.md)

