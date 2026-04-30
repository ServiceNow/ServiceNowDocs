---
title: View an application service map in base system
description: An application service map provides a visualization of data for the CIs comprising an application service, and the relationships and connections between these CIs.
locale: en-US
release: xanadu
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Application services, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# View an application service map in base system

An application service map provides a visualization of data for the CIs comprising an application service, and the relationships and connections between these CIs.

## Before you begin

Role required: app\_service\_user to view the map in View mode, and app\_service\_admin to modify services in Edit mode.

## About this task

When you create an application service, the system generates an associated application service map. The system then updates the map to reflect any changes to the application service. This map consists of icons representing CIs and arrows that represent the connections between them.

If Service Mapping is deployed, see [Application service maps](https://www.servicenow.com/docs/access?context=c_UndestandMaps&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US) and [View CI connection attributes in an application service map](https://www.servicenow.com/docs/access?context=view-connector-properties&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US) for more details.

To open an application service map, navigate to **CSDM** &gt; **Manage Technical Services** &gt; **Application Service**, select an application service, and then click **View map**.

Perform any of the following operations in the application service map.

## Procedure

-   Select ![Menu to navigate to a different application service.](../image/AppServiceDropDown2.png) on the windows bar to navigate to a different application service.

-   Use the navigation tools to increase or decrease the view of the map and to move the map on the page.

    You can also click anywhere on the map area and drag a segment of the map into the visible area.![Control zoom and positioning of the map.](../image/MapZoomNavigationAppSer.png)

-   View changes: You can view changes and change records associated with the application service as a whole or with any of its CIs, within a time range.

    For more information, see [View the change history of application services](https://www.servicenow.com/docs/access?context=t_ViewCIChanges&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US).

    Records under the **Change** tab underneath the map, which are associated with a selected CI or connection, are highlighted. If you select a change record under the **Change** tab, then the associated CI icon appears yellow on the map.

-   View attributes: When you select a device, application, or connector on the map, it appears in blue and its attributes appear in the Properties pane on the right of the map.

    When nothing is selected on the map, the details of the application service itself appear on the Properties pane.

    Open the CI's form for further details by clicking **Detailed Properties** at the bottom of the Properties pane.

-   Select **Edit** to add or remove CIs from the map or **View** to switch the map mode.

-   Select ![Additional actions menu.](../image/AdditionalActionsAppSer.png) for **Additional actions**:

    -   Set **Group CIs on map**: Simplify maps by grouping 10 or more CIs belonging to the same type and hosted on servers sharing prefix and domain name.
    -   Set **Spanning tree view**: Simplify the map by organizing CIs into a tree structure and hiding some connection lines. This option is especially useful for very large maps.
    -   **Map Indicators**: Show additional information for a CI or for the application service itself by displaying related records such as alerts, outages, incidents, and problems. For each indicator that is enabled, the corresponding indicator icon appears next to CIs with associated records, and the corresponding tab appears underneath the map. If a record is associated with the application service itself, the indicator appears next to the application service name.

        For information about managing map indicators, see [Create or modify map indicators](../../business-service-management-map-ng/task/t_CreateModifyNGBSMMapIndicators.md). For more general information, see [Event Management Map Indicators \(Video\)](https://www.youtube.com/watch?v=wjtpJe8J3iA).

    -   **Export to PDF**: Export the map to a .PDF file which you can then share as needed. After the PDF file is ready, click ![Icon to download a PDF to your local drive.](../image/AppSerDownloadPDF.png) to download the PDF file to your local drive.
-   View the details of a connection.

    By default, connection lines for the same CI on an application service map, are merged. This merge reduces clutter on the map and helps to make the map more readable. For a merged connection line, you can view details for all the underlying connection lines.

    ![Merged connection lines](../../service-mapping/image/MapAddOptionsMergeEdgesExample.png "Merged connection lines")

    -   To view the source and target CIs of a connection, right-click a connection line.

        If spanning tree view is enabled:

        1.  Select the CI whose connections you want to view to show all the concealed connections for the CI.
        2.  Right-click one of the connection lines.
    -   To view properties of a connection, click a connection line. For manually added connections, Endpoint Type is Manual Endpoint.
    -   To view properties of a connection within a merged connection:
        1.  Right-click the merged connection line.
        2.  Select one of the connections.
        3.  Select **Select edge**.

## What to do next

You can change the details that appear in the Properties pane by updating the form view 'Form view and section', as described in [Configuring the form layout](https://www.servicenow.com/docs/access?context=configure-form-layout&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

**Related topics**  


[Spanning tree view property](../reference/components-installed-app-services.md)

