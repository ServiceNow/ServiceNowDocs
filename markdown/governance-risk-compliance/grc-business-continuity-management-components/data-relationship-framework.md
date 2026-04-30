---
title: Data Relationships Framework
description: The Data Relationships Framework application \(sn\_grc\_rel\_config\) supports the BCM application with the underlying framework to fetch the dependencies in the BIAs, plans, and events from different sources such as CMDB, BIA, and BCP. Beginning with the Yokohama release, the Data Relationships Framework \(sn\_grc\_rel\_config\) application is installed with the BCM application by default.
locale: en-US
release: yokohama
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 6
breadcrumb: [Reference, Business Continuity Management, Governance, Risk, and Compliance]
---

# Data Relationships Framework

The Data Relationships Framework application \(sn\_grc\_rel\_config\) supports the BCM application with the underlying framework to fetch the dependencies in the BIAs, plans, and events from different sources such as CMDB, BIA, and BCP. Beginning with the Yokohama release, the Data Relationships Framework \(sn\_grc\_rel\_config\) application is installed with the BCM application by default.

## Framework for fetching the dependencies

The Data Relationships Framework \(sn\_grc\_rel\_config\) stores the configurations for how a main object type can relate to other object types. It enables the users to configure the source \(main node\) for the dependency updates, configure its relationship with the child nodes, and fetch the dependencies for the selected object.

A scheduled job scans the object configuration data at regular intervals and checks if any dependencies have been updated. If any changes are observed in the dependencies, the scheduled job fetches the dependencies of the selected object from one of the configured sources such as BIA, BCP, or CMDB.

## Benefits of the Data Relationships Framework

The Data Relationships Framework provides the following benefits for the BCM application users:

-   Provides a single API to fetch the dependencies from different sources.
-   Supports the configuration of the main node \(source\) and maintains its relationships with its child nodes such as assets, risks, and so on.
-   Enables the users to control the performance by selecting different sources.

## Roles associated with the Data Relationships Framework

The following roles are associated with the Data Relationships Framework application.

<table id="table_tbw_wpg_rzb"><thead><tr><th>

Roles

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Data Relationships Framework administrator \[sn\_grc\_rel\_config.admin\]

</td><td>

Configures the relationship of the object types such as the relationship of the main node to the child nodes.

</td></tr><tr><td>

Data Relationships Framework reader \[sn\_grc\_rel\_config.reader\]

</td><td>

Views the data for the object types as defined in the Data Relationships Framework.**Note:** All BCM application users have the Data Relationships Framework reader role.

</td></tr></tbody>
</table>## Tables for the framework

To support the Data Relationships Framework, the following new tables have been added and existing tables have been revised.

|New and existing tables|Table|Description|
|-----------------------|-----|-----------|
|New table|Main node configuration \[sn\_grc\_rel\_config\_main\_node\_confi\]|Table to store the configuration of the main node from where the dependencies are fetched.|
|New table|Node relationship configuration \[sn\_grc\_rel\_config\_node\_rel\_config\]|Table to store the configuration that determines the dependencies of the main node and child nodes. It also maintains a reference to the main node configuration.|
|Existing table|Relationship registries \[sn\_data\_registry\_relationship\]|Table to determine the relationship of an object with other objects.|

## Modules for configuring the relationships

The BCM application users can navigate to **Data Relationship Framework** in the application navigator and access its modules for configuring the relationships.

![Module path.](../image/data-rela-fw-modue-path.png)

The Data Relationships Framework application consists of the following modules:

1.  Main node configuration: Configure the details of the main node such as its name, source, table name, filer conditions, and so on as shown in the following examples.

    ![Main node configuration.](../image/main-node-config-new-bcm.png)

    The following main node configurations are provided as sources with the base system as shown in the following example:

    ![Base system configuration.](../image/main-node-config-ootb-bcm.png)

    -   BIA upstream dependency
    -   BIA downstream dependencies
    -   CMDB
    -   Plan primary assets
    -   Plan related assets
    The BCM administrators use the main node configuration to perform the following tasks:

    -   Configure the Impact analysis dependency update configuration module and fetch the dependency updates into a BIA \(add the dependency updates to the BIA\) from these sources.![Sources.](../image/sources-bia-updates.png)
    -   Configure the Planning dependency update configuration module and fetch the planning dependency updates into a plan \(add the updated related assets to the plan\) from these sources.
    -   Configure the Event dependency source configuration module and configure the sources for the event dependency updates \(add the updated impacted assets to a recovery event\).
    **Note:** All the information on how data should be pulled is stored in the Main node configuration, which is attached to the records. This configuration determines the order in which the data is pulled. To reduce the amount of data pulled and how it is pulled, you need to configure the conditions in both the Main node configuration and the records. This ensures that only the necessary data is retrieved.

    The main node configuration records for plans and CMDB are shown in the following examples.

    ![Main node configuration for a BCP.](../image/main-node-config-for-bcp.png)

    ![Sample main node configuration.](../../grc-business-continuity-management/image/main-node-configuration-bcm.png)

    For information on creating a main node configuration record, see [Create a main node configuration record](../task/create-a-main-node-config-record.md).

2.  Relationship registries: Configure the relationship registries for the main node. Relationship registries are part of the 360-degree configuration in GRC where a user can define how one object has a related object. The configuration details of a relationship registry record such as its name, table, relationship type, relationship table, and so on are shown in the form.

    ![New relationship registry record.](../image/rela-registry-record-new.png)

    A sample relationship registry record for a BIA and BIA template is shown in the following example.

    ![Sample relationship registry record.](../image/rela-registry-record-sample.png)

    For information on creating a relationship registry record, see [Create a relationship registry record](../task/create-a-rela-registry-record.md).

3.  Properties: Configure the properties of the Data Relationships Framework as shown in the following example.

    ![Properties for the Data Relationship Framework.](../image/data-rela-framework-properties.png)

    For information on configuring the properties, see [Configure the properties for the Data Relationships Framework](../task/configure-properties-for-data-rel-framework.md).


## Use cases for the Data Relationships Framework

The Data Relationships Framework is used to configure the node and asset relationships such as mapping a main node to its child node or mapping an asset to a risk.

Consider the following use case that shows the main node configuration and its relationships.

![Data relationship framework.](../image/data-relationship-framework-mapping.png)

In this example, INC1010 is the main node where the source is an Incident. INC1010 has two child nodes:

1.  Asset A: The affected configuration item for Asset A is Risk A.
2.  INC1011: The affected configuration items \(CIs\) for INC1011 are Asset B and Asset C. For Asset B, the affected configuration item is Risk B.

With the underlying Data Relationships Framework, the following relationships are configured:

-   Main nodes:
    -   INC1010 -&gt; Asset A
    -   INC1010 -&gt; INC1011
-   Node relationships:
    -   Asset A -&gt; Risk A
    -   INC1011 -&gt; Asset B
    -   INC1011 -&gt; Asset C
    -   Asset B -&gt; Risk B
-   Input nodes:
    -   Source = Incident
    -   Record = INC1010
    -   Max Levels = 5
    -   Max Nodes = 1000
-   Output nodes:
    -   INC1010
    -   Asset A
    -   INC1011
    -   Risk A
    -   Asset B
    -   Asset C
    -   Risk B
-   Edges:
    -   INC1010 -&gt; Asset A
    -   INC1010 -&gt; INC1011
    -   Asset A -&gt; Risk A
    -   INC1011 -&gt; Asset B
    -   INC1011 -&gt; Asset C
    -   Asset B -&gt; Risk B

## Limitations of using the Data Relationships Framework

The Data Relationships Framework has the following limitations:

-   The data fetched for an object cannot be reused for another purpose.
-   The sources provided in the framework must be used for fetching the dependency updates into an object. It is not possible to configure your own sources for fetching the data.

For more information on the administrative setup for the configuration records, see [Dependency Configuration records](../../grc-business-continuity-management/concept/dependency-config-modules.md).

-   **[Create a main node configuration record](../task/create-a-main-node-config-record.md)**  
Create a main node configuration record to configure the source for fetching the dependencies. You can configure the details of the main node such as its name, source, table name, filer conditions, and so on.
-   **[Update the node relationship configuration](../../grc-business-continuity-management/task/update-node-rel-config-bcm.md)**  
Update the node relationship configuration for each main node configuration. You can select the sequence of the node configuration in the Node relationship configurations related list and update the source table, relationships such as relationship registry, relationship table, target table, target conditions, and so on.
-   **[Create a relationship registry record](../task/create-a-rela-registry-record.md)**  
Create a relationship registry record to set up relationship between the record and object defined in the table. You can configure the details of the main node such as its name, source, table name, filer conditions, and so on.
-   **[Configure the properties for the Data Relationships Framework](../task/configure-properties-for-data-rel-framework.md)**  
Configure the properties for the Data Relationships Framework application.

**Parent Topic:**[BCM reference](../../grc-business-continuity-management/reference/bcm-reference.md)

