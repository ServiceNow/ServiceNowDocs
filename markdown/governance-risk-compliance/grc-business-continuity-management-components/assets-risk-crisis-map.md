---
title: View assets at risk within the impacted area
description: View the list of resources that are at stake because of an alert threat that is near your business locations. Take actions to protect your resources and prevent major loss.
locale: en-US
release: zurich
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Crisis Management map, Using BCM Classic Workspace, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# View assets at risk within the impacted area

View the list of resources that are at stake because of an alert threat that is near your business locations. Take actions to protect your resources and prevent major loss.

## Before you begin

Role required: BCM admin or BCM Program Manager

## Procedure

1.  Navigate to **Business Continuity** &gt; **Business Continuity Workspace**.

2.  Click the map icon \(![Crisis map icon](../image/CrisisMapIcon.png)\).

3.  Click an alert record to open the alert in its detailed view.

    You can see various details of the alert on the form header.

    ![Assets at risk form header.](../image/AssetsAtRiskFormHeader.png "Assets at risk form header")

    -   The title of the alert
    -   The category of the alert
    -   Urgency of the alert whether it is going to strike immediately or expected in future
    -   Its severity in terms of loss
    -   Its certainty as to how likely it can strike
    -   Source of the alert feed
    -   The coordinates of the impacted area
    -   The source or the website from where the feed alert was received
    -   Its description
    ![Assets at risk in the map.](../image/AssetsAtRiskCrisisMap.png "Assets at risk in the map")

4.  Expand **Assets at Risk** section to view all the listed assets that are at risk.

    The **Assets at Risk** lists locations, datacenters, and core companies that lie within the impacted area of the alert. It also displays the count as to how many of these assets are impacted. You can view the impacted area on the map and take any of the suggested actions.

    The boundary of the alert's impacted area on the map is marked in mauve color. You can view the assets that are at risk within this impacted area on the map. If one of your location, datacenter, or a core company is impacted by the alert, you can edit the impacted zone to include the asset.

5.  To edit an impacted area, click the alert menu icon \(![Alert menu icon.](../image/AlertMenuIcon.png)\).

    1.  Click the **Edit Impact Area** option.

    2.  In the Edit Impacted Area pop over that opens on the map, select either Custom Shape or Custom Radius depending on the shape of the impacted area.

        -   Custom Shape: Select Custom Shape if the impacted area is polygonal shape.
        -   Custom Radius: If the impacted area is a circle.
    3.  Click and drag the vertex on the boundary of the impacted area to include the asset location.

        ![Edit impacted area.](../image/VertexAlertImpactedArea.png "Edit impacted area")

    4.  Click **Save**.

6.  Save or bookmark the URL of the alert to open the detailed view of the alert directly anytime.

7.  Click an asset card like a location or datacenter in the **Assets at Risk** section.

    The list view of the records opens up in a new tab.

8.  To view the details of the asset, click the link to the record in the **Name** column.

    You can view the complete details of the asset including its latitude and longitude.


