---
title: Google Cloud Platform \(GCP\) Big Query Out Of Box permissions
description: GCP Big Query Out Of Box catalog items permissions
locale: en-US
release: yokohama
product: Cloud Services Catalog
classification: cloud-services-catalog
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Google Cloud Platform \(GCP\) Big Query, Out Of Box Catalogs using Cloud Services Catalog, Cloud Services Catalog, ITOM Cloud Accelerate, IT Operations Management]
---

# Google Cloud Platform \(GCP\) Big Query Out Of Box permissions

GCP Big Query Out Of Box catalog items permissions

<table id="table_ug3_wqz_dbc"><thead><tr><th>

Catalog item

</th><th>

Services

</th><th>

Permission

</th></tr></thead><tbody><tr><td rowspan="3">

CSC GCP BigQuery

</td><td>

Provision

</td><td>

-   bigquery.datasets.create
-   bigquery.tables.create
-   storage.objects.get

</td></tr><tr><td>

Pointed discovery

</td><td>

-   bigquery.tables.list
-   bigquery.datasets.get

</td></tr><tr><td>

Deprovision

</td><td>

-   bigquery.tables.delete
-   bigquery.datasets.delete
-   bigquery.routines.delete
-   bigquery.models.delete

</td></tr></tbody>
</table>**Parent Topic:**[Google Cloud Platform \(GCP\) Big Query](google-cloud-platform-big-query.md)

