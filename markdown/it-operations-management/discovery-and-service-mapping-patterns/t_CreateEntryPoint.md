---
title: Create entry point types for Service Mapping
description: An entry point is a point where clients access a service instance. Service Mapping starts the mapping process for every application service from the entry point you define for it. Service Mapping includes a wide range of preconfigured entry point types that cover most commonly used applications. If your organization uses a less known or proprietary application that does not have a corresponding entry point type in Service Mapping, you must create it.
locale: en-US
release: australia
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Create entry point types for Service Mapping

An entry point is a point where clients access a service instance. Service Mapping starts the mapping process for every application service from the entry point you define for it. Service Mapping includes a wide range of preconfigured entry point types that cover most commonly used applications. If your organization uses a less known or proprietary application that does not have a corresponding entry point type in Service Mapping, you must create it.

## Before you begin

If your ServiceNow instance uses domain separation and you have access to the global domain, log in to the relevant domain. The selected domain must be a domain without any child domains.

Role required: service\_mapping\_admin or admin

## About this task

In addition to starting the mapping process from entry points, Service Mapping patterns use entry points to discover CI outbound connections.

Entry points are modeled in the ServiceNow CMDB as CIs of endpoint type. Entry points are stored as records in the Endpoint \[cmdb\_ci\_endpoint\] tables.

Like any other CI type, an entry point contains several important definitions that apply to all CIs belonging to it:

-   CI attributes are added as fields to the CMDB tables.
-   Identifiers help Service Mapping and Discovery to differentiate between new and existing CIs. For example, if there is an endpoint CI type for Active Directory Forest in the CMDB 360, and Service Mapping discovers an Active Directory Forest CI. Service Mapping processes this CI using identifiers and recognizes it as an updated version of the Active Directory Forest CI that exists in the system, not a new Active Directory Forest CI.
-   CI type hierarchy. CMDB stores CI class in the form of a hierarchy where some CI classes are parents to other CI classes, who automatically derive their parent's attributes in addition to attributes you configure specifically for child CI classes. CI class hierarchy is used widely for configuring CI behavior, relationships, and display. Create standard entry points as child CIs for the endpoint CI type, which creates an extension for the cmdb\_ci\_endpoint table. For entry points of inclusion type create child CIs for the inclusion endpoint CI type extending the cmdb\_ci\_endpoint\_inclusion table. In an inclusion, a server hosts applications that are treated as independent objects.

## Procedure

1.  Navigate to **All** &gt; **Configuration** &gt; **CI Class Manager**.

2.  Select **Open Hierarchy**.

3.  To create a standard entry point, right-click **Endpoint** from the **Class Hierarchy** pane and select **Add Child Class**.

4.  To create an entry point of the inclusion type, right-click **Inclusion Endpoint** from the **Class Hierarchy** pane and select **Add Child Class**.

5.  Define the parameters for the new entry point type as described in [Create a CI class](https://www.servicenow.com/docs/access?context=t_CreateCIType&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).


**Parent Topic:**[Discovery patterns used by ITOM Visibility](../concept/c_MappingPatternsCustomization.md)

**Previous topic:**[Create CI types for Service Mapping and Discovery](t_CreateCITypeForSM.md)

**Next topic:**[Create or customize patterns](t_CreatePatternPatDef.md)

**Related topics**  


[Map a single application service using classic Service Mapping](t_DefineNewBusinessService.md)

[Create CI types for Service Mapping and Discovery](t_CreateCITypeForSM.md)

