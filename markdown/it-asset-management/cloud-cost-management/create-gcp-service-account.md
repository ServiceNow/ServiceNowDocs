---
title: Create a Google Cloud billing account
description: Create a billing account, project, and BigQuery dataset in the Google Cloud Console.
locale: en-US
release: xanadu
product: Cloud Cost Management
classification: cloud-cost-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Set up access to Google Cloud billing and usage data, Configure Cloud Cost Management for Google Cloud, Configuring Cloud Cost Management, Cloud Cost Management, IT Asset Management]
---

# Create a Google Cloud billing account

Create a billing account, project, and BigQuery dataset in the Google Cloud Console.

## Before you begin

You must be familiar with Google Cloud policies.

Role required: Google Cloud administrator

## Procedure

1.  Under the Google Cloud billing account, create a project that can store the billing data in a BigQuery dataset.

    **Note:** Charges associated with BigQuery usage are based on billing plans.

    1.  Create a service account under the project and create a key.

        See the Create service accounts and Manage service accounts sections in [Google Cloud docs](https://cloud.google.com/iam/docs) for more information.

    2.  Configure the service account to have access to all projects.

        You must have the Viewer role to all the projects.

    3.  Download the key file \(JSON file\) which contains the required credentials.

2.  In the Google Cloud, enable Detailed usage costs to use Google Cloud Billing Download.![Detailed usage costs](../image/billing_export.png)

    **Note:** If you’re configuring the billing download BigQuery dataset for the first time, read the Data availability section in the [Understand the Cloud Billing data tables in Big Query](https://cloud.google.com/billing/docs/how-to/export-data-bigquery-tables) topic from [Google cloud documentation](https://cloud.google.com/docs).


