---
title: Summarize CMDB readiness with the ServiceNow Otto skill
description: View an AI-generated summary of the CMDB success advisor for HAM or CMDB success advisor for Data Foundations dashboard data. The summary highlights the key findings on CMDB data accuracy, completeness, and health, and recommends remediation actions to address the findings.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-cmdb-skill-summ-rdy.html
release: australia
product: Now Assist for Configuration Management Database \(CMDB\)
classification: now-assist-for-configuration-management-database-cmdb
topic_type: task
last_updated: "2026-06-25"
reading_time_minutes: 4
keywords: [Summarize CMDB readiness skill, ServiceNow Otto for CMDB, CMDB success advisor dashboard, summarize dashboard data, remediation actions]
breadcrumb: [Use generative AI skills, ServiceNow Otto for Configuration Management Database \(CMDB\), Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Summarize CMDB readiness with the ServiceNow Otto skill

View an AI-generated summary of the CMDB success advisor for HAM or CMDB success advisor for Data Foundations dashboard data. The summary highlights the key findings on CMDB data accuracy, completeness, and health, and recommends remediation actions to address the findings.

## Before you begin

-   Set up the CMDB success advisor for HAM or Data Foundations advisor scope so that the advisor dashboard has data to summarize. See [CMDB success advisor for HAM setup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/cmdb-sa-ham-config-settings.md) or [CMDB success advisor for Data Foundations setup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/cmdb-sa-df-config-settings.md).
-   Configure and activate the summarize CMDB readiness skill. See [Configure the summarize CMDB readiness skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-cmdb-config-summ-rdy.md).

The sn\_cmdb\_user role grants access to the HAM or Data Foundations advisor dashboard but doesn't grant access to business rules or data manager policies. To follow remediation links from the summary into business rules, data manager policies, and similar records, the sn\_cmdb\_admin role is required.

Role required: sn\_cmdb\_user or sn\_cmdb\_admin

## About this task

The AI-generated summary of the CMDB success advisor for HAM or Data Foundations dashboard data highlights data accuracy, completeness, and health findings, and the recommended remediation actions to address them.

Issues are grouped into categories and ranked within and across categories primarily by the percentage of CIs or CI classes each issue affects. Severity doesn't determine the ranking. Duplicate CIs and stale CIs \(not updated in the last 90 days\) are evaluated first because they can inflate the counts behind other issues. For the category list for each product, see [Monitoring CMDB data quality using dashboard metrics in CMDB success advisor for HAM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/cmdb-sa-ham-dashboard.md) or [Monitoring CMDB data quality using dashboard metrics in CMDB success advisor for Data Foundations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/cmdb-sa-df-dashboard.md).

The summary also applies the following rules when ranking and presenting issues:

-   A setting or business rule can be the underlying cause of an issue already shown on the dashboard. When this happens, the two are merged into a single recommendation that addresses the underlying cause instead of listing them separately.
-   The reasoning text includes the percentage of CIs or CI classes affected by each issue. It doesn't show the category order or the percentage gaps used to rank issues.
-   A percentage gap of more than 15 points between issues in the same category can change their default order. A percentage gap of more than 40 points between issues in different categories can also change their default order.
-   Each ranked issue maps to one primary remediation action, such as a skill, an agentic workflow, or a navigation link, selected based on your role. If no action is available that you're eligible to run, the summary doesn't offer a remediation action for that issue.

## Procedure

1.  On the CMDB success advisor landing page, select **View insights** within the HAM or Data Foundations card.

    See [Viewing the CMDB success advisor landing page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/cmdb-sa-landing-page.md).

2.  Select the **Dashboard** tab.

3.  Apply or change the dashboard filters on the tab.

    The summary reflects the data and the recommended remediation actions that are shown on the dashboard when you generate it.

    **Note:** Each time you change a filter, the AI-generated summary indicates that the inputs have changed and enables the **Refresh** link to regenerate the summary against the latest selection.

4.  Review the summary and the recommended remediation actions.

    The summary lists the key findings on CMDB data accuracy, completeness, and health, along with the recommended remediation actions. Follow the links in the summary to open the records that you can act on.

    **Note:** Each remediation link has a minimum role requirement. Some links navigate to business rules, data manager policies, or other records that require the sn\_cmdb\_admin role. The **Minimum user role** column in the Remediation Action \[sn\_cmdb\_gen\_ai\_advisor\_remediation\_action\] table shows the role required for each remediation action.

5.  Provide feedback, copy the response text to the clipboard, or refresh the response.

<table id="choicetable_md1_nyf_xyb"><thead><tr><th align="left" id="d213871e327">

Option

</th><th align="left" id="d213871e330">

Procedure

</th></tr></thead><tbody><tr><td id="d213871e336">

**Provide feedback for the summary**

</td><td>

If you think that the response was helpful, select thumbs-up \[Omitted image "icon-thumbs-up.png"\]. If you think that it wasn’t helpful, select thumbs-down \[Omitted image "icon-thumbs-down.png"\].This feedback improves the agentic AI model and can help to improve the future versions of this skill. The system gathers the feedback on each generated response and stores it in the agentic AI logs \(sys\_generative\_ai\_log\_list.do\).

</td></tr><tr><td id="d213871e351">

**Copy the summary**

</td><td>

Select the copy to clipboard icon \[Omitted image "icon-clipboard.png"\] to use the response information for another purpose, such as pasting into an email.

</td></tr><tr><td id="d213871e362">

**Refresh the summary**

</td><td>

If you think that data might have changed after you viewed the response, select the redo icon \[Omitted image "icon-redo.png"\] to refresh the response information.

</td></tr></tbody>
</table>
**Related topics**  


[Configure the summarize CMDB readiness skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-cmdb-config-summ-rdy.md)

