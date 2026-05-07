---
title: Configure Source-to-Pay integration with Coupa
description: Integrate your ServiceNow instance and Coupa by creating a custom OAuth application in Coupa to authenticate ServiceNow requests.
locale: en-US
release: australia
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Source-to-Pay integration with Coupa, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Configure Source-to-Pay integration with Coupa

Integrate your ServiceNow instance and Coupa by creating a custom OAuth application in Coupa to authenticate ServiceNow requests.

## Application set up

-   Activate the Source-to-Pay integration with Coupa application from the ServiceNow Store to activate the Coupa Spoke automatically.
-   Set up [Coupa Spoke](https://www.servicenow.com/docs/csh?topicname=setup-coupa-spoke-v4&version=yokohama&pubname=yokohama-integrate-applications).
-   Activate the Source-to-Pay integration framework from ServiceNow Store. Source-to-Pay integration with Coupa uses the Source-to-Pay integration framework to pull tasks from Coupa into your ServiceNow instance.For more information on Source-to-Pay integration framework, see [Source-to-Pay integration framework](../../source-to-pay-operations/concept/source-to-pay-integration-framework.md).


## Primary Data Integration Dependencies with Coupa

Install the following dependencies of Primary Data integration with Coupa. When you install the plugin, all the dependencies get installed automatically. All primary data are synchronized based on the configurable scheduled job Fetch Spend Primary Data.

Run the Trigger Coupa Integration that pulls tasks into your ServiceNow instance. For more information, see [Use schedule flows in Oracle EBS](using-schedule-flows-oracle-ebs.md).

|App name|Plugin ID|
|--------|---------|
|ERP Integration Framework|sn\_fcms\_intg|
|Coupa Spoke|sn\_coupa\_spoke|

## Supplier lifecycle Operations Integration Dependencies with Coupa

Install the following dependencies of Supplier Lifecycle Operations integration with Coupa. When you install the plugin, all the dependencies get installed automatically.

|App name|Plugin ID|
|--------|---------|
|ERP Integration Framework|sn\_fcms\_intg|
|Source-to-Pay Integration Framework|sn\_spend\_intg|
|Source-to-pay Common Architecture|sn\_shop|
|Supplier Common Architecture|sn\_slm|
|Coupa Spoke|sn\_coupa\_spoke|

## Sourcing and Procurement Operations Integration Dependencies with Coupa

Install the following dependencies of Sourcing and Procurement Operations integration with Coupa. When you install the plugin, all the dependencies get installed automatically.

|App name|Plugin ID|
|--------|---------|
|ERP Integration Framework|sn\_fcms\_intg|
|Source-to-pay Common Architecture|sn\_shop|
|Sourcing and Purchasing Automation|sn\_pr|
|Source-to-Pay Integration Framework|sn\_spend\_intg|
|Coupa Spoke|sn\_coupa\_spoke|

## Accounts Payable Operations Integration Dependencies with Coupa

Install the following dependencies of Accounts Payable Operations integration with Coupa. When you install the plugin, all the dependencies get installed automatically.

|App name|Plugin ID|
|--------|---------|
|ERP Integration Framework|sn\_fcms\_intg|
|Coupa Spoke|sn\_coupa\_spoke|
|Accounts Payable Invoice Processing|sn\_ap\_apm|
|Source-to-Pay Integration Framework|sn\_spend\_intg|

## Schedule flow activation

Activate and run the Trigger Coupa Integration that pulls tasks into your ServiceNow instance. For more information, see [Activate the schedule flows](../task/activate-schedule-flows-coupa.md).

-   **[ERP Source Configuration for Coupa](erp-source-configuration-coupa.md)**  
Configure your Source-to-Pay \(S2P\) instance to support inbound and outbound integration with your ERP system. This integration configuration enables you to post purchase order, receipt, invoice, and download primary data from the ERP automatically.
-   **[Define an ERP source configuration for Coupa](../task/define-erp-source-coupa.md)**  
Define an ERP source configuration that specifies the Coupa ERP source to which the ERP system connects. Map the integration payload with the Coupa tables.
-   **[Configure integration services for Coupa](../task/configure-integration-services-coupa.md)**  
Configure integration services for Coupa. Provide the connection end point and the Coupa ERP credentials that you set up for your authentication profile. Also, create a separate web service record for each service request that you want to customize.
-   **[Activate the schedule flows](../task/activate-schedule-flows-coupa.md)**  
Activate the schedule flow that interacts with Coupa to pull information into your ServiceNow instance. You can pull information on primary data, supplier management, sourcing, invoice, and so on.
-   **[Looking up primary data in Coupa](look-up-primary-data-coupa.md)**  
You can run a job to look up primary data from different ERP sources into ServiceNow

**Parent Topic:**[Source-to-Pay integration with Coupa](source-to-pay-coupa-integration.md)

