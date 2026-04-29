---
title: Configure the Workplace Case Summarization Skill
description: As an admin, you can customize the Workplace Case Summarization skill to include additional fields for the case summary.
locale: en-US
release: australia
product: Now Assist for WSD
classification: now-assist-for-wsd
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Now Assist for Workplace Service Delivery \(WSD\), Workplace Service Delivery, Employee Service Management]
---

# Configure the Workplace Case Summarization Skill

As an admin, you can customize the Workplace Case Summarization skill to include additional fields for the case summary.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Now Asisst Admin** &gt; **Skills**.

2.  On the Now Assist Skills tab, select **Employee**, then select **WSD**.

3.  Create a copy of the `Workplace Case Summarization` skill for customization.

4.  From the context menu of the newly created skill, select **Edit**.

5.  Edit any of the following sections based on your requirement.

<table id="choicetable_nxz_ynt_33c"><thead><tr><th align="left" id="d507430e102">

Section

</th><th align="left" id="d507430e105">

Description

</th></tr></thead><tbody><tr><td id="d507430e111">

**General details**

</td><td>

You can edit basic information about the skill like the name, workflow, LLM, and skill template.

</td></tr><tr><td id="d507430e120">

**Choose input**

</td><td>

You can select the fields to be included as an input for the summarization skill. For example, you can add the start and end time fields as an input to the summary.You can customize inputs for every state of the case like new, work in progress, or resolved.

For more information about customizing the input fields, see [Configure case or incident summarization in the Now Assist Admin console](https://www.servicenow.com/docs/access?context=configure-case-or-incident-summarization-in-the-now-assist-admin-console&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

</td></tr><tr><td id="d507430e137">

**Customize prompt**

</td><td>

You can add or remove sections that are included in the generated summary. You can customize the prompts for every state of the case like new, work in progress, or resolved.For more information about customizing the prompt output, see [Configure case or incident summarization in the Now Assist Admin console](https://www.servicenow.com/docs/access?context=configure-case-or-incident-summarization-in-the-now-assist-admin-console&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

</td></tr><tr><td id="d507430e152">

**Role attribution**

</td><td>

You can select the table, fields for the requester and fulfiller, and fulfiller roles for the skill.

</td></tr><tr><td id="d507430e162">

**Define availability**

</td><td>

You can customize whether the skill is available by default, or only available based on the configured conditions. For more information about the availability, see [Activate a Now Assist skill](https://www.servicenow.com/docs/access?context=configure-a-now-assist-skill&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)

</td></tr><tr><td id="d507430e174">

**Define access**

</td><td>

You can add roles to provide access to summarize a case. For example, `sn_wsd_core.workplace_manager`.

</td></tr><tr><td id="d507430e186">

**Select display**

</td><td>

You can configure where the case summarization feature is displayed. For more information about configuring the display, see [Activate a Now Assist skill](https://www.servicenow.com/docs/access?context=configure-a-now-assist-skill&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)

</td></tr></tbody>
</table>6.  After you make your changes, save the skill and exit.


