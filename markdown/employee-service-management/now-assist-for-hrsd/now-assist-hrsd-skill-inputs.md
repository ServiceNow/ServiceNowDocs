---
title: Skill inputs and triggers for Now Assist for HRSD
description: Get a quick overview of the skill inputs and triggers for Now Assist for HR Service Delivery \(HRSD\). By configuring the inputs or triggers for a skill, you can determine how and when a skill is used.
locale: en-US
release: zurich
product: Now Assist for HRSD
classification: now-assist-for-hrsd
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Configure, Now Assist for HR Service Delivery \(HRSD\), HR Service Delivery, Employee Service Management]
---

# Skill inputs and triggers for Now Assist for HRSD

Get a quick overview of the skill inputs and triggers for Now Assist for HR Service Delivery \(HRSD\). By configuring the inputs or triggers for a skill, you can determine how and when a skill is used.

Depending on the selected skill, you can configure the inputs or triggers. These settings determine how and when a skill is used. An input identifies the data that is used for a skill, such as the table and fields that are used to generate a case summary. A trigger initiates an action, such as when the system generates a chat summary.

## Chat summarization skill

For the chat summarization skill, select the triggers that determine when a chat summary is generated and how a chat summary is displayed.

The following table lists the triggers that you can configure for the chat summarization skill of the Chat Assist feature.

|Trigger|Description|
|-------|-----------|
|Virtual Agent to Live Agent handoff|Chat summary that is generated when the chat handoff is done from Virtual Agent to a live agent.|
|Quick action|Chat summary that is generated when the live agent performs the `/summarize` quick action.|
|Short description|**Short description** field that is updated for the interaction when the live agent ends the chat.|
|Chat wrap-up|Chat summary that is generated when the live agent ends the chat. The **Chat Summary** field is updated for the interaction.|
|Bulleted list|Chat summary as an unordered list.|
|Task creation|**Short description** and **Description** fields that are auto-populated when a task is created.|

## Case summarization skill

The case summarization skill includes the inputs that identify the table and fields that are used when a case summary is generated.

**Note:** These fields are read-only.

The following table lists the inputs for the case summarization skill.

<table id="table_case_summary_inputs"><thead><tr><th>

Input

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Input table

</td><td>

HR Case \[sn\_hr\_core\_case\]

</td></tr><tr><td>

Input fields

</td><td>

-   Description
-   Priority
-   Short description
-   State
-   Additional comments
-   Work notes

</td></tr></tbody>
</table>**Note:** Case summarization is not available for **Cancelled** or **Suspended** cases.

## Resolution notes generation skill

The resolution notes generation skill includes the inputs that identify the table and fields that are used when the resolution notes are generated for a case.

**Note:** These fields are read-only.

The following table lists the inputs for the resolution notes generation skill.

<table id="table_resolution_notes_inputs"><thead><tr><th>

Input

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Input table

</td><td>

HR Case \[sn\_hr\_core\_case\]

</td></tr><tr><td>

Input fields

</td><td>

-   Short description
-   Description
-   State
-   Additional comments
-   Work notes

</td></tr></tbody>
</table>## Case sentiment analysis skill

The case sentiment analysis skill includes the inputs and outputs that identify the table and fields that are used when a case sentiment is generated.

<table id="table_rbs_gbj_l2c"><thead><tr><th>

Input

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Input table

</td><td>

Case \[case\]

</td></tr><tr><td>

Input fields

</td><td>

-   Short description
-   Description
-   Priority
-   State
-   Creation date
-   Activities

</td></tr></tbody>
</table><table id="table_lm1_qcj_l2c"><thead><tr><th>

Output

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Sentiment values

</td><td>

-   Positive
-   Neutral
-   Negative

</td></tr><tr><td>

Sentiment trend

</td><td>

-   Improving
-   Declining
-   Stable

</td></tr><tr><td>

Sentiment reasoning

</td><td>

Reasons for providing the sentiment value.

</td></tr></tbody>
</table>|Scheduled job name|Default value|Description|
|------------------|-------------|-----------|
|Sentiment analysis scheduled job \(case\)|True|Refreshes sentiments on the Trigger frequency screen for the Sentiment analysis skill.|
|Update sentiment historical records|False|When active, calculates sentiment and sentiment trends for historical records.|

## Knowledge article generation skill

The knowledge article generation skill includes the inputs that identify the table and fields that are used when a knowledge article is generated for a case.

**Note:** These fields are read-only.

The following table lists the inputs for the knowledge article generation skill.

<table id="table_s3v_ywp_hbc"><thead><tr><th>

Input

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Input table

</td><td>

HR Case \[sn\_hr\_core\_case\]

</td></tr><tr><td>

Input fields

</td><td>

-   Short description
-   Description
-   Close notes \(for HR cases\)
-   Additional comments
-   Work notes

</td></tr></tbody>
</table>## ER case summarization skill

The ER case summarization skill includes the inputs that identify the table and fields that are used to generate case summary.

**Note:** These fields are read-only.

The following table lists the inputs for the ER case summarization skill.

<table id="table_fsq_s4h_mhc"><thead><tr><th>

Input

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Input table

</td><td>

Employee Relations Case

</td></tr><tr><td>

Input fields

</td><td>

-   Description
-   Priority
-   Short Description
-   State
-   Additional comments
-   Work notes
-   Number
-   HR service

</td></tr></tbody>
</table>## ER interview summarization skill

The ER interview summarization skill includes the inputs that identify the table and fields that are used to generate interview summary.

**Note:** These fields are read-only.

The following table lists the inputs for the ER interview summarization skill.

<table id="table_qw1_53t_g3c"><thead><tr><th>

Input

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Input table

</td><td>

Interview

</td></tr><tr><td>

Input fields

</td><td>

-   Start date
-   End date
-   Interviewee
-   Interviewee - &gt;Type
-   Interviewers
-   External attendees
-   External URL
-   Additional parties
-   Created by
-   Interview notes
-   HR case -&gt; Number
-   HR case - &gt;Short description
-   HR case -&gt; Description

</td></tr></tbody>
</table>**Parent Topic:**[Configure Now Assist for HR Service Delivery \(HRSD\)](../task/configure-now-assist-hr.md)

