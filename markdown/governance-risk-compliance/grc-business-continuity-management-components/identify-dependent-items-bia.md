---
title: Identify critical dependencies to prioritize recovery plans
description: Use the Dependency Assessment tab to identify items or assets that belong to a definite object type or a dependency group.
locale: en-US
release: australia
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Assess impact categories and dependencies of process, Structured workflows for BIA, Using BCM Classic Workspace, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Identify critical dependencies to prioritize recovery plans

Use the **Dependency Assessment** tab to identify items or assets that belong to a definite object type or a dependency group.

## Before you begin

Role required: sn\_bcm.planner, sn\_bcm.program\_manager

## About this task

Add a description of use and a timeframe to recover the item and provide data backup for the item. Assessing dependencies for a group helps you to know the underlying dependent items or assets of your business process. This assessment helps to prioritize critical dependencies that require recovery strategies to be established during the planning phase.

The BIA template that you use to create a business impact analysis has dependency groups associated to it. When you do an assessment, the dependency groups are automatically populated in the BIA. You can view them as Applications, Hardware, Software, Vendors, Workplaces, and others, each in its own container depending on how many of these groups are associated to the template. Each of them is a dependency group and you can add or remove items that belong to each group within its container.

**Note:** You can add or remove dependent items only if you are a user with appropriate access.

## Procedure

1.  Navigate to **Business Continuity** &gt; **Business Continuity Workspace**.

2.  Click the lists icon ![Lists icon](../../grc-workspace-audit/image/ListsIcon.jpg)\).

3.  Click the link to the record in the **Name** column in the **In Draft** state.

4.  To review a group and identify the items within each group, click the **Dependency Assessment** tab.

    You can click the container to know the group and the items that belong to the group. For example, if the group is Application, you can select an item related to the business process that is assessed like Enterprise Resource Planning or Customer Relationship Management.

5.  To add an item to a dependency group, click the **Add New** button of that container.

    -   If it is the Application, Hardware, or Software dependency group that uses class extensions to populate configuration items and discover technologies or software, see [Add dependencies based on CI relationships in CMDB](add-dependencies-based-on-cmdb.md).
    -   If it is Vendors or Locations group, add assets accordingly. You can add multiple items in the modal form. The grid in the container becomes editable and you can enter data in each cell for an item.
    The state of the dependency group changes to **Pending**.

    1.  Select an item from the list in the **Depends on** cell.

    2.  Double-click the **Description of Use** cell and enter the function or role of the item.

    3.  Select the time period in the **Required Recovery Timeframe** cell by which the item is to be recovered.

    4.  In the **Required Data Backup** cell, select the time period by which a data backup for the asset can be provided.

        While configuring an element in the Element Definition form, you can set the **Requires data backup** field as **Yes**. However, at the time when a BIA is created, the application copies the required data backup information from the element definition over to the dependency group of the BIA. If at this point, the required data backup is true for the dependency group, then the **Required Data Backup** column appears in the grid.

6.  To expand the dependency grid to full screen and edit the grid values, click the full screen icon \(![Full-screen icon](../image/FullScreenIcon.png)\).

    You can use the collapse screen icon \(![Collapse-screen icon](../image/CollapseScreenIcon.png)\) to collapse the grid back to the normal screen size.

7.  To update a group with dependent items, click the **Edit** button.

    The state of the dependency group changes to **Pending**.

8.  To remove a previously identified dependency item, select the item in the check box and click the **Remove** button.

    When you click **Remove**, the record is deleted from the Dependency table \[sn\_bia\_dependency\].

9.  Click **Complete** to complete the assessment of a group.

    Confirm that you have entered data in all the cells for the items before clicking complete. Otherwise, the system prompts you to fill in the incomplete cells. The container closes, the state is set to **Complete**, and you are directed to the next container. You cannot edit it unless you click the **Edit** button again.

10. Click **Save** to save the BIA and its dependency details.

11. Click **Submit for Review** to submit the BIA for a BCM program manager's review.

12. Click **Add Dependencies** to add dependent CIs collectively for all the dependency sections of the BIA.

    If the dependency groups depend on configuration items \(CIs\) in CMDB, then those CIs are linked as dependent items for the corresponding group in each section.

    **Note:** Dependency mapping of the dependency groups to their CIs is tracked up to five levels. Items within these five layers are added as dependent items to those Dependency Assessments that are only defined in the BIA template. For example, if Applications, Hardware, and Software are defined as Dependency Assessments in the Business Process BIA template, then only those CIs mapped up to five levels of the Dependency Assessments are added.

    To select and add CI as dependent item to each dependency group individually, see [Add dependencies based on CI relationships in CMDB](add-dependencies-based-on-cmdb.md).

    The filter condition in the Element definition is used to add specific configuration items \(CIs\) via the pop-up. The **Update dependencies** UI action also considers the element definition's filter and retrieves the related CIs of the configuration item listed in the **Applies to** field of the BIA. These relationships are retrieved from the CI Relationships table.


