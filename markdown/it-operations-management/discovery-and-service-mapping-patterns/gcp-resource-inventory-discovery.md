---
title: Google Cloud Platform \(GCP\) resource inventory discovery with Patterns
description: The ServiceNow Discovery application uses the Google Cloud Platform \(GCP\) asset inventory pattern to find GCP resources and policies. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: zurich
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 8
breadcrumb: [GCP discovery, Available cloud discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Google Cloud Platform \(GCP\) resource inventory discovery with Patterns

The ServiceNow Discovery application uses the Google Cloud Platform \(GCP\) asset inventory pattern to find GCP resources and policies. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

The pattern provides visibility for services supported by the Asset Inventory API, as well as collecting inventory data on the deployed GCP services and updating the CMDB.

The pattern collects inventory data either for all GCP-supported resources or for a preconfigured inclusion list of resources. The Cloud Inventory Resource Inclusion List contains all resource types supported by GCP Cloud Asset Inventory, except for Compute Engine resources and IAM policies. You can expand the inclusion list with additional resource types per your requirements. For more information about Google Cloud assets, see [https://cloud.google.com/resource-manager/docs/cloud-asset-inventory/overview](https://cloud.google.com/resource-manager/docs/cloud-asset-inventory/overview).

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

Starting with Discovery and Service Mapping Patterns version 1.18.1, you can discover the GCP storage by two types of discovery: Serverless and Cloud Discovery. Running Cloud Discovery schedules enables you to run one schedule per all your GCP projects without manually configuring separate schedules. You can also continue using Serverless discovery as before.

The enhanced Google Cloud Platform \(GCP\) asset inventory pattern runs queries to check the configurations on your system and trigger a discovery according to your configurations. The queries by order:

1.  If you have the **Discovery Pattern Launcher Parameters** configured, the pattern triggers a Serverless discovery schedule.

2.  If the former query carries no results, the pattern continues to query if you have the **mid.gcp\_resource\_inventory\_bucketpath** MID Server property configured. If you do, the pattern runs a Cloud Discovery schedule by cloud accounts.

3.  If the former query carries no results, the pattern continues to query if you have the **mid.gcp\_resource\_inventory\_bucketpath.default** MID Server property configured. If you do, the pattern triggers a default Cloud Discovery schedule.

4.  If none of these properties are configured, the pattern terminates gracefully.

## Prerequisites

-   **Verify the store apps are up to date**
    -   Discovery and Service Mapping Patterns
    -   Visibility Content
-   **GCP authorization for Discovery to use the Cloud Asset API**
    -   API endpoint: https://cloudasset.googleapis.com/v1/projects/&lt;account\_id&gt;:exportAssets
    -   Required one or more of the following IAM permissions on the specified resource parent:
        -   cloudasset.assets.exportResource
        -   cloudasset.assets.exportIamPolicy
-   **Service Account user for the cloud storage API**

    The ServiceNow Cloud Service Account need to have a read-only permission from GCP to access the API endpoint - https://www.googleapis.com/storage/v1.

    **Note:** You can use the headers on the Encryption page to do the following:

    -   Download an object that is encrypted by a customer-supplied encryption key.
    -   Get object metadata with content hashes.
-   **Permission to read and write to a Cloud Storage Bucket**
    -   Storage Object Creator
    -   Storage Object Viewer
    -   Storage Object Admin
-   **Create a cloud storage bucket using Google Cloud console**
    1.  Go to the **Google Cloud console**.
    2.  From the **Navigation menu**, select **Cloud Storage** &gt; **Buckets**.
    3.  To create a new bucket, select **+ Create**.
    4.  On the **Create a bucket** page, fill in the bucket information.

<table id="table_zsj_vdw_pbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name your bucket

</td><td>

Enter a globally unique name for your bucket.

</td></tr><tr><td>

Choose where to store your data

</td><td>

Select a Location type and Location where the bucket data will be permanently stored.-   Location type: Multi-region, for global storage \(for example, us, eu, asia\).
-   Location: List of the Cloud Storage locations available for storing your data.


</td></tr><tr><td>

Choose a storage class for your data

</td><td>

Select the appropriate storage class for your needs \(for example, Standard, Nearline, Coldline, or Archive\).

</td></tr><tr><td>

Choose how to control access to objects

</td><td>

Select whether or not your bucket enforces public access prevention.

</td></tr><tr><td>

Choose how to protect object data

</td><td>

Configure protection tools, if required.

</td></tr></tbody>
</table>    5.  Select **Create**.

        **Note:** For more information, see [Google Cloud Storage documentation](https://cloud.google.com/storage/docs).

-   **Retention Policy for the storage bucket**

    Ensure that the Retention Policy for the storage bucket is not active. If the Retention Policy is active, the auto-generated inventory data file cannot be deleted by the pattern.

-   **Create a Serverless discovery schedule**

    Create a discovery schedule to perform targeted discovery of GCP asset inventory.

    1.  Navigate to **Discovery** &gt; **Discovery Schedules**.
    2.  Click **New** and then fill in the form.![Serverless discovery](../../it-operations-management/image/itom-serverless-discovery.png)

<table id="table_ut3_sby_hhb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name for the Discovery schedule. For example, `Discover GCP Asset Inventory`.

</td></tr><tr><td>

Discover

</td><td>

Discover type. Select **Serverless**.

</td></tr><tr><td>

MID Server

</td><td>

Name of the MID Server.

</td></tr><tr><td>

Run

</td><td>

Option to select when should the next discovery run.

</td></tr></tbody>
</table>    3.  Right-click the header of the Discovery Schedule form and select **Save**.
    4.  Click the **Serverless Execution Patterns** tab, click **New**, and then fill in the form. ![Serverless execution patterns](../../it-operations-management/image/itom-serverless-execution-patterns.png)

        |Field|Description|
        |-----|-----------|
        |Name|Name for this Serverless Execution Pattern. For example, `Discover GCP Asset Inventory`.|
        |Pattern|Select the **Google Cloud Platform \(GCP\) Resource Inventory** pattern.|
        |Proxy Host|Fully qualified domain name of the machine on which you are installing the proxy server. Specify **Global**.|
        |Active|Option for enabling this schedule for discovery. Select this check box to enable discovery.|

    5.  Select **Submit**.
    6.  In the **Discovery Pattern Launcher Parameters** tab, configure the following parameters with the relevant values:

        |Parameter|Value|
        |---------|-----|
        |cloud\_account\_id|The Project ID within GCP.|
        |full\_path\_file|The complete file path of the storage bucket. For example: `gs://<bucketname>`.|
        |cloud\_cred\_id|The sysid of the GCP credentials.|
        |cloud\_datacenter\_type|`cmdb_ci_google_datacenter`|

-   **Storage discovery configurations with MID Server properties**

    1.  Configure the **mid.gcp\_resource\_inventory\_bucketpath** property.

        1.  Navigate to **All** &gt; **MID Server** &gt; **Properties** and filter the list by `Name start with mid.gcp`.
        2.  Select **mid.gcp\_resource\_inventory\_bucketpath**.
        3.  fill in the form.
            1.  Configure the property **Name** field to include your account ID as follows:`mid.gcp_resource_inventory_bucketpath.<Cloud Account Id>`.
            2.  Fill in the **Value** field with the bucket URI, which is the complete file path of the storage bucket. For example: `gs://<bucketname>`.
            3.  In the **MID Server** field, leave it blank to set a MID Server property that affects all MID Servers. To set a MID Server property for a particularMID Server, select the preferred server.
            4.  Select **Update**.
    2.  Configure the **mid.gcp\_resource\_inventory\_bucketpath.default** property.

        1.  Navigate to **All** &gt; **MID Server** &gt; **Properties** and filter the list by `Name start with mid.gcp`.
        2.  Select **mid.gcp\_resource\_inventory\_bucketpath.default**.
        3.  Fill in the **Value** field with the bucket URI, which is the complete file path of the storage bucket. For example: `gs://<bucketname>`.
        4.  Select **Update**.
    For more information, see [Export asset metadata from one project to another](https://cloud.google.com/asset-inventory/docs/faq#export-between-projects)

-   **Cloud inventory resource inclusion list**
    -   To collect inventory data for resources supported by GCP, in ServiceNow AI Platform, navigate to **Cloud Inventory Resource Inclusion List** and clear all GCP table records.

        ![GCP Inclusion List](../image/GCP-inclusion-list.png "Cloud Inventory Resource Inclusion List")

    -   Fine-tune GCP resource discovery using the Cloud Inventory Resource Inclusion List.

        If your deployment has custom patterns for GCP discovery, ensure that you do not discover GCP resources twice:

        1.  Ensure that the application scope is Discovery and Service Mapping Patterns:
            1.  Navigate to **Settings** &gt; **Developer**.
            2.  Select `Discovery and Service Mapping Patterns` from the **Application** list.
        2.  Navigate to **System Definitions** &gt; **Tables**.
        3.  Open the Cloud Inventory Resource Inclusion List \[sa\_cloud\_inventory\_resource\_whitelist\] table.
        4.  Under **Related Links**, click **Show List**.
        5.  Select resource types for which you have custom patterns, and select `Delete` from the **Actions on selected rows** list.
        The Cloud Inventory Resource Inclusion List is predefined with common services. You can expand the list with additional resource types that you want the pattern to discover, as follows:

        **Note:** If you modify the list provided in the base system, it is no longer updated automatically in application updates. You need to maintain customized lists yourself.

        1.  Open the Cloud Inventory Resource Inclusion List \[sa\_cloud\_inventory\_resource\_whitelist\] table.
        2.  Click **New**.
        3.  Fill in the form, and then click **Submit**.

            **Note:** The names of additional resource types must conform to the appropriate vendor naming conventions.

            |Field|Description|
            |-----|-----------|
            |Cloud Vendor|The vendor of the resource type: GCP.|
            |Resource Type|The GCP resource type value.|
            |Application|The application scope: Discovery and Service Mapping Patterns.|

        The changes are applied the next time you run the pattern.


## Data collected by Discovery during horizontal discovery

This pattern discovers data that provides visibility for all GCP services in your organization. The discovered data includes the following tables and fields.

|Table and field|Description|
|---------------|-----------|
|Main CI \[cmdb\_ci\_cmp\_resource\]|
|object\_id|The ID of the item. The item is accessed with this URL.|
|name|The name of the resource.|
|resource\_type|The asset resource type, according to the data in the JSON file.|
|Key Value \[cmdb\_key\_value\]|
|Key|The GCP tag key name.|
|Value|The GCP tag value name.|

The Dependency Views map shows the discovered Configuration Items \(CIs\) in your organization and the relationships between them. Here, the only meaningful relationship between the CIs is the one that helps Discovery identify them.

Each GCP Inventory CI is related either to a Logical Datacenter \(LDC\) CI or to a Cloud Service Account CI. In this example, the Inventory CI is related to a Cloud Service Account CI.

![CIs and connections on a Dependency Views map](../../discovery/image/gcp-inventory-dependency-views.png "Dependency Views map showing Cloud Service Account CI")

## CI relationships

These relationships are created to support GCP asset inventory discovery:

|CI|Relationship|CI|
|---|------------|---|
|For Global Resources:|
|Main CI \[cmdb\_ci\_cmp\_resource\]|Contained by::Contains|Cloud Service Accounts|
|For Regional Resources:|
|Main CI \[cmdb\_ci\_cmp\_resource\]|HostedOn::Hosts|Logical Datacenter \(LDC\)|

**Parent Topic:**[Google Cloud Platform \(GCP\) Cloud discovery using Patterns](gcp-cloud-discovery-patterns.md)

