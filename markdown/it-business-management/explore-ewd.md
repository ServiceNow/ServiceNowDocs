---
title: Exploring SPM Enterprise-Wide Deployment
description: SPM Enterprise-Wide Deployment \(EWD\) partitions SPM tables data so that you can restrict record access by department, business unit, or other function.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/explore-ewd.html
release: brazil
topic_type: concept
last_updated: "2026-10-09"
reading_time_minutes: 8
breadcrumb: [SPM Enterprise-Wide Deployment, Strategic Portfolio Management]
---

# Exploring SPM Enterprise-Wide Deployment

SPM Enterprise-Wide Deployment \(EWD\) partitions SPM tables data so that you can restrict record access by department, business unit, or other function.

\[Omitted video\] Description: SPM Enterprise-Wide Deployment overview

EWD is a Strategic Portfolio Management \(SPM\) product for enterprise-scale organizations that must balance centralized platform management with department-level data isolation. Administrators can create and configure partitions that separate data across functions such as IT Operations, HR, and Finance. Each partition is governed by a dedicated role that determines which records users can access, reducing the need for separate ServiceNow instances for each function.

EWD supports key SPM tables, including projects, demands, programs, and portfolios. Partition logic extends automatically to related records such as cost plans, resource plans, and planning items through automatic partition stamping. For the complete list of supported tables and related entities, see [Supported tables for partition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/supported-tables-for-partition-ewd.md).

## Partitions

A partition is a vertical data separation unit that controls which users and roles can access specific records within supported tables. Partitions are configured at the function level using a partition criteria field such as Department. Each partition is assigned a dedicated role that governs record visibility for users in that department.

For example, an organization can create separate partitions for IT Operations and HR Learning and Development. A user assigned to the IT Operations partition accesses only IT Operations projects, demands, and related records. That user can't access records belonging to the HR partition.

After a partition is configured, access control is enforced automatically at runtime. Partition criteria and role assignments determine data visibility without additional configuration.

This enforcement applies consistently across Project Workspace, Resource Management Workspace, Portfolio Planning Workspace, and Strategic Planning Workspace.

## Partition criteria

Partition criteria define the reference column that determines which partition a record belongs to. When a record is created, the application evaluates the value in the criteria column — such as **Department**, **Portfolio**, or **Investment Type** — and stamps the record with the matching partition.

Each supported table uses a single criteria column across all its partitions, so that records are segregated consistently throughout the SPM data model. When set, the criteria column is locked for that table to maintain consistency across existing and future partitions.

## Automatic partition stamping

When a record is created in a supported table, the application evaluates the partition criteria and stamps the partition value on the record. Partitions are assigned automatically — no manual assignment is required.

For related records and subentities such as cost plans, resource plans, and planning items, the partition value is automatically inherited from the parent record. This maintains data consistency across the full SPM data model without manual intervention.

For existing records created before partition configuration, an administrator can run a backfill job to stamp partition values on historical records.

## How partitions control access

Partitions enforce data visibility through Security Data Filters using a dynamic filter called **One of my partitions**. When a user accesses a record, the system evaluates their assigned partition role and returns only the records that match their partition criteria.

The following diagram shows the end-to-end flow of partition setup and access control across four departments: IT Ops, HR L&amp;D, Finance, and Sales.

\[Omitted image "partitions-feature-example.png"\] Alt text: Flowchart showing how EWD partitions control record access across four departments and roles.

An EWD admin creates partitions for each department and configures the partition criteria using a reference field such as Department on each supported table. An administrator assigns partition roles to department members and assigns the EWD PMO role to organization leads who require visibility across all partitions. For records created before partition configuration, a scheduled job stamps existing records with the correct partition value.

When a record such as a project, demand, program, or portfolio is created, the application stamps it with the correct partition based on the department field. The **One of my partitions** filter then evaluates the partition at runtime, so each user sees only the records in their assigned partition. Users with the PMO role can access records across all partitions.

The following examples show how partition access works at runtime:

-   A user assigned to the IT Ops partition can access only IT Ops projects and demands in all workspaces. No HR L&amp;D, Finance, or Sales data is visible in list views, search results, or dashboards.
-   A user assigned to the HR L&amp;D partition can access only HR L&amp;D records. No other partitioned data is visible anywhere in the application.
-   A user with roles for multiple partitions, such as a portfolio lead, can access records from all assigned partitions. Records appear across all views — workspaces, list views, search results, and dashboards — with no duplication or data merging.

Partition access also applies to the partitions themselves. When users select a partition from the **Current view** list on the Demands page in Strategic Planning Workspace, only the partitions they have access to are available. For example, a demand manager in the HR partition sees only the HR partition, not the IT Ops or Finance partitions. Users with the EWD admin or EWD PMO role can see all partitions.

Extended Security for Enterprise-Wide Deployment \(Extended Security for EWD\) provides additional security for partitioned tables. It extends partition access controls across APIs, agentic workflows, indirect references, and unpartitioned parent tables. For details, see [Additional security with Extended Security for EWD](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/additional-security-with-extended-security-ewd.md).

## Workspace support

EWD partition enforcement applies across the following workspaces:

-   Project Workspace — Partition enforcement applies across all tabs, including the **Details**, **Planning**, **Resources**, **Financials**, **RIDAC**, and **Status Reports** tabs.
-   Portfolio Planning Workspace \(PPW\) — Partition enforcement applies to projects, demands, roadmaps, scenario planning, financial planning, resource capacity, and dashboards.
-   Strategic Planning Workspace \(SPW\) — Partition enforcement applies to planning item types — project and demand — when the **ServiceNow Internal** Alignment integration is enabled. When a user populates the partition criteria field on either the planning item or its linked execution record, the partition details are stamped on both records. This bidirectional behavior helps strategic and operational teams work from the same data while maintaining departmental data separation. Partition support also extends to dashboards. On the Demands page, users can select a partition from the **Current view** list to see the dashboard mapped to that partition and only the demands in that partition.
-   Resource Management Workspace — Partition enforcement applies to resource plans, allocations, capacity views, and time cards linked to partitioned records.

## EWD roles

EWD includes two roles that govern partition creation, access, and record visibility:

-   **EWD admin \[sn\_spm\_ewd.ewd\_admin\]**

    Grants access for creating and configuring partitions. Users with this role can create partitions, define a role for each partition, configure partition criteria for each supported table, and manage partition settings. This role grants no elevated privileges outside the partition configuration scope.

-   **EWD PMO \[sn\_spm\_ewd.ewd\_pmo\]**

    Grants visibility across all partitions regardless of the assigned partition role. When the **One of my partitions** dynamic filter detects this role, all partition records are returned. Use this role for PMO users who require enterprise-wide visibility across all departments.


## Scope and limitations

Partition enforcement applies to classic form views, list views, search results, and dashboards. The following limitations apply:

-   Partition criteria can be defined only on reference columns available on the partitioned table.
-   All partitions on the same table must use the same reference column. For example, if Department is set as the criteria for the Project table, all subsequent partitions on the Project table must also use Department.
-   Different supported tables can each have their own criteria field defined independently — for example, the Demand table can use a different reference column than the Project table.
-   Only one condition per partition is supported.
-   Changing partition criteria after data has been populated requires deleting and recreating the affected partitions.
-   Partitioning is supported only on the Project \[pm\_project\], Portfolio \[pm\_portfolio\], Demand \[dmn\_demand\], and Program \[pm\_program\] tables.
-   Partition enforcement does not apply to indicator-based reports and widgets that calculate scores from a separate table. Users may see unfiltered data in indicator-based widgets regardless of their partition assignment.

## Comparing EWD with Extended Security for EWD

-   EWD: Partition SPM records by function so that users can access only the records in their assigned partitions.
-   Extended Security for EWD: Extend partition access controls across APIs, agentic workflows, indirect references, and unpartitioned parent tables.

|Feature|Enterprise-Wide Deployment|Extended Security for Enterprise-Wide Deployment|
|-------|--------------------------|------------------------------------------------|
|[Create and configure partitions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/create-partition-ewd.md)|\[Omitted image "icon-check-mark-green.png"\] Alt text: Yes|\[Omitted image "icon-check-mark-green.png"\] Alt text: Yes|
|[Assign partition role for access to the partition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/assign-partition-role-ewd.md)|\[Omitted image "icon-check-mark-green.png"\] Alt text: Yes|\[Omitted image "icon-check-mark-green.png"\] Alt text: Yes|
|[Assign PMO role for visibility across all partitions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/assign-pmo-roles-for-visibility-across-all-partitions.md)|\[Omitted image "icon-check-mark-green.png"\] Alt text: Yes|\[Omitted image "icon-check-mark-green.png"\] Alt text: Yes|
|[Update partition details for existing records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/update-partition-details-for-existing-records.md)|\[Omitted image "icon-check-mark-green.png"\] Alt text: Yes|\[Omitted image "icon-check-mark-green.png"\] Alt text: Yes|
|[Enable additional security for partitions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/enable-additional-security-extended-security-ewd.md)|\[Omitted image "icon-error-red-x.png"\] Alt text: No|\[Omitted image "icon-check-mark-green.png"\] Alt text: Yes|

**Note:** The Extended Security for Enterprise-Wide Deployment application is an extension to the Enterprise-Wide Deployment application. When you install the Extended Security for Enterprise-Wide Deployment application, you get all the features of Enterprise-Wide Deployment and the additional security for partitioned tables feature.

