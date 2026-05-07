---
title: Explore Data Catalog
description: The Data Catalog is the self-service discovery layer for finding, evaluating, and accessing governed data assets.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Data Catalog, Workflow Data Fabric]
---

# Explore Data Catalog

The Data Catalog is the self-service discovery layer for finding, evaluating, and accessing governed data assets.

The Data Catalog provides a centralized discovery and governance layer where users search for data assets, understand their lineage and quality, and request access to governed data across the enterprise.

## Data Catalog overview

The Data Catalog addresses a common enterprise challenge. Data exists across dozens of systems, but finding trustworthy, well-documented assets requires manual coordination across teams. The Data Catalog solves this by providing a unified discovery layer. Metadata collectors automatically harvest technical metadata, Data Stewards add business context, and consumers evaluate trust scores and lineage before requesting access.

Search and discovery:

Find data assets through keyword search, faceted filtering, and browsing by source system, domain, or collection. Search looks across asset names, descriptions, tags, classifications, and business glossary terms. Results include trust scores and quality indicators. ![View of data assets in the data catalog](../image/data-catalog-home.png)

Asset details and relationships:

View comprehensive details for each data asset including schema, field descriptions, ownership, data classifications, and data relationships, including lineage. ![View details of a data asset](../image/dc-data-asset-details.png)

Business glossary:

Create and maintain business glossary terms that define enterprise data vocabulary. Link glossary terms to catalog assets to provide business context. This promotes consistent use of data definitions across the organization. ![List of glossary terms](../image/dc-glossary-list.png)

Metadata collectors:

Automated scanners that connect to source systems, discover schemas, and build lineage relationships. They populate the Data Catalog with technical metadata. Collectors run on schedules or on demand to keep catalog metadata current as source systems evolve. ![List of metadata collectors](../image/dc-mcollector-list.png)

## Data Catalog users

|User|Description|
|----|-----------|
|Connection admin|Creates and manages connections to external systems and configures metadata collectors. Schedules collector runs and monitors collection execution and logs.|
|Data Steward|Enriches catalog assets with business context and creates and maintains business glossary terms. Links terms to assets, assigns ownership, manages tags and classifications, organizes assets into domains and collections, and tracks asset lifecycle status.|
|Catalog Viewer|Searches and browses the Data Catalog to discover data assets. Views asset details and lineage, evaluates trust scores and quality indicators, previews sample data, and identifies assets for use in analytics, workflows, or AI applications.|

## Data Catalog workflow

This lifecycle shows the distinct phases of discovery, governance, and consumption in the Data Catalog:

1.  Connect: Connection Admins create connections to external data sources and configure metadata collectors. These harvest technical metadata including schemas, tables, columns, relationships, and lineage.
2.  Harvest: Metadata collectors run on schedules or on demand to discover assets and build lineage relationships. They populate the catalog with up-to-date technical metadata from connected source systems.
3.  Enrich: Data Stewards add business context by creating glossary terms, linking terms to assets, adding descriptions, assigning ownership, applying classifications, and organizing assets into domains and collections
4.  Discover: Catalog Viewers search and browse to find relevant data assets. They review metadata and lineage, evaluate trust scores, preview sample data, and identify assets that meet their requirements.
5.  Access: Users request access to discovered assets through governance workflows. After approval, they consume governed data through Data Fabric tables, APIs, analytics dashboards, or AI agents.

## Data Catalog benefits

|Benefit|Feature|Users|
|-------|-------|-----|
|Find data assets across enterprise systems without manual coordination|Search, browse, faceted filtering|All users|
|Understand data quality and trustworthiness before requesting access|Trust scores, quality indicators, sample data preview|Catalog Viewer|
|Automatically discover and catalog metadata as source systems evolve|Metadata collectors, scheduled harvesting|Connection admin|
|Provide business context and shared vocabulary for enterprise data|Business glossary terms, asset descriptions|Data Steward|
|Organize and classify assets for improved discoverability and governance|Domains, collections, tags, classifications|Data Steward|
|Establish accountability through ownership and stewardship assignments|Owner and steward assignment, lifecycle management|Data Steward|

## What to explore next

To learn more about using the Data Catalog, see:

-   [Configuring metadata collectors](configure-metadata-collectors-dc.md)
-   [Finding and accessing data assets](find-access-data-assets-dc.md)
-   [Governing the Data Catalog](manage-data-catalog.md)

