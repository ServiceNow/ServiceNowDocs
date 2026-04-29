---
title: Create or edit a dependency type
description: Use one of the dependency types provided, or create a custom dependency type with a script that will execute in real time to generate a custom view of a Dependency Views map for a specific CI.
locale: en-US
release: australia
product: Dependency Views
classification: dependency-views
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Administer, Dependency Views, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Create or edit a dependency type

Use one of the dependency types provided, or create a custom dependency type with a script that will execute in real time to generate a custom view of a Dependency Views map for a specific CI.

## Before you begin

Role required: none

## About this task

Create a JavaScript to customize the map. The script must comply with JavaScript syntax guidelines and the directions in the default script template, and it can call platform APIs. Use a dependency type, for example:

-   To narrow down and simplify a map, leaving out CIs that are not important for a specific task.
-   To include only specific CIs that are hidden by default, such as qualifiers, end-points, and entry points.
-   To display virtual relationships that are calculated, and that otherwise do not exist in the CMDB.
-   As a tool to plan a new topology deployment that is based on existing resources.

The following dependency types are available in the base system:

-   **Default**

    The default setting in the base system. With this setting, there is no processing of the dependency map through any dependency type scripts that might filter or modify the map.

-   **Show All Relationships**

    Returns all qualifiers, end points, and entry points. This dependency type is available in the base system and is disabled by default. Typically, you would enable this dependency type for debugging and tracking purposes.


The following dependency types are available with [Service Mapping](https://www.servicenow.com/docs/access?context=c_ServiceMappingOverview&version=australia&pubname=australia-it-operations-management&ft:locale=en-US):

-   **Application to Network Devices**

    Returns the network devices in the network paths leading to/from the given CI.

-   **Network Device to Applications**

    Returns the applicative CIs which are target or source of network paths containing the given network device. In addition, returns the hosts of those applicative CIs, and for an applicative CI that is an inclusion, its parent CI is returned too.

-   **Physical Network Connections**

    Returns hosts/network devices that are physically connected to the given host or network device.

-   **Flow Dependencies**

    Returns all the server to server connections that were discovered using the Netflow collector. The script builds a graph based on data in the \[sa\_flow\_server\_comm\] table. This table contains pairs of services represented by an IP and a listening port that are communicating with each other. For more information, see [Data collection and discovery using Netflow](https://www.servicenow.com/docs/access?context=data-collection-netflow-mapping&version=australia&pubname=australia-it-operations-management&ft:locale=en-US) and [Data collection and discovery using VPC Flow Logs](https://www.servicenow.com/docs/access?context=data-collection-vpc-mapping&version=australia&pubname=australia-it-operations-management&ft:locale=en-US).


## Procedure

1.  Navigate to **All** &gt; **Dependency Views** &gt; **Dependency Types**.

2.  In the **Load Filter Scripts** list view, select an existing depenency type, or click **New**.

3.  Enter or modify a script, adhering to the guidelines and requirements in the script template that is provided.

4.  Click **Submit**.


## Result

In a Dependency Views map, you can click **Dependency Type** to apply a custom script defined in a dependency type.

**Parent Topic:**[Administer Dependency Views](../topic/p_AdministerNGBSM.md)

**Related topics**  


[Create or modify map indicators](t_CreateModifyNGBSMMapIndicators.md)

[Create or modify map icons](t_CreateModifyNGBSMMapIcons.md)

[Create a predefined filter](create-predefined-filter.md)

[Set a predefined filter as default](set-predefined-filter-default.md)

[Create or modify Map Related Items](t_CreateModifyNGBSMMapRelatedItems.md)

[Create or modify Dependency Views menu actions](t_CreateModifyNGBSMMenuActions.md)

[Condition and script parameters for menu actions](../reference/condition-script-parameters.md)

[Data collection and discovery using Netflow](https://www.servicenow.com/docs/access?context=data-collection-netflow-mapping&version=australia&pubname=australia-it-operations-management&ft:locale=en-US)

