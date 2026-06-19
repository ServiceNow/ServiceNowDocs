---
title: Data catalog navigation
description: Access Connect Hub to manage metadata collectors and the Data Catalog to discover and govern data assets.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/workflow-data-fabric/data-catalog-navigation.html
release: australia
product: Workflow Data Fabric
classification: workflow-data-fabric
topic_type: concept
last_updated: "2026-04-23"
reading_time_minutes: 1
breadcrumb: [Explore, Data Catalog, Workflow Data Fabric]
---

# Data catalog navigation

Access Connect Hub to manage metadata collectors and the Data Catalog to discover and govern data assets.

Both areas are accessed from the same starting point: navigate to **All** &gt; **Workflow Data Fabric** &gt; **Workflow Data Fabric Home**, then select the relevant icon in the sidebar. Connection Admins work in Connect Hub to bring data into the catalog. Data Stewards and Catalog Viewers work in the Data Catalog to manage and discover it.

## Connect Hub

Connect Hub is accessed from **All** &gt; **Workflow Data Fabric** &gt; **Workflow Data Fabric Home** by selecting the Connect Hub icon in the left sidebar in the sidebar. Connection Admins create and manage metadata collectors in Connect Hub. These automated scanners connect to external data sources, harvest table schemas, column definitions, lineage, and other metadata, and publish them to the Data Catalog. Collectors can be run on demand or scheduled to keep catalog content current as source systems evolve. Runtime logs for each collector run are also available in Connect Hub for monitoring and troubleshooting. \[Omitted image "dc-navigation-metadata-collectors.gif"\] Alt text: Connect Hub in Workflow Data Fabric Home showing a list of configured metadata collectors with their connection status.

## Data Catalog

The Data Catalog is accessed from **All** &gt; **Workflow Data Fabric** &gt; **Workflow Data Fabric Home** by selecting the Data Catalog icon in the sidebar. This is the primary workspace for both Data Stewards and Catalog Viewers. Catalog Viewers search and browse published data assets and open asset detail pages to review schemas, lineage, and governance metadata. Data Stewards use the same catalog interface to manage asset metadata. \[Omitted image "dc-navigation-data-catalog.gif"\] Alt text: Data Catalog search view showing filter panel and a list of data assets with descriptions and source system labels.

