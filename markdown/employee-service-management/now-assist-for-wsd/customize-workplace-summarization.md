---
title: Configure the workplace case summarization skill
description: As an admin, customize the workplace case summarization skill to include additional fields for the case summary.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/employee-service-management/now-assist-for-wsd/customize-workplace-summarization.html
release: zurich
product: Now Assist for WSD
classification: now-assist-for-wsd
topic_type: task
last_updated: "2026-02-19"
reading_time_minutes: 1
breadcrumb: [Configure, Now Assist for Workplace Service Delivery \(WSD\), Workplace Service Delivery, Employee Service Management]
---

# Configure the workplace case summarization skill

As an admin, customize the workplace case summarization skill to include additional fields for the case summary.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Now Asisst Admin** &gt; **Skills**.

2.  On the **Now Assist Skills** tab, select **Employee**, then select **WSD**.

3.  Create a copy of the `Workplace Case Summarization` skill for customization.

4.  From the context menu of the newly created skill, select **Edit**.

5.  Edit any of the following sections based on your requirement.

<table id="choicetable_nxz_ynt_33c"><thead><tr><th align="left" id="d234094e105">

Section

</th><th align="left" id="d234094e108">

Description

</th></tr></thead><tbody><tr><td id="d234094e114">

**General details**

</td><td>

Edit basic information about the skill like the name, workflow, large language model \(LLM\), and skill template.

</td></tr><tr><td id="d234094e123">

**Choose input**

</td><td>

Select the fields to be included as an input for the summarization skill. For example, you can add the start and end time fields as an input to the summary.You can customize inputs for every state of the case like new, work in progress, or resolved.

For more information about customizing the input fields, see [Configure case or incident summarization in the Now Assist Admin console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/enable-ai-experiences/configure-case-or-incident-summarization-in-the-now-assist-admin-console.md).

</td></tr><tr><td id="d234094e140">

**Customize prompt**

</td><td>

Add or remove sections that are included in the generated summary. You can customize the prompts for every state of the case like New, Work in progress, or Resolved.For more information about customizing the prompt output, see [Configure case or incident summarization in the Now Assist Admin console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/enable-ai-experiences/configure-case-or-incident-summarization-in-the-now-assist-admin-console.md).

</td></tr><tr><td id="d234094e155">

**Role attribution**

</td><td>

Select the table, fields for the requester and fulfiller, and fulfiller roles for the skill.

</td></tr><tr><td id="d234094e165">

**Define availability**

</td><td>

Customize whether the skill is available by default, or only available based on the configured conditions. For more information about the availability, see [Activate a Now Assist skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/enable-ai-experiences/configure-a-now-assist-skill.md).

</td></tr><tr><td id="d234094e178">

**Define access**

</td><td>

Add roles to provide the access required to summarize a case. For example, `sn_wsd_core.workplace_manager`.

</td></tr><tr><td id="d234094e190">

**Select display**

</td><td>

Configure where the case summarization feature is displayed. For more information about configuring the display, see [Activate a Now Assist skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/enable-ai-experiences/configure-a-now-assist-skill.md).

</td></tr></tbody>
</table>6.  After you make your changes, select **Exit**.


