---
title: Summarize CMDB readiness with the Now Assist skill
description: View an AI-generated summary of the CMDB success advisor for HAM or CMDB success advisor for Data Foundations dashboard data. The summary highlights the key findings on CMDB data accuracy, completeness, and health, and recommends remediation actions to address the findings.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-cmdb-skill-summ-rdy.html
release: yokohama
product: Now Assist for Configuration Management Database \(CMDB\)
classification: now-assist-for-configuration-management-database-cmdb
topic_type: task
last_updated: "2026-06-25"
reading_time_minutes: 3
keywords: [Summarize CMDB readiness skill, Now Assist for CMDB, CMDB success advisor dashboard, summarize dashboard data, remediation actions]
breadcrumb: [Use generative AI skills, ServiceNow Otto for Configuration Management Database \(CMDB\), CMDB schema model, Exploring CMDB, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Summarize CMDB readiness with the Now Assist skill

View an AI-generated summary of the CMDB success advisor for HAM or CMDB success advisor for Data Foundations dashboard data. The summary highlights the key findings on CMDB data accuracy, completeness, and health, and recommends remediation actions to address the findings.

## Before you begin

-   Set up the CMDB success advisor for HAM or Data Foundations advisor scope so that the advisor dashboard has data to summarize. See [CMDB success advisor for HAM setup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-asset-management/cmdb-sa-ham-config-settings.md) or [CMDB success advisor for Data Foundations setup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/servicenow-platform/configuration-management-database-cmdb/cmdb-sa-df-config-settings.md).
-   Configure and activate the summarize CMDB readiness skill. See [Configure the summarize CMDB readiness skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-cmdb-config-summ-rdy.md).

The sn\_cmdb\_user role grants access to the HAM or Data Foundations advisor dashboard but doesn't grant access to business rules or data manager policies. To follow remediation links from the summary into business rules, data manager policies, and similar records, the sn\_cmdb\_admin role is required.

Role required: sn\_cmdb\_user or sn\_cmdb\_admin

## About this task

The AI-generated summary of the CMDB success advisor for HAM or Data Foundations dashboard data highlights data accuracy, completeness, and health findings, and the recommended remediation actions to address them.

Issues are grouped into categories and ranked within and across categories primarily by the percentage of CIs or CI classes each issue affects. Severity doesn't determine the ranking. Duplicate CIs and stale CIs \(not updated in the last 90 days\) are evaluated first because they can inflate the counts behind other issues. For the category list for each product, see [Monitoring CMDB data quality using dashboard metrics in CMDB success advisor for HAM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-asset-management/cmdb-sa-ham-dashboard.md) or [Monitoring CMDB data quality using dashboard metrics in CMDB success advisor for Data Foundations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/servicenow-platform/configuration-management-database-cmdb/cmdb-sa-df-dashboard.md).

## Procedure

1.  On the CMDB success advisor landing page, select **View insights** within the HAM or Data Foundations card.

    See [Viewing the CMDB success advisor landing page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/servicenow-platform/configuration-management-database-cmdb/cmdb-sa-landing-page.md).

2.  Select the **Dashboard** tab.

3.  Apply or change the dashboard filters on the tab.

    The summary reflects the data and the recommended remediation actions that are shown on the dashboard when you generate it.

    **Note:** Each time you change a filter, the AI-generated summary indicates that the inputs have changed and enables the **Refresh** link to regenerate the summary against the latest selection.

4.  Review the summary and the recommended remediation actions.

    The summary lists the key findings on CMDB data accuracy, completeness, and health, along with the recommended remediation actions. Follow the links in the summary to open the records that you can act on.

    **Note:** Each remediation link has a minimum role requirement. Some links navigate to business rules, data manager policies, or other records that require the sn\_cmdb\_admin role. The **Minimum user role** column in the Remediation Action \[sn\_cmdb\_gen\_ai\_advisor\_remediation\_action\] table shows the role required for each remediation action.

5.  
**Related topics**  


[Configure the summarize CMDB readiness skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-cmdb-config-summ-rdy.md)

