---
title: Configure the Source-to-Pay integration with Oracle EBS
description: Integrate the ServiceNow instance and Oracle EBS by creating a custom OAuth application in Oracle EBS to authenticate ServiceNow requests.
locale: en-US
release: australia
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Source-to-Pay integration with Oracle EBS, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Configure the Source-to-Pay integration with Oracle EBS

Integrate the ServiceNow instance and Oracle EBS by creating a custom OAuth application in Oracle EBS to authenticate ServiceNow requests.

## Application set up

Verify that you have performed the following:

-   Activated the Source-to-Pay integration with the Oracle EBS application from ServiceNow Store. This automatically activates the Oracle EBS Spoke.
-   Set up [Oracle EBS Spoke](https://www.servicenow.com/docs/csh?topicname=setup-oebs-spoke&version=yokohama&pubname=yokohama-integrate-applications).
-   Activated the Source-to-Pay integration framework from ServiceNow Store. Source-to-Pay integration with Oracle EBS uses the Source-to-Pay integration framework to pull tasks from Oracle EBS into ServiceNow. For more information on the Source-to-Pay integration framework, see [Source-to-Pay integration framework](source-to-pay-integration-framework.md).


## Primary Data Integration with Oracle EBS's Dependencies

Install the following dependencies of Primary Data integration with Oracle EBS. When you install the plugin, all the dependencies get installed automatically. All primary data are synchronized based on the configurable scheduled job Fetch Spend Primary Data.

Run the Trigger Oracle EBS Integration that pulls tasks into ServiceNow. For more information, see [Use schedule flows in Oracle EBS](using-schedule-flows-oracle-ebs.md).

|App name|Plugin ID|
|--------|---------|
|ERP Integration Framework|sn\_fcms\_intg|
|Source-to-pay Common Architecture|sn\_shop|
|Supplier Common Architecture|sn\_slm|
|EBS Spoke|sn\_oracle\_ebs\_spk|

## Supplier Lifecycle Operations Integration Dependencies with Oracle EBS

Install the following dependencies of Supplier Lifecycle Operations integration with Oracle EBS. When you install the plugin, all the dependencies get installed automatically.

|App name|Plugin ID|
|--------|---------|
|Primary Data Integration with Oracle EBS|sn\_orcl\_data\_int|
|Source-to-Pay Integration Framework|sn\_spend\_intg|

## Sourcing and Procurement Operations Integration Dependencies with Oracle EBS

Install the following dependencies of Sourcing and Procurement Operations integration with Oracle EBS. When you install the plugin, all the dependencies get installed automatically.

|App name|Plugin ID|
|--------|---------|
|Primary Data Integration with Oracle EBS|sn\_orcl\_data\_int|
|Sourcing and Purchasing Automation|sn\_pr|
|Source-to-Pay Integration Framework|sn\_spend\_intg|

## Accounts Payable Operations Integration Dependencies with Oracle EBS

Install the following dependencies of Accounts Payable Operations integration with Oracle EBS. When you install the plugin, all the dependencies get installed automatically.

|App name|Plugin ID|
|--------|---------|
|Primary Data Integration with Oracle EBS|sn\_orcl\_data\_int|
|Accounts Payable Invoice Processing|sn\_ap\_apm|
|Source-to-Pay Integration Framework|sn\_spend\_intg|

-   **[ERP source configuration for Oracle EBS](erp-source-configuration-oracle.md)**  
Configure your Source-to-Pay \(S2P\) instance to support inbound and outbound integration with your ERP system. This integration configuration enables you to automatically post purchase order, receipt, invoice, and download primary data from the ERP.
-   **[Define ERP source configuration for Oracle EBS](../task/define-erp-source-oracle.md)**  
ERP source configuration determines the ERP source to which your ERP system connects. Map the integration payload with the Oracle EBS tables.
-   **[Configure integration services for Oracle EBS](../task/configure-service-maps-oracle-ebs.md)**  
For configuring integration services, provide the connection end point and the Oracle EBS ERP credentials that you set up for your authentication profile. Also, create a separate web service record for each service request that you want to customize.
-   **[Load data to ERP user-mapping table for Oracle EBS](../task/load-data-erp-user-mapping-oracle-ebs.md)**  
Set up Oracle EBS and ERP User ID mapping for the integration to work. The mapping is maintained for all active users who have the procurement buyer role in ERP. These users should be used in the requisition assignment rule.
-   **[Look up primary data in Oracle EBS](look-up-primary-data-oracle-ebs.md)**  
You can run a job to look up primary data from different ERP sources into ServiceNow.
-   **[Scheduled jobs to look up primary data in Oracle EBS](scheduled-jobs-to-primary-data-oracle-ebs.md)**  
You can schedule on-demand jobs to be run at specific intervals of time to fetch primary data from different Oracle EBS ERP sources into ServiceNow.

**Parent Topic:**[Source-to-Pay integration with Oracle EBS](source-to-pay-oracle-ebs-integration.md)

