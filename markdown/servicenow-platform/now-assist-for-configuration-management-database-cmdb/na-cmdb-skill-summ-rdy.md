---
title: Summarize CMDB readiness with the Now Assist skill
description: View an AI-generated summary of the CMDB success advisor for HAM dashboard data. The summary highlights the key findings on CMDB data accuracy, completeness, and health, and recommends remediation actions to address the findings.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-cmdb-skill-summ-rdy.html
release: zurich
product: Now Assist for Configuration Management Database \(CMDB\)
classification: now-assist-for-configuration-management-database-cmdb
topic_type: task
last_updated: "2026-06-25"
reading_time_minutes: 2
keywords: [Summarize CMDB readiness skill, Now Assist for CMDB, CMDB success advisor dashboard, summarize dashboard data, remediation actions]
breadcrumb: [Use generative AI skills, Now Assist for Configuration Management Database \(CMDB\), Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Summarize CMDB readiness with the Now Assist skill

View an AI-generated summary of the CMDB success advisor for HAM dashboard data. The summary highlights the key findings on CMDB data accuracy, completeness, and health, and recommends remediation actions to address the findings.

## Before you begin

-   Set up the CMDB success advisor for HAM advisor scope so that the advisor dashboard has data to summarize. See [Set up CMDB success advisor for HAM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-asset-management/cmdb-sa-ham-config-settings.md).
-   Configure and activate the summarize CMDB readiness skill. See [Configure the summarize CMDB readiness skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-cmdb-config-summ-rdy.md).

The sn\_cmdb\_user role grants access to the HAM advisor dashboard but doesn't grant access to business rules or data manager policies. To follow remediation links from the summary into business rules, data manager policies, and similar records, the sn\_cmdb\_admin role is required.

Role required: sn\_cmdb\_user or sn\_cmdb\_admin

## About this task

The AI-generated summary of the CMDB success advisor for HAM dashboard data highlights data accuracy, completeness, and health findings, and the recommended remediation actions to address them.

## Procedure

1.  On the CMDB success advisor landing page, select **View insights** within the HAM card.

    See [Viewing the CMDB success advisor landing page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/configuration-management-database-cmdb/cmdb-sa-landing-page.md).

2.  Select the **Dashboard** tab.

3.  Apply or change the dashboard filters on the tab.

    The summary reflects the data and the recommended remediation actions that are shown on the dashboard when you generate it.

    **Note:** Each time you change a filter, the AI-generated summary indicates that the inputs have changed and enables the **Refresh** link to regenerate the summary against the latest selection.

4.  Review the summary and the recommended remediation actions.

    The summary lists the key findings on CMDB data accuracy, completeness, and health, along with the recommended remediation actions. Follow the links in the summary to open the records that you can act on.

    **Note:** Each remediation link has a minimum role requirement. Some links navigate to business rules, data manager policies, or other records that require the sn\_cmdb\_admin role. The **Minimum user role** column in the Remediation Action \[sn\_cmdb\_gen\_ai\_advisor\_remediation\_action\] table shows the role required for each remediation action.

5.  Provide feedback, copy the response text to the clipboard, or refresh the response.

<table id="choicetable_md1_nyf_xyb"><thead><tr><th align="left" id="d214004e249">

Option

</th><th align="left" id="d214004e252">

Procedure

</th></tr></thead><tbody><tr><td id="d214004e258">

**Provide feedback for the summary**

</td><td>

If you think that the response was helpful, select thumbs-up \[Omitted image "icon-thumbs-up.png"\]. If you think that it wasn’t helpful, select thumbs-down \[Omitted image "icon-thumbs-down.png"\].This feedback improves the agentic AI model and can help to improve the future versions of this skill. The system gathers the feedback on each generated response and stores it in the agentic AI logs \(sys\_generative\_ai\_log\_list.do\).

</td></tr><tr><td id="d214004e273">

**Copy the summary**

</td><td>

Select the copy to clipboard icon \[Omitted image "icon-clipboard.png"\] to use the response information for another purpose, such as pasting into an email.

</td></tr><tr><td id="d214004e284">

**Refresh the summary**

</td><td>

If you think that data might have changed after you viewed the response, select the redo icon \[Omitted image "icon-redo.png"\] to refresh the response information.

</td></tr></tbody>
</table>
**Related topics**  


[Configure the summarize CMDB readiness skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-cmdb-config-summ-rdy.md)

