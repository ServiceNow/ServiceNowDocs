---
title: Relationships between CSDM objects
description: You can configure relationships between various CSDM objects such as business services, service offerings, business processes, and application services by using the Main node configurations. The \[sn\_grc\_m2m\_profile\_profile table\] serves as the source table for establishing these relationships.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Node relationship configurations, Main node configurations: A component of the Data Relationship Framework, Explore, Operational Resilience, Governance, Risk, and Compliance]
---

# Relationships between CSDM objects

You can configure relationships between various CSDM objects such as business services, service offerings, business processes, and application services by using the Main node configurations. The \[sn\_grc\_m2m\_profile\_profile table\] serves as the source table for establishing these relationships.

## Establishing relationships between different objects

To illustrate the relationships between different CSDM objects, consider the following example of a business service \(BS1\).

The business service \(BS1\) includes the following objects as shown in the example.

-   Service offering \(SO1\)
-   Business process \(BP2\)
-   Application service \(AS1\)
-   Service offering \(SO3\)

![CSDM objects.](../image/csdm-objects-rel.png)

The Service offering \(SO1\) is related to the Business process \(BP1\) and Service offering \(SO2\). BP1 has the following dependencies:

-   Acer
-   PS Apache01

BP2 has a dependency on PS Apache02. AS1 has a dependency on AS2 and AS2 has a dependency on PS Apache03.

**Note:** When you set up the Main node configurations, you must ensure that the entities are set up in Operational Resilience. Only when these entities exist, relationships can be established between the CSDM objects and then data is brought into Operational Resilience for reporting.

The **Applies to** field in a business impact analysis \(BIA\) shows the object that has the dependency. The example shows that the business process \(BP1\) has Acer as a dependency.

![Applies to field.](../image/bp1.png)![Dependency.](../image/bp2.png)

The dependency is also brought from the **Parent** field into Operational Resilience for the service offerings and application services. For example, the parent for service offering \(SO3\) is business service \(BS1\). Therefore, when the scheduled job is executed, it fetches SO3 as a configured relationship for business service \(BS1\).

![SO.](../image/bs-parent-for-so.png)

All the CMDB relationships, as shown in the example, are maintained in the CI relationships \[cmdb\_rel\_ci\] table.

![CI relationships [cmdb_rel_ci] table.](../image/ci-rel-table.png)

To bring these relationships into Operational Resilience, you must use the Main node configurations. For more information, see [Configure the Main node configurations](../task/set-up-main-node.md).

You can establish the following relationships between objects such as business services, service offerings, and business processes.

<table id="table_zpx_rxk_v2c"><thead><tr><th>

Entity

</th><th>

Relationships

</th></tr></thead><tbody><tr><td>

Business services

</td><td>

-   Service offering for a business service: BS -&gt; SO1, SO2
-   Business process for a business service
-   Application service for a business service
-   Dependencies for a business service

</td></tr><tr><td>

Service offerings

</td><td>

-   Business process for a service offering
-   Application service for a service offering
-   Dependencies for a service offering

</td></tr><tr><td>

Business processes

</td><td>

-   Application service for a business process
-   Dependencies for a business process

</td></tr></tbody>
</table>The same relationship can be applied and used on multiple forms. For example, the business process relationship can be used on both Business service and Service offering forms.

For information on the Main node configurations, see [Main node configurations: A component of the Data Relationships Framework](main-node-relationship-fw.md).

**Parent Topic:**[Node relationship configurations](node-relationship-configurations.md)

