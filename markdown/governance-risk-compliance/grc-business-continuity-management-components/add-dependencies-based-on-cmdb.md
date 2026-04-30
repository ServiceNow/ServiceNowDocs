---
title: Add dependencies based on CI relationships in CMDB
description: Add an item by referencing its CI relationship to drill down to the item that is related directly to the dependency group. You can map the item's relationship with the dependency group while assessing the business impact analysis of an asset that is at risk.
locale: en-US
release: xanadu
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Identify critical dependencies, Assess impact categories and dependencies of process, Structured workflows for BIA, Using BCM Classic Workspace, Business Continuity Management, Governance, Risk, and Compliance]
---

# Add dependencies based on CI relationships in CMDB

Add an item by referencing its CI relationship to drill down to the item that is related directly to the dependency group. You can map the item's relationship with the dependency group while assessing the business impact analysis of an asset that is at risk.

## Before you begin

Role required: sn\_bcm.planner, sn\_bcm.program\_manager

## About this task

If it is an Application, Hardware, or Software dependency group that uses class extensions to populate configuration items and discover technologies or software, you can add items by filtering records based on the item’s relationship with the BIA dependency group. Or, you can add items to the group by simply selecting items from all the records.

For example, your business function, Accounts Receivable, may depend on the business application, Acrobat, to complete a business process. Therefore, the relationship is captured as Depends on::Used by. The Accounts Receivable business function depends on the Acrobat application item, and the Acrobat application is used by Accounts Receivable. Similarly, your business function may depend on other dependency groups like software technology or hardware to accomplish a business process.

## Procedure

1.  Navigate to **Business Continuity** &gt; **Business Continuity Workspace**.

2.  Click the lists icon \(![Lists icon](../../grc-workspace-audit/image/ListsIcon.jpg)\).

3.  Click the link to the record in the **Name** column in the **In Draft** state.

4.  To review a group and identify the items within each group, click the **Dependency Assessment** tab.

5.  To add an item to a dependency group, click the **Add New** button of that container.

6.  To filter items from all the records, click the **From all records** button.

    1.  Click **Next**.

    2.  Select items from the Add items pop-up.

    3.  Click **Add**.

7.  To filter an item based on its relationship with the dependency group, click **Based on CMDB dependencies \(Level 1\)**.

    1.  Click **Next**.

    2.  Select items based on the relationship.

    3.  Click **Next**.

    4.  Select the item.

    5.  Click **Add**.

        The dependency group grid lists items that depend on the BIA. If you add an item from all the records, then the **Relationship source** is **BCM**. If it is based on CMDB dependencies, then it is **CMDB**.

        **Note:** If you select an item **Based on CMDB dependencies \(Level 1\)**, only those items that are directly related or in the level 1 of dependency based on the relationship types identified in CMDB are listed in the Add items pop-up. On the other hand, if you select **From all records**, then all items from the respective table, irrespective of its relationship in CMDB, are displayed and are tracked up to a maximum of five levels.

8.  To view the details of the dependent item, click ![Information icon](../image/InformationIcon.png).

    The dependency details of the item that your business function depends on opens in a new tab. You can update the required recovery timeframe, required data backup, and the description of its use in the business function, and save the details.


**Parent Topic:**[Identify critical dependencies to prioritize recovery plans](identify-dependent-items-bia.md)

