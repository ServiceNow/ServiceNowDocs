---
title: Prepare to run the Azure Data Factory collector
description: Set up Azure data assets, authentication, and permissions before running the collector.Register an Azure application and create a client secret for Service Principal authentication.Obtain Azure subscription and tenant IDs for collector configuration.Grant Reader role to the Service Principal for Azure Data Factory access.Import dataset schemas to enable column and lineage harvesting.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/workflow-data-fabric/prepare-to-run-azure-data-factory-collector.html
release: australia
product: Workflow Data Fabric
classification: workflow-data-fabric
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Azure Data Factory metadata collector, Configuring metadata collectors, Data Catalog, Workflow Data Fabric]
---

# Prepare to run the Azure Data Factory collector

Set up Azure data assets, authentication, and permissions before running the collector.

## Before you begin

Role required: admin

## About this task

The collector uses Azure Service Principal for authentication. You must register an application, obtain Azure IDs, and grant subscription-level access. You can also prepare datasets for lineage harvesting.

## Procedure

1.  Register an application in Azure Active Directory and create credentials.

    See [Register application and create client secret](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/prepare-to-run-azure-data-factory-collector.md).

2.  Obtain required Azure IDs.

    See [Obtain subscription and tenant IDs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/prepare-to-run-azure-data-factory-collector.md).

3.  Grant Service Principal access to Data Factory data assets.

    See [Grant Service Principal access to Data Factory](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/prepare-to-run-azure-data-factory-collector.md).

4.  Prepare datasets for lineage harvesting.

    See [Prepare to harvest lineage](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/prepare-to-run-azure-data-factory-collector.md).


**Parent Topic:**[Azure Data Factory metadata collector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/azure-data-factory-metadata-collector.md)

## Register application and create client secret

Register an Azure application and create a client secret for Service Principal authentication.

### Before you begin

Role required: admin

### About this task

Register an application in Azure Active Directory and create credentials for the collector.

### Procedure

1.  Register a new application.

    1.  Navigate to **Azure Portal** &gt; **Azure Active Directory**.

    2.  Select **App Registrations**.

    3.  Select **New Registration**.

    4.  Enter the application name.

        Example: DataDotWorldADFApplication.

    5.  For **Supported account types**, select **Accounts in this organizational directory only**.

    6.  Select **Register**.

2.  Create a client secret.

    1.  On the application page, select **Certificates and Secrets** &gt; **Client secrets**.

    2.  Select **New client secret**.

    3.  Add a description and set the expiration date.

    4.  Select **Add**.

    5.  Copy and save the secret value.

3.  Obtain the Client ID.

    1.  Select the **Overview** tab.

    2.  Copy the Application \(Client\) ID from the Essentials section.


## Obtain subscription and tenant IDs

Obtain Azure subscription and tenant IDs for collector configuration.

### Before you begin

Role required: admin

### About this task

You will use these IDs when configuring the collector.

### Procedure

1.  Obtain the Tenant ID.

    1.  Navigate to the application page that you created.

    2.  Copy and save the Directory \(tenant\) ID.

        You will use this value for the Tenant ID field in the collector configuration.

2.  Obtain the Subscription ID.

    1.  Navigate to a storage account that you want to harvest from.

    2.  On the Overview page, copy the Subscription ID.

        You will use this value for the Subscription ID field in the collector configuration.


## Grant Service Principal access to Data Factory

Grant Reader role to the Service Principal for Azure Data Factory access.

### Before you begin

Role required: admin

### About this task

The Service Principal does not require explicit permission for each Data Factory. If the Data Factories you want to catalog were created within a specific subscription, add the Service Principal to that subscription with the Reader role.

### Procedure

1.  Navigate to the Subscriptions page in Azure Portal.

2.  Select the subscription containing your Data Factories.

3.  Select the **Access Control \(IAM\)** tab.

4.  Select **Add** &gt; **Add Role Assignment**.

5.  Under **Job Function Roles**, search for and select **Reader**.

6.  Select the **Members** tab.

7.  Select **Select Members**.

8.  Search for and select `DataDotWorldADFApplication`.

9.  Select **Review + assign**.


## Prepare to harvest lineage

Import dataset schemas to enable column and lineage harvesting.

### Before you begin

Role required: admin

### About this task

Complete this task if you want to harvest columns and the associated lineage.

### Procedure

1.  Navigate to the dataset you want to harvest columns and lineage from.

2.  Select the **Schema** tab.

3.  Select **Import Schema**.

4.  Publish the dataset.


