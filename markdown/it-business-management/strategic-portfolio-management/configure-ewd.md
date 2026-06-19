---
title: Configuring SPM Enterprise-Wide Deployment
description: Configuring Enterprise-Wide Deployment \(EWD\) involves creating partitions, defining partition criteria for supported tables, and assigning partition roles to users or user groups to enforce function-level data separation.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/strategic-portfolio-management/configure-ewd.html
release: australia
product: Strategic Portfolio Management
classification: strategic-portfolio-management
topic_type: concept
last_updated: "2026-06-19"
reading_time_minutes: 2
breadcrumb: [SPM Enterprise-Wide Deployment, Strategic Portfolio Management]
---

# Configuring SPM Enterprise-Wide Deployment

Configuring Enterprise-Wide Deployment \(EWD\) involves creating partitions, defining partition criteria for supported tables, and assigning partition roles to users or user groups to enforce function-level data separation.

## High-level configuration process

EWD configuration is an administrative activity that requires planning before implementation. To achieve data separation with EWD, complete the following steps in order:

1.  Create a partition record with assigning a new or existing role to it. For details, see [Create and configure a partition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/strategic-portfolio-management/create-partition-ewd.md).
2.  Configure partition criteria for each supported table that you want to define data partitioning for that partition. For details, see [Assign partition role for access to the partition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/strategic-portfolio-management/assign-partition-role-ewd.md).
3.  Assign the partition role associated with the partition record to the users or user groups who should have access to those partitioned tables. For details, see [Verify partition configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/strategic-portfolio-management/verify-partition-configuration-ewd.md).

    Repeat this process for each function partition you need to create. For example, create separate partitions for IT Operations and HR Learning and Development.

4.  Update the existing records in the project, demand, programs, portfolios, and planning item tables with partition details by running the scheduled job. For details, see [Update partition details for existing records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/strategic-portfolio-management/update-partition-details-for-existing-records.md).

**Important:** Apply partition configuration changes and role assignments during a maintenance window when users are not accessing the instance, to ensure record visibility updates take effect correctly.

## Partition configuration checklist

Before configuring Enterprise-Wide Deployment, ensure the following are in place:

-   The EWD admin \[sn\_spm\_ewd.ewd\_admin\] role assigned to you.
-   The reference column to use as the partition criteria field is identified. All partitions on the same table must use the same reference column — for example, Department for all partitions on the Project table.
-   The users or user groups that should have access to each partition are identified.
-   A plan for handling existing records is in place. After configuring partitions, run the **Update existing records with partition details** scheduled job to populate partition values on historical records.

**Important:** Once partition criteria is configured for a table, the criteria field becomes read-only and cannot be changed for subsequent partitions on that table. Plan your partition structure accordingly before creating partitions.

## Supported tables for partition criteria

Partition criteria can be configured for the following core tables:

-   Project \[pm\_project\]
-   Demand \[dmn\_demand\]
-   Program \[pm\_program\]
-   Portfolio \[pm\_portfolio\]

Related records and sub-entities for these tables automatically inherit the partition value from the parent record. For a full list of tables in scope, see [Supported tables for partition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/strategic-portfolio-management/supported-tables-for-partition-ewd.md).

## Supported workspace versions

Partition enforcement is supported in the following workspaces. For partition enforcement to function in a workspace, that workspace must be installed at the specified minimum version:

-   Project Workspace \(7.3.0\)
-   Portfolio Planning Workspace \(8.15.0\)
-   Strategic Planning Workspace \(4.15.0\)
-   Resource Management Workspace \(5.7.0\)

