---
title: Google Cloud Platform \(GCP\) Organization discovery with Patterns
description: The ServiceNow Discovery application uses the Discover Google Organization discovery pattern to find GCP Organization projects and resources. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: australia
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [GCP discovery, Available cloud discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Google Cloud Platform \(GCP\) Organization discovery with Patterns

The ServiceNow Discovery application uses the Discover Google Organization discovery pattern to find GCP Organization projects and resources. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Prerequisites

For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

-   **GCP Organization structure**

    Verify that a GCP Organization resource is structured correctly, with projects underneath it in a miscellaneous hierarchy.

    Ensure that all projects under the GCP Organization resource have the Compute Engine API enabled.

-   **Service Account user settings**

    Check that Service Account users have access to the GCP Organization resource node.

    Verify that Service Account users are members of all other projects located under the GCP Organization resource node.

    Ensure that Service Account users have the following Cloud Identity and Access Management credentials for projects under the GCP Organization resource:

    -   resourcemanager.folders.list
    -   resourcemanager.organizations.get
    -   resourcemanager.projects.get
    -   resourcemanager.projects.list
-   **Credentials for API elements**

    During the discovery, the pattern uses the following API elements. The user that was added to the credentials in the instance must have permissions to send these queries.

    -   https://cloudresourcemanager.googleapis.com/v1/\{name=organizations/\*\}
    -   https://cloudresourcemanager.googleapis.com/v1/projects
    -   https://cloudresourcemanager.googleapis.com/v2/folders:search
-   **Credentials for creating a discovery schedule**

    Configure the following credentials:

    1.  Create GCP credentials.
    2.  Create a GCP Service Account:
        1.  Credentials: The GCP credentials.
        2.  Account ID: The Google Service Account ID.
        3.  Datacenter type: Select **cmdb\_ci\_google\_datacenter**.
    3.  Create a discovery schedule.
-   **\(Optional\) Create a serverless discovery schedule**

    Create a discovery schedule to perform targeted discovery of GCP Organization resources.

    1.  Navigate to **Discovery** &gt; **Discovery Schedules**.
    2.  Click **New** and then fill in the form.

<table id="table_ut3_sby_hhb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name for the Discovery schedule. For example, `Discover GCP Organization`.

</td></tr><tr><td>

Discover

</td><td>

Discover type. Select **Serverless**.

</td></tr><tr><td>

MID Server

</td><td>

Name of the MID Server.

</td></tr><tr><td>

Active

</td><td>

Option for enabling this schedule for discovery. Select this check box to enable discovery.

</td></tr></tbody>
</table>    3.  Right-click the header of the Discovery Schedule form and select **Save**.
    4.  Click the **Serverless Execution Patterns** tab, click **New**, and then fill in the form.

        ![Serverless execution pattern](../image/serverless-execution-pattern.png)

        |Field|Description|
        |-----|-----------|
        |Name|Name for this Serverless Execution Pattern. For example, `Discover GCP Organization`.|
        |Pattern|Name of the pattern to run: Discover Google Organization.|
        |Proxy Host|Fully qualified domain name of the machine on which you are installing the proxy server. Specify **Global**.|
        |Active|Option for enabling this schedule for discovery. Select this check box to enable discovery.|

    5.  Under **Discovery Pattern Launcher Parameters**, configure the following parameters with the relevant values:

        |Parameter|Value|
        |---------|-----|
        |cloud\_account\_id|The Project ID within GCP.|
        |cloud\_cred\_id|The sysid of the GCP credentials.|
        |cloud\_datacenter\_type|`cmdb_ci_google_datacenter`|

        ![Pattern Launcher Parameters](../image/discovery-pattern-launcher-params.png)

-   **Customers with early access to the GCP Organization pattern**

    Verify that the Discover-GCP-SubAccounts scheduled job is not enabled in your instance.

    1.  Navigate to **System Definition** &gt; **Scheduled Jobs**.
    2.  Click the Discover-GCP-SubAccounts scheduled job.
    3.  Clear the **Active** check box, and then click **Update**.

## Data collected by Discovery during horizontal discovery

<table id="table_vk1_wvy_vmb"><thead><tr><th>

Table and field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Organization \[cmdb\_ci\_cloud\_org\]

</td></tr><tr><td>

name

</td><td>

The name of the organization resource.

</td></tr><tr><td>

object\_id

</td><td>

The ID of the organization resource.

</td></tr><tr><td>

time

</td><td>

The time the organization resource was created in GCP.

</td></tr><tr><td>

operational\_status

</td><td>

Current operational status. One of the following:-   Operational
-   Non-Operational
-   Repair in Progress
-   DR Standby
-   Ready
-   Retired

</td></tr><tr><td class="sub-head" colspan="2">

Folder \[cmdb\_ci\_gcp\_folder\]

</td></tr><tr><td>

name

</td><td>

The name of the organization folder.

</td></tr><tr><td>

parent\_id

</td><td>

The ID of the parent resource.

</td></tr><tr><td>

parent\_type

</td><td>

The type of the parent resource. Can be `organization` or `folder`.

</td></tr><tr><td>

time

</td><td>

The time the resource was created in GCP.

</td></tr><tr><td>

status

</td><td>

The status of the folder according to the `lifecycleState` status in GCP.

</td></tr><tr><td>

object\_id

</td><td>

The ID of the organization folder.

</td></tr><tr><td class="sub-head" colspan="2">

Project \[cmdb\_ci\_gcp\_project\]

</td></tr><tr><td>

name

</td><td>

The name of the project.

</td></tr><tr><td>

project\_id

</td><td>

The ID of the project.

</td></tr><tr><td>

parent\_id

</td><td>

The ID of the parent folder resource.

</td></tr><tr><td>

parent\_type

</td><td>

The type of the parent resource. Can be `organization` or `folder`.

</td></tr><tr><td>

time

</td><td>

The time the resource was created in GCP.

</td></tr><tr><td>

operational\_status

</td><td>

The status of the folder according to the `lifecycleState` status in GCP.

</td></tr><tr><td>

object\_id

</td><td>

The ID of the project.

</td></tr><tr><td>

discovery\_credentials

</td><td>

GCP account credentials.

</td></tr><tr><td class="sub-head" colspan="2">

Resource \[cmdb\_key\_value\]

</td></tr><tr><td>

key

</td><td>

The key, or label, associated with the GCP project. For example, `country`.

</td></tr><tr><td>

value

</td><td>

The project label value assigned to the GCP project. For example, `ca`.

</td></tr><tr><td>

configuration\_item

</td><td>

The URL or path of the CI.

</td></tr></tbody>
</table>## CI relationships

|CI|Relationship|CI|
|---|------------|---|
|Cloud Organization \[cmdb\_ci\_cloud\_org\]|Contained by::Contains|Google Project \[cmdb\_ci\_gcp\_project\]|
|Cloud Organization \[cmdb\_ci\_cloud\_org\]|Contained by::Contains|Service Account|
|Cloud Organization \[cmdb\_ci\_cloud\_org\]|Contained by::Contains|Google Folder \[cmdb\_ci\_gcp\_folder\]|
|Service Account|Owns::Owned by|Google Project \[cmdb\_ci\_gcp\_project\]|
|Google Folder \[cmdb\_ci\_gcp\_folder\]|Contained by::Contains|Google Project \[cmdb\_ci\_gcp\_project\]|
|Google Folder \[cmdb\_ci\_gcp\_folder\]|Contained by::Contains|Sub Google Folder|
|Sub Google Folder|Contained by::Contains|Google Project \[cmdb\_ci\_gcp\_project\]|

**Parent Topic:**[Google Cloud Platform \(GCP\) Cloud discovery using Patterns](gcp-cloud-discovery-patterns.md)

