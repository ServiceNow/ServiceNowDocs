---
title: UiPath Spoke
description: Automate business processes in UiPath from your ServiceNow instance.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# UiPath Spoke

Automate business processes in UiPath from your ServiceNow® instance.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## IntegrationHub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

UiPath spoke v2.5.0 is the latest version.

## Supported version

This spoke was built for these UiPath versions, but may be compatible with later versions.

-   Platform version 2020.4.1
-   Cloud Platform version 2022.7.14

## Spoke requirements

Ensure that you have UiPath account information before you [Set up the UiPath spoke](../task/conf-alias-uipath.md#).

-   If you are using the UiPath Cloud Platform:
    -   Token URL
    -   Client Id
    -   Account Logical Name
    -   Tenant Logical Name
    -   User Key
-   If you are using the UiPath Platform installed on private or public cloud:
    -   Tenant Name
    -   Credentials to authenticate the UiPath Orchestrator API

See the [UiPath documentation](https://docs.uipath.com/orchestrator) for more information about obtaining the required details.

## Spoke subflows

The UiPath spoke provides subflows to retrieve information about jobs, processes, robots, and so on. Available subflows include:

|Subflow|Description|
|-------|-----------|
|Process UiPath Job Webhook|Retrieves information about the jobs in UiPath. This subflow is the answer for the default Flow: Process UiPath Job Webhook routing policy.|
|Process UiPath Process Webhook|Retrieves information about the processes in UiPath. This subflow is the answer for the default Flow: Process UiPath Process Webhook routing policy.|
|Process UiPath Robot Webhook|Retrieves information about the robots in UiPath. This subflow is the answer for the default Flow: Process UiPath Robot Webhook routing policy.|
|Process UiPath Any Webhook|Retrieves information about any other required entity. To process information about the required entity, create a copy of this subflow and customize it as per your requirement.|

**Note:** While customizing a new subflow, create a copy of one of the default subflows to ensure that all the default input payload items are present.

## Spoke actions

The UiPath spoke provides actions to manage environments, jobs, machines, processes, robots, queue, and release, when events occur in ServiceNow. Available actions include:

<table id="table_utm_22z_wkb"><thead><tr><th>

Category

</th><th>

Action

</th><th>

Description

</th></tr></thead><tbody><tr><td rowspan="3">

Environment Management**Note:** These actions work within classic folders only.

</td><td>

Look up Environment by ID

</td><td>

Retrieves the details of the required environment.

</td></tr><tr><td>

Look up Environments

</td><td>

Retrieves the details of the required environments. The environments are retrieved based on the filter query.

</td></tr><tr><td>

Look up Folders

</td><td>

Looks up folders under a tenant in UiPath and gets the folder name and ID.

</td></tr><tr><td rowspan="3">

Job Management

</td><td>

Look up Job By ID

</td><td>

Retrieves the details of the required job.

</td></tr><tr><td>

Look up Jobs

</td><td>

Retrieves the details of the required jobs. The jobs are retrieved based on the filter query.

</td></tr><tr><td>

Start Jobs

</td><td>

Starts the jobs to execute the required process.**Note:** When working with the modern folders, select either **Allocate Dynamically** from the **Execution Target** list.

</td></tr><tr><td rowspan="2">

Machine Management

</td><td>

Look up Machine By ID

</td><td>

Retrieves the details of the required machine.

</td></tr><tr><td>

Look up Machines

</td><td>

Retrieves the details of the required machines. The machines are retrieved based on the filter query.

</td></tr><tr><td>

Process Management

</td><td>

Look up Processes

</td><td>

Retrieves the details of the required processes. The processes are retrieved based on the filter query.

</td></tr><tr><td rowspan="6">

Queue Management

</td><td>

Add Item to Queue

</td><td>

Adds a new item to the specified queue.

</td></tr><tr><td>

Create Queue

</td><td>

Creates a queue with the specified configuration.

</td></tr><tr><td>

Delete Queue

</td><td>

Deletes the specified queue.

</td></tr><tr><td>

Delete Queue Item

</td><td>

Deletes the specified queue item.

</td></tr><tr><td>

Look up Queue Items

</td><td>

Retrieves a list of queue item definition records.

</td></tr><tr><td>

Look up Queues

</td><td>

Retrieves the details of the required queue definition records. The queues are retrieved based on the filter query.

</td></tr><tr><td rowspan="2">

Release Management

</td><td>

Look up Release By ID

</td><td>

Retrieves the details of the required release.

</td></tr><tr><td>

Look up Releases

</td><td>

Retrieves the details of the required releases. The releases are retrieved based on the filter query.

</td></tr><tr><td rowspan="4">

Robot Management**Note:** These actions work within classic folders only.

</td><td>

Create Robot

</td><td>

Creates a robot in UiPath.

</td></tr><tr><td>

Delete Robot

</td><td>

Deletes a robot in UiPath.

</td></tr><tr><td>

Look up Robot By ID

</td><td>

Retrieves the details of the required robot.

</td></tr><tr><td>

Look up Robots

</td><td>

Retrieves the details of the required robots. The robots are retrieved based on the filter query.

</td></tr><tr><td>

Session Management**Note:** These actions work within classic folders only.

</td><td>

Look up Sessions

</td><td>

Retrieves the details of the required sessions. The sessions are retrieved based on the filter query.

</td></tr></tbody>
</table>## Spoke modules

The UiPath spoke adds the UiPath application to your ServiceNow instance. The UiPath application includes these modules:

|Module|Description|
|------|-----------|
|UiPath Webhook Registries|Contains details about the webhook registry records.|
|UiPath Webhook Routing Policies|Contains details about the webhook routing policy records. Three routing policies are available with the spoke that retrieve information about jobs, robots, and processes.|

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection. For more information, see [Connections and Credentials](https://www.servicenow.com/docs/access?context=r-credentials&version=australia&pubname=australia-platform-security&ft:locale=en-US).

For information about setting up the spoke, see [Set up the UiPath spoke](../task/conf-alias-uipath.md#).

## MID Server requirements

These actions use REST calls, which can run on an instance or MID Server. Use the connection record associated with the UiPath alias to configure where actions run as well as set MID Server selection attributes. For more information, see [MID server](https://www.servicenow.com/docs/access?context=mid-server-landing&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

**Note:** The MID Server users must have the sn\_uipath\_spoke.uipath\_admin role.

To set up the MID Server for this spoke, see [Set up MID Server for a spoke](../task/config-adv-mid-settings-for-oauth-on-mid.md).

