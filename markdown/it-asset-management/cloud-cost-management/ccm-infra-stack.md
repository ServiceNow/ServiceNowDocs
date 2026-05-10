---
title: Cloud Cost Management Infra Stack
description: Use the Cloud Cost Management Infra Stack application to process and download billing files with improved data processing speed. The Cloud Cost Management Infra Stack application also supports high transaction volumes.
locale: en-US
release: australia
product: Cloud Cost Management
classification: cloud-cost-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Exploring Cloud Cost Management, Cloud Cost Management, IT Asset Management]
---

# Cloud Cost Management Infra Stack

Use the Cloud Cost Management Infra Stack application to process and download billing files with improved data processing speed. The Cloud Cost Management Infra Stack application also supports high transaction volumes.

## Overview of the Cloud Cost Management Infra Stack application

The Cloud Cost Management Infra Stack application is an optional plugin that can be installed alongside Cloud Cost Management version 8.1 and later from the ServiceNow Store. Installing this plugin also activates the Glide Fenix \(com.glide.fenix\) plugin.

**Important:** If you have activated the Cloud Cost Management Infra Stack application, you can't deactivate it later.

Provider-specific credential aliases are installed by default with the Cloud Cost Management Infra Stack application.

|Provider|Credential alias|
|--------|----------------|
|AWS|ccm\_aws\_alias|
|Microsoft Azure|ccm\_azure\_alias|
|Google Cloud|ccm\_google\_alias|

For the billing download job to complete successfully, you should map the alias that's applicable to your cloud provider with the corresponding credentials.

## Benefits of the Cloud Cost Management Infra Stack application

The Cloud Cost Management Infra Stack application offers several key benefits for more efficient and effective cloud cost management. These benefits enable organizations to optimize their cloud resources and reduce overall costs.

-   **Improved data processing speed**

    The application significantly improves data processing speed, which enables faster processing and analysis of billing files.

-   **Support for high transaction volumes**

    It’s designed to handle high transaction volumes efficiently, making it suitable for large-scale cloud environments.

-   **Enhanced performance with Kubernetes**

    The application uses a cost-aware Kubernetes cluster that helps it process billing data with cost efficiency and manage complex cloud infrastructures effectively.

-   **Better cloud cost management**

    By providing frequent insights and faster data processing, the Cloud Cost Management Infra Stack application enables organizations to manage their cloud costs effectively and make informed decisions.


## Requirements for processing billing jobs using the Cloud Cost Management Infra Stack application

The framework of the Cloud Cost Management Infra Stack application enables parallel processing of billing files, resulting in faster processing of large files. The application processes billing jobs using a Kubernetes cluster that's outside Cloud Cost Management Glide but within ServiceNow datacenters.

You must fulfill these requirements to process billing jobs.

-   Map all the provider-specific credentials of your billing download jobs to the corresponding credential alias. For example, if you have two AWS credentials, map them to ccm\_aws\_alias so that the billing download job completes successfully. For more details on mapping credentials to aliases, see [Credential aliases for Discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/connections-and-credentials/discovery-credential-alias.md).

    **Note:** If you’re upgrading from an earlier version to Cloud Cost Management version 10.0 and have installed the Cloud Cost Management Infra Stack application, the mapping of credentials to alias happens automatically for all active billing download jobs. However, for any new job, you should do the mapping manually.

-   Make sure to have enough storage on your Cloud Cost Management Glide database for storing the attachments of the AWS billing job with Assume role authentication temporarily until the billing download job is processed. After the job is complete, these temporary attachments are deleted from the Glide database. The storage that you should have depends on the size of data on AWS. For more details, see [Processing AWS billing jobs with Assume role authentication](process-aws-assume-infra.md).

