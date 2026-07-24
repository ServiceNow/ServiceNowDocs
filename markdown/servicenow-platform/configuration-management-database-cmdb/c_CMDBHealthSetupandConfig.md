---
title: Configuring CMDB Health
description: Data collection for CMDB Health is highly configurable to reflect data health requirements and standards in your organization. Most importantly, the CMDB Health Dashboard jobs are disabled by default and health data isn't collected until you enable those jobs.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/configuration-management-database-cmdb/c\_CMDBHealthSetupandConfig.html
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [CMDB Health, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Configuring CMDB Health

Data collection for CMDB Health is highly configurable to reflect data health requirements and standards in your organization. Most importantly, the CMDB Health Dashboard jobs are disabled by default and health data isn't collected until you enable those jobs.

To report valuable and meaningful health data, review and adjust CMDB Health-related settings.

1.  Review [CMDB Health KPIs and metrics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/r_CMDBHealthMetrics.md) to learn what CMDB Health can monitor, and what to configure to enable and support each metric. Deactivate any KPIs and metrics that you aren't interested in reporting, and set failure thresholds.
2.  For each KPI and associated metric that you want monitored, define the necessary rules and fulfill other needed requirements. For example, you might need to:
    -   [Set a CI attribute to be mandatory](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/t_SetCIFieldMandatory.md)
    -   [Set a CI field to be recommended](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/t_MakingAFieldRecommended.md)
    -   [Create a CMDB Health orphan rule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/t_CreateCMDBHealthOrphanRule.md)
    -   [Create a CMDB Health staleness rule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/t_CreateCMDBHealthStaleRule.md)
3.  Narrow the scope of CIs that are included in health calculations - see [Create health inclusion rule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/create-health-inclusion-rule.md).
4.  Examine and adjust as needed the [CMDB Health system properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/r_CMDBHealthProperties.md).
5.  Enable the Health Dashboard jobs for the KPIs that you want reported - for more information, see [Enable and configure a CMDB Health Dashboard job](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/t_EnableCMDBHealthDashboardJob.md).

