---
title: Set up and configure billing data export in Google Cloud
description: Create a Google Cloud billing account, set up a project and BigQuery dataset, and enable detailed usage cost export so Cloud Cost Management can download your Google Cloud billing data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-asset-management/cloud-cost-management/create-gcp-service-account.html
release: zurich
product: Cloud Cost Management
classification: cloud-cost-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [Set up access to Google Cloud billing and usage data, Configure Cloud Cost Management for Google Cloud, Configure, Cloud Cost Management, IT Asset Management]
---

# Set up and configure billing data export in Google Cloud

Create a Google Cloud billing account, set up a project and BigQuery dataset, and enable detailed usage cost export so Cloud Cost Management can download your Google Cloud billing data.

## Before you begin

-   Role required: Google Cloud administrator
-   You must be familiar with Google Cloud policies.
-   To create a Google Cloud billing account, you must have the Billing Account Creator role at the organization level.
-   To enable and configure the billing usage cost export, you must have the Billing Account Costs Manager role or the Billing Account Administrator role on the target billing account.
-   To create the BigQuery project and dataset, you must have the BigQuery user role on the target project.

## About this task

Before Cloud Cost Management can download your Google Cloud billing data, you must set up detailed usage cost export in the Google Cloud Console. This involves creating a billing account \(if you don't have one\), creating a project and BigQuery dataset to store the exported data, and enabling the export. You also must note a few key values: your billing account ID, BigQuery project ID, and BigQuery dataset name, which you will use later when you schedule the Billing Download job in Cloud Cost Management.

## Procedure

1.  Create a Google Cloud billing account.

    1.  Log in to the Manage billing accounts page in the [Google Cloud Console](https://console.cloud.google.com/billing).

    2.  Select **Add billing account**.

    3.  Follow the steps to complete billing account creation.

        For more information, see [Create a billing account](https://docs.cloud.google.com/billing/docs/how-to/create-billing-account#create-new-billing-account) in Google Cloud documentation.

2.  Create a project to store your billing data in a BigQuery dataset.

    1.  Go to [Project selector](https://console.cloud.google.com/projectselector2/home/dashboard) in the Google Cloud Console.

    2.  Select **Create project** and fill in the required fields to create a project.

    **Note:** Verify the following:

    -   Billing is enabled on the Google Cloud project you create to contain your dataset.
    -   The same billing account must be linked to this project that contains the data that you plan to export to the BigQuery dataset.
3.  Create a service account under the project and generate a key.

    1.  In the Google Cloud Console, navigate to **Identity &amp; Access** &gt; **Service Accounts** for your project.

    2.  Select **Create service account** and provide required details.

        You must assign the Viewer role to the service account.

    3.  Select **Create and close**.

        The service account gets added to the list of service accounts for the project.

    4.  Select the service account and go to the Keys tab.

    5.  Select **Add key** and create a key.

        A dialog box opens prompting you to select the key type.

    6.  Select **JSON** and then select **Create**.

        This action downloads the JSON file, which contains the Project ID and private key, on your device. Keep the file in a secure location for later use.

4.  In the Google Cloud Console, enable Detailed usage costs to use Google Cloud Billing Download.\[Omitted image "billing\_export.png"\] Alt text: Detailed usage costs

    **Note:** If you’re configuring the billing download BigQuery dataset for the first time, read the Data availability section in the [Understand the Cloud Billing data tables in Big Query](https://cloud.google.com/billing/docs/how-to/export-data-bigquery-tables) topic in Google Cloud documentation.

5.  Record the values that you need for the Google Cloud Billing Download job in Cloud Cost Management.

    |Field|Location|Example|
    |-----|--------|-------|
    |Billing account ID|**Google Cloud Console** &gt; **Billing** &gt; **Account management**. The ID appears near the account name.|0XX0A-AXX9-6XXXA|
    |BigQuery project ID|**Google Cloud Console** &gt; **BigQuery**. The ID appears at the project selector at the top of the Explorer panel.|my-finops-project|
    |BigQuery dataset name|**Google Cloud Console** &gt; **BigQuery**. The name appears on the Explorer panel under your project.|all\_billing\_data|


## What to do next

Create Google API credentials to access data securely on your provider account. For details, see [Create Google API credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/cloud-cost-management/create-google-api-credentials.md).

**Related topics**  


[Enable cost allocation in Google Cloud for Kubernetes cluster](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/cloud-cost-management/enable-cost-allocation-kc-gcp.md)

[Schedule and manage the jobs that download Google Cloud billing data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/cloud-cost-management/gcp-bill-dwnld-job-cloudin.md)

