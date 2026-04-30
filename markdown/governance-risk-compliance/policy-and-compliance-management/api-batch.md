---
title: Accessing the batch records in the content integration batch table
description: You can access the batch records in the content integration batch table that is displayed in the GRC: Policy and Compliance integrator application UI. By accessing these records, you can import the data into the Policy and Compliance Management application.
locale: en-US
release: yokohama
product: Policy and Compliance Management
classification: policy-and-compliance-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [GRC: Policy and Compliance integrator, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Accessing the batch records in the content integration batch table

You can access the batch records in the content integration batch table that is displayed in the GRC: Policy and Compliance integrator application UI. By accessing these records, you can import the data into the Policy and Compliance Management application.

## Overview of the content integration batch table

As a user with the sn\_compliance.admin role, you can access the batch records in the content integration batch table and create a library import task for each record. The compliance managers assignment group reviews the library import task and imports the staging records into the Policy and Compliance Management tables.

## Details of the content integration batch table

The content integration batch table displays the details that are shown in the following example:

-   Number of the content integration batch record. In the example, CIB0001006 is the record number.
-   Provider of the content integration batch. In the example, Thomson Reuters is the provider.
-   State of the content integration batch. In the example, the state is New.
-   Domain of the content integration batch. In the example, the domain is Global.
-   Content type of the content integration batch. In the example, the type is Compliance.

![Content integration batch records table.](../image/cib-records.png "Content integration batch records table")

To learn how you can use the user roles to access the APIs and batch records, see [User roles for the integration process](../../grc-integrations-with-third-party-content/reference/int-integrator-user-roles.md).

Select a record in the table to display the content integration batch record form and its related lists. See the following example.

**Note:** The fields in the form and the related lists are auto-populated.

![Content integration batch record form.](../image/cib-record-staging-related-lists.png "Content integration batch record form")

## Using the Compliance staging processor flow

You can use the new Compliance staging processor flow that is provided with the GRC: Policy and Compliance integrator application. See the following example. The flow is used to process the compliance staging data and it runs in the background on a weekly basis. It searches for the content integration batch records where the state is Ready and the content type is Compliance. For each record in the content integration batch, it creates a library import task and it updates the content integration batch status automatically.

![Compliance staging processor flow.](../image/compliance-staging-processor-flow.png "Compliance staging processor flow")

**Note:** You can update the flow to change its setting. For example, you can update the start time of the flow.

## Using the REST APIs

You can use the REST APIs to insert the records in the GRC: integrations with third-party content and later move the records to the Policy and Compliance Management tables by using the GRC: Policy and Compliance integrator application. The following internal APIs are provided with the GRC: integrations with third-party content application and the GRC: Policy and Compliance integrator application:

-   Create batch
-   Insert policy staging records
-   Update batch status to ready
-   Get batch
-   Cancel batch

**Note:** You can use third-party tools, such as the Postman API platform, to execute the APIs.

When you execute the APIs in the Postman API platform as shown in the following example, the staging records are imported in the Policy and Compliance Management tables.

![Create a batch using the Postman API platform.](../image/create-batch-postman.png "Create a batch using the Postman API platform")

## Processing the batch records

The Update batch status to ready API and the Compliance staging processor flow process the batch records as follows:

1.  The Update batch status to ready API updates the content integration batch status to Ready as shown in the figure.

    ![Batch status Ready in the content integration batch.](../image/batch-status-cib-module.png "Batch status Ready in the content integration batch")

2.  The Compliance staging processor flow picks up the content integration batch and its records. When the Update batch status to Ready API sets the content integration batch status to Ready, the Compliance staging processor flow acknowledges the content integration batch.
3.  When the state of the content integration batch is updated to Ready, the Compliance staging processor flow starts importing the records from staging to the GRC: Policy and Compliance integrator application.

    The system automatically creates a library import task to track the import process.

4.  When the library import task is created, the Compliance staging processor flow automatically updates the batch status to In progress.
5.  When the library import task is created and the provider that is mentioned in the content integration batch is not found, the state of the task is updated to Provider onboarding. A provider import task is created in the content onboarding task related list of the library import task.
6.  As the library import task is created, the staging recommendations for each record are generated for the content integration batch as shown in the following example.

    ![Staging recommendations.](../image/staging-recommendations.png "Staging recommendations")


The library import task is used to import the staging records in the Policy and Compliance Management tables. The library import task and staging recommendations for each record are displayed for the content integration batch table in the GRC: Policy and Compliance integrator module. A user with the sn\_compliance.admin role can assign the library import task to the compliance managers assignment group. To learn how to assign a library import task, see [Assign a library import task for approval](../task/assign-lib-import-task.md).

