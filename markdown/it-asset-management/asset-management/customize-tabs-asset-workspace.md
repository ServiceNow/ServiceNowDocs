---
title: Customize tabs in Asset Workspace
description: Adjust the content shown in the tabs of Asset Workspace or Hardware Asset Workspace views to meet your specific business needs.
locale: en-US
release: zurich
product: Asset Management
classification: asset-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Explore, Asset Management, IT Asset Management]
---

# Customize tabs in Asset Workspace

Adjust the content shown in the tabs of Asset Workspace or Hardware Asset Workspace views to meet your specific business needs.

## Before you begin

Role required: admin

## About this task

In the Asset Management Workspace, the content displayed in tabs such as All Assets and Hardware Assets in the Asset Estate view is determined by functions in the `AssetWorkspaceUtil` script include. These functions specify which table to use and what title to display for each tab. For example, the Asset estate page uses the getAssetEstateTabs function to fetch tab details, while other pages like Model Management and Inventory have their own specific functions. When a tab is selected, its index is used to fetch the corresponding item from the list, determining the displayed content.

**Note:** This task shows how to hide the All Assets tab on the Asset estate page. Using the same approach, you can hide other tabs in Asset estate, Model management, or Inventory pages. Modify the content displayed in a tab by updating the script include where details such as list titles and data sources are defined.

-   To properly hide a tab, you must deactivate the tab in UIB and comment out the corresponding JSON structure in the Script Include file.
-   The order of tab details in the functions within the Script Include file must match with the tab order in UI Builder. If not, the tabs displayed won’t match their corresponding configurations.

## Procedure

1.  In UIB settings, deactivate the All Assets tab by deselecting the **Active** check box for the Availability option.

    ![Deselect the Active check box for the Availability option.](../../hardware-asset-management/image/customize-tabs.png)

2.  The tab details in the Asset Estate page are fetched using the getAssetEstateTabs function defined in the script include.

    ![getAssetEstateTabs function defined in the script include.](../../hardware-asset-management/image/customize-tabs-script-include.png)

3.  Comment out the JSON section containing details related to the All Assets tab and save the Script Include file.

    ![Commenting out the JSON section containing details related to the All Assets tab.](../../hardware-asset-management/image/customize-tabs-json-comment.png)

4.  Reload the Asset estate page in the workspace.

    The All Assets tab has been hidden, but all the other tabs remain visible.


