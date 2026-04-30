---
title: Scheduled jobs to fetch primary data
description: You can schedule on-demand jobs to be run at specific intervals of time to fetch primary data from different ERP sources into ServiceNow.
locale: en-US
release: xanadu
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Source-to-Pay integration framework, Source-to-Pay integration with third-party applications, Source-to-Pay Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Scheduled jobs to fetch primary data

You can schedule on-demand jobs to be run at specific intervals of time to fetch primary data from different ERP sources into ServiceNow.

Before you start the ERP integration, you must configure the integration services record for target ERP source using the sn\_fcms\_intg\_service table. The sn\_fcms\_intg\_service table is a mapping table between sub flows and target ERP source. For more information on creating a integration service record, see [Create Integration Service record](../task/create-integration-service-record.md).

Scheduled jobs are configured for entities using scripts. Example: Fetch cost center from ERP systems. For more information on configuring scheduled jobs using scripts, see [Automatically run a script of your choosing](https://www.servicenow.com/docs/access?context=t_ScheduleAScriptExecution&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US). The script invokes subflow which is associated with an entity as shown in the figure below. The subflow queries the active entities or ERP source configuration \(optional\) listed in the integration service table.

![Scheduled script execution](../image/scheduled-script.png)

The scheduled jobs are run for the following entities:

-   Cost center
-   Payment terms
-   Legal entity
-   Plant/address
-   GL account
-   Purchasing org
-   Product category/Product model \(Material group/Material number\)
-   Currency
-   Department
-   Supplier
-   FX currency rate

