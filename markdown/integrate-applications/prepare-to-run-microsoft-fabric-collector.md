---
title: Prepare to run the Microsoft Fabric collector
description: Set up access and authentication for your Fabric instance before running the collector.Register an application in the Azure Portal and obtain the Client ID, Tenant ID, and client secret for the Microsoft Fabric collector.Enable service principal access to Fabric APIs and grant workspace access for the Microsoft Fabric collector.Enable metadata scanning to allow the collector to access detailed data source information and establish lineage.Enable report image harvesting to allow the collector to export Fabric reports as images.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/prepare-to-run-microsoft-fabric-collector.html
release: brazil
topic_type: task
last_updated: "2026-09-17"
reading_time_minutes: 4
keywords: [Microsoft Fabric, collector, authentication, service principal, Azure, metadata scanning, Microsoft Fabric, collector, app registration, client secret, Azure, Microsoft Fabric, collector, service principal, authentication, workspace access, Microsoft Fabric, collector, metadata scanning, lineage, Fabric APIs, Microsoft Fabric, collector, report images, image harvesting]
breadcrumb: [Microsoft Fabric metadata collector, Configuring metadata collectors, Data Catalog, Workflow Data Fabric]
---

# Prepare to run the Microsoft Fabric collector

Set up access and authentication for your Fabric instance before running the collector.

## Before you begin

A Fabric administrator is needed to enable settings in the Fabric Admin Portal.

The collector can only harvest metadata for Fabric workspaces to which the service principal has been given access.

The collector uses a JDBC connection to catalog database resources from Warehouses and Lakehouses with service principal authentication. The collector also uses the following APIs to catalog detailed metadata about Fabric resources: Fabric APIs, OneLake APIs, and Power BI APIs.

Role required: admin

## Procedure

1.  Register your application in the Azure Portal and obtain the required IDs.

    See [Register application and get IDs for the Microsoft Fabric collector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/prepare-to-run-microsoft-fabric-collector.md).

2.  Set up service principal authentication.

    See [Set up service principal authentication for the Microsoft Fabric collector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/prepare-to-run-microsoft-fabric-collector.md).

3.  Set up metadata scanning.

    See [Set up metadata scanning for the Microsoft Fabric collector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/prepare-to-run-microsoft-fabric-collector.md).

4.  Configure report image harvesting.

    See [Configure report image harvesting for the Microsoft Fabric collector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/prepare-to-run-microsoft-fabric-collector.md).


**Parent Topic:**[Microsoft Fabric metadata collector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/microsoft-fabric-metadata-collector.md)

## Register application and get IDs for the Microsoft Fabric collector

Register an application in the Azure Portal and obtain the Client ID, Tenant ID, and client secret for the Microsoft Fabric collector.

### Before you begin

Role required: admin

### Procedure

1.  Go to the [Azure Portal](https://portal.azure.com/) and select **App Registrations** in the Azure services.

2.  Select **New Registration** and enter the following information.

    |Field|Value|
    |-----|-----|
    |**Application Name**|For example, DataDotWorldFabricApplication|
    |**Supported account types**|Accounts in this organizational directory only|

3.  Select **Register** to complete the registration.

4.  Create a client secret.

    1.  On the application page, select **Certificates and Secrets**.

    2.  Select **Secret** and add a description.

    3.  Select the desired expiration date.

    4.  Select **Create** and copy the secret value.

5.  Obtain the Client ID and Tenant ID.

    1.  Select the **Overview** tab in the left sidebar of the App registration.

    2.  Copy the Client ID from the Essentials section.

    3.  Copy the Tenant ID from the Essentials section.


## Set up service principal authentication for the Microsoft Fabric collector

Enable service principal access to Fabric APIs and grant workspace access for the Microsoft Fabric collector.

### Before you begin

The service principal must have at least [contributor access](https://learn.microsoft.com/en-us/rest/api/fabric/datapipeline/items/get-data-pipeline-definition?tabs=HTTP) to the workspace.

Role required: admin

### Procedure

1.  Sign in to Fabric using a Fabric Admin account.

2.  Navigate to **Settings** &gt; **Admin Portal**.

3.  Under developer settings, search for **Service principals can use Fabric APIs**.

4.  Enable the setting and select whether it applies to the entire organization or a specific security group that includes the service principal.

5.  Select **Apply** to save the changes.

    For more information, see the [Microsoft documentation](https://learn.microsoft.com/en-us/power-bi/developer/embedded/embed-service-principal?tabs=azure-portal#step-3---enable-the-power-bi-service-admin-settings).

6.  Open the workspace and select **Manage access**.

7.  Search for the service principal or the security group the service principal belongs to.

    At a minimum, [Contributor](https://learn.microsoft.com/en-us/rest/api/fabric/datapipeline/items/get-data-pipeline-definition?tabs=HTTP) access is required.

8.  Select **Add**.


## Set up metadata scanning for the Microsoft Fabric collector

Enable metadata scanning to allow the collector to access detailed data source information and establish lineage.

### Before you begin

A Fabric administrator must complete this setup before running metadata scanning on an organization's Fabric workspaces. Familiarize yourself with the [limitations to the scanner APIs](https://learn.microsoft.com/en-us/fabric/governance/metadata-scanning-run#considerations-and-limitations).

Role required: admin

### About this task

The collector uses the [Fabric Scanner APIs](https://learn.microsoft.com/en-us/power-bi/enterprise/service-admin-metadata-scanning) to establish lineage to source tables and columns.

### Procedure

1.  Follow the [Fabric documentation](https://learn.microsoft.com/en-us/fabric/admin/enable-service-principal-admin-apis) to enable service principal authentication for Fabric read-only APIs.

2.  Follow the [Fabric documentation](https://learn.microsoft.com/en-us/fabric/admin/metadata-scanning-setup#enable-tenant-settings-for-metadata-scanning) to enable the following enhanced tenant settings for metadata scanning.

    -   Enhance admin APIs responses with detailed metadata
    -   Enhance admin APIs responses with DAX and mashup expressions
    **Warning:** When running under a service principal, no API permissions are required, and the registered app must have no admin-consent-required permissions set in the Azure portal. For more information, see [Enable service principal authentication for read-only admin APIs](https://learn.microsoft.com/en-us/fabric/admin/metadata-scanning-enable-read-only-apis).


## Configure report image harvesting for the Microsoft Fabric collector

Enable report image harvesting to allow the collector to export Fabric reports as images.

### Before you begin

Reports must be located in a workspace with Premium, Embedded, or Fabric capacity. For details, see the [Fabric documentation](https://learn.microsoft.com/en-us/power-bi/developer/embedded/export-to#considerations-and-limitations).

Role required: admin

### Procedure

1.  Enable the **Export reports as image files** setting from the [Admin settings](https://learn.microsoft.com/en-us/power-bi/developer/embedded/export-to#using-the-api).

2.  Confirm that the reports to be exported are in a workspace with Premium, Embedded, or Fabric capacity.

3.  If using non-Fabric database sources, set up a data source YAML file for lineage mapping.

    See the [Power BI collector documentation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/prepare-to-run-powerbi-collector.md) for instructions. This can be used with the **Datasource Name Mapping File** option in the Microsoft Fabric collector.


