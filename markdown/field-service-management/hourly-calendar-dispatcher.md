---
title: Configure an hourly calendar for Dispatcher Workspace
description: Configure Dispatcher Workspace to show a calendar with each column representing an hour. In this document were going to show a five-hour calendar, but you can change the number of hours to fit your needs.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Dispatcher Workspace, CSM/FSM Configurable Workspace, Configure, Field Service Management]
---

# Configure an hourly calendar for Dispatcher Workspace

Configure Dispatcher Workspace to show a calendar with each column representing an hour. In this document were going to show a five-hour calendar, but you can change the number of hours to fit your needs.

## Before you begin

Role required: admin

## About this task

Benefits of configuring an hourly calendar include:

-   **Granular Time Display**: Each column represents exactly 1 hour
-   **5-Day Span**: Shows 120 consecutive hours \(5 × 24 hours\)
-   **Zoom Capability**: Enhanced zoom functionality for better visibility
-   **Responsive Design**: Optimized column width and spacing
-   **Event Management**: Full support for event creation, editing, and visualization

![hourly view span showing](../image/hourly-view.png "Hourly view in Dispatcher Workspace")

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Script includes**.

2.  Find and open **DispatcherWorkspaceConstants**.

3.  Locate the `CALENDAR_VIEW_SETTINGS` object, and add the `TIMELINE_FIVE_DAYS_HOURLY_VIEW` configuration.

    ```
    "TIMELINE_FIVE_DAYS_HOURLY_VIEW": {
        // Template configurations for UI components
        "templates": {
            "rowBody": {
                "type": "macroponent",
                "value": "23c3967f53d07110443cddeeff7b1222"
            },
            "sectionHeadBody": {
                "type": "macroponent",
                "value": "43899a6ded592110f87778b05e3c80a7",
                "sticky": true,
                "autoCollapse": false,
                "manageCollapsed": true,
                "disableUXFContainerClickEvents": true
            },
            "sectionHeadTitle": {
                "type": "macroponent",
                "value": "a1ff3ba6b7803110a311aa7e1e11a964",
                "autoCollapse": false,
                "manageCollapsed": true,
                "disableUXFContainerClickEvents": true
            },
            "rowTitle": {
                "type": "macroponent",
                "value": "0c1ae3a8b1346110f8776e5c40f98bd2",
                "style": {
                    "height": "100%"
                }
            },
            "eventBody": {
                "type": "component",
                "value": "sn-fsm-event-body"
            },
            "timestampBody": {
                "type": "macroponent",
                "value": "3deb30f8d149e110f8773e7b5e3fce04"
            }
        },
     
        // Core time configuration - THIS IS THE KEY PART
        "xStart": 0,                    // Start from hour 0
        "xStep": 1,                     // Increment by 1 hour per column
        "xSize": 120,                   // Show 120 hours total (5 days × 24 hours)
        "xUnitName": "hours",           // Each column represents hours
     
        // Display and layout settings
        "columnWidthInPx": 65,          // Width of each hourly column
        "viewProvider": "TIMELINE_CONFIGURABLE_COLUMN",
     
        // Time scale header configuration. Adds another row on top of the 1 hour per column for better visibility and more information
        "timeScaleGridRows": [{
            "id": "days",
            "order": 1,
            "unit": "days",
            "format": "dddd MMMM DD"    // Display format: "Monday January 15"
        }],
     
        // UI behavior settings
        "rowHeightBottomPaddingInLines": 2,
        "snapGranularity": 15,
        "groupBy": "group",
        "animation": false,
        "hideAgendaView": true,
        "eventHeight": 20,
        "minEventRowHeight": 24,
        "eventMinWidthMS": 1000,
        "noScrolling": false,
        "usePropertyDiff": true,
        "hideSidebarOnLoad": true,
     
        // Zoom and toolbar configuration
        "floatingToolbarConfig": {
            "manage": false,
            "zoomSize": 0.2,
            "disableCollapse": false,
            "collapseOnLoad": true,
            "collapseOnResize": true
        }
    }
    ```

4.  Find the `AVAILABLE_VIEWS` array in the same script includes.

    **Note:** See the image in the previous step.

5.  Add the new view entry, see the image in this step.

    ```
    {
        "view": "TIMELINE_FIVE_DAYS_HOURLY_VIEW",
        "viewProvider": "TIMELINE_CONFIGURABLE_COLUMN", 
        "label": gs.getMessage("5 days hourly"),
        "type": "Timeline"
    }
    ```

6.  Save the script include.

7.  Capture the file changes in an update set and commit the update set.

8.  Navigate to Dispatcher Workspace to verify your implementation.

9.  Search for and select the **5 days hourly** option in the view selector.


