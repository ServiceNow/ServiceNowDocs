---
title: Customize theme-able empty state images for your theme
description: Customize default theme-able empty state images for your Next Experience and Theme Builder themes using the theme's Imagery record.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Theme-able empty state images, Working with themes, Configure, Next Experience UI, Configure UIs and portals, Configure user experiences]
---

# Customize theme-able empty state images for your theme

Customize default theme-able empty state images for your Next Experience and Theme Builder themes using the theme's Imagery record.

## Before you begin

Role required: admin

## About this task

**Important:** You can customize empty state images for Workspaces, but customization is not supported in the Core UI.

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **Themes** &gt; **UX Themes**.

2.  Select your theme from the UX Themes table.

    The UX Theme record for your chosen theme appears.

3.  From the **Compositional App Theme** tab, select the **Imagery** record.

4.  From the Imagery style record, enter the following empty state image theme hooks into the **Style** field.

    ```
    {
        "properties": {
            "--now-illustration--add-attachment-sm--url": "",
            "--now-illustration--add-attachment-md--url": "",
            "--now-illustration--add-attachment-lg--url": "",
            "--now-illustration--add-data-sm--url": "",
            "--now-illustration--add-data-md--url": "",
            "--now-illustration--add-data-lg--url": "",
            "--now-illustration--completed-tasks-sm--url": "",
            "--now-illustration--completed-tasks-md--url": "",
            "--now-illustration--completed-tasks-lg--url": "",
            "--now-illustration--error-sm--url": "",
            "--now-illustration--error-md--url": "",
            "--now-illustration--error-lg--url": "",
            "--now-illustration--first-time-user-sm--url": "",
            "--now-illustration--first-time-user-md--url": ""
            "--now-illustration--first-time-user-lg--url": "",
            "--now-illustration--interrupted-sm--url": "",
            "--now-illustration--interrupted-md--url": "",
            "--now-illustration--interrupted-lg--url": "",
            "--now-illustration--no-data-sm--url": "",
            "--now-illustration--no-data-md--url": "",
            "--now-illustration--no-data-lg--url": "",
            "--now-illustration--no-search-results-sm--url": "",
            "--now-illustration--no-search-results-md--url": "",
            "--now-illustration--no-search-results-lg--url": "",
            "--now-illustration--offline-sm--url": "",
            "--now-illustration--offline-md--url": "",
            "--now-illustration--offline-lg--url": "",
            "--now-illustration--permissions-sm--url": "",
            "--now-illustration--permissions-md--url": "",
            "--now-illustration--permissions-lg--url": "",
            "--now-illustration--unconfigured-sm--url": "",
            "--now-illustration--unconfigured-md--url": "",
            "--now-illustration--unconfigured-lg--url": "",
            "--now-illustration--no-activities-sm--url": "",
            "--now-illustration--no-activities-md--url": "",
            "--now-illustration--no-activities-lg--url": "",
        }
    }
    ```

5.  Add your custom image in one of the following ways.

    -   Add image to UX Style Assets list.
        1.  On the **UX Style Assets** tab, select **New**.
        2.  Select the search icon![Search](../image/SearchIcon.png)next to the **Asset** item.
        3.  In the UX Theme Assets list, select **New**.
        4.  Select the Manage Attachments icon ![](../image/icon-manage-attachment.png) to add an image.
        5.  When the image asset is uploaded, close the Attachments window.

            **Note:** Verify that your image is in SVG format.

        6.  Enter the file name of the asset in the **Name** field and select **Submit**. The asset is added to the UX Style Assets list.
        7.  Select and hold \(or right-click\) on the asset from the UX Style Assets list, and select **Copy sys\_id**.
        8.  Enter the sys\_id into the Style field using the following format:`"/uxta/ENTERYOURSYSID.assetx"`
    -   Add your custom image to the Images \[db\_images\_list.do\] table.

        **Note:** Verify that your image is in SVG format.

        1.  For detailed instructions, see [Upload one or more images](upload-multiple-images.md).
        2.  From the Imagery style record, enter the image file name into the **Style** field using the following format: `"/FILENAME.svg"`.
6.  Select **Update**.

    The custom images appear in your theme.

7.  Customize the colors of your empty state images using the UX Style color record associated with your theme to override the default theme hooks.

    For a step-by-step tutorial on editing your UX Style color record, see Exercise 3, Activity 2 and 3 of the [Next Experience Workshop](https://servicenownextexperience.github.io/labs/CCL1319-K24-Theming-Lab/ex3/activity-2) in the ServiceNow Community.

    **Note:** Using the default theme hooks is recommended.


**Parent Topic:**[Working with theme-able empty state images](../concept/themeable-empty-state-images.md)

