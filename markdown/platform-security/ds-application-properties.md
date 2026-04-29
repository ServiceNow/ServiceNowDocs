---
title: Domain separation application properties
description: The Domain Separation plugin has two new tables to give service providers more flexibility in customizing their applications that use domain separation. These tables are the System Application Property table \[sys\_application\_property\] and the System Application Property Value table \[sys\_application\_property\_value\].
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Advanced administration, Setup and administration, Domain separation for service providers, Access Management]
---

# Domain separation application properties

The Domain Separation plugin has two new tables to give service providers more flexibility in customizing their applications that use domain separation. These tables are the System Application Property table \[sys\_application\_property\] and the System Application Property Value table \[sys\_application\_property\_value\].

## New tables offer more options

With service provider \(SP\) applications, certain actions can vary depending on the domain. However, the ServiceNow® base system System Properties \[sys\_properties\] table is not domain-separated, so it doesn't satisfy the requirements for applications that use domain separation.

Each SP customer may want to customize their applications differently. Previously, features that could be customized were defined as only one global value. Application developers need a more flexible table. Now you can modify your application without having to create code every time you want to add or change the functionality.

## How overrides work in the new tables

Developers typically use the ServiceNow System Property \[sys\_properties\] table to create various functions in applications. If you wanted to develop an application to behave differently in different domains, you'd have to customize it yourself.

In the Paris release, the new Application Property \[sys\_application\_property\] table simplifies that customization. Instead of going directly to the System Property table for a value, the application property table goes to the System Application table first. This new table now stores the logic that you require to configure your application. If it finds a property in the new table, it uses that content. If there is no information in that table, it moves on to the base system properties table.

When you configure support for domain separation, you can add domain logic to this new Application Properties table. This table can contain properties that don't exist in the System Properties table. Or you can add properties to the configuration table that can override any property that you select in the System Properties table.

For example, let's say that you want to configure an application with a First day of the week feature. Sometimes, you might want the first day of the week to be Sunday. In other cases, you might want the first day of the week to be Monday. In the base system table, there might be only one Day 1 option, which is Sunday. With the new table, you can store another property, making Day 1, Sunday, and a child domain, Monday.

This figure shows how the system draws properties from the Application Property table before going to the System Property \[sys\_properties\] table.![New table goes to sys_application_property table before going to sys_properties table.](../image/app-property-table-diagram.png)

## How scoped apps work in the new table

The new Application Properties table is supported from scoped applications. The application property name, similar to the system property name, is unique, which means that it is prefixed with the scope name if it is not global. The scope of an application impacts your configuration. The scope may determine which Day 1 is defined as Sunday and which as Monday. You can use the same property but customize it so that Day 1, Sunday is the parent domain and Day 1, Monday is the child domain. In the new table, there is both a domain column and a scope column, so you can set these properties for each.

You can use the Expand Domain Scope view in the sys\_application\_property\_value table to show all overrides, as shown in the following image.

![Expanded application properties table](../image/expanded-app-properties.png)

**Note:**

If those tables are not available, make sure that you have activated the Domain Extension Installer \(com.glide.domain.msp\_extensions.installer\) plugin.

## New application property tables

The new System Application Property \[sys\_application\_property\] table contains these fields:

-   name
-   description
-   type \(choice of string, true\|false, integer, time zone, color, and so on\)
-   default\_value
-   property \(reference to sys\_properties\)
-   usage\_notes
-   read\_roles
-   write\_roles
-   unique key: \(name\)

The new System Application Property Value \[sys\_application\_property\_value\] table contains these fields:

-   sys\_application\_property \(ref to sys\_application\_property\)
-   sys\_domain
-   sys\_overrides
-   value
-   unique key: \(sys\_application\_property, sys\_domain\)

## New APIs

The new APIs are also supported in scoped apps. Domain-separated application properties have distinct APIs. The GlideApplicationProperty API has two new scriptable methods, available in both global and scoped applications. See [GlideApplicationProperty - Scoped, Global](https://www.servicenow.com/docs/access?context=GlideApplicationProperty&version=australia&pubname=australia-api-reference&ft:locale=en-US) to learn more about these new APIs.

**Parent Topic:**[Advanced domain separation administration](c_DomainSeparationAdministration.md)

**Related topics**  


[Use domain selection menus](c_DisplayingDomainSelectionMenus.md)

[Domain separation recommended practices for service providers](../reference/bp-domain-sep-recommended.md)

