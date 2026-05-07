---
title: Data products navigation
description: Navigate to four areas to build, publish, and manage data products from data ingestion through consumer access.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-04-23"
reading_time_minutes: 1
breadcrumb: [Explore, Data Products, Workflow Data Fabric]
---

# Data products navigation

Navigate to four areas to build, publish, and manage data products from data ingestion through consumer access.

The data products workflow spans four platform areas, each serving a specific stage from data ingestion to consumer access. Navigate to **All** &gt; **Workflow Data Fabric** &gt; **Workflow Data Fabric Home** to access all areas from the sidebar.

## Connect Hub

Connect Hub is where zero-copy connectors and metadata collectors are configured. Zero-copy connectors establish the live data pathway between ServiceNow and external systems such as Snowflake, Databricks, and Oracle. Metadata collectors are configured separately and run on a schedule to publish data asset metadata to the Data Catalog. ![Connect Hub interface for managing meta data collectors and zero copy connectors](../image/wdf-navigation-connect-hub.png)

## Data Workbench

Data Workbench is the authoring environment where Data Stewards create, configure, and manage data interfaces and data products. It provides a list of all draft and published assets, with filtering by type and status. All creation and editing of data assets happens in Data Workbench. ![Data Workbench interface displaying a list of data products and data interfaces.](../image/wdf-navigation-data-workbench.png)

## Data Catalog

The Data Catalog is where consumers discover published data products and request access. After a data product is published and the metadata collector runs, it is set to visible in the Data Catalog with its name, description, tags, and included data interfaces. Consumers submit access requests through the Data Catalog.![Data Catalog interface with search functionality, filters, and search results showing available data assets.](../image/wdf-navigation-data-catalog.png)

## Approval Center

Approval Center is where approvers review and process access requests for data products. When consumers request access to a data product, approval tasks are routed here for review. Approvers can grant or deny access based on governance policies, automatically provisioning the necessary roles for approved requests. ![Approval Center showing the Approvals list with pending access requests and their details.](../image/wdf-navigation-approve-access.png)

