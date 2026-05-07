---
title: dbt Cloud metadata collector
description: The dbt Cloud metadata collector provides read-only access to metadata from an external dbt Cloud account.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configuring metadata collectors, Data Catalog, Workflow Data Fabric]
---

# dbt Cloud metadata collector

The dbt Cloud metadata collector provides read-only access to metadata from an external dbt Cloud account.

The dbt cloud collector connects to the dbt cloud project and harvests dbt assets and column-level lineage relationships from database views associated with dbt assets.

## Metadata cataloged

The dbt Cloud collector catalogs the following information.

|Object|Information cataloged|
|------|---------------------|
|Analysis|Name, Description, Path, Root path, Package name, Unique ID, Alias, Meta, Raw SQL, Compiled SQL/Compiled Code, Enabled, Materialized, Resource type|
|Model|Name, Description, Path, Root path, Package name, Unique ID, Alias, Meta, Raw SQL, Compiled SQL/Compiled Code, Enabled, Materialized, Resource type|
|Model column|Column name|
|Project|Name, Project version|
|Snapshot|Name, Description, Path, Root path, Package name, Unique ID, Alias, Meta, Raw SQL/Raw Code, Compiled SQL/Compiled Code, Enabled, Materialized, Resource type|
|Seed|Name, Description, Path, Root path, Package name, Unique ID, Alias, Meta, Raw SQL/Raw Code, Compiled SQL/Compiled Code, Enabled, Materialized, Resource type|
|Source|Name, Description, Path, Root path, Package name, Unique ID, Alias, Meta, Raw SQL/Raw Code, Compiled SQL/Compiled Code, Enabled, Source name, Resource type|
|Test|Name, Description, Path, Root path, Package name, Unique ID, Alias, Meta, Raw SQL/Raw Code, Compiled SQL/Compiled Code, Enabled, Materialized, Resource type|
|Test result|Time the test was executed, Status, Count of failures \(if any\), Message emitted by the test \(if any\)|
|Semantic Models|Name, Description, Path, Package name, Unique ID, Enabled, Resource Type, Semantic Model Components, Primary Entity|
|Entities|Title, SQL Expression, Entity Type|
|Dimensions|Title, Dimension Type|
|Measures|Title, Description, Has Measure Aggregation|
|Metrics|Title, Description, Path, Package Name, Unique ID, Metric Type|

## Relationship between objects

Catalog pages show relationships between the following data asset types:

|Data asset page|Relationship|
|---------------|------------|
|Model|Project containing dbt model, Tests testing the integrity of model, dbt data assets \(test, seed, model, snapshot, source\) that are upstream of model, dbt data assets \(Test, Seed, Model, Snapshot, Source\) that are downstream of model|
|Semantic Model|Project containing the semantic model, dbt model related to the semantic model, dbt semantic model components \(dimensions, entities, measures\), Metric that the semantic model provides context for|
|Model column|The database column in the manifested table or view|
|Project|dbt data assets \(Test, Seed, Model, Snapshot, Source\) contained within project|
|Snapshot|Project containing dbt project, dbt data assets \(Test, Seed, Model, Source\) that are upstream of snapshot, dbt data assets \(Test, Seed, Model, Source\) that are downstream of snapshot|
|Seed|Project containing dbt project, dbt data assets \(Test, Seed, Model, Snapshot, Source\) that are upstream of seed, dbt data assets \(Test, Seed, Model, Snapshot, Source\) that are downstream of seed|
|Source|Project containing dbt project, dbt data assets \(Test, Seed, Model, Snapshot\) that are downstream of seed, Database schema that the source represents|
|Test|Project containing dbt project, dbt model that has its integrity tested by this test|
|Test result|The dbt test that was executed to produce the result|

## Lineage for dbt

The following lineage information is collected by the dbt Cloud collector.

|Object|Lineage available|
|------|-----------------|
|dbt model materialized as view|Referenced database tables and columns in dbt model materialized as view|
|dbt resource|dbt data assets that are upstream and downstream \(for example, seeds that are upstream of models, and tests that are downstream of models\) of dbt data asset.|

Snowflake is the currently supported data source for cross-system lineage.

-   **[Prepare to run the dbt Cloud collector](../task/prepare-to-run-dbt-cloud-collector.md#)**  
Configure dbt Cloud and create authentication tokens before running the collector.
-   **[Create a dbt Cloud metadata collector](../task/create-dbt-cloud-metadata-collector.md)**  
Create a collector to import metadata from dbt Cloud.

**Parent Topic:**[Configuring metadata collectors](configure-metadata-collectors-dc.md)

