---
title: Discover CIs identified as generic applications
description: Service Mapping identifies application configuration items \(CIs\) that it failed to properly discover as generic applications. Correctly identify generic applications by creating a simplified discovery pattern from an application service map, rather than creating a fully functional pattern from scratch using the Pattern Designer.
locale: en-US
release: yokohama
product: Service Mapping
classification: service-mapping
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 6
breadcrumb: [Fine-tune application services to implement owner requests, Application service mapping using classic Service Mapping, Using Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Discover CIs identified as generic applications

Service Mapping identifies application configuration items \(CIs\) that it failed to properly discover as generic applications. Correctly identify generic applications by creating a simplified discovery pattern from an application service map, rather than creating a fully functional pattern from scratch using the Pattern Designer.

## Before you begin

You can edit discovered and manually created service instances.

**Important:** You cannot fine-tune or edit tag-based and dynamic services from the map.

Make sure that you understand what [discovery process classification](../../discovery/concept/discovery-classifiers.md) is.

Request information about the CI discovered as generic application from the application service owner.

Role required: pd\_admin

## About this task

ServiceNow applications refer to devices and applications that comprise a service instance as configuration items \(CIs\).

As part of creating a simplified pattern for complete and proper application CI discovery, you create these necessary articles:

-   **CI type**

    All applications and hosts in your organization must have a corresponding configuration item \(CI\) type, which is necessary for discovering and processing applications and hosts correctly. A CI type \(or class\) contains several important definitions that apply to all CIs belonging to it. Preconfigured CI types form a hierarchy where child CI types derive attributes from their parents.

    Define the CI type name and label for Service Mapping to create a child CI type for the application \[cmdb\_ci\_appl\] CI type. For more information about CI types, see [Create CI types for Service Mapping and Discovery](t_CreateCITypeForSM.md).

-   **Process classification**

    Service Mapping relies on process information collected and classified by Discovery to run relevant patterns to discover an application CI. During the horizontal discovery process, Discovery checks if the attributes of the processes running by the application match classification criteria you define. When a match is found, Discovery uses the existing Application Rule identifier to check if the application CI is new or if it already exists in the CMDB. Then Discovery either updates an existing record or creates a new record for this application CI in the CMDB.

    Prior to starting the top-down discovery of an application CI, Service Mapping checks its process classification in the CMDB. It then runs only those patterns that are relevant for this application CI.

    Create process classification by defining the classification criteria based on preconfigured process attributes. The new process classification is added to the Process Classification \[discovery\_classy\_proc\] table. To learn about process classification, refer to [Discovery classifiers](../../discovery/concept/discovery-classifiers.md).

-   **Pattern**

    A pattern is a sequence of commands whose purpose it is to detect attributes of a CI and its outbound connections. When you create a simplified pattern for a generic application, Service Mapping assigns the new simplified pattern to the CI type you define as part of this process. The default name for the pattern starts with "ga\_".

-   **Association of an icon with this CI type**

    Each CI type is associated with an icon. When a CI is discovered and classified as belonging to a CI type, the map displays the associated icon to visualize this CI.


You cannot create simplified patterns from generic applications that are based on multiple processes. In this case, you have to either [create a fully functional pattern using the Pattern Designer](t_CreatePatternPatDef.md) or [create a new CI type](t_CreateCITypeForSM.md).

## Procedure

1.  Open the service instance map.

    1.  Navigate to **All** &gt; **CSDM** &gt; **Manage Technology Management Services** &gt; **Service Instance**.

    2.  Select the needed service instance.

    3.  On the service instance page, select **View Map**.

2.  Click **Edit** to be in Edit mode.

    ![When you click Edit, the Discovery Messages section appears.](../image/MapEditDiscoveryMessages.png)

3.  On the map, right-click the relevant generic application CI.

    The **CI Type** attribute in the **Application** pane is Generic Application.

    In the base system, the map displays generic application CIs with the gear icon.

    ![Generic applications displayed on the map](../image/MapGenericApp.png)

4.  Select **Create pattern for this generic application**.

5.  Define the CI type for the application.

<table id="table_t3c_lqk_gbb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Label

</td><td>

CI type name. For example, Citrix Licensing Server.

</td></tr><tr><td>

Name

</td><td>

The table name containing data for this CI type. For example, cmdb\_ci\_app\_license\_server.

 Use a name that is consistent with existing CI type names. Typically, application CI type names start from "cmdb\_ci\_app".

</td></tr><tr><td>

Icon

</td><td>

Select the name of the existing icon to represent this application on maps.

</td></tr></tbody>
</table>6.  Create the process classification for this CI by defining classification criteria for identifying the process that the generic application is running.

    In the base system, there are two conditions based on the running process name and the running process command. The values are filled in by the latest process discovery.

    1.  Select the CI attribute from the list.

        The attributes in the list are from the Running Process \[cmdb\_running\_process\] table.

    2.  Select an operator from the list.

        If you select `Is Empty`, the second field is rendered irrelevant and disappears.

    3.  Specify the value to match.

        The value field displays a dynamically generated suggestion from the latest process discovery.

    4.  To add a dependent condition, click **OR** or **AND**.

        **Note:** If the value in the first condition is not unique like Java.exe, use additional conditions to narrow down the results.

        ![Define classification criteria using the condition builder.](../image/GAprocessClassificationCondition.png)

        For example, to discover a Citrix Licensing server, use the following classification criteria: the process name `Imadmin.exe` with the command `C:\Program Files (x86)\Citrix\Licensing\LS\lmadmin.exe`.

    5.  To add a top-level condition, click **New Criteria**.

7.  Click **Create**.

    Once Service Mapping finished creating the CI type, the pattern, and the process classification, it resumes discovery of the CI initially identified as a generic application.

8.  Verify that Service Mapping discovered the CI as you expected.

    ![Correctly discovered application.](../image/MapGenericAppEgResult.png)

    Notice that Service Mapping uses the name of the process for the CI label on the map.


## What to do next

If Service Mapping still has not discovered the CI as you expected, [fine-tune the match and classification criteria for the process classifier](../../discovery/task/t_CreateAProcessClassification.md) and [configure advanced classification parameters](../../discovery/reference/classification-parameters.md).

If you are familiar with modifying patterns in the Pattern Designer, you can also enrich the simplified pattern by defining operations that discover more attributes for the CI.

You may configure Discovery to use a different identifier. For more information, see [Discovery identifiers](../../discovery/concept/c_DiscoveryIdentifiers.md).

**Parent Topic:**[Fine-tune application services to implement owner requests](review-implement-business-service-maps.md)

**Related topics**  


[Pattern-based discovery in Service Mapping](../concept/pattern-based-discovery.md)

