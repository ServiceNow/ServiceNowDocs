---
title: Scheduled jobs to look up primary data in Oracle EBS
description: You can schedule on-demand jobs to be run at specific intervals of time to fetch primary data from different Oracle EBS ERP sources into ServiceNow.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/source-to-pay-integration-framework/scheduled-jobs-to-primary-data-oracle-ebs.html
release: australia
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, Source-to-Pay integration with Oracle EBS, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Scheduled jobs to look up primary data in Oracle EBS

You can schedule on-demand jobs to be run at specific intervals of time to fetch primary data from different Oracle EBS ERP sources into ServiceNow.

Before you start the Oracle EBS ERP integration, you must configure the integration services record for target ERP source using the `sn_fcms_intg_service` table. The `sn_fcms_intg_service` table is a mapping table between sub flows and target ERP source. For more information on creating an integration service record, see [Create Integration Service record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/source-to-pay-integration-framework/create-integration-service-record.md).

Scheduled jobs are configured for entities using scripts. Example: Fetch cost center from ERP systems. For more information on configuring scheduled jobs using scripts, see [Automatically run a script of your choosing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_ScheduleAScriptExecution.md). The script invokes a subflow, which is associated with an entity as shown in the following figure. The subflow queries the active entities or ERP source configuration \(optional\) listed in the integration service table.

\[Omitted image "scheduled-script.png"\] Alt text: Scheduled script execution

-   **[Run scheduled jobs in Oracle EBS](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/source-to-pay-integration-framework/run-scheduled-jobs-oracle-ebs.md)**  
Run adhoc scheduled jobs to look up entity primary data from the target Oracle EBS ERP source.

**Parent Topic:**[Configure the Source-to-Pay integration with Oracle EBS](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/source-to-pay-integration-framework/configuring-source-to-pay-oracle-ebs-integration.md)

**Related topics**  


[ERP source configuration for Oracle EBS]()

[Define ERP source configuration for Oracle EBS]()

[Configure integration services for Oracle EBS]()

[Load data to ERP user-mapping table for Oracle EBS]()

[Look up primary data in Oracle EBS]()

