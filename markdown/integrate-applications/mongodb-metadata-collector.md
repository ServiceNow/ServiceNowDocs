---
title: MongoDB metadata collector
description: MongoDB metadata collector provides read-only access to metadata from a MongoDB account.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring metadata collectors, Data Catalog, Workflow Data Fabric]
---

# MongoDB metadata collector

MongoDB metadata collector provides read-only access to metadata from a MongoDB account.

The MongoDB collector harvests metadata from MongoDB instances \(clusters\), databases, collections, indexes, search indexes, and document fields. The collector supports harvesting nested fields for Document and Object field types. The collector captures relationship information between instances, databases, collections, document fields, search indexes, and indexes.

## Authentication supported

The MongoDB collector supports the following authentication methods:

-   Username and password authentication \(SCRAM\)
-   X.509 authentication
-   AWS Authentication

## Metadata cataloged

The MongoDB collector catalogs the following information:

|Object|Information cataloged|
|------|---------------------|
|MongoDB|MongoDB \(instance, cluster\) name, MongoDB \(instance, cluster\) version, Is Debug Mode|
|MongoDB Database|Database Name, Size On Disk, Is Empty, Views Number, Collections Number, Average Database Object Size, Data Size, Storage Size, Total Free Storage Size, Database Indexes Number, Database Indexes Size|
|MongoDB Collection \(including Materialized View\)|Collection Name, Documents Count, Collection Size, Average Object Size, Orphan Documents Number, Storage Size, Collection Free Storage Size, Total Index Size, Index Number, Collection Total Size, Is Capped, Capped Collection Maximum Size, Capped Documents Maximum Number|
|MongoDB View|View Name|
|MongoDB Collection Field|Field Name|
|MongoDB Index|Index Name, Index Size, Is Unique, Default Language|
|MongoDB Search Index|Index Name, Type, Status, Is Queryable, Is Dynamic, Creation Time|

## Relationships between objects

Catalog pages show relationships between the following data asset types:

<table id="table_a53_1zf_yhc"><thead><tr><th>

Data asset page

</th><th>

Relationship

</th></tr></thead><tbody><tr><td>

MongoDB

</td><td>

MongoDB Databases

</td></tr><tr><td>

MongoDB Database

</td><td>

-   MongoDB Collections
-   MongoDB instance
-   MongoDB Views

</td></tr><tr><td>

MongoDB Collection

</td><td>

-   MongoDB Database
-   MongoDB Collection Fields
-   MongoDB Indexes
-   MongoDB Search Indexes

</td></tr><tr><td>

MongoDB View

</td><td>

MongoDB Collection Field

</td></tr><tr><td>

MongoDB Collection FieldNote: The Analysis samples count parameter specifies the number of documents sampled from a collection to determine collection field types. This value must be a non-negative integer, with a default of 1000. Sampling is performed using the $sample aggregation. For more information, see the [MongoDB sampling documentation](https://www.mongodb.com/docs/manual/reference/operator/aggregation/sample/).

</td><td>

-   Nested MongoDB Collection Fields
-   MongoDB Collection
-   MongoDB View

</td></tr><tr><td>

MongoDB Index

</td><td>

MongoDB Collection

</td></tr><tr><td>

MongoDB Search Index

</td><td>

MongoDB Collection

</td></tr></tbody>
</table>-   **[Prepare to run the MongoDB collector](../task/prepare-to-run-mongodb-collector.md)**  
Create a MongoDB user and configure authentication before running the collector.
-   **[Create a MongoDB metadata collector](../task/create-mongodb-metadata-collector.md)**  
Create a collector to import metadata from MongoDB.

**Parent Topic:**[Configuring metadata collectors](configure-metadata-collectors-dc.md)

