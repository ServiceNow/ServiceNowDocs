---
title: Configure the Source-to-Pay integration with Oracle Financial Cloud
description: Integrate the ServiceNow instance and Oracle Financial Cloud by creating a custom OAuth application in Oracle Financial Cloud to authenticate ServiceNow requests.
locale: en-US
release: zurich
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: concept
last_updated: "2026-05-01"
reading_time_minutes: 1
breadcrumb: [Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Configure the Source-to-Pay integration with Oracle Financial Cloud

Integrate the ServiceNow instance and Oracle Financial Cloud by creating a custom OAuth application in Oracle Financial Cloud to authenticate ServiceNow requests.

## Application set up

Verify that you have performed the following:

-   Activated the Source-to-Pay integration with the Oracle Financial Cloud application from ServiceNow Store. This automatically activates the Oracle Financial Cloud Spoke.
-   Set up [Oracle EBS Spoke](https://www.servicenow.com/docs/csh?topicname=oracle-fin-cloud&version=zurich&pubname=zurich-integrate-applications).
-   Activated the Source-to-Pay integration framework from ServiceNow Store. Source-to-Pay integration with Oracle Financial Cloud uses the Source-to-Pay integration framework to pull tasks from Oracle Financial Cloud into ServiceNow. For more information on the Source-to-Pay integration framework, see [Source-to-Pay integration framework](source-to-pay-integration-framework.md).


## Primary Data Integration with Oracle Financial Cloud's Dependencies

Install the following dependencies of Primary Data integration with Oracle Financial Cloud. When you install the plugin, all the dependencies get installed automatically. All primary data are synchronized based on the configurable scheduled job Fetch Spend Primary Data.

Run the Trigger Oracle Financial Cloud Integration that pulls tasks into ServiceNow. For more information, see [Run scheduled jobs in Oracle Financial Cloud](../task/run-scheduled-jobs-oracle-fin-cloud.md).

|App name|Plugin ID|
|--------|---------|
|ERP Integration Framework|sn\_fcms\_intg|
|Source-to-pay Common Architecture|sn\_shop|
|Supplier Common Architecture|sn\_slm|
|Oracle Financial Cloud Spoke|sn\_ofc\_spoke.OracleCloudFinancials|

## Supplier Lifecycle Operations Integration Dependencies with Oracle Financial Cloud

Install the following dependencies of Supplier Lifecycle Operations integration with Oracle Financial Cloud. When you install the plugin, all the dependencies get installed automatically.

|App name|Plugin ID|
|--------|---------|
|Primary Data Integration with Oracle Financial Cloud|sn\_orcl\_data\_int|
|Source-to-Pay Integration Framework|sn\_spend\_intg|

