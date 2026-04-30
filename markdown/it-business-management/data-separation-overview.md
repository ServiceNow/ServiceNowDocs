---
title: Exploring Data Separation
description: Learn about the features, configuration, and benefits that Data Separation provides.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Data Separation, Strategic Portfolio Management]
---

# Exploring Data Separation

Learn about the features, configuration, and benefits that Data Separation provides.

## Data Separation overview

Data Separation helps you restrict data in ServiceNow® Strategic Portfolio Management based on a lens hierarchy and its leaf node. The leaf node is the bottom-level entity in a lens hierarchy. For example, if the Organization lens is used for data separation, the leaf node would be Department for the base system lens.

You can enable Data Separation on select Demand, Project, Resource Plan, and Cost Plan entities, as needed. Also, you can enable Data Separation on select Cost Plan Breakdown and Project Task related entities.

Data Separation supports records, related items, planning consoles, workbenches, and reports.

**Note:** Access control list \(ACL\) and query Business Rule \(BR\) limitations apply even when Data Separation is enabled. For example, reports with aggregate numbers may not be data separated.

Data Separation applies even on child projects and sub-tasks based on the Data Separation that is configured for the parent project or task.

## Data Separation key components

-   Hierarchy: Defines the hierarchy for enabling Data Separation using a lens and its leaf node.
-   Supported Entities: Enables Data Separation on select entities and related entities, as needed.
-   Entity-Group Mapping: Defines entity-group mappings between a business area and user group.

## Features

You can use the Data Separation features to do the following:

-   Configure a data separation hierarchy using a lens hierarchy and its leaf node.
-   Enable data separation on select entities and related entities, as needed.
-   Create as many entity group mappings as required to restrict data to specified user groups.
-   Grant access for the users who always need access to sensitive data by assigning the data separation privileged user \(sn\_ds.ds\_privileged\_user\) role.

## How Data Separation works

The following is the process flow for restricting access to the sensitive data in Strategic Portfolio Management using Data Separation.

-   A lens is selected for defining a hierarchy for Data Separation. The Data Separation admin can modify the hierarchy of the lens for data separation as needed.
-   The required entities and related entities are enabled for Data Separation.
-   An entity group mapping is created for each business group \(where the business group could be a business unit, department, or company\) that defines the set of users that the access is restricted to.
-   The data of the business group is then restricted for the enabled entities only to the users that are part of the user group populated in the entity-group mapping record.

## Examples data separation

-   **Example 1**

    Consider a scenario where:

    -   The Data Separation hierarchy is defined using the Organization lens and the lens structure is Company, Business Unit, and Department \(from top-to-bottom\).
    -   The entity mapping is created for the HR department \(Department : HR\) with the group HR leads.
    -   Data Separation is enabled for the Demand and Project entities.
    In this case, no user can access the project and demand records of the HR department except the users that are part of the HR leads group. However, all users \(based on the ACLs that the user currently has\) can access other records \(for example, the resource plan and cost plan\) of the HR department.

-   **Example 2**

    The Company XYZ has a data separation-enabled lens structure as shown in the following image and wants to restrict data to specific groups based on different use cases. Also, all the supported entities are enabled for Data Separation. The following use cases help you understand how Data Separation works and how to configure Data Separation for different use cases.![Data Separation lens structure example.](../image/lens-structure-ds-example.jpg)

    -   Case 1: Restrict data of the Payroll department to the Payroll managers

        You can restrict data for this case by configuring Data Separation as follows:

        -   Create a Payroll managers user group.
        -   Create an entity-group mapping for the Payroll department with the lens entity record \(Department : Payroll\) and the Payroll managers user group.
    -   Case 2: Restrict data of the HR business unit \(both the Onboarding and L&amp;D departments\) to the HR leads

        You can restrict data for this case by configuring Data Separation as follows:

        -   Create an HR leads user group.
        -   Create an entity-group mapping for the HR business unit with the lens entity record \(Business Unit : HR\) and the HR leads user group.
    -   Case 3: Restrict data of the entire organization to the Organization leads

        You can restrict data for this case by configuring Data Separation as follows:

        -   Create an Organization leads user group.
        -   Create an entity-group mapping for the Company XYZ with the lens entity record \(Company : XYZ\) and the Organization leads user group.

