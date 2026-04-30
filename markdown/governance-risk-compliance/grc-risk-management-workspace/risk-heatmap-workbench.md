---
title: Risk heatmap workbench
description: As an operational risk manager, you can visualize the risk details and better understand the risk posture of your entity by using the risk heatmap workbench in the Advanced Risk application.
locale: en-US
release: xanadu
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Analytics and reporting solutions for Risk Management, Risk Management, Governance, Risk, and Compliance]
---

# Risk heatmap workbench

As an operational risk manager, you can visualize the risk details and better understand the risk posture of your entity by using the risk heatmap workbench in the Advanced Risk application.

## Overview of the heatmap workbench

A risk heatmap is a graphical representation of your risk data where the individual values that are contained in a matrix are represented in colors that denote a meaning. You can use risk heatmaps to see your risk assessment results in a convenient, visually attractive, and succinct format. Starting in version 14.0, you can launch the risk heatmap workbench with the launch workbench icon \( ![Launch Workbench icon.](../image/risk_heatmap_workbench.png)\).

![Launch risk heatmap workbench from the risk workspace.](../image/heatmap-launcher.png)

## Features of the heatmap workbench

By using the risk heatmap workbench, you can view the following aspects for risks:

-   Risk count: Shows the number of risks that are in each cell on a heatmap such as when an X-axis factor like Impact is combined with a Y-axis factor like Likelihood. ![Risk count.](../image/risk_count.png)
-   Risk index: Shows the risk IDs in each cell and the details of each risk on the contextual side panel. ![Risk index.](../image/risk_index.png)
-   Risk name: Shows the names of all the risks in each cell. ![Risk name.](../image/risk_name_workbench.png)
-   Top Risks: Shows the top risks on the heatmap workbench. For example, if you select 10 from the Top Risks filter selection list, you can see all the top 10 risks that are associated with the selected Risk Assessment Methodology \(RAM\) on the heatmap.
-   Entity: Shows the risks that are associated with the specific entities and their downstream entities on the heatmap workbench. You can filter the risks that are associated with the specific entities that are defined in the RAM.

By pointing to each risk, you can quickly get details about the risk. For example, you can see who the risk owner is, the entity to which the risk belongs, and the category of the risk. The contextual side panel shows 20 entries at a time on a page. You can configure the total number of entries that you want to see. You can either view all the risks as cards or select a single risk and view its details. After you select a risk from the heatmap cell, you can see the details of that risk on the side panel. For example, you can see the risk rating, the risk response, the risk tracking, and the risk hierarchy. The activity log captures all the activities that are performed on a risk. If you click the more actions icon ![More Actions icon.](../image/more-details.png), you can see the following options:

-   **Open**: Provides the risk record.
-   **360° view**: Provides an overview of the associated entities, controls, risk statements, risk assessments, and risk response tasks.
-   **View assessment**: Provides an assessment summary of the risk.

## Reporting in the heatmap workbench

The heatmap workbench is the primary tool that you use for risk reporting and analysis. By looking at the Risk movement and Risk trend, you can visualize your organization's risk profile and share that information with your stakeholders.

![Risk movement trend.](../image/risk-movement-trend.png)

You can view the risk movement from inherent \(risk level without controls or mitigating actions\), to residual risk \(leftover risk after the implementation of controls\), finally to target risk \(risk level that you want to achieve in future\) on the heatmap workbench. This information helps you to analyze the assigned controls to mitigate if the risks are effective or not. The risk movement is available only for RAMs where the residual risk has the same factors as an inherent risk.

![Risk movement.](../image/risk-movement.png)

You can view the risk score movement across multiple assessments on the heatmap workbench. The risk trend shows how the risk has changed and analyzes how you have been managing the risk. The risk trend is available for the last five risk assessments. You can also disable the trend line on the heatmap for a clear and less cluttered view.

![Risk trend.](../image/risk-trend.png)

## Risk appetite in the heatmap workbench

You can view the status of the risk appetite on the heatmap workbench. The risk appetite trend is also available on the heatmap. You can also see the details of the risk to get an understanding of the risk appetite status.![Risk appetite on the heatmap.](../image/risk-appetite-heatmap.png)

## Filtering in the heatmap workbench

You can filter the data that you see on the heatmap workbench. For example, let's say that you see 40 entries on the heatmap and you'd like to filter those risks where the entity is ACME Global. You can use the condition builder and apply your filters. After the filters are applied, the heatmap is refreshed and displays the data based on the filter conditions that you have applied. For more information on how to filter the data, see [Filter data in the risk heatmap workbench](../task/filtering-in-the-risk-heatmap.md). The ability to filter is only available in the workbench view. You can save the frequently used filters in the My saved filters section.

## Downloading and copying in the heatmap workbench

You can download or copy the risk heatmap information to include in reports or share with relevant stakeholders as needed. The download ![Download heatmap icon.](../image/download-heatmap-icon.png) icon enables you to download the heatmap as an image. The copy ![Copy heatmap to clipboard icon.](../image/copy-heatmap-icon.png) icon enables you to copy the heatmap information in your clipboard. You can then paste it into emails, reports, presentations, or other documents to share the visual data representation as needed.

## Searching in the heatmap workbench

As a risk user, while looking for a particular risk, you can quickly search a risk by the name, owner, or any of the other information that is shown in the card. You can also filter the data by searching the risks. In the contextual side panel, you can enter your keyword in the search field and the filtered results are visible.

**Note:** The search feature considers the risk name, risk description, and fields that are shown in the card. For example, if you search for the word Operational, then all risks that have the word operational will appear in the search result.

## Immersive view of the heatmap workbench

With the immersive view of the heatmap, you can view the expanded form of the heatmap where the X-axis and the Y-axis values are highlighted. The benefit of this view is that if you have too much information in one zone, you can focus on that zone and analyze each risk. The pagination enables you to see all records. You can point to a risk to quickly understand more details about the risk. You can also view the different values of both the axes by clicking the value. For example, let's say that in the heatmap, the X-axis has the values low, medium, and high and the Y-axis has the values unlikely, likely, and almost certain. You can click any value in both the axes to see the risks for that combination.

**Parent Topic:**[Analytics and reporting solutions for Risk Management](../../../use/dashboards/application-content-packs/grc-risk-mgmt-content-pack.md)

