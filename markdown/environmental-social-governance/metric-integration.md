---
title: Metric integration
description: The metric integration tool enables you to manage your third-party Operational Sustainability Management data by normalizing and mass loading data using flat file. The terms flat file and normalized data refer to how data is stored electronically.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Exploring GRC: Metrics, GRC: Metrics, Operational Sustainability Management \(formerly Environmental, Social, and Governance\)]
---

# Metric integration

The metric integration tool enables you to manage your third-party Operational Sustainability Management data by normalizing and mass loading data using flat file. The terms flat file and normalized data refer to how data is stored electronically.

Metric integrations is a common import utility tool for GRC: Metrics, which can be used by multiple integrations to import data from an external source, such as a spreadsheet, into the metric data. This tool uses different mapping configurations to obtain the data needed to create or update existing metric data.

The following are the benefits of the metric integration tool:

-   Provides flat file normalization for bulk data uploads.
-   Enables configurations for your own integrations or uses the default configurations provided by ServiceNow, such as the Watershed integration.
-   Enables the automatic creation of metric definitions.
-   Provides the ability to automate the creation or update of data in bulk.
-   Provides the ability to automate the creation of entity types and entities.
-   Provides the ability to set up your own normalization and upload rules for metrics.
-   Helps to stage data to verify the upload format of data being updated or created.
-   Enables users to clean up data before loading to the database using the error log.

The Metric integration form also enables you to [create data mappings](../../esg-management-reporting/task/create-an-entity-mapping.md). Data mappings enable you to map the columns from any source of data such as the Watershed spreadsheet with the metric definitions. You must ensure that the data is mapped according to your system. For example, Watershed may name an entity as Office at Atlanta, US, whereas the metric definition may have the entity name as Atlanta, US-office. This difference would result in a mismatch when importing the data. To prevent this issue, you must ensure that the data mapping is accurate. When you map data, it is important to understand that metrics are derived from the combination of entity, entity type, and metric definition. Therefore, you must have the following tables in your data mapping.

-   sn\_grc\_profile
-   sn\_grc\_profile\_type
-   sn\_grc\_metric\_definition

