---
title: Scheduled jobs to fetch primary data
description: Schedule on-demand jobs to fetch primary data from ERP sources into Accounts Payable Operations at defined intervals.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/source-to-pay-integration-framework/run-scheduled-job-to-fetch-primary-data.html
release: australia
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [APO, Accounts Payable Operations, ERP integration, invoice automation, AP automation]
breadcrumb: [Source-to-Pay integration framework, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Scheduled jobs to fetch primary data

Schedule on-demand jobs to fetch primary data from ERP sources into Accounts Payable Operations at defined intervals.

Before you start the ERP integration, you must configure the integration services record for target ERP source using the sn\_fcms\_intg\_service table. The sn\_fcms\_intg\_service table is a mapping table between sub flows and target ERP source. For more information on creating a integration service record, see [Create Integration Service record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/source-to-pay-integration-framework/create-integration-service-record.md).

Scheduled jobs are configured for entities using scripts. Example: Fetch cost center from ERP systems. For more information on configuring scheduled jobs using scripts, see . The script invokes subflow which is associated with an entity as shown in the figure below. The subflow queries the active entities or ERP source configuration \(optional\) listed in the integration service table.

\[Omitted image "scheduled-script.png"\] Alt text: Scheduled script execution

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

