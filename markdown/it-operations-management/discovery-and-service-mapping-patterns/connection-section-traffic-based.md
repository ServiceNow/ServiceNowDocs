---
title: Fine-tune patterns using traffic-based discovery
description: As an alternative to customizing the pattern from the Pattern Designer side, improve existing patterns so that Service Mapping can use them to find configuration item \(CI\) connections previously found using traffic-based discovery.
locale: en-US
release: zurich
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Fine-tune patterns using traffic-based discovery

As an alternative to customizing the pattern from the Pattern Designer side, improve existing patterns so that Service Mapping can use them to find configuration item \(CI\) connections previously found using traffic-based discovery.

## Before you begin

Role required: pd\_admin

Basic knowledge of programming is desirable.

## About this task

Service Mapping can discover and map configuration items \(CIs\) following their traffic-based connections. This method is referred to as traffic-based mapping and complements pattern-based mapping.

Using traffic-based discovery, Service Mapping may discover an important CI connection. In this case, you can make sure that this connection is always found for all CIs belonging to the same CI type. You do that by modifying the pattern used to discover CIs of that CI type. A pattern is a sequence of commands designed to detect attributes of a CI and its outbound connections.

You can search CI configuration files to locate data discovered using traffic-based discovery, for example IP address and port. If there are configuration files containing this data, you create a pattern step to parse this file. Next time Service Mapping discovers this CI using the modified pattern, it extracts the information about this connection directly from the configuration file.

## Procedure

1.  Navigate to **Service Mapping** &gt; **Services** &gt; **Application Services**.

2.  Select **View Map** next to the relevant service instance.

3.  Right-click the relevant CI.

4.  Select **Show traffic based connections**.

    The Traffic Based Connections List displays the following information:

<table id="ShowTrafficBasedConnectionsTableProper"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

IP

</td><td>

The IP address of the application connected to the selected CI.

</td></tr><tr><td>

Port

</td><td>

The port on the selected CI that is used to communicate to the other application.

</td></tr><tr><td>

Process

</td><td>

The ID of the process in the selected CI.

</td></tr><tr><td>

Already on map

</td><td>

-   **Yes** — if this connection shows on the map.
-   **No** — if this connection is not part of the service instance and not on the map.


</td></tr><tr><td>

System decision

</td><td>

The setting defines if Service Mapping keeps the discovered traffic-based connection or removes it. The value comes from the algorithm that Service Mapping uses.

</td></tr><tr><td>

User decision

</td><td>

\(Optional\) The setting overrides the System decision setting, which defines if Service Mapping keeps the discovered traffic-based connection or removes it. For example, if the System decision setting for a connection is Keep, and you want to remove this connection, select `Remove`.

</td></tr></tbody>
</table>    **Note:** There may be a case when you can see traffic-based connections on the map, but the Traffic Based Connections list does not display them. It happens for the connections that have been removed from the TCP Connection \[cmdb\_tcp\] table less than three days.

5.  Double-click the connection you want to use to create a pattern step.

6.  If there are multiple patterns used to discover this CI, select the pattern for which you want to create the step, and click **OK**.

    Pattern Designer creates a temporary connection section for this pattern with a new step.

    ![Temporary Connection section in the Pattern Designer](../image/CreateParseStepTempStep.png)

    The Debug Connection Section window is displayed with some fields automatically populated.

7.  Click **Connect**.

    The Debug mode is activated.

    The Search Assistant window opens.

8.  Search CI configuration files for data received using traffic-based discovery:

    1.  Under **Free Text**, review data automatically filled in from the Traffic Based Connections List.

        ![Search Assistant shows search criteria pulled directly from the Traffic Based Connections List](../image/CreateParseStepSearchAssistant.png)

        The File Patterns field displays file types in which Pattern Designer performs the search.

    2.  Click the **Search Files** tab and review files.

        If necessary, you can remove irrelevant files from the search by clicking the Minus icon.

    3.  Click **Search**.

        After search completes, the **Search Result** tab opens with the list of files in which any of the search criteria was found.

9.  Create a pattern step for parsing the configuration file containing information about the connection:

    1.  On the Search Result tab, click one of the files and review connection data found in this file.

    2.  Wait for the file content to load and select the relevant entry under the file name:

        ![Search Result tab showing data found in files.](../image/CreateParseStepSearchResults.png)

    3.  To use this data to create the pattern step, click **Create parse file step**.

        Pattern Designer shows the new step with the Parse File operation. It automatically assigns this step the name in the following format: Parsing &lt;file name&gt;.

        Pattern Designer automatically sets the file name, file path, and parsing strategy for the step. It also creates variables that contain data you searched for. If there is a variable, which contains the file path, Pattern Designer enters this variable for the path.

        ![Automatically created step](../image/CreateParseStepPatternStep.png)

    4.  If necessary, you can modify parsing strategy.

    5.  Rename the section to provide a meaningful name, for example Discover HA Proxy client connection.

        Or

        Copy and past the step into the relevant connection section.

10. Complete modifying the pattern as described in [Finalize a pattern](t_FinalizePatternPatDef.md).


**Parent Topic:**[Discovery patterns used by ITOM Visibility](../concept/c_MappingPatternsCustomization.md)

**Previous topic:**[Enhance patterns without changing their identification sections](modify-pattern-using-extensions.md)

**Next topic:**[Finalize a pattern](t_FinalizePatternPatDef.md)

**Related topics**  


[Traffic-based discovery in Service Mapping](../concept/traffic-based-discovery.md)

[Enable traffic-based discovery for CI types or specific CIs](t_CreateATrafficBasedDiscoveryRule.md)

[Discovery patterns used by ITOM Visibility](../concept/c_MappingPatternsCustomization.md)

