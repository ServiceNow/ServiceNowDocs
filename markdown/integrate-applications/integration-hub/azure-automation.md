---
title: Microsoft Azure Automation Spoke
description: Integrate the ServiceNow instance with the Microsoft Azure Automation. Manage the cloud-based automation and configuration services from your ServiceNow instance. Also reuse this short description in the release notes.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Microsoft Azure Automation Spoke

Integrate the ServiceNow instance with the Microsoft Azure Automation. Manage the cloud-based automation and configuration services from your ServiceNow instance.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

The Microsoft Azure Automation spoke v2.0.0 is the latest version.

## Supported versions

This spoke was built for the Microsoft Azure Automation 2023-11-01 version, but may be compatible with the later versions.

## Spoke requirements

Microsoft Azure account.

## Spoke dependencies

If you’re having trouble installing the app, confirm that these dependent plugins are installed:

-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   Complex Object \(com.glide.cobject\)
-   ServiceNow Flow Designer - Dynamic Inputs \(com.glide.hub.dynamic\_inputs\)
-   ServiceNow IntegrationHub Action Template - Data Stream \(com.glide.hub.action\_type.datastream\)
-   Azure Resource Management spoke \(sn\_azure\_rm\_spoke\) v2.0.0 is installed and a connection alias is created on your instance.

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation. For more information on the licenses, contact your account manager.

## Spoke actions

The Microsoft Azure Automation spoke provides actions to automate the Microsoft Azure tasks when events occur in your ServiceNow instance. Available actions include:

|Category|Action|Description|
|--------|------|-----------|
|Account Management|Create Account|Creates an automation account.|
|Delete Account|Deletes an account.|
|Look up Account|Retrieves the details of an automation account using the resource group.|
|Look up Accounts Stream by Resource Group|Retrieves the list of accounts present under the specified resource group. Page size is fixed to 100 according to Microsoft.|
|Look up Accounts Stream by Subscription ID|Retrieves the list of accounts present under the specified subscription ID. Page size is fixed to 100 according to Microsoft.|
|Update Account|Updates the details of an automation account.|
|Job Management|Create Job|Creates a job of the runbook.|
|Look up Job|Retrieves the details of a runbook job.|
|Look up Job Output|Retrieves the details of an executed job output identified by the job ID.|
|Look up Job Schedule|Retrieves the details of a scheduled job.|
|Look up Job Schedules Stream|Retrieves the list of scheduled jobs present in an automation account. The page size is fixed to 100 according to Microsoft.|
|Look up Jobs Stream|Retrieves the list of runbook jobs present in an automation account. Page size is fixed to 100 according to Microsoft.|
|Resume Job|Resumes the job identified by job name.|
|Stop Job|Stops the job execution identified by job name.|
|Suspend Job|Suspends the job identified by job name.|
|Job Schedule Management|Create Job Schedule|Creates a schedule for a job execution.|
|Delete Job Schedule|Deletes a job schedule.|
|Runbook Management|Create Runbook|Creates a runbook.|
|Delete Runbook|Deletes a runbook.|
|Look up Runbook|Retrieves the details of a runbook.|
|Look up Runbook Content|Retrieves the content of the a runbook.|
|Look up Runbooks Stream|Retrieves the list of runbooks present in an automation account. Page size is fixed to 100 according to Microsoft.|
|Update Runbook|Updates the details of a runbook.|
|Schedule Management|Create Schedule|Creates a schedule.|
|Delete Schedule|Deletes a schedule.|
|Look up Schedule|Retrieves the details of a schedule.|
|Look up Schedules Stream|Retrieves the list of schedules present in an automation account. Page size is fixed to 100 according to Microsoft.|
|Update Schedule|Updates the details of a schedule.|
|Software Update Configuration Management|Look up Software Update Configuration Machine Runs Stream|Retrieves the list of software update configuration machine runs present in an automation account. Page size is fixed to 100 according to Microsoft.|
|Look up Software Update Configuration Run|Retrieves the details of a software update configuration run.|
|Look up Software Update Configuration Runs Stream|Retrieves the list of software update configuration runs present in an automation account. Page size is fixed to 100 according to Microsoft.|
|State Configuration Management|Compile DSC Configuration|Creates the desired State Configuration compilation job.|
|Create DSC Configuration|Creates the desired State Configuration.|
|Look up DSC Configuration|Retrieves the details of the Desired State Configuration.|
|Look up DSC Configuration Content|Retrieves the content of the Desired State Configuration.|
|Look up DSC Configurations Stream|Retrieves the list of DSC Configurations present in an automation account. Page size is fixed to 100 according to Microsoft.|
|Look up Nodes Stream|Retrieves the list of Nodes present in an automation account. Page size is fixed to 100 according to Microsoft.|
|Update DSC Configuration|Updates the Desired State Configuration.|
|Update Node DSC Configuration|Updates the details of desired State Configuration for the specified node\(VM\).|
|Watcher Management|Delete Watcher|Deletes the watcher.|
|Look up Watchers Stream|Retrieves the list of watchers present in an automation account. Page size is fixed to 100 according to Microsoft.|
|Start Watcher|Starts the watcher.|
|Stop Watcher|Stops the watcher.|

## Set up the Microsoft Azure Automation Spoke

To execute the actions of the Microsoft Azure Automation Spoke, you must first install and configure the Microsoft Azure Resource Management Spoke. No separate configuration of the Microsoft Azure Automation Spoke is necessary. To view the procedure to set up the Microsoft Azure Resource Management Spoke, see [Set up the Microsoft Azure Resource Management spoke](../task/setup-res-mngmt.md#).

