---
title: Add asset and scope to the BCP
description: Add an asset and the scope to the business continuity plan \(BCP\). You can then view the primary elements in the BCM Configurable Workspace.
locale: en-US
release: yokohama
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Structured workflows for BCPs, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Add asset and scope to the BCP

Add an asset and the scope to the business continuity plan \(BCP\). You can then view the primary elements in the BCM Configurable Workspace.

## Before you begin

Role required: sn\_bcm.admin, sn\_bcm.program\_manager, or sn\_bcm.planner

## About this task

You can select a primary asset and track its related assets in the plan. You can also designate the same asset as either a primary or a related asset within the plan, as indicated in the Types column of the plan record. To add the related assets in the **Asset dependencies** tab, select the **Update Dependencies** button in the plan. The source of the relationship is displayed in the Primary Source column, which includes sources such as Configuration Management Database \(CMDB\), Manual, BIA upstream, or BIA downstream.

You can check the Types column in the **Scope** tab to see the classification of an asset. An asset can be classified as a primary scope type, a related asset type, or both. To understand the source of the relationship for related assets, such as an upstream BIA or a CMDB asset from which the dependency originates, refer to the Relationship Source column in the Plan Asset and Snapshot records. The Relationship source column in the **Asset dependencies** tab shows the actual record responsible for pulling this relationship. If two business impact analyses \(BIAs\) have the same asset dependencies, the most recent BIA is recognized as the relationship source and it is shown in the Types column in the plan.

You can use the Hierarchical view in the plan form to view the parent-child relationship of the assets. You can toggle the view to display either the List view or the Hierarchical view. When the dependencies are updated, the values in the columns of the **Scope** and **Asset dependencies** tabs are updated and color-coded for reference as shown in the examples:

-   BIA
-   Recovery time objective \(RTO\)
-   Recovery point objective \(RPO\)
-   Recovery tier \(RT\)

You can use the updated dependencies from the most recent BIA record to conduct a dependency assessment on an asset. Employing these updated dependencies enables you to accurately carry out the business impact analysis. Additionally, it assists in determining the essential recovery timeframe and data backup needs for the assets, which are then shown in the Required Recovery Timeframe and Required Data Backup columns of the BIA record.

![Data in scope tab.](../image/data-pulled-in-scope-tab.png)

The Hierarchical view is used to evaluate the BIA, Recovery time objective \(RTO\), Recovery point objective \(RPO\), and Recovery tier \(RT\) values between the primary and related assets within a plan. The color coding helps Business Continuity Management \(BCM\) planners to compare these metrics:

-   Rows where the RTO or RPO value for the primary asset is lower than that of the related asset are marked in Red.
-   Rows where the RTO or RPO value for the primary asset exceeds that of the related asset are marked in Green.
-   Rows where the RTO or RPO values for the primary and related assets are identical are marked in Yellow.
-   Rows where the RTO or RPO values for the primary assets are missing remain uncolored.

For example, if the RTO value for the primary asset exceeds that of the related asset, it is marked in Green. If the RTO value for the primary asset is less than that of the related asset, it is marked in Red.

![Columns updated.](../image/columns-plan-record-updated.png)

When you hover over the information icon in the column, it shows the comparison data for the primary and related asset as shown in the example.

![Hovering data.](../image/hovering-columns.png)

## Procedure

1.  Navigate to **Workspaces** &gt; **Business Continuity Workspace**.

2.  In the List view, navigate to **Planning** and select the link to the plan record in the **Name** column.

3.  Select the **Scope** tab and add primary scope for the business continuity plan.

    If the plan is created from a plan template, you can view the primary elements defined in the plan template.

4.  Select the **Asset dependencies** tab.

    Asset dependencies show the relationships of the assets and allow users to assess the risk or gaps when the assets are operationally down. The example shows how to add an asset type to the business continuity plan.

    The purpose of **source\_table\_fields** is to set the columns for the modal based on the asset types. The following examples show the columns that appear when you select **Add primary scope** for Applications and Business Processes asset types.

    ![Assets shown when you select Add primary scope for the Applications asset types.](../image/assets1.png)![Assets shown when you select Add primary scope for the Business Processes asset types.](../image/assets2.png)

    A sample plan with various asset types is shown in the example.

    ![Business continuity plan with various asset types.](../image/bcp-plan-sample-asset-types.png)

5.  Select **Save**.


**Parent Topic:**[Structured workflows for BCPs](../concept/bcp-tasks-performed-by-bcp-owner.md)

