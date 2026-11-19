---
title: Configure the summarize CMDB readiness skill
description: Review and configure the settings of the summarize CMDB readiness skill to control its availability and to enable an AI-generated summary of the CMDB success advisor dashboard data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-cmdb-config-summ-rdy.html
release: yokohama
product: Now Assist for Configuration Management Database \(CMDB\)
classification: now-assist-for-configuration-management-database-cmdb
topic_type: task
last_updated: "2026-06-25"
reading_time_minutes: 4
keywords: [Summarize CMDB readiness skill, Now Assist for CMDB, CMDB success advisor dashboard, configure skill]
breadcrumb: [Configure, ServiceNow Otto for Configuration Management Database \(CMDB\), CMDB schema model, Exploring CMDB, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Configure the summarize CMDB readiness skill

Review and configure the settings of the summarize CMDB readiness skill to control its availability and to enable an AI-generated summary of the CMDB success advisor dashboard data.

## Before you begin

Role required: admin

## About this task

The summarize CMDB readiness skill reads the data findings and suggest remediation actions that the CMDB success advisor for HAM or CMDB success advisor for Data Foundations dashboard displays. The skill uses the Now LLM Service to generate the summary.

<table id="table_req_summ_readiness"><thead><tr><th>

Detail type

</th><th>

Requirements and dependencies

</th></tr></thead><tbody><tr><td>

CMDB success advisor

</td><td>

The CMDB success advisor application must be installed and active. The skill draws its inputs from the findings and the recommended remediation actions that the dashboard surfaces.

</td></tr><tr><td>

HAM

</td><td>

Set up the CMDB success advisor for Hardware Asset Management \(HAM\). See [CMDB success advisor for HAM setup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-asset-management/cmdb-sa-ham-config-settings.md).

</td></tr><tr><td>

Data Foundations

</td><td>

Set up the CMDB success advisor for Data Foundations. See [CMDB success advisor for Data Foundations setup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/servicenow-platform/configuration-management-database-cmdb/cmdb-sa-df-config-settings.md).

</td></tr><tr><td>

Now Assist for CMDB

</td><td>

The ServiceNow Otto for Configuration Management Database \(CMDB\) application provides the skill. Activate the application from the **Now Assist Admin** console before you configure the skill.

</td></tr></tbody>
</table>By default, all skills exist in the global domain. When you use Now Assist in a domain-separated environment, users are only able to access data in their domain. For example, if a user uses the summarization skill, Now Assist only uses material that exists in the user's domain when generating that summary. Additionally, there is no co-mingling of data for domain-separated instances when using generative AI skills. The data resides only on the instance, and the shared services used for generative AI do not persist any requests \(prompts\) and responses. For more information, see [Domain separation in the AI Admin Hub console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/domain-separation-in-the-now-assist-admin-console.md). \(Note that global domain is not the same as global scope. For more information, see [Exploring Next Experience pickers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-user-interface/next-experience-pickers.md).\)

## Procedure

1.  Access the setting tabs for the summarize CMDB readiness skill.

    1.  Navigate to **All** &gt; **Now Assist Admin**.

    2.  On the **Now Assist Features** tab, expand **Technology** and then select **CMDB**.

    3.  On the Now Assist Skills for CMDB page, review the skills and then select **View details**.

    4.  On the **Active skills** card on the Configuration Management Database \(CMDB\) page, select the context menu for the summarize CMDB readiness skill and then select **Edit**.

2.  Review and configure the settings.

<table id="table_tabs_summ_readiness"><thead><tr><th>

Tab

</th><th>

Action

</th></tr></thead><tbody><tr><td>

General details

</td><td>

Review general information about the summarize CMDB readiness skill.

</td></tr><tr><td>

Choose inputs

</td><td>

**Note:** In this release of the skill, all configuration settings on this section are read-only.

Review the inputs that the Now LLM Service uses to generate the summary, such as the applied filters and the recommended remediation actions on the HAM and Data Foundations advisor dashboards.

</td></tr><tr><td>

Define availability

</td><td>

Select **Customize skill availability** to restrict the availability of the skill to certain conditions or particular users or groups.

 Use the condition builder to specify the field conditions that must be met for the skill to be available and then select **Save and continue**.

</td></tr><tr><td>

Select display

</td><td>

1.  Toggle the **Display** switch to expose the summarize CMDB readiness skill on the CMDB success advisor dashboard. When the **Display** toggle is in the off state, the skill isn't available on the dashboard even when the skill itself is activated.
2.  Specify the user roles that can use the skill by selecting the drop-down list icon \[Omitted image "NowAssistDisplayDropDown.png"\] and then selecting the user roles in the **User roles** field.
3.  Select **Save and continue**.


</td></tr><tr><td>

Review and activate

</td><td>

Review the summary of settings for the skill \(each card displays a different category of settings\). Select **Activate** or **Done**.**Important:** Confirm that the answer is **Yes** on the card that indicates whether the skill displays in the product. Otherwise, the Summarize CMDB readiness button doesn't appear on the dashboard even when the skill itself is activated.

</td></tr></tbody>
</table>    The Dashboard tabs of the CMDB success advisor for HAM and CMDB success advisor for Data Foundations shows a summary of the cards includes in the dashboard and remediation action plan for them.


## Result

To deactivate the skill later, return to the **Now Assist Admin** console and deactivate the skill from the **Active skills** card.

**Note:** To reactivate a deactivated skill, follow the same skill configuration procedure. Then, in the Skill Config \[sn\_nowassist\_skill\_config\_status\] table, open the skill's record and select the **In Product Active** check box.

## What to do next

[Summarize CMDB readiness with the Now Assist skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-cmdb-skill-summ-rdy.md).

**Parent Topic:**[Configuring Now Assist for CMDB](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/servicenow-platform/now-assist-for-configuration-management-database-cmdb/now-assist-cmdb-configuring.md)

