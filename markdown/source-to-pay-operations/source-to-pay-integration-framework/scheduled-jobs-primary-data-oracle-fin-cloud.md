---
title: Scheduled jobs to look up primary data in Oracle Financial Cloud
description: You can schedule on-demand jobs to be run at specific intervals of time to fetch primary data from different Oracle Financial Cloud ERP sources into ServiceNow.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/source-to-pay-integration-framework/scheduled-jobs-primary-data-oracle-fin-cloud.html
release: australia
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Source-to-Pay integration with Oracle Financial Cloud, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Scheduled jobs to look up primary data in Oracle Financial Cloud

You can schedule on-demand jobs to be run at specific intervals of time to fetch primary data from different Oracle Financial Cloud ERP sources into ServiceNow.

Before you start the Oracle Financial Cloud ERP integration, you must configure the integration services record for target ERP source using the `sn_fcms_intg_service` table. The `sn_fcms_intg_service` table is a mapping table between sub flows and target ERP source. For more information on creating an integration service record, see [Create Integration Service record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/source-to-pay-integration-framework/create-integration-service-record.md).

Scheduled jobs are configured for entities using scripts. Example: Fetch cost center from ERP systems. For more information on configuring scheduled jobs using scripts, see . The script invokes a subflow, which is associated with an entity as shown in the following figure. The subflow queries the active entities or ERP source configuration \(optional\) listed in the integration service table.

\[Omitted image "oracle-fin-scheduled-jobs-script.png"\] Alt text:

