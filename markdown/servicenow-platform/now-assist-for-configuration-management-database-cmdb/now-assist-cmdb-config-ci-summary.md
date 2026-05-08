---
title: Configure the CI summarization skill
description: Review and configure the settings of the Now Assist for Configuration Management Database \(CMDB\) CI summarization skill to restrict the availability of the skill to certain users or conditions.
locale: en-US
release: australia
product: Now Assist for Configuration Management Database \(CMDB\)
classification: now-assist-for-configuration-management-database-cmdb
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Configure, Now Assist for Configuration Management Database \(CMDB\), Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Configure the CI summarization skill

Review and configure the settings of the Now Assist for Configuration Management Database \(CMDB\) CI summarization skill to restrict the availability of the skill to certain users or conditions.

## Before you begin

Role required: admin

## About this task

The CI summarization skill might scan activated plugins, activated applications, and CMDB tables. The skill uses the Now LLM Service to generate summaries.

<table id="table_r1s_bl3_1dc"><thead><tr><th>

Detail type

</th><th>

Requirements and dependencies

</th></tr></thead><tbody><tr><td>

Discovery

</td><td>

The CI summarization skill extracts details from the **Discovery source** and **Most recent discovery** CI attributes.

 If CMDB 360 is enabled, the summary can show additional discovery sources for the CI. For more information, see [CMDB 360](../concept/multisource-cmdb.md).

</td></tr><tr><td>

Alerts

</td><td>

Event Management must be activated for the CI summarization skill. For more information, see Event Management.

</td></tr><tr><td>

Security vulnerabilities

</td><td>

Security Operations must be activated for the CI summarization skill. For more information, see Security Operations.

</td></tr><tr><td>

CI ownership

</td><td>

The CI summarization skill determines the CI ownership based on the attribute that is specified in the **glide.cmdb.health.ci\_ownership\_field** system property.

 For more information, see [CMDB Health system properties](../reference/r_CMDBHealthProperties.md) and [CMDB Health](../concept/c_CMDBHealth.md).

</td></tr><tr><td>

Data on the CMDB Health Dashboard

</td><td>

The Correctness Score Calculation scheduled job improves the accuracy of the summary details on the CMDB Health Dashboard. For more information, see [Enable and configure a CMDB Health Dashboard job](t_EnableCMDBHealthDashboardJob.md).

</td></tr></tbody>
</table>By default, all skills exist in the global domain. When you use Now Assist in a domain-separated environment, users are only able to access data in their domain. For example, if a user uses the summarization skill, Now Assist only uses material that exists in the user's domain when generating that summary. Additionally, there is no co-mingling of data for domain-separated instances when using generative AI skills. The data resides only on the instance, and the shared services used for generative AI do not persist any requests \(prompts\) and responses. For more information, see Domain separation in the Now Assist Admin console. \(Note that global domain is not the same as global scope. For more information, see Exploring Next Experience pickers.\)

## Procedure

1.  Access the setting tabs for the CI summarization skill.

    1.  Navigate to **All** &gt; **Now Assist Admin**.

    2.  On the **Now Assist Features** tab, expand **Technology** and then select **CMDB**.

    3.  On the Now Assist Skills for CMDB page, review the skills and then select **View details**.

    4.  On the **Active skills** card on the Configuration Management Database \(CMDB\) page, select the context menu for the CI summarization skill and then select **Edit**.

2.  Review and configure the settings.

<table id="table_xkc_m2x_2dc"><thead><tr><th>

Tab

</th><th>

Action

</th></tr></thead><tbody><tr><td>

General details

</td><td>

Review general information on the CI summarization skill.

</td></tr><tr><td>

Choose inputs

</td><td>

**Note:** In this release of the skill, all configuration settings on this section are read-only.

Review the tables and fields that the Now LLM Service uses to gather details for the CI summary.

</td></tr><tr><td>

Define availability

</td><td>

Select **Customize skill availability** to restrict the availability of the skill to certain conditions or particular users or groups.

 Use the condition builder to specify the field conditions that must be met for the skill to be available and then select **Save and continue**.

</td></tr><tr><td>

Select display

</td><td>

1.  Toggle the Display switch to expose the CI summarization skill on CI forms. When the **Display** toggle is in the off state, the CI summarization skill isn't available even when the skill itself is activated.
2.  Specify the user roles that can use the CI summarization skill by selecting the drop-down list icon ![](../image/NowAssistDisplayDropDown.png) and then selecting the user roles in the **User roles** field.
3.  Select **Save and continue**.


</td></tr><tr><td>

Review and activate

</td><td>

Review the summary of settings for the skill \(each card displays a different category of settings\). Select **Activate** or **Done**.**Important:** Confirm that the answer is **Yes** on the card titled **Will CI summarization display in product?**. Otherwise, the CI summarization function won't be available to users even if the skill itself is activated.

</td></tr></tbody>
</table>    The **Summarize** button appears when a user with the appropriate role views a CI.

    ![Summarize button becomes available for any CI.](../../now-assist-cmdb/image/na-cmdb-summarize-button.png)


## What to do next

[Use the CI summarization skill](../concept/now-assist-cmdb-using.md).

**Parent Topic:**[Configuring Now Assist for CMDB](../concept/now-assist-cmdb-configuring.md)

