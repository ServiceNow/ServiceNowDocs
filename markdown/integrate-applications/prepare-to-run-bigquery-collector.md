---
title: Prepare to run the BigQuery collector
description: Create a service account and configure authentication before running the collector.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [BigQuery metadata collector, Configuring metadata collectors, Data Catalog, Workflow Data Fabric]
---

# Prepare to run the BigQuery collector

Create a service account and configure authentication before running the collector.

## Before you begin

Role required: admin

## About this task

The collector connects to BigQuery using a service account associated with your project.

## Procedure

1.  Create a [service account](https://cloud.google.com/iam/docs/creating-managing-service-accounts).

    Assign the following roles to the service account:

    -   [BigQuery Data Viewer](https://cloud.google.com/bigquery/docs/access-control#bigquery.dataViewer)
    -   [BigQuery User](https://cloud.google.com/bigquery/docs/access-control#bigquery.user)
2.  Create a key for the service account and download the JSON key file.

    See the [Creating and managing service account keys](https://cloud.google.com/iam/docs/creating-managing-service-account-keys) documentation for details.

3.  Place the key file on the machine where you plan to run the collector.

    You need this file when configuring the collector.


## What to do next

See the [Google Cloud Platform predefined roles and permissions documentation](https://cloud.google.com/iam/docs/understanding-roles#predefined_roles) for additional information.

**Parent Topic:**[BigQuery metadata collector](../concept/bigquery-metadata-collector.md)

