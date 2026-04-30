---
title: Scheduled jobs to look up primary data in Oracle EBS
description: You can schedule on-demand jobs to be run at specific intervals of time to fetch primary data from different Oracle EBS ERP sources into ServiceNow.
locale: en-US
release: xanadu
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: concept
last_updated: "2025-03-12"
reading_time_minutes: 2
breadcrumb: [Configuring the Source-to-Pay integration with Oracle EBS, Source-to-Pay integration with Oracle EBS, Source-to-Pay integration with third-party applications, Source-to-Pay Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Scheduled jobs to look up primary data in Oracle EBS

You can schedule on-demand jobs to be run at specific intervals of time to fetch primary data from different Oracle EBS ERP sources into ServiceNow.

Before you start the Oracle EBS ERP integration, you must configure the integration services record for target ERP source using the `sn_fcms_intg_service` table. The `sn_fcms_intg_service` table is a mapping table between sub flows and target ERP source. For more information on creating a integration service record, see [Create Integration Service record](../../accounts-payable-operations/task/create-integration-service-record.md).

Scheduled jobs are configured for entities using scripts. Example: Fetch cost center from ERP systems. For more information on configuring scheduled jobs using scripts, see [Automatically run a script of your choosing](https://www.servicenow.com/docs/access?context=t_ScheduleAScriptExecution&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US). The script invokes subflow which is associated with an entity as shown in the figure below. The subflow queries the active entities or ERP source configuration \(optional\) listed in the integration service table.

![Scheduled script execution](../../accounts-payable-operations/image/scheduled-script.png)

-   **[Run scheduled jobs in Oracle EBS](../task/run-scheduled-jobs-oracle-ebs.md)**  
Run adhoc scheduled jobs to look up entity primary data from the target Oracle EBS ERP source.

**Parent Topic:**[Configuring the Source-to-Pay integration with Oracle EBS](configuring-source-to-pay-oracle-ebs-integration.md)

**Related topics**  


[ERP Source Configuration for Oracle EBS](erp-source-configuration-oracle.md)

[Define ERP source configuration for Oracle EBS](../task/define-erp-source-oracle.md)

[Configure service maps for Oracle EBS](../task/configure-service-maps-oracle-ebs.md)

[Load data to ERP user mapping table for Oracle EBS](../task/load-data-erp-user-mapping-oracle-ebs.md)

[Look up primary data in Oracle EBS](look-up-primary-data-oracle-ebs.md)

