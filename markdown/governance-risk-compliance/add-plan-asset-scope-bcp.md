---
title: Add an asset to the scope of a business continuity plan
description: Use the Scope tab to add an asset to the scope of the plan. If the business impact analysis \(BIA\) application is installed, you can view the primary elements defined in the plan template, its recovery time objective \(RTO\) and recovery point objective \(RPO\) details, and the business impact analysis.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Structured workflows for Business Continuity Planning, Using BCM Classic Workspace, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Add an asset to the scope of a business continuity plan

Use the **Scope** tab to add an asset to the scope of the plan. If the business impact analysis \(BIA\) application is installed, you can view the primary elements defined in the plan template, its recovery time objective \(RTO\) and recovery point objective \(RPO\) details, and the business impact analysis.

## Before you begin

Role required: sn\_bcm.admin, sn\_bcm.program\_manager, or sn\_bcm.planner

## Procedure

1.  Navigate to **Business Continuity** &gt; **Business Continuity Workspace**.

2.  Click the lists icon \(![Lists icon](../../grc-workspace-audit/image/ListsIcon.jpg)\).

3.  Click **In Draft** state in the Planning list.

4.  Click the link to the plan record in the **Name** column.

5.  Click the **Scope** tab.

    If the plan is created from a plan template, you can view the primary elements defined in the plan template.

6.  To add new scope to the plan, click **Add**.

7.  On the Add Items modal, select the plan asset.

8.  Click **Add**.

    Assets that are displayed in the Add Items modal belong to the element definition type identified in the **Primary element recovered** field of the plan template.

    If an asset has an approved BIA attached to it while adding the plan asset, then the approved BIA is automatically added in the **BIA** column of the asset.

    If the BIA is attached to the plan scope, then you cannot edit the RTO and RPO as they are values populated from the BIA.

    **Note:**

    -   If the BIA application is installed, then **RTO** and **RPO** fields are visible and non-editable. **BIA** field is visible and editable. You can attach a BIA by clicking the link BIA icon \(![Link BIA icon](../image/LinkBIAicon.png)\).
    -   If BIA is not installed, then **RTO** and **RPO** fields are visible and editable.
    -   If an approved BIA is attached to the plan, then **RTO**, **RPO**, and **BIA** fields are populated with values and they are read only and non-editable.
9.  To update a plan asset or to link a BIA to it, click the asset in the **Name** column.

    1.  Click the link BIA icon \(![Link BIA icon](../image/LinkBIAicon.png)\).

        If there is an approved BIA for the asset, then the BIA is automatically attached to the asset when you click the link. If you have adjusted the RTO and RPO values based on the criticality of an asset, then the Adjusted RTO and Adjusted RPO values take precedence over the system-calculated RTO and RPO values. The adjusted RTO and RPO values are displayed in the **Recovery Time Objective** and **Recovery Point Objective** fields when you click ![Link BIA icon](../image/LinkBIAicon.png).

    2.  Click **Save**.

10. To remove an asset from the plan list, select the item and click **Remove**.


