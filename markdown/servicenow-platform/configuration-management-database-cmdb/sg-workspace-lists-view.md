---
title: Lists view in Service Graph Workspace
description: The Lists view in Service Graph Workspace provides access to CIs within the CMDB hierarchy and to records in tables that aren't descendants of the Configuration Item \[cmdb\_ci\] table, but are important in the CMDB ecosystem.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Explore, Service Graph Workspace, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Lists view in Service Graph Workspace

The Lists view in Service Graph Workspace provides access to CIs within the CMDB hierarchy and to records in tables that aren't descendants of the Configuration Item \[cmdb\_ci\] table, but are important in the CMDB ecosystem.

## Access

Navigate to **Workspaces** &gt; **Service Graph Workspace**, and then in the navigation panel, select the Lists icon.

Role required: sn\_cmdb\_user, sn\_cmdb\_editor, or sn\_cmdb\_admin

## Default lists

Provides lists of records from the associated list tables as specified in the Platform table UX List Menu Configuration \[sys\_ux\_list\_menu\_config\] table, in the Service Graph Workspace record. By default, the list contains related tables that are referenced in commonly used CI classes, and tables that a CMDB Admin might need to update records in.

Initially, the default lists are:

-   CMDB Groups:

    -   Source table: CMDB Groups \[cmdb\_group\]
    -   More information: [CMDB groups](cmdb-groups.md#)
-   CI Identifier:

    -   Source table: Identifiers \[cmdb\_identifier\]
    -   More information: Identifiers in identification rule sets which are defined for different classes of CIs. For more information, see [Create a CI identification rule](../task/t_CreateCIIdentificationRule.md)
-   Relationships:

    -   Source table: Cl Relationship \[cmdb\_rel\_ci\]
    -   More information: [CI relationships in the CMDB](c_CIRelationships.md)
-   Tags:

    -   Source table: Key Value \[cmdb\_key\_value\]
    -   More information: To manage a tag, select a tag, and then in CI Form select Tags and in the Tags card select **Manage**. For more information, see [Manage CI details using CI Form in Service Graph Workspace](ci-form-sg-workspace.md)
-   Switch Forwarding Rules:

    -   Source table: Switch Forwarding Rule \[dscy\_swtch\_fwd\_rule\]
    -   More information: [Network switch and router discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-visibility/r_DataCollDiscoNWRouteAndSwitch.md)
-   Switch Partitions:

    -   Source table: Switch Partition \[dscy\_swtch\_partition\]
    -   More information: [Network switch and router discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-visibility/r_DataCollDiscoNWRouteAndSwitch.md)
-   Switch Ports:

    -   Source table: Switch Port \[cmdb\_switch\_port\]
    -   More information: [Layer 2 discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-visibility/c_Layer2Discovery.md)
-   Switchports:

    -   Source table: Switchport \[dscy\_switchport\]
    -   More information: [Network switch and router discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-visibility/r_DataCollDiscoNWRouteAndSwitch.md)
-   TCP Connections:

    -   Source table: TCP Connection \[cmdb\_tcp\]
    -   More information: [TCP connection discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-visibility/r_DataCollDiscoTCPConnections.md)

Users with the sn\_cmdb\_editor or sn\_cmdb\_admin roles, can select **New** to add a record to the list table.

## My lists

Custom and shared lists where you can select **Create new list** to create a new custom list associated with the logged on user. For more information, see [Create a custom list in the Lists view in Service Graph Workspace](../task/sg-workspace-create-custom-list.md).

